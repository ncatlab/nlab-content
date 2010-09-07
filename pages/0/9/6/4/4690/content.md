
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents
* table of contents
{:toc}

## Idea

The _Einstein-Hilbert action_ is the [[action functional]] that defines the dynamics [[gravity]] in [[general relativity]]. It is a canonical invariant of [[pseudo-Riemannian manifold]]s.

## Definition

For $(X,g)$ a [[Riemannian manifold]] or [[pseudo-Riemannian manifold]], its **vaccuum Einstein-Hilbert action** is the number

$$
  (X,g) := \int_X R(g) dvol(g)
  \,,
$$

where

* $R(g) : X\to \mathbb{R}$ is the [[Riemann curvature]] function of the [[metric]] $g$;

* $dvol(g)$  is the [[volume form]] defined by the metric.

If the metric is instead encoded in terms of an [[Poincare group]]-[[connection on a bundle|connection]] $\nabla$ (the [[first-order formulation of gravity]]) then (for $dim X = 4$ and assuming for simplicity that the underlying bundle is trivial) this is equivalently

$$
  (X,\nabla) \mapsto \int_X \langle R \wedge e \wedge e \rangle
  \,,
$$

where now

* $R$ denotes the [[curvature]] 2-form of the [[orthogonal group]]-connection part of $\nabla$;

* $e$ denotes the [[vielbein]], (the translation part of the connection 1-form);

* $\langle -\rangle$ is the [[invriant polynomial]] which in terms of the canonical basis has components $(\epsilon_{a b c d})$.

This extends to an [[action functional]] for gravity coupled to "matter" (which in the context of [[general relativity]] conventionally means every other field, for instance the [[electromagnetic field]]) by simply adding the matter action on a given gravitational background

$$
  (X,g,\phi) \mapsto \int_X (L_{EH}(g) + L_\phi(g)) d vol(g)
  \,.
$$


The [[critical point]]s of the Einstein-Hilbert action define the physically realized [[spacetime]]s. This are [[Einstein's equations]] (the [[Euler-Lagrange equation]]s of this action)

$$
  \delta S_{EH}(g) = 0
  \,.
$$

(...)