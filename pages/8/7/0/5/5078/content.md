
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .un_defn}
###### Definition


A **posite** (or **(0,1)-site**) is a [[poset]] (or more generally a [[preordered set]]) equipped with a [[Grothendieck topology]] or a [[coverage]].  

=--

(The name is a portmanteau/pun on _[[poset]]_ and _[[site]]_ .)

+-- {: .un_remark}
###### Remark

The definition of coverage simplifies a little in this case: thus we may consider a posite to be simply a poset $P$ equipped with, for each $x\in P$, a collection of covering families $(y_i)_i$ where each $y_i\le x$, such that if $(y_i)$ covers $x$ and $z\le x$, then there is a covering $(w_j)$ of $z$ such that for each $j$ there is an $i$ with $w_j \le y_i$.

=--

## Properties

+-- {: .un_prop}
###### Proposition

The [[topos of sheaves]] on any posite $P$ is a [[localic topos]].  

=--

+-- {: .proof}
###### Proof

We may describe the relevant [[locale]] explicitly as follows: the elements of its [[frame]] (i.e. its "open subsets") are the [[lower subsets]] $F\subseteq P$ of $P$ satisfying the closure property that if $(y_i)$ covers $x$ and each $y_i\in F$, then $x\in F$ also.  

=--

Such an $F$ is sometimes called an **ideal** for the coverage on $P$.



## Examples

* The [[double negation topology]] used in the sheaf-theoretic approach to [[forcing]] is a posite.

  Classical [[set theory|set-theoretic]] [[forcing]] is done exclusively on posites.  One "reason" for this is explained in a paper of Peter Freyd called something like "all topoi are localic, or why permutation models prevail."

* The [[semilattice of commutative subalgebras]] of a [[C-star algebra]] $A$ is a posite (with trivial topology) internal to whose sheaf topos we have a [[constructive Gelfand duality theorem]] for $A$, even if $A$ was externally non-commutative.



[[!redirects posites]]
[[!redirects (0,1)-site]]
[[!redirects (0,1)-sites]]
[[!redirects 0-site]]
[[!redirects 0-sites]]
