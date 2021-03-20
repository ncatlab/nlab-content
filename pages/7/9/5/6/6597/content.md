
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _symplectic gradient_ is the analog in [[symplectic geometry]] of the [[gradient]] in [[Riemannian geometry]].

## Definition

Let $(X,\omega)$ be a [[symplectic manifold]] and $H \in C^\infty(X)$ a [[function]].

The **symplectic gradient** of $H$ is the [[vector field]]

$$
  X_H := \omega^{-1} d_{dR} H \in \Gamma(T X)
  \,,
$$

where $d_{dR} : C^\infty(X) \to \Omega^1(X)$ is the [[de Rham differential]].

This is the unique vector field $X_H$ such that 

$$
  d_{dR} H = \omega(-,X_H)
$$

The function $H$ in this context is called an [[Hamiltonian]] and the vector field $H_X$ an [[Hamiltonian vector field]].

Equivalently, the vector field $X_H$ is defined by the condition

$$
X_H(f)=\{H,f\}
$$
for any $f \in C^\infty(X)$, where $\{\,,\,\}$ is the [[Poisson bracket]] on $(M,\omega)$.


## Examples 

If $(M,g)$ is $\mathbb{R}^{2n}$ endowed with the standard [[symplectic form]] $\omega=dp_i\wedge dq^i$, then

$$
X_f= \sum_{i=1}^n\frac{\partial f}{\partial p_i}\frac{\partial}{\partial q^i}-\frac{\partial f}{\partial q^i}\frac{\partial}{\partial p_i}.
$$

[[!redirects symplectic gradients]]