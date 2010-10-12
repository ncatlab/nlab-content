
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition


The $n$-dimensional unit **sphere** , or simply **$n$-sphere**, is the [[topological space]] given by the [[subset]] of the $(n+1)$-dimensional [[Cartesian space]] $\mathbb{R}^{n+1}$ consisting of all points $x$ whose distance from the origin is $1$

$$ 
  S^n = \{ x: \mathbb{R}^{n+1} \;|\; \|x\| = 1 \} 
  \,.
$$

The $n$-dimensional sphere of radius $r$ is
$$ S^n_r = \{ x: \mathbb{R}^{n+1} \;|\; \|x\| = r \} .$$
Topologically, this is equivalent to the unit sphere for $r \gt 0$, or a [[point]] for $r = 0$.

This is naturally also a [[smooth manifold]] of [[dimension]] $n$, with the [[smooth structure]] induced from the standard sooth structure on $\mathbb{R}$^n.

One can also talk about a sphere in an arbitrary (possibly infinite-dimensional) [[Banach space]] $V$:
$$ S(V) = \{ x: V \;|\; \|x\| = 1 \} .$$
Homotopy theorists define $S^\infty$ to be the sphere in the (incomplete) [[normed vector space]] (traditionally with the $l^2$ norm) of infinite [[sequence]]s almost all of whose values are $0$, which is the [[directed colimit]] of the $S^n$:
$$ S^{-1} \hookrightarrow S^0 \hookrightarrow S^1 \hookrightarrow S^2 \hookrightarrow \cdots S^\infty .$$
But these provide nothing new to [[homotopy theory]], as these infinite-dimensional spheres are [[contractible space|contractible]].  (See [Usenet discussion](http://www.math.niu.edu/~rusin/known-math/93_back/s-infty).)



## Properties

* The $n$-sphere is the [[boundary]] of the $(n+1)$-[[ball]].

* These spheres, or rather their underlying [[topological space]]s or [[simplicial set]]s, are fundamental in (ungeneralised) [[homotopy theory]].  In a sense, [[Whitehead's theorem]] says that these are all that you need; no further [[generalized (Eilenberg-Steenrod) homotopy theory|generalised homotopy theory]] (in a sense [[Eckmann–Hilton duality|dual]] to [[Eilenberg–Steenrod cohomology theory]]) is needed.



## Low dimensions

*  The $(-1)$-sphere is the [[empty space]].
*  The $0$-sphere is the disjoint union of two [[point]]s.
*  The $1$-sphere is the [[circle]].
*  The $2$-sphere is usual sphere from ordinary geometry.

Note that this violates the convention that a $1$-foo is a foo; instead the ruling convention being used is that an $n$-foo has dimension $n$.  One could follow both by saying '$n$-circle' instead, although this might get confused with the $n$-[[torus]].


[[!redirects n-sphere]]
[[!redirects spheres]]