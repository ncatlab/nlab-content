

#Contents#
* table of contents
{:toc}

## Idea

The _Stokes theorem_ asserts that the [[integral]] of the [[de Rham differential]] of a [[differential form]] over a domain equals the integral of the form itself over the boundary of the domain.

## Statement

Let 

$$
  \Delta_{Diff} : \Delta \to Diff
$$

be the [[cosimplicial object]] of standard $k$-[[simplices]] in [[Diff]]: in degree $k$ this is the standard $k$-[[simplex]] $\Delta^k_{Diff} \subset \mathbb{R}^k$ regarded as a [[smooth manifold]] (with boundary and corners). This may be parameterized as

$$
  \Delta^k = \{ t^1, \cdots, t^k \in \mathbb{R}_{\geq 0} | \sum_i t^i \leq 1\}
  \subset \mathbb{R}^k
  \,.
$$

In this parameterization the coface maps of $\Delta_{Diff}$ are 

$$
  \partial_i : (t^1, \cdots, t^{k-1}) \mapsto
  \left\{
    \array{
       (t^1, \cdots, t^{i-1}, t^{i+1} , \cdots, t^{k-1}) & | i \gt 0
       \\
       (1- \sum_{i=1}^{k-1} t^i, t^1, \cdots, t^{k-1})
    }
  \right.
  \,.
$$

For $X$ any [[smooth manifold]] a **smooth $k$-simplex in $X$** is a [[smooth function]]

$$
  \sigma : \Delta^k \to X
  \,.
$$

The **boundary** of this simplex in $X$ is the the [[chain]] (formal linear combination of smooth $(k-1)$-simplices)

$$
  \partial \sigma = \sum_{i = 0}^k (-1)^i \sigma \circ \partial_i
  \,.
$$


Let $\omega \in \Omega^{k-1}(X)$ be a degree $(k-1)$-[[differential form]] on $X$.

+-- {: .un_theorem}
###### Theorem
**(Stokes theorem)**

The [[integral]] of $\omega$ over the boundary of the simplex equals the integral of its [[de Rham differential]] over the simplex itself

$$
  \int_{\partial \sigma} \omega = \int_\sigma d \omega
  \,.
$$

=--

It follows that for $C$ any $k$-[[chain]] in $X$ and $\partial C$ its boundary $(k-1)$-chain, we have

$$
  \int_{\partial C} \omega = \int_{C} d \omega
  \,.
$$



[[!redirects Stokes' theorem]]
[[!redirects Stokes's theorem]]