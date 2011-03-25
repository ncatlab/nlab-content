
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Superalgebra_ is the study of ([[higher algebra|higher]]) [[algebra]] over the [[base topos]] on [[superpoint]]s.


## Associative superalgebras

### Definition

Recall that an ordinary [[associative algebra]] (a [[vector space]] with a linear and associative and unital product operation) is a [[monoid]] in the [[category]] [[Vect]] of [[vector spaces]].

Accordingly, **super algebra** is a [[monoid]] in the [[category]] [[SVect]] of [[super vector space]]s.

### Examples

#### Grassmann algebra 
 
* For $V$ a [[vector space]] or [[graded vector space]] the [[Grassmann algebra]] $\wedge^\bullet V$ is a super algebra. This are the _free_ superalgebras.

#### Clifford algebra 

See [[Clifford algebra]].

## Universal superalgebra

Write $SuperPoint$ for the [[site]] of [[superpoint]]s. Write 

$$
  SuperSet := Sh(SuperPoint)
$$

for the [[sheaf topos]] (a [[presheaf topos]]) over this site.

By the general mechanism of [[internalization]] (see for instance [[group object]]) algebraic objects internal to $SuperSet$ may be identified (using the [[Yoneda lemma]]) with [[functor]]s on the [[opposite category]] of $SuperPoint$ with values in the [[category]] of ordinary such algebraic structures.

For instance an associative [[superalgebra]] $A$ may be characterized by its [[functor of points]]

$$
  A(-) : Spec \wedge^\bullet \mathbb{R}^k \mapsto Hom_{sAlg}(A,\wedge^\bullet \mathbb{R}^k)
  \,,
$$

where $\wedge^\bullet \mathbb{R}^k$ is the $\mathbb{Z}_2$-graded [[Grassmann algebra]] on $k$ generators and $Spec \wedge^\bullet \mathbb{R}^k$ its formally dual [[superpoint]], and where the set $Hom_{sAlg}(A,\wedge^\bullet \mathbb{R}^k)$ naturally has the structure of an object in $Alg^{op}$.

In much of the superalgebra literature, notably that having connections to [[physics]], this incarnation of the [[Yoneda lemma]] goes by the name _[[even rules]]_ . 

## References

Section 3 of

* [[Christoph Sachse]], _A Categorical Formulation of Superalgebra and Supergeometry_ ([arXiv:0802.4067](http://arxiv.org/abs/0802.4067))

[[!redirects superalgebra]]
[[!redirects super-algebra]]