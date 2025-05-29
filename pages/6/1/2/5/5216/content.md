[[!redirects Lack&#39;s coherence theorem]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

One form of the [[bicategory#Coherence|coherence theorem for bicategories]] states that every [[bicategory]] is [[equivalence of bicategories|equivalent]] to a [[strict 2-category]].  **Lack's coherence observation** (named for [[Steve Lack]]) states that naturally occurring bicategories tend to be [[equivalence of bicategories|equivalent]] to naturally occurring strict 2-categories.  

## Examples

Instances of Lack's coherence observation include:

* The bicategory [[Prof]] of [[small categories]] and [[profunctors]] is equivalent to the strict 2-category of [[presheaf categories]] and [[cocontinuous functors]].

* The bicategory [[Span]](C) of [[spans]] in a category $C$ with [[pullbacks]] is equivalent to the strict 2-category of [[slice categories]] of $C$ and [[linear polynomial functors]]. More generally, the bicategory of [[polynomial functor|polynomials]] in a [[locally cartesian closed category]] is equivalent to the strict 2-category of slices and [[polynomial functors]].

Both examples are instances of a more general result. Given a [[relative pseudomonad]] $T$ on a strict 2-category $K$, the [[Eilenberg--Moore bicategory]] of $T$ will also be a strict 2-category, whereas the [[Kleisli bicategory]] will usually not be. However, the Kleisli bicategory embeds fully faithfully into the Eilenberg--Moore bicategory, and so will be [[biequivalent]] to the full sub-2-category of the Eilenberg--Moore bicategory on the free algebras.

It is not clear whether there are other examples that are not special cases of the observation above.

## References

This observation first appears in Example 1.5(k) of

*  [[Steve Lack]], _A 2-categories companion_, in: John C. Baez and J. Peter May (Eds) Towards Higher Categories, The IMA Volumes in Mathematics and its Applications, vol 152, Springer, 2009, doi:[10.1007/978-1-4419-1524-5_4](https://doi.org/10.1007/978-1-4419-1524-5_4), [arXiv:math/0702535](https://arxiv.org/abs/math/0702535).

The observation that instances generally arise from [[Kleisli bicategories]] is in:

* [[Nathanael Arkor]], [[Philip Saville]], Andrew Slattery, *Bicategories of algebras for relative pseudomonads*, [arXiv:2501.12510](https://arxiv.org/abs/2501.12510)

[[!redirects Lack's coherence theorem]]
