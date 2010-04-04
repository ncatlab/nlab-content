# Commutative diagrams

## Idea

A commutative diagram is a [[diagram]] in which [[composition]] is [[path independence|path-independent]].


## Slick definition

For our purposes, a __[[diagram]]__ $D$ in a [[category]] $C$ consists of a [[directed graph]] $J$ and a [[functor]] to $C$ from the [[free category]] on $J$:
$$ J \overset{D}\to C ,\; J\;\text{a quiver}. $$
Then this diagram $D$ __commutes__ if this functor $D$ factors (up to [[natural isomorphism]]) through a [[poset]] $P$:
$$ J \to P \to C \;\cong\; J \to C ,\; P\;\text{a poset} ;$$
or equivalently (treating $C$ as a [[strict category]]) if the functor factors up to [[equality]] through a [[proset]] $Q$:
$$ J \to Q \to C \;\cong\; J \to C ,\; Q\;\text{a proset} .$$


## Elementary definition

Since it is possible to define [[functors]] in terms of commutative diagrams, we need to write down an elementary definition too.


## Links

* [Wikipedia](http://en.wikipedia.org/wiki/Commutative_diagram)
* [Mathworld](http://mathworld.wolfram.com/CommutativeDiagram.html)
* [[alternative experimental definition of commutative diagram|An Experiment]]


[[!redirects commutative diagram]]
[[!redirects commuting diagram]]
