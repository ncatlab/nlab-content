

# Contents #
* automatic table of contents
{:toc}


## Idea ##

As a [[Grothendieck topos]] is a [[categorification|categorified]] [[locale]], so an ionad is a categorified [[topological space]].  While the opens are primary in toposes and locales, the points are primary in ionads and topological spaces.

[[Richard Garner]] developed the theory of ionads, in which the [[topos]] $Set^X$ plays an role analogous to that of the [[lattice]] $\mathbb{2}^X$ (the [[power set]] of $X$) in the theory of topological spaces.

+--{: .query}
[[David Roberts]]: The idea strikes me that we are passing from the [[subobject classifier]] $2 = \{0 \lt 1\}$ in $Set$ (assuming classical Booleaness) to the categorified subobject classifier $Set$ in $Cat$.

_Toby_:  I expect that you know this, David, but for the record: it\'s still the subobject classifier constructively, but that may not be $2$.  I have written this as '$\mathbb{2}$' to try to keep it simple but unbiased.
=--

The word 'ionad' is Irish for a location, place, or site; 'Ionad' often translates 'Centre' in titles of institutions.  It is pronounced /&#712;&#618;n&#601;d/ (roughly 'INN-ad' or 'UNN-ad', not 'i-NAD' or 'yonad'; '&#1067;&#1053;-&#1072;&#1076;' in a North Slavic language), or more precisely [&#712;&#616;&#798;n&#810;&#736;&#601;d&#810;&#736;] (at least in Munster), following [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Irish_phonology).  The plural (which you can use if you like to use 'topoi' too) is 'ionaid' (/&#712;&#618;n&#601;&#607;/, 'INN-adge' or 'UNN-adge', '&#1067;&#1053;-&#1072;&#1076;&#1100;', [&#712;&#616;&#798;n&#810;&#736;&#601;d&#690;]).  We could go on to decline it out of the nominative case, but now it\'s getting silly.

+--{: .query}
[[Finn Lawler]]: I would pronounce this more like 'UNN-ad' (I don't know enough about IPA to make that more precise).  The Irish dialect I was exposed to (there being no Dublin or Leinster dialect) is the standard one taught in schools, which is an amalgam of all three, but principally that of Connacht, I think.

The nominative plural is 'ionaid', which I would pronounce something like 'UNN-idge'.  Here the 'd' is palatized.

_Toby_:  I\'m just using my knowledge of phonology to follow the information on Wikipedia\'s articles, so take it with a grain of salt.  However, I can imagine someone hearing [&#712;&#616;&#798;n&#810;&#736;&#601;d&#810;&#736;] as 'UNN-ad', so I happily add it to the text.  I don\'t suppose you can get a good recording?  (Also, thanks for the plural, which I should have looked up for myself.)
=--


## Definition

Recall that a [[topological space|topology]] on a set $X$ can be defined by giving its interior operator, an operation $Int\colon \mathbb{2}^X \to \mathbb{2}^X$ (where $\mathbb{2}$ is the poset of [[truth values]]) such that

*  $A \supseteq Int(A)$,
*  $Int(Int(A)) \supseteq Int(A)$,
*  $Int(X) = X$, and
*  $Int(A \cap B) = Int(A) \cap Int(B)$

for all [[subsets]] $A, B$ of $X$.

In more sophisticated language, $Int$ is a finite [[meet]]-preserving [[comonad]] on the [[power set]] of $X$.

[[categorification|Categorifying]] (mostly), we have this:

+-- {: .un_defn}
###### Definition

An __ionad__ is a set $X$ together with a [[left exact functor|finite limit-preserving]] [[comonad]] $Int_X$ on the category $Set^X$.  An ionad is __bounded__ if the comonad is [[accessible monad|accessible]].
=--

+-- {: .query}
It seems to me that a full categorification would allow $X$ to be a [[groupoid]].  ---Toby

[[Mike Shulman]]: Actually, if you want to allow groupoids, I don't think there's any reason not to allow arbitrary categories.  Richard and I had a discussion about this question, and at one point I think he was on the side you present, but we've both since come around to this version.  Notice that any ionad *induces* a category structure on its set of points, since each point is in particular a geometric morphism from $Set$ to $\Omega(X)$.  I think this induced "category of points" should be regarded as a categorification of the [[specialization order]] *induced* on the points of a topological space.  In particular, it comes for free as part of the structure; you don't have to specify it in advance.

You *can* specify either of them in advance; you can start with $X$ being a category in the definition of ionad, or you can define a generalized sort of topological space as a poset equipped with a lex comonad on its poset of downsets.  In either case it amounts to specifying an ordinary ionad/space, together with a distinguished category/poset mapping bijectively-on-objects to its induced category/poset of points.  In both cases, any continuous map necessarily preserves the induced category/order, but if you start with a distinguished category/order of points, your continuous maps have to preserve that too.  These notions might be interesting, but the comparison makes me fairly sure that ionads starting with a *set* are already the natural "fully categorified" categorification of topological space.

_Toby_:  I didn\'t want to allow just any category, to be analogous to not allowing just any p(r)oset as points of a topological space.  But I\'ll think about what happens when the points are allowed to form a groupoid.

[[Mike Shulman]]: I think the same argument applies to groupoids.  As I said, any ionad induces a category structure on its set of points, and if you start with a groupoid you're just picking a distinguished groupoid on that set of points which maps bijectively-on-objects to the induced category.

It's like the difference between a [[Segal space]] and a [[complete Segal space]].  Segal spaces may be interesting, but it's the complete ones that model $(\infty,n)$-categories.  And also the difference between an ordinary multicategory and an "enhanced" multicategory in the sense of Baez-Dolan-Cheng.  The weird notions that come with an extra groupoid structure on the objects may be technically useful, but usually the more fundamental notion is the one where the groupoid of objects is induced from the category of objects.
=--

Although Garner does not require an ionad to be bounded, the nicest results hold for them, and all of his applications involve only bounded ionads.  In fact, Garner writes, 'Indeed, the existence of unbounded ionads is a problem that seems to be independent of the axioms of [[Zermelo-Fraenkel set theory]].' (Section 3.8).


## Morphisms of ionads ##

Recall that, given two topological spaces $X$ and $Y$, a [[continuous map]] from $X$ to $Y$ is a [[function]] $f\colon X \to Y$ (on the [[underlying set]]s) such that

*  $f^*(Int(A)) \subseteq Int(f^*(A))$

for every subset $A$ of $Y$, where $f^*$ takes the [[preimage]].

Categorifying (and adding a coherence law), we have this:

+-- {: .un_defn}
###### Definition

Given ionads $X$ and $Y$, a __continuous map__ from $X$ to $Y$ consists of a [[function]] $f\colon X \to Y$ (on the underlying sets of points) together with a [[natural transformation]]
$$ Int_f\colon f^* \circ Int_Y \to Int_X \circ f^* ,$$
where $f^*\colon Set^Y \to Set^X$ is $Set^f$, such that $Int_f$ 'respects the comonad structures'.
=--

+-- {: .query}
I need to figure out exactly what this last clause means.
=--

Note that $Int_f$ is part of the [[extra structure|structure]] here; it is not merely a property.  (In other words, the [[forgetful functor]] from ionads to topological spaces is not [[faithful functor|faithful]].)

There is an obvious notion of [[2-morphism]], which turns out to be trivial (but probably would not be if $X$ were allowed to be a groupoid).  However, the category of ionads is presumably (like [[Top]]) still a [[locally prosetal 2-category]] under the [[specialisation order]].


## The topos of opens

As every topological space has a [[Heyting algebra]] (in fact a [[frame]], or dually a [[locale]]) of open subsets, so every ionad has a [[topos]] (in fact a [[Grothendieck topos]], if it is bounded) of opens.

+-- {: .un_defn}
###### Definition

Given an ionad $X$, an __open__ in $X$ is simply a [[algebra of a monad|coalgebra]] of the comonad $Int_X$.
=--

The opens of $X$ form a topos $\Omega(X)$, and we have a [[surjective geometric morphism|surjective]] [[geometric morphism]] from $Set^X$ to $\Omega(X)$.  In fact, an ionad may be defined as a set $X$ together with a surjective geometric morphism from $Set^X$ to some topos, much as a topological space may be defined as a set $X$ together with a surjective locale morphism from $\mathbb{2}^X$ to some [[locale]].  The topos $\Omega(X)$ is essentially unique by surjectivity, and this also shows that $\Omega(X)$ has [[enough points]].

Just as $\Omega(X)$ is a [[frame]] whenever $X$ is a topological space, so $\Omega(X)$ should be a [[Grothendieck topos]] when $X$ is an ionad.  In fact, this holds only for *bounded* ionads; an ionad may be defined to be bounded if and only if its topos of opens is [[cocomplete category|cocomplete]] (or equivalently a Grothendieck topos).

A continous map between topological spaces may be given by a function $f\colon X \to Y$ and a commuting square

$$ \array {
   \Omega(Y)    & \to              & \Omega(X) \\
   \downarrow   &                  & \downarrow \\
   \mathbb{2}^Y & \overset{f^*}\to & \mathbb{2}^X
} $$

Similarly, a continuous map between ionads may be given by a function $f\colon X \to Y$ and a commuting square

$$ \array {
   \Omega(Y)    & \to              & \Omega(X) \\
   \downarrow   &                  & \downarrow \\
   Set^Y        & \overset{f^*}\to & Set^X
} $$

Without loss of generality, we may require this square to commute on the nose; this is related to the triviality of $2$-morphisms in the category of ionads.

Note that the map $\Omega(Y) \to \Omega(X)$ must be the preimage half of a [[geometric morphism]] from $\Omega(X)$ to $\Omega(Y)$; we may also define a continous map $X$ to $Y$ to be such a geometric morphism together with a compatible map between the generating points of the toposes.


## Bases of ionad structures

...


## References ##

Ionads have been introduced and studied in 

*  [[Richard Garner]], _Ionads: a generalisation of the notion of topological space_, ([web](http://www.dpmms.cam.ac.uk/~rhgg2/Ionads/Ionads.html), [pdf](http://www.dpmms.cam.ac.uk/~rhgg2/Ionads/Ionads.pdf))

Some basic aspects of the theory are developed there, and applications to [[topology]], [[logic]] and [[geometry]] are discussed. 


[[!redirects ionaid]]