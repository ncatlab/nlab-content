
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

The _Lebesgue number lemma_ makes a statement about properties of [[open covers]] of [[sequentially compact space|sequentially compact]] [[metric spaces]]. It serves as ingredient of the proof that [[sequentially compact metric spaces are equivalently compact metric spaces]].


## Statement

+-- {: .num_prop}
###### Proposition

Assuming [[excluded middle]] and [[countable choice]] then:

If $(X,d)$ is a [[metric space]] which is [[sequentially compact space|sequentially compact]], then for every [[open cover]] $\{U_i \to X\}_{i \in I}$ there exists a [[positive number|positive]] [[real number]] $\delta \in \mathbb{R}$, $\delta \gt 0$, called a _Lebesgue number_ for $X$, such that for every point $x \in X$ there exists an $i \in I$ such that the [[open ball]] around $x$ of [[radius]] $\delta$ is contained in $U_i$:

$$
  \left(
      (X,d) \, \text{sequentially compact}
  \right)
    \;\Rightarrow\;
   \underset{\delta \gt 0}{\exists}  
   \left(
     \underset{x \in X}{\forall}
     \left(
       \underset{i \in I}{\exists}
       \left(
         B^\circ_x(\delta) \subset U_i 
       \right)
     \right)
   \right)
$$

=--

+-- {: .proof}
###### Proof

Assume that the statement were not true. This would mean that for every $n \in \mathbb{N}$ there exists a point $x_n \in X$ such that for all $i \in I$ the open ball $B^\circ_{x_n}(1/(n+1))$ is not contained in $U_i$. These points $(x_n)_{n \in \mathbb{N}}$ would constitute a [[sequence]] and so by assumption on $X$ there would exist a sub-sequence $(x_{n_k})_{k \in \mathbb{N}}$ which converges to some $x_\infty \in X$. Hence then there would be some $i_\infty \in I$ with $x_\infty \in U_{i_\infty}$, and this, since $U_{i_\infty}$ is open, also a positive real number $\epsilon \gt 0$ with $B^\circ_{x_\infty}(\epsilon) \subset U_{i_\infty}$. By convergence of the sub-sequence $(x_{n_k})_k$ we could now choose a $k \in \mathbb{N}$ such that 

$$
  \frac{1}{n_k + 1} \lt \frac{\epsilon}{2}
   \phantom{AAA}
   \text{and}
   \phantom{AAA}
   d(x_{n_k}, x_{\infinity}) \lt \frac{\epsilon}{2}
  \,.
$$


This would imply that 

$$
  B^\circ_{x_{n_k}}(1/n_k)
  \subset 
  B^\circ_{x_\infty}(\epsilon)
  \subset U_\infty
  \,.
$$

This contradicts the assumption that none of the $U_i$ contains the open ball $B^\circ_{x_{n_k}}(1/n_k)$, and hence we have a  [[proof by contradiction]].

=--


## References

Named after [[Henri Lebesgue]].

* Wikipedia, _[Lebesgue's number lemma](https://en.wikipedia.org/wiki/Lebesgue%27s_number_lemma)_


[[!redirects Lebesgue number lemma]]
[[!redirects Lebesgue's number lemma]]
