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
A countably compact space is a [[limit compact space]]. 
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
Equivalently (under classical logic), the assertion is that if a $T_1$ space $X$ is not countably compact, then it is not limit point compact. Indeed, under this hypothesis, there is a countable open cover $U_1, U_2, \ldots$ of $X$ that admits no finite subcover. We put $V_n = U_1 \cup \ldots \cup U_n$ so that $V_1 \subseteq V_2 \subseteq \ldots$; since every point belongs to some $V_n$ but no $V_n$ is all of $X$, we may discard repetitions and assume without loss of generality that all the inclusions 

$$\emptyset = V_0 \subset V_1 \subset V_2 \subset \ldots$$ 

are strict. Thus for each $n \geq 1$ we may pick a point $x_n \in V_n \setminus V_{n-1}$. Observe that if $m \lt n$, then $x_n \notin V_m$. 

Since $X$ is $T_1$ (points are closed), the set $W_m = V_m \cap \neg \{x_1, \ldots, x_{m-1}\}$ is an open neighborhood of $x_m$ that does not contain $x_n$ whenever $m \lt n$, and does not contain $x_n$ for $n \lt m$. Thus every point $x_m$ is open relative to $A = \{x_1, x_2, \ldots\}$, i.e., $A$ is a discrete subspace. 

Finally, any point $x \notin A$ belongs to some $V_n$, and then $V_n \cap \neg \{x_1, \ldots x_n\}$ is an open neighborhood of $x$ that doesn't intersect $A$. Thus $A$ is an infinite closed discrete subspace, meaning that $X$ is not limit point compact. 
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
