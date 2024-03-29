
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Plump ordinals

* table of contents
{: toc}

## Idea

The [[ordinal numbers]] admit two [[inequalities]]: a strict one $\lt$ and a non-strict one $\le$.  When the ordinals are defined in [[material set theory]] in the von Neumann style as "the set of all smaller ordinals", these relations are identified with $\in$ (set [[membership]]) and $\subseteq$ ([[subset|containment]]).  And when ordinals are defined in a structural theory as certain well-ordered sets, the relation $\le$ refers to inclusion as an [[initial subset]] (a [[simulation]]) while $A\lt B$ refers to such an inclusion as the strict slice $\{ y | y \lt x \}$ of some element $x$ of $B$.

In [[classical mathematics]], $\lt$ and $\le$ are definable in terms of each other's negation: $A\lt B$ if and only if $\neg(B\le A)$, and similarly $A\le B$ if and only if $\neg(B\lt A)$.  However, in [[constructive mathematics]] this is no longer true (although $\leq$ can still be defined from $\lt$ in a more round-about way).  This phenomenon occurs for other ordered structures as well; for instance, for the [[real numbers]].  (For the most commonly used notions of real number, $\le$ is definable as the negation of $\gt$, but not conversely.)   In general, there are certain laws we may expect such a pair of inequalities to satisfy, such as:

* $x\le x$.
* Not $x \lt x$.
* If $x\le y\le z$, then $x\le z$.
* If $x\lt y$, then $x\le y$.
* If $x\lt y\lt z$, then $x\lt z$.
* If $x\lt y\le z$, then $x\lt z$.
* If $x\le y\lt z$, then $x\lt z$.

For the constructive ordinal numbers, these are all satisfied *except for the last one*.  In fact, it's easy to see that if $x\le y\lt z$ implies $x\lt z$ for all $x,y,z$, then [[excluded middle]] holds: consider $z = 2 = \{0,1\}$ and $y = 1 = \{0\}$ and $x = \{0 | P\}$ for some proposition $P$.

However, Paul Taylor [(Taylor)](#Taylor) realized that this last property can be recovered by essentially "restricting to the subclass of ordinals $z$ for which it holds hereditarily".  These are the *plump ordinals*.


## Definition

An [[ordinal]] $A$ is **plump** if

1. every ordinal $B\lt A$ is plump, and
2. whenever $C\le B\lt A$ and $C$ is a plump ordinal, then $C\lt A$.

It is not obvious that this definition is sound (i.e. non-circular), but it can be shown to be so based on a well-founded relation (other than $A$ itself).  It does, however, require the existence of [[power sets]], so it is not obviously sensible in [[predicative mathematics]] which denies the existence of those.


## Examples

$0 = \varnothing$ is trivially plump.

Since $0$ is plump, $1 = \mathcal{P}0 = \{0\}$ is also plump.

More generally, any subset of $1$ (which may be thought of as a [[truth value]]) is a plump ordinal.

But $2 = \{0,1\}$ (the set of classical truth values) with $0 \lt 1$ is plump if and only if excluded middle holds.

In contrast, $\Omega = \mathcal{P}1$ (the set of all truth values) with $0 \lt 1$ (as the only instance of ${\lt}$) is plump.  So $\Omega$ is the plump version of $2$, equal to $2$ iff excluded middle holds.

The plump version of $3$ may be quite large; it consists of all [[lower sets]] (downwards-closed collections) of truth values.  So it includes $0$, $1$, and $\Omega$, the other truth values between $0$ and $1$, the [[downset]] ${\downarrow}p$ (the lower set generated by $p$) of any given truth value $p$ (not just $1 = {\downarrow}0$ and $\Omega = {\downarrow}1$), the lower set generated by two not-necessarily-comparable truth values $p$ and $q$, etc.  But if excluded middle holds, then it\'s just $\{0,1,2\}$.

Generalizing most of these examples, if $\alpha$ is a plump ordinal, then the successor $\alpha^+$, consisting of all lower sets of $\alpha$, is also a plump ordinal.  This is bigger than $\alpha + 1 = \alpha \cup \{\alpha\}$, in that if $0 \lt \alpha$ and $\alpha^+ = \alpha + 1$, then excluded middle holds.

Any downwards-closed subset of a plump ordinal is also a plump ordinal.


## References

* [[Paul Taylor]], *Intuitionistic sets and ordinals*, Journal of Symbolic Logic, 61:705-744, 1996, available [here](http://www.paultaylor.eu/ordinals/#intso)

* See also Section 6.7 of [[Paul Taylor]], *Practical Foundations of Mathematics*, [here](http://www.paultaylor.eu/prafm/html/s67.html).

 {#Taylor}
