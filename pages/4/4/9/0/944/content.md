
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
* table of contents
{:toc}

## Definition

+-- {: .num_defn }
###### Definition

The __Sierpi&#324;ski space__ $\Sigma$ is the [[topological space]] which is the [[set]] of [[truth value]]s, classically $\{\bot, \top\}$, equipped with the [[specialization topology]], in which $\{\bot\}$ is closed and $\{\top\}$ is open but not conversely.  (The opposite convention is also used.)

=--


+-- {: .num_remark }
###### Remark

In [[constructive mathematics]], it is important that $\{\top\}$ be open (and $\{\bot\}$ closed), rather than the other way around.  Indeed, the general definition (since we can\'t assume that every element is either $\top$ or $\bot$) is that a subset $P$ of $\Sigma$ is open as long as it is upward closed: $p \Rightarrow q$ and $p \in P$ imply that $q \in P$.  The ability to place a topology on $\Top(X,\Sigma)$ is fundamental to [[abstract Stone duality]], a constructive approach to general topology.

=--


## Properties

### As a topological space

This Sierpinski space 

* is a [[contractible space]];

* is a [[locally contractible space]];

* has a [[focal point]].

According properties are inherited by the [[Sierpinski topos]] and the [[Sierpinski (∞,1)-topos]] over $Sierp$.

### As a classifer for closed subspaces

The Sierpinski space is a classifier for [[closed subspaces]] of a [[topological space]] $X$ in that for any closed subspace $A$ of $X$ there is a unique [[continuous function]] $\chi_A: X \to S$ such that $A = \chi_A^{-1}(\bot)$.  

Dually, it classifies [[open subsets]] in that any open subspace $A$ is $\chi_A^{-1}(\top)$.  Note that the closed subsets and open subsets of $X$ are related by a [[bijection]] through [[complement|complementation]]; one gets a topology on the set of either by identifying the set with $\Top(X,\Sigma)$ for a suitable [[function space]] topology.

## Related concepts

* [[Sierpinski topos]], [[Sierpinski (∞,1)-topos]]

* [[Stone duality]]

* In [[synthetic topology]], an analogue of the Sierpinski space is called a [[dominance]].

## References

* [[Paul Taylor]],  _Foundations for computable topology -- 7 The Sierpinski space_ ([html](http://www.paultaylor.eu/ASD/foufct/sierpinski.html))

[[!redirects Sierpi?ski space]]
[[!redirects Sierpinski topology]]
[[!redirects Sierpi?ski topology]]