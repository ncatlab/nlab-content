

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

More generally, a _differential graded commutative superalgebra_ $(A,d) \in dgcSAlg$ is a [[commutative monoid]] in the [[symmetric monoidal category|symmetric monoidal]] [[category of chain complexes]] of [[super vector spaces]].

This means that $(A,d)$ has a $\mathbb{Z} \times \mathbb{Z}/2$-bigrading and that 

1. for $a,b \in A$ two elements of homogeous degree $(n_a, \sigma_a), (n_b, \sigma_b) \in \mathbb{Z} \times \mathbb{Z}/2$, respectively, then 

   $a b = (-1)^{n_a n_b} (-1)^{\sigma_a \sigma_b} \, b a$

1. $d (a b) = (d a) b + (-1)^{n_1} a (d b)$.

See also at _[[signs in supergeometry]]_.

In bidegree $(0,-)$ this is a _[[commutative superalgebra]]_.

## Examples

* The [[de Rham algebra]] of [[differential forms]] on a [[smooth manifold]] is a differential-graded commutative algebra. The algebra of [[super differential forms]] on a [[supermanifold]] is a differential-graded commutative superalgebra.

* The dg-algebra of [[polynomial differential forms]] on an [[n-simplex]];

The following are [[semifree differential graded-commutative algebras]]:

* A [[Sullivan algebra]].

* The [[Chevalley-Eilenberg algebra]] of a [[Lie algebra]] or more generally of an [[L-infinity algebra]] or [[L-infinity algebroid]] is a differential-graded-commutative algebra, that of a [[super L-infinity algebra]] is a differential graded-commutative superalgebra.

## Related concepts

* [[dgc-coalgebra]]

* [[model structure on differential graded-commutative algebras]]

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
