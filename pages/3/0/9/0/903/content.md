# Idea #

The _homotopy groups_ $\pi_n(X,a)$ of a [[pointed object|pointed]] space $(X,a)$ are a sequence of [[group]]s that generalise the [[fundamental group]] $\pi_1(X,a)$ to higher homotopies.

Actually, $\pi_0(X,a)$ is not a group at all but merely a [[pointed set]].  Conversely, $\pi_2(X,a)$ and above are all [[abelian group]]s.  Only $\pi_1(X,a)$ may be an arbitrary group.

Lower homotopy groups act on higher homotopy groups; the nonabelian group cohomology of this gives the Postnikov invariants of the space.  All of this data put together allows one to reconstruct the original space, at least up to weak [[homotopy type]], through its [[Postnikov tower]].

# History #

In the early years of the 20th century it was known that the nonabelian fundamental group $\pi_1(X,a)$ of a space $X$ with base point $a$ was useful in geometry and complex analysis. It was also known that the abelian [[homology group]]s $H_n(X)$ existed for all $n \geq 0$ and that if $X$ is connected then $H_1(X)$ is isomorphic to the abelianisation of any $\pi_1(X,a)$. 

Consequently it was hoped to generalise the fundamental group to higher dimensions, producing nonabelian groups whose abelianisations would be the homology groups.

In 1932, E. &#268;ech proposed a definition of higher homotopy groups using maps of spheres, but the paper was rejected for the Zurich ICM since it was found that these groups $\pi_n(X,a)$ were abelian for $n \geq 2$, and so do not generalise the fundamental group as desired.

Nonetheless they have proved to be important, although more difficult to compute in general than homology groups.

# Properties #

It was early realised that the fundamental groupoid $\pi_1(X,a)$ operates on the family of groups $\{\pi_n(X,a) | a \in X\}$ which should thus together be regarded as a module over $\pi_1(X,a)$.

A key property of homotopy groups is the _Whitehead theorem_: if $f:X \to Y$ is a map of connected [[m-cofibrant space]]s (spaces each of the homotopy type of a [[CW complex]]), and $f$ induces isomorphisms $\pi_n(X,a) \to \pi_n(Y,f(a))$ for some $a$ and all $n \geq 1$, then $f$ is a [[homotopy equivalence]].

However, the homotopy groups by themselves, even considering the operations of $\pi_1$, do not characterise homotopy types. See also [[algebraic homotopy|algebraic homotopy theory]].

+--{.query}
But the entire Postnikov tower does characterise weak homotopy types, does it not? (Actually, I shouldn\'t really phrase it that way, since the Postnikov tower as such is a sequence of maps that begins with the space in question.  I mean the homotopy groups together with the Postnikov invariants.) ---Toby
=--