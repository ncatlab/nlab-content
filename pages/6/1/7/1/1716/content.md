
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _numerable open cover_ is an [[open cover]] of a [[topological space]] that admits a subordinate [[partition of unity]]. 



## Definition

Let $\{U_i\}$ be an open [[cover]] of the [[topological space]] $X$ (actually Dold doesn't always require open, see discussion below). It is said to be **numerable** if there is a collection of functions $\phi_i:X \to [0,1]$ such that 

* $\overline{supp(\phi_i)} \subset U_i$,
* at each point $x\in X$, only finitely many of the $\phi_i$ are non-zero,
* $\sum_i \phi_i(x) \equiv 1 \forall x\in X$.

The open cover $\phi_i^{-1}(0,1]$ is then a locally finite cover that refines $\{U_i\}$. The functions $\{\phi_i\}$ are a [[partition of unity]].

Numerable open covers form a [[site]] called the **numerable site**. More precisely, numerable open covers are a [[coverage]] on the category of topological spaces (this is essentially given in Dold's _Lectures on algebraic topology_, A.2.17, but not using this terminology).

Many classical theorems concerning bundles are stated for the numerable site. For example, the [[classifying space]] $\mathcal{B}G$ actually classifies [[bundles]] which trivialise over a numerable cover. (References? Dold for Milnor's classifying space, and tom Dieck I think for Segal's) These are called [[numerable bundles]]. This is because the standard constructions of the universal bundle by Minor and Segal both are trivialisable over a numerable cover.

For paracompact spaces, numerable covers are cofinal in open covers, so that the numerable site is equivalent to the open cover site for such spaces.

There is also some result by Bourbaki that [[David Roberts|I]] have to look up that numerable covers are cofinal in [[locally finite open cover|locally finite covers]] of [[normal spaces]].

## References ##

* A. Dold, _Partitions of unity in the theory of fibrations_, Ann. of Math. (2) 78 1963 223&#8211;255 [MR0155330](http://www.ams.org/mathscinet-getitem?mr=155330) [jstor](http://www.jstor.org/stable/1970341) [doi](http://dx.doi.org/10.2307/1970341)

The appendix of

* A. Dold _Lectures on algebraic topology_

talks about "stacked covers": these are useful for 'decomposing' numerable covers of products to a sort of parameterised version depending on a numerable cover of the first factor. This is important in looking at concordance of numerable bundles.

[[!redirects numerable open covers]]

[[!redirects numerable cover]]
[[!redirects numerable covers]]
