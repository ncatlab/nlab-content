# Normal spaces
* table of contents
{: toc}

## Idea

A normal space is a space (typically a [[topological space]]) which satsifies one of the stronger [[separation axioms]].


## Definitions

A [[topological space]] $X$ is __normal__ if it satisfies:

*  $T_4$: for every two [[closed subspace|closed]] [[disjoint subsets]] $A,B \subset X$ there are (optionally [[open subspace|open]]) [[neighborhoods]] $U \supset A$, $V \supset B$ such that $U \cap V$ is [[empty set|empty]].

Often one adds the requirement

*  $T_1$: every [[point]] in $X$ is closed.

(Unlike with [[regular spaces]], $T_0$ is not sufficient here.)

One may also see terminology where a __normal space__ is any space that satsifies $T_4$, while a __$T_4$ space__ must satisfy both.  This has the benefit that a $T_4$-space is always also a $T_3$-space while still having a term available for the weaker notion.  On the other hand, the reverse might make more sense, since you would expect any space that satisfies $T_4$ to be a $T_4$-space; this convention is also seen.

If instead of $T_1$, you add only

*  $R_0$: if $x$ is in the closure of $\{y\}$, then $y$ is in the [[topological closure|closure]] of $\{x\}$,

then the result may be called an __$R_3$-space__.

Any space that satisfies both $T_4$ and $T_1$ must be [[Hausdorff space|Hausdorff]], and every Hausdorff space satisfies $T_1$, so one may call such a space a __normal Hausdorff space__; this terminology should be clear to any reader.

Any space that satisfies both $T_4$ and $R_0$ must be [[regular space|regular]] (in the weaker sense of that term), and every regular space satisfies $R_0$, so one may call such a space a __normal regular space__; however, those who interpret 'normal' to include $T_1$ usually also interpret 'regular' to include $T_1$, so this term can be ambiguous.

It can be useful to rephrase $T_4$ in terms of open sets instead of closed:

*  $T_4$: if $G,H \subset X$ are [[open subspace|open]] and $G \cup H = X$, then there exist open sets $U,V$ such that $U \cup G$ and $V \cup H$ are still $X$ but $U \cap V$ is empty.

This definition is suitable for generalisation to [[locales]] and also for use in [[constructive mathematics]] (where it is not equivalent to the usual one).

To spell out the localic case, a __normal locale__ is a [[frame]] $L$ such that

*  $T_4$: if $G,H \in L$ are opens and $G \vee H = \top$, then there exist opens $U,V$ such that $U \vee G$ and $V \vee H$ are still $\top$ but $U \wedge V = \bot$.


## Remarks

The class of normal spaces was introduced by Tietze (1923) and Aleksandrov--Uryson (1924). 

Every [[metric space]] is normal Hausdorff. Every normal Hausdorff space is an [[Urysohn space]], a fortiori regular and a fortiori Hausdorff.

Every regular [[second countable space]] is normal. Every [[paracompact space|paracompact]] Hausdorff space is normal (Dieudonn&#233;'s theorem).

The [[Tietze extension theorem]] applies to normal spaces.


## References

* Ryszard Engelking, __General topology__, (Monographie Matematyczne, tom 60) Warszawa 1977; expanded Russian edition Mir 1986.


[[!redirects normal space]]
[[!redirects normal spaces]]
[[!redirects Normal space]]
[[!redirects Normal spaces]]

[[!redirects T4 space]]
[[!redirects T4 spaces]]
[[!redirects T4-space]]
[[!redirects T4-spaces]]
[[!redirects T-4 space]]
[[!redirects T-4 spaces]]
[[!redirects T-4-space]]
[[!redirects T-4-spaces]]

[[!redirects normal Hausdorff space]]
[[!redirects normal Hausdorff spaces]]

[[!redirects R3 space]]
[[!redirects R3 spaces]]
[[!redirects R3-space]]
[[!redirects R3-spaces]]
[[!redirects R-3 space]]
[[!redirects R-3 spaces]]
[[!redirects R-3-space]]
[[!redirects R-3-spaces]]

[[!redirects normal regular space]]
[[!redirects normal regular spaces]]

[[!redirects normal topological space]]
[[!redirects normal topological spaces]]

[[!redirects normal locale]]
[[!redirects normal locales]]
