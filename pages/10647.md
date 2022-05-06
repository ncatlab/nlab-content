
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Formally, Ricci curvature $Ric$ is a [[curvature]] [[differential 2-form]] with values in scalars obtained by contraction from the [[Riemann curvature]] of a [[Riemannian manifold]]. Geometrically one may think $Ric(v, w)$ as the first order approximation of the infinitesimal behavior of the surface spanned by $v$ and $w$. This is made explicit by the following formula for the volume element around some point
$$
 d\mu _{g}=\left[1-{\tfrac {1}{6}}Ric_{jk}x^{j}x^{k}+O\left(|x|^{3}\right)\right]d\mu _{Euclidean}.
$$

A [[spacetime]] with vanishing Ricci curvature is also called _Ricci flat_.

## Harmonic coordinate representation and regularity

By a trick of Lanczos, that was recovered by DeTurck and Kazdan, in harmonic coordinates the Ricci tensor can be expressed as
$$
Ric_{lm} = -\frac{1}{2} \sum_{j,k} g^{jk} \partial_j \partial_k g_{lm} + Q_{lm}(g, \nabla g)
$$
where $g^{jk}$ denotes the inverse of the metric tensor and $Q_{lm}$ is a quadratic form in $\nabla g$ with coefficients that are rational expressions in which numerators are polynomials $g$ and the denominator depends only on $\sqrt{\det g}$. Note that this formula describes the metric tensor as a quasilinear elliptic PDE. This representation is especially useful in two ways: First, there are theorems that give bounds on the regularity of the metric tensor in harmonic coordinates under geometric assumptions (Anderson, Cheeger and Naber). Second, as this expression is a quasilinear elliptic PDE, one can conclude on regularity bounds for the metric tensor from regularity estimates for the Ricci tensor. This argument allows for a regularity bootstrap in case of [[Einstein manifold|Einstein manifolds]]: given a rough Einstein metric with $k$ derivatives, the regularity theory for quasilinear PDEs gives $k+2$-regularity of the metric tensor. But the Einstein property $g = \lambda Ric$ implies the same regularity for the Ricci tensor. Hence one can apply the argument again and add infinitum.

## Related concepts

[[!include curvature in Riemannian geometry -- table]] 


* [[Einstein-Hilbert action]]

* [[Einstein equations of motion]]

* [[Einstein manifold]]



## References

* Wikipedia, _[Ricci curvature](http://en.wikipedia.org/wiki/Ricci_curvature)_

* Lanczos, _Ein vereinfachendes Koordinatensystem für die Einsteinschen Gravitationsgleichungen_ Phys. Z. 23, 537-539 (1922)

* DeTurck and Kazdan, _Some regularity theorems in Riemannian geometry_ Ann. scient. Éc. Norm. Sup. (1981)

For regularity result see

* Anderson, _Convergence  and rigidity of manifolds under Ricci curvature bounds_ , Invent. Math. (1990)
* Cheeger and Naber, _Lower bounds on Ricci curvature and quantitative behavior of singular sets_ Invent. Math. (2013)

For weaker but more general regularity results see also:

* Anderson and Cheeger, _$C^\alpha$-compactness for manifolds with Ricci curvature and injectivity radius bounded below_ J. Diff. Geo. (1992)

[[!redirects Ricci curvatures]]

[[!redirects Ricci tensor]]
[[!redirects Ricci tensors]]

[[!redirects Ricci flat]]
[[!redirects Ricci flatness]]