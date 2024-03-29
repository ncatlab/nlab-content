
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Riemannian geometry
+-- {: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

Let $(X,g)$ be a [[Riemannian manifold]] and $f \in C^\infty(X)$ a [[function]].

The **gradient** of $f$ is the [[vector field]]

$$
  \nabla f := g^{-1} d_{dR} f \in \Gamma(T X)
  \,,
$$

where $d_{dR} : C^\infty(X) \to \Omega^1(X)$ is the [[de Rham differential]].

This is the unique vector field $\nabla f$ such that 

$$
  d_{dR} f = g(-,\nabla f)
$$

or equivalently, if the manifold is [[oriented]],  this is the unique vector field such that

$$
  d_{dR} f = \star_g \iota_{\nabla f} vol_g
  \,,
$$

where $vol_g$ is the [[volume form]] and $\star_g$ is the [[Hodge star operator]] induced by $g$.  (The result is independent of [[orientation]], which can be made explicit by interpreting both $vol$ and $\star$ as valued in [[pseudoforms]].)

Alternatively, the gradient of a scalar field $A$ in some point $x\in M$ is calculated (or alternatively defined) by the integral formula 

$$
grad A = lim_{vol D\to 0} \frac{1}{vol D} \oint_{\partial D} \vec{n} A d S
$$

where $D$ runs over the domains with smooth boundary $\partial D$ containing point $x$ and $\vec{n}$ is the unit vector of outer normal to the surface $S$. The formula does not depend on the shape of boundaries taken in limiting process, so one can typically take a coordinate chart and balls with decreasing radius in this particular coordinate chart. 


## Example

If $(M,g)$ is the [[Cartesian space]] $\mathbb{R}^n$ endowed with the standard Euclidean metric, then

$$
\nabla f= \sum_{i=1}^n\frac{\partial f}{\partial x^i}\partial_i
.$$

This is the classical gradient from [[vector analysis]].


## Remark

In many classical applications of the gradient in [[vector analysis]], the Riemannian structure is actually irrelevant, and the gradient can be replaced with the [[differential form|differential 1-form]].


## Related concepts

* [[nabla]]

* **gradient**

  * [[gradient flow]]

  * [[symplectic gradient]]

* [[slope of a line]]

* [[Hamiltonian flow]]

* [[curl]]

* [[divergence]]


[[!redirects gradient]]
[[!redirects gradients]]
[[!redirects gradient vector field]]
[[!redirects gradient vector fields]]
