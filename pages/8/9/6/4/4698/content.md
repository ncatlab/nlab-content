
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Riemannian geometry
+-- {: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

On a [[Riemannian manifold]] $(X,g)$, a __geodesic__ (or geodesic line, geodesic path) is a path $x : I \to X$, for some (possibly infinite) [[interval]] $I$, which locally minimizes distance.

## Definition

One way to define a geodesic is as a [[critical point]] of the [[functional]] of length 

$$
  (x : I \to M) 
   \mapsto 
   \int_I \sqrt{g(\stackrel{\cdot}{x}(t),\stackrel{\cdot}{x}(t))} dt
$$

on the appropriate space of curves $I \to X$, where $g$ is the [[metric]] tensor. This implies that it satisfies the corresponding [[Euler-Lagrange equation]]s, which in this case means that the [[covariant derivative]] (for the [[Levi-Civita connection]])

$$
\nabla_{\stackrel{\cdot}{x}} \stackrel{\cdot}{x} = 0
$$

vanishes.

In local coordinates, with [[Christoffel symbol]]s $\Gamma^i_{jk}$ the Euler-Lagrange equations for geodesics form a system 

$$
\frac{d^2 x^i}{dt^2} + \sum_{jk} \Gamma^i_{jk}(x) \frac{d x^j}{dt} \frac{d x^k}{dt} = 0.
$$

So this means that a curve is a _geodesic_ if at every point its [[tangent vector]] is the [[parallel transport]] of the tangent vector at the start point along the curve.

## Minimizing geodesics

A geodesic may not *globally* minimize the distance between its end points.  For instance, on a 2-dimensional [[sphere]], geodesics are [[arcs]] of [[great circle]]s.  Any two distinct non-antipodal points are connected by exactly two such geodesics, one shorter than the other (you can go from Los Angeles to Boston directly across North America, or the long way around the world).

A geodesic which does globally minimize distance between its end points is called a **minimizing geodesic**.  The length of a minimizing geodesic between two points defines a distance function for any Riemannian manifold which makes it into a [[metric space]].

## Related concepts

* [[prime geodesic]]

* [[geodesic completeness]]

* [[totally geodesic submanifold]]

* [[variational calculus]]


## References


* Wikipedia: *[Geodesic](http://en.wikipedia.org/wiki/Geodesic)*
 
* Springer [[eom]]: Yu. A. Volkov, [Geodesic line](http://eom.springer.de/G/g044120.htm); Yu. A. Volkov, [Geodesic coordinates](http://eom.springer.de/G/g044060.htm); [Geodesic distance](http://eom.springer.de/G/g044080.htm); V.A. Zalgaller, [Geodesic geometry](http://eom.springer.de/G/g044100.htm); D.V. Anosov, [Geodesic flow](http://eom.springer.de/G/g044090.htm)

* Sh. Kobayashi, K. Nomidzu, _Foundations of differential geometry_, vol 1, 1963, vol 2, 1969, Wiley Interscience; reedition 1996 in series Wiley Classics; Russian ed.: Nauka, Moscow 1981.  

* Arthur L. Besse, _Einstein manifolds_, Ergebnisse der Mathematik und ihrer Grenzgebiete, Band 10, Springer-Verlag 1987, xii + 510 pp. (for a review see [Bull. AMS](http://projecteuclid.org/euclid.bams/1183554925) and [MR88f:53087](ttp://www.ams.org/mathscinet-getitem?mr=88f:53087)); reprinted 2008, Springer Classics in Math. 

On [[Maslov indices]] and stability of geodesics:

* [[Paolo Piccione]], [[Alessandro Portaluri]], [[Daniel V. Tausk]]: *Spectral Flow, Maslov Index and Bifurcation of Semi-Riemannian Geodesics*, Annals of Global Analysis and Geometry **25** (2004) 121–149 \[<a href="https://doi.org/10.1023/B:AGAG.0000018558.65790.db">doi:10.1023/B:AGAG.0000018558.65790.db</a>\]

* {#PortaluriWuYang21} [[Alessandro Portaluri]], Li Wu, Ran Yang: *Linear instability for periodic orbits of non-autonomous Lagrangian systems*, Nonlinearity **34** 1 (2021) 237 &lbrack;[arXiv:1907.05864](https://arxiv.org/abs/1907.05864)&rbrack;


[[!redirects geodesic line]]
[[!redirects geodesic path]]
[[!redirects geodesics]]

[[!redirects geodesic equation]]
[[!redirects geodesic equations]]
