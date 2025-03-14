
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

In [[Riemannian geometry]], the **divergence** of a 
[[vector field]] $X$ over a [[Riemannian manifold]] $(M,g)$ is the real valued [[smooth function]] $div(X)$ defined by

$$
  div(X) 
  \;=\; 
  \star_g^{-1} \mathrm{d} \star_g g(X)
  \,,
$$

where 

* $\star_g$ is the [[Hodge star]] operator of $(M,g)$,

  $$
    \star_g
    \,\colon\, 
    \Omega^i(M;\mathbb{R}) \to \Omega^{dim M-i}(M;\mathbb{R})
    \,,
  $$

* $\mathrm{d}$ is the [[de Rham differential]].

Alternatively, the divergence of a vector field $\vec\mathcal{A}$ in some point $x\in M$ is calculated (or alternatively defined) by the integral formula 

$$
  div \vec\mathcal{A} 
  \;=\; 
  \lim_{vol D\to 0} \frac{1}{vol D} 
  \oint_{\partial D} \vec{n}\cdot \vec\mathcal{A} 
  \mathrm{d} S
$$

where $D$ runs over the [[open subspace|open]] [[submanifolds]] containing point $x$ and with smooth boundary $\partial D$ and $\vec{n}$ is the unit vector of outer normal to the [[hypersurface]] $S$. The formula does not depend on the shape of boundaries taken in limiting process, so one can typically take a [[coordinate chart]] and [[balls]] with decreasing radius in this particular coordinate chart. 

Although an [[orientation]] is required for the usual notion of Hodge star as given above, we may take it as valued in [[pseudoforms]] to show that the orientation (or even orientability) of $M$ is irrelevant (since the Hodge star is applied twice, returning us to untwisted forms, and since a bounding hypersurface has a natural 'outwards' pseudoorientation). However, the metric, which is hidden in the volume form and in the "dot product", is relevant. 


## Example

If $(M,g)$ is the [[Cartesian space]] $\mathbb{R}^n$ endowed with the canonical Euclidean metric, then the divergence of a vector field $X^i \partial_i$ is

$$
div(X) = \sum_{i=1}^n\frac{\partial X^i}{\partial x^i}
.$$


## Remarks

The divergence was first developed in [[quaternion]] analysis, where its opposite appeared most naturally, called the _convergence_ $con(X) = - div(X)$.  In many applications of the divergence to the successor field, classical [[vector analysis]], the metric is irrelevant and we may use [[differential forms]] instead: we translate a vector field $X$ into the $(n-1)$-form $\star_g g(X)$ and a scalar field $f$ into the $n$-form $\star_g f$, so that the divergence *is* simply the [[de Rham differential]], and simply use the differential forms from the start.


## Related concepts

* [[nabla]]

* [[gradient]]

  * [[gradient flow]]

  * [[symplectic gradient]]

* [[Hamiltonian flow]]

* [[curl]]

* **divergence**


[[!redirects divergence]]
[[!redirects divergences]]
