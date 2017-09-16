
A _stable $(\infty,1)$-topos_ is to an [[(infinity,1)-topos]] as a [[stable (infinity,1)-category]] is to an [[(infinity,1)-category]].

Recall that a Grothendieck-Rezk-Lurie [[(infinity,1)-topos]] is an [[(infinity,1)-category of (infinity,1)-sheaves]], i.e. of [[sheaf|sheaves]] with values in the [[(infinity,1)-category]] of [[infinity-groupoid]]s. 

A _stable_ Grothendieck--Rezk--Lurie [[(infinity,1)-topos]] should therefore be an [[(infinity,1)-category]] of [[sheaf|sheaves]] with values in [[spectrum|spectra]].

But maybe a full formalization of this idea has not appeared yet (?)

+--{: .query}
[[Mike Shulman|Mike]]: While the general study of sheaves of spectra is certainly an important topic, I'm not sure I agree that they should be called "stable $(\infty,1)$-toposes."  They're not very topos-like; they're much more like, say, [[Ab]].

[[Urs Schreiber|Urs]]: okay, right. We should remove this entry then, or do something to it. But let's see why I created it, that may indicate a question I have which would be nice to answer in some form:

over at [[cohomology]] I said something like: see, in every $(\infty,1)$-category $H$ which behaves roughly like [[Top]] does, we are entitled to think of the hom-spaces $H(X,A)$ as computing cohomology of the source object $X$ with coefficients in the target object $A$;

if the objects of $H$ moreover are stable, then this reproduces abelian cohomology.

so I wanted to put this together and say: if it looks stable and homs in it can be thought of as computing cohomology, then it should be called  stable $(\infty,1)$-topos. Now, I see, that may be a wrong idea. But don't we want to say _something_ like that? Or should we think of the hom spaces of _every_ possible $(\infty,1)$-category as some kind of cohomology? That seems wrong, too. (?)

_Toby_:  You could call this an _abelian $(\infty,1)$-category_.  A topos is like the category of sets ($0$-groupoids), while an abelian category is like the category of abelian groups (stably monoidal $0$-groupoids).  So we just change $0$ to $(\infty,1)$, equivalently $1$ to $(\infty,1)$, in both of those.

[[Mike Shulman|Mike]]: Well, while an abelian category is like the category of abelian groups, there are plenty of abelian categories other than categories of abelian sheaves, and it sounds like Urs is particularly interested in $(\infty,1)$-categories of sheaves of spectra.

Also, I feel like a broken record saying this, but the category of spectra is _not_ the category of stably monoidal $\infty$-groupoids; that would be the category of _connective_ spectra.

_Toby_:  I didn\'t think that this would make a difference to the elementary properties of the category, but maybe that\'s wrong.  I certainly see your point about restricting to categories of sheaves, however; I expected that that would go under the 'Grothendieck' or 'Grothendieck--Rezk--Lurie' condition.  But do we even have yet a notion of 'Grothendieck' abelian category that reproduces the concept of a category of abelian sheaves (other than simply 'category of abelian shaves')?

[[Mike Shulman|Mike]]: Including the non-connective spectra makes a big difference to the elementary properties: otherwise the "suspension" functor would not be an auto-equivalence.  I don't think I've ever seen a set of Giraud-like axioms for categories of abelian sheaves, but it seems plausible that they might exist.  I'm nothing like an expert on abelian categories.

_Toby_:  All right.  Well, it might be possible to get something out of 'abelian' yet, but presumably not 'abelian $(\infty,1)$-category' exactly.

_Mike_: Maybe the best notion of "abelian" in the $(\infty,1)$-world is just a [[stable (infinity,1)-category]].
=--
