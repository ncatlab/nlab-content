
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

Formally, Ricci curvature $Ric$ is a [[curvature]] [[differential 2-form]] with values in scalars obtained by contraction from the [[Riemann curvature]] of a [[Riemannian manifold]]. Geometrically one may think $Ric(v, w)$ as the first order approximation of the infinitesimal behaviour of the surface spanned by $v$ and $w$. This is made explicit by the following formula for the volume element around some point
$$
 d\mu _{g}=\left[1-{\tfrac {1}{6}}Ric_{jk}x^{j}x^{k}+O\left(|x|^{3}\right)\right]d\mu _{Euclidean}.
$$

A [[spacetime]] with vanishing Ricci curvature is also called _Ricci flat_.

## Harmonic coordinate representation and regularity

By a trick of DeTurck and Kazan (or already Lanczos?) in harmonic coordinates the Ricci tensor can be expressed as
$$
Ric_{lm} = -\frac{1}{2} \sum_{j,k} \partial_j g^{jk}(x) \partial_k g_{lm} + Q_{lm}(g, \nabla g)
$$
where $g^{jk}$ denotes the inverse of the metric tensor and $Q_{lm}$ is a quadratic form in $\nabla g$ with coefficients that are polynomials in the coefficients of $g$. Note that this formula involves only first derivatives of the metric tensor. This representation is especially useful in two ways: First, there are theorems that give bounds on the regularity of the metric tensor in harmonic coordinates under geometric assumptions (Anderson, Anderson and Cheeger, Cheeger and Naber). Second, by theory of partial differential equations one can conclude on regularity bounds for the metric tensor from regularity estimates for the Ricci tensor.

## Related concepts

[[!include curvature in Riemannian geometry -- table]] 


* [[Einstein-Hilbert action]]

* [[Einstein equations of motion]]

* [[Einstein manifold]]



## References

* Wikipedia, _[Ricci curvature](http://en.wikipedia.org/wiki/Ricci_curvature)_
* Anderson, _Convergence  and rigidity of manifolds under Ricci curvature bounds_ , Invent. Math. (1990)
* Anderson und Cheeger, _$C^\alpha$-compactnes for manifolds with Ricci curvature and infectivity radius bounded below_ J. Diff. Geo. (1992)
* Cheeger and Naber, _Lower bounds on Ricci curvature and quantitative behavior of singular sets_ Invent. Math. (2013)

[[!redirects Ricci curvatures]]

[[!redirects Ricci tensor]]
[[!redirects Ricci tensors]]

[[!redirects Ricci flat]]
[[!redirects Ricci flatness]]