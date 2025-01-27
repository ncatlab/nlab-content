
> not to be confused with _[[Wigner classification]]_

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### AQFT
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

What is known as *Wigner's theorem* (in honor of the appendix of §20 in [Wigner 1931](#Wigner31)/[59](#Wigner1959)) is one of the basic results on the foundations of [[quantum mechanics]] (generally of [[quantum physics]]). The theorem characterizes the intrinsic notion of *[[symmetry|symmetries]]* in [[quantum physics]] ("quantum symmetries") assuming only [[observable]] properties of ([[pure state|pure]]) [[quantum states]] (namely their [[projective space|projectivity]] subject to the [[Born rule]]) and *deriving* from this that quantum symmetries are necessarily [[linear representation|represented]] by [[unitary operators]] *or* [[anti-unitary operators]] on the [[Hilbert space]] [[space of quantum states|of states]].

Notice that a prominent class of examples of [[anti-unitary operators]] appearing as [[quantum symmetries]] are [[time-reversal symmetry|time-reversal symmetries]] ([Wigner 1959, §26](#Wigner1959)) such as appearing in the [[CPT-theorem]].

A key applications of Wigner's theorem is within the [[K-theory classification of topological phases of matter]], where the (anti-)unitary quantum symmetries of [[effective field theory|effectively]] [[free field|free]] [[electrons]] in a [[crystal]] are identified with possible [[twisted equivariant K-theory|twistings]] of the [[equivariant K-theory]] of the crystal's [[Brillouin torus]] ([Freed & Moore 2013, §1](#FreedMoore13), see also [[schreiber:Anyonic topological order in TED K-theory|SS22, §2.2]]).



## Preliminaries
 {#Preliminaries}

Let $\mathcal{H}$ be a [[complex vector space|complex]] [[separable Hilbert space|separable]] [[Hilbert space]] and write

\[
  \label{ProjectiveSpaceOfHilbertSpace}
  P\mathcal{H}
  \;\coloneqq\;
  \big(
    \mathcal{H} \setminus \{0\}
  \big)/ \mathbb{C}^\times
\]

for its [[complex projective space]] (here $\mathbb{C}^\times = \mathbb{C} \setminus \{0\}$ denotes the [[group of units]] of the [[ring]] of [[complex numbers]] and $\mathrm{U}(1) \subset \mathbb{C}^\times$ will denote the [[unitary group]] [[U(1)]]).

In [[quantum physics]] one often says that a [[pure state|pure]] [[quantum state]] is an element (hence a [[vector]], then often called a "[[wavefunction]]") $\psi \,\in\, \mathcal{H}$, but by the [[Born rule]] it is really only the corresponding [[complex line]]

$$
  [\psi]
  \;\coloneqq\;
  \big\{
    c \cdot \psi
    \,\big\vert\,
    c \in \mathrm{U}(1)
  \big\}
  \;\;\;
  \in
  \;
  P\mathcal{H}
$$

which is physically observable. In fact, what is concretely observable (still according to the [[Born rule]]) are the transition [[probabilities]], given by the following [[function]] to the [[closed interval]] of possible [[probability]] values:

\[
  \label{ProbabilityFunctionOnRays}
  \array{
    P\mathcal{H}
    \times 
    P\mathcal{H}
    &\xrightarrow{\;\;\;p\;\;\;}&
    [0,1]
    \\
    \big(
      [\psi_1]
      ,\,
      [\psi_2]
    \big)
    &
    \overset{\;\;\;\;}{\mapsto}
    &
    \frac{
       \langle \psi_1 \vert \psi_2 \rangle
       \langle \psi_2 \vert \psi_1 \rangle
    }{
       \langle \psi_1 \vert \psi_1 \rangle
       \langle \psi_2 \vert \psi_2 \rangle
    }
    \mathrlap{\,,}
  }
\]

where $\langle - \vert - \rangle$ denotes the given [[inner product]] on $\mathcal{H}$.

Hence a "quantum symmetry" in the sense of a re-shuffling of the [[pure states]] of a [[quantum system]] which leaves the observable physics [[invariant]] must be a [[bijection]] on the projective space $P\mathcal{H}$ (eq:ProjectiveSpaceOfHilbertSpace) which preserves the observable probabilities (eq:ProbabilityFunctionOnRays):

\[
  \label{QuantumSymmetry}
  S
  \;\colon\;
  P\mathcal{H}
  \xrightarrow{\;\sim\;}
  P\mathcal{H}
  \,,
  \;\;\;\;\;\;
  p
  \big(
    S(-)
    ,\,
    S(-)
  \big)
  \;=\;
  p(-,\,-)
  \,.
\]

An *example* of a quantum symmetry (eq:QuantumSymmetry) is provided by any [[complex numbers|complex]]-[[linear map|linear]] and [[unitary operator]] on the underlying [[Hilbert space]],

$$
  U \,\colon\, 
  \mathcal{H}
  \xrightarrow{\;\;}
  \mathcal{U}
  \,,
  \;\;\;\;\;\;\;\;
  \big\langle
    U(-)
  \big\vert
    U(-)
  \big\rangle
  \;=\;
  \big\langle
    -
  \big\vert
    -
  \big\rangle
  \,,
$$

in that the induced projectivization

\[
  \label{ProjectivisedUnitaryOperator}
  \array{
    P\mathcal{H}
    &\xrightarrow{\;\;[U]\;\;}&
    P\mathcal{H}
    \\
    [\psi] 
    &\mapsto& 
    \big[
      U(\psi)
    \big]
  }
\]

evidently satisfies (eq:QuantumSymmetry).

On the one hand, there are more quantum symmetries than arise from unitary operators this way. Namely, if $U$ is an [[anti-linear map|anti-linear]] [[anti-unitary operator]], then (eq:ProjectivisedUnitaryOperator) still holds.

On the other hand, this does now already exhaust the most general situation: Wigner's theorem (Prop. \ref{WignerTheorem} below) says that for every quantum symmetry $S \,\colon\, P\mathcal{H} \xrightarrow{\;} P\mathcal{H}$ (eq:QuantumSymmetry) there exists a map $U \,\colon\, \mathcal{H} \xrightarrow{\;} \mathcal{H}$ which is either a [[unitary operator]] or an [[anti-unitary operator]], such that $S \,=\, [U]$ (eq:ProjectivisedUnitaryOperator).

## Statement
 {#Statement}

\begin{proposition}\label{WignerTheorem}
**(Wigner's theorem)**
\linebreak
  Every quantum symmetry $S \,\colon\, P\mathcal{H} \xrightarrow{\;} P\mathcal{H}$ (eq:QuantumSymmetry) is the projectivization (eq:ProjectivisedUnitaryOperator) of a map 
$U \,\colon\, \mathcal{H} \xrightarrow{\;} \mathcal{H}$ which is either a [[unitary operator]] or an [[anti-unitary operator]].
\end{proposition}
The first full proof of this statement seems to be that due to [Bargmann 1964, §1.3](#Bargmann64), following indications in the appendix of §20 in [Wigner 1931](#Wigner31)/[59](#Wigner1959). A geometric proof via the [[Fubini-Study metric]] is given in [Freed 2012, Thm. 8](#Freed12). Statement and proof in the greater generality of possibly non-[[pure state|pure]] [[quantum states]] is given in [Moretti 2017, Thm. 12.11](#Moretti17).


## Related theorems


Other theorems about the foundations and [[interpretation of quantum mechanics]] include:

* [[order-theoretic structure in quantum mechanics]]

  * [[Kochen-Specker theorem]]

  * [[Alfsen-Shultz theorem]]

  * [[Harding-Döring-Hamhalter theorem]]

* [[Fell's theorem]]

* [[Gleason's theorem]]

* [[Bell's theorem]]

* [[Bub-Clifton theorem]]

* [[Kadison-Singer problem]]


## Related entries

* [[particle statistics]]

* [[K-theory classification of topological insulators]]


## References
 {#References}

The original:

* {#Wigner31} [[Eugene P. Wigner]]: §20(app.) *Gruppentheorie und ihre Anwendung auf die Quantenmechanik der Atomspektren*, Springer (1931) &lbrack;[doi:10.1007/978-3-663-02555-9](https://doi.org/10.1007/978-3-663-02555-9), [pdf](https://digbib.ubka.uni-karlsruhe.de/volltexte/wasbleibt/33355459/33355459.pdf)&rbrack;

and its English translation:

* {#Wigner1959} [[Eugene P. Wigner]], §20(app.) and §26 in: *Group theory: And its application to the quantum mechanics of atomic spectra*, Academic Press (1959) &lbrack;[doi:978-0-12-750550-3](https://www.elsevier.com/books/group-theory/wigner/978-0-12-750550-3)&rbrack;

The first full proof:
 
* {#Bargmann64} [[Valentine Bargmann]], _Note on Wigner's theorem on symmetry transformations_, Journal of Mathematical Physics **5** 7 (1964) 862-868 &lbrack;[doi:10.1063/1.1704188](https://doi.org/10.1063/1.1704188), [pdf](http://materias.df.uba.ar/t2a2019c2/files/2012/07/Bergman-1964.pdf), [[Bargmann-WignerTheorem.pdf:file]]&rbrack;

New proof using the [[Fubini-Study metric]]:

* {#Freed12} [[Daniel Freed]], _On Wigner's theorem_, Geometry & Topology Monographs **18** (2012) 83–89 &lbrack;[arXiv:1112.2133](http://arxiv.org/abs/1112.2133), [doi:10.2140/gtm.2012.18.83](http://dx.doi.org/10.2140/gtm.2012.18.83)&rbrack;

A proof in the greater generality of possibly non-[[pure state|pure]] [[quantum states]]:

* {#Moretti17} [[Valter Moretti]], Thm. 12.11 of:  *Spectral Theory and Quantum Mechanics*, Springer (2017) &lbrack;[doi:10.1007/978-3-319-70706-8](https://doi.org/10.1007/978-3-319-70706-8)&rbrack;

See also:

* Wikipedia, _[Wigner's theorem](https://en.wikipedia.org/wiki/Wigner%27s_theorem#Statement)_


Discussion for [[quaternions|quaternionic]] Hilbert spaces:

* C. S. Sharma and D. F. Almeida, _Additive isometries on a quaternionic Hilbert space_, Journal of Mathematical Physics 31, 1035 (1990) ([doi:10.1063/1.528779](https://doi.org/10.1063/1.528779))

In the context of the [[K-theory classification of topological phases of matter]]:

* {#FreedMoore13} [[Daniel Freed]], [[Gregory Moore]], §1 of: *Twisted equivariant matter*, Ann. Henri Poincaré **14** (2013)  1927-2023 &lbrack;[arXiv:1208.5055](https://arxiv.org/abs/1208.5055), [doi:10.1007/s00023-013-0236-x](https://doi.org/10.1007/s00023-013-0236-x)&rbrack;




[[!redirects Wigner theorem]]
[[!redirects Wigner's theorem]]
[[!redirects Wigner's theorem]]

[[!redirects quantum symmetry]]
[[!redirects quantum symmetries]]

