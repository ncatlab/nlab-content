# Hypervirtual double categories

* table of contents
{: toc}

## Idea

A **hypervirtual double category** is a [[virtual double category]] enhanced with additional 2-cells whose vertical target has length 0 (i.e. is a single object rather than a horizontal arrow).

In particular, there is always a "vertical 2-category" consisting of the objects, vertical arrows, and 2-cells whose vertical source and target are both length 0.  A virtual double category, by contrast, does not have a vertical 2-category unless it has all units.

## Examples

[[large category|Large]] (not necessarily [[locally small category|locally small]]) [[categories]], [[functors]], small-set-valued [[profunctors]], and transformations form a hypervirtual double category.  Note that only locally small categories have units therein, so the underlying virtual double category does not have enough data to reconstruct the 2-category of large categories, functors, and natural transformations; but the hypervirtual double category does.

## Applications

Hypervirtual double categories are a natural context in which to compare [[proarrow equipments]] and [[Yoneda structures]], which are two different approaches to "formal category theory".  In both cases there is a notion of "profunctor" which are generally considered to be small-set-valued, but Yoneda structures require non-locally-small categories (the presheaf categories of non-small categories).  In this context the Yoneda embedding can be given a universal property relative to the horizontal arrows.  See [(Koudenburg)](#Koudenburg).

## Related pages

* [[virtual double category]]
* [[virtual equipment]]
* [[Yoneda structure]]

## Reference

* Seerp Roald Koudenburg, *A double-dimensional approach to formal category theory*, [arXiv](http://arxiv.org/abs/1511.04070)
 {#Koudenburg}

[[!redirects hypervirtual double category]]

