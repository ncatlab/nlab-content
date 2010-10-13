
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

The definition of _geodesic convexity_ is like that of _[[convexity]]_ , but with straight lines in a [[Euclidean space]] generalized to [[geodesics]] in a [[Riemannian manifold]] or [[metric space]].

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

For $X$ a [[metric space]] ...


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


[[!redirects geodesically convex]]
[[!redirects strongly geodesically convex]]

[[!redirects convexity radius]]