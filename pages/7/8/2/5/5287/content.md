
> under construction

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

In [[perturbative quantum field theory]] the _BV-operator_ is the difference between the action of the [[BV differential]] on the [[algebra of observables]] before and after [[quantization]].


In [[higher algebra]], under the identification of a [[BV-algebra]] with the [[chain homology]] of a [[little k-cubes operad|E2-algebra]], the _BV-operator_ corresponds to the operation of rotating a little disk around.

For the relation between the two see _[[relation between BV and BD]]_.

## In perturbative quantum field theory

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] admitting a [[gauge fixing]], and let $\mathbf{L}' - \mathbf{L}'_{BRST}$ be its BV-BRST [[Lagrangian density]] after [[gauge fixing]] ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)), so that the gauge-fixed [[local BRST complex|local BV-BRST differential]] is given by the [[local antibracket]] as

$$
  s' 
    \;=\;
  \left\{ -\mathbf{L}' + \mathbf{L}'_{BRST}, - \right\}
$$

The corresponding global BV-BRST differential on [[regular polynomial observables]] is ([this def.](A+first+idea+of+quantum+field+theory#ComplexBVBRSTGlobal))

$$
  \left\{ -S' + S'_{BRST} \;,\; -\right\}
  \;\coloneqq\;
  \left\{ -\tau_\Sigma\mathbf{L}'(x) + \tau_\Sigma\mathbf{L}'_{BRST}(x), - \right\} 
  \;\colon\;
  PolyObs(E)_{reg} \longrightarrow PolyObs(E)_{reg}
  \,.
$$

By definition of [[gauge fixing]] ([this def.](A+first+idea+of+quantum+field+theory#GaugeFixingLagrangianDensity)), the [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] for $\mathbf{L}'$ are [[Green hyperbolic differential equations|Green hyperbolic]] and hence have a [[causal propagator]] $\Deta = \Delta_+ - \Delta_-$ and admit a compatible _[[Wightman propagator]]_ $\Delta_H = \tfrac{i}{2}(\Delta_+ - \Delta_-) + H$ and the corresponding [[Feynman propagator]] $\Delta_F \coloneqq \tfrac{i}{2}(\Delta_+ + \Delta_-) + H$.  The [[star products]] with respect to these ([this def.](star+product#PropagatorStarProduct)) on [[regular polynomial observables]] 

$$
  \star_H, \star_F
  \;\colon\;
  PolyObs(E)_{reg}[ [\hbar] ]
    \longrightarrow
  PolyObs(E)_{reg}[ [\hbar] ]
$$

are, respectively, the [[Wick algebra]] product ([[operator product]], see [this def.](Wick+algebra#NormalOrderedProductNotation))

$$
  A_1 A_2
  \;\coloneqq\;
  A_1 \star_H A_2 
  \;\coloneqq\;
  ((-) \cdot (-))
  \circ
  \exp\left(
    \hbar 
    \underset{\Sigma \times \Sigma}{\int}
      \Delta_{H}(x,y)^{a b} 
      \frac{\delta}{\delta \mathbf{\Phi}^a(x)} 
        \otimes 
      \frac{\delta}{\delta \mathbf{\Phi}^b(y)}
      \, dvol_\Sigma(x) \, dvol_\Sigma(y)
  \right)
  (A_1 \otimes A_2)
$$

and the [[time-ordered product]] (see again [this def.](Wick+algebra#NormalOrderedProductNotation))

$$
  T(A_1 A_2)
  \;\coloneqq\;
  A_1 \star_F A_2 
  \;\coloneqq\;
  ((-) \cdot (-))
  \circ
  \exp\left(
    \hbar 
    \underset{\Sigma \times \Sigma}{\int}
      \Delta_{F}(x,y)^{a b} 
      \frac{\delta}{\delta \mathbf{\Phi}^a(x)} 
        \otimes 
      \frac{\delta}{\delta \mathbf{\Phi}^b(y)}
      \, dvol_\Sigma(x)\, dvol_\Sigma(y)
  \right)
  (A_1 \otimes A_2)
  \,,
$$

Since the [[Feynman propagator]] is symmetric ([this prop.](A+first+idea+of+quantum+field+theory#SymmetricFeynmanPropagator)), the latter [[time ordered product]] on [[regular polynomial observables]] is [[isomorphism|isomorphic]] (via [this prop.](star+product#SymmetricContribution)) to the pointwise product, via

$$
  \mathcal{T}A
  \;\coloneqq\;
  \exp\left(
    \tfrac{1}{2}
    \hbar 
    \underset{\Sigma}{\int} 
     \Delta_F(x,y)^{a b} 
     \frac{\delta^2}{\delta \mathbf{\Phi}^a(x) \delta \mathbf{\Phi}^b(y)}
  \right)
  A
$$

as

$$
  A_1 \star_{F} A_2
  \;=\;
  \mathcal{T}( \mathcal{T}^{-1}A_1 \cdot \mathcal{T}^{-1}A_2 )
$$

The _BV-operator_ $\Delta$ on [[regular polynomial observables]] is, up to a prefactor, the difference between the gauge-fixed [[BV-differential]] $s'$ from above with its transformation under this isomorphism:

$$
  i \hbar \Delta 
    \coloneqq
  \mathcal{T} \circ 
  \left\{ -S',(-) \right\} 
  \circ \mathcal{T}^{-1}
  -
  \left\{ -S',(-) \right\}
  \,.
$$

Assume that all [[field bundles]] are [[trivial vector bundles]], then 

$$
  \Delta 
  \;=\;
  \int \pm \frac{\delta}{\delta \Phi^a(x)} \frac{\delta}{\delta \Phi^{\ddagger}_a(y)}
$$

([Fredenhagen-Rejzner 11](#FredenhagenRejzner11))

To see this:

By definition $\mathbf{L}'$ is independent of antifields, so that 

$$
  \begin{aligned}
    \left\{ -S', -\right\}
    & =
    \underset{\Sigma}{\int}
    j^{\infty}\left(\mathbf{\Phi}\right)^\ast
    \left(
      \frac{\overset{\leftarrow}{\delta}_{EL} L}{\delta \phi^a}
    \right)(x) 
    \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_a(x)} 
    \,
    dvol_\Sigma(x)
    \\
    & =
    \underset{a}{\sum}
      (-1)^{deg(\phi^a)}
    \underset{}{\int}
      (P\mathbf{\Phi})_a(x)
      \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_a(x)}
    \,
    dvol_\Sigma(x)
  \end{aligned}
$$

Hence 

$$
  \label{AAA}
  \begin{aligned}
    \mathcal{T} \circ \left\{ -S,-\right\} \circ \mathcal{T}^{-1}
    & =
    \phantom{+}
    \left\{ -S , -\right\}
    \\
    &
    \phantom{=}
    +
    \left[
      \tfrac{1}{2}\hbar 
      \underset{\Sigma \times \Sigma}{\int} 
      \Delta_F^{a b}(x,y)
      \frac{\delta^2}{\delta \mathbf{\Phi}^a(x) \delta \mathbf{\Phi}^b(y)}
      \, dvol_\Sigma(x)
      \, dvol_\Sigma(y)
      \;,\;
      \underset{a}{\sum}
      (-1)^{deg(\phi^a)}
      \underset{\Sigma}{\int}
        (P\mathbf{\Phi})_a(x)
        \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_a(x)}
      \,
      dvol_\Sigma(x)
    \right]
   \\
   & =
   \left\{ -S', -\right\}
   \\
   & \phantom{=}
   +
   \underset{a}{\sum} 
    (-1)^{deg(\phi^a)}
   \underset{\Sigma \times \Sigma}{\int} 
     \underset{ =  i \delta(x-y) }{\underbrace{P_x \Delta_F(x,y)}}
     \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
     \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_a(y)}
    \, dvol_\Sigma(x)
    \, dvol_\Sigma(y)
    \\
   & = \left\{ -S', -\right\} 
   + i \hbar 
   \underset{a}{\sum}
   (-1)^{deg(\phi^a)}
   \underset{\Sigma}{\int}
    \frac{\delta}{\delta \mathbf{\Phi}^a(x)}
    \frac{\delta}{\delta \mathbf{\Phi}^\ddagger_a(x)}
    \,
    dvol_\Sigma(x)
  \end{aligned}
$$

Here under the brace we used that the [[Feynman propagator]] is $+i$ times a [[Green function]] for the [[Klein-Gordon equation]] ([this cor.](A+first+idea+of+quantum+field+theory#GreenFunctionFeynmanPropagator))

## References

The understanding of the BV-operator in the rigorous formulation [[perturbative quantum field theory]] via [[causal perturbation theory]]/[[perturbative AQFT]] is due to 

* {#FredenhagenRejzner11} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Batalin-Vilkovisky formalism in perturbative algebraic quantum field theory_, Commun. Math. Phys. (2013) 317: 697 ([arXiv:1110.5232](https://arxiv.org/abs/1110.5232), [doi:10.1007/s00220-012-1601-1](https://doi.org/10.1007/s00220-012-1601-1))

* {#Rejzner11} [[Katarzyna Rejzner]], section 5.1.2 of _Batalin-Vilkovisky formalism in locally covariant field theory_ ([arXiv:1111.5130](https://arxiv.org/abs/1111.5130))

surveyed in

* {#Rejzner16} [[Katarzyna Rejzner]], section 7.3 of _[[Perturbative Algebraic Quantum Field Theory]]_, Mathematical Physics Studies, Springer 2016 ([web](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))


[[!redirects BV-operators]]