
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Enriched category theory
+-- {: .hide}
[[!include enriched category theory contents]]
=--
=--
=--

# Algebroids (linear categories)
* table of contents
{: toc}


## Idea

A *linear category*, or *algebroid*, is a [[category]] whose [[hom-sets]] are all [[vector spaces]] (or [[modules]]) and whose [[composition]] operation is [[bilinear map|bilinear]].  This concept is a [[horizontal categorification]] of the concept of (unital associative) *[[unital associative algebra|algebra]]*.


## Definitions

Fix a [[commutative ring]] $K$.  (Often we want $K$ to be a [[field]], such as the field $\mathbb{C}$ of [[complex numbers]], but we could also choose more generally a [[rig|commutative rig]] for $K$.)

A __$K$-linear category__, or __$K$-algebroid__, is a [[enriched category|category enriched]] over $K\,$[[Mod]], the [[monoidal category]] of $K$-[[modules]] with the usual [[tensor product of modules]].  (Note that one usually speaks of $K\,$[[Vect]] instead of $K\,Mod$ when $K$ is a [[field]].)

Just as a $\mathbb{Z}$-algebra is the same thing as a [[ring]], so a $\mathbb{Z}$-algebroid is the same thing as a *[[ringoid]]*.


## Remarks

*  An [[unital associative algebra|algebra]] is a [[pointed category|pointed]] algebroid with a single object, hence a one-object $K\,Mod$-enriched (or $K\,Vect$-enriched) category.  Compare with similar '[[oidification|oidfied]]' concepts such as [[groupoid]] and [[ringoid]].

*  Many linear categories are also assumed to be [[additive category|additive]].  A [[linear functor]] (that is, a $K\,Mod$-enriched or $K\,Vect$-[[enriched functor]]) between additive linear categories is automatically an [[additive functor]].

* A **symmetric monoidal $K$-linear category** is a category which is at the same time a $K$-linear category and a [[symmetric monoidal category]] and such that the composition and the tensor product on morphisms are bilinear.

*  Beware that a [[Lie algebroid]] is not a special case of an algebroid in the above sense, just as a [[Lie algebra]] is not a [[unital associative algebra]]. The point is that there is a restrictive and a general sense of "algebra". In the restrictive sense an algebra is an associative unital algebra, hence a [[monoid]] in $Vect$, hence a one-object $Vect$-enriched category. But in a more general sense an algebra is an algebra over an [[operad]]. It is this more general sense in terms of which Lie algebras are special cases of algebras and [[Lie algebroid]]s their [[horizontal categorification]].


## Generalizations

* Replacing plain vector spaces with [[chain complexes]] of vector spaces leads to an $\infty$-version of algebroids: a category enriched in chain complexes, which following the above reasoning could justly be called a _DG algebroid_  is usually called a _[[DG-category]]_.

* Replacing plain vector spaces with [[Banach space]]s leads to a $C^*$-version of algebroids: a category enriched in Banach spaces with some extra structure (mimicing the extra structure of a $C^*$-[[C-star-algebra|algebra]]), which following the above reasoning could justly be call a _$C^*$-algebroid_ is usually called a $C^*$-category. See [[spaceoid]]s.

* [[vertex operator algebroid]]

[[!redirects algebroid]]
[[!redirects algebroids]]
[[!redirects linear category]]
[[!redirects linear categories]]

## References

- Gabriel & Roiter, *Representations of Finite-Dimensional Algebras*, 1992.
