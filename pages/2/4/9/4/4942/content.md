
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

The definition of _geodesic convexity_ is like that of _[[convexity]]_, but with straight lines in an [[affine space]] generalized to [[geodesics]] in a [[Riemannian manifold]] or [[metric space]].

## Definition

### In a Riemannian manifold

Let $(X,g)$ be a [[Riemannian manifold]] and $C \subset X$ a [[subset]]. We say that $C$ is

* **weakly geodesically convex** if for any two points from $C$ there exists exactly one minimizing [[geodesic]] in $C$ connecting them;

* **geodesically convex** if for any two points in $C$ there exists exactly one minimizing geodesic in $X$ connecting them, and that geodesic arc lies completely in $C$

* **strongly geodesically convex** if for any two points in $C$ there exists exactly one minimizing geodesic in $X$ connecting them, and that geodesic arc lies completely in $C$; and furthermore there exists no nonminimizing geodesic inside $C$ connecting the two points.

+-- {: .un_defn}
###### Definition

The **convexity radius** at a point $p \in X$ is the [[supremum]] (which may be $+ \infty$) of $r \in \mathbb{R}$ such that for all $\eta \lt r$ the geodesic ball $B_p(r)$ is strongly geodesically convex. 

The convexity radius of $(X,g)$ is the [[infimum]] over the points $p \in X$ of the convexity radii at these points.

=--


### In a metric space

For $X$ a [[metric space]], a *distance-preserving path* is a function $x \colon [a,b]\to X$ which is an [[isometry]].  This is a metric-space analogue of an "arc-length-parametrized minimizing geodesic" on a Riemannian manifold.  In particular, the existence of such a path implies that $d(x(a),x(b)) = b-a$.  We then say that $X$ is **geodesic** (or *geodesically convex*) if any two points can be connected by a distance-preserving path.

We say that $X$ is a **length space** if for any $x$ and $y$, the distance $d(x,y)$ is the [[infimum]] of the lengths of all continuous paths from $x$ to $y$.  The [[Hopf-Rinow theorem]] says that for a metric space in which every [[closed subset|closed]] [[bounded subset|bounded]] subset is [[compact space|compact]], being a length space is equivalent to being geodesic.


## Properties

+-- {: .un_proposition}
###### Proposition

At any point $p \in X$ of a Riemannian manifold, the convexity radius is positive.

=--

This is due to ([Whitehead](#Whitehead)).


+-- {: .un_proposition}
###### Proposition

If $X$ is a [[compact space]] then the convexity radius of $(X,g)$ is positive.

=--

This is reproduced for instance as proposition 95 in ([Berger](#Berger))

+-- {: .un_theorem}
###### Theorem

Every [[paracompact manifold]] admits a complete [[Riemannian metric]] with bounded absolute sectional curvature and positive injectivity radius.

=--

This is shown in ([Greene](#Greene)).


## References

Original literature includes

* J. H. C. Whitehead, _Convex regions in the geometry of paths_ Quart. J. Math. 3, 33--42 (1932).
{#Whitehead}

* R. Greene, _Complete metrics of bounded curvature on noncompact manifolds_  Archiv der Mathematik Volume 31, Number 1 (1978) 
{#Greene}


A review of geodesic convexity in Riemannian manifolds is in 

* Isaac Chavel, _Riemannian geometry &#8211; A modern introduction_ Cambridge University Press (1993)
{#Chavel}

* Marcel Berger, _A panoramic view of Riemannian geometry_
{#Berger}

A categorical perspective on geodesic convexity for metric spaces can be found in

* _Taking categories seriously_, Reprints in Theory and Applications of Categories, No. 8, 2005, pp. 1&#8211;24. ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))

Much of the issues on geodesic convexity becomes more complicated when trying to generalize from Riemannian to Lorentzian manifolds, as discussed at length at 

* John K. Beem, Paul E. Ehrlich, Kevin L. Easley, _Global Lorentzian geometry_, Marcel Dekker, 1996, 635 pages
* John K. Beem, _Lorentzian geometry in the large_, Math. of gravitation I, Lorentzian geometry and Einstein equations, Banach Center Publications __41__, Inst. of Math. Polish Acad. of Sci. Warszawa 1997 [pdf](http://matwbn.icm.edu.pl/ksiazki/bcp/bcp41/bcp4111.pdf)

In particular, the conclusions of the Hopf-Rinow Theorem fail to hold for complete Lorentzian manifolds.
[[!redirects geodesically convex]]
[[!redirects strongly geodesically convex]]
[[!redirects geodesically convex subset]]
[[!redirects strongly geodesically convex subset]]
[[!redirects geodesically convex set]]
[[!redirects strongly geodesically convex set]]

[[!redirects convexity radius]]

[[!redirects length space]]
[[!redirects geodesic metric space]]
[[!redirects geodesic space]]
[[!redirects length spaces]]
[[!redirects geodesic metric spaces]]
[[!redirects geodesic spaces]]
