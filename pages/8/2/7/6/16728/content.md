
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

The **dense topology** is a [[Grothendieck topology]] $J_d$ on a small category $\mathcal{C}$ whose [[sieves]] generalize the idea of a 'downward dense' [[poset]]. The corresponding sheaf topos $Sh(\mathcal{C},J_d)$ yields the [[double negation|double negation subtopos]] of the [[presheaf topos]] on $\mathcal{C}$.

The dense topology is important for sheaf-theoretic approaches to [[forcing|forcing in set theory]]  (cf. [[continuum hypothesis]]).

There is also a closely related but more general concept of a _dense_ [[Lawvere-Tierney topology]] which is discussed at [[dense subtopos]].

## Definition

Let $\mathcal{C}$ be a category. The _dense topology_ $J_d$ is the [[Grothendieck topology]] with collections of [[sieves]] $J_d(Y)$ of the form:

A sieve $S$ is in $J_d(Y)$ iff for all $f:X\to Y$ there exists a $g:Z\to X$ such that $f\circ g:Z\to Y$ is in $S$.

## Properties

Recall that a category $\mathcal{C}$ satisfies the [[Ore condition]] if every diagram $X\rightarrow W\leftarrow Y$ can be completed to a commutative square. In this case the dense topology has a simpler description as the collection of all nonempty sieves and is called the [[atomic site|atomic topology]] $J_{at}$ on $\mathcal{C}$ :

+-- {: .num_prop #atomic_dense}
###### Proposition
Let $\mathcal{C}$ be a [[category]] satisfying the [[Ore condition]]. Then the dense topology $J_d$ coincides with the atomic topology $J_{at}$. 
=--

For the (easy) argument see at [[atomic site]]. One direction relies on the following straight forward

+-- {: .num_prop #atomic_dense}
###### Observation
If $S\in J_d$ then $S\neq \emptyset$ . $\qed$
=--

Note that the coincidence with the atomic topology on categories satisfying the Ore condition affords for the sheaves of $J_d$ the following simple description in such cases:

+-- {: .num_prop #atomic_sheaf}
###### Proposition
Let $(\mathcal{C}, J_{d})$ be a site such that $\mathcal{C}$ satisfies the Ore condition. A presheaf $P\in Set^{\mathcal{C}^{op}}$ is a sheaf for $J_{d}$ iff for any morphism $f:D\to C$ and any $y\in P(D)$ , if $P(g)(y)=P(h)(y)$ for all diagrams
$$
E\overset{g}{\underset{h}{\rightrightarrows}} D\overset{f}{\to} C
$$
with $f\cdot g=f\cdot h$ , then $y=P(f)(x)$ for a unique $x\in P(C)$.
=--

For the proof see Mac Lane-Moerdijk ([1994](#MM94), pp.126f).

+-- {: .num_remark}
###### Remark
It is possible to define the atomic topology $J_{at}$ on arbitrary categories $\mathcal{C}$ as the smallest topology containing all non-empty sieves. Then  observation \ref{atomic_dense} implies that $J_d\subseteq J_{at}$, and accordingly, $Sh(\mathcal{C},J_{at})\subseteq Sh(\mathcal{C},J_d)$ . But $J_d=J_{at}$ precisely if $\mathcal{C}$ satisfies the Ore condition (for details see at [[atomic site]]).
=--

The next result warrants the importance of the dense topology:

+-- {: .num_prop}
###### Proposition
For every small category $\mathcal{C}$, the [[Lawvere-Tierney topology]] on the [[presheaf topos]] $Set^{\mathcal{C}^{op}}$ corresponding to the dense topology on $\mathcal{C}$ is the [[double negation|double negation topology]] $\neg\neg$ on $Set^{\mathcal{C}^{op}}$ . In other words, 
$Sh(\mathcal{C},J_d)\simeq Sh_{\neg\neg}(Set^{\mathcal{C}^{op}})$ .
=--

This appears as ([MacLaneMoerdijk, corollary VI 5](#MacLaneMoerdijk)).

In particular, the [[Lawvere-Tierney topology]] corresponding to the dense topology is [[dense subtopos|dense as a Lawvere-Tierney topology]]!

## Related entries

* [[dense]]

* [[atomic site]]

* [[double negation]]

* [[dense subtopos]]

* [[continuum hypothesis]]

## Reference

* {#MacLaneMoerdijk} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994. (pp.115, 273)