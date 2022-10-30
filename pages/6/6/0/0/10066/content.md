
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


### Relation to representation theory
 {#RelationToRepresentationTheory}

The $G$-equivariant $K$-theory of the point is the [[representation ring]] of the group $G$:

$$
  K_G(\ast) \simeq Rep(G)
  \,.
$$

Accordingly the construction of an [[index]] ([[push-forward in generalized cohomology|push-forward]] to the point) in equivariant K-theory is a way of producing $G$-[[representations]] from [[equivariant vector bundles]]. This method is also called _[[Dirac induction]]_. 

Specifically, applied to equivariant [[complex line bundles]] on [[coadjoint orbits]] of $G$, this is a K-theoretic formulation of the [[orbit method]].


## Examples

The $G$-equivariant K-theory of the point for $G$ a [[compact Lie group]] is the [[representation ring]] of $G$.

## Related concepts

* [[Baum-Connes conjecture]], [[Green-Julg theorem]], [[Atiyah-Segal completion theorem]]

* [[equivariant elliptic cohomology]]

## References
 {#References}

The idea of equivariant K-theory goes back to 

[[Graeme Segal]] and [[Michael Atiyah]]

* {#Segal68} [[Graeme Segal]], _Equivariant K-theory_, Inst. Hautes Etudes Sci. Publ. Math.  No. 34 1968 129-151. 
 

and for [[algebraic K-theory]] to

* [[Robert Thomason]], _Algebraic K-theory of group scheme actions_, Algebraic topology and algebraic K-theory (Princeton, N.J., 1983), Ann. of Math. Stud., vol.
113, Princeton Univ. Press, Princeton, NJ, 1987, pp. 539&#8211;563

See also at _[algebraic K-theory -- References -- On quotient stacks](algebraic+K-theory#ReferencesAlgebraicKTheoryForQuotientStacks)_.

Introductions and surveys include

* N. C. Phillips, _Equivariant K-theory for proper actions_, Pitman 
Research Notes in Mathematics Series 178, Longman, Harlow, UK, 1989. 


* [[Bruce Blackadar]], section 11 of _[[K-Theory for Operator Algebras]]_

* Alexander Merkujev, _Equivariant K-theory_ ([pdf](http://www.math.uiuc.edu/K-theory/0981/book/2-0925-0954.pdf))

* Zachary Maddock, _An informal discourse on equivariant K-theory_ ([pdf](http://math.columbia.edu/~ellis/ass/equiv_k-thry.pdf))

Discussion relating to K-theory of homotopy quotients / Borel construction is in 

* [[Jacob Lurie]], around p. 11 of _[[A Survey of Elliptic Cohomology]]_ ([pdf](http://www.math.harvard.edu/~lurie/papers/survey.pdf))

Discussion of the [[adjoint action]]-equivariant K-theory of suitable [[Lie groups]] in in 

* [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], _[[Loop Groups and Twisted K-Theory]]_.

Discussion of K-theory of [[orbifolds]] is for instance in section 3 of 

* Alejandro Adem, Johanna Leida, Yongbin Ruan, _Orbifolds and string topology_, Cambridge Tracts in Mathematics 171, 2007 ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf))

