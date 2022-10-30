

#Morava K-theory
* table of contents
{:toc}

## Definition

For each [[prime number|prime integer]] $p$ there exists a sequence of [[generalized homology theories]] (equivalently [[spectra]]) $\{K(n)\}$ indexed by the non-negative integers, with the following properties:

1. $K(0)_\ast(X)=H_\ast(X;\mathbb{Q})$ and $\overline{K(0)}_\ast(X)=0$ when $\overline{H}_\ast(X)$ is all [[torsion]].
1. $K(1)_\ast(X)$ is one of $p-1$ isomorphic summands of mod-$p$ complex [[topological K-theory]]. 
1. $K(0)_\ast(pt.)=\mathbb{Q}$ and for $n\neq 0$, $K(n)_\ast(pt.)=\mathbb{Z}/(p)[v_n,v_n^{-1}]$ where $\vert v_n\vert=2p^n-2$.  This [[ring]] is a graded [[field]] in the sense that every graded [[module]] over it is [[free module|free]].  $K(n)_\ast(X)$ is a module over $K(n)_\ast(pt.)$.
1. There is a [[Künneth isomorphism]]: $K(n)_\ast(X\times Y)\cong K(n)_\ast(X)\otimes_{K(n)_\ast(pt.)}K(n)_\ast(Y).$
1. Let $X$ be a p-local finite [[CW-complex]]. If $\overline{K(n)}_\ast(X)$ vanishes then so does $\overline{K(n-1)}_\ast(X)$.
1. If $X$ as above is not contractible then $\overline{K(n)}_\ast(X)=K(n)_\ast(pt.)\otimes \overline{H}_\ast(X;\mathbb{Z}/(p))$.

## Related concepts

* [[K-theory]], [[topological K-theory]], [[algebraic K-theory]]

## References

* Ravenel, Douglas: _Nilpotence and Periodicity in Stable Homotopy Theory_

