

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

In [[perturbative quantum field theory]] formulated in terms of [[BV-BRST formalism]], the _classical master equation_ expresses the nilpotency of the [[BV-differential]] before [[quantization]], with the latter regarded as a [[Hamiltonian vector field]] with respect to the _[[antibracket]]_ $\{-,-\}$, for "Hamiltonian" the BV-BRST-extended [[action functional]] "S + S_{BRST}":

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


## Details

> under construction

Let $(E_{\text{BV-BST}},\mathbf{L}')$ be a [[gauge fixing|gauge fixed]] [[free field theory|free]] [[Lagrangian field theory]] with global [[BV-differential]]

$$
  \{-S', -\}
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ] 
$$

and with [[Feynman propagator]] $\Delta_F$.

the [[perturbative S-matrix]] on [[regular polynomial observables]]

$$
  \mathcal{S} 
  \;\colon\;
  PolyObs(E_{\text{BV-BRST}})_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E_{\text{BV-BRST}})_{reg}((\hbar))
$$

is

$$
  \mathcal{S}(S_{int})
  =
  \exp_{\star_F}(\tfrac{1}{i \hbar} S_{int})
  \coloneqq
  1 
    + 
  \tfrac{1}{\i \hbar} S_{int} 
    +
  \tfrac{1}{2}
  \tfrac{1}{(i \hbar)^2} 
  S_{int} \star_F S_{int}
  + 
  \cdots
$$

[[quantum Møller operator]] from [[Bogoliubov's formula]]

$$
  \mathcal{R}
    \;\coloneqq\;
  \mathcal{S}(S_{int})^{-1} 
    \star_H 
  (\mathcal{S}(S_{int}) \star_F (-))
$$

its inverse:

$$
  \mathcal{R}^{-1}
  \;=\;
  \mathcal{S}(-S_{int}) \star_F ( \mathcal{S}(S_{int}) \star(-) )
$$

notice the implicit dependencies

| symbol | meaning | depends on choice of |
|--------|---------|----------------------|
| $\mathcal{T}$ | [[time-orered product|time-ordering]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] |
| $\mathcal{S}$ | [[S-matrix]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] |
| $\mathcal{R}$ | [[quantum Møller operator]] | [[free field theory|free]] [[Lagrangian density]] and [[Wightman propagator]] and [[interaction]] |



isomorphism to interacting star product on regular polynomial observables:

$$
  A_1 \star_{int} A_2
  \;\coloneqq\;
  \mathcal{R}_{S_{int}}
  \left(
    \mathcal{R}_{S_{int}}^{-1}(A_1) 
     \star_H 
    \mathcal{R}_{S_{int}}^{-1}(A_2)
  \right)
$$

(e.g. [Fredenhagen-Rejzner 11b, (19)](#FredenhagenRejzner11b))

interacting quantum BV-differential:

$$
  \mathcal{R}_V \circ \{-S', (-)\} \circ \mathcal{R}_V^{-1}
$$

([Rejzner 11, (5.38)](#Rejzner11))

proposition:

if the [[perturbative S-matrix]] for [[interaction]] $S_{int}$ is $BV$-closed 

$$
  \{-S', \mathcal{S}(S_{int})\} = 0
$$

then the interacting quantum BV-differential is equal to

$$
  \mathcal{S}(-S_{int}) \star_F \{-S', \mathcal{S}(S_{int} \star_F  (-))\}
$$

proof:

$$
  \{-S', \mathcal{R}_{S_{int}}(A)\}
  \coloneqq
  \left\{
   -S', 
  \right\}
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
