
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[information geometry]], a _(Fisher-)information metric_ is a [[Riemannian metric]] on a [[manifold]] of [[probability distribution]]s over some probability space $X$ (the latter often assumed to be finite).

## Definition

On a finite probability space $X \in $ [[Set]] a positive [[measure]] is a [[function]] $\rho : X \to \mathbb{R}_+$ and a [[probability distribution]] is one such that $\sum_{x \in X} \rho(x) = 1$.

This space is actually a [[submanifold]] of $\mathbb{R}_{\geq 0}^{\vert X \vert}$. For $\{\frac{\partial}{\partial x^i}\}$ the canonical [[basis]] of [[tangent vector]]s on this wedge of [[Cartesian space]], the information metric $g$ is given by

$$
  g(\frac{\partial}{\partial x^i}, \frac{\partial }{\partial x^j})(\rho) = \frac{1}{\rho(x^i)} \delta_{i j}
  \,.
$$

## Related concepts

* [[Wasserstein metric]]

## References

* L. L. Campbell, _An extended &#268;encov characterization of the information metric_ 
Journal: Proc. Amer. Math. Soc. 98 (1986), 135-141.  ([AMS](http://www.ams.org/journals/proc/1986-098-01/S0002-9939-1986-0848890-5/home.html))

[[!redirects information metrics]]

[[!redirects Fisher information metric]]
[[!redirects Fisher information metrics]]