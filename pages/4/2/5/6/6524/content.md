
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


> For other notions of _[[torsion]]_ see there.

***

#Contents#
* table of contents
{:toc} 

## Definition

A ([[pseudo-Riemannian metric|pseudo]]) [[Riemannian metric]] with metric-compatible [[Levi-Civita connection]] on a [[smooth manifold]] $X$ may be encoded by a [[connection on a bundle|connection]] with values in the [[Poincaré Lie algebra]] $\mathfrak{iso}(p,q)$.

This [[Lie algebra]] is the [[semidirect product]] 

$$
  \mathfrak{iso}(p,q) \simeq \mathfrak{so}(p,q) \ltimes \mathbb{R}^{p+q}
$$

of the [[special orthogonal Lie algebra]] and the abelian translation Lie algebra. Accordingly, a connection 1-form has two components

* $\Omega \in \Omega^1(U,\mathfrak{so}(p,q))$ (sometimes called the "[[spin connection]]");

* $E \in \Omega^1(U,\mathbb{R}^{p+q})$ (sometimes called the "[[vielbein]]").

The metric itself is 

$$
  g = \lanfle E \otimes E \rangle
  \,.
$$

Accordingly also the [[curvature]] 2-form has two components:

* $R = d \Omega + [\Omega \wedge \Omega] \in \Omega^2(U, \mathfrak{so}(p,q))$ -- the [[Riemann curvature]];

* $\tau = d E + [\Omega \wedge E]$ -- the **torsion**.

## Generalizations

In [[supergeometry]] a metric structure is given by a connection with values in the [[super Poincaré Lie algebra]]. The corresponding notion of torsion has an extra contribution from [[spinor]] fields: the [[super torsion]].

## Related concepts

* [[first-order formulation of gravity]]

