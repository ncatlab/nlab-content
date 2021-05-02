


#Contents#
* table of contents
{:toc}


## Idea

*Quantum error corection* is concerned with ensuring the robustness of [[quantum computation]] against [[noise]] (as in classical [[error correction]]) and particularly against [[quantum noise]] and [[quantum decoherence]].

Typically, for $\mathcal{H}$ a given [[Hilbert space]] of [[quantum states]] ([[finite dimensional vector space|finite-dimensional]] in practice), a *quantum error correcting code* is a choice of [[linear subspace|linear embedding]] (the *code subspace*) of $\mathcal{H}$ into a $n$-fold [[tensor product]] (typically of copies of itself), for some [[natural number]] $n \in \mathbb{N}$:

$$
  \array{
    \mathcal{H}
    & 
      \overset{\;\;\;code\;\;\;}{
        \hookrightarrow
      }
    &
    \mathcal{H}^{(1)} 
      \otimes 
    \mathcal{H}^{(2)}
      \otimes
        \cdots
      \otimes
    \mathcal{H}^{(n)}  
  }
  \,,
$$

such that the information in $code(\psi)$ in some of the tensor factors $\mathcal{H}^{(i)}$ can be lost without obstructing the reconstruction of $\psi$.

Often one demands additional properties, such as that a given set of [[linear operators]] $O$ ([[quantum observables]]) acting on $\psi \in \mathcal{H}$ are implemented on $code(\psi)$ by combionations of operators that act non-trivially only on some of the tensor factors (and hence are unaffected by errors in the remaining factors).

## Example

### A qtrit error correcting code
 {#A3FoldqtritCode}

Simple example from [Cleve, Gottesman & Lo 99, p. 1-2](#CleveGottesmanLo99):

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

## Related concepts

* [[quantum computing]], [[topological quantum computing]]

* [[quantum secret sharing]]

* [[tensor network]]

## References

### General

* Simon J. Devitt, Kae Nemoto, William J. Munro, _Quantum Error Correction for Beginners_, Rep. Prog. Phys. 76 (2013) 076001 ([arXiv:0905.2794](https://arxiv.org/abs/0905.2794))

* [[Eric Rowell]], [[Zhenghan Wang]], Section 3.2.3 of: _Mathematics of Topological Quantum Computing_, Bull. Amer. Math. Soc. 55 (2018), 183-238 ([arXiv:1705.06206](https://arxiv.org/abs/1705.06206), [doi:10.1090/bull/1605](https://doi.org/10.1090/bull/1605))

See also

* Wikipedia, _[Quantum error correction](https://en.m.wikipedia.org/wiki/Quantum_error_correction)_

In the context of [[quantum secret sharing]]:

* {#CleveGottesmanLo99} Richard Cleve, Daniel Gottesman, Hoi-Kwong Lo, *How to share a quantum secret*, Phys. Rev. Lett. 83 (1999) 648-651 ([arXiv:quant-ph/9901025](https://arxiv.org/abs/quant-ph/9901025))

### Operator algebraic Heisenberg picture

[[operator algebra|Operator algebraic]] formulation of quantum error correction in the [[Heisenberg picture]]:

* {#BenyKempfKribs06} Cédric Bény, Achim Kempf, David W. Kribs, _Generalization of Quantum Error Correction via the Heisenberg Picture_, Phys. Rev. Lett. 98, 100502 – Published 7 March 2007 ([doi:10.1103/PhysRevLett.98.100502](https://doi.org/10.1103/PhysRevLett.98.100502), [arXiv:quant-ph/0608071](https://arxiv.org/abs/quant-ph/0608071))

* Cédric Bény, Achim Kempf, David W. Kribs, _Quantum Error Correction of Observables_, Phys. Rev. A 76, 042303 (2007) ([arXiv:0705.1574](https://arxiv.org/abs/0705.1574))

### Via holographic tensor networks

Interpretation of [[tensor networks]] encoding [[holographic entanglement entropy]] as [[quantum error correcting codes]] (using [Bény-Kempf-Kribs 06](#BenyKempfKribs06)):

* {#ADH14} [[Ahmed Almheiri]], [[Xi Dong]], [[Daniel Harlow]], _Bulk Locality and Quantum Error Correction in AdS/CFT_, JHEP 1504:163,2015 ([arXiv:1411.7041](https://arxiv.org/abs/1411.7041), <a href="https://doi.org/10.1007/JHEP04(2015)163">doi:10.1007/JHEP04(2015)163</a>)

* {#PYHP15} Fernando Pastawski, Beni Yoshida, [[Daniel Harlow]], [[John Preskill]], _Holographic quantum error-correcting codes: Toy models for the bulk/boundary correspondence_, JHEP 06 (2015) 149 ([arXiv:1503.06237](https://arxiv.org/abs/1503.06237))

Review:

* {#Harlow18} [[Daniel Harlow]], _TASI Lectures on the Emergence of Bulk Physics in AdS/CFT_, PoS TASI2017 (2018) 002 ([arXiv:1802.01040](https://arxiv.org/abs/1802.01040), [doi:10.22323/1.305.0002](https://doi.org/10.22323/1.305.0002))

* Alexander Jahn, [[Jens Eisert]], _Holographic tensor network models and quantum error correction: A topical review_ ([arXiv:2102.02619](https://arxiv.org/abs/2102.02619))


See also

* Alexander Jahn, Marek Gluza, Fernando Pastawski, [[Jens Eisert]], _Majorana dimers and holographic quantum error-correcting codes_, Phys. Rev. Research 1, 033079 (2019) ([arXiv:1905.03268](https://arxiv.org/abs/1905.03268))

* [[Ahmed Almheiri]], _Holographic Quantum Error Correction and the Projected Black Hole Interior_ ([arXiv:1810.02055](https://arxiv.org/abs/1810.02055))


[[!redirects quantum error correction code]]
[[!redirects quantum error correction codes]]

[[!redirects quantum error correcting code]]
[[!redirects quantum error correcting codes]]

