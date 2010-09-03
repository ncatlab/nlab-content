
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The formal notion of _curvature_ is a formalization and generalization of the intuitive notion of the ("[extrinsic](Extrinsic)") curvature of a [[surface]] embedded in a [[Cartesian space]] $\mathbb{R}^n$.

This extrinsic curvature of a surface is called [[Gaussian curvature]]. It may also be understood intrinsically as a property of just the surface without reference to the ambient [[Cartesian space]] that it is embedded in: the canonical [[metric]] on $\mathbb{R}^n$ induces a [[Riemannian metric]] on the surface and the surface's curvature is encoded in the [[Levi-Civita connection]] on the [[tangent bundle]] of the surface.

This notion of curvature of a [[Levi-Civita connection]] in turn generalizes straightforwardly to a notion of curvature of any [[connection on a bundle]] and thus gives the name to the general concept. 

For instance in the [[first-order formulation of gravity]] the curvature of [[spacetime]] is literally the curvature of the [[Levi-Civita connection]] on spacetime in this sense. But also the [[Yang-Mills field]] is a connection on a [[principal bundle]] and its curvature encodes the [[field strength]] of the [[Yang-Mills field]], which is a concept rather remote from the intuition of a curved surface (thogh not unrelated).

Even more generally, the notion of a [[connection on a bundle]] and of a [[Lie algebra]]-valued 1-form generalizes to connections on [[principal 2-bundle]]s and [[principal ∞-bundle]]s and [[schreiber:curvature of ∞-Lie algebroid valued differential forms]]. 

In [[generalized (Eilenberg-Steenrod) cohomology|Eilenberg-Steenrod]]-type [[differential cohomology]] describing _abelian_ such higher connections these curvatures appear in the form of generalized [[Chern character]] [[curvature characteristic form]]s. 


## Extrinsic curvature of embedded manifolds {#Extrinsic}

Curvature $\kappa(\gamma)$ of a smooth curve $\gamma$ at a point $p$ of a smooth curve is the (signed) inverse radius of the (oriented) circle having tangency of order 1 with the curve at the point $p$. Every smooth curve in a 3-dimensional space is determined up to isometry by its (parametrised) curvature and torsion. Intuitively, the curvature measures how much curves are bent, when measured in some metrics. Fernet-Serret formulas describe the curvature, torsion and higher analogues for [[naturally parametrized curve]]s in $n$-dimensional Euclidean space. 

For higher dimensional surfaces one can look at normal curvature which is the curvature of the curve which is intersection of a plane determined by the normal vector to the surface and a given tangent vector. For any 2-dimensional tangent plane, the normal curvature has two extreme values. Their product is called the **Gaussian curvature**. 

**Sectional curvature** of a higher dimensional smooth surface at its point $p$ in an Euclidean space along a tangent 2-dimensional plane is the Gaussian curvature of the curve which is the intersection of the surface with the plane. As a plane is determined by two vectors, the sectional curvature is determined by a surface and a pair of vectors, and all possible sectional curvatures can be read form that 2-form; therefore we talk about the operator of the curvature. 

Curvature can be described also intrinsically, without recourse to the ambient space and its metric. Therefore it makes sense in Riemannian geometry based on the [[metric]] tensor just on a manifold. In 1917, Herman Weyl postulated a more fundamental quantity than a [[Riemannian metric]], the [[connection on a bundle|connection]] on a fibre bundle, giving hence rise to a modern, generalized idea of the curvature. While Riemannian metric gives rise to a [[Levi-Civita connection]] on the [[tangent bundle]] of the Riemannian manifold, not every connection on a vector or principal bundles is induced by metrics. In that sense the connection is a more basic notion in geometry. 

## Curvature of a connection

The _curvature_ of a [[connection on a bundle]] measures how the connection is _locally_ non-trivial.

In as far as the notion of connection on a bundle is generalized by the notion of a cocycle in [[differential cohomology]], curvature is essentially the [[Chern character]].

In as far as cocycles in differential cohomology represent [[gauge field]]s in [[physics]], the curvature is the [[field strength]] of these gauge fields.

After the conception of [[gauge theory]], the term _curvature_ was firmly established in its generalization from this special case to the case of connections on all kinds of [[bundle]]s and [[principal infinity-bundle|higher bundles]].


### Curvature of a Lie-algebra valued form


* A connection on a trivial [[line bundle]] on a [[space]] $X$ is just a [[differential forms|1-form]] 

  $$
    A \in \Omega^1(X)
    \,.
  $$ 

  The curvature in this case is the 2-form $F = d A$.

*  A connection on a trivial $G$-[[principal bundle]] for $G$ a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ is a $\mathfrak{g}$-valued 1-form (see [[groupoid of Lie-algebra valued forms]])
 
   $$
     A \in \Omega^1(X) \otimes \mathfrak{g}
     \,.
   $$

   Its curvature is the Lie-algebra valued 2-form

   $$
     F_A = d A + [A \wedge A]
     \,,
   $$

   where $[-,-]$ is the Lie bracket in $\mathfrak{g}$.

* According to the discussion at [[schreiber:differential cohomology in an (∞,1)-topos]], a connection on a trivial [[principal ∞-bundle]] is given by a collection of [[schreiber:∞-Lie algebroid valued differential forms]]. The notion of curvature in this general context is discussed at [[schreiber:curvature of ∞-Lie algebroid valued differential forms]].

### Curvature characteristic forms

* [[curvature characteristic form]]


(TO ADD: Something about curved $A_\infty$ algebras and curved dg algebras.)

[[!redirects curvatures]]

[[!redirects curvature form]]
[[!redirects curvature forms]]

[[!redirects curvature differential form]]
[[!redirects curvature differential forms]]
