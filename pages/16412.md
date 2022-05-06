
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context
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

[[Georg Cantor]] used to define the [[continuum]] as a **perfect space** that is [[connected space|connected]] as well.  Hence, the property of 'being perfect', as the name indicates as well, can be viewed as forming part of the concept of a 'prototypical' [[topological space]].


## Definitions

A [[topological space]] $X$ is **perfect** if it has no isolated points, i.e., if every point $x$ belongs to the topological [[closure operator|closure]] of its [[complement]] $X \setminus \{x\}$.  Sometimes one requires a perfect space to be [[inhabited space|inhabited]] (nonempty), although it is better to allow the [[empty space]].

In a topological space $X$, a [[subset]] is said to be __perfect__ if it is [[closed set|closed]] in $X$ and perfect in its [[subspace topology]].  In other words, a set $A$ is perfect if and only if it equals its set $A'$ of [[accumulation points]].  Because of the closure requirement, being a perfect set/subset/subspace depends on the ambient space and is stronger than being a perfect space.  (But $X$ is a perfect subset of itself iff $X$ is a perfect space.)

In a topological space $X$, a subset $A$ has the __perfect-set property__ if it is either [[countable set|countable]] (possibly [[finite set|finite]] or even [[empty subset|empty]]) or has an inhabited perfect subset.  Of course, any perfect set has the perfect-set property.

If for each set $B$, ($B$ has a point apart from each point in $A$ if $B$ is inhabited and $B$ is perfect) and ($B$ is empty if $B$ is contained in $A$ and $B$ is perfect) and ($B$ has an isolated point if $B$ is contained in $A$ and inhabited), then $A$ is countable.


## Examples

* The [[empty space]] is perfect (unless it is excluded by fiat).

* The [[Cantor space]] $2^\mathbb{N}$ is perfect, in fact, it is the only [[totally disconnected space|totally disconnected]], [[compact space|compact]], [[metrizable space|metrizable]] space that is perfect.

* The [[real line]] is perfect.

* Every [[Polish space]] (including the previous two examples) is perfect.  Furthermore, any [[closed subset]] of a Polish space has the perfect-set property.

*  Using the [[axiom of choice]], one may prove the existence of subsets of the real line that do not have the perfect-set property.  In contrast, one of the axioms of [[dream mathematics]] is that every subset of the real line does have this property.  This makes the [[continuum hypothesis]] a theorem of dream mathematics.


## Properties

* Every topological space $X$ is the disjoint union of a [[scattered space|scattered subset]] and a perfect subset.

* Every perfect subset of a [[Polish space]] $X$ (including $X$ itself) has the [[cardinality of the continuum]] ($\beth_1$).  (This is why the continuum hypothesis follows from the non-classical axiom that every subset of the real line has the perfect-set property.)

* Every [[closed subset]] of a [[Polish space]] is a unique [[disjoint union]] of a countable set and a (possibly empty) perfect set.


## Related entries

* [[scattered space]]

* [[limit point]] 

* [[Cantor space]]

* [[Polish space]] 

* [[descriptive set theory]] 


## Reference

* S. Willard, _General Topology_ , Addison-Wesley Reading 1970. (Dover reprint 2004, pp.216ff)


category: foundational axiom

[[!redirects perfect space]]
[[!redirects perfect spaces]]
[[!redirects perfect topological space]]
[[!redirects perfect topological spaces]]

[[!redirects perfect set]]
[[!redirects perfect sets]]
[[!redirects perfect subset]]
[[!redirects perfect subsets]]
[[!redirects perfect subspace]]
[[!redirects perfect subspaces]]

[[!redirects perfect set property]]
[[!redirects perfect-set property]]
