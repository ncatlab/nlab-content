
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Definitions

### For topological spaces

For $X$ a [[topological space]], a __[[base]]__ or __basis__ for the topology of $X$ is a collection of [[open subset]]s -- called __basic open subsets__ or __generating open subsets__ -- such that every open subset is a [[union]] of basic ones.

If we think of the topology on $X$ as being encoded in the standard [[Grothendieck topology]] that it induces on its [[category of open subsets]] $Op(X)$, then a base for the topology induces a _[[coverage]]_ on $Op(X)$, whose covering families are the open covers by basic open subsets, which generates this Grothendieck topology.


### For sites / Grothendieck topologies

For $C$ a [[category]] with [[pullback]]s and equipped with a [[Grothendieck topology]], a [[basis for the Grothendieck topology]] is a [[coverage]] that generates this Grothendieck topology and which is stable under pullback and is transitive.


### Warning 

Unfortunately the established terminology "basis" in [[topology]] and [[topos theory]]  is not quite consistent with the inclusion of topological spaces into topos theory:

because the collection of basic open subsets of a base for a topological space $X$ is in general not closed under intersection with open subsets, this [[coverage]] on $Op(X)$ is in general _not_ a [[basis for a Grothendieck topology]] (a [[Grothendieck pretopology]]) on $Op(X)$.

So "basis" in topology corresponds to "[[coverage]]" in topos theory, not to "basis" in topos theory.

On the other hand, some authors avoid the term [[basis for a Grothendieck topology]] and say [[Grothendieck pretopology]] instead.


## Properties

...


## Examples

We list examples for bases of topological spaces. For examples of bases of Grothendieck topologies see [[basis for a Grothendieck topology]] instead.

* For the [[discrete topology]] on a set $X$, the collection of all singleton subsets is a base.

* For every [[metric space]], in particular every [[paracompact space|paracompact]] [[manifold]] the collection of open subsets that are [[open ball]]s forms a base for the topology.

  Notice that this means that [[covering]] families consisting of such basic open subsets are [[good open cover]]s.

  For instance a base for the topology on the [[real line]] is given by the collection of open intervals $(a,b) \subset \mathbb{R}$



[[!redirects base for a topology]]
[[!redirects basis for a topology]]
[[!redirects bases for a topology]]
[[!redirects base for the topology]]
[[!redirects basis for the topology]]
[[!redirects bases for the topology]]

[[!redirects topological base]]
[[!redirects topological basis]]
[[!redirects topological bases]]
