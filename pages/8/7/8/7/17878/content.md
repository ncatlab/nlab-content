

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### Differential graded-commutative algebra

A _differential graded-commutative algebra_ (also _DGCA_ or _dgca_, for short) is a [[differential-graded algebra]] which is [[supercommutative superalgebras|supercommutative]] in that for $v,w$ any two elements in homogeneous degree $deg(v), deg(w) \in \mathbb{Z}$, respectively, then  the product in the algebra satisfies

$$
  v w \;=\; (-1)^{deg(v) deg(w)} w v 
  \,.
$$

Equivalently this is a [[commutative monoid]] in the [[symmetric monoidal category|symmetric monoidal]] [[category of chain complexes]] of [[vector spaces]] equipped with the [[tensor product of chain complexes]].

### Differential graded-commutative superalgebra
 {#DifferentialGradedCommutativeSuperalgebra}

More generally, a _differential graded commutative superalgebra_ $(A,d) \in dgcSAlg$ is a [[commutative monoid]] in the [[symmetric monoidal category|symmetric monoidal]] [[category of chain complexes of super vector spaces]].

There are (at least) two such symmetric monoidal structures $\tau_{Deligne}$ and $\tau_{Bernst}$ ([this Prop.](chain+complex+in+super+vector+spaces#SymmetricStructureOnCategoryOfChainComplexesOfSuperVectorSpaces)). While equivalent ([this Prop.](chain+complex+in+super+vector+spaces#EquivalenceTwoSymmetricMonoidalStructuresOnChSuperVect)) these yield two superficially different [[signs in supergeometry|sign rules]] for differential graded-commutative superalgebras:

   1. for $a,b \in A$ two elements of homogeous degree $(n_a, \sigma_a), (n_b, \sigma_b) \in \mathbb{Z} \times \mathbb{Z}/2$, respectively, we have

1. in _Deligne's convention_


   $a b = (-1)^{n_a n_b + \sigma_a \sigma_b} \, b a$

1. in _Berstein's convention_

   $a b = (-1)^{ (n_a + \sigma_a)(n_b + \sigma_b) } \, b a$


While in both cases the [[differential]] satisfies.

$$ 
  d (a b) = (d a) b + (-1)^{n_1} a (d b)
  \,.
$$

[[!include sign rules in homological superalgebra -- table]]

Restricted tro bidegree $(0,-)$ both of these sign rules yield a _[[commutative superalgebra]]_, which restricted to $(-,even)$ thy yield a [[differential graded-commutative algebra]].

## Examples

* The [[de Rham algebra]] of [[differential forms]] on a [[smooth manifold]] is a differential-graded commutative algebra. The algebra of [[super differential forms]] on a [[supermanifold]] is a differential-graded commutative superalgebra.

* The dg-algebra of [[polynomial differential forms]] on an [[n-simplex]];

The following are [[semifree differential graded-commutative algebras]]:

* A [[Sullivan algebra]].

* The [[Chevalley-Eilenberg algebra]] of a [[Lie algebra]] or more generally of an [[L-infinity algebra]] or [[Lie infinity-algebroid|L-infinity algebroid]] is a differential-graded-commutative algebra, that of a [[super L-infinity algebra]] is a differential graded-commutative superalgebra.

## Related concepts

* [[category of dgc-algebras]]

* [[dgc-coalgebra]]

* [[model structure on differential graded-commutative algebras]]

* [[model structure on differential graded-commutative superalgebras]]


* [[rational homotopy theory]]

* [[monoidal Dold-Kan correspondence]]

* [geometry of physics -- superalgebra -- Z-graded commutative superalgebra](https://ncatlab.org/nlab/show/geometry+of+physics+--+superalgebra#ZGradedSupercommutativeSuperalgebra)

[[!redirects differential graded-commutative algebras]]

[[!redirects DGCA]]
[[!redirects DGCAs]]

[[!redirects CDGA]]
[[!redirects CDGAs]]

[[!redirects dgca]]
[[!redirects dgca-s]]

[[!redirects dgc-algebra]]
[[!redirects dgc-algebras]]

[[!redirects cdga]]
[[!redirects cdga-s]]

[[!redirects differential graded-commutative superalgebra]]
[[!redirects differential graded-commutative superalgebras]]
