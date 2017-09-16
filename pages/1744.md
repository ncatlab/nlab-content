#Idea#

...

#Definition#


For every $k \in \mathbb{N}$ let $\Delta|_k \hookrightarrow \Delta$ be the full [[subcategory]] of the [[simplex category]] $\Delta$ on objects $[n]$  with $0 \leq n \leq k$.

Precomposition with the inclusion induces a functor

$$
 (-)|_k SSet = [\Delta^{op}, Set] \to [\Delta|_k, Set]
$$

from [[simplicial set]]s to $k$-truncated simplicial sets.

This functor has a [[left adjoint]]

$$
  sk_k : [\Delta|_k,Set] \to SSet
$$

called the $k$-**skeleton**

and a [[right adjoint]]

$$
  cosk_k : [\Delta|_k,Set] \to SSet
$$

called the $k$-**coskeleton**.

The $k$-skeleton produces a simplicial set that is freely filled with degenerate simplices above degree $k$.

Usually the same terms and notation are also used for the composite functors $SSet \to SSet$

$$
  sk_k : SSet \to [\Delta|_k, Set] \stackrel{sk_k}{\to} SSet
$$

and

$$
  cosk_k : SSet \to [\Delta|_k, Set] \stackrel{cosk_k}{\to} SSet
  \,.
$$

The $k$-coskeleton of a simplicial set $X$ is given by the formula

$$
  cosk_k X : [n] \mapsto SSet(sk_k \Delta^n, X)
  \,.
$$