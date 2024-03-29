
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


## Statement

+-- {: .num_prop}
###### Proposition

Let $(X,\tau)$ be a [[topological space]], and let $C \subset X$ be a [[closed subset]], regarded as a [[topological subspace]] $(C,\tau_{sub})$. Then a subset $S \subset C$ is a [[closed subset]] of $(C,\tau_{sub})$ precisely if it is closed as a subset of $(X,\tau)$.

=--

+-- {: .proof}
###### Proof

If $S \subset C$ is closed in $(C,\tau_{sub})$ this means equivalently that there is an open open subset $V \subset C$ in $(C, \tau_{sub})$ such that 

$$
  S = C \backslash V
  \,.
$$

But by the definition of the subspace topology, this means equivalently that there is a subset $U \subset X$ which is open in $(X,\tau)$ such that $V = U \cap C$. Hence the above is equivalent to the existence of an open subset $U \subset X$ such that

$$
  \begin{aligned}
    S & = C \backslash V 
    \\
    & = C \backslash (U \cap C) 
    \\
    & = C \backslash U
  \end{aligned}
  \,.
$$

But now the condition that $C$ itself is a closed subset of $(X,\tau)$ means equivalently that there is an open subset $W \subset X$ with $C = X \backslash W$. Hence the above is equivalent to the existence of two open subsets $W,U \subset X$ such that

$$
  S = (X \backslash W) \backslash U
   = 
   X \backslash (W \cup U)
  \,.
$$

Since the union $W \cup U$ is again open, this implies that $S$ is closed in $(X,\tau)$. 

Conversely, that $S \subset X$ is closed in $(X,\tau)$ means that there exists an open $T \subset X$ with  $S = X \backslash T \subset X$. This means that  $S = S \cap C = (X \backslash T) \cap C = C\backslash T = C \backslash (T \cap C)$, and since $T \cap C$ is open in $(C,\tau_{sub})$ by definition of the subspace topology, this means that $S \subset C$ is closed in $(C, \tau_{sub})$.

=--

## Related statements

* [[closed subsets of compact spaces are compact]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]
