
# Cofinality
* table of contents
{: toc}

## Idea

The cofinality of a [[quoset]] (quasi-ordered set) is a measure of the size of the quoset and in particular of the size of its tails.  An important special case is the cofinality of an [[ordinal number]], and there is a related concept of the cofinality of a [[cardinal number]].


## Definitions

We begin with definitions that work even in weak [[foundations of mathematics]].

Given a [[quasi-ordered set]] $Q$, the __cofinality__ of $Q$ is the collection of all [[cardinal numbers]] $\kappa$ such that every [[function]] $f\colon [\kappa] \to Q$ (where $[\kappa]$ is any [[set]] of cardinality $\kappa$) has a (strict) [[upper bound]]: an element $x$ of $Q$ such that, whenever $y$ belongs to the [[image]] of $f$, $y \lt x$.  A priori, this collection $Cf(Q)$ may be a [[proper class]], but it is often a [[set]], indeed always in [[classical mathematics]] (as shown below).  We traditionally write $\kappa \lt cf(Q)$ to mean $\kappa \in Cf(Q)$ (for reasons to be seen below).

The __ordinal cofinality__ of $Q$ is the collection $Ocf(Q)$ of all [[ordinal numbers]] $\alpha$ such that ${|\alpha|} \lt cf(Q)$.  This collection is clearly a [[down-set]] and so may be identified with an ordinal number $\ocf(Q)$, also called the __ordinal cofinality__; so we may write $\alpha \lt ocf(Q)$ in place of $\alpha \in Ocf(Q)$, although traditionally we simply write $\alpha \lt cf(Q)$.

If we start with a collection $C$ of [[cardinal numbers]], the __cardinal cofinality__ of $C$ is the collection $Ccf(C)$ of all cardinal numbers $\kappa$ such that, given any $[\kappa]$-indexed [[family]] $F$ of [[sets]], each of which has cardinality in $C$, the [[disjoint union]] of this family (or equivalently the [[union]] in a [[material set theory]]) also has cardinality in $C$.  Again we write $\kappa \lt ccf(C)$ or even $\kappa \lt cf(C)$ to mean $\kappa \in Ccf(C)$.


## Identifications

Assume the [[axiom of choice]].  Then we may identify and simplify some of the concepts above.

*  As a class of cardinal numbers, $cf(Q)$ is clearly a [[down-set]] (that is closed under [[subsets]]), so it must be the set $\{\kappa \;|\; \kappa \lt cf(Q)\}$ for some cardinal number $cf(Q)$, also called the __cofinality__.  (Note that $cf(Q) \leq {|Q|}$, equivalently ${|Q|} \nless cf(Q)$, since the [[identity function]] $Q \to Q$ has no upper bound, so in particular we are *not* dealing with [[proper classes]].)  In this case, we conclude that there is a function $[cf(Q)] \to Q$ that has no strong upper bound, and that $cf(Q)$ is the smallest cardinal number with this property, which is the usual definition.  Assuming that $Q$ is a [[linear order]], it follows that the [[image]] of some function $[cf(Q)] \to Q$ is [[cofinal subset|cofinal]] in $Q$ (whence the terminology).

*  Using the identification of cardinal numbers with certain [[von Neumann ordinals]], the ordinal cofinality $Ocf(Q)$ or $ocf(Q)$ becomes identified with the classical cofinality $cf(Q)$.  (But note that $Cf(Q)$, the collection of cardinal numbers, is only a subset of $Ocf(Q)$ when we identify cardinals as certain ordinals.)

*  Every cardinal cofinality $Ccf(C)$ is also a down-set of cardinal numbers, hence of the form $\{\kappa \;|\; \kappa \lt ccf(C)\}$ for some cardinal number $ccf(C)$.  Furthermore, if we start with a cardinal number $\lambda$ and define the collection $C_\lambda \coloneqq \{\kappa \;|\; \kappa \lt \lambda\}$ of cardinal numbers, then $cf([\lambda]) = ccf(C_\lambda)$.  If we identify $\lambda$ with a von Neumann ordinal, then we also have $cf([\lambda]) = ocf(\lambda)$, so all notions of cofinality agree.


## Properties

Here is an important theorem on ordinal cofinality, which following our definitions is entirely [[constructive mathematics|constructive]]:
$$ ocf(ocf(Q)) = ocf(Q) .$$
In general, an ordinal number $\alpha$ such that $ocf(\alpha) = \alpha$ is called __regular__, so every ordinal cofinality is regular.  For example, $0$, $1$, and $\omega$ are regular ordinals.

A __[[regular cardinal]]__ may be defined to be a collection of cardinals $C$ such that $Ccf(C) = C$.  Assuming the [[axiom of choice]] and making identifications as above, the regular cardinals and the regular ordinals are the same, except that $2$ is a regular cardinal (but not a regular ordinal).  Also, $\{1\}$ is a regular collection of cardinals that is not a down-set, although every other regular cardinal is (and so can be identified with a cardinal number), classically.

Traditionally, one requires a regular ordinal or cardinal to be [[infinite set|infinite]], and thus classically they are the same with no exceptions.


## Cofinality without choice

Assuming the consistency of the existence
of arbitrarily large [[strongly compact cardinals]],
it is consistent with ZF that
every infinite set is a countable union of sets of smaller cardinality.
See \cite{Gitik}.


## Related concepts

* [[initial functor]], [[final functor]]

## References

* {#Gitik} M. Gitik, _All uncountable cardinals can be singular_, Israel Journal of Mathematics 35:1-2 (1980), 61-88.  [doi](http://dx.doi.org/10.1007/bf02760939).


[[!redirects cofinality]]
[[!redirects cofinalities]]

[[!redirects ordinal cofinality]]
[[!redirects ordinal cofinalities]]

[[!redirects cardinal cofinality]]
[[!redirects cardinal cofinalities]]

[[!redirects confinality]]
