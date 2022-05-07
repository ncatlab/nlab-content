
# Cyclic orders
* table of contents
{: toc}

## Idea #

If a [[linear order]] is a way of arranging the elements of a set 'on a line' (with a direction), then a *cyclic order* is a way of arranging them 'on a circle' (with a chosen direction, say clockwise or counterclockwise).

Unlike a linear order (and most other things called 'order') which are defined as a sort of binary relation, a cyclic order is defined as a sort of *ternary* [[relation]], since on a circle we can't say "$x$ comes before (or after) $y$" only "$x$, $y$, and $z$ come in clockwise (or counterclockwise) order."


## Definition #

A **cyclic relation** on a [[set]] $S$ is a ternary [[relation]] $R$ on $S$ such that, if $R(x,y,z)$ for any elements $x, y, z$ of $S$, then $R(y,z,x)$ (and hence also $R(z,x,y)$).

Then a **cyclic order** on $S$ is a cyclic relation $R$ that satisfies ternary versions of the properties of a [[linear order]]:

*  Cyclic [[irreflexive relation|irreflexivity]]:  If $R(x,y,z)$, then $y \ne z$.
*  Cyclic [[asymmetric relation|asymmetry]]:  If $R(x,y,z)$ and $R(x,z,w)$, then $y \ne w$.
*  Cyclic [[transitive relation|transitivity]]:  If $R(x,y,z)$ and $R(x,z,w)$, then $R(x,y,w)$.
*  Cyclic [[comparison]]:  If $R(x,y,z)$, then for any $w$, $R(x,y,w)$ or $R(x,w,z)$ or $R(w,y,z)$.
*  Cyclic [[connected relation|connectedness]]:  If $x \ne y$, $x \ne z$, and $y \ne z$, then $R(x,y,z)$ or $R(x,z,y)$.

Actually, none of these order axioms (except for comparison) is really complete as stated; any cyclic permutation of the axiom should also be assumed.  However, these permutations all follow automatically for a cyclic relation.

Note that for a [[constructive mathematics|constructive]] version, the set $S$ needs to be already equipped with a (tight) [[apartness relation]] for the connectedness axiom to make sense; unlike with a linear order, we can\'t recover the apartness relation from the cyclic order.  For a similar reason, it\'s difficult to state [[antisymmetric relation|antisymmetry]] correctly for a nonstrict (like a [[total order]]) version of a cyclic order.


As with a linear order, not all of these axioms are needed.  In particular, using [[excluded middle]], it\'s enough if a cyclic relation is transitive and satisfies

*  Cyclic trichotomy:  For all $x, y, z$, ($x = y$ or $x = z$ or $y = z$) xor $R(x,y,z)$ xor $R(x,z,y)$.


## Monotone functions

An [[injection|injective]] function $f:S\to T$ between cyclically ordered sets is **strictly monotone** if it preserves the ternary relation $R$, i.e. if $R_S(x,y,z)$ implies $R_T(f(x),f(y),f(z))$.  This is the cyclic counterpart of a strictly monotone function between linear orders (one which preserves the relation $\lt$).  As in that case, irreflexivity then implies that $f$ is injective as long as $S$ has at least three distinct elements; but in general, this should be stated explicitly (and interpreted in the strongest sense for constructive mathematics).

We say that $f$ is merely **monotone** if it satisfies (either of) the following _equivalent_ conditions:

* $f$ reflects the ternary relation $R$, i.e. if $R_T(f(x),f(y),f(z))$ then $R_S(x,y,z)$.
* $f$ preserves the ternary relation $R$ for elements with pairwise distinct images, i.e. if $R_S(x,y,z)$ holds and $f(x)$, $f(y)$, and $f(z)$ are pairwise distinct, then $R_T(f(x),f(y),f(z))$.

This is the cyclic counterpart of a monotone function between linear orders (one which reflects the relation $\lt$).


## Remarks

* One would like the [[cycle category]] $\Lambda$ to be the category of [[finite set|finite]] [[inhabited set|nonempty]] cyclically ordered sets and monotone functions, just as the [[simplex category]] $\Delta$ is the category of finite nonempty linearly ordered sets and monotone functions.  However, this seems to fail for the $0$-cycle, which has a nontrivial loop and is therefore not [[terminal object|terminal]] (unlike the cyclically ordered [[singleton]], which is terminal).


## Related concepts

* a [[round chord diagram]] is a cyclic order equipped with a pairing of all its elements


[[!redirects cyclic orders]]
[[!redirects cyclic ordering]]
[[!redirects cyclic orderings]]
[[!redirects cyclically ordered]]
[[!redirects cyclically ordered set]]
[[!redirects cyclically ordered sets]]