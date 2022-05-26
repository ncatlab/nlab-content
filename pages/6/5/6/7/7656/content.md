
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--

# Locally internal categories

* table of contents
{: toc}


## Idea

A _locally internal category_ is an analogue of a [[large category|large]] but [[locally small category]] relative to an [[elementary topos]], when that topos is thought of as generalizing the category of sets.

More generally, locally internal catgegories can be defined over any category with finite limits.  The notion is best-behaved when $E$ is [[locally cartesian closed category|locally cartesian closed]] (for instance, in that case the [[codomain fibration]] of $E$ is an example).

## Definition
 {#Definition}

Given a [[category]] $E$ with [[finite limits]] and an [[object]] $X$ in $E$, one notices that the [[slice category]] $E/X$ is a [[symmetric monoidal category]] under [[fiber product]] in $E$.  Hence we can consider [[enriched category|categories enriched]] over $E/X$, i.e. $E/X$-categories. 

A __locally internal category__ $C$ over $E$ is given by 

* An $(E/X)$-[[enriched category]] $C_X$ for each object $X$ in $E$.  This is thought of as the category of $X$-[[indexed families]] of objects of $E$.

* For each morphism $f \colon X\to Y$ in $E$, an $(E/X)$-[[full subcategory|full embedding]] $\theta_f \colon f^* C_Y\to C_X$.  Here $f^* C_Y$ means the $(E/X)$-enriched category obtained by applying the symmetric monoidal functor $f^* \colon E/Y \to E/X$ to the [[hom-objects]] of the $(E/Y)$-enriched category $C_Y$, and an [[enriched functor]] is a "full embedding" if it induces [[isomorphisms]] on [[hom-objects]].

* $f \mapsto \theta_f$ is functorial up to [[coherence|coherent]] isomorphism.  This means certain [[commuting diagram|diagrams commute]] analogous to those of a [[pseudofunctor]], but with the functors $f^*$ applied at appropriate places to make them [[type checking|typecheck]].

## Properties

In the [[stack semantics]] of $E$, a locally internal category "looks like" an ordinary locally small category.

Locally internal categories can also be identified with [[Grothendieck fibrations]] or [[indexed categories]] over $E$ which satisfy a certain "representability" or "comprehensibility" condition:

A Grothendieck fibration $p: C \to E$ is called __locally small__ if, for every pair $A,B \in C$, there exists an object of $E_{pA \times pB}$,  $(x,y) : I \to pA \times pB$, and a morphism $f: x^*A \to y^*B \in C_I$, which is __terminal__, in the sense that given another such datum $(J,z,w,g)$, there is a unique map $u: J \to I$ so that $xu = z, yu = w$, and the coherence isomorphisms identify $u^*f$ with $g$. (This is [Elephant](#Elephant) B.1.3.12).

An indexed category $E \to \operatorname{CAT}$ is called locally small if the associated fibration is locally small.

If we also take care of the appropriate morphisms have the following:

+-- {: .un_remark}
###### Remark
(1)  The obvious forgetful functor from locally internal categories to $E$-indexed categories (equivalently, Grothendieck fibrations over $E$) is a [[full sub-2-category | fully faithful 2-functor]]. In particular, every [[indexed functor]] between locally internal categories is an [[enriched functor]]. [Elephant](#Elephant), Proposition B2.2.2.

(2a) Let $S$ be a [[locally cartesian closed category]], let $F:S\to S$ be an $S$-enriched functor whose underlying (ordinary) functor preserves pullbacks. Then $F$ extends to an $S$-[[indexed functor]].
		
 (2b) ([[Robert Pare]]) If this indexed functor preserves pullbacks (as an indexed functor) and if it induces the given enrichment, this extension is unique (up to a canonical isomorphism). [Elephant](#Elephant)  B2.2.8.
=--

## Related pages

* [[internal category]]
* [[indexed category]]
* [[enriched category]]
* [[enriched indexed category]]

## References

* J. Penon, _Categories localement internes_, C. R. Acad. Sci. Paris __278__ (1974) A1577-1580

* Locally internal categories, Appendix in: P. Johnstone, Topos theory, 1977

* Chapter B2.2 of [[Sketches of an Elephant]]{#Elephant}

[[!redirects locally internal categories]]