<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>

#Contents#
* automatic table of contents
{:toc}

## Definition

A $2n$-dimensional topological [[manifold]] $M$ is a real __symplectic manifold__ if it has a symplectic atlas; a symplectic atlas consists of smooth charts $\phi_i:U_i\to M$ as usual, such that the transition functions $\phi_j^{-1}\circ\phi_i:\phi_i^{-1}(\phi_i(U_i)\cap\phi_j(U_j))\to \phi_j^{-1}(\phi_i(U_i)\cap\phi_j(U_j))$ are preserve the standard symplectic form $\omega_0=\sum_{i=1}^n dx_i\wedge dp_i$ on $\mathbb{R}^{2n}$ with the basis $(x_1,\ldots,x_n,p_1,\ldots,p_n)$.

Equivalently, a __symplectic manifold__ is a differentiable [[manifold]] equipped with a smooth [[differential form|2-form]] $\omega\in \Gamma(\Lambda^2 T^* M)$ which is nondegenerate in the sense that $\omega^{\wedge n}=\omega\wedge\omega\wedge\cdots\wedge\omega$ has the maximal rank at every point $p\in M$, or equivalently such that $(\Lambda^2 T^*_p M,\omega_p)$ is a [[symplectic vector space]] for every point $p\in M$.  We call such $\omega$ a __symplectic form__.


## Higher versions

The [[vertical categorification|categorification]] of the notion of symplectic manifold is [[n-symplectic manifold]].

+-- {: .query}
Shouldn't there be an explanation how a symplectic manifold is a 0-symplectic manifold?

[[Urs Schreiber]]: such an explanation is currently at [[schreiber:symplectic ∞-Lie algebroid]]. Should eventually be merged here into the $n$Lab proper.

=--

[[!redirects symplectic manifolds]]
[[!redirects symplectic form]]

[[!redirects symplectic structure]]