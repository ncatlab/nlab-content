
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Equivariant K-theory_ is the [[equivariant cohomology]] version of the [[generalized cohomology theory]] [[K-theory]]. 

To the extent that [[K-theory]] is given by [[equivalence classes]] of [[virtual vector bundles]] ([[topological K-theory]], [[operator K-theory]]), equivariant K-theory is given by equivalence classes of virtual [[equivariant bundles]] or generalizations to [[noncommutative topology]] thereof, as in _[[equivariant operator K-theory]]_, _[[equivariant KK-theory]]_.



## Properties

### Relation to operator K-theory of crossed product algebras

The _[[Green-Julg theorem]]_ identifies, under some conditions, equivariant K-theory with [[operator K-theory]] of corresponding [[crossed product algebras]].




### Relation to representation theory
 {#RelationToRepresentationTheory}

The [[representation ring]] of $G$ over the [[complex numbers]] is the $G$-[[equivariant K-theory]] of the point, or equivalently by the [[Green-Julg theorem]], if $G$ is a [[compact Lie group]], the [[operator K-theory]] of the [[group algebra]] (the [[groupoid convolution algebra]] of the [[delooping]] groupoid of $G$):

$$
  R_{\mathbb{C}}(G) \simeq KU^0_G(\ast) \simeq KK(\mathbb{C}, C(\mathbf{B}G))
  \,.
$$

The first [[isomorphism]] here follows immediately from the elementary definition of equivariant [[topological K-theory]], since a $G$-[[equivariant vector bundle]] over the point is manifestly just a [[linear representation]] of $G$ on a [[complex vector space]].

(e.g. [Wilson 16, example 1.6 p. 3](#Wilson16))

Therefore a similar isomorphism identifies the $G$-representation ring over the [[real numbers]] with the equivariant orthogonal $K$-theory of the point in degree 0:

$$
  R_{\mathbb{R}}(G)
  \;\simeq\;
  KO_G^0(\ast)
  \,.
$$

But beware that equivariant [[KO]], even of the point, is much richer in higher degree ([Wilson 16, remark 3.34](#Wilson16))

Accordingly the construction of an [[index]] ([[push-forward in generalized cohomology|push-forward]] to the point) in equivariant K-theory is a way of producing $G$-[[representations]] from [[equivariant vector bundles]]. This method is also called _[[Dirac induction]]_. 

Specifically, applied to equivariant [[complex line bundles]] on [[coadjoint orbits]] of $G$, this is a K-theoretic formulation of the [[orbit method]].


### Relation to K-theory of homotopy quotient spaces (Borel constructions)

For $X$ a [[topological space]] equipped with a $G$-[[action]] for $G$ a [[topological group]], write $X//G$ for the [[homotopy type]] of the corresponding [[homotopy quotient]]. A standard model for this is the [[Borel construction]]

$$
  X//G \simeq (X \times EG)/G
  \,.
$$

The ordinary [[topological K-theory]] of $X//G$ is also called the _Borel-equivariant K-theory_ of $X$, denoted

$$
  K_G^{Bor}(X) \coloneqq K(X//G)
  \,.
$$

There is a canonical map

$$
  K_G(X) \to K_G^{Bor}(X)
$$

from the genuine equivariant K-theory to the Borel equivariant K-theory. In terms of the [[Borel construction]] this is given by the composite

$$
  K_G(X) \to K_G(X \times E G) \simeq K((X \times E G) / G ) \simeq K_G^{Bor}(X)
  \,,
$$

where the first map is pullback along the [[projection]] $X \times E G \to X$ and the first equivalence holds because the $G$-action on $X \times E G$ is free.

This map from genuine to Borel equivariant K-theory is not in general an isomorphism.

Specifically for $X$ the point, then $K_G(\ast) \simeq R(G)$ is the [[representation ring]] and $K_G^{Bor}(\ast) \simeq K(B G)$ is the [[topological K-theory]] of the [[classifying space]] $B G$ of $G$-[[principal bundles]]. In this case the above canonical map is of the form

$$
  R(G) \to K(B G)
  \,.
$$

This is never an [[isomorphism]], unless $G$ is the trivial group. But the [[Atiyah-Segal completion theorem]] says that the map identifies $K(B G)$ as the completion of $R(G)$ at the [[ideal]] of [[virtual representations]] of rank 0.

[[!include Segal completion -- table]]

### Equivariant Chern-character

There is a [[Chern character]] map from equivariant K-theory to [[equivariant ordinary cohomology]].

(e.g. [Stefanich](#Stefanich))



## Related concepts

* [[Baum-Connes conjecture]], [[Green-Julg theorem]], 

* [[Atiyah-Segal completion theorem]]

* [[equivariant elliptic cohomology]]

* [[equivariant algebraic K-theory]]

* [[McKay correspondence]]


## References
 {#References}

The idea of equivariant [[topological K-theory]] goes back to 

* {#Segal68} [[Graeme Segal]], _Equivariant K-theory_, Inst. Hautes Etudes Sci. Publ. Math.  No. 34 (1968) p. 129-151 

* {#SegalAtiyah69} [[Graeme Segal]], [[Michael Atiyah]], _Equivariant K-theory and completion_, J. Differential Geometry 3 (1969), 1&#8211;18. MR 0259946 (41 #4575
 
and for [[algebraic K-theory]] to

* [[Robert Thomason]], _Algebraic K-theory of group scheme actions_, Algebraic topology and algebraic K-theory (Princeton, N.J., 1983), Ann. of Math. Stud., vol.
113, Princeton Univ. Press, Princeton, NJ, 1987, pp. 539&#8211;563

See also at _[algebraic K-theory -- References -- On quotient stacks](algebraic+K-theory#ReferencesAlgebraicKTheoryForQuotientStacks)_.

Introductions and surveys include

* [[John Greenlees]], _Equivariant version of real and complex connective K-theory_, Homology Homotopy Appl. Volume 7, Number 3 (2005), 63-82. ([Euclid:1139839291](http://projecteuclid.org/euclid.hha/1139839291))

* N. C. Phillips, _Equivariant K-theory for proper actions_, Pitman 
Research Notes in Mathematics Series 178, Longman, Harlow, UK, 1989. 

* [[Bruce Blackadar]], section 11 of _[[K-Theory for Operator Algebras]]_

* Alexander Merkujev, _Equivariant K-theory_ ([pdf](http://www.math.uiuc.edu/K-theory/0981/book/2-0925-0954.pdf))

* Zachary Maddock, _An informal discourse on equivariant K-theory_ ([pdf](http://math.columbia.edu/~ellis/ass/equiv_k-thry.pdf))

* [[Akhil Mathew]], _[Equivariant K-theory](https://amathew.wordpress.com/2011/12/03/equivariant-k-theory/)_

* {#Wilson16} [[Dylan Wilson]], _Equivariant K-theory_, 2016 ([pdf](https://www.math.uchicago.edu/~dwilson/notes/equivariant-k-theory-talk.pdf), [[WilsonKTheory16.pdf:file]])


The equivariant [[Chern character]] is discussed in 

* {#Stefanich} German Stefanich, _Chern Character in Twisted and Equivariant K-Theory_ ([pdf](https://math.berkeley.edu/~germans/Chern2.pdf))

Discussion relating to K-theory of [[homotopy quotients]]/[[Borel constructions]] is in 

* [[Jacob Lurie]], around p. 11 of _[[A Survey of Elliptic Cohomology]]_ ([pdf](http://www.math.harvard.edu/~lurie/papers/survey.pdf))

Discussion of the [[adjoint action]]-equivariant K-theory of suitable [[Lie groups]] in in 

* [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], _[[Loop Groups and Twisted K-Theory]]_.

Discussion of K-theory of [[orbifolds]] is for instance in section 3 of 

* Alejandro Adem, Johanna Leida, Yongbin Ruan, _Orbifolds and string topology_, Cambridge Tracts in Mathematics 171, 2007 ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf))

Discussion of combined [[twisted K-theory|twisted]] and [[equivariant K-theory|equivariant]] and [[real K-theory|real]] K-theory

* {#Gomi17} [[Kiyonori Gomi]], _Freed-Moore K-theory_ ([arXiv:1705.09134](https://arxiv.org/abs/1705.09134))

