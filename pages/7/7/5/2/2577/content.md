Let $A$ be an $E_\infty$-ring and let $M$ be an $A$-module.  $M$ is **flat** if 

1. $\pi_0 M$ is a [[flat morphism|flat module]] over $\pi_0 A$ in the classical sense (i.e. $\otimes_{\pi_0 A} M$ is an exact functor);

1. For each $n$, the induced map
$$
\pi_n A \otimes_{\pi_0 A} \pi_0 M \to \pi_n M
$$
is an isomorphism.

A map $A \to B$ of $E_\infty$-rings is **flat** if $B$ is flat when regarded as an $A$-module. 

The same definitions work for some other contexts of derived local algebra, e.g. dg-algebras. 

A morphism $X \to Y$ of [[derived scheme]]s is **flat** if for all affine subsets $U \subset X$ and $ f(U) = V \subset Y$ the induced map on global sections $\Gamma (V) \to \Gamma (U)$ is flat as a map of $E_\infty$-rings.