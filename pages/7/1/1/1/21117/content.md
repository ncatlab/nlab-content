
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



#Contents#
* table of contents
{:toc}


## Idea

### General

*Quantum error corection* is concerned with ensuring the robustness of [[quantum computation]] against [[noise]] (as in classical [[error correction]]) and particularly against [[quantum noise]] and [[quantum decoherence]].

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


### Quantum error correcting codes

The simple but important special case of passive correction of erasures may be  handled by *quantum error correcting codes*:

Recall that a classical [[error correcting code]] on a [[finite set]] of states $S$ is, typically, a choice of [[injection]] of $S$ into some larger set, typicall a [[Cartesian power]] 

$$
  L \overset{code}{\hookrightarrow} P \coloneqq H \times \cdots \times H
$$

(often considered in the form of [[linear codes]], but classical nonetheless). In [[quantum physics]] the [[Cartesian product]] of sets of states is replaced by the [[tensor product of vector spaces|tensor product]] of [[Hilbert spaces]].

For $\mathcal{L}$ a given [[Hilbert space]] of [[quantum states]] ([[finite dimensional vector space|finite-dimensional]] in practice), a *quantum error correcting code* is a choice of [[linear subspace|linear embedding]] (the *code subspace*) of $\mathcal{H}$ into a larger Hilbert spaces, often an  $n$-fold [[tensor product]] of copies of some $H$:

$$
  \array{
    \underset{
     {\color{blue}logical}
     \atop
     {\color{blue}qbits}
    }{
      \mathcal{H}
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

such that the information in $code(\psi)$ in some of the tensor factors $\mathcal{H}^{(i)}$ can be lost without obstructing the reconstruction of $\psi$ (e.g. [Rowell & Wang 17, Sec. 3.2.3](#RowellWang17)).

(Often one demands additional properties, such as that a given set of [[linear operators]] $O$ ([[quantum observables]]) acting on $\psi \in \mathcal{H}$ are implemented on $code(\psi)$ by combionations of operators that act non-trivially only on some of the tensor factors.)

While this is superficially analogous to a classical [[error correcting code]], the crucial and subtle difference is that quantum error correction codes thus take place in a non-[[cartesian monoidal category|Cartesian]] [[symmetric monoidal category|symmetric]] [[monoidal category]]. For this reason, effects of [[quantum entanglement]] play a paramount role in quantum error correction codes.


## Example

### Specific examples

#### A 3-qtrit code
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

  1 and its 6th uncontracted index remaining as an input (shown in red);

   1. regading the uncontrated edges at the cutoff boundary as output (shown in white)

and thus as a [[linear map]] form the [[tensor product]] over the [[bulk]]-[[vertices]] to the [[tensor product]] over the edges sticking out over the boundary.

#### Majorana dimer codes

See at *[[Majorana dimer code]]*.

### Classes of examples

* [[stabilizer code]]


## Related concepts

* [[error correcting code]]

* [[quantum entanglement]]

* [[entanglement entropy]], [[holographic entanglement entropy]]

* [[quantum computing]], [[topological quantum computing]]

* [[quantum secret sharing]]

* [[tensor network]]

## References

### General

Original articles on quantum error correcting codes:

* {#Shor95} [[Peter W. Shor]], *Scheme for reducing decoherence in quantum computer memory*, Phys. Rev. A 52, R2493(R) 1995 ([doi:10.1103/PhysRevA.52.R2493](https://doi.org/10.1103/PhysRevA.52.R2493))

* {#Steane96} [[Andrew M. Steane]], *Error Correcting Codes in Quantum Theory*, Phys. Rev. Lett. 77, 793 1996 ([doi:10.1103/PhysRevLett.77.793](https://doi.org/10.1103/PhysRevLett.77.793))

* {#CalderbankShor96} [[Robert Calderbank]], [[Peter W. Shor]], *Good Quantum Error-Correcting Codes Exist*, Phys. Rev. A, Vol. 54, No. 2, pp. 1098-1106, 1996 ([doi:10.1103/PhysRevA.54.1098](https://doi.org/10.1103/PhysRevA.54.1098))

* {#LMPZ96} [[Raymond Laflamme]], Cesar Miquel, Juan Pablo Paz, [[Wojciech H. Zurek]], *Perfect Quantum Error Correction Code*, Phys. Rev. Lett., 77:198, 1996 ([arXiv:quant-ph/9602019](https://arxiv.org/abs/quant-ph/9602019))

* {#BDSW96} Charles H. Bennett, David P. DiVincenzo, John A. Smolin, William K. Wootters, *Mixed State Entanglement and Quantum Error Correction*, Phys. Rev. A54:3824-3851, 1996 ([doi:10.1103/PhysRevA.54.3824](https://doi.org/10.1103/PhysRevA.54.3824))

* [[Andrew M. Steane]], *Multiple Particle Interference and Quantum Error Correction*, Proc. Roy. Soc. Lond. A452 (1996) 2551 ([arXiv:quant-ph/9601029](https://arxiv.org/abs/quant-ph/9601029))

* [[Emanuel Knill]], [[Raymond Laflamme]], *A Theory of Quantum Error-Correcting Codes*, Phys. Rev. Lett. 84:2525-2528, 2000 ([arXiv:quant-ph/9604034](https://arxiv.org/abs/quant-ph/9604034))


Realization that quantum error correcting codes could make quantum computation practically feasible:

* [[John Preskill]], *Reliable Quantum Computers*, Proc. Roy. Soc. Lond. A454 (1998) 385-410 ([arXiv:quant-ph/9705031](https://arxiv.org/abs/quant-ph/9705031))

* Dorit Aharonov, Michael Ben-Or, *Fault-Tolerant Quantum Computation With Constant Error Rate*, SIAM J. Comput. **38** 4 (2008) 1207–1282 ([arXiv:quant-ph/9906129](https://arxiv.org/abs/quant-ph/9906129), [doi:10.1137/S0097539799359385](https://doi.org/10.1137/S0097539799359385))

* Panos Aliferis, [[Daniel Gottesman]], [[John Preskill]], *Quantum accuracy threshold for concatenated distance-3 codes*, Quant. Inf. Comput. 6 (2006) 97-165 ([arXiv:quant-ph/0504218](https://arxiv.org/abs/quant-ph/0504218))


[[operator algebra|Operator algebraic]] formulation of quantum error correction:

* [[David Kribs]], [[Raymond Laflamme]], [[David Poulin]], *A Unified and Generalized Approach to Quantum Error Correction*, Phys. Rev. Lett. 94, 180501 (2005) ([arXiv:quant-ph/0412076](https://arxiv.org/abs/quant-ph/0412076))

* [[David W. Kribs]], [[Raymond Laflamme]], [[David Poulin]], [[Maia Lesosky]], *Operator quantum error correction*, Quant. Inf. & Comp., 6 (2006), 383-399 ([arXiv:quant-ph/0504189](https://arxiv.org/abs/quant-ph/0504189))

on [[quantum observables]]:

* {#BenyKempfKribs06} Cédric Bény, Achim Kempf, [[David W. Kribs]], _Generalization of Quantum Error Correction via the Heisenberg Picture_, Phys. Rev. Lett. 98, 100502 – Published 7 March 2007 ([doi:10.1103/PhysRevLett.98.100502](https://doi.org/10.1103/PhysRevLett.98.100502), [arXiv:quant-ph/0608071](https://arxiv.org/abs/quant-ph/0608071))

* Cédric Bény, Achim Kempf, [[David W. Kribs]], _Quantum Error Correction of Observables_, Phys. Rev. A 76, 042303 (2007) ([arXiv:0705.1574](https://arxiv.org/abs/0705.1574))


Introduction and survey

* {#DevittNemotoMunro09} [[Simon J. Devitt]], Kae Nemoto, William J. Munro, _Quantum Error Correction for Beginners_, Rep. Prog. Phys. 76 (2013) 076001 ([arXiv:0905.2794](https://arxiv.org/abs/0905.2794))

* Simeon Ball, Aina Centelles, Felix Huber, *Quantum error-correcting codes and their geometries* ([arXiv:2007.05992](https://arxiv.org/abs/2007.05992))

* {#Steane06} [[Andrew M. Steane]], *A Tutorial on Quantum Error Correction*, in: Proceedings of the International School of Physics “Enrico Fermi”, course CLXII, "Quantum Computers,Algorithms and Chaos", 2006 ([pdf](https://www2.physics.ox.ac.uk/sites/default/files/ErrorCorrectionSteane06.pdf), [[SteaneTutorialQuantumErrorCorrection.pdf:file]]) 

* {#RowellWang17} [[Eric Rowell]], [[Zhenghan Wang]], Section 3.2.3 of: _Mathematics of Topological Quantum Computing_, Bull. Amer. Math. Soc. 55 (2018), 183-238 ([arXiv:1705.06206](https://arxiv.org/abs/1705.06206), [doi:10.1090/bull/1605](https://doi.org/10.1090/bull/1605))

* Joschka Roffe, *Quantum Error Correction: An Introductory Guide*, Contemporary Physics 2019 ([arXiv:1907.11157](https://arxiv.org/abs/1907.11157))

* {#ZhuCross20} Guanyu Zhu, Andrew Cross, *[Hardware-aware approach for fault-tolerant quantum computation](https://www.ibm.com/blogs/research/2020/09/hardware-aware-quantum/)*, IBM Research Blog, September 2, 2020

See also:

* Wikipedia, _[Quantum error correction](https://en.m.wikipedia.org/wiki/Quantum_error_correction)_

In the context of [[quantum secret sharing]]:

* {#CleveGottesmanLo99} Richard Cleve, Daniel Gottesman, Hoi-Kwong Lo, *How to share a quantum secret*, Phys. Rev. Lett. 83 (1999) 648-651 ([arXiv:quant-ph/9901025](https://arxiv.org/abs/quant-ph/9901025))

Realization in [[experiment]]:

* D. G. Cory, M. D. Price, W. Maas, [[Emanuel Knill]], [[Raymond Laflamme]], [[Wojchiek H. Zurek]], T. F. Havel, and S. S. Somaroo, *Experimental Quantum Error Correction*, Phys. Rev. Lett. 81, 2152 (1998) ([doi:10.1103/PhysRevLett.81.2152](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.81.2152))

* Adrian Cho, *[The biggest flipping challenge in quantum computing](https://www.sciencemag.org/news/2020/07/biggest-flipping-challenge-quantum-computing)*, Science News Jul. 9, 2020 

* Ming Gong et al. *Experimental exploration of five-qubit quantum error correcting code with superconducting qubits*, National Science Review, nwab011 (2021) ([doi:10.1093/nsr/nwab011](https://doi.org/10.1093/nsr/nwab011))

  survey in:

   EurekaAlert, Science China Press: *Demonstration of the universal quantum error correcting code with superconducting qubits*, March 2021 ([2021-03/scp-dot031521](https://www.eurekalert.org/pub_releases/2021-03/scp-dot031521.php))


and via methods from [[topological quantum computation]]:

* Daniel Nigg, Markus Mueller, Esteban A. Martinez, Philipp Schindler, Markus Hennrich, Thomas Monz, Miguel A. Martin-Delgado, Rainer Blatt, 

  *Experimental Quantum Computations on a Topologically Encoded Qubit*, Science 18 Jul 2014: Vol. 345, Issue 6194, pp. 302-305 ([arXiv:1403.5426](https://arxiv.org/abs/1403.5426), [doi:10.1126/science.1253742](https://science.sciencemag.org/content/345/6194/302))

and prospect:

* {#Lucero21} Erik Lucero, *[Unveiling our new Quantum AI campus](https://blog.google/technology/ai/unveiling-our-new-quantum-ai-campus/)*,  May 18, 2021


On (in-)compatibility of quantum error correction with universality of quantum gates ([[Eastin-Knill theorem]]):

* [[Bryan Eastin]], [[Emanuel Knill]], *Restrictions on Transversal Encoded Quantum Gate Sets*,  Phys. Rev. Lett. 102, 110502 (2009) ([arXiv:0811.4262](https://arxiv.org/abs/0811.4262))

* {#WVSB20} Paul Webster, Michael Vasmer, Thomas R. Scruby, Stephen D. Bartlett, *Universal Fault-Tolerant Quantum Computing with Stabiliser Codes* ([arXiv:2012.05260](https://arxiv.org/abs/2012.05260))


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

Introduction of the more general [[Majorana dimer code]]:

* [[Alexander Jahn]], [[Marek Gluza]], [[Fernando Pastawski]], [[Jens Eisert]], _Majorana dimers and holographic quantum error-correcting codes_, Phys. Rev. Research 1, 033079 (2019) ([arXiv:1905.03268](https://arxiv.org/abs/1905.03268))

Exposition and review:

* [[John Preskill]], *Is spacetime a quantum error-correcting code?*, talk at KITP 2015 ([pdf](http://theory.caltech.edu/~preskill/talks/Preskill-KITP-holographic-2015.pdf))

* {#Harlow18} [[Daniel Harlow]], _TASI Lectures on the Emergence of Bulk Physics in AdS/CFT_, PoS TASI2017 (2018) 002 ([arXiv:1802.01040](https://arxiv.org/abs/1802.01040), [doi:10.22323/1.305.0002](https://doi.org/10.22323/1.305.0002))

* [[Pratik Rath]], *Aspects of Holography And Quantum Error Correction*, 2020 ([pdf](https://digitalassets.lib.berkeley.edu/etd/ucb/text/Rath_berkeley_0028E_19810.pdf), [[RathHolographyAndQEC.pdf:file]]) 

* [[Melanie Swan]], [[Renato P dos Santos]], [[Frank Witte]], *The AdS/CFT Correspondence and Holographic Codes* ([doi:10.1142/9781786348210_0013](https://doi.org/10.1142/9781786348210_0013), [doi:10.1142/9781786348210_0014](https://www.worldscientific.com/doi/abs/10.1142/9781786348210_0014)), Part 5 in: Between Science and Economics, Volume 2: *Quantum Computing Physics, Blockchains, and Deep Learning Smart Networks*, World Scientific 2020 ([doi:10.1142/q0243](https://doi.org/10.1142/q0243))

* {#Harlow20} [[Daniel Harlow]], *Computation and Holography*, talk at [Snowmass Computational Frontier Workshop 2020](https://indico.fnal.gov/event/43829/) ([pdf](https://indico.fnal.gov/event/43829/contributions/193566/attachments/132763/163346/snowmasscomp.pdf), [[HarlowComputationHolography.pdf:file]])


* [[Alexander Jahn]], [[Jens Eisert]], _Holographic tensor network models and quantum error correction: A topical review_ ([arXiv:2102.02619](https://arxiv.org/abs/2102.02619))

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


Musings on possible implications on relations between [[quantum gravity]] and [[quantum information]]:

* {#SimonsFoundationItFromQBit} [[Simons Foundation]], *[It from Qubit: Simons Collaboration on Quantum Fields, Gravity and Information](https://www.simonsfoundation.org/mathematics-physical-sciences/it-from-qubit/)*


* Iulia Georgescu, *Strings and qubits*, Nature Reviews Physics volume 1, page 477 (2019) ([doi:s42254-019-0087-6](https://www.nature.com/articles/s42254-019-0087-6))

* Natalie Wolchover, *[How Space and Time Could Be a Quantum Error-Correcting Code](https://www.quantamagazine.org/how-space-and-time-could-be-a-quantum-error-correcting-code-20190103/)*, Quanta Magazine, Jan. 3 2019

* [[Tom Banks]], *Holographic Space-time and Quantum Information* ([arXiv:2001.08205](https://arxiv.org/abs/2001.08205))

    


[[!redirects quantum error correction code]]
[[!redirects quantum error correction codes]]

[[!redirects quantum error correcting code]]
[[!redirects quantum error correcting codes]]

[[!redirects code subspace]]
[[!redirects code subspaces]]


[[!redirects holographic quantum error correction]]

[[!redirects holographic quantum error correction code]]
[[!redirects holographic quantum error correction codes]]

[[!redirects holographic quantum error correcting code]]
[[!redirects holographic quantum error correcting codes]]


