

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Topological Yang-Mills theory is a [[gauge theory]] [[topological quantum field theory]] .

## Definition

For $X$ a 3-[[dimensional]] [[smooth manifold]], $\mathfrak{g}$ a [[Lie algebra]] with [[Lie group]] $G$ and $\langle-,-\rangle \in W(\mathfrak{g})$ a binary [[invariant polynomial]] on $\mathfrak{g}$, **topological Yang-Mills theory** is the [[quantum field theory]] defined by the [[action functional]]

$$
  S : G Bund_\nabla(X) \to \mathbb{R}
$$

on the [[groupoid]] of $G$-[[principal bundle]]s with [[connection on a bundle]] that sends a connecton $\nabla$ to the integral of the [[curvature]] 4-form $\langle F_\nabla \wedge F_\nabla \rangle$ of the corresponding [[Chern-Simons circle 3-bundle]]:

$$
  S : \nabla \mapsto \int_X \langle F_A \wedge F_A\rangle
  \,.
$$

## Relaton to other models

The ordinary kinetic term of [[Yang-Mills theory]] differs from this by the fact that the [[Hodge star operator]] appears $\langle F_\nabla \wedge \star F_\nabla \rangle$. In full Yang-Mills theory both terms appear.

The topological Yang-Mills action also appears in the [[generalized Chern-Simons theory]] given by a [[Chern-Simons element]] in a [[Lie 2-algebra]], where it is coupled to [[BF-theory]]. See [[Chern-Simons element]] for details.




