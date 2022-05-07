
# Indexed families
* table of contents
{: toc}

## Idea

The term 'family' is often used as a synonym for '[[collection]]' (especially in the sense of [[subset]]).  However, we can use it more precisely, for the concept of an _indexed_ family.


## Definitions

A __family__, or __indexed family__ (or sometimes __indexed set__, etc), consists of an __index set__ $I$ (whose [[elements]] are the __indices__ of the family) and, for each index $k$, some __element__ $x_k$.  One can also speak of an __$I$-indexed family__.  An __[[ordered pair]]__ is a family indexed by $2 = \{0,1\}$; an __[[infinite sequence]]__ is an $\mathbb{N}$-indexed family.


## Notation

As a whole, this family may be denoted $(x_k \;|\; k\colon I)$, $(x_k)_{k\colon I}$, $(x_k)_k$, or simply $x$.  Sometimes one sees braces used instead of parentheses, giving the same notation for a family as for a [[collection]], although this is falling out of fashion; the parentheses ultimately come from notation for [[ordered pairs]].  One can also use notation for [[functions]], such as $\lambda\, k\colon I.\; x_k$ or $(k \mapsto x_k)$.  Finally, instead of $k\colon I$, one can see the [[type]] of $k$ indicated using any other method, especially $k \in I$ (which ultimately derives from [[material set theory]]).


## Families vs collections

Formally, a family of things should be distinguished from a [[collection]] of things; properly, it is the *[[range]]* of a family of things that is a collection, such as a [[subset]] of an appropriate ambient set of things.  On the other hand, often the difference between a family and a collection is unimportant, and the two may be used interchangeably.  (For example, one can take the [[union]] of either a family of subsets or a collection of subsets, with equivalent results; but one can take the sum of only a family of [[cardinal numbers]].)


## Formalization

We have been vague so far about what a family is a family *of* (what the elements are).  The easiest case is when the elements are from a [[set]] $S$; then an $I$-indexed __family of elements__ of $S$, also called an __indexed [[subset]]__ of $S$, is simply a [[function]] to $S$ from $I$.  If the elements are from a category $C$, then an $I$-indexed __family of objects__ of $C$ is a [[functor]] (or [[anafunctor]]) to $C$ from the [[discrete category]] on $I$, and an $I$-indexed __family of morphisms__ of $C$, also called an __indexed [[subcategory]]__, is similarly a functor to the [[arrow category]] of $C$.  In general, the elements ought to be from (at the very least) some sort of $\infty$-[[infinity-groupoid|groupoid]] $G$, in which case the family is a functor to $G$ from the discrete $\infty$-groupoid on $I$.

A formal [[structural set theory]] with a formal definition/notion of family is known as a [[first-order set theory]], while a set theory without a formal definition or notion of family is a [[zeroth-order set theory]]; this parallels the distinction between predicate and propositional logic. 

In [[foundations]] without [[proper classes]] or higher categories, it may be tricky to specify exactly what a [[family of sets]] is, if one cannot literally speak of a functor from a discrete category to the [[large category]] [[Set]]; see the article. On the other hand, there is no difficulty in speaking of a [[family of subsets]] of a given set; even in [[predicative mathematics]] (where one cannot speak of the [[power set]]), a __family of subsets__ of $S$ is simply a [[binary relation]] between $S$ and some index set $I$, writing $a \in x_k$ to denote that the $S$-element $a$ is related to the index $k$.

## Related concepts

* [[dependent type]]

* [[empty family]]

[[!redirects family]]
[[!redirects families]]
[[!redirects indexed family]]
[[!redirects indexed families]]
[[!redirects indexed set]]
[[!redirects indexed sets]]

[[!redirects index set]]
[[!redirects index sets]]
[[!redirects index preset]]
[[!redirects index presets]]

[[!redirects family of elements]]
[[!redirects families of elements]]
[[!redirects indexed subset]]
[[!redirects indexed subsets]]

[[!redirects family of objects]]
[[!redirects families of objects]]
[[!redirects family of morphisms]]
[[!redirects families of morphisms]]
[[!redirects indexed subcategory]]
[[!redirects indexed subcategories]]

[[!redirects family of subsets]]
[[!redirects families of subsets]]
