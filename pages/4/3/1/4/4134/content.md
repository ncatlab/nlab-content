
<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The _Liouville cocycle_ is a degree 1 [[cocycle]] in the [[groupoid cohomology]] of the [[action groupoid]] of the [[action]] of conformal rescalings on the space of [[Riemannian metric]]s on a surface.

## Definition

Recall that given a space $X$ with an [[action]] of a [[group]] $G$ on it, a $U(1)$-[[cocycle]] on the [[action groupoid]] $X// G$, i.e. a [[functor]] $X//G \to \mathbf{B} U(1)$, can be explicitly described as a function 
$\lambda: G\times X \to U(1)$ such that 

$$
\lambda(h g,x)=\lambda(h, g x)\lambda(g,x).
$$

Now fix a [[Riemann surface]] $\Sigma$ and take as $X$ the space of [[Riemannian metric]]s on $\Sigma$, and as $G$ the additive group of  [[real line|real]]-valued [[smooth function]]s on $\Sigma$, acting on metrics by conformal rescaling: 

$$
  (f,g_{i j})\mapsto e^f g_{i j}
  \,.
$$

The **Liouville cocycle** is the function

$$
\lambda: C^\infty(\Sigma,\mathbb{R})\times Met(\Sigma) \to U(1)
$$

defined by

$$
\lambda(f,g)=exp(\frac{i}{2} \int_\Sigma(d f\wedge *_g d f +2 f R_g d \mu_g)),
$$

where $*_g$ is the [[Hodge star operator]] defined by the Riemannian metric $g$, $R_g$ is the [[scalar curvarure]] and $d \mu_g$ is the [[volume form]]. 