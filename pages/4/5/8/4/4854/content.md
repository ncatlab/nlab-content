

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Gravity
+-- {: .hide}
[[!include gravity contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Minkowski metric_ is a [[pseudo-Riemannian metric]] which is completely _flat_ in that its [[Riemann curvature]] vanishes.

For $p \in \mathbb{N}$, a [[Cartesian space]] $\mathbb{R}^p+1$ equipped with the Minkowski metric $\eta$ is called _[[Minkowski spacetime]]_ of [[dimension]] $p + 1$, denoted $\mathbb{R}^{p,1} \coloneqq (\mathbb{R}^{p+1}, \eta)$.

## Definition

In terms of the standard [[coordinates]] $(x^\mu)_{\mu = 0}^p$ on $\mathbb{R}^{p+1}$ the Minkowski metric is the [[invariant differential form|constant]] rank 2-[[tensor]] which is given by the [[diagonal matrix]] $\eta = diag(-1,+1,+1, \cdots , +1)$ (or else $\eta = diag(+1,-1,-1, \cdots, -1)$).

This means that for $v = (v^\mu)_{\mu = 0}^p \in \mathbb{R}^{p,1}$ then 

$$
  \eta(v_1, v_2)
    \;=\;
  \eta_{\mu \nu} v_1^\mu v_2 \mu
  \coloneqq
  - (v^0)^2 + \underoverset{j = 1}{p}{\sum} (v^j)^2
  \,.
$$
 

## Properties

### In terms of hermitian matrices.

In the dimensions $p+1 \in \{3,4,6,10\}$ the [[quadratic form]] corresponding to the Minkowski metric may be identified simply with the [[determinant]] function on $2 \times 2$ [[hermitian matrices]] with [[coefficients]] in one of the four [[real numbers|real]] [[normed division algebra]] $\mathbb{K} \in \{\mathbb{R}, \mathbb{C}, \mathbb{H}, \mathbb{O}\}$.

For details see at _[[geometry of physics -- A first idea of quantum field theory]]_ the chapter _[spacetime](geometry+of+physics+--+A+first+idea+of+quantum+field+theory#Spacetime)_.

## Related concepts

* [[super-Minkowski spacetime]]

[[!redirects Minkowski metrics]]

[[!redirects Lorentz metric]]
[[!redirects Lorentz metrics]]