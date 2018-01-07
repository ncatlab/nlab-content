

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[perturbative quantum field theory]] formulated in terms of [[BV-BRST formalism]], the _classical master equation_ expresses the nilpotency of the [[BV-differential]] before [[quantization]], with the latter regarded as a [[Hamiltonian vector field]] with respect to the _[[antibracket]]_ $\{-,-\}$, for "Hamiltonian" the BV-BRST [[action functional]]:

$$
  \left( 
    s_{BV}
  \right)^2 = 0
  \phantom{AA}
  \Leftrightarrow
  \phantom{AA}
  \left( \{S + S_{BRST},(-)\}\right)^2 = 0
  \phantom{AA}
  \Leftrightarrow
  \phantom{AA}
  \{S + S_{BRST}, S + BRST\} = 0
  \,.
$$

The _quantum  master equation_ is the version of this equation after [[quantization]], in which case the the [[BV-differential]] picks up a quantum correction of order $\hbar$ ([[Planck's constant]]) by the [[BV-operator]] $\Delta_{BV}$:

$$
  \left(\, \{S + S_{BRST},(-)\} + i \hbar \Delta_{BV} \, \right)^2 = 0
 \,.
$$



## Related concepts

* [[master Ward identity]]


## References

Discussion in the rigorous context of [[relativistic field theory]] in [[causal perturbation theory]]/[[perturbative AQFT]] is in:

* {#FredenhagenRejzner11a} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in the functional approach to classical field theory_, Commun. Math. Phys. 314(1), 93&#8211;127 (2012) ([arXiv:1101.5112](https://arxiv.org/abs/1101.5112))

* {#FredenhagenRejzner11b} [[Klaus Fredenhagen]], [[Kasia Rejzner]], _Batalin-Vilkovisky formalism in perturbative algebraic quantum field theory_, Commun. Math. Phys. 317(3), 697&#8211;725 (2012) ([arXiv:1110.5232](https://arxiv.org/abs/1110.5232))

* {#Rejzner11} [[Katarzyna Rejzner]], _Batalin-Vilkovisky formalism in locally covariant field theory_ ([arXiv:1111.5130](https://arxiv.org/abs/1111.5130))

* {#Rejzner13} [[Katarzyna Rejzner]], _Remarks on local symmetry invariance in perturbative algebraic quantum field theory_ ([arXiv:1301.7037](https://arxiv.org/abs/1301.7037))

and surveyed in

* {#Rejzner16} [[Kasia Rejzner]], section 7 of _Perturbative algebraic quantum field theory_ Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))


[[!redirects classical master equation]]
