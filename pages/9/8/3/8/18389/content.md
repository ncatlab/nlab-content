
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Statement

+-- {: .num_prop}
###### Proposition
**(continuous metric space valued function on compact metric space is uniformly continuous)**

Let $K$ and $Y$ be two [[metric spaces]] regarded as [[topological spaces]] via their [[metric topology]], such that $K$ [[compact topological space|compact]]. 

Then every [[continuous function]] of the form

$$
  K \overset{f}{\longrightarrow} Y
$$

is [[uniformly continuous function|uniformly continuous]].

In particular since [[subspaces]] of metric spaces canonically are metric spaces, it follows that if $X$ is a metric space

=--

+-- {: .proof}
###### Proof

Assume on the contrary that it were not. This would mean that for all $\epsilon \in (0,\infty)$ there would for all $n \in \mathbb{N}$ be points $x_n,y_n \in K$ with $d_K(x_n,y_n) \lt 1/(n+1)$ but $d_Y(f(x_n),f(y_n)) \gt \epsilon$.

Since  in compact metric spaces every [[sequence]] has a [[convergence|converging]] subsequence ([[sequentially compact metric spaces are equivalently compact metric spaces|here]]), it follows that there is a  converging subsequences $(x_{n_k})_{k \in \mathbb{N}}$. Since $d_K(x_{n_k} y_{n_k}) \lt 1/(n+1)$ it follows that also $(y_{n_k})_{k \in \mathbb{N}}$ is a converging subsequence which converges to the same point:

But since continuous functions preserve [[limits of sequences]], it would follow that 

$$
  \underset{k \to \infty}{\lim} f(x_{n_k})
  \;=\;
  \underset{k \to \infty}{\lim} f(y_{n_k})
  \,.
$$ 

This however would contradict the assumption that $d_Y(f(x_k), f(y_k)) \gt \epsilon$. Hence we have a [[proof by contradiction]].

=--

## Related statements

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[sequentially compact metric spaces are equivalently compact metric spaces]]

* [[compact spaces equivalently have converging subnet of every net]]

* [[countably compact metric spaces are equivalently compact metric spaces]]

* [[sequentially compact metric spaces are totally bounded]]

* [[Lebesgue number lemma]]


[[!redirects continuous function on compact space is uniformly continuous]]
