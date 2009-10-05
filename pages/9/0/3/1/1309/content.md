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

+--{: .query}
[[Mike Shulman|Mike]] and [[Toby Bartels|Toby]]:  If anyone wants to have a go at a cyclic analogue of a total order, be our guest.
=--

As with a linear order, not all of these axioms are needed.  In particular, using [[excluded middle]], it\'s enough if a cyclic relation is transitive and satisfies

*  Cyclic trichotomy:  For all $x, y, z$, ($x = y$ or $x = z$ or $y = z$) xor $R(x,y,z)$ xor $R(x,z,y)$.


## Monotone functions #

An [[injection|injective]] function $f:S\to T$ between cyclically ordered sets is **strictly monotone** if it preserves the ternary relation $R$, i.e. if $R_S(x,y,z)$ implies $R_T(f(x),f(y),f(z))$.  This is the cyclic counterpart of a strictly monotone function between linear orders (one which preserves the relation $\lt$).  As in that case, irreflexivity then implies that $f$ is injective as long as $S$ has at least three distinct elements; but in general, this should be stated explicitly (and interpreted in the strongest sense for constructive mathematics).

We say that $f$ is merely **monotone** if it satisfies (either of) the following _equivalent_ conditions:
* $f$ reflects the ternary relation $R$, i.e. if $R_T(f(x),f(y),f(z))$ then $R_S(x,y,z)$.
* $f$ preserves the ternary relation $R$ for elements with pairwise distinct images, i.e. if $R_S(x,y,z)$ holds and $f(x)$, $f(y)$, and $f(z)$ are pairwise distinct, then $R_T(f(x),f(y),f(z))$.

This is the cyclic counterpart of a monotone function between linear orders (one which reflects the relation $\lt$).

+--{: .query}
[[Mike Shulman|Mike]]: I just made this up, but it seems right.  With a $\le$-version of cyclic orders we could maybe recover monotone functions more directly.  Whatever the definition of monotone function is, it should let us recover $\Lambda$ as below.

_Toby_:  Doubting a $\le$ version and believing that reflecting linear orders is quite natural, I\'ve phrased this entirely in those terms.  Also, fixed (in my opinion) the definition of strict monotone function.  (It\'s interesting that this suggests that $\Delta$ should be seen as a category of linearly ordered sets; being finite sets, this is equivalent even constructively.)
=--


## Remarks #

* The [[cycle category]] $\Lambda$ is the category of [[finite set|finite]] [[inhabited set|nonempty]] cyclically ordered sets and monotone functions, just as the [[simplex category]] $\Delta$ is the category of finite nonempty linearly ordered sets and monotone functions.

+-- {: .query}
[[Todd Trimble|Todd]]: Guys, I may be confused here, but I'm having a problem: it seems that the empty relation on the 1-element set 1 is a cyclic order (in fact the only one on 1), and therefore (under the definition that monotone functions are those which reflect the cyclic order) that 1 is terminal. But then the category of finite (nonempty) cyclically ordered sets and monotone sets would have to be contractible. How does this square with the homotopy type of Connes' cyclic category (which I'm told is the same as that of $S^1$)? 

This is the point that I stumbled on in the blog discussion on the cyclic category almost exactly two years ago, when I attempted to give my own description of $\Lambda$ (but using a cyclic analogue of total orders, which you two have challenged readers to give). You can see my attempted description [here](http://golem.ph.utexas.edu/category/2007/06/the_curious_incident_of_the_do.html#c010503), and my retraction [here](http://golem.ph.utexas.edu/category/2007/06/the_curious_incident_of_the_do.html#c010511). 

_Toby_:  The problem is that the $0$-cycle (unlike the $[0]$-simplex) should not be a point but instead have a nontrivial loop, is that right?  And so it\'s not terminal, since a map to it from $[n]$ really consists of $n + 1$ binary choices (whether to be a degeneracy or to map to the nontrivial loop).

_Todd_: I'm sorry -- I must be making some embarrassingly stupid mistake -- but I still don't follow. What loop? For the 1-element set {t}, there are only two ternary relations. The relation consisting of the point (t, t, t) cannot be a cyclic order by irreflexivity. So the only cyclic order is the empty one (which seems to be vacuously allowed by the axioms). And it seems that the condition that the unique map f: C --> {t} is monotone [by Mike's definition], for any cyclically ordered set C, is vacuously satisfied. 

Trust me -- I want you guys to be right, because I think that the definition of $\Lambda$ I attempted two years ago is (in classical logic) equivalent to yours (although I should check that carefully) -- and I was disappointed when I thought it failed. 

_Toby_:  It\'s also possible that I\'m making an embarrassingly stupid mistake, but if you\'re making one, then it\'s probably missing my word 'should'.  I agree with you that there is a unique cyclic order (as defined here) on the $1$-element set and that this gives the terminal cyclically ordered set.  What I\'m not certain about is that I understand what the cycle category is supposed to be, but is it right that the $1$-element cycle (the $0$-cycle) *should* have a nontrivial loop?  Because if so, then I understand what your objection is!

_Todd_: Part of the problem is that I don't have a deep feeling myself for Connes' $\Lambda$. But David Ben-Zvi (I believe) mentioned on the blog that $\Lambda$ has the homotopy type of a circle, meaning I guess that the classifying space of the nerve $B N \Lambda$ has this homotopy type. But the classifying space of a category with a terminal object is contractible. That's the point where I got worried about my own construction, and it's a worry for me here as well: terminal objects would seem to be fatal.

_Toby_:  OK, so neither of us understands it well enough to be sure.  Still, if I get the description as an ordered graph, then I see that there is a problem with maps to the $0$-cycle.

The good news is that, looking at your definition of a cyclically reflexive notion of cyclic order, I can no longer imagine why I might have thought that such a thing would not work.  Indeed, applying [[de Morgan duality]] to the axioms above for an irreflexive version, we immediately get a reflexive version that is (classically, and even constructively for finite sets) equivalent to your definition.  (It\'s still true that the irreflexive version is probably better from a constructive perspective, much as is true for linear/total orders, because cyclic totality fails for the reflexive ternary order relation on the unit circle in the located Dedekind complex plane, but that\'s not what was concerning me before, nor is it relevant for finite sets.)

[[Mike Shulman]]: Probably this whole discussion should be taking place at [[cycle category]].

According to [Berger-Moerdijk](http://arxiv.org/abs/0809.3341)'s characterization of the cycle category (Example 2.7), I think the $0$-cycle is not terminal.  They describe it as the "total category" of a certain "crossed $\Delta$-group" which is a presheaf $n\mapsto G_n$ of groups on $\Delta$ with certain extra structure; in this case the relevant presheaf sends each set $[n] = \{0,1,\dots,n\}$ to $C_n$, the cyclic group on $n$ letters.  The total category of a crossed $\Delta$-group has the same objects as $\Delta$, and the morphisms $[m]\to [n]$ are pairs $(\alpha,g)$ where $\alpha:[m]\to [n]$ in $\Delta$ and $g\in G_m$.  Thus, in particular, the morphisms $[m]\to [0]$ in $\Lambda$ can be identified with elements $g\in C_m$, so there is more than one of them.

I think I have just lost whatever geometric intuition I used to think I had for the cycle category.
=--
