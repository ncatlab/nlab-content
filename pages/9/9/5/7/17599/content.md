
# Augmented virtual double categories

* table of contents
{: toc}

## Idea

An **augmented virtual double category** is a [[virtual double category]] enhanced with additional 2-cells whose vertical target has length 0 (i.e. is a single object rather than a horizontal arrow).

In particular, there is always a "vertical 2-category" consisting of the objects, vertical arrows, and 2-cells whose vertical source and target are both length 0.  A virtual double category, by contrast, does not have a vertical 2-category unless it has all units.

## Examples

[[large category|Large]] (not necessarily [[locally small category|locally small]]) [[categories]], [[functors]], small-set-valued [[profunctors]], and transformations form an augmented virtual double category.  Note that only locally small categories have units therein, so the underlying virtual double category does not have enough data to reconstruct the 2-category of large categories, functors, and natural transformations; but the augmented virtual double category does.

## Applications

Augmented Virtual double categories are a natural context in which to compare [[proarrow equipments]] and [[Yoneda structures]], which are two different approaches to [[formal category theory]].  In both cases there is a notion of "profunctor" which are generally considered to be small-set-valued, but Yoneda structures require non-locally-small categories (the presheaf categories of non-small categories).  In this context the Yoneda embedding can be given a universal property relative to the horizontal arrows.  See [(Koudenburg)](#Koudenburg19).

## Related pages

* [[virtual double category]]
* [[virtual equipment]]
* [[Yoneda structure]]

## Reference

* {#Koudenburg15} Seerp Roald Koudenburg, *A double-dimensional approach to formal category theory*, [arXiv](http://arxiv.org/abs/1511.04070), 2015.  In this paper augmented virtual categories are called "hypervirtual double categories".

* {#Koudenburg19} Seerp Roald Koudenburg, *Augmented virtual double categories*, [arXiv](https://arxiv.org/abs/1910.11189), 2019.  This is a streamlined and expanded version of Sections 1, 2 and 3 of the previous paper, published in [TAC](http://www.tac.mta.ca/tac/volumes/35/10/35-10abs.html)

[[!redirects hypervirtual double category]]
[[!redirects hypervirtual double categories]]
[[!redirects augmented virtual double categories]]

