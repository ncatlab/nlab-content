
## Idea

In [[perturbative quantum field theory]] the _BV-operator_ is the difference between the action of the [[BV differential]] on the [[algebra of observables]] before and after [[quantization]].


In [[higher algebra]], under the identification of a [[BV-algebra]] with the [[chain homology]] of a [[little k-cubes operad|E2-algebra]], the _BV-operator_ corresponds to the operation of rotating a little disk around.

For the relation between the two see _[[relation between BV and BD]]_.

## In perturbative quantum field theory

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] and let $\mathbf{L}' - \mathbf{L}'_{BRST}$ be its [[Lagrangian density]] after [[gauge fixing]], so that the gauge-fixed [[local BRST complex|local BV-BRST differential]] is given by the [[local antibracket]] as

$$
  s' 
    \;=\;
  \left\{ -\mathbf{L}' + \mathbf{L}'_{BRST}, - \right\}
$$

This descends to [[regular polynomial observables]]:

$$
  \int \left\{ -\mathbf{L}'(x) + \mathbf{L}'_{BRST}(x), - \right\}
$$

By definition of [[gauge fixing]] the [[equation of motion]] for $\mathbf{L}'$ are [[Green hyperbolic differential equations|Green hyperbolic]] and hence admit, in particular, a _[[Wightman propagator]]_ $\Delta_H$ and a [[Feynman propagator]] $\Delta_F$.  The [[star products]] with respect to these ([this def.](star+product#PropagatorStarProduct)) are, respectively, the [[Wick algebra]] product 

$$
  A_1 \star_H A_2 
  \;\coloneqq\;
  ((-) \cdot (-))
  \circ
  \exp\left(
    \hbar \int_\Sigma \Delta_{H}(x,y)^{a b} \frac{\delta}{\delta \phi^a(x)} \otimes \frac{\delta}{\delta \phi^b(y)}
  \right)
  (A_1 \otimes A_2)
$$

and the [[time-ordered product]]

$$
  A_1 \star_F A_2 
  \;\coloneqq\;
  ((-) \cdot (-))
  \circ
  \exp\left(
    \hbar \int_\Sigma \Delta_{F}(x,y)^{a b} \frac{\delta}{\delta \phi^a(x)} \otimes \frac{\delta}{\delta \phi^b(y)}
  \right)
  (A_1 \otimes A_2)
  \,,
$$


Since the [[Feynman propagator]] is symmetric, the latter [[time ordered product]] on [[regular polynomial observables]] is [[isomorphism|isomorphic]] (via [this prop.](star+product#SymmetricContribution)), on [[regular polynomial observables]], to the pointwise product, via

$$
  \mathcal{T}A
  \;\coloneqq\;
  \exp\left(
    \tfrac{1}{2}
    \hbar 
    \int_\Sigma \Delta_F(x,y)^{a b} \frac{\delta^2}{\delta \Phi^a(x) \delta \Phi^b(y)}
  \right)
  A
$$

as

$$
  A_1 \star_{F} A_2
  \;=\;
  \mathcal{T}( \mathcal{T}^{-1}A_1 \cdot \mathcal{T}^{-1}A_2 )
$$


[[!redirects BV-operators]]