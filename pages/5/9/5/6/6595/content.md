
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

## Definitions
 {#Definition}

### In terms of differential forms
 {#InTermsOfDifferentialForms}

In [[Riemannian geometry]], the __curl__ or __rotation__ of a [[vector field]] $v$ on an [[orientation|oriented]] $3$-[[dimension|dimensional]] [[Riemannian manifold]] $(X,g)$ is the vector field denoted $curl(v)$ (or $rot(v)$ or $\Del \times v$) defined by

$$
  curl(v) \;\coloneqq\; g^{-1} \left(\star_g d_{dR}\, g(v) \right) 
  \,.
$$

where 

1. $\Gamma(T X) \underoverset{\underset{g}{\longrightarrow}}{\overset{g^{-1}}{\longleftarrow}}{\phantom{AA}\simeq\phantom{AA}} \Omega^1(X)$ is the [[linear isomorphism]] between [[vector fields]] and [[differential 1-forms]] given by the [[metric tensor]] $g$;

2. $d_{dR} \;\colon\; \Omega^n(X) \longrightarrow \Omega^{n+1}(X)$ is the [[de Rham differential]]

3. $\star_g \;\colon\; \Omega^n(X) \to \Omega^{dim(X)-n}(X)$ is the [[Hodge star operator]] (which uses the orientation of $X$). 

Notice that for this to make sense it is crucial that the [[dimension]] of $X$ is $3$, for only then is the Hodge dual of the de Rham differential of a $1$-form again a $1$-form; that is, $n = 3$ is the unique solution of $n - (1 + 1) = 1$.


### Via integration {#ViaIntegration}

Alternatively, the curl/rotation of a vector field $\vec v$ at some point $x\in X$ may be defined as the [[limit of a sequence|limit]] [[integral]] formula 

$$
  \vec{n}\cdot rot \vec v 
  = 
  \lim_{area S\to 0} 
  \frac{1}{area S} 
  \oint_{\partial S} \vec{t}\cdot \vec v d r
$$

where $D$ runs over the smooth oriented [[surfaces]] ([[submanifolds]] of [[dimension]] $2$) containing the point $x$ and with smooth [[boundary]] $\partial D$, $\vec{n}$ is the unit vector through the surface $S$, and $\vec{t}$ is the unit vector tangent to the [[curve]] $\partial S$. (We use the orientation of $X$ to determine the [[direction of a vector|direction]] of $\vec{n}$ from the [[orientation]] of $S$.)

This formula does not depend on the shape of boundaries taken in limiting process, so one can typically take a [[coordinate chart]] and [[discs]] with decreasing radius in this particular coordinate chart.  One can even use $\pi r^2$ in place of the actual area of the disc around $x$ with coordinate-radius $r$, to save on calculating this area, as long as the coordinate chart assigns the standard coordinates to the metric at $x$.

The proof that this definition is coherent and agrees with the previous one is essentially the [[Kelvin–Stokes Theorem]]; see [below](#Stokes) for discussion.


### Via cross products

More generally, if $(X,g)$ is a [[Riemannian manifold]] whose [[cotangent spaces]] (equivalently, [[tangent spaces]]) are smoothly equipped with a binary [[cross product]] $&#10761;\colon \Omega^2(X;\mathbb{R}) \to \Omega^1(X;\mathbb{R})$, then the __curl__ of any vector field $v$ is

$$
  curl(c) 
  \;=\; g^{-1} &#10761; d_{dR} g(v)
$$

However, this is not as general as it may appear:

* in $0$ or $1$ [[dimension]], the cross product, hence the curl, must always be $0$;
* in $3$ dimensions, a smooth choice of cross product is equivalent to a smooth choice of [[orientation]], and we recover the previous formula;
* in $7$ dimensions, if a smooth choice of cross product is possible (as on the [[7-sphere]]), then uncountably many are possible, giving as many different notions of curl;
* in any other number of dimensions, no binary cross product exists at all, hence no curl.

That said, there are also cross products of other [[arities|arity]] in other dimensions; using essentially the same formula, we can take the curl of a $k$-[[multivector field]] if we have a smooth $(k+1)$-ary cross product.  Or if the cross product is other than vector-valued, then we can obtain a curl that is other than a vector field.

In particular, in $2$ dimensions, we have the __scalar curl__

$$
  curl(c) 
  \;=\; &#10761; d_{dR} g(v)
$$

where $&#10761;\colon \Omega^2(X;\mathbb{R}) \to \Omega^0(X;\mathbb{R})$ is the [[volume form]] (or area form) on the $2$-dimensional Riemannian manifold $X$.


## Examples

If $(X,g)$ is $\mathbb{R}^3$ endowed with the canonical Euclidean metric, then the curl of a vector field $(v^1,v^2,v^3) = v^1\partial_1 + v^2\partial_2 + v^3\partial_3$ is

$$
curl(v)^1 = \frac{\partial v^3}{\partial x^2}-\frac{\partial v^2}{\partial x^3} 
;\qquad
curl(v)^2 = \frac{\partial v^1}{\partial x^3}-\frac{\partial v^3}{\partial x^1} 
;\qquad
curl(v)^3 = \frac{\partial v^2}{\partial x^1}-\frac{\partial v^1}{\partial x^2} 
.$$

This is the classical curl from [[vector analysis]].

If $(X,g)$ is $\mathbb{R}^2$ endowed with the canonical Euclidean metric, then the curl of a vector field $(v^1,v^2) = v^1\partial_1 + v^2\partial_2$ is

$$
curl(v) = \frac{\partial v^2}{\partial x^1}-\frac{\partial v^1}{\partial x^2} 
.$$


## Relation to the Stokes theorems {#Stokes}

Recall that if $X$ is an $n$-dimensional [[differentiable manifold]], $D$ is a $p$-dimensional [[submanifold]] [[manifold with boundary|with boundary]], and $\alpha$ is a [[differentiable function|differentiable]] $(p-1)$-rank [[exterior differential form]] on a [[neighbourhood]] of $D$ in $X$, then the generalized [[Stokes Theorem]] says that the [[integration of differential forms|integral]] of $\alpha$ on the boundary $\partial{D}$ equals the integral on $S$ of the [[de Rham differential]] $\mathrm{d}_{DR}\alpha$.

When $n=3$, $p=2$, and $X$ is equipped with an orientation and a metric, then this is equivalent to saying that the integral of a vector field $v$ along the boundary of an oriented surface $D$ in $X$ is equal to the integral of the vector field\'s curl across the surface:

\[ \int_{\partial{D}} v \cdot \mathrm{d}\mathbf{r} = \int_D curl v \cdot \mathrm{d}\mathbf{S} \label{KS}.\]

(In particular, when $X$ is $\mathbb{R}^3$ with its standard orientation and metric, then this is equivalent to the classical Kelvin--Stokes Theorem.)  At least, this is what it says if the curl is defined [in terms of differential forms](#InTermsOfDifferentialForms); if the curl is defined [via integration](#ViaIntegration) instead, then \eqref{KS} is immediate, and the Kelvin--Stokes Theorem says that this definition matches the other one.

When $n=2$, $p=2$, and $X$ is equipped with an orientation and a metric, then the Stokes Theorem is equivalent to saying that the integral of a vector field $v$ along a [[simple closed curve]] in $X$ is equal to the integral of the vector field\'s scalar curl on the region $D$ enclosed by the curve:

\[ \int_{\partial{D}} v \cdot \mathrm{d}\mathbf{r} = \int_D curl v \mathrm{d}A \label{Green}.\]

(In particular, when $X$ is $\mathbb{R}^2$ with its standard orientation and metric, then this is equivalent to the curl-circulation form of [[Green's Theorem]].)


## Remark

In many classical applications of the curl in [[vector analysis]], the Riemannian structure is actually irrelevant, and the gradient can be replaced with the [[exterior differential|deRham differential]] $d_{dR}$.  That is, $X$ is treated as the $1$-form $g(X)$, its curl is treated as the $2$-form $d_{dR} g(X)$, and once these identifications are made there is no need to involve $g$ or $X$ directly at all.


## Related concepts

* [[nabla]]

* [[gradient]]

  * [[gradient flow]]

  * [[symplectic gradient]]

* [[Hamiltonian flow]]

* **curl**

* [[divergence]]


## References

See also 

* Wikipedia, _[Curl](https://en.wikipedia.org/wiki/Curl_%28mathematics%29)_


[[!redirects curl]]
[[!redirects curls]]
[[!redirects curl of a vector field]]
[[!redirects curls of vector fields]]
[[!redirects rotation of a vector field]]
[[!redirects rotations of vector fields]]
