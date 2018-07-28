[[!redirects countably compact space]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

A [[topological space]] is called _countably compact_ if every [[open cover]] consisting of a [[countable set]] of [[open subsets]] (every [[countable cover]]) admits a [[finite cover|finite subcover]], hence if there is a [[finite set|finite]] [[subset]] of the open in the original cover which still cover the space.

## Examples

* A [[compact space]] is _a fortiori_ countably compact. 

* A [[sequentially compact space]] is countably compact. 

* The [[long line]] is an example of a countably compact space that is not compact. 

## Properties 

+-- {: .num_prop} 
###### Proposition 
A countably compact space is a [[limit point compact space]]. 
=-- 

+-- {: .proof} 
###### Proof 
Recall that a space is limit point compact if every [[closed subspace|closed]] [[discrete space|discrete]] [[subspace]] is [[finite set|finite]]; equivalently, if every [[countable set|countable]] closed discrete subspace is finite. 

Suppose $X$ is countably compact and $A$ is a countable closed discrete subspace. For each $a \in A$, choose an open neighborhood $U_a$ such that $U_a \cap A = \{a\}$, and let $V_a$ be the open subset $U_a \cup \neg A$. Clearly we still have $V_a \cap A = \{a\}$. Also, $\{V_a: a \in A\}$ is a countable cover of $X$, hence admits a finite subcover $V_{a_1}, \ldots, V_{a_n}$. But then 

$$A = \left(\bigcup_{i=1}^n V_{a_i} \right) \cap A = \bigcup_{i=1}^n (V_{a_i} \cap A) = \{a_1, \ldots, a_n\}$$ 

as was to be shown.  
=-- 

+-- {: .num_prop} 
###### Proposition 
A space that is $T_1$ and limit point compact is countably compact. 
=-- 

+-- {: .proof} 
###### Proof 
Consider any countable open cover $U_1, U_2, \ldots$ of $X$. Put $V_n = U_1 \cup \ldots \cup U_n$ so that $V_1 \subseteq V_2 \subseteq \ldots$, and discard repetitions, i.e., consider the maximal chain of *strict* inclusions 

$$\emptyset = V_0 \subset V_{n_1} \subset V_{n_2} \subset \ldots$$ 

It suffices to show this maximal chain is finite. Rename it as $\emptyset = W_0 \subset W_1 \subset W_2 \subset \ldots$. 

For each $W_n$ occurring in this chain ($n \geq 1$), pick a point $x_n \in W_n \setminus W_{n-1}$. Observe that if $m \lt n$, then $x_n \notin W_m$. 

Since $X$ is $T_1$ (points are closed), the set $W_m \cap \neg \{x_1, \ldots, x_{m-1}\}$ is an open neighborhood of $x_m$ that does not contain $x_n$ whenever $n \gt m$, and does not contain $x_n$ whenever $n \lt m$. Thus every point $x_m$ is open relative to $A = \{x_1, x_2, \ldots\}$, i.e., $A$ is a discrete subspace. 

Finally, any point $x \notin A$ belongs to some $W_n$, and then $W_n \cap \neg \{x_1, \ldots x_n\}$ is an open neighborhood of $x$ that doesn't intersect $A$. Thus $A$ is a closed discrete subspace, and is finite by limit point compactness. Therefore the maximal chain consisting of the sets $W_n$ is finite, as was to be shown. 
=-- 


* In the case of metric spaces, [[countably compact metric spaces are equivalently compact metric spaces]]. 


## Related concepts

* [[countably paracompact topological space]]

* [[compact topological space]]

* [[countably compact topological space]]

* [[sequentially compact topological space]]

* [[paracompact topological space]]

* [[strongly compact topological space]]

[[!redirects countably compact spaces]]