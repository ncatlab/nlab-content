
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--



\tableofcontents



## Idea

*Quantum error correction* (QEC) is concerned with ensuring the robustness of [[quantum computation]] against [[noise]] (as in classical [[error correction]]) and particularly against [[quantum noise]] and [[quantum decoherence]], by *correcting computational errors as they occur* at runtime.

The need for quantum error correction is particularly urgent for the currently existing *noisy* quantum memories (cf. [NISQ](#quantum+computation#ReferencesNISQ)), which, despite their inherent instability, are widely envisioned to scale up to useful [[quantum computers]] by having them vigorously corrected by massive classical computing power; cf. discussion of the *decoding bottleneck* [below](#IdeaOfQECInPractice).

What is being corrected with QEC are [[quantum computing|quantum computations]] on a [[quantum computer]], while the correction mechanisms are classical [[computations]]: During and in parallel to the execution of the [[quantum computer]], a classical computer executes an indefinite loop which in each step:

1. reads out [[quantum measurement]] results on parts of the [[quantum memory]] (on the "syndromes"), 

2. infers from these (via a *decoding* algorithm) potential errors that may have occured in the quantum machine, 

3. [[controlled quantum gate|controls]] the quantum computer to execute [[quantum gates]] designed to counteract these errors.

Hence QEC is about a [quantum/classical interaction loop](quantum+computation#ClassicalControlQuantumData):

<center>
<div style="margin:-40px 0px 00px 0px;">
<img src="/nlab/files/QEC-interaction-loop_26-11-04.png" width="700">
</div>
</center>

It is a nontrivial and remarkable theoretical insight (involving results such as *[[quantum error threshold theorems]]*) that such a scheme can work 

* [in principle](#InTheory),

but it remains a substantial engineering challenge to also make it work

* [in practice](#InPractice).


### In principle
 {#InTheory}

From [Ferris & Poulin 2013](#FerrisPoulin13):

> The basic principle of quantum error correction (QEC) is to encode information into the long-range correlations of  [[quantum entanglement|entangled]] quantum many-body  states in  such  a  way that it  cannot be accessed locally. When a local error affects the system, it leaves a detectable imprint—called the error syndrome. The decoding problem consists  in inferring the recovery with greatest probability of success given the error syndrome.  In general, this is a hard problem, but for well-chosen codes, it can be solved efficiently either exactly or heuristically.

From [Steane 06](#Steane06):

> Error correction is especially important in quantum computers, because efficient quantum algorithms make use of large scale quantum interference, which is fragile, i.e. sensitive to imprecision in the computer and to unwanted coupling between the computer and the rest of the world. This makes large scale quantum computation so difficult as to be practically impossible unless error correction methods are used. Indeed, before quantum error correction was discovered, it seemed that this fragility would forbid large scale quantum computation. The ability to correct a quantum computer efficiently without disturbing the coherence of the computation is highly non-intuitive, and was thought more or less impossible. The discovery of powerful error correction methods therefore caused much excitement, since it converted large scale quantum computation from a practical impossibility to a possibility.

From [Devitt, Nemoto & Munro 2009](#DevittNemotoMunro09):

> Starting in 1995, several papers appeared, in rapid succession, proposing codes which were appropriate to perform error correction on quantum data ([Sho95](#Shor95); [Ste96a](#Steane96); [CS96](#CalderbankShor96);  [LMPZ96](#LMPZ96);  [BSW96](#BDSW96)). This  was a key theoretical development needed to convince the general community that quantum computation was indeed a possibility. Since this initial introduction, the progress in this field has been extensive.

From [Zhu & Cross 20](#ZhuCross20):

> Although we are currently in an era of quantum computers with tens of noisy qubits, it is likely that a decisive, practical quantum advantage can only be achieved with a scalable, fault-tolerant, error-corrected quantum computer. Therefore, development of quantum error correction is one of the central themes of the next five to ten years. 

[Lucero 21](#Lucero21): 

> Within the decade, Google aims to build a useful, error-corrected quantum computer. $[\cdots]$ Our journey to build an error-corrected quantum computer within the decade includes several scientific milestones, including building an error-corrected logical qubit.

Specifically on [[holographic tensor network|holographic quantum error correcting codes]] (see references [below](#ReferencesViaHolographicTensorNetworks)):

From [Harlow 20](#Harlow20):

> The codes provided by AdS/CFT often come close to saturating theoretical bounds on the performance of quantum codes. It seems AdS/CFT may be a tool for discovering better quantum cryptography?

[WVSB 20](#WVSB20):

> $[$ [[holographic tensor network|holographic codes]] $]$ could be promising candidates to circumvent our results and could possibly realise a universal set of unitary implementations of logical operators.


From [CDCW 21](#CDCW21):

> There are a number of reasons to suspect that [[holographic tensor network|holographic codes]] may be of practical use for quantum computing.

> Holographic codes can admit erasure thresholds comparable to that of the widely-studied surface code, and likewise for their threshold against Pauli errors.  Their holographic structure also naturally leads to an organization of encoded qubits into a hierarchy of levels of protection from errors, which could be useful for applications which call for many qubits withvarying levels of protection. In particular, this is reminiscent of many schemes for magic state distillation -- and indeed, the concatenated codes utilized for magic state distillation share a similar hierarchical structure to holographic codes. The layered structure of holographic codes is also reminiscent of memory architectures in classical computers, where it is useful to have different levels of short- and long-term memory.  Although these codes have some notable drawbacks, in particular holographic stabilizer codes require nonlocal stabilizer generators, other codes such as concatenated codes suffer similar drawbacks and have still proven to be useful. Conversely, the stringent requirement of non-local stabilizer generators allows holographic codes to protect many more qubits than a topological code and in fact attain a finite nonzero encoding rate, which is typically not possible for topological codes. Nonetheless, many open questions remain about the usefulness of holographic codes for fault-tolerant quantum computing.



#### Basic idea of QEC via the 3-qbit code
 {#BasicIdeaOfQECVia3QBitCode}

It is useful and common to illustrate the basic idea of QEC with the [3-qbit code](bit+flip+code#3QbitFlipCode), since it already showcases the key stages of (1.) *encoding*, (2) *syndrome* and (3.) *correction*. But beware that practically relevant code these days are *[[surface codes]]* which are quite different in nature, see also [below](#NestedCodesAndSurfaceCodes).
 

##### The classical case
 {#TheClassicalCase}

Before considering quantum error correction it is useful to step back and briefly reconsider the analogous case of classical error correction.

To set the stage: We regard [[bit]] values as elements of the [[cyclic group]] $\mathbb{Z}_{/2} = \{0,1\}$ of [[integers]] [[modulo]] 2. 

1. Their [[addition]] mod 2 is the *[[exclusive disjunction|exclusive or]]* ([[xor]]) of [[bits]], denoted

   $$
     \begin{aligned}
       0 \oplus 0 & = 1 \oplus 1 \,=\, 0
       \\
       0 \oplus 1 & = 1 \oplus 0 \,=\, 1
     \mathrlap{\,,}
     \end{aligned}
   $$

   so that $b \mapsto b \oplus 1$ is the flip of a bit $b$, 

1. Their [[multiplication]] mod 2 is the logical *[[conjunction|and]]*.

Now, a bit stored or transmitted in a noisy medium may get flipped with some small probability $p \in [0,1]$, and error correction is about fixing such flips. 

The simplest remedy is redundancy: encode each *logical bit* by a [[triple]] of equal *physical bits*,

\[
  \label{ClassicalTripledEncoding}
  \array{
    \mathbb{Z}_{/2} &\longrightarrow& (\mathbb{Z}_{/2})^{3}
    \\
    b &\mapsto& (b,b,b) 
    \mathrlap{\,.}
  }
\]

If at most one of the bits in $(b_1, b_2, b_3)$ gets flipped, its position in the triple is exactly determined by the following [[pair]] of  *parities*:

$$
  \begin{aligned}
    s_1 & \coloneqq  b_1 \oplus b_2
    \\
    s_2 & \coloneqq  b_2 \oplus b_3
  \,,
  \end{aligned}
$$

which vanish exactly on the codewords $(0,0,0)$ and $(1,1,1)$. This pair $(s_1,s_2)$ is hence called the *error syndrome*, since it allows to uniquely identify the position of a one-it flip error (if any), as follows:

\[
  \label{SyndromeToError}
  \begin{aligned}
    (s_1, s_2) = (0,0) 
      & \;\;\;\;\Leftrightarrow\;\;\;\; 
    \text{no error}
    \\
    (s_1, s_2) = (1,0) 
      & \;\;\;\;\Leftrightarrow\;\;\;\; 
    \text{1st bit flipped}
    \\
    (s_1, s_2) = (1,1) 
      & \;\;\;\;\Leftrightarrow\;\;\;\; 
    \text{2nd bit flipped}
    \\
    (s_1, s_2) = (0,1) 
      & \;\;\;\;\Leftrightarrow\;\;\;\; 
    \text{3rd bit flipped}
    \mathrlap{\,.}
  \end{aligned}
\]

Hence *classical error correction* in this case proceeds by:

1. **Syndrome:** Measuring the triple state and computing the error syndrome from it.

1. **Decoding:** Computing from the syndrome the apparent position of the flipped bit according to (eq:SyndromeToError).

1. **Correction:** Flipping that identified bit back.

This prodedure:

* succeeds if none or one bit flipped,

* fails if two or three bits flipped.

  Assuming that the bits flip independently of each other, this failure happens with probability

  $$
    \underset{
      \text{two flips}
    }{
    \underbrace{
      3 p^2 (1-p)
    }}
    \;+\;
    \underset{
      \text{three flips}
    }{
    \underbrace{
      p^3
    }}
    \;=\;
    3 p^2 - 2 p^3
    \,,
  $$

  where the factor of 3 counts the choices of the pair of flipped bits. Since $p - (3p^2 - 2p^3) = p(1-p)(1-2p)$, this is smaller than the error probability $p$ of an unprotected bit as long as $p \lt 1/2$.

\linebreak

A characteristic property of this classical error correction is that the error syndrome is obtained in the most direct way: by reading out, hence by *[[measurement|measuring]]*, the state of the tuple of physical bits. Classically, this does no harm, but for [[qbits]] this does not work so directly and quantum error correction needs to be a tad more clever than this.


##### The issue with the quantum case
 {#TheIssueWithTheQuantumCase}

As we pass from classical [[bits]] to [[quantum information theory|quantum]] bits, *[[qbits]]*, the information to be protected is that of a [[quantum state]] ${\vert \psi \rangle} = \alpha {\vert 0 \rangle} + \beta {\vert 1 \rangle}$ of a [[qbit]], encoded by the amplitudes $\alpha, \beta \in \mathbb{C}$. 

The classical triple encoding (eq:ClassicalTripledEncoding) [[linear span|extends linearly]] from the canonical [[linear basis]] $\big\{ {\vert 0\rangle}, {\vert 1 \rangle} \}$ to $QBit \equiv \mathbb{C}^2$:


\[
  \label{QuantumTripledEncoding}
  \begin{array}{ccc}
    \mathbb{C}^2 &\longrightarrow& 
    \big(\mathbb{C}^2\big)^{\otimes_3}
    \\
    {\vert \psi \rangle}
    &\mapsto&
    {\vert \psi_L \rangle}
    \\
    \alpha {\vert 0\rangle} + \beta {\vert 1 \rangle}
    &\mapsto&
    \alpha {\vert 000 \rangle} + \beta {\vert 111 \rangle}
    \,.
  \end{array}
\]

In terms of [[quantum circuits]] this operation (eq:QuantumTripledEncoding) may be implemented by ${\vert \psi\rangle} \mapsto {\vert \psi \rangle} \otimes {\vert 00 \rangle}$ followed by two [[CNOT gates]] (see [below](#TheProperQuantumCase)). 


> This (eq:QuantumTripledEncoding) is a copying operation, namely of the computational [[linear basis|basis]] states. The *[[no-cloning theorem]]* only rules out that copying be [[natural transformation|natural]] (in particular: independent of the choice of basis), which would instead send general ${\vert \psi \rangle}$ to ${\vert \psi \rangle}^{\otimes 3}$.

A flip of the $i$th qbit now acts as the [[Pauli operator]] $X_i$, hence as

$$
  X
  \;\coloneqq\;
  \left(
    \array{
      0 & 1
      \\
      1 & 0
    }
  \right)
  \,,
  \qquad
  X {\vert b \rangle} \,=\, {\vert b \oplus 1 \rangle}
$$

on the $i$th tensor factor and as the identity on the others (with $X_0 \coloneqq 1$ for the error-free case). For example:

$$
  X_2 {\vert \psi_L \rangle}
  \;=\;
  \alpha {\vert 010 \rangle} + \beta {\vert 101 \rangle}
  \,.
$$

Now, applying the classical strategy [above](#TheClassicalCase) verbatim would mean [[quantum measurement|measuring]] the three qbits in the computational basis. While this would reveal the syndrome, already the first measurement would [[collapse of the wavefunction|collapses]] the [[quantum state]] onto one of its two branches (here ${\vert 010 \rangle}$ or ${\vert 101 \rangle}$, with [[Born rule]] [[probability]] ${\vert \alpha \vert}^2$ or ${\vert \beta \vert}^2$, respectively). This would serve to diagnose the error, but would itself destroy the quantum state completely: the amplitudes $\alpha, \beta$ (the very data to be protected) would be lost.

Notice, however, that the syndrome takes the same value on both branches (here $(s_1, s_2) = (1,1)$ for ${\vert 010 \rangle}$ as well as for ${\vert 101 \rangle}$). 

To turn this into a [[quantum observable]], consider the [[Pauli operator]]

$$
  Z
  \;\coloneqq\;
  \left(
    \array{
      1 & 0
      \\
      0 & -1
    }
  \right)
  \,,
  \qquad
  Z {\vert b \rangle} \,=\, (-1)^b {\vert b \rangle}
  \,,
$$

with which the syndrome appears as 

$$
  \begin{aligned}
    Z_1 Z_2 {\vert b_1 b_2 b_3 \rangle} 
      & = 
    (-1)^{b_1 \oplus b_2} {\vert b_1 b_2 b_3 \rangle}
   \\
    Z_2 Z_2 {\vert b_1 b_2 b_3 \rangle} 
      & = 
    (-1)^{b_2 \oplus b_3} {\vert b_1 b_2 b_3 \rangle}
    \mathrlap{\,.}
  \end{aligned}
$$ 

This means that each $X_i {\vert \psi_L \rangle}$ is a joint [[eigenstate]] of the syndrome *parity observables* $Z_1 Z_2$ and $Z_2 Z_3$, with [[eigenvalues]] $(-1)^{s_1}$ and $(-1)^{s_2}$, respectively. 

Hence while the individual physical bits must not be measured, their parities may.

This motivates adjoining auxiliary *ancilla* [[qbits]] onto which the parities are imprinted by unitary gates. A [[quantum measurement]] of just the ancillas is then a measurement on the total system which reveals the syndrome without collapsing the encoded state.


##### The proper quantum case
 {#TheProperQuantumCase}

Concretely, consider adjoining to the logical [[Hilbert space]] $\big(\mathbb{C}^2\big)^3$ two ancilla qbits, hence pass to 

$$
  \mathscr{H}
  \coloneqq
  \big(\mathbb{C}^2\big)^3 
    \otimes 
  \underbrace{ 
    \big(\mathbb{C}^2\big)^2
  }_{\text{ancillary}}
$$ 

and consider on this the *imprint* [[unitary operator]]

\[
  \label{TheImprintingOperator}
  \begin{array}{ccc}
  \mathscr{H} &\overset{I}{\longrightarrow}& \mathscr{H}
  \\
  {\vert b_1 b_2 b_3 \rangle} 
    \otimes 
  {\vert a_1 a_2 \rangle}
    &\mapsto&
  {\vert b_1 b_2 b_3 \rangle} 
    \otimes 
  {\vert a_1 \oplus b_1 \oplus b_2 ,\, a_2 \oplus b_2 \oplus b_3 \rangle}
  \end{array}
\]

(a [[permutation]] of the computational [[linear basis|basis]], implementable by four [[CNOT gates]]), which imprints the parities of the code qbits onto ancillas initialized in ${\vert 00 \rangle}$.

Suppose that the code state has suffered at most one bit flip, so that it is $X_i {\vert \psi_L \rangle}$ for some *unknown* $i \in \{0,1,2,3\}$. Since the parities agree on both branches of $X_i {\vert \psi_L \rangle}$, we have

$$
  I\left( X_i {\vert \psi_L \rangle} \otimes {\vert 00 \rangle} \right)
  \;=\;
  X_i {\vert \psi_L \rangle} \otimes {\vert s_1 s_2 \rangle}
  \,,
$$

where $(s_1, s_2)$ is the syndrome of the error $X_i$ in that $i$ may be computed from it (eq:SyndromeToError).


Error correction now proceeds in three steps analogous to the classical case [above](#TheClassicalCase), but replacing code bit measurement by ancilla qbit [[quantum measurement]]:

1. **Syndrome:** Since on the right of (eq:TheImprintingOperator) we have a product state, measuring only the ancillas yields the syndrome $(s_1, s_2)$ with certainty, while leaving the code qbits in $X_i {\vert \psi_L \rangle}$, [[collapse of the wavefunction|uncollapsed]].

1. **Decoding:** From the syndrome, a classical algorithm, the *decoder*, determines $i$, here via the [above](#TheClassicalCase)) syndrome table (eq:SyndromeToError), and thereby *chooses* the correcting [[quantum gate]] $X_i$.

1. *Correction:* Applying the chosen correction [[quantum gate]], which restores the code state in case of at most one bit flip error: $X_i X_i {\vert \psi_L \rangle} = {\vert \psi_L \rangle}$, since $X X = 1$.


This is the *3-qbit bit flip code*. Its full [[quantum circuit]] reads as follows: encoding, error, syndrome extraction by $I$, measurement, decoding and correction:

\linebreak

\linebreak

\[
  \label{3QBItQECcircuit} 
\]

<center>
<div style="margin:-100px 0px 00px 0px;">
<img src="/nlab/files/3QBit-QEC-circuit_26-11-04.png" width="700">
</div>
</center>

(The final [[quantum gates|gates]] are [[classically controlled quantum gate|classically controlled]] (double lines) by the [[quantum measurement]] outcomes.)

It should be noted here that the quantum correction mechanism (eq:3QBItQECcircuit) is itself nothing but a [[quantum circuit]], hence, when physically executed, is *itself subject to quantum errors*. This is a problem that is solved *in principle* by the [[quantum error threshold theorems]], but *in practice* it makes this and similar codes actually unusable, see the discussion of *Nested codes and Surface codes* [below](#NestedCodesAndSurfaceCodes).


##### Refinements
 {#Refinements}

The [above](#TheProperQuantumCase) [[bit flip code]] does not protect against *phase flips* as reflected by the [[Pauli operator]] $Z_i$. These send ${\vert \psi_L \rangle}$ to $\alpha {\vert 000 \rangle} - \beta {\vert 111 \rangle}$, which is again a code state and hence has trivial syndrome under the [above](#TheProperQuantumCase) code: the error goes undetected and corrupts the logical state.

But since the [[Hadamard gate]]

$$
  H
  \;\coloneqq\;
  \frac{1}{\sqrt{2}}
  \left(
    \array{
      1 & 1
      \\
      1 & -1
    }
  \right)
$$

exchanges bit and phase flips, $H X H = Z$, the same scheme may be run in the Hadamard-transformed basis ${\vert {\pm} \rangle} \coloneqq H {\vert 0/1 \rangle} = \frac{1}{\sqrt{2}} \left( {\vert 0 \rangle} \pm {\vert 1 \rangle} \right)$. Hence the encoding

$$
  \begin{aligned}
    {\vert 0 \rangle} 
      & \mapsto
    {\vert {+}{+}{+} \rangle}
    \\
    {\vert 1 \rangle} 
      & \mapsto 
   {\vert {-}{-}{-} \rangle}
  \end{aligned}
$$

gives the "3-qbit *phase flip* code", with syndrome given by the parity observables $X_1 X_2$ and $X_2 X_3$. It corrects any single phase flip, but now not bit flips.

Nesting the two codes, by encoding each of the three qbits of the phase flip code via the bit flip code, yields *Shor's 9-qbit code*:

$$
  \begin{aligned}
  {\vert 0 \rangle}
    & \mapsto
  \frac{1}{2\sqrt{2}}
  \left( 
    {\vert 000 \rangle} + {\vert 111 \rangle}
  \right)^{\otimes 3}
  \\
  {\vert 1 \rangle}
    & \mapsto
  \frac{1}{2\sqrt{2}}
  \left( 
    {\vert 000 \rangle} - {\vert 111 \rangle} 
  \right)^{\otimes 3}
  \mathrlap{\,.}
  \end{aligned}
$$

This corrects bit flips, phase flips and their composites $X_i Z_i$ on any single qbit. In fact this suffices to correct *arbitrary* errors on a single qbit. Every operator on a qbit is a linear combination of $1$, $X$, $Z$ and $X Z$, and the syndrome measurement collapses such a superposition of errors onto one of its components, which is then corrected as before.

All of these are examples of *[[stabilizer codes]]*: the code space is the joint $(+1)$-eigenspace of a commuting set of products of Pauli operators (for the bit flip code: $Z_1 Z_2$ and $Z_2 Z_3$), whose measurement via ancillas yields the error syndrome.






#### General QEC codes

The simple but important special case of passive correction of erasures may be  handled by *[[quantum error correcting codes]]*:

Recall that a classical [[error correcting code]] on a [[finite set]] of states $L$ is, typically, a choice of [[injection]] of $L$ into some larger [[finite set]], typically a [[Cartesian power]] 

$$
  L 
    \overset{code}{\hookrightarrow} 
  P 
    \coloneqq 
  H \times \cdots \times H
$$

(often considered in the form of [[linear codes]], but [[classical physics|classical]] nonetheless). In [[quantum physics]] the [[Cartesian product]] of sets of states is replaced by the [[tensor product of vector spaces|tensor product]] of [[Hilbert spaces]].

For $\mathcal{L}$ a given [[Hilbert space]] of [[quantum states]] ([[finite dimensional vector space|finite-dimensional]] in practice), a *quantum error correcting code* is a choice of [[linear subspace|linear embedding]] (the *code subspace*) of $\mathcal{L}$ into a larger Hilbert spaces, often an  $n$-fold [[tensor product]] of copies of some $\mathcal{H}$:

$$
  \array{
    \underset{
     {\color{blue}logical}
     \atop
     {\color{blue}qbits}
    }{
      \mathcal{L}
    }
    & 
      \underoverset
        {{\color{blue}code} \atop {\color{blue} subspace}}
        {\;\;\;code\;\;\;}
        {
        \hookrightarrow
      }
    &
    \mathcal{P}
    \coloneqq
    \underset{
      \color{blue}
      physical\;qbits
    }{
    \mathcal{H}^{(1)} 
      \otimes
        \cdots
      \otimes
    \mathcal{H}^{(n)}  
    }
  }
  \,,
$$

such that the information in $code(\psi)$ in some of the tensor factors $\mathcal{H}^{(i)}$ can be lost without obstructing the reconstruction of $\psi$ (cf. [Rowell & Wang 17, Sec. 3.2.3](#RowellWang17)).

(Often one demands additional properties, such as that a given set of [[linear operators]] $O$ ([[quantum observables]]) acting on $\psi \in \mathcal{H}$ are implemented on $code(\psi)$ by combinations of operators that act non-trivially only on some of the tensor factors.)

While this is superficially analogous to a classical [[error correcting code]], the crucial and subtle difference is that quantum error correction codes thus take place in a non-[[cartesian monoidal category|Cartesian]] [[symmetric monoidal category|symmetric]] [[monoidal category]]. For this reason, effects of [[quantum entanglement]] play a paramount role in quantum error correction codes.













### In practice 
 {#InPractice}

While the [[quantum error threshold theorem]] shows that quantum error correction of noisy [[quantum circuits]] is possible *in principle*, the practice of QEC *at scale* remains a major engineering challenge.


#### The decoding bottleneck
 {#IdeaOfQECInPractice}

As of the 2020s, [[quantum error correction]] (QEC) applied to noisy intermediate-scale quantum ([NISQ](quantum+computation#ReferencesNISQ)) machines is the dominant strategy paradigm, in both academia and industry, for potentially achieving [[quantum advantage|meaningful]] [[quantum computation]] in the future. 

But in technical discussions, the physical reality of the "endgame" of this approach may be easily missed by outsiders: Even in optimistic scenarios where theoretical error thresholds are achieved, the NISQ+QEC roadmap requires envisioning a staggering future feat of quantum and classical hardware engineering, haunted by intrinsic design tensions.

Namely, the [[quantum error correction|quantum error-correcting]] mechanism required to run a useful, large-scale application on currently available [[qubit]] technology --- such as [[Shor's algorithm]] (e.g. for cracking RSA-2048 [[cryptography|encryption]]) will involve an astronomical rate of [[data analysis|data processing]]. To maintain the logical [[quantum state]], the auxiliary classical system must measure millions of physical [[qubits]] every microsecond, exchanging hundreds of terabytes of error "syndrome" data per second between the quantum device and its classical controller (cf. [riverlane 2025](#Riverlane2025)). This is a data rate of the order of the global internet traffic! Decoding this torrent of data in real-time requires an amount of classical computational power that exceeds the capabilities of contemporary, building-sized exascale supercomputers (cf. [Waintal 2024](#Waintal24)). 

Even if such classical computing power is or were available, standard data cables connecting the quantum chip to an external supercomputer would introduce signal latency exceeding the coherence time of current qubits, rendering the correction commands obsolete upon arrival. Furthermore, the sheer volume of data transfer will or would transmit enormous amounts of thermal noise from the outside world into the quantum machine, jeopardizing its near-zero cooling and its [[quantum coherence]].

This problem is also known as the *decoding bottleneck* or *decoder bottleneck* (cf. [Mishan 2025](#Mishan2025), [Croot et al. 2025](#CrootEtAl2025), [Ivezic 2026](#Ivezic2026), [Mahmud at al. 2026](#MahmudEtAl2026), [Canton 2026](#Canton2026)).

To overcome this formidable scenario, the NISQ+QEC field has now turned to speculating on future classical hardware technology where *Application Specific Integrated Circuit* ([ASICs](https://technav.ieee.org/topic/application-specific-integrated-circuits/)) hardware is integrated directly into the ultra-cooled quantum refrigerator (e.g., via specialized "Cryo-CMOS" logic; cf. [Erol 2026](#Erol2026)).  However, this poses severe thermodynamic contradictions: Standard silicon transistors suffer from carrier freeze-out below $\sim 40K$, whence one needs to envision an entire *new kind of classical computing hardware*. More generally, the cooling power at the base of a dilution refrigerator is strictly limited to a few micro-Watts. Therefore, placing a petaflop ASIC chip in near proximity to the quantum device would produce excess heat that under currently understood conditions would destroy the cryogenic environment that the quantum computer relies on.

<center>
<div style="margin:-30px 0px 00px 0px;">
<img src="/nlab/files/QDecodingBottleneck-Cartoon_26-11-04.jpg" width="700"/>
</div>
<small>
  Error correcting a reasonably powerful but noisy quantum computer will require novel classical supercomputers operating, partially, in currently unachieved cryogenic temperature regimes. [graphics from <a href="https://ncatlab.org/schreiber/show/WIKO+2026">Schreiber 2026</a>]
</small>
</center>

In conclusion, the NISQ+QEC roadmap for achieving meaningful commercial value quantum computers is now tacitly banking on unheard of and intrinsically dubious future progress in *classical supercomputing* technology --- which, assuming it can be brought into existence, would then not be used for contentful computation itself, but would solely serve the task of preventing the memory of a quantum computer from decaying.


<center>
<div style="margin:-0px 0px 00px 0px;">
<img src="/nlab/files/QEC-Buckets_26-11-04b.png" width="700">
</div>
<small>
Noisy qbits are like water in a leaky bucket. In this analogy, (1.) <i>quantum error correction</i> is like continuously catching the leaking water and rapidly filling it back into the bucket, (2.) the <i>decoding bottleneck</i> is the intense amount of auxiliary  machinery and effort of pumping this requires, (3.) hardware-level <i>topological quantum</i> protection is the patching of the buckets. [graphics from <a href="https://ncatlab.org/schreiber/show/WIKO+2026">Schreiber 2026</a>]
</small>
</center>



#### Aside: Hardware-level protection

The initial problem at the base of the decoding bottlenck problem [above](#IdeaOfQECInPractice) is the instability of current qubit technology (*NISQ*, see [there](quantum+computation#ReferencesNISQ)). 

The problem is akin to that of a bucket brigade which operates with extremely leaky buckets. In this picture, the QEC-style solution is like using ever more buckets together with sophisticated machinery that cleverly catches the leaked water only to fill it back into the buckets. 

This analogy makes clear that an alternative strategy may be to actually fix the buckets. On the quantum technology side this corresponds to the approach of [[topological quantum computing]] (cf. [Das Sarma 2022](#DasSarma22)), where it is not runtime software redundancy that stabilizes shaky qubits, but intrinsic physical effects in [[topological order|topological]] [[quantum materials|quantum hardware]]. 


However, while such topological stabilization of quantum states and topological protection of quantum gates exists in theory (and even that theory is not well developed at this point) essentially no experience with practical engineering implementation exists to date. 


#### Nested codes and Surface codes
 {#NestedCodesAndSurfaceCodes}

An intrinsic practical problem with QEC implemented via [[quantum circuits]] as in the simple 3-qbit code example (eq:3QBItQECcircuit) [above](#BasicIdeaOfQECVia3QBitCode) is that these quantum circuits are *themselves* subject to errors, needing *themselves* another layer of QEC, and so on. This may appear to already lead to an infinite regression problem. Remarkably, the *[[quantum error threshold theorem]]* says that, in principle, a *finite* depth of nested codes is sufficient for breaking even if the baseline physical error rate $p$ is below some threshold (whence the name). 

However, nested codes require non-local [[qbit]] connectivity on the quantum hardware, which becomes quickly technologically unachievable. For this reason, the nested codes that the theory of the threshold theorem considers are actually useless in practice.

For this reason the community has turned instead to *[[surface codes]]*. These mimic ("[[quantum simulation|simulate]]") [[topological quantum computing|topological]] mechanisms of error protection by a lattice of qbits using only local connectivity. 

While surface codes solve the non-locality of nested codes, this comes at the cost that they correct errors only in [[Clifford gates]], which are not sufficient for universal quantum computation, leaving non-Clifford gates like [[T-gates]] unprotected (see [below](#TGatesAndMagicStates)).


#### Magic state factories
 {#TGatesAndMagicStates}

The decoding bottleneck ([above](#IdeaOfQECInPractice)) is only part of the problem of practically implementing QEC at scale. 

Namely, with the currently most popular error correcting codes, which are *[[surface codes]]* ([above](#NestedCodesAndSurfaceCodes)), it is only *[[Clifford gates]]* that are error protected (after solving the decoding bottleneck), while [universal quantum computing](quantum+logic+gate#UniversalGateSets) requires further gate type (such as the [[T-gate]]) that remain uncorrected by [[surface codes]].

The now standard strategy to work around this problem, trades the missing gate for a resource [[quantum state]]: [[T-gates]] are enacted by *gate teleportation*, consuming *[[magic states]]* ${\vert A \rangle} = T {\vert + \rangle}$ via a [[CNOT gate|CNOT]], a [[Pauli gate|$Z$-]][[quantum measurement|measurement]] and a [[controlled quantum gate|classically controlled]] $S$-correction (which are all Clifford operations). 

This leads to the further practical problem of equipping the quantum computer with a good supply of [[magic states]], which has become a research field all in itself: "*magic state factories*". Current estimates are that "magic state distillation" alone will occupy about 90% of the quantum chip, leaving 10% for actual computation, and that this creates a bottleneck on top of and dwarfing the error correction bottlenect (cf. [NKM 2026](#NKM2026)).


#### Summary and outlook
 {#QECPracticalChallengesSummaryAndOutlook}

<center>
<div style="margin:-20px 0px 00px 0px;">
<img src="/nlab/files/bump-in-the-QEC-carpet_26-11-05d.png" width="820">
</div>
<small>
  <b>Pushing the bump in the carpet around.</b> The strategy of quantum error correction at scale has led to a cascade of subsequent technological problems. The currently dominant strategy for QEC at useful scale is now betting on future advances in <i>classical</i> supercomputer technology, in order to handle the decoding bottleneck and the magic state factory bottleneck of classical compute needed for fixing surface codes, which in turn were introduced to solve the impractical qbit non-locality of QEC.
</small>
</center>


#### References: Practical challenges of QEC

More on the [above](#InPractice) discussion of practical QEC challenges may be found in the following references, with some quotes highlighted:

* {#DasSarma22} [[Sankar Das Sarma]]: *Quantum computing has a hype problem*, [MIT Technology Review (March 2022)](https://www.technologyreview.com/2022/03/28/1048355/quantum-computing-has-a-hype-problem/)
  > "The qubit systems we have today are a tremendous scientific achievement, but they take us no closer to having a quantum computer that can solve a problem that anybody cares about. \[...\] What is missing is the breakthrough \[...\] bypassing [[quantum error correction]] by using far-more-stable qubits, in an approach called topological quantum computing."

* Francesco Battistel et al.: *Real-Time Decoding for Fault-Tolerant Quantum Computing: Progress, Challenges and Outlook*, Nano Futures **7** 032003 (2023) &lbrack;[arXiv:2303.00054](https://arxiv.org/abs/2303.00054), [doi:10.1088/2399-1984/aceba6](https://doi.org/10.1088/2399-1984/aceba6)&rbrack;

* {#Waintal24} Xavier Waintal: *The Quantum House Of Cards*, PNAS **121** 1 (2024) e2313269120 \[<a href="https://doi.org/10.1073/pnas.2313269120">doi:10.1073/pnas.2313269120</a>, [arXiv:2312.17570](https://arxiv.org/abs/2312.17570)\]

* {#Mishan2025} Lior Mishan: *[Scalable Quantum Error Correction: Breaking Bottlenecks in Quantum Computing](https://www.quantum-machines.co/scalable-quantum-error-correction/)*, Quantum Machine Blog (June 2025)

* {#riverlane2025} [riverlane](https://www.riverlane.com/): *[Quantum Error Correction](https://www.riverlane.com/quantum-error-correction)* (2025)

* {#Erol2026} Volkan Erol: *[Quantum Computing is No Longer a Physics Problem. It is a Systems Engineering Nightmare](https://volkan-erol.medium.com/quantum-computing-is-no-longer-a-physics-problem-it-is-a-systems-engineering-nightmare-a1ecba474ecb)*, Medium (Jan 2026) &lbrack;[[Erol2026-QECProblem.pdf:file]]&rbrack;

* {#CrootEtAl2025} X. Croot et al.: *Enabling Technologies for Scalable Superconducting Quantum Computing* \[<a href="https://arxiv.org/abs/2512.15001">arXiv:2512.15001 quant-ph</a>\]
  > "The i/o of signal between qubit and control electronics is a central bottleneck to scaling. \[...\] Many proposals for long-term fault-tolerant quantum computing require qubit numbers that are orders of magnitude greater than the capacity of available fridges, even when accounting for densification of components and reduction of thermal loads per qubit. \[...\] The qubit overheads for the best FT-QEC schemes are daunting, and the implementation of decoding on the time-scale of the quantum gates (clock cycle) remains an open challenge in many leading hardware platforms. \[...\] Systems of 100k qubits would demand large fractions of the yearly world production \[of Helium\] based on naive linear scaling."

* {#Ivezic2026} Marin Ivezic: *[The Decoder Bottleneck: The CRQC Challenge Nobody Is Talking About](https://postquantum.com/quantum-computing/decoder-bottleneck-crqc/)*, PostQuantum (April 2026)
  > "**The Capability Nobody Mentioned** \[...\] The decoder is the classical computer sitting next to the quantum processor, receiving a continuous stream of error syndrome measurements and determining, in real time, what corrections to apply. \[...\] Without a decoder that can keep pace with the quantum hardware, quantum error correction is an offline statistical exercise, not a fault-tolerant computation. A million qubits without a real-time decoder is a million qubits that cannot compute.

  > This is the capability dimension that \[...\] is most likely to determine whether a cryptographically relevant quantum computer (CRQC) arrives in 2030 or 2045. It is the classical engineering challenge hiding inside the quantum machine, the piece that connects the quantum physics to the classical computation, and the capability that most threat assessments ignore entirely.

  > The quantum computing field has trained the public, and by extension the security community, to track one number: how many qubits. Security professionals need a more sophisticated model. 

  > If the decoder cannot keep up with the syndrome stream, a backlog forms. \[...\] The backlog grows exponentially, and eventually the computation fails. This is the “backlog problem,” and it is the reason that decoder speed is not a performance optimization but a hard requirement. A decoder that is 10% too slow does not produce a 10% slower computation. It produces a computation that fails entirely.

  > The decoder must satisfy three simultaneous requirements. \[...\] Speed, accuracy, and scale. Getting any two of three is tractable. Getting all three simultaneously is the unsolved engineering problem at the center of the CRQC timeline.

  > &lbrack;...&rbrack; **Decoding Is Harder Than It Sounds**

  > &lbrack;For [superconducting qbits](superconducting+qbits+--+references)&rbrack; the decoder must complete its work within that microsecond to avoid backlog. This is the most demanding timing constraint in the quantum computing stack, and it is why [FPGA](https://en.wikipedia.org/wiki/Field-programmable_gate_array) and [ASIC](https://technav.ieee.org/topic/application-specific-integrated-circuits/) implementations are necessary: software decoders running on conventional CPUs cannot reliably meet microsecond deadlines for codes at the distances required for cryptographic applications. The superconducting decoder challenge is fundamentally a hardware problem. The algorithm must be compiled into dedicated circuitry ([FPGA](https://en.wikipedia.org/wiki/Field-programmable_gate_array) or [ASIC](https://technav.ieee.org/topic/application-specific-integrated-circuits/)) that executes in deterministic time, without the variable-latency interrupts, cache misses, and scheduling jitter that make general-purpose CPUs unsuitable for hard real-time constraints.

  > &lbrack;...&rbrack; The gap between current decoder demonstrations and CRQC requirements is large and precisely quantifiable. \[...\] The progress curve is steep. But the destination \[...\] remains far ahead."


* {#NKM2026} Kris Naudts, Zeynep Koruturk, Donald Harmitt: *[The Quantum Bottleneck Isn't Error Correction, It's the Magic State Factory](https://firgun.vc/insights/quantum-bottleneck-magic-state-factory)*, Firgun Ventures Insight (July 2026)

* {#MahmudEtAl2026} Mahmud et al.: *Decoder Architectures and Computational Bottlenecks in QEC*: section IV of: *Quantum Error Correction Survey*,  IEEE Access **14** (Sep 2026) 154233--154277 &lbrack;[doi:10.1109/ACCESS.2026.3737721](https://doi.org/10.1109/ACCESS.2026.3737721)&rbrack;

* {#Canton2026} Manuel Esparcia Cantos: *[Decoders: The Quiet Bottleneck of Quantum Error Correction](https://www.linkedin.com/pulse/decoders-quiet-bottleneck-quantum-error-correction-esparcia-cantos-er0ve)*, LinkedIn (8. Oct 2026)
  > "&lbrack;Quantum error&rbrack; correction is a hard computational problem that has to be solved by a classical computer, in real time, faster than the quantum computer produces the next round of errors. This is the decoder, and it is one of the field's quietest and most underappreciated bottlenecks.

  > This article is about the problem almost no popular account mentions. Everyone talks about qubits and codes; far fewer talk about the classical machine that has to keep up with them. Yet a fault-tolerant quantum computer is impossible without a decoder that is simultaneously accurate enough to correct the errors and fast enough to do it before the backlog explodes.

  > &lbrack;...&rbrack;  In a superconducting machine, a new round of syndrome data arrives roughly every microsecond. If the decoder cannot keep pace, unprocessed syndromes pile up faster than they are cleared, a backlog that grows without bound and eventually makes the computation impossible. This is the decoding bottleneck, and it is as real an obstacle to fault tolerance as qubit quality.

  > &lbrack;...&rbrack; **WHY DECODERS DESERVE MORE ATTENTION**

  > The decoder is where a beautiful theory meets an unforgiving stopwatch. All the elegance of stabilizer codes and the guarantee of the threshold theorem assume, quietly, that a decoder exists which is accurate enough and fast enough. That assumption is doing enormous work. A code below threshold with a decoder too slow to keep up is not fault-tolerant in practice, no matter how good the qubits are. The classical co-processor is not a footnote to the quantum computer; it is part of the quantum computer.

  > &lbrack;...&rbrack; There is a genuine tension the field has not fully resolved: the most accurate decoders tend to be the slowest, and the fastest tend to be less accurate. The whole game is beating that trade-off, and the platform that first fields a decoder both accurate enough and fast enough at scale removes one of the last quiet obstacles between below-threshold hardware and a working machine."

\linebreak

## Examples

### Specific examples

#### Bit flip codes

See at *[[bit flip code]]*, and the exposition of the 3-qbit code [above](#BasicIdeaOfQECVia3QBitCode).

#### A 3-qutrit code
 {#A3FoldqtritCode}

The following is a simple illustrative example from [Cleve, Gottesman & Lo 99, p. 1-2](#CleveGottesmanLo99):

Consider a [[quantum system]] with a 3-dimensional [[space of quantum states]]:

$$
  \mathcal{H} 
    \;\coloneqq\; 
  \mathbb{C}^3 
    \;=\; 
  Span\big( 
    \left\vert 0 \right\rangle,\,
    \left\vert 1 \right\rangle,\,
    \left\vert 2 \right\rangle
  \big)
$$

and consider a code space inside 3 copies of this space given by the following [[linear map]]

$$
  \array{
    \mathcal{H}
    &
    \overset{
      \phantom{AAAA}
      code
      \phantom{AAAA}
    }{\longrightarrow}&
    \mathcal{H}^{\otimes 3}
    \\
    \array{
      & \alpha \left\vert 0 \right\rangle
      \\
      + & \beta \left\vert 1 \right\rangle
      \\
      + & \gamma \left\vert 2 \right\rangle
    }
    &
      \mapsto
    &
    \array{
      & \alpha 
        \tfrac{1}{\sqrt{3}}
        \big( 
          \left\vert 000 \right\rangle 
          +
          \left\vert 111 \right\rangle 
          +
          \left\vert 222 \right\rangle 
        \big)
      \\
      + & \beta
        \tfrac{1}{\sqrt{3}}
        \big( 
          \left\vert 012 \right\rangle 
          +
          \left\vert 120 \right\rangle 
          +
          \left\vert 201 \right\rangle 
        \big)
      \\
      + & \gamma 
        \tfrac{1}{\sqrt{3}}
        \big( 
          \left\vert 021 \right\rangle 
          +
          \left\vert 102 \right\rangle 
          +
          \left\vert 210 \right\rangle 
        \big)
    }
  }
$$

This code corrects errors consisting of the loss of one of the three copies, in the following sense:

There is a [[linear operator]] acting only on two of the three copies, explicitly given ([ADH 14 (3.6)](#ADH14)) by

$$
  \array{
    \mathcal{H} \otimes \mathcal{H}
    &
    \overset{
      \;\;\;\;\;\;
      U^{(12)}
      \;\;\;\;\;\;
    }{\longrightarrow}
    &
    \mathcal{H} \otimes \mathcal{H}
    \\
    \left\vert 00 \right\rangle &\mapsto& \left\vert 00 \right\rangle
    \\
    \left\vert 01 \right\rangle &\mapsto& \left\vert 12 \right\rangle
    \\
    \left\vert 02 \right\rangle &\mapsto& \left\vert 21 \right\rangle
    \\
    \left\vert 10 \right\rangle &\mapsto& \left\vert 22 \right\rangle
    \\
    \left\vert 11 \right\rangle &\mapsto& \left\vert 01 \right\rangle
    \\
    \left\vert 12 \right\rangle &\mapsto& \left\vert 10 \right\rangle
    \\
    \left\vert 20 \right\rangle &\mapsto& \left\vert 11 \right\rangle
    \\
    \left\vert 21 \right\rangle &\mapsto& \left\vert 20 \right\rangle
    \\
    \left\vert 22 \right\rangle &\mapsto& \left\vert 02 \right\rangle
  }
$$

such that

$$
  \big( U^{(12)} \otimes id^{(3)} \big)
  \circ
  code
  \big(
    \left\vert \psi \right\rangle
  \big)
  \;\; = \;\;
  \left\vert \psi \right\rangle
  \,
  \otimes  
  \,
  \tfrac{1}{\sqrt{3}}
  \left(
    \left\vert 00 \right\rangle
    +
    \left\vert 11 \right\rangle
    +
    \left\vert 22 \right\rangle
  \right)
$$

#### The HaPPY code

The [[HaPPY code]] is a [[quantum error correction code]] (a class of such codes really, indexed by a "cutoff" [[natural number]]) which is thought to exhibit characteristic properties akin to the encoding of [[bulk]]-[[quantum states]] by [[boundary field theory|boundary]]-states expected in the [[AdS/CFT correspondence]]. In particular, the HaPPY code (or rather the [[tensor network]] that defines it) exhibits a discretized form of the [[Ryu-Takayanagi formula]] for [[holographic entanglement entropy]].

Concretely, the the HaPPY [[code subspace]] is the [[image]] of the [[linear map]] formed by:


\begin{imagefromfile}
    "file_name": "HaPPYCodeTesselation.jpg",
    "float": "right",
    "width": 440,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Harlow 18](#Harlow18)"
\end{imagefromfile}

1. picking a [[perfect tensor]] $T$ of [[rank]] 6;

1. picking a finite cutoff of the [[pentagon|pentagonal]] [[tesselation]] of the [[hyperbolic plane]];

1. regarding its [[Poincaré duality|Poincaré dual]] [[graph]] as a [[tensor network]] ([[string diagram]] in [[finite-dimensional vector spaces]]) by 

   1. assigning $T$ to each [[vertex]] at the center of the [[pentagons]] (show in blue), with 5 of its indices contracted with its neighbours in the hyperbolic plane,

   1. and its 6th uncontracted index remaining as an input (shown in red);

1. regarding the uncontracted edges at the cutoff boundary as output (shown in white)

and thus as a [[linear map]] from the [[tensor product]] over the [[bulk]]-[[vertices]] to the [[tensor product]] over the edges sticking out over the boundary.

#### Majorana dimer codes

See at *[[Majorana dimer code]]*.

### Classes of examples

* [[bit flip code]]

* [[Æ codes]]

* [[stabilizer code]]

  * [[HaPPY code]]

  * [[Majorana dimer code]]

* [[toric code]]

## Related concepts

* [[error correcting code]], [[surface code]]

* [[error threshold theorem]]

* [[dynamic lifting]]

* [[repeat-until-success computing]]

* [[quantum entanglement]]

* [[entanglement entropy]], [[holographic entanglement entropy]]

* [[quantum computing]], [[topological quantum computing]]

* [[quantum secret sharing]]

* [[tensor network]]

* [[quantum relation]]

## References

### General

The idea of quantum encryption based on the [[no-cloning theorem]] originates with:

* [[Stephen Wiesner]], *Conjugate Coding*, circulated in the 1960s, finally published in ACM SIGACT News **15** 1 (1983) 78–88 ([original pdf](http://users.cms.caltech.edu/~vidick/teaching/120_qcrypto/wiesner.pdf), [doi:10.1145/1008908.1008920](https://doi.org/10.1145/1008908.1008920))

Original articles on quantum error correcting codes:

* {#Shor95} [[Peter W. Shor]], *Scheme for reducing decoherence in quantum computer memory*, Phys. Rev. A 52, R2493(R) 1995 ([doi:10.1103/PhysRevA.52.R2493](https://doi.org/10.1103/PhysRevA.52.R2493))

* {#Steane96} [[Andrew M. Steane]], *Error Correcting Codes in Quantum Theory*, Phys. Rev. Lett. 77, 793 1996 ([doi:10.1103/PhysRevLett.77.793](https://doi.org/10.1103/PhysRevLett.77.793))

* {#CalderbankShor96} [[Robert Calderbank]], [[Peter W. Shor]], *Good Quantum Error-Correcting Codes Exist*, Phys. Rev. A, Vol. 54, No. 2, pp. 1098-1106, 1996 ([doi:10.1103/PhysRevA.54.1098](https://doi.org/10.1103/PhysRevA.54.1098))

* {#LMPZ96} [[Raymond Laflamme]], Cesar Miquel, Juan Pablo Paz, [[Wojciech H. Zurek]], *Perfect Quantum Error Correction Code*, Phys. Rev. Lett., 77:198, 1996 ([arXiv:quant-ph/9602019](https://arxiv.org/abs/quant-ph/9602019))

* {#BDSW96} Charles H. Bennett, David P. DiVincenzo, John A. Smolin, William K. Wootters, *Mixed State Entanglement and Quantum Error Correction*, Phys. Rev. A54:3824-3851, 1996 ([doi:10.1103/PhysRevA.54.3824](https://doi.org/10.1103/PhysRevA.54.3824))

* [[Andrew M. Steane]], *Multiple Particle Interference and Quantum Error Correction*, Proc. Roy. Soc. Lond. A452 (1996) 2551 ([arXiv:quant-ph/9601029](https://arxiv.org/abs/quant-ph/9601029))

* [[Emanuel Knill]], [[Raymond Laflamme]], *A Theory of Quantum Error-Correcting Codes*, Phys. Rev. Lett. 84:2525-2528, 2000 ([arXiv:quant-ph/9604034](https://arxiv.org/abs/quant-ph/9604034))


{#FeasabilityReferences} Realization that quantum error correcting codes could make quantum computation practically feasible (quantum [[error threshold theorem]]):

* [[Emanuel Knill]], [[Raymond Laflamme]], [[Wojciech H. Zurek]], *Resilient Quantum Computation: Error Models and Thresholds*, Proceedings of the Royal Society A **454** 1969 (1998) &lbrack;[arXiv:quant-ph/9702058](https://arxiv.org/abs/quant-ph/9702058)&rbrack;

* [[John Preskill]], *Fault-tolerant quantum computation*, in: *Introduction to Quantum Computation and Information*, World Scientific (1998) $[$[arXiv:quant-ph/9712048](https://arxiv.org/abs/quant-ph/9712048), [doi:10.1142/3724](https://doi.org/10.1142/3724)$]$

* [[John Preskill]], *Reliable Quantum Computers*, Proc. Roy. Soc. Lond. A **454** (1998) 385-410 $[$[arXiv:quant-ph/9705031](https://arxiv.org/abs/quant-ph/9705031), [doi:10.1098/rspa.1998.0167](https://doi.org/10.1098/rspa.1998.0167)$]$

* [[Daniel Gottesman]], *Theory of fault-tolerant quantum computation*, Phys. Rev. A **57** (1998) 127-137 $[$[doi:10.1103/PhysRevA.57.127](https://doi.org/10.1103/PhysRevA.57.127)$]$

* [[Dorit Aharonov]], [[Michael Ben-Or]], *Fault-Tolerant Quantum Computation With Constant Error Rate*, SIAM J. Comput., **38** 4 (2008) 1207–1282 &lbrack;[arXiv:quant-ph/9906129](https://arxiv.org/abs/quant-ph/9906129), [doi:10.1007/978-3-642-32512-0_31](https://doi.org/10.1007/978-3-642-32512-0_31)&rbrack;

* [[Daniel Gottesman]], *Fault-Tolerant Quantum Computation*,  Physics in Canada **63** 4  (2007) 183-189 $[$[arXiv:quant-ph/0701112](https://arxiv.org/abs/quant-ph/0701112)$]$


* Dorit Aharonov, Michael Ben-Or, *Fault-Tolerant Quantum Computation With Constant Error Rate*, SIAM J. Comput. **38** 4 (2008) 1207–1282 ([arXiv:quant-ph/9906129](https://arxiv.org/abs/quant-ph/9906129), [doi:10.1137/S0097539799359385](https://doi.org/10.1137/S0097539799359385))

* Panos Aliferis, [[Daniel Gottesman]], [[John Preskill]], *Quantum accuracy threshold for concatenated distance-3 codes*, Quant. Inf. Comput. 6 (2006) 97-165 ([arXiv:quant-ph/0504218](https://arxiv.org/abs/quant-ph/0504218))

* Earl T. Campbell, Barbara M. Terhal, Christophe Vuillot: *Roads towards fault-tolerant universal quantum computation*, Nature **549** (2017) 172–179 \[<a href="https://doi.org/10.1038/nature23460">doi:10.1038/nature23460</a>, [arXiv:1612.07330](https://arxiv.org/abs/1612.07330)\]


    

[[operator algebra|Operator algebraic]] formulation of quantum error correction:

* [[David Kribs]], [[Raymond Laflamme]], [[David Poulin]], *A Unified and Generalized Approach to Quantum Error Correction*, Phys. Rev. Lett. 94, 180501 (2005) ([arXiv:quant-ph/0412076](https://arxiv.org/abs/quant-ph/0412076))

* [[David W. Kribs]], [[Raymond Laflamme]], [[David Poulin]], [[Maia Lesosky]], *Operator quantum error correction*, Quant. Inf. & Comp., 6 (2006), 383-399 ([arXiv:quant-ph/0504189](https://arxiv.org/abs/quant-ph/0504189))

on [[quantum observables]]:

* {#BenyKempfKribs06} Cédric Bény, Achim Kempf, [[David W. Kribs]], _Generalization of Quantum Error Correction via the Heisenberg Picture_, Phys. Rev. Lett. 98, 100502 – Published 7 March 2007 ([doi:10.1103/PhysRevLett.98.100502](https://doi.org/10.1103/PhysRevLett.98.100502), [arXiv:quant-ph/0608071](https://arxiv.org/abs/quant-ph/0608071))

* Cédric Bény, Achim Kempf, [[David W. Kribs]], _Quantum Error Correction of Observables_, Phys. Rev. A 76, 042303 (2007) ([arXiv:0705.1574](https://arxiv.org/abs/0705.1574))


Introduction and survey:


* [[Alexei Kitaev]],  *Quantum computations: algorithms and error correction*, Russian Mathematical Surveys, **52** 6 (1997) &lbrack;[doi:10.1070/RM1997v052n06ABEH002155](https://iopscience.iop.org/article/10.1070/RM1997v052n06ABEH002155), <a href="https://ochicken.top/Library/Physics/Quantum_Computation_and_Quantum_Information/1997.06%20A.Yu.Kitaev_%20Quantum%20computations_%20algorithms%20and%20error%20correction%20(kitaev1997).pdf">pdf</a>&rbrack;

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], Chapter 10 of: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

* Simeon Ball, Aina Centelles, Felix Huber, *Quantum error-correcting codes and their geometries* ([arXiv:2007.05992](https://arxiv.org/abs/2007.05992))

* {#Steane06} [[Andrew M. Steane]], *A Tutorial on Quantum Error Correction*, in: Proceedings of the International School of Physics “Enrico Fermi”, course CLXII, "Quantum Computers, Algorithms and Chaos"  (2006) &lbrack;[pdf](https://www2.physics.ox.ac.uk/sites/default/files/ErrorCorrectionSteane06.pdf), [[SteaneTutorialQuantumErrorCorrection.pdf:file]]&rbrack; 

* [[Daniel Gottesman]]: *An Introduction to Quantum Error Correction and Fault-Tolerant Quantum Computation*, in: *Quantum Information Science and Its Contributions to Mathematics*, Proceedings of Symposia in Applied Mathematics **68** (2010) &lbrack;[arXiv:0904.2557](https://arxiv.org/abs/0904.2557), [doi:10.1090/psapm/068](https://doi.org/10.1090/psapm/068)&rbrack;


* [[Isaac L. Chuang]], *Quantum error correction*, Chapter 7 in: *Quantum Machines: Measurement and Control of Engineered Quantum Systems* Lecture Notes of the Les Houches Summer School **96** (2011) 273–320  &lbrack;[doi:10.1093/acprof:oso/9780199681181.003.0007](https://doi.org/10.1093/acprof:oso/9780199681181.003.0007)&rbrack;


* {#DevittNemotoMunro09} [[Simon J. Devitt]], [[Kae Nemoto]], [[William J. Munro]], *Quantum Error Correction for Beginners*, Rep. Prog. Phys. **76** (2013) 076001 &lbrack;[arXiv:0905.2794](https://arxiv.org/abs/0905.2794), [doi:10.1088/0034-4885/76/7/076001](https://iopscience.iop.org/article/10.1088/0034-4885/76/7/076001)&rbrack;

* Daniel A. Lidar, Todd A. Brun (eds.): *Quantum Error Correction*, Cambridge University Press (2013) \[<a href="https://www.cambridge.org/de/universitypress/subjects/physics/quantum-physics-quantum-information-and-quantum-computation/quantum-error-correction?format=HB&isbn=9780521897877">ISBN:9780521897877</a>, <a href="https://doi.org/10.1017/CBO9781139034807">doi:10.1017/CBO9781139034807</a>\]

* Héctor Bombín: *An Introduction to Topological Quantum Codes*, in: *Quantum Error Correction*, Cambridge University Press (2013) \[<a href="https://www.cambridge.org/de/universitypress/subjects/physics/quantum-physics-quantum-information-and-quantum-computation/quantum-error-correction?format=HB&isbn=9780521897877">ISBN:9780521897877</a>, [arxiv:1311.0277](https://arxiv.org/abs/1311.0277)\]

* {#RowellWang17} [[Eric Rowell]], [[Zhenghan Wang]], Section 3.2.3 of: _Mathematics of Topological Quantum Computing_, Bull. Amer. Math. Soc. 55 (2018), 183-238 ([arXiv:1705.06206](https://arxiv.org/abs/1705.06206), [doi:10.1090/bull/1605](https://doi.org/10.1090/bull/1605))


* [[Scott Aaronson]], Chapter 27 of: *Introduction to Quantum Information Science* (2018) &lbrack;[pdf](https://www.scottaaronson.com/qclec.pdf), [webpage](https://www.scottaaronson.com/cs378/)&rbrack;


* Joschka Roffe, *Quantum Error Correction: An Introductory Guide*, Contemporary Physics 2019 ([arXiv:1907.11157](https://arxiv.org/abs/1907.11157))

* [[Bei Zeng]], [[Xie Chen]], [[Duan-Lu Zhou]], [[Xiao-Gang Wen]]: 

  Sec. 3 of: *[[Quantum Information Meets Quantum Matter]] -- From Quantum Entanglement to Topological Phases of Many-Body Systems*, Quantum Science and Technology (QST), Springer (2019) $[$[arXiv:1508.02595](https://arxiv.org/abs/1508.02595), [doi:10.1007/978-1-4939-9084-9](https://doi.org/10.1007/978-1-4939-9084-9)$]$

* {#ZhuCross20} Guanyu Zhu, Andrew Cross, *[Hardware-aware approach for fault-tolerant quantum computation](https://www.ibm.com/blogs/research/2020/09/hardware-aware-quantum/)*, IBM Research Blog, September 2, 2020

* Priya J. Nadkarni, Narayanan Rengaswamy, Bane Vasić: *Tutorial on Quantum Error Correction for 2024 Quantum Information Knowledge (QuIK) Workshop* &lbrack;[arXiv:2407.12737](https://arxiv.org/abs/2407.12737), [inSpire:2808724](https://inspirehep.net/literature/2808724)&rbrack;


See also:

* Wikipedia, _[Quantum error correction](https://en.m.wikipedia.org/wiki/Quantum_error_correction)_

* {#AlbertECZ} [[Victor V. Albert]] et al.,  *[errorcorrectionzoo.org](https://errorcorrectionzoo.org)*

* [[Victor V. Albert]], Philippe Faist: *Handbook of Error-Correcting Codes* &lbrack;[arXiv:2606.11484](https://arxiv.org/abs/2606.11484)&rbrack;


In the context of [[quantum secret sharing]]:

* {#CleveGottesmanLo99} Richard Cleve, [[Daniel Gottesman]], Hoi-Kwong Lo, *How to share a quantum secret*, Phys. Rev. Lett. 83 (1999) 648-651 ([arXiv:quant-ph/9901025](https://arxiv.org/abs/quant-ph/9901025))

In the context of quantum communication:

* [[Matthias Christandl]], Alexander Müller-Hermes, *Fault-tolerant Coding for Quantum Communication*,
IEEE Transactions on Information Theory, &lbrack;[arXiv:2009.07161](https://arxiv.org/abs/2009.07161)  [doi:10.1109/TIT.2022.3169438](https://ieeexplore.ieee.org/document/9761242)&rbrack;

On (in-)compatibility of quantum error correction with universality of quantum gates ([[Eastin-Knill theorem]]):

* [[Bryan Eastin]], [[Emanuel Knill]], *Restrictions on Transversal Encoded Quantum Gate Sets*,  Phys. Rev. Lett. 102, 110502 (2009) ([arXiv:0811.4262](https://arxiv.org/abs/0811.4262))

* {#WVSB20} Paul Webster, Michael Vasmer, Thomas R. Scruby, Stephen D. Bartlett, *Universal Fault-Tolerant Quantum Computing with Stabiliser Codes* ([arXiv:2012.05260](https://arxiv.org/abs/2012.05260))

For [[quantum annealing]] processes:

* Kristen L. Pudenz, Tameem Albash, Daniel A. Lidar: *Error-corrected quantum annealing with hundreds of qubits*, Nature Communications **5** 3243 (2014) &lbrack;[doi:10.1038/ncomms4243](https://doi.org/10.1038/ncomms4243)&rbrack;


On continuous variable quantum codes:

* [[Samuel L. Braunstein]], Peter van Loock, §IV.C in: *Quantum information with continuous variables*, Rev. Mod. Phys. **77** 2 (2005) 513 &lbrack;[arXiv:quant-ph/0410100](https://arxiv.org/abs/quant-ph/0410100), [doi:10.1103/RevModPhys.77.513](https://doi.org/10.1103/RevModPhys.77.513)&rbrack;

* [[Samuel L. Braunstein]], Arun K. Pati, *Quantum Information with Continuous Variables*, Springer (2003) &lbrack;[doi:10.1007/978-94-015-1258-9](https://doi.org/10.1007/978-94-015-1258-9)&rbrack;

* Allan D. C. Tosta, Thiago O. Maciel, [[Leandro Aolita]], *Grand Unification of continuous-variable codes* &lbrack;[arXiv:2206.01751](https://arxiv.org/abs/2206.01751)&rbrack;


In relation to the [[SYK model]]:

* Shao-Kai Jian, Chunxiao Liu, Xiao Chen, [[Brian Swingle]], Pengfei Zhang, *Quantum error as an emergent magnetic field* ([arXiv:2106.09635](https://arxiv.org/abs/2106.09635))

In relation to continuous symmetries:

* Zi-Wen Liu, Sisi Zhou, *Approximate symmetries and quantum error correction* ([arXiv:2111.06355](https://arxiv.org/abs/2111.06355))

Further developments:

* Mackenzie H. Shaw, [[Andrew C. Doherty]], Arne L. Grimsmo, *Stabilizer subsystem decompositions for single- and multi-mode Gottesman-Kitaev-Preskill codes* &lbrack;[arXiv:2210.14919](https://arxiv.org/abs/2210.14919)&rbrack;

On relevant classical control mechanisms:

* Hideo Mabuchi, *Continuous quantum error correction as classical hybrid control*, New J. Phys. **11** (2009) 105044
&lbrack;[doi:10.1088/1367-2630/11/10/105030](https://iopscience.iop.org/article/10.1088/1367-2630/11/10/105030)&rbrack;

* {#PalerHerrDevitt19} Alexandru Paler, Daniel Herr, [[Simon J. Devitt]], *Really Small Shoe Boxes - On Realistic Quantum Resource Estimation*, Computer **52** 6 (2019) &lbrack;[arXiv:1902.08104](https://arxiv.org/abs/1902.08104), [doi:10.1109/MC.2019.2908621](https://doi.org/10.1109/MC.2019.2908621)&rbrack;

In relation to the [[Penrose tiling]]:

* Zhi Li, [[Latham Boyle]], *The Penrose Tiling is a Quantum Error-Correcting Code* &lbrack;[arXiv:2311.13040](https://arxiv.org/abs/2311.13040)&rbrack;

Relating quantum error correction to [[linear logic]]:

* [[Daniel Murfet]], William Troiani, *Linear Logic and Quantum Error Correcting Codes* &lbrack;[arXiv:2405.19051](https://arxiv.org/pdf/2405.19051)&rbrack;


### Experimental realization

Realization of [[quantum error correction]] in [[experiment]], hence in actual [[quantum computers]]:

* D. G. Cory, M. D. Price, W. Maas, [[Emanuel Knill]], [[Raymond Laflamme]], [[Wojchiek H. Zurek]], T. F. Havel, and S. S. Somaroo, *Experimental Quantum Error Correction*, Phys. Rev. Lett. 81, 2152 (1998) ([doi:10.1103/PhysRevLett.81.2152](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.81.2152))


* Daniel Nigg, Markus Mueller, Esteban A. Martinez, Philipp Schindler, Markus Hennrich, Thomas Monz, Miguel A. Martin-Delgado, Rainer Blatt, 

  *Experimental Quantum Computations on a Topologically Encoded Qubit*, Science 18 Jul 2014: Vol. 345, Issue 6194, pp. 302-305 ([arXiv:1403.5426](https://arxiv.org/abs/1403.5426), [doi:10.1126/science.1253742](https://science.sciencemag.org/content/345/6194/302))

  > (via methods from [[topological quantum computation]])


* Adrian Cho, *[The biggest flipping challenge in quantum computing](https://www.sciencemag.org/news/2020/07/biggest-flipping-challenge-quantum-computing)*, Science News Jul. 9, 2020 

  > (exposition)

* Y. Ma et al. *Error-transparent operations on a logical qubit protected by quantum error correction*, Nature Physics volume 16, pages 827–831 (2020) ([doi:10.1038/s41567-020-0893-x](https://doi.org/10.1038/s41567-020-0893-x))


* Ming Gong et al. *Experimental exploration of five-qubit quantum error correcting code with superconducting qubits*, National Science Review, nwab011 (2021) ([doi:10.1093/nsr/nwab011](https://doi.org/10.1093/nsr/nwab011))

  survey in:

   EurekaAlert, Science China Press: *Demonstration of the universal quantum error correcting code with superconducting qubits*, March 2021 ([2021-03/scp-dot031521](https://www.eurekalert.org/pub_releases/2021-03/scp-dot031521.php))

* {#Lucero21} Erik Lucero (Google), *[Unveiling our new Quantum AI campus](https://blog.google/technology/ai/unveiling-our-new-quantum-ai-campus/)*,  May 18, 2021
  > (outlook)


* Th. Monz et al., *Demonstration of fault-tolerant universal quantum gate operations*, Nature **605** (2022) 675–680 &lbrack;[doi:10.1038/s41586-022-04721-1](https://doi.org/10.1038/s41586-022-04721-1)&rbrack;

* {#MüllerWallraffEtAl22} [[Markus Müller]], [[Andreas Wallraff]] et al., *Realizing Repeated Quantum Error Correction in a Distance-Three Surface Code*, Nature **605** (2022) 669–674 &lbrack;[arXiv:2112.03708](https://arxiv.org/abs/2112.03708), [doi:10.1038/s41586-022-04566-8](https://doi.org/10.1038/s41586-022-04566-8)&rbrack;

* [[Markus Müller]] et al., *Demonstration of fault-tolerant universal quantum gate operations*, Nature **605** (2022) 675-680 &lbrack;[doi:10.1038/s41586-022-04721-1](https://doi.org/10.1038/s41586-022-04721-1), [arXiv:2111.12654](https://arxiv.org/abs/2111.12654)&rbrack;

* {#GQ2025} Google Quantum AI et al.: *Quantum error correction below the surface code threshold*, Nature **638** (2025) 920-926 &lbrack;[doi:10.1038/s41586-024-08449-y](https://doi.org/10.1038/s41586-024-08449-y), [arXiv:2408.13687](https://arxiv.org/abs/2408.13687)&rbrack;

### Via holographic tensor networks
 {#ReferencesViaHolographicTensorNetworks}

First quantum error correcting codes associated with planar bulk/boundary systems:

* S. B. Bravyi, [[Alexei Kitaev]], *Quantum codes on a lattice with boundary* ([arXiv:quant-ph/9811052](https://arxiv.org/abs/quant-ph/9811052))

* [[Michael Freedman]], David A. Meyer, *Projective Plane and Planar Quantum Codes*, Found. Comput. Math. 1, 325–332 (2001) ([arXiv:quant-ph/9810055](https://arxiv.org/abs/quant-ph/9810055), [doi:10.1007/s102080010013](https://doi.org/10.1007/s102080010013))


First suggestion relating quantum error correction to [[black hole entropy]]:

* {#VerlindeVerlinde12} [[Erik Verlinde]], [[Herman Verlinde]], *Black Hole Entanglement and Quantum Error Correction*, J. High Energ. Phys. 2013, 107 (2013) ([arXiv:1211.6913](https://arxiv.org/abs/1211.6913),  <a href="https://doi.org/10.1007/JHEP10(2013)107">doi:10.1007/JHEP10(2013)107</a>)
     

Introducing the idea of quantum error correcting codes given by [[tensor network states]]:

* {#FerrisPoulin13} Andrew J. Ferris, [[David Poulin]], *Tensor Networks and Quantum Error Correction*, Phys. Rev. Lett. 113, 030501 (2014) ([arXiv:1312.4578](https://arxiv.org/abs/1312.4578))

* Dave Bacon, Steven T. Flammia, Aram W. Harrow, Jonathan Shi, *Sparse Quantum Codes from Quantum Circuits*, Proc. of STOC '15, pp. 327-334 (2015); IEEE Transactions on Information Theory, vol 63, no 4, pp 2464-2479, April 2017 ([arXiv:1411.3334](https://arxiv.org/abs/1411.3334))

following observations in

* {#Swingle09} [[Brian Swingle]], _Entanglement Renormalization and Holography_, Phys. Rev. D 86, 065007 (2012) ([arXiv:0905.1317](https://arxiv.org/abs/0905.1317))

* {#Swingle12} [[Brian Swingle]], _Constructing holographic spacetimes using entanglement renormalization_ ([arXiv:1209.3304](https://arxiv.org/abs/1209.3304), [spire:1185813](http://inspirehep.net/record/1185813))

Interpretation of [[holographic tensor networks]] encoding [[holographic entanglement entropy]] in models for [[AdS2-CFT1 duality]] as [[quantum error correcting codes]]:

* {#ADH14} [[Ahmed Almheiri]], [[Xi Dong]], [[Daniel Harlow]], _Bulk Locality and Quantum Error Correction in AdS/CFT_, JHEP 1504:163,2015 ([arXiv:1411.7041](https://arxiv.org/abs/1411.7041), <a href="https://doi.org/10.1007/JHEP04(2015)163">doi:10.1007/JHEP04(2015)163</a>)

  > (using [Bény-Kempf-Kribs 06](#BenyKempfKribs06))

with precursor observations in 

* [[Beni Yoshida]], *Information storage capacity of discrete spin systems*, Annals of Physics 338, 134 (2013) ([arXiv:1111.3275](https://arxiv.org/abs/1111.3275))

  > (focus on classical [[error correcting codes]])

* Jose I. Latorre, German Sierra, *Holographic codes* ([arXiv:1502.06618](https://arxiv.org/abs/1502.06618))

and concrete implementation by the [[HaPPY code]]:

* {#PYHP15} [[Fernando Pastawski]], [[Beni Yoshida]], [[Daniel Harlow]], [[John Preskill]], _Holographic quantum error-correcting codes: Toy models for the bulk/boundary correspondence_, JHEP 06 (2015) 149 ([arXiv:1503.06237](https://arxiv.org/abs/1503.06237))

and possibly more generally:

* [[Daniel Harlow]], *The Ryu–Takayanagi Formula from Quantum Error Correction*, Comm. Math. Phys. **354** (2017) 865–912 &lbrack;[doi:10.1007/s00220-017-2904-z](https://doi.org/10.1007/s00220-017-2904-z), [arXiv:1607.03901](https://arxiv.org/abs/1607.03901)&rbrack;


Introduction of the more general [[Majorana dimer code]]:

* [[Alexander Jahn]], [[Marek Gluza]], [[Fernando Pastawski]], [[Jens Eisert]], _Majorana dimers and holographic quantum error-correcting codes_, Phys. Rev. Research 1, 033079 (2019) ([arXiv:1905.03268](https://arxiv.org/abs/1905.03268))

Exposition and review:

* [[John Preskill]], *Is spacetime a quantum error-correcting code?*, talk at KITP 2015 ([pdf](http://theory.caltech.edu/~preskill/talks/Preskill-KITP-holographic-2015.pdf), [[Preskill_SpacetimeQEC.pdf:file]])

* {#Harlow18} [[Daniel Harlow]], _TASI Lectures on the Emergence of Bulk Physics in AdS/CFT_, PoS TASI2017 (2018) 002 ([arXiv:1802.01040](https://arxiv.org/abs/1802.01040), [doi:10.22323/1.305.0002](https://doi.org/10.22323/1.305.0002))

* [[Pratik Rath]], *Aspects of Holography And Quantum Error Correction*, 2020 ([pdf](https://digitalassets.lib.berkeley.edu/etd/ucb/text/Rath_berkeley_0028E_19810.pdf), [[RathHolographyAndQEC.pdf:file]]) 

* [[Melanie Swan]], [[Renato P dos Santos]], [[Frank Witte]], *The AdS/CFT Correspondence and Holographic Codes* ([doi:10.1142/9781786348210_0013](https://doi.org/10.1142/9781786348210_0013), [doi:10.1142/9781786348210_0014](https://www.worldscientific.com/doi/abs/10.1142/9781786348210_0014)), Part 5 in: Between Science and Economics, Volume 2: *Quantum Computing Physics, Blockchains, and Deep Learning Smart Networks*, World Scientific 2020 ([doi:10.1142/q0243](https://doi.org/10.1142/q0243))

* {#Harlow20} [[Daniel Harlow]], *Computation and Holography*, talk at [Snowmass Computational Frontier Workshop 2020](https://indico.fnal.gov/event/43829/) ([pdf](https://indico.fnal.gov/event/43829/contributions/193566/attachments/132763/163346/snowmasscomp.pdf), [[HarlowComputationHolography.pdf:file]])


* [[Alexander Jahn]], [[Jens Eisert]], _Holographic tensor network models and quantum error correction: A topical review_ ([arXiv:2102.02619](https://arxiv.org/abs/2102.02619))

* Tanay Kibe, Prabha Mandayam, Ayan Mukhopadhyay, *Holographic spacetime, black holes and quantum error correcting codes: A review* ([arXiv:2110.14669](https://arxiv.org/abs/2110.14669))


Further discussion of holographic quantum error correcting codes:

* Henrique Lazari, Reginaldo Palazzo Jr., *Geometrically uniform hyperbolic codes*, Comput. Appl. Math. vol.24 no.2 Petrópolis 2005 ([doi:10.1590/S0101-82052005000200002](https://doi.org/10.1590/S0101-82052005000200002))

* Enrico M. Brehm, Benedikt Richter, *Classical Holographic Codes*, Phys. Rev. D 96, 066005 (2017) ([arXiv:1609.03560](https://arxiv.org/abs/1609.03560))

* [[Fernando Pastawski]], [[John Preskill]], *Code properties from holographic geometries*, Phys. Rev. X 7, 021022 (2017) ([arXiv:1612.00017](https://arxiv.org/abs/1612.00017))


* [[Robert J. Harris]], [[Nathan A. McMahon]], [[Gavin K. Brennen]], [[Thomas M. Stace]], *Calderbank-Steane-Shor Holographic Quantum Error Correcting Codes*, Phys. Rev. A 98, 052301 (2018) ([arXiv:1806.06472](https://arxiv.org/abs/1806.06472))

* Tamara Kohler, Toby Cubitt, *Toy Models of Holographic Duality between local Hamiltonians*, 	J. High Energy Phys. 2019:17 (2019) ([arXiv:1810.08992](https://arxiv.org/abs/1810.08992))

* Tobias J. Osborne, Deniz E. Stiegemann, *Dynamics for holographic codes*, J. High Energ. Phys. 2020, 154 (2020) ([arXiv:1706.08823](https://arxiv.org/abs/1706.08823))

* Martina Gschwendtner, Robert König, Burak Şahinoğlu & Eugene Tang, *Quantum error-detection at low energies*, Journal of High Energy Physics volume 2019, Article number: 21 (2019) ([arXiv:1902.02115](https://arxiv.org/abs/1902.02115))


* [[Nathan A. McMahon]], [[Gavin K. Brennen]], [[Thomas M. Stace]], [[Robert J. Harris]], Elliot Coupe, *Decoding Holographic Codes with an Integer Optimisation Decoder* ([arXiv:2008.10206](https://arxiv.org/abs/2008.10206))


* [[Terry Farrelly]], [[Robert J. Harris]], [[Nathan A. McMahon]], [[Thomas M. Stace]], *Tensor-network codes* ([arXiv:2009.10329](https://arxiv.org/abs/2009.10329))

* ChunJun Cao, Brad Lackey, *Approximate Bacon-Shor Code and Holography* ([arXiv:2010.05960](https://arxiv.org/abs/2010.05960))

* {#CDCW21} Sam Cree, Kfir Dolev, Vladimir Calvera, Dominic J. Williamson, *Fault-tolerant logical gates in holographic stabilizer codes are severely restricted* ([arXiv:2103.13404](https://arxiv.org/abs/2103.13404))

* Robert de Mello Koch, Eunice Gandote, Nirina Hasina Tahiridimbisoa, Hendrik J.R. Van Zyl, *Quantum Error Correction and Holographic Information from Bilocal Holography* ([arXiv:2106.00349](https://arxiv.org/abs/2106.00349))

* [[Chris Akers]], [[Geoff Penington]], *Quantum minimal surfaces from quantum error correction* ([arXiv:2109.14618](https://arxiv.org/abs/2109.14618))

* ChunJun Cao, Brad Lackey, *Quantum Lego: Building Quantum Error Correction Codes from Tensor Networks*, PRX Quantum **3** 020332 (2022) $[$[arXiv:2109.08158](https://arxiv.org/abs/2109.08158), [doi:10.1103/PRXQuantum.3.020332](https://doi.org/10.1103/PRXQuantum.3.020332)$]$

* Jason Pollack, Patrick Rall, Andrea Rocchetto, *Understanding holographic error correction via unique algebras and atomic examples*, Journal of High Energy Physics, 56 (2022) $[$[arXiv:2110.14691](https://arxiv.org/abs/2110.14691)$]$

* Dmitry S. Ageev, *Exploring uberholography* &lbrack;[arXiv:2208.07387](https://arxiv.org/abs/2208.07387)&rbrack;

* Matthew Steinberg, Sebastian Feld, [[Alexander Jahn]], *Holographic Codes from Hyperinvariant Tensor Networks* &lbrack;[arXiv:2304.02732](https://arxiv.org/abs/2304.02732)&rbrack;


Understanding in terms of the [[eigenstate thermalization hypothesis]]:

* [[Ning Bao]], Newton Cheng, *Eigenstate Thermalization Hypothesis and Approximate Quantum Error Correction*, JHEP 08 (2019) 152 ([arXiv:1906.03669](https://arxiv.org/abs/1906.03669))

In relation to [[holographic Renyi entropy]]:

* [[Chris Akers]], [[Pratik Rath]], *Holographic Renyi entropy from quantum error correction*,  J. High Energ. Phys. 2019, 52 (2019) ([arXiv:1811.05171](https://arxiv.org/abs/1811.05171))

From [[tesselations]] of higher-dimensional [[hyperbolic space]]:

* Vivien Londe, Anthony Leverrier, *Golden codes: quantum LDPC codes built from regular tessellations of hyperbolic 4-manifolds* ([arXiv:1712.08578](https://arxiv.org/abs/1712.08578))



In view of [[black hole thermodynamics]]:

* [Verlinde & Verlinde 2012](#VerlindeVerlinde12)

* [[Ahmed Almheiri]], _Holographic Quantum Error Correction and the Projected Black Hole Interior_ ([arXiv:1810.02055](https://arxiv.org/abs/1810.02055))

* Isaac H. Kim, Eugene Tang, [[John Preskill]], *The ghost in the radiation: Robust encodings of the black hole interior*, JHEP 2020, 31 (2020) ([arXiv:2003.05451](https://arxiv.org/abs/2003.05451))

* [[Chris Akers]], [[Netta Engelhardt]], [[Daniel Harlow]], [[Geoff Penington]], [[Shreya Vardhan]], *The black hole interior from non-isometric codes and complexity* &lbrack;[arXiv:2207.06536](https://arxiv.org/abs/2207.06536)&rbrack;

* [[Daniel Harlow]], *A theory of the black hole interior*, talk at *[Strings 2022](https://indico.cern.ch/event/1085701) &lbrack;[indico:4940817/](https://indico.cern.ch/event/1085701/contributions/4940817/)&rbrack;




Discussion of [[gauge symmetry]] of [[holographic tensor networks]] and their [[quantum error correcting codes]]:

* Kfir Dolev, Vladimir Calvera, Sam Cree, Dominic J. Williamson, 
*Gauging the bulk: generalized gauging maps and holographic codes* ([arXiv:2108.11402](https://arxiv.org/abs/2108.11402))

Relation of quantum error correcting codes to the [[Monster vertex operator algebra]] and more generally to [[2d SCFT]] and [[string theory]]:

* [[Jeffrey A. Harvey]], [[Gregory W. Moore]], *Moonshine, Superconformal Symmetry, and Quantum Error Correction*,  J. High Energ. Phys. **2020**, 146 (2020). ([arXiv:2003.13700](https://arxiv.org/abs/2003.13700))

In relation to the [[large N limit]]:

* Alexey Milekhin, *Quantum error correction and large $N$* ([arXiv:2008.12869](https://arxiv.org/abs/2008.12869))

In relation to [[renormalization group flow]]:

* Keiichiro Furuya, Nima Lashkari, Mudassir Moosa, *Renormalization group and approximate error correction* ([arXiv:2112.05099](https://arxiv.org/abs/2112.05099))

In relation to fixed-point [[path integrals]]:

* Andreas Bauer, _Topological error correcting processes from fixed-point path integrals_ ([arXiv:2303.16405](https://arxiv.org/abs/2303.16405))


Musings on possible implications on relations between [[quantum gravity]] and [[quantum information]]:

* {#SimonsFoundationItFromQBit} [[Simons Foundation]], *[It from Qubit: Simons Collaboration on Quantum Fields, Gravity and Information](https://www.simonsfoundation.org/mathematics-physical-sciences/it-from-qubit/)*


* Iulia Georgescu, *Strings and qubits*, Nature Reviews Physics volume 1, page 477 (2019) ([doi:s42254-019-0087-6](https://www.nature.com/articles/s42254-019-0087-6))

* Natalie Wolchover, *[How Space and Time Could Be a Quantum Error-Correcting Code](https://www.quantamagazine.org/how-space-and-time-could-be-a-quantum-error-correcting-code-20190103/)*, Quanta Magazine, Jan. 3 2019

* [[Tom Banks]], *Holographic Space-time and Quantum Information* ([arXiv:2001.08205](https://arxiv.org/abs/2001.08205))

* ChunJun Cao, *From Quantum Codes to Gravity: A Journey of Gravitizing Quantum Mechanics* ([arXiv:2112.00199](https://arxiv.org/abs/2112.00199))

* Takaaki Kuwahara, Ryota Nasu, Gota Tanaka, Asato Tsuchiya: *Quantum error correction realized by the renormalization group in scalar field theories* &lbrack;[arXiv:2401.17795](https://arxiv.org/abs/2401.17795)&rbrack;

    


[[!redirects quantum error correction code]]
[[!redirects quantum error correction codes]]

[[!redirects quantum error correcting code]]
[[!redirects quantum error correcting codes]]

[[!redirects QEC]]

[[!redirects code subspace]]
[[!redirects code subspaces]]

[[!redirects logical qbit]]
[[!redirects logical qbits]]

[[!redirects physical qbit]]
[[!redirects physical qbits]]


[[!redirects holographic quantum error correction]]

[[!redirects holographic quantum error correction code]]
[[!redirects holographic quantum error correction codes]]

[[!redirects holographic quantum error correcting code]]
[[!redirects holographic quantum error correcting codes]]


