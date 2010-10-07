+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


* [[category]]

* **2-category**

* [[3-category]]

* [[n-category]]

* [[(n,r)-category]]

***


# Contents
* automatic table of contents goes here
{:toc}

## Idea

A $2$-category is any of several concepts that generalize [[category|categories]] one step in [[higher category theory]]. 

It consists of 

* [[objects]];

* [[morphisms]] between objects;

* [[2-morphisms]] between morphisms.

The morphisms can be composed along the objects, while the 2-morphisms can be composed in two different directions: along objects and along morphisms.  This is a "globular" description, which is the most commonly used, but there are (equivalent) variants which use different shapes of 2-morphism as basic.

The concept generalizes to $n$-[[n-category|categories]] which have $k$-morphisms for all $k\le n$.


## Definitions

The easiest definition of 2-category is that it is a category [[enriched category|enriched]] over the [[cartesian monoidal category]] [[Cat]].  Thus it has a collection of objects, and for each pair of objects a category $hom(x,y)$.  The objects of these hom-categories are the morphisms, and the morphisms of these hom-categories are the 2-morphisms.  This produces the classical notion of [[strict 2-category]].

For some purposes, this type of 2-category is too strict: one would like to allow composition of morphisms to be associative and unital only up to coherent invertible 2-morphisms.  A direct generalization of the above "enriched" definition produces the classical notion of [[bicategory]].

One can also obtain notions of 2-category by specialization from the case of higher categories.  Specifically, if we fix a meaning of $\infty$-[[infinity-category|category]], however weak or strict we wish, then we can define a __$2$-category__ to be an $\infty$-category such that every 3-morphism is an [[equivalence]], and all parallel pairs of $j$-morphisms are equivalent for $j \geq 3$.  It follows that, up to equivalence, there is no point in mentioning anything beyond $2$-morphisms, except whether two given parallel $2$-morphisms are equivalent.  In some models of $\infty$-categories, it is possible to make this precise by demanding that all parallel pairs of $j$-morphisms are actually *equal* for $j\geq 3$, producing a simpler notion of 2-category in which we can speak about [[equality]] of 2-morphisms instead of equivalence.  (This is the case for both strict $2$-categories and bicategories.)

All of the above definitions produce "equivalent" theories of 2-category, although in some cases (such as the fact that every bicategory is equivalent to a strict 2-category) this requires some work to prove.  On the nLab, we often use the word "2-category" in the general sense of referring to whatever model one may prefer, but usually one in which composition is weak; a [[bicategory]] is an adequate definition.  One should beware, however, that in the literature it is common for "2-category" to refer only to *strict* 2-categories.


## Types of morphisms

* [[subcategory]]
* [[faithful morphism]]
* [[fully faithful morphism]]
* [[conservative morphism]]
* [[pseudomonic morphism]]
* [[discrete morphism]]


## Specific versions

* globular [[strict 2-category]]
* [[bicategory]]

## Double nerve

An ordinary  [[category]] has a [[nerve]] which is a [[simplicial set]]. For 2-categories one may consider their [[double nerve]] which is a [[bisimplicial set]].


## References

See also the references as [[bicategory]].

* [[Ross Street]], _Encyclopedia article on 2-categories and bicategories_ ([pdf](http://www.maths.mq.edu.au/~street/Encyclopedia.pdf))


[[!redirects 2-category]]
[[!redirects 2-categories]]
