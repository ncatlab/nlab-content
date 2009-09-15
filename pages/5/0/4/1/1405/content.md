<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>


While an [[algebraic definition of higher category|algebraic]] definition of [[strict ∞-categories]] is comparatively straightforward, algebraic definitions of fully weak $\omega$-categories (aka $\infty$-[[infinity-category|categories]]) are difficult to work with (although some definitions exist, such as those of [[Batanin n-category|Batanin]], [[Leinster n-category|Leinster]], and [[Penon n-category|Penon]]).

Howver, just like strict $\omega$-categories have a [[simplicial set|simplicial]] [[nerve]] -- a [[complicial set]] -- induced by the [[orientals]], and just like the category of strict $\omega$-categories is equivalent to the category of complicial sets, one expects that every weak $\omega$-category naturally has a simplicial nerve and that the theory of algebraically defined weak $\omega$-categories is equivalent to the theory of the simplicial sets that arise as their nerves.  In fact, one can hope that the theory is _simpler_ in the weak case: complicial sets are simplicial sets equipped with extra [[stuff, structure, property|structure]] (a [[stratified simplicial set|stratification]] representing the chosen 'strict' composites), while in the nerve of a weak $\omega$-category this structure might be reducible to a property.

In the context of _simplicial models for weak $\omega$-categories_ the goal is to characterize those [[simplicial sets]] (or [[stratified simplicial sets]]) which should arise as [[nerves]] of algebraically defined weak $\omega$-categories and thus provide a [[geometric definition of higher category]] generalizing the familiar simplicial description of $\omega$-[[infinity-groupoid|groupoids]] as [[Kan complexes]] and of $(\omega,1)$-[[(infinity,1)-category|categories]] as [[quasi-category|quasi-categories]] to general higher categories.

In effect, the goal is to _define_ a weak $\omega$-category to be a certain sort of ([[stratified simplicial set|stratified]]) simplicial set.  One could then hope to prove that these are precisely the [[nerve|nerves]] of weak $\omega$-categories defined in some other way.


To distinguish the study of weak $\omega$-categories in terms of their presumed nerves from the study of their would-be algebraic descriptions people speak of [[simplicial weak omega-category|simplicial weak ∞-categories]], see in particular the articles by Dominic Verity referenced below.  One should just beware that in this context [[simplicial weak ∞-category]] is not meant as [[simplicial object]] in the category of weak $\omega$-categories.

This program was originally begun by Ross Street and has been carried forward by Dominic Verity with the theory of [[weak complicial sets]].  It is expected that the (nerves of) weak $\omega$-categories will be weak complicial sets satisfying an extra "saturation" condition ensuring that "every [[equivalence]] is [[thin element|thin]]."

#References#

* [[Dominic Verity]], _Weak complicial sets, a simplicial weak omega-category theory. Part I: basic homotopy theory_ ([arXiv](http://arxiv.org/abs/math.CT/0604414))

* [[Dominic Verity]], _Weak complicial sets, a simplicial weak omega-category theory. Part II: nerves of complicial Gray-categories_ ([pdf](http://uk.arxiv.org/PS_cache/math/pdf/0604/0604416v1.pdf))

***

Discussion on a previous version of this entry:

+--{: .query}
[[Mike Shulman|Mike]]: This term is kind of unfortunate; *simplicial weak $\omega$-category* could also mean a simplicial object in weak $\omega$-categories.  I don't suppose we can do anything about that?

[[Urs Schreiber|Urs]]: my impression is that what Dominic Verity mainly wants to express with the term is "simplicial model for weak $\omega$-category". Maybe we could/should use a longer phrase like that?

[[Mike Shulman|Mike]]: That would make me happier.

[[Urs Schreiber|Urs]]: okay, I changed it. Let me know if this is good now.

_Toby_:  But what about 'globular $\omega$-category' and things like that?  Doesn\'t 'simplicial $\omega$-category' fit right into that framework?  This page title sounds like an entire framework for defining $\omega$-category rather than a single $\omega$-category simplicially defined.

[[Urs Schreiber|Urs]]: i am open to suggestions -- but notice that it does indeed seem to me that Dominic Verity wants to express  "an entire framework for defining $\omega$-category", namely the framework where one skips over the attempt to define $\omega$-categories and instead tries to find a characterization of what should be their nerves.

_Toby_:  OK, that fits in with most of what\'s written here, but not the beginning
>**Simplicial models for weak $\omega$-categories** -- sometimes called [[simplicial weak omega-category|simplicial weak ∞-categories]] -- are [...]
Maybe that was just poorly written, but it threw me off.
Should it be
>A **simplicial model for weak $\omega$-categories** -- which are then sometimes called [[simplicial weak ∞-categories]] -- is [...]
or even
>A **simplicial model for weak $\omega$-categories** is [...]
and only later mention [[simplicial weak ∞-categories]]?

[[Mike Shulman|Mike]]: You're right that 'simplicial $\omega$-category' it fits into 'globular $\omega$-category' and 'opetopic $\omega$-category' and so on.  It seems more problematic in this case, though, since simplicial objects of random categories are a good deal more prevalent than globular ones and opetopic ones.  But perhaps I should just live with it.  

[[Urs Schreiber|Urs]]: I have now expanded the entry text on this point, trying to make very clear to the reader what's going on here.

_Toby_:  Thanks, that\'s much clearer.  And if Verity\'s definition is at [[weak complicial set]], then we may not really need anything at [[simplicial weak ∞-category]], so no need to offend Mike\'s sensibilities (^_^) either.

=--

[[!redirects simplicial model for weak ∞-categories]]