
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Riemannian geometry
+-- {: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Cauchy surfaces
* table of contents
{: toc}

## Idea

A Cauchy surface is a [[hypersurface]] in [[spacetime]] (so actually a $3$-dimensional region in our $4$-dimensional spacetime) that can profitably be seen as constituting 'all of space at a given time'.


## Definition

For $(X,g)$ a [[Lorentzian manifold]], a **Cauchy surface** is an [[embedding|embedded]] [[submanifold]] $\Sigma \hookrightarrow X$ such that every [[timelike]] [[curve]] in $X$ may be extended to a timelike curve that intersects $\Sigma$ precisely in one point.

A Lorentzian manifold that does admit a Cauchy surface is called _[[globally hyperbolic]]_. 

## Properties

\begin{proposition}\label{FoliationOfGloballyHyperbolicSpacetimes}
  For $X^D$ a [[smooth manifold|smooth]] [[globally hyperbolic spacetime]], it admits a smooth [[foliation]]  by smooth spacelike Cauchy surfaces $X^d$, exhibited by a [[diffeomorphism]]
$$
  X^D \,\simeq\, \mathbb{R}^{0,1} \times X^d
  \,,
$$
which is [[isometry|isometric]] with respect to a possibly non-product [[pseudo-Riemannian metric]] on the right
\end{proposition}
([Bernal & Sánchez 2005, Thm. 1.1](#BernalSánchez03), following [Geroch 1970](#Geroch70), reviewed in [Sánchez 2022 (3)](#Sánchez22)).

## Applications

One way to formulate [[causality]] in [[physics]] is that the values of all [[observables]] at all points on a single Cauchy surface in [[spacetime]] is enough information (in the sense of a [[boundary condition]] to apply to a [[differential equation]] constituting a relevant physical theory) to determine the values of all observables at all points of spacetime.  (This is not always an actual theorem of differential equations.)  Stated more intuitively, the state of the universe at any given time is enough information to determine the state of the universe at all times.

If [[spacetime]] can be equipped with a [[foliation]] of Cauchy surfaces, then we may assign a [[real number]] $t$ to each surface $\Sigma$, so that we think of $\Sigma$ as 'space at time $t$'.  Of course, there are typically many ways to do this (if any), in accordance with the principle of [[relativity of simultaneity]].  On the other hand, for some spacetimes, this may not be possible at all (because they are not globally hyperbolic).

## Related concepts

* [[Cauchy horizon]]

## References

The existence of a splitting of globally hyperbolic spacetimes into Cauchy surfaces is 

in the topological category due to 

* {#Geroch70} [[Robert Geroch]], §5, Thm. 11 in: *Domain of Dependence*, J. Math. Phys. **11** (1970) 437–449 &lbrack;[doi:10.1063/1.1665157](https://doi.org/10.1063/1.1665157)&rbrack;

and in the smooth category (needed in practice) due to 

* {#BernalSánchez03} Antonio N. Bernal, [[Miguel Sánchez]], _On smooth Cauchy hypersurfaces and Geroch's splitting theorem_, Commun. Math. Phys. 243 (2003) 461-470 &lbrack;[arXiv:gr-qc/0306108](http://arxiv.org/abs/gr-qc/0306108), [doi:10.1007/s00220-003-0982-6](https://doi.org/10.1007/s00220-003-0982-6)&rbrack;

* {#BernalSánchez05} [[Antonio N. Bernal]], [[Miguel Sánchez]], *Smoothness of time functions and the metric splitting of globally hyperbolic spacetimes*, Commun. Math. Phys. **257** (2005) 43-50 &lbrack;[arXiv:gr-qc/0401112](https://arxiv.org/abs/gr-qc/0401112), [doi:10.1007/s00220-005-1346-1](https://doi.org/10.1007/s00220-005-1346-1)&rbrack;


* {#Sánchez22} [[Miguel Sánchez]], *Globally hyperbolic spacetimes: slicings, boundaries and counterexamples*, Gen Relativ Gravit **54** 124 (2022) &lbrack;[arXiv:2110.13672](https://arxiv.org/abs/2110.13672), [doi:10.1007/s10714-022-03002-6](https://doi.org/10.1007/s10714-022-03002-6)&rbrack;



[[!redirects Cauchy surface]]
[[!redirects Cauchy surfaces]]
