
> This page discusses bases for the topology on [[topological spaces]]. For the concept of topological [[linear basis]] see at _[[basis in functional analysis]]_. For bases on [[sites]], that is for [[Grothendieck topologies]], see at _[[Grothendieck pretopology]]_.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}



## Idea

A _base_ and a _subbase_ for a [[topological space]] are ways of generating its topology from something simpler.  This is the application to topology of the general concept of [[base]].


## Definition {#ForTopologicalSpaces}

Let $X$ be a [[topological space]], and let $\tau$ be its collection of [[open subsets]] (its 'topology').

+-- {: .num_defn}
###### Definition

A __base__ or __basis__ for (or "of") $X$ (or $\tau$) is a [[subset|collection]] $B \subset \tau$ -- whose members are called __basic open subsets__ or __generating open subsets__ -- such that every open subset is a [[union]] of basic ones.
=--

+-- {: .num_defn}
###### Definition

A __subbase__ for (or "of") $X$ (or $\tau$) is a subcollection $S \subset \tau$ -- whose members are called __subbasic open subsets__ -- such that every open subset is a [[union]] of [[finitary intersections]] of subbasic ones.
=--

If only the [[underlying set]] of $X$ is given, then a __base__ or __subbase__ on this [[set]] is any collection of [[subsets]] of $X$ that is a base or subbase for *some* topology on $X$.  See [below](#generation) for a characterisation of which collections these can be.

Now fix a [[point]] $a$ in $X$.

+-- {: .num_defn}
###### Definition

A __local base__ or __base of neighborhoods__ or __fundamental system of neighborhoods__ for (or "of") $X$ (or $\tau$) at $a$ is a subcollection $B \subset \tau$ -- whose members are called __basic neighborhoods__ or __generating neighborhoods__ of $a$ -- such that every basic neighborhood of $a$ is a [[neighborhood]] and every neighborhood of $a$ is a [[superset]] of some basic neighborhood.
=--

We may also allow basic neighborhoods to be non-open, but this really doesn\'t make any difference; any local base may be refined to a local base of open neighborhoods, and most local bases in practices already come that way.

A __local subbase__ at $a$ is a family of neighbourhoods $a$ such that each neighbourhood of $a$ contains a finite [[intersection]] of elements of the family.

+-- {.num_defn}
###### Definition

The minimum [[cardinality]] of a base of $X$ is the __weight__ of $X$.  The minimum cardinality of a base of neighborhoods at $a$ is the __character__ of $X$ at $a$.  The [[supremum]] of the characters at all points of $X$ is the __character__ of $X$.
=--

We have assumed the [[axiom of choice]] to simplify the description of this concept; but in general one must speak of classes of cardinalities rather than individual cardinalities.

If the character of $X$ is [[countable set|countable]], we say that $X$ satisfies the [[first-countable space|first axiom of countability]]; if the weight is countable, we say that $X$ satisfies the [[second-countable space|second axiom of countability]].


## Examples

+-- {: .num_example}
###### Example

For the [[discrete topology]] on a set $X$, the collection of all [[singleton]] subsets is a base, and the singleton $\{x\}$ is a local base at $x$.  Thus every discrete space is first-countable, but only [[countable set|countable]] discrete spaces are second-countable.
=--

+-- {: .num_example}
###### Example

For every [[metric space]], in particular every [[paracompact space|paracompact]] [[Riemannian manifold]], the collection of [[open subsets]] that are [[open balls]] forms a base for the topology.  (For instance, a base for the topology on the [[real line]] is given by the collection of open intervals $(a,b) \subset \mathbb{R}$.)  Similarly, the collection of open balls containing a given point is a local basis at that point.
=--

+-- {: .num_remark}
###### Remark

This means that [[covering]] families consisting of such _basic_ open subsets are [[good open covers]].
=--

+-- {: .num_example}
###### Example

Refining the previous example, every [[metric space]] has a basis consisting of the [[open balls]] with *[[rational number|rational]]* radius.  (For instance, a base for the topology on the [[real line]] is given by the collection of open intervals $(a,b) \subset \mathbb{R}$ where $b - a$ is rational.)  Similarly, the collection of open balls with rational radius containing a given point is a local base at that point.  Therefore, every metric space is first-countable.
=--

+-- {: .num_example}
###### Example

Now consider a [[separable space|separable]] metric space; that is, we have a [[dense subset]] $D$ which is [[countable set|countable]].  Now the space has a basis consisting of the [[open balls]] with [[rational number|rational]] radius and centres in $D$.  (For instance, a base for the topology on the [[real line]] is given by the collection of open intervals $(a,b) \subset \mathbb{R}$ where $a$ and $b$ are rational.)  Therefore, every separable metric space is second-countable.
=--

## Properties

### Generating topologies 
 {#generation}

Let $X$ be simply a [[set]].

+-- {: .num_prop #Recognition}
###### Proposition
**(recognition of topological bases)**

A collection $B$ of [[subsets]] of $X$ is a base for *some* topology on $X$ iff these conditions are met:

*  The elements of $B$ cover $X$;
*  For any $U, V \in B$ and any point $x \in U \cap V$ there is a $W \in B$ such that $W \subseteq U \cap V$ and $x \in W$.
=--

These conditions amount to saying that for each $x\in X$, the subcollection of those $U\in B$ such that $x\in U$ is a base for a [[filter]] on $X$ (which is then the [[neighborhood]] filter of $x$) --- in other words, that these subcollections are "colaxly closed" under finite intersections.

+-- {: .num_prop}
###### Proposition

*Every* collection $S$ of subsets of $X$ is a subbase for some topology on $X$.
=--

A subbase naturally generates a base (for the same topology) by [[Moore closure|closing]] it under finitary intersections.  (The resulting base will actually be closed under intersection.)


### Relation to Grothendieck topologies and coverages
 {#ForSites}

If one thinks of the topology on $X$ as being encoded in the standard [[Grothendieck topology]] that it induces on its [[category of open subsets]] $Op(X)$, then a base for the topology induces a _[[coverage]]_ on $Op(X)$, whose covering families are the open covers by basic open subsets, which generates this Grothendieck topology.

This coverage is *not* in general a [[basis for the Grothendieck topology]], because a base for a topological space is in general not closed under [[intersection]] with arbitrary [[open subsets]]; a coverage is only a basis if is stable under [[pullback]] (here, closed under these intersections) and transitive.  Unfortunately the established terminology "basis" in [[topology]] and [[topos theory]] is not quite consistent with the inclusion of topological spaces into topos theory: "basis" in topology corresponds to "coverage" in topos theory, not to "basis" in topos theory.



## Related concepts

* [[neighbourhood base]]

## Literature

* [[Ryszard Engelking]], _General Topology_, PWN; Warszawa 1977; Revised and completed edition in: Sigma series in pure mathematics __6__, Heldermann 1989 [ISBN 388538-006-4](https://www.heldermann.de/SSPM/SSPM06/sspm06.htm)

* Parimal, Proofs (?), Lecture 13: [Basis for a topology](https://ece.iisc.ac.in/~parimal/proofs/lecture-13.pdf


[[!redirects base for a topology]]
[[!redirects basis for a topology]]
[[!redirects bases for a topology]]
[[!redirects bases for topologies]]
[[!redirects base of a topology]]
[[!redirects basis of a topology]]
[[!redirects bases of a topology]]
[[!redirects bases of topologies]]
[[!redirects basis of topology]]

[[!redirects topological basis]]
[[!redirects topological basises]]

[[!redirects base for a topological space]]
[[!redirects basis for a topological space]]
[[!redirects bases for a topological space]]
[[!redirects bases for topological spaces]]
[[!redirects base of a topological space]]
[[!redirects basis of a topological space]]
[[!redirects bases of a topological space]]
[[!redirects bases of topological spaces]]
[[!redirects topological base]]
[[!redirects topological bases]]
[[!redirects base for the topology]]
[[!redirects basis for the topology]]
[[!redirects bases for the topology]]
[[!redirects base of the topology]]
[[!redirects basis of the topology]]
[[!redirects bases of the topology]]
[[!redirects base for its topology]]
[[!redirects basis for its topology]]
[[!redirects bases for its topology]]
[[!redirects base of its topology]]
[[!redirects basis of its topology]]
[[!redirects bases of its topology]]

[[!redirects subbase for a topology]]
[[!redirects subbasis for a topology]]
[[!redirects subbases for a topology]]
[[!redirects subbases for topologies]]
[[!redirects subbase of a topology]]
[[!redirects subbasis of a topology]]
[[!redirects subbases of a topology]]
[[!redirects subbases of topologies]]
[[!redirects subbase for a topological space]]
[[!redirects subbasis for a topological space]]
[[!redirects subbases for a topological space]]
[[!redirects subbases for topological spaces]]
[[!redirects subbase of a topological space]]
[[!redirects subbasis of a topological space]]
[[!redirects subbases of a topological space]]
[[!redirects subbases of topological spaces]]
[[!redirects topological subbase]]
[[!redirects topological subbases]]
[[!redirects subbase for the topology]]
[[!redirects subbasis for the topology]]
[[!redirects subbases for the topology]]
[[!redirects subbase of the topology]]
[[!redirects subbasis of the topology]]
[[!redirects subbases of the topology]]
[[!redirects subbase for its topology]]
[[!redirects subbasis for its topology]]
[[!redirects subbases for its topology]]
[[!redirects subbase of its topology]]
[[!redirects subbasis of its topology]]
[[!redirects subbases of its topology]]

[[!redirects sub-base for a topology]]
[[!redirects sub-basis for a topology]]
[[!redirects sub-bases for a topology]]
[[!redirects sub-bases for topologies]]
[[!redirects sub-base of a topology]]
[[!redirects sub-basis of a topology]]
[[!redirects sub-bases of a topology]]
[[!redirects sub-bases of topologies]]
[[!redirects sub-base for a topological space]]
[[!redirects sub-basis for a topological space]]
[[!redirects sub-bases for a topological space]]
[[!redirects sub-bases for topological spaces]]
[[!redirects sub-base of a topological space]]
[[!redirects sub-basis of a topological space]]
[[!redirects sub-bases of a topological space]]
[[!redirects sub-bases of topological spaces]]
[[!redirects topological sub-base]]
[[!redirects topological sub-bases]]
[[!redirects sub-base for the topology]]
[[!redirects sub-basis for the topology]]
[[!redirects sub-bases for the topology]]
[[!redirects sub-base for its topology]]
[[!redirects sub-basis for its topology]]
[[!redirects sub-bases for its topology]]
[[!redirects sub-base of its topology]]
[[!redirects sub-basis of its topology]]
[[!redirects sub-bases of its topology]]
