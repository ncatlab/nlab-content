[[!redirects limit compact space]]

# Contents 
* table of contents 
{:toc}

## Definitions 

A [[topological space]] is *limit point compact* if every [[infinite set|infinite]] [[subset]] has a [[limit point]] (in the sense of Definition 2.3 there, i.e., an accumulation point). 

Under [[classical logic]], there are several tautologously equivalent ways of formulating the definition. Let us first recall that points $x$ of a [[closed subset]] $A$ of a space $X$ are either *isolated* (meaning that for some neighborhood $U$ of $x$ we have $U \cap A = \{x\}$) or not; in the latter case we say $x$ is a *limit point* or *accumulation point* of $A$. More generally, for any subset $A$, a limit point of $A$ is defined to be a limit point of its closure $\bar{A}$. 

Thus, a subset $A$ has no limit point iff every point of $\bar{A}$ is isolated, in other words iff $\bar{A}$ equipped with the [[subspace topology]] is a [[discrete space]]. In view of this, an equivalent definition of limit point compactness is: 

* Every closed discrete subspace is [[finite set|finite]]. 

Another characterization focuses in on [[countable set|countability]]: if there are no infinite closed discrete spaces, then obviously there are no countably infinite closed discrete spaces. Conversely, if there is an infinite closed discrete subspace $A$ of $X$, then because any countably infinite subset of $A$ is also closed and discrete in $X$, we can say that $X$ is *not* limit point compact iff there exists an infinite closed discrete subspace iff there exists a countably infinite closed discrete subspace. It follows that another characterization of limit point compactness is 

* Every countably infinite set has a limit point, or

* Every countable closed discrete subspace is finite. 

Limit point compactness is closely related to [[countably compact space|countable compactness]]. Indeed, every countably compact space is limit point compact; in the converse direction, every limit point compact space satisfying the $T_1$ [[separation axiom]] (namely, that points are closed) is also countably compact. For this reason, limit point compact spaces are also known as "weakly countably compact spaces". See [[countably compact space]] for further details. 

+-- {: .num_remark} 
###### Remark 
For a [[metrizable space]] $X$, the following are equivalent: 

* $X$ is a limit point compact space
* $X$ is a [[countably compact space]] 
* $X$ is a [[sequentially compact space]] 
* $X$ is a [[compact space]]
=-- 

## Terminology 

The term "limit point compact" was invented by James Munkres as he was writing his famous text on [[point-set topology]]. He writes that other terms that have appeared in the literature are "Bolzano-Weierstrass compactness" and "Fr&eacute;chet compactness". 

## References 

* [[James Munkres]], *Topology*, 2nd edition, Prentice-Hall 1999. ISBN 0-13-181629-2.