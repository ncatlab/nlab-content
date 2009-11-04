
This entry is supposed to suggest answers to the question: 

* "Why should I care about [[(infinity,1)-category|(infinity,1)-categories]]?"


# Natural language #

The language of $(\infty,1)$-categories happens to naturally capture, unify and also simplify a plethora of constructions and considerations in [[homotopy theory]], [[homological algebra]] and [[cohomology]] theory. All these subjects are thereby seen to be different realizations of a single underlying principle. 

To appreciate this point, it may be useful to first consider the analogous statement in the case of 1-[[category|categories]]:

## preparation: set theory is the theory of the category of sets ##

While mathematics is based to a large extent on the notion of a [[set]], the search for the _right_ formulation of [[set theory]] has been a long one. William Lawvere famously argued, in particular as discussed in his book

* F. William Lawvere, R. Rosebrugh, _[Sets for mathematics](http://books.google.de/books?id=h3_7aZz9ZMoC&pg=PP1&dq=sets+for+mathematics)_

that the theory of sets is indeed best understood as the theory of the _[[category]]_ [[Set]] of sets: this lore is called the [[ETCS|Elementary Theory of the Category of Sets]] ( _ETCS_ for short.)

A detailed pedagogical discussion of why it is good, right and possibly best to look at sets as [[object]]s in a certain [[category]] -- which in fact is a [[topos]] -- is given at [[Trimble on ETCS I]], [[Trimble on ETCS II|II]], [[Trimble on ETCS III|III]].

Possibly the most striking consequence of the realization that [[set theory]] is really the theory of the [[topos]] [[Set]] is that it widens the context and allows for considerable unification of concepts: 

A large class of general constructions and facts that work within [[Set]] (namely all those that make sense within [[constructive mathematics]]) actually make sense in every other [[topos]] (with [[natural numbers object]]), too. Using the concept of [[internalization]], the category-theoretic description of [[set theory]] extends to a considerable unification of concepts.  

In particular, every [[category of sheaves]] is a [[topos]] and therefore allows to be treated as a category of generalized sets. For instance the theory of [[generalized smooth space]]s, which underlies [[Lie theory]] is the study of the [[topos]] of [[sheaf|sheaves]] on the category [[Diff]] of [[manifold]]s. Constructions in this [[topos]], for instance involving [[group]]s, will be smooth versions of constructions in [[Set]], for instance [[Lie groupoid|Lie group]]s.



## induction: homotopy theory is the theory of the $(\infty,1)$-category of topological spaces ##

A further large part of mathematics is concerned not just with sets, but with sets that are equipped with the structure of a [[topological space]]. Their study is [[homotopy theory]].

If [[set theory]] is really the [[ETCS|elementary theory of the category of sets]], then what is [[homotopy theory]], really, in this sense? The answer to this is supposed to be: the theory of the [[(infinity,1)-category]] [[Top]] of topological spaces.

And the entire discussion for the 1-category [[Set]] above then has its analogs for the [[(infinity,1)-category]] [[Top]]. In particular, [[Top]] is an [[(infinity,1)-category]] which happens to be the archetypical example of an [[(infinity,1)-topos]]. This means that once one understands constructions in [[homotopy theory]] as $(\infty,1)$-categorical constructions, they tend to generalize to the wider contexts of other [[(infinity,1)-topos|(infinity,1)-topoi]].


+--{+ .query}

_David_ : Just as not all reasoning in the topos [[Set]] carries over to other toposes, what can be said of the reasoning in [[Top]] that does/does not work in other (infinity, 1)-toposes?

[[Urs Schreiber|Urs]]: good question. I added one little remark in response to this below. But likely much more could be said here (both known to date and not yet known to date, I suppose). In particular, this only addresses the geometric aspects of $(\infty,1)$-topoi. I don't think anyone has as yet considered $(\infty,1)$-topoi as context in which to interpret logic.  And after all, one must not forget that, [[Higher Topos Theory|HTT]] is only (hah!) about _Grothendieck_ $(\infty,1)$-topoi ($(\infty,1)$-presheaf topoi).

=--

Many constructions familiar from the [[homotopy theory]] of [[Top]] make sense in every [[(infinity,1)-topos]]. For an account see [section 6.5](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=521) [[Higher Topos Theory|HTT]]. 



## side remark: relation to more general $\infty$-categories ##

At this point the natural question is:

>But why then $(\infty,1)$-categories instead of directly more general [[infinity-category|infinity-categories]]?

This has a good but somewhat more technical answer:

the problem of defining higher categories is the problem of defining the right coherence laws -- associators, pentagonators and so forth. But even if the higher category in question is not groupoidal, i.e. is [[directed object|directed]], the coherence cells will be equivalences, i.e. weakly invertible cells. So the problem of controlling coherence laws is a problem of $(\infty,0)$-categorical nature. 

For this reason it is useful to first go to infinit cell degree with just the invertible cells, and  only after that start increasing the degree of the non-invertible cells. 

Concretely, we have the following useful constructions for $(\infty,1)$-categories:

* there is a simple definition of the [[(infinity,1)-category of (infinity,1)-categories]]. This should be the $(\infty,1)$-subcategory on all invertible 2-cells (transformations of $(\infty,1)$-functors) of the [[(infinity,2)-category of (infinity,1)-categories]], which has a more involved definition, but the point is that the $(\infty,1)$-category of all $(\infty,1)$-categories is already quite sufficient for many constructions. 

* there is a simple iterative definition of [[(infinity,n)-category]] by an iterative weak enrichment in $(\infty,n-1)$-categories, again precisely due to the presence of invertible cells in all degrees, which allows to say what a [[homotopy limit]] of $(\infty,n-1)$-categories is, as enters for instance in the definition of [[complete Segal space]].



## consequence: unification and generalization ##

In particular, there is an [[(infinity,1)-category of (infinity,1)-sheaves|(infinity,1)-category of (infinity,1)-sheaves]] on every [[site]] $S$. Homotopy theory inside these "Grothendieck-Rezk-Lurie" $(\infty,1)$-topoi is much like ordinary [[homotopy theory]], only that what used to be topological spaces are now generalized spaces called [[infinity-stack homotopically|infinity-stacks]].

This for instance yields a unified picture of [[cohomology]]: in [[Top]] the cohomology on one object $X$ with coefficients in another object $A$ is nothing but the [[hom-space]] $[X,A]$. By simply [[internalization|internalizing]] this statement into other [[(infinity,1)-topos|(infinity,1)-topoi]] one finds many notions of [[cohomology]] as special cases, for instance group cohomology, [[abelian sheaf cohomology]], [[nonabelian cohomology]].

More details on the key ideas of this are at [[motivation for sheaves, cohomology and higher stacks]].

Notably in the "abelian" or "stable" case, where the objects of the [[(infinity,1)-category]] don't just behave like [[topological space]]s but like [[spectrum|spectra]], this allows to subsume central developments in [[homological algebra]] in a simple pattern:

in its modern form [[homological algebra]] is about [[derived category|derived]] [[triangulated category|triangulated categories]]. But unfortunately the axioms of a [[triangulated category]] are a bit unwieldy, which is not just a practical nuisance but leads to bad behaviour of the general theory of these categories. But then it turns out that most triangulated categories that arise in practice are nothing but the 1-categorical shadow of what is called  a [[stable (infinity,1)-category]] (the [[homotopy category of an (infinity,1)-category|homotopy category of a stable (infinity,1)-category]]): an $(\infty,1)$-category in which each object is "stable"/"abelian" -- and moreover the definition of [[stable (infinity,1)-category]] is short and simple and obvious. The awkward axioms of [[triangulated category|triangulated categories]] follow from these simple laws by forcing them into the 1-categorical version.

## new possibilities ##

Natural language is never just a value in its own right, but always the potential to achieve new things which are literally unthinkable without this language.

The identification of a coherent framework of $(\infty,1)$-categories is rapidly leading to a wealth of new developments in areas where [[infinity-category]] theory has long been expected to be crucial, but never quite lived up to the status of a useful well-developed tool that would allow to go beyond its own introspection.

This is notably the case in (functorial extended topological) [[FQFT|quantum field theory]]:

* using [[(infinity,n)-category|(infinity,1)-categories]] iteratively built out of [[(infinity,1)-category|(infinity,1)-categories]] Jacob Lurie has formalized proven the fundamental structure theorem for extended topological [[quantum field theory]] (TFT): the [[generalized tangle hypothesis|Baez-Dolan hypothesis]];

* based on this, Ben-Zvi, Francis and Nadler have begun in their work on [[geometric infinity-function theory]] to systematically study those extended TFTs which arise from _geometric backgrounds_ as _$\sigma$-models_ using an $(\infty,1)$-categorical version of [[geometric function theory]]. They show that [[infinity-stack homotopically|infinity-stacks]] arising in [[Lie theory]] represent $\infty$-categorical extended TFTs in this sense which organize a rich amount of structures and theorems in [[representation theory]]. 

* this perspective also incorporates the $A_\infty$-categorical work by Kontsevich, Fukaya and others on homological mirror symmetry: linear [[A-infinity category|A-infinity categories]] are equivalent to [[dg-category|dg-categories]] and [[pretriangulated dg-category|pretriangulated dg-categories]] are [[stable (infinity,1)-category|stable (infinity,1)-categories]].


(... needs more detals and more scope ...)


***

#Discussion#

A previous version of this entry triggered the following discussion.

+--{+ .query}

This gives impression that (infty,1) categories are the first higher categorical framework to naturally capture TQFT-s, and derived techniques in rep theory. My impression is that so far much greater number of concrete cases has been worked out using A-infty categories, related to mirror
symmetry and related models; and the picture in Lagrangean geometry and homological mirror symmetry emerged in works of Fukaya and Kontsevich in early 1990s. Can (infty, 1) approach at least reproduce after the fact the results which can be studied using Ainfty setup ? in particular is there a good treatment of Lagrangean intersection theory using derived geometry of topos and (infty,1) school ? -- [[Zoran Skoda|Zoran]]

[[Urs Schreiber|Urs]]: good point. I'll have to think about that. Just two quick remarks: 

* David Ben-Zvi keeps emphasizing that the dg-categories used in much of this QFT business are naturally thought of as $(\infty,1)$-categories. For instance in his latest article he makes some connection to the Kapustin-Witten description.

* Over on the blog John and Mike are talking about whether and in which sense $A_\infty$-categories are models for $(\infty,1)$-categories, too.


[[David Ben-Zvi]] (by email, forwards here by [[Urs Schreiber|Urs]]): the $A-\infty$ categories appearing
in the literature mentioned above are all $A-\infty$ categories in the usual linear sense (unlike the nonlinear ones John talks about on the blog). Anyway these are all quasiequivalent to dg categories - ie. the $\infty$-cats of dg cats and $A_\infty$-cats are all the same. 
In particular they are all examples of $(\infty,1)$-cats -- and are almost stable
(ie. they might be too small, like dg cats with one object, but if you add cones to them -- aka passing to their category of modules or derived category -- you get a stable $\infty$-cat. So it's really the same subject,
or rather rationally these are all equivalent languages.)

=--


[[!redirects Why (infinity,1)-categories?]]
[[!redirects Why (∞,1)-categories?]]
[[!redirects why (∞,1)-categories?]]
[[!redirects why (∞,1)-categories]]
[[!redirects why (infinity,1)-categories]]