


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

### Quantum error correcting codes

The simple but important special case of passive correction of erasures may be  handled by *quantum error correcting codes*:

Recall that a classical [[error correcting code]] on a [[finite set]] of states $S$ is, typically, a choice of [[injection]] of $S$ into a [[Cartesian product]] with itself

$$
  S \overset{\;\;\;\;\;\;\;\;}{\hookrightarrow} S \times \cdots \times S
$$

(often considered in the form of [[linear codes]], but classical nonetheless). In [[quantum physics]] the [[Cartesian product]] of sets of states is replaced by the [[tensor product of vector spaces|tensor product]] of [[Hilbert spaces]].

For $\mathcal{H}$ a given [[Hilbert space]] of [[quantum states]] ([[finite dimensional vector space|finite-dimensional]] in practice), a *quantum error correcting code* is a choice of [[linear subspace|linear embedding]] (the *code subspace*) of $\mathcal{H}$ into a larger Hilbert spaces, typically an  $n$-fold [[tensor product]] of copies of $H$:

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

Original articles:

* {#Shor95} [[Peter W. Shor]], *Scheme for reducing decoherence in quantum computer memory*, Phys. Rev. A 52, R2493(R) 1995 ([doi:10.1103/PhysRevA.52.R2493](https://doi.org/10.1103/PhysRevA.52.R2493))

* {#Steane96} [[Andrew M. Steane]], *Error Correcting Codes in Quantum Theory*, Phys. Rev. Lett. 77, 793 1996 ([doi:10.1103/PhysRevLett.77.793](https://doi.org/10.1103/PhysRevLett.77.793))

* {#CalderbankShor96} [[Robert Calderbank]], [[Peter W. Shor]], *Good Quantum Error-Correcting Codes Exist*, Phys. Rev. A, Vol. 54, No. 2, pp. 1098-1106, 1996 ([doi:10.1103/PhysRevA.54.1098](https://doi.org/10.1103/PhysRevA.54.1098))

* {#LMPZ96} [[Raymond Laflamme]], Cesar Miquel, Juan Pablo Paz, [[Wojciech H. Zurek]], *Perfect Quantum Error Correction Code*, Phys. Rev. Lett., 77:198, 1996 ([arXiv:quant-ph/9602019](https://arxiv.org/abs/quant-ph/9602019))


* {#BDSW96} Charles H. Bennett, David P. DiVincenzo, John A. Smolin, William K. Wootters, *Mixed State Entanglement and Quantum Error Correction*, Phys. Rev. A54:3824-3851, 1996 ([doi:10.1103/PhysRevA.54.3824](https://doi.org/10.1103/PhysRevA.54.3824))

* [[Andrew M. Steane]], *Multiple Particle Interference and Quantum Error Correction*,  	Proc. Roy. Soc. Lond. A452 (1996) 2551 ([arXiv:quant-ph/9601029](https://arxiv.org/abs/quant-ph/9601029))


Further original developments:

* [[Emanuel Knill]], [[Raymond Laflamme]], *A Theory of Quantum Error-Correcting Codes*, Phys. Rev. Lett. 84:2525-2528, 2000 ([arXiv:quant-ph/9604034](https://arxiv.org/abs/quant-ph/9604034))

[[operator algebra|Operator algebraic]] formulation of quantum error correction:

* [[David Kribs]], [[Raymond Laflamme]], [[David Poulin]], *A Unified and Generalized Approach to Quantum Error Correction*, Phys. Rev. Lett. 94, 180501 (2005) ([arXiv:quant-ph/0412076](https://arxiv.org/abs/quant-ph/0412076))

* [[David W. Kribs]], [[Raymond Laflamme]], [[David Poulin]], [[Maia Lesosky]], *Operator quantum error correction*, Quant. Inf. & Comp., 6 (2006), 383-399 ([arXiv:quant-ph/0504189](https://arxiv.org/abs/quant-ph/0504189))

on [[quantum observables]]:

* {#BenyKempfKribs06} Cédric Bény, Achim Kempf, [[David W. Kribs]], _Generalization of Quantum Error Correction via the Heisenberg Picture_, Phys. Rev. Lett. 98, 100502 – Published 7 March 2007 ([doi:10.1103/PhysRevLett.98.100502](https://doi.org/10.1103/PhysRevLett.98.100502), [arXiv:quant-ph/0608071](https://arxiv.org/abs/quant-ph/0608071))

* Cédric Bény, Achim Kempf, [[David W. Kribs]], _Quantum Error Correction of Observables_, Phys. Rev. A 76, 042303 (2007) ([arXiv:0705.1574](https://arxiv.org/abs/0705.1574))


Introductions:

* {#DevittNemotoMunro09} Simon J. Devitt, Kae Nemoto, William J. Munro, _Quantum Error Correction for Beginners_, Rep. Prog. Phys. 76 (2013) 076001 ([arXiv:0905.2794](https://arxiv.org/abs/0905.2794))

* Simeon Ball, Aina Centelles, Felix Huber, *Quantum error-correcting codes and their geometries* ([arXiv:2007.05992](https://arxiv.org/abs/2007.05992))

* {#Steane06} [[Andrew M. Steane]], *A Tutorial on Quantum Error Correction*, in: Proceedings of the International School of Physics “Enrico Fermi”, course CLXII, "Quantum Computers,Algorithms and Chaos", 2006 ([pdf](https://www2.physics.ox.ac.uk/sites/default/files/ErrorCorrectionSteane06.pdf), [[SteaneTutorialQuantumErrorCorrection.pdf:file]]) 

* {#RowellWang17} [[Eric Rowell]], [[Zhenghan Wang]], Section 3.2.3 of: _Mathematics of Topological Quantum Computing_, Bull. Amer. Math. Soc. 55 (2018), 183-238 ([arXiv:1705.06206](https://arxiv.org/abs/1705.06206), [doi:10.1090/bull/1605](https://doi.org/10.1090/bull/1605))

* Joschka Roffe, *Quantum Error Correction: An Introductory Guide*, Contemporary Physics 2019 ([arXiv:1907.11157](https://arxiv.org/abs/1907.11157))


See also

* Wikipedia, _[Quantum error correction](https://en.m.wikipedia.org/wiki/Quantum_error_correction)_

In the context of [[quantum secret sharing]]:

* {#CleveGottesmanLo99} Richard Cleve, Daniel Gottesman, Hoi-Kwong Lo, *How to share a quantum secret*, Phys. Rev. Lett. 83 (1999) 648-651 ([arXiv:quant-ph/9901025](https://arxiv.org/abs/quant-ph/9901025))

Implementation in [[experiment]]:

* D. G. Cory, M. D. Price, W. Maas, [[Emanuel Knill]], [[Raymond Laflamme]], [[Wojchiek H. Zurek]], T. F. Havel, and S. S. Somaroo, *Experimental Quantum Error Correction*, Phys. Rev. Lett. 81, 2152 (1998) ([doi:10.1103/PhysRevLett.81.2152](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.81.2152))


### Via holographic tensor networks

On quantum error correction in terms of [[tensor networks]]:

* {#FerrisPoulin13} Andrew J. Ferris, [[David Poulin]], *Tensor Networks and Quantum Error Correction*, Phys. Rev. Lett. 113, 030501 (2014) ([arXiv:1312.4578](https://arxiv.org/abs/1312.4578))


Interpretation of [[tensor networks]] encoding [[holographic entanglement entropy]] as [[quantum error correcting codes]] (using [Bény-Kempf-Kribs 06](#BenyKempfKribs06)):

* {#ADH14} [[Ahmed Almheiri]], [[Xi Dong]], [[Daniel Harlow]], _Bulk Locality and Quantum Error Correction in AdS/CFT_, JHEP 1504:163,2015 ([arXiv:1411.7041](https://arxiv.org/abs/1411.7041), <a href="https://doi.org/10.1007/JHEP04(2015)163">doi:10.1007/JHEP04(2015)163</a>)


and concrete implementation by the [[HaPPY code]]:

* {#PYHP15} Fernando Pastawski, Beni Yoshida, [[Daniel Harlow]], [[John Preskill]], _Holographic quantum error-correcting codes: Toy models for the bulk/boundary correspondence_, JHEP 06 (2015) 149 ([arXiv:1503.06237](https://arxiv.org/abs/1503.06237))

Review:

* {#Harlow18} [[Daniel Harlow]], _TASI Lectures on the Emergence of Bulk Physics in AdS/CFT_, PoS TASI2017 (2018) 002 ([arXiv:1802.01040](https://arxiv.org/abs/1802.01040), [doi:10.22323/1.305.0002](https://doi.org/10.22323/1.305.0002))

see also

* [[Ahmed Almheiri]], _Holographic Quantum Error Correction and the Projected Black Hole Interior_ ([arXiv:1810.02055](https://arxiv.org/abs/1810.02055))


Introduction of the more general [[Majorana dimer code]]:

* [[Alexander Jahn]], [[Marek Gluza]], [[Fernando Pastawski]], [[Jens Eisert]], _Majorana dimers and holographic quantum error-correcting codes_, Phys. Rev. Research 1, 033079 (2019) ([arXiv:1905.03268](https://arxiv.org/abs/1905.03268))

Review:

* [[Alexander Jahn]], [[Jens Eisert]], _Holographic tensor network models and quantum error correction: A topical review_ ([arXiv:2102.02619](https://arxiv.org/abs/2102.02619))


[[!redirects quantum error correction code]]
[[!redirects quantum error correction codes]]

[[!redirects quantum error correcting code]]
[[!redirects quantum error correcting codes]]

[[!redirects code subspace]]
[[!redirects code subspaces]]

