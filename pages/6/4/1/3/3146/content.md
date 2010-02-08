
#Contents#
* automatic table of contents goes here
{:toc}

## Classical curvature

Curvature $\kappa(\gamma)$ of a smooth curve $\gamma$ at a point $p$ of a smooth curve is the (signed) inverse radius of the (oriented) circle having tangency of order 1 with the curve at the point $p$. Every smooth curve in a 3-dimensional space is determined up to isometry by its (parametrised) curvature and torsion. Intuitively, the curvature measures how much curves are bent, when measured in some metrics. Fernet-Serret formulas describe the curvature, torsion and higher analogues for [[naturally parametrized curve]]s in $n$-dimensional Euclidean space. 

For higher dimensional surfaces one can look at normal curvature which is the curvature of the curve which is intersection of a plane determined by the normal vector to the surface and a given tangent vector. For any 2-dimensional tangent plane, the normal curvature has two extreme values. Their product is called the **Gaussian curvature**. 

**Sectional curvature** of a higher dimensional smooth surface at its point $p$ in an Euclidean space along a tangent 2-dimensional plane is the Gaussian curvature of the curve which is the intersection of the surface with the plane. As a plane is determined by two vectors, the sectional curvature is determined by a surface and a pair of vectors, and all possible sectional curvatures can be read form that 2-form; therefore we talk about the operator of the curvature. 

Curvature can be described also intrinsically, without recourse to the ambient space and its metric. Therefore it makes sense in Riemannian geometry based on the metric tensor just on a manifold. In 1917, Herman Weyl postulated a more fundamental quantity then Riemannian metric, the connection on a fibre bundle, giving hence rise to a modern, generalized idea of the curvature. While Riemannian metric gives rise to a [[Levi-Civita connection]] on the [[tangent bundle]] of the Riemannian manifold, not every connection on a vector or principal bundles is induced by metrics. In that sense the connection is a more basic notion in geometry. 

## Modern generalized ideas of curvature

The _curvature_ of a [[connection on a bundle]] measures how the connection is _locally_ non-trivial.

In as far as the notion of connection on a bundle is generalized by the notion of a cocycle in [[differential cohomology]], curvature is essentially the [[Chern character]].

In as far as cocycles in differential cohomology represent [[gauge field]]s in [[physics]], the curvature is the [[field strength]] of these gauge fields.

After the conception of [[gauge theory]], the term _curvature_ was firmly established in its generalization from this special case to the case of connections on all kinds of [[bundle]]s and [[principal infinity-bundle|higher bundles]].


## On trivial bundles

On a trivial bundle (and in particular locally, on every locally trivial bundle) a [[connection on a bundle|connection]] is given by [[differential form]] data. We describe the curvatures of these:

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

* According to the discussion at [[schreiber:theory of differential nonabelian cohomology]], a connection on a trivial [[principal ∞-bundle]] is given by a collection of [[schreiber:∞-Lie algebroid valued differential forms]]. The notion of curvature in this general context is discussed at [[schreiber:curvature of ∞-Lie algebroid valued differential forms]].