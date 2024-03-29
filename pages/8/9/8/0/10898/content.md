
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The notion of _category enriched in a bicategory_ is the many-object-generalization of the notion of an [[enriched category]] enriched in a [[monoidal category]] via regarding a [[monoidal category]] as a [[bicategory]] with a single object.

Originally B&#233;nabou called these *polyads*. 

## Definition

Let $B$ be a [[bicategory]], and write $\otimes$ for horizontal (1-cell) composition (written in Leibniz order). A [[category enriched in a bicategory|category enriched in the bicategory]] $B$ consists of a [[set]] $X$ together with 

* A function $p: X \to B_0$, 
* A function $\hom: X \times X \to B_1$, satisfying the typing constraint $\hom(x, y): p(x) \to p(y)$, 
* A function $\circ: X \times X \times X \to B_2$, satisfying the constraint $\circ_{x, y, z}: \hom(y, z) \otimes \hom(x, y) \to \hom(x, z)$, 
* A function $j: X \to B_2$, satisfying the constraint $j_x: 1_{p(x)} \to \hom(x, x)$, 

such that the associativity and unitality diagrams, as written above, commute. Viewing a monoidal category $M$ as a 1-object bicategory $\Sigma M$, the notion of enrichment in $M$ coincides with the notion of enrichment in the bicategory $\Sigma M$. 

Equivalently this is simply a [[lax functor]] from the [[codiscrete category]] on $X$ into $B$. In particular if $X$ is the singleton set then this is the same as a [[monad]].

If $X$, $Y$ are sets which come equipped with enrichments in $B$, then a $B$-functor consists of a function $f: X \to Y$ such that $p_Y \circ f = p_X$, together with a function $f_1: X \times X \to B_2$, satisfying the constraint $f_1(x, y): \hom_X(x, y) \to \hom_Y(f(x), f(y))$, and satisfying equations expressing coherence with the composition and unit data $\circ$, $j$ of $X$ and $Y$. (Diagram to be inserted, perhaps.)

## Related concepts

* [2-category equipped with proarrows -- Categories enriched in an equipment](2-category+equipped+with+proarrows#CategoriesEnrichedInAnEquipment)
* [[locally cocomplete bicategory]]

## References

Discussion of [[Kleisli objects]] (collages) for [[monads]] generalized to categories enriched in bicategories is in section 15.9 of

* [[Richard Garner]], [[Michael Shulman]], _Enriched categories as a free cocompletion_ ([arXiv:1301.3191](http://arxiv.org/abs/1301.3191))
 {#GarnerShulman13}

[[!redirects categories enriched in a bicategory]]
[[!redirects category enriched over a bicategory]]
[[!redirects categories enriched over a bicategory]]

[[!redirects category enriched in a 2-category]]
[[!redirects categories enriched in a 2-category]]
[[!redirects category enriched over a 2-category]]
[[!redirects categories enriched over a 2-category]]

[[!redirects bicategory-enriched category]]
[[!redirects bicategory-enriched categories]]

[[!redirects polyad]]
[[!redirects polyads]]



