

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

In [[relativistic field theory|relativistic]] [[perturbative quantum field theory]], the _time-ordered product_ is a product on [[observables]] which is such that observables which evaluate [[field histories]] not in the [[past]] of some [[event]] are ordered to the left of those which do, before taking their [[Wick algebra]] product. For example for point-evaluation [[field observables]] and distinct [[events]] $x,y \in \Sigma$ the time-ordered product is defined by

$$
  T(\mathbf{\Phi}^a(x) \mathbf{\Phi}^b(y))
  \;\coloneqq\;
  \left\{
    \array{
      \mathbf{\Phi}^a(x) \mathbf{\Phi}^a(y) 
        &\vert& 
      x\, \text{not in the past of}\ y
      \\
      \mathbf{\Phi}^a(y) \mathbf{\Phi}^a(x) &\vert& \text{otherwise} 
    }
  \right.
$$



This may be understood as arising from the [[causal additivity]]-[[axiom]] of the [[perturbative S-matrix]]. It generalizes the 1-dimensional time-ordering (path ordering) of the [[Dyson series]] in [[quantum mechanics]].

More precisely, the time-ordere product is a  [[commutative algebra]]-[[structure]] on the [[microcausal polynomial observables]] of a [[free field theory|free]] [[Lagrangian field theory]] equipped with a [[vacuum state]] ([[Hadamard state]]) which on [[regular polynomial observables]] given on the [[regular polynomial observables]] by the [[star product]] which is induced (via [this def.](star+product#PropagatorStarProduct)) by the [[Feynman propagator]] and which is extended from there, in the sense of [[extensions of distributions]], to all [[microcausal polynomial observables]]. (This extension is the "[[renormalization]]" of the time-ordered product).

## Related concepts

[[!include products in pQFT -- table]]

$\,$

[[!include Wick algebra -- table]]


## References

See the references at _[[S-matrix]]_

[[!redirects time-ordered products]]

[[!redirects time ordered product]]
[[!redirects time ordered products]]
