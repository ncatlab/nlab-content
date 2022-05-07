
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

## Definition

+-- {: .num_defn }
###### Definition

The __Sierpi&#324;ski space__ $\Sigma$ is the [[topological space]] 

1. whose underlying set has two elements, say $\{0,1\}$,

1. whose set of [[open subsets]] is $\left\{ \emptyset, \{1\}, \{0,1\}  \right\}$.

(We could exchange "0" and "1" here, the result would of course be [[homeomorphism|homeomorphic]]).

Equivalently we may think of the underlying [[set]] as the set of of [[classical mathematics|classical]] [[truth values]]  $\{\bot, \top\}$, equipped with the [[specialization topology]], in which $\{\bot\}$ is [[closed subset|closed]] and $\{\top\}$ is an [[open subset|open]] but not conversely.  

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

* has a [[focal point]];

* is a [[sober topological space]] (but not [[separation axiom|T1]]).

According properties are inherited by the [[Sierpinski topos]] and the [[Sierpinski (∞,1)-topos]] over $Sierp$.


### As a classifer for open/closed subspaces

The Sierpinski space $S$ is a classifier for [[open subspaces]] of a [[topological space]] $X$ in that for any open subspace $A$ of $X$ there is a unique [[continuous function]] $\chi_A: X \to S$ such that $A = \chi_A^{-1}(\top)$.  

Dually, it classifies [[closed subsets]] in that any closed subspace $A$ is $\chi_A^{-1}(\bot)$.  Note that the closed subsets and open subsets of $X$ are related by a [[bijection]] through [[complement|complementation]]; one gets a topology on the set of either by identifying the set with $\Top(X,\Sigma)$ for a suitable [[function space]] topology.  (This part does not work as well in [[constructive mathematics]].)


## Related concepts

* [[empty space]], [[point space]]

* [[Cantor space]]

* [[Sierpinski topos]], [[Sierpinski (∞,1)-topos]]

* [[Stone duality]]

* [[separation axioms in terms of lifting properties]]

* In [[synthetic topology]], an analogue of the Sierpinski space is called a [[dominance]].


## References

* Wikipedia, _[Sierpinski space](https://en.wikipedia.org/wiki/Sierpi%C5%84ski_space)_

* [[Paul Taylor]],  _Foundations for computable topology -- 7 The Sierpinski space_ ([html](http://www.paultaylor.eu/ASD/foufct/sierpinski.html))


[[!redirects Sierpinski space]]
[[!redirects Sierpi?ski space]]
[[!redirects Sierpinski topology]]
[[!redirects Sierpi?ski topology]]
