
#Contents#
* table of contents
{:toc}

## Idea 

On a [[Riemannian manifold]] $(X,g)$, a __geodesic__ (or geodesic line, geodesic path) is a path $x : I \to X$ which locally minimizes the length between its end points. In other words, it is a [[critical point]] of the [[functional]] of length 

$$
  (x : I \to M) 
   \mapsto 
   \int_I \sqrt{g(\stackrel{\cdot}{x}(t),\stackrel{\cdot}{x}(t))} dt
$$

on the appropriate space of curves $I \to X$, where $g$ is the [[metric]] tensor. Hence it satisfies the corresponding [[Euler-Lagrange equation]]s, namely for geodesic $x : I\to M$ on a Riemannian manifold $M$, the [[covariant derivative]] (for the [[Levi-Civita connection]])

$$
\nabla_{\stackrel{\cdot}{x}} \stackrel{\cdot}{x} = 0
$$

vanishes. 

In local coordinates, with [[Christoffel symbol]]s $\Gamma^i_{jk}$ the Euler-Lagrange equations for geodesics form a system 

$$
\frac{d^2 x^i}{dt^2} + \sum_{jk} \Gamma^i_{jk}(x) \frac{d x^j}{dt} \frac{d x^k}{dt} = 0.
$$

So this means that a curve is a _geodesic_ if at every point its [[tangent vector]] is the [[parallel transport]] of the tangent vector at the start point along the curve.


## Links and literature

* [[variational calculus]]

* en.wikipedia: [geodesic](http://en.wikipedia.org/wiki/Geodesic) 
* Springer [[eom]]: Yu. A. Volkov, [Geodesic line](http://eom.springer.de/G/g044120.htm); Yu. A. Volkov, [Geodesic coordinates](http://eom.springer.de/G/g044060.htm); [Geodesic distance](http://eom.springer.de/G/g044080.htm); V.A. Zalgaller, [Geodesic geometry](http://eom.springer.de/G/g044100.htm); D.V. Anosov, [Geodesic flow](http://eom.springer.de/G/g044090.htm)
* Sh. Kobayashi, K. Nomidzu, _Foundations of differential geometry_, vol 1, 1963, vol 2, 1969, Wiley Interscience; reedition 1996 in series Wiley Classics; Russian ed.: Nauka, Moscow 1981.  
* Arthur L. Besse, _Einstein manifolds_, Ergebnisse der Mathematik und ihrer Grenzgebiete, Band 10, Springer-Verlag 1987, xii + 510 pp. (for a review see [Bull. AMS](http://projecteuclid.org/euclid.bams/1183554925) and [MR88f:53087](ttp://www.ams.org/mathscinet-getitem?mr=88f:53087)); reprinted 2008, Springer Classics in Math. 

[[!redirects geodesic line]]
[[!redirects geodesic path]]
[[!redirects geodesics]]