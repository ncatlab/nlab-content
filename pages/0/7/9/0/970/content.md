
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **large category** is a [[category]] which belongs to the "next largest" size category than a [[small category]] does.  This is made precise in different ways depending on the [[foundations]] chosen.

* In [[ZF]], where a *small category* is one whose objects and morphisms form [[sets]], a *large category* is one whose whose objects and morphisms form [[classes]].

* In ZF with a single specified [[Grothendieck universe]] $U$, where a *small category* is one whose objects and morphisms belong to $U$ (or have cardinalities belonging to $U$), a *large category* usually means a category whose objects and morphisms are still sets, but not (necessarily) belonging to $U$.

  * Sometimes, however, such as in [[Categories Work]] (second half of p. 23), a *large category* means one whose objects and morphisms are *subsets* of $U$.  People who use the previous meaning of "large category" in the context of one universe sometimes call a category of this sort *[[moderate category|moderate]]*.

* In ZF with two specified universes $U\in V$, where a *small category* is one whose objects and morphisms belong to $U$, a *large category* may mean one whose objects and morphisms belong to $V$, with a term such as *very large category* used for one whose objects and morphisms are sets not necessarily belonging even to $V$.

* With more than two universes, one usually prefixes "small" with the universe to which it refers: a *$U$-small category* is one whose objects and morphisms belong to $U$.  In this context it is more common to say "$V$-small category" for some universe $V$ containing $U$, than to say "$U$-large category."

* In a class-set theory such as [[NBG]] or [[MK]], it is natural to use *small category* for one whose objects and morphisms form sets, *large category* for one whose whose objects and morphisms are classes (of sets), and *very large category* for one whose objects and morphisms are "superclasses" or "conglomerates".  The latter are *collections of classes* that have no formal existence in the theory, but can be identified with the first-order formulas which define them; their ontological status in a class-set theory is identical to that of proper classes in ZF.

  Note that if $U$ is a Grothendieck universe, then there is a model of MK (hence also NBG) whose sets are the $U$-small sets and whose classes are the subsets of $U$.  However, the "large categories" in this model of MK are only the $U$-*moderate* categories in the universe picture, while its "very large categories" are still only $U$-large (unless one uses the CWM definition of "large category" in the context of a universe).

In all cases, it is somewhat ambiguous whether "large category" means "properly large," i.e. large and not small, or whether small categories should be considered as a subclass of large categories.  Usage may vary depending on need.


## Properties

Many tools and results about small categories, in particular concerning [[limit]]s indexed by such a category and [[functor categories]], fail for large categories.  For instance:

* Many large categories have all *small* limits and/or colimits, but a large category with *large* limits or colimits must (at least in [[classical mathematics]]) be a [[preorder]].  Most large categories do have *some* large limits and colimits, however, although they are not always very useful; see for instance [[total category]].

* In a foundation of ZF, NBG, or MK, one cannot form the functor category $[C,D]$ unless $C$ is small.  In a foundation with universes, one can form $[C,D]$, but it will sometimes be oddly behaved.  In particular, it is not generally moderate, even if $C$ and $D$ are.


There are various notions and techniques to deal with this problem and reduce or relate large categories to small categories as much as possible:

* In the simplest case the large category is *essentially* small in that it is [[equivalence of categories|equivalent]] to a [[small category]].  Then (for all non-[[evil]] purposes) you can simply replace it with a small category.

* Many large categories that arise in practice are (even essentially) large but still *accessible*.  An [[accessible category]] is a large category which behaves like the category of [[ind-object]]s of a small category and is therefore, while itself large, entirely governed by a small category.

* Some problems can be avoided by simply assuming a [[Grothendieck universe]], so that large categories become small ones relative to a larger universe.


## Related concepts

* [[small category]], [[locally small category]], [[moderate category]]

* **large category**

* [[universe enlargement]]

[[!redirects large categories]]
