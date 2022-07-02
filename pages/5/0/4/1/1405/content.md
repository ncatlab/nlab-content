
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

While an [[algebraic definition of higher category|algebraic]] definition of [[strict ∞-categories]] is comparatively straightforward, algebraic definitions of fully weak $\omega$-categories (aka $\infty$-[[infinity-category|categories]]) are difficult to work with (although some definitions exist, such as those of [[Batanin ∞-category|Batanin]], [[Trimble n-category|Trimble]], [[Leinster n-category|Leinster]], and [[n-category|Penon]]).

However, just like strict $\omega$-categories have a [[simplicial set|simplicial]] [[nerve]] -- a [[complicial set]] -- induced by the [[orientals]], and just like the category of strict $\omega$-categories is equivalent to the category of complicial sets, one expects that every weak $\omega$-category naturally has a simplicial nerve and that the theory of algebraically defined weak $\omega$-categories is equivalent to the theory of the simplicial sets that arise as their nerves.  In fact, one can hope that the theory is _simpler_ in the weak case: complicial sets are simplicial sets equipped with extra [[stuff, structure, property|structure]] (a [[stratified simplicial set|stratification]] representing the chosen 'strict' composites), while in the nerve of a weak $\omega$-category this structure might be reducible to a property.

In the context of _simplicial models for weak $\omega$-categories_ the goal is to characterize those [[simplicial sets]] (or [[stratified simplicial sets]]) which should arise as [[nerves]] of algebraically defined weak $\omega$-categories and thus provide a [[geometric definition of higher category]] generalizing the familiar simplicial description of $\omega$-[[infinity-groupoid|groupoids]] as [[Kan complexes]] and of $(\omega,1)$-[[(infinity,1)-category|categories]] as [[quasi-category|quasi-categories]] to general higher categories.

In effect, the goal is to _define_ a weak $\omega$-category to be a certain sort of ([[stratified simplicial set|stratified]]) simplicial set.  One could then hope to prove that these are precisely the [[nerve|nerves]] of weak $\omega$-categories defined in some other way.


To distinguish the study of weak $\omega$-categories in terms of their presumed nerves from the study of their would-be algebraic descriptions people speak of [[simplicial weak omega-category|simplicial weak ∞-categories]], see in particular the articles by Dominic Verity referenced below.  One should just beware that in this context [[simplicial weak ∞-category]] is not meant as [[simplicial object]] in the category of weak $\omega$-categories.

This program was originally begun by Ross Street and has been carried forward by Dominic Verity with the theory of [[weak complicial sets]].  It is expected that the (nerves of) weak $\omega$-categories will be weak complicial sets satisfying an extra "saturation" condition ensuring that "every [[equivalence]] is [[thin element|thin]]."

#References#

* [[Dominic Verity]], _Weak complicial sets, a simplicial weak omega-category theory. Part I: basic homotopy theory_ ([arXiv](http://arxiv.org/abs/math.CT/0604414))

* [[Dominic Verity]], _Weak complicial sets, a simplicial weak omega-category theory. Part II: nerves of complicial Gray-categories_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0604/0604416v1.pdf))

[[!redirects simplicial model for weak ∞-categories]]
[[!redirects simplicial models for weak ∞-categories]]
[[!redirects simplicial models for weak omega-categories]]