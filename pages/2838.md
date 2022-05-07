
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Contents #
* table of contents
{:toc}


## Idea ##

As a [[Grothendieck topos]] is a [[categorification|categorified]] [[locale]], so an ionad is a categorified [[topological space]].  While the opens are primary in toposes and locales, the points are primary in ionads and topological spaces.

[[Richard Garner]] developed the theory of ionads, in which the [[topos]] $Set^X$ plays an role analogous to that of the [[lattice]] $\mathbb{2}^X$ (the [[power set]] of $X$) in the theory of topological spaces.  Intuitively, we are [[categorification|categorifying]] the [[subobject classifier]] $\mathbb{2}\in Set$ to the "categorified subobject classifier" $Set\in Cat$ (which classifies [[discrete opfibrations]].

The word 'ionad' is Irish for a location, place, or site; 'Ionad' often translates 'Centre' in titles of institutions.  It is pronounced /&#712;&#618;n&#601;d/ (roughly 'INN-ad' or 'UNN-ad', not 'i-NAD' or 'yonad'; '&#1067;&#1053;-&#1072;&#1076;' in a North Slavic language), or more precisely [&#712;&#616;&#798;n&#810;&#736;&#601;d&#810;&#736;] (at least in Munster), following [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Irish_phonology).  The plural (which you can use if you like to use 'topoi' too) is 'ionaid' (/&#712;&#618;n&#601;&#607;/, 'INN-adge' or 'UNN-adge', '&#1067;&#1053;-&#1072;&#1076;&#1100;', [&#712;&#616;&#798;n&#810;&#736;&#601;d&#690;]).  We could go on to decline it out of the nominative case, but now it\'s getting silly.

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

Although Garner does not require an ionad to be bounded, the nicest results hold for them, and all of his applications involve only bounded ionads.  In fact, Garner writes, 'Indeed, the existence of unbounded ionads is a problem that seems to be independent of the axioms of [[Zermelo-Fraenkel set theory]].' (Section 3.8).

+-- {: .un_defn}
###### Remark (Garner Remark 3.9)
Bounded ionads give rise to exactly the Grothendieck toposes with [[point of a topos|enough points]] as their topos of coalgebras. (See below)
=--

### Sets, groupoids, or categories?

It may seem odd to take $X$ to be a *set* rather than something else such as a [[groupoid]] or a [[category]].  An analogous definition can be given where $X$ is a groupoid or a category, of course, but the reason for taking it to be a set is that it makes the analogy to classical topological spaces closer.  Consider the following three notions:

1. A set $X$ together with a finite-limit-preserving comonad on its powerset $\mathbb{2}^X$.
2. A set $X$ equipped with an [[equivalence relation]] (which we can regard as a [[preorder]] that happens to be symmetric) together with a finite-limit-preserving comonad on the hom-preorder $\mathbb{2}^X$.
3. A [[preorder]] $X$ together with a finite-limit-preserving comonad on $\mathbb{2}^X$.

All three of these *induce* a topology on the underlying set of $X$.  But it is (1) that is *exactly* a topological space: (2) and (3) include the extra data of a (perhaps symmetric) preorder on $X$ that maps bijectively-on-objects into the [[specialization preorder]] of that topology.

However, as in other cases such as [[Segal categories]]/[[complete Segal spaces]] and [[generalized multicategories]], another way to "get rid of extra data" is to  force it to duplicate data that's already present (a "completeness" condition).  Thus we could consider instead (still in the uncategorified case):

* A structure as in (2) above, but such that the given equivalence relation coincides with the relation "$x$ and $y$ are in all the same open sets" (which it automatically *implies*).
* A structure as in (3) above, but such that the given preorder coincides with the specialization preorder.

These would give equivalent definitions to (1), but may be better-behaved in some ways.  In [[homotopy type theory]] without [[sets cover]], they would no longer be equivalent, but the groupoidal/preorder versions might be better.  For ionads the corresponding definitions would be

* A groupoid $X$ with a finite-limit-preserving comonad on $Set^X$ such that the induced functor from $X$ to the category of points of the resulting topos is [[pseudomonic functor|pseudomonic]].
* A category $X$ with a finite-limit-preserving comonad on $Set^X$ such that the induced functor from $X$ to the category of points of the resulting topos is [[fully faithful]].

(Asking that these functors also be surjective on objects would be a [[sober space|sobriety]] condition on an ionad.)

When categorifying further to "$n$-ionads" and "$\infty$-ionads", the possible options multiply further; but that is probably a topic for another page.  For discussion of these questions, see the [nForum thread](https://nforum.ncatlab.org/discussion/5857).


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

*  [[Richard Garner]], _Ionads_,  J. Pure Appl. Algebra 216 (2012), no. 8-9, 1734&#8211;1747. ([arXiv](http://arxiv.org/abs/0912.1415)) ([doi](http://dx.doi.org/10.1016/j.jpaa.2012.02.013)) ([author-archived version of published copy](http://comp.mq.edu.au/~rgarner/Papers/Ionads.pdf))

Some basic aspects of the theory are developed there, and applications to [[topology]], [[logic]] and [[geometry]] are discussed. 


[[!redirects ionads]]

[[!redirects ionaid]]
