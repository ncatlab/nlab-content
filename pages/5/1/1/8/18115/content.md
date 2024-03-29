
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

# Contents
* table of contents
{: toc}

## Statement

+-- {: .num_prop}
###### Proposition

Using [[excluded middle]] and [[dependent choice]] then:

Let $(X,d)$ be a [[metric space]] which is [[sequentially compact topological space|sequentially compact]]. Then it is [[totally bounded metric space]].

=--

+-- {: .proof}
###### Proof

Assume that $(X,d)$ were not totally bounded. This would mean that there existed a [[positive number|positive]] [[real number]] $\epsilon \gt 0$ such that for every [[finite set|finite]] [[subset]] $S \subset X$ we had that $X$ is not the [[union]] of the [[open balls]] of [[radius]] $\epsilon$ around the elements of this finite subset
 
$$
  X \neq \underset{s \in S}{\cup} B^\circ_s(\epsilon)
  \,.
$$

This would mean that we could [[induction|inductively]] choose elements

* $x_0 \in X$

* $x_1 \in X\backslash B^\circ_{x_0}(\epsilon)$

* $x_{n+1} \in X \backslash \left( \underoverset{i = 0}{n}{\cup}  B^\circ_{x_i}(\epsilon)\right)$

This constituted a [[sequence]] $(x_i)$, and by assumption of sequential compactness this would have a [[convergence|converging]] sub-sequence. But this would then be a contradiction, since by the above assumption that $X$ is not totally bounded we have $d(x_j, x_k) \gt \epsilon$ for all $j \neq k$. Hence we have a [[proof by contradiction]] that $(X,d)$ in fact is totally bounded.

=--


## Related pages

* [[Lebesgue number lemma]]

* [[sequentially compact metric spaces are equivalently compact metric spaces]]

* [[countably compact metric spaces are equivalently compact metric spaces]]