
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

[[fiber integration|Fiber integration]] in [[ordinary differential cohomology]] is the partial [[higher parallel transport|higher]] [[holonomy]] operation for [[circle n-bundles with connection]]:

for $Y \to X$ a [[bundle]] of [[compact space|compact]] [[smooth manifold]]s $S$ of [[dimension]] $k$ and $[\nabla] \in H_{diff}^n(Y)$ a class in [[ordinary differential cohomology]] of degree $n$ on $Y$, its [[fiber integration]]

$$
  \left[\exp(i \int_{Y/X} \nabla)\right] \in H^{n-k}_{diff}(X)
$$

is a differential cohomology class on $X$ of degree $k$ less.

In the particular case that $X = *$ is the [[point]] and $dim Y = k = n-1$ the element

$$
  \exp(i \int_{Y} \nabla) \in H^{1}_{diff}(*) \simeq U(1)
$$

is the [[higher parallel transport|higher]] [[holonomy]] of $\nabla$ over $Y$.

## Properties

### General

(...)

### Abstract formulation

At least the fiber integration all the way to the point exists on general grounds for the <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos%20--%20structures#DifferentialCohomology">intrinsic differential cohomology</a> in any [[cohesive (∞,1)-topos]]: the general abstract formulation is in the section _<a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos%20--%20structures#ChernSimonsTheory">Higher holonomy and Chern-Simons functional</a>_ and the implementation in [[smooth ∞-groupoid]]s is in the section _<a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#StrucChernSimons">Smooth higher holonomy and Chern-Simons functional</a>_ .

## References

A discussion in the general sense of [[fiber integration]] in [[generalized (Eilenberg-Steenrod) cohomology]] is in section 3.4 of 

* [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_

Explicit formulas for fiber integration of cocycles in [[Cech cohomology|Cech]]-[[Deligne cohomology]] are given in

* [[Kiyonori Gomi]] and Yuji Terashima, _A Fiber Integration Formula for the Smooth Deligne Cohomology_ International Mathematics Research Notices
2000, No. 13 ([pdf](http://imrn.oxfordjournals.org/content/2000/13/699.full.pdf))

