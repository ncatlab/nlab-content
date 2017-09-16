# Idea #

If a [[linear order]] is a way of arranging the elements of a set 'on a line' (with a direction), then a *cyclic order* is a way of arranging them 'on a circle' (with a chosen direction, say clockwise or counterclockwise).


# Definition #

Unlike a linear order (and most other things called 'order') which are defined as a sort of binary relation, a cyclic order is defined as a sort of *ternary* relation, since on a circle we can't say that "$x$ comes before $y$" only that "$x$, $y$, and $z$ come in (say) clockwise order."

Formally, a **cyclic order** on a set $S$ is a ternary relation $R$ on $S$ such that for all $x,y,z,w\in S$:

* If $R(x,y,z)$, then $R(y,z,x)$ (and hence also $R(z,x,y)$).

* If $R(x,y,z)$, then $x$, $y$, and $z$ are pairwise distinct (a ternary version of [[irreflexive relation|irreflexivity]]).

* If $x$, $y$, and $z$ are pairwise distinct, then either $R(x,y,z)$ or $R(x,z,y)$ (a ternary version of [[trichotomous relation|trichotomy]]).

* If $R(x,y,z)$ and $R(x,z,w)$, then $R(x,y,w)$ (a ternary version of [[transitive relation|transitivity]]).

Note that irreflexivity and transitivity together imply that $R(x,y,z)$ and $R(x,z,y)$ cannot both hold.

+--{: .query}
[[Mike Shulman|Mike]]: I took this from [Wikipedia](http://en.wikipedia.org/wiki/Cyclic_order); it is evidently a cyclic analogue of a [[linear order]].  If anyone wants to have a go at a cyclic analogue of a [[total order]] or at the right way of making this [[constructive mathematics|constructive]], be my guest.
=--


# Monotone functions #

A function $f:S\to T$ between cyclically ordered sets is **strictly monotone** if it preserves the ternary relation $R$, i.e. if $R_S(x,y,z)$ implies $R_T(f(x),f(y),f(z))$.  This is the cyclic counterpart of a strictly monotone function between linear orders (one which preserves the relation $\lt$).  As in that case, irreflexivity then implies that $f$ is necessarily injective (as long as $S$ has at least three distinct elements).

We say that $f$ is merely **monotone** if it satisfies (either of) the following _equivalent_ conditions:

* $f$ reflects the ternary relation $R$, i.e. if $R_T(f(x),f(y),f(z))$ then $R_S(x,y,z)$.

* $f$ preserves the ternary relation $R$ for elements with pairwise distinct images, i.e. if $R_S(x,y,z)$ holds and $f(x)$, $f(y)$, and $f(z)$ are pairwise distinct, then $R_T(f(x),f(y),f(z))$.

This is the cyclic counterpart of a monotone function between [[total order]]s (one which preserves the relation $\le$).

+--{: .query}
[[Mike Shulman|Mike]]: I just made this up, but it seems right.  With a $\le$-version of cyclic orders we could maybe recover monotone functions more directly.  Whatever the definition of monotone function is, it should let us recover $\Lambda$ as below.
=--


# Remarks #

* The [[Connes' cyclic category|cycle category]] $\Lambda$ is the category of finite nonempty cyclically ordered sets and monotone functions, just as the [[simplex category]] $\Delta$ is the category of finite nonempty totally ordered sets and monotone functions.
