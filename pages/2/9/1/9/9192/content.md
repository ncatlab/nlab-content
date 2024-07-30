
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition 

For $(X,e)$ a ([[pseudo-Riemannian manifold|pseudo]]-)[[Riemannian manifold]] with [[smooth manifold]] $X$ and [[vielbein field]] $e$, its **scalar curvature** is the [[smooth function]]

$$
  R(e) \in C^\infty(X, \mathbb{R})
$$

defined to be the [[trace]] of the [[Ricci tensor]] of $e$

$$
  R(e) \coloneqq tr_e Ric(c)
  \,.
$$


## Examples

\begin{example}\label{RicciTensorOfRoundNSphere}
  For $n \in \mathbb{N}_{\gt 0}$ and $r \in \mathbb{R}_{\gt 0}$, the Ricci tensor of the [[round sphere|round]] [[n-sphere|$n$-sphere]] $S^n$ of [[radius]] $r$ satisfies
$$
  Ric(v,v) \;=\; \frac{n-1}{r^2}
$$
for all unit-length [[tangent vectors]] $v \in T S^n$, ${\vert v \vert} = 1$.

Accordingly, the [[scalar curvature]] of the [[round sphere|round]] [[n-sphere|$n$-sphere]] of [[radius]] $r$ is the [[constant function]] with value
$$
  \mathrm{R} \;=\; \frac{n(n-1)}{r^2}
  \,.
$$
\end{example}
(e.g. [Lee 2018, Cor. 11.20](#Lee18))


## Related concepts

* [[scalar]]

* The product of the scalar curvature with the [[volume form]] is the [[Lagrangian]] of the [[theory (physics)]] of [[gravity]]. The corresponding [[action functional]] is the [[Einstein-Hilbert action]].

* [[Lichnerowicz formula]]


## References

Most references listed at *[[Riemannian geometry]]* discuss scalar curvature, for instance

* {#Lee97} [[John M. Lee]], _Riemannian manifolds. An introduction to curvature_, Graduate Texts in Mathematics **176** Springer (1997) &lbrack;ISBN: 0-387-98271-X&rbrack;

  second edition (retitled):

  {#Lee18} [[John M. Lee]], *Introduction to Riemannian Manifolds*, Springer (2018) &lbrack;ISBN:978-3-319-91754-2, [doi:10.1007/978-3-319-91755-9](https://doi.org/10.1007/978-3-319-91755-9)&rbrack;


[[!include curvature in Riemannian geometry -- table]] 

[[!redirects scalar curvatures]]

[[!redirects Riemann scalar curvature]]
[[!redirects Riemann scalar curvatures]]

[[!redirects Riemann scalar]]
[[!redirects Riemann scalars]]

