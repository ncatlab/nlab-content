
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

## Idea

For general [[topological spaces]] the condition of being [[compact topological space|compact]] neither implies nor is implied by being [[sequentially compact]]. However for [[metric spaces]] the two conditions happen to be equivalent


## Statement

+-- {: .num_prop #sequentiallyCompactMetricSpacesAreEquivCompact}
###### Proposition

Using [[excluded middle]] and [[countable choice]], then:

If $(X,d)$ is a [[metric space]], regarded as a [[topological space]] via its [[metric topology]], then the following are equivalent:

1. $(X,d)$ is a [[compact topological space]].

1. $(X,d)$ is a [[sequentially compact topological space]].

=--

+-- {: .proof}
###### Proof

Assume first that $(X,d)$ is a [[compact topological space]]. Let $(x_k)_{k \in \mathbb{N}}$ be a [[sequence]] in $X$. We need to show that it has a sub-sequence which [[convergence|converges]].

Consider the [[topological closures]] of the sub-sequences that omit the first $n$ elements of the sequence

$$
  F_n
   \;\coloneqq\;
  Cl(\left\{
    x_k \,\vert\, k \geq n
  \right\})
$$

and write

$$
  U_n \coloneqq X \backslash F_n
$$

for their [[open subset|open]] [[complements]].

Assume now that the [[intersection]] of all the $F_n$ were [[empty set|empty]]

$$
  (\star)
  \phantom{AA}
  \underset{n \in \mathbb{N}}{\cap} F_n \;= \; \emptyset
$$

or equivalently that the [[union]] of all the $U_n$ were all of $X$

$$
  \underset{n \in \mathbb{N}}{\cup} U_n
  \;=\;
  X
  \,,
$$

hence that $\{U_n \to X\}_{n \in \mathbb{N}}$ were an [[open cover]]. By the assumption that $X$ is compact, this would imply that there is a [[finite set|finite]] [[subset]] $\{i_1 \lt i_2 \lt  \cdots \lt i_k\} \subset \mathbb{N}$ with

$$
  \begin{aligned}
    X & = U_{i_1} \cup U_{i_2} \cup \cdots \cup U_{i_k}
    \\
    & = U_{i_k}
  \end{aligned}
  \,.
$$

This in turn would mean that $F_{i_k} = \empty$, which contradicts the construction of $F_{i_k}$. Hence we have a [[proof by contradiction]] that assumption $(\ast)$ is wrong, and hence that there must exist an element

$$
  x \in \underset{n \in \mathbb{N}}{\cap} F_n
  \,.
$$

By definition of [[topological closure]] this means that for all $n$ the [[open ball]] $B^\circ_x(1/(n+1))$ around $x$ of [[radius]] $1/(n+1)$ must intersect the $n$th of the above subsequence:

$$
  B^\circ_x(1/(n+1))
  \,\cap\,
  \{x_k \,\vert\, k \geq n \}
  \;\neq\;
  \emptyset
  \,.
$$

Picking one point $(x'_n)$ in the $n$th such intersection for all $n$ hence defines a sub-sequence, which converges to $x$.

This proves that compact implies sequentially compact for metric spaces.

For the converse, assume now that $(X,d)$ is sequentially compact. Let $\{U_i \to X\}_{i \in I}$ be an [[open cover]] of $X$. We need to show that there exists a finite sub-cover.

Now by the [[Lebesgue number lemma]], there exists a positive real number $\delta \gt 0$ such that for each $x \in X$ there is $i_x \in I$ such that $B^\circ_x(\delta) \subset U_{i_x}$.
Moreover, since [[sequentially compact metric spaces are totally bounded]], there exists then  a [[finite set]] $S \subset X$ such that

$$
   X
     \;=\;
   \underset{s \in S}{\cup}
   B^\circ_s(\delta)
   \,.
$$

Therefore $\{U_{i_s} \to X\}_{s \in S}$ is a finite sub-cover as required.

=-- 


## Remarks

+-- {: .num_defn #weakerAssumptions}
###### Remark

In the proof of prop. \ref{sequentiallyCompactMetricSpacesAreEquivCompact} the implication that a compact topological space is sequentially compact requires less of $(X,d)$ than being a metric space. Actually, the proof works for any [[first-countable space]] that is a [[countably compact space]], i. e. any countable open cover admits a finite sub-cover. Hence [[countably compact metric spaces are equivalently compact metric spaces]].

=--

## Related statements

* [[compact spaces equivalently have converging subnets]]

* [[countably compact metric spaces are equivalently compact metric spaces]]

* [[sequentially compact metric spaces are totally bounded]]

* [[Lebesgue number lemma]]

* [[continuous metric space valued function on compact metric space is uniformly continuous]]
