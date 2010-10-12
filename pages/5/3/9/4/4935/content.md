
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


For $(X,g)$ a [[Riemannian manifold]] and $p \in X$ a point, the **geodesic flow** at $p$ is the map defined on an open neighbourhood of the origin in $(T_p X ) \times \mathbb{R}$ that sends $(v,r)$ to the endpoint of the [[geodesic]] that starts with tangent vector $v$ at $p$ and has length $r$.

(...)

## Definition

Let $(X,g)$ be a [[Riemannian manifold]]

+-- {: .un_defn}
###### Definition

(...) geodesic flow (...)

=--


{#InjectivityRadius}
+-- {: .un_defn}
###### Definition

For $p \in P$ a point, the **injectivity radius** $inj_p \in \mathbb{R}$ is the [[supremum]] over all values of $r \in \mathbb{R}$ such that the geodesic flow starting at $p$ with radius $r$ $\exp(-) : B_r(T_p X) \to X$ is a [[diffeomorphism]] onto its image.

The injectivity radius of $X$ is the infimum of the injectivity radii at each point.

=--


{#ConvexityRadius}
+-- {: .un_defn}
###### Definition

(...) convexity radius (...)

=--


## Properties

### Properties of the injectivity radius

+-- {: .un_proposition}
###### Proposition

The injectivity radius is 

* either equal to half the length of the smalled periodic geodesic,

* or equal to the smallest distance between two conjugate points.

=--

This appears for instance as scholium 91 in ([Berger](#Berger)).



### Lower bounds on the injectivity radius


There are several lower boundas on the [injectivity radius](#InjectivityRadius) of a Riemannian manifold.

+-- {: .un_proposition}
###### Proposition

The convexity radius is always less than or equal to half of the injectivity radius:

$$
  conv (X,g) \leq \frac{1}{2} inj(X,g)
  \,.
$$

=--

This appears for instance as proposition IX.6.1 in [Chavel](#Chavel), where it is attributed to M. Berger (1976). In ([Berger](#Berger)) it is proposition 95. 



Let $R$ be the [[Riemann curvature]] tensor of $g$. For $p \in X$ the [[sectional curvature]] of a plane spanned by vectors $v,w \in T_p X$ is

$$
  K(v,w) :=
  \frac{R(v,w,v,w)}{g(v,v)g(w,w) - g(v,w)^2}
  \,.
$$

Say that $(X,g)$ is **complete** if, equivalently,  

* with the [[distance]] function $X$ is a [[complete metric space]];

* $(X,g)$ is geodesically complete in that for all $v \in T_p X$ the flow $t \mapsto \exp_p(t v)$ exists for all $t \in \mathbb{R}$.


+-- {: .un_theorem}
###### Theorem

Let $(X,g)$ be complete and such that

1. the [[absolute value]] of the sectional curvature at all points is bounded from above;

1. the [[volume]] of the geodesic unit ball at all points is bounded from below.

Then the injectivity radius is positive.

=--

This is due to ([CheegerGromovTaylor](#CheegerGromovTaylor)). A survey is in ([Grant](#Grant)).

+-- {: .un_theorem}
###### Theorem

Every [[paracompact manifold]] admits a complete [[Riemannian metric]] with bounded absolute sectional curvature and positive injectivity radius.

=--

This is shown in ([Greene](#Greene)).

## References

* Gabriel Paternein, _Geodesic flows_ Birkh&#228;user (1999)

The following is literature on injectivity radius estimates

A general exposition is in sectin 6 "Injectivity, Convexity radius and cut locuss" of

* Marcel Berger, _A panoramic view of Riemannian geometry_
{#Berger}

Also section IX of

* Isaac Chavel, _Riemannian geometry: a modern introduction_
{#Chavel}

A survey of the main estimates is in

* James Grant, _Injectivity radius estimates_ ([pdf](http://www.mat.univie.ac.at/~grant/papers/talk.pdf))
{#Grant}

The main theorem is due to

* [[Jeff Cheeger]], M. Gromov, and M. Taylor, _Finite propagation speed, kernel estimates for functions of the Laplace operator, and the geometry of complete Riemannian manifolds_ , J. Differential Geom., 17 (1982), pp. 15&#8211;53.
{#CheegerGromovTaylor}

Older results on compact manifolds are in

* [[Jeff Cheeger]], _Finiteness theorems for Riemannian manifolds_ . 

The existence of metrics with all the required propertiers for the injectivity estimates (completeness, bounded absolute sectional curvature) on paracompact manifolds is shown in

* R. Greene, _Complete metrics of bounded curvature on noncompact manifolds_  Archiv der Mathematik Volume 31, Number 1 
{#Greene}

More discussion of construction of Riemannian manifolds with bounds on curvature and volume is in

* John Lott, Zhongmin Chen, _Manifolds with quadratic curvature decay and slow volume growth_ ([pdf](http://math.berkeley.edu/~lott/science.pdf))

Analogous results for [[Lorentzian manifold]]s are discussed in

* Bing-Long Chen, Philippe G. LeFloch, _Injectivity Radius of Lorentzian Manifolds_ ([pdf](http://philippelefloch.files.wordpress.com/2009/12/2008-chenlefloch-cmp.pdf))



[[!redirects injectivity radius]]