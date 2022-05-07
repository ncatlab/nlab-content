
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A **large category** is a [[category]] which is not (necessarily) [[small category|small]].

There are some variations in usage depending on the [[foundations]] chosen.  Also, not all authors agree on whether a large category is *not* small, or merely not *necessarily* small (i.e., whether small categories are also large).


## Definitions

The precise meaning of the above definition depends on the [[foundations]] chosen.

* In [[ZF]], where a *small category* is one whose objects and morphisms form [[sets]], a *large category* is one whose objects and morphisms form (perhaps proper) [[classes]].

* In ZF with a specified [[Grothendieck universe]] $U$, where a *small category* is one whose objects and morphisms belong to $U$ (or have cardinalities belonging to $U$), a *large category* means a category whose objects and morphisms are still sets, but not (necessarily) belonging to $U$.  In this foundational system, one rarely considers categories whose objects and morphisms are proper classes.

* More generally, for any universe $U$, we may refer to categories whose objects and morphisms are elements of $U$ as **$U$-small**, and other categories as **$U$-large**.  In a context of multiple universes, it is perhaps more common to speak of "$V$-small categories" for some universe $V$ containing $U$, than "$U$-large categories."  If there are two fixed universes $U$ and $V$ with $U \in V$, then categories that are not even in $V$ may be called **very large**.

In all cases, it is somewhat ambiguous whether "large category" means "properly large," i.e., large and not small, or whether small categories should be considered as a subclass of large categories.  Usage may vary depending on need.


### Largeness and moderateness

A **[[moderate category]]** may be defined as one whose collections of objects and morphisms are no bigger than the size of the universe of small sets.  This is related to largeness in different ways depending on the foundations.

* In ZF, where all classes are subclasses of the class of all (small) sets, then *all* categories (small or large) are moderate.

* On the other hand, when smallness and largeness are defined with respect to a Grothendieck universe $U$, then a moderate category would be one whose objects and morphisms are (bijective to) subsets of $U$.  Thus, in this case, there are vastly more large categories than there are moderate ones.

* An in-between case, with some resulting ambiguity, is that of a class-set theory such as [[NBG]] or [[MK]], where *small category* means one whose objects and morphisms form sets.  Since such theories are closely related to ZF (indeed, NBG is conservative over ZF), it is natural to want to use "large category" to coincide with its ZF meaning: a category whose objects and morphisms form classes.

  However, in this case one can also consider categories which are "very large": their objects and morphisms are "superclasses" or "conglomerates" (collections of classes defined by first-order formulas, just as we do for classes in ZF).  Thus, in this case it may be more appropriate to say "moderate" for a category whose objects and morphisms are classes, and "large" for one which is not (necessarily) even moderate.

  This latter terminology also accords better with the usage for universes, since any Grothendieck universe $U$ gives rise to a model of NBG (and even MK) whose sets are the sets in $U$ and whose classes are the subsets of $U$.  One might even go backwards from this and start using "moderate" in the context of ZF for categories whose objects and morphisms are (not necessarily proper) classes.

  On the other hand, one could import terminology the other way, and use "large category" even in the context of a universe $U$ to mean one whose objects and morphisms are *subsets* of $U$ (i.e. what we have called above a "($U$-)moderate category").  This usage is that of [[Categories Work]]; it has the disadvantage that some categories are "too large to be large," although they are still "very large."  However, it does accord better with the ZF-usage, which is the original context in which "large category" was used.


## Properties

Many tools and results about small categories, in particular concerning [[limit]]s indexed by such a category and [[functor categories]], fail for large categories.  For instance:

* Many large categories have all *small* limits and/or colimits, but a large category with *large* limits or colimits must (at least in [[classical mathematics]]) be a [[preorder]].  Most large categories do have *some* large limits and colimits, however, although they are not always very useful; see for instance [[total category]].

* In a foundation of ZF, NBG, or MK, one cannot form the functor category $[C,D]$ unless $C$ is small.  In a foundation with universes, one can form $[C,D]$, but it will sometimes be oddly behaved.  In particular, it is not generally moderate, even if $C$ and $D$ are.


There are various notions and techniques to deal with this problem and reduce or relate large categories to small categories as much as possible:

* In the simplest case the large category is *essentially* small in that it is [[equivalence of categories|equivalent]] to a [[small category]].  Then (for all purposes adhering to the [[principle of equivalence]]) you can simply replace it with a small category.

* Many large categories that arise in practice are (even essentially) large but still *accessible*.  An [[accessible category]] is a large category which behaves like the category of [[ind-object]]s of a small category and is therefore, while itself large, entirely governed by a small category.

* Some problems can be avoided by simply assuming a [[Grothendieck universe]], so that large categories become small ones relative to a larger universe.


## Related concepts

* [[small category]], [[locally small category]], [[moderate category]]

* **large category**

* [[universe enlargement]]

* [[very large (∞,1)-sheaf (∞,1)-topos]]

## References

* [[Mike Shulman]], _Set theory for category theory) ([arXiv:0810.1279](http://www.arxiv.org/abs/0810.1279))

* [[Paul Blain Levy]], _Formulating Categorical Concepts using Classes_ ([arXiv:1801.08528](https://arxiv.org/abs/1801.08528))

[[!redirects large category]]
[[!redirects large categories]]
[[!redirects very large category]]
[[!redirects very large categories]]

[[!redirects moderate category]]
[[!redirects moderate categories]]
