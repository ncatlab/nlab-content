
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition ##

If $C$ and $D$ are [[enriched categories]] over a [[cosmos]] $V$, that is, a complete and cocomplete symmetric [[closed monoidal category]], then a [[profunctor]] $F$, from $C$ to $D$, that is, a $V$-functor $D^{op} \otimes C\to V$, induces two adjoint $V$-functors: $F_{\ast}: (V^C)^{op} \to V^{D^{op}}$ and $F^{\ast}: V^{D^{op}} \to (V^C)^{op}$.

$$
(V^C)^{op}(F^{\ast} p, q) \cong V^{D^{op}}(p, F_{\ast} q).
$$

In the case of the $Hom$ profunctor, $Hom: A^{op} \otimes A \to V$, of a $V$-enriched category $A$, this adjunction is known as [[Isbell duality]] or Isbell conjugation.

The **nucleus** of $F$ is the [[center of an adjunction|center]] of this adjunction. In the case where $F = Hom$, the nucleus is called the Isbell or reflexive completion.

##Examples with $F = Hom$##

* $V = Ab$, the category of abelian groups. Let $k$ be a field, viewed as a one-object $Ab$-category. Both $[k^{op},Ab]$ and $[k,Ab]$ are the category of $k$-vector spaces, and both adjoints are the dual vector space construction. The nucleus of the profunctor, or reflexive completion $R(k)$ of $k$, is the category of $k$-vector spaces $V$ for which the canonical map $V \to V^{\ast \ast}$ is an isomorphism &#8212; in other words, the [[finite-dimensional vector spaces]].


##Examples with other profunctors##
* $V$ = truth values. Given two sets, $A$ and $B$, and a relation (truth-valued profunctor) between them, the adjunction is known as a [[Galois connection]], which restricts to the nucleus, a [[Galois correspondence]].
* $V = \overline{\mathbb{R}} = ([-\infty, \infty], \geq, +)$. Let a real vector space, $W$, be considered as a discrete $\overline{\mathbb{R}}$-category, and consider the $\overline{\mathbb{R}}$-profunctor corresponding to evaluation between an element of $W$ and an element of its dual. Then the nucleus is composed of $\overline{\mathbb{R}}$-valued functions on $W$, and the duality expresses the [[Legendre-Fenchel transform]]. (See Simon Willerton's [post](http://golem.ph.utexas.edu/category/2014/05/enrichment_and_the_legendrefen_1.html).)

##References

* [[Simon Willerton]], Tight spans, Isbell completions and semi-tropical modules, ([tac](http://www.tac.mta.ca/tac/volumes/28/22/28-22abs.html))
* [[Simon Willerton]], _The Nucleus of a Profunctor: Some Categorified Linear Algebra_, [blog post](http://golem.ph.utexas.edu/category/2013/08/the_nucleus_of_a_profunctor_so.html)
* [[Simon Willerton]], _Galois Correspondences and Enriched Adjunctions_, [blog post](http://golem.ph.utexas.edu/category/2014/02/galois_correspondences_and_enr.html)