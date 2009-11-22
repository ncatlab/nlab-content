

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

The word 'ionad' is Irish for a location, place, or site; 'Ionad' often translates 'Centre' in titles of institutions.  It is pronounced /&#712;&#618;n&#601;d/ (roughly 'INN-ad', not 'i-NAD' or 'yonad'), or more precisely [&#712;&#616;&#798;n&#810;&#736;&#601;d&#810;&#736;] (at least in Munster), following [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Irish_phonology).


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
   \Omega(Y)    & \to & \Omega(X) \\
   \downarrow   &     & \downarrow \\
   \mathbb{2}^Y & f^* & \mathbb{2}^X
} $$

Similarly, a continuous map between ionads may be given by a function $f\colon X \to Y$ and a commuting square

$$ \array {
   \Omega(Y)    & \to & \Omega(X) \\
   \downarrow   &     & \downarrow \\
   Set^Y        & f^* & Set^X
} $$

Without loss of generality, we may require this square to commute on the nose; this is related to the triviality of $2$-morphisms in the category of ionads.

Note that the map $\Omega(Y) \to \Omega(X)$ must be the preimage half of a [[geometric morphism]] from $\Omega(X)$ to $\Omega(Y)$; we may also define a continous map $X$ to $Y$ to be such a geometric morphism together with a compatible map between the generating points of the toposes.


## Bases of ionad structures

Recall that, given a set $X$, a basis for a topology on $X$ is given by a collection $B$ of subsets of $X$ that is [[filter|cofiltered]], in the sense that

...


## References ##

Ionads have been introduced and studied in 

*  [[Richard Garner]], _Ionads: a generalisation of the notion of topological space_, ([web](http://www.dpmms.cam.ac.uk/~rhgg2/Ionads/Ionads.html), [pdf](http://www.dpmms.cam.ac.uk/~rhgg2/Ionads/Ionads.pdf))

Some basic aspects of the theory are developed there, and applications to [[topology]], [[logic]] and [[geometry]] are discussed. 