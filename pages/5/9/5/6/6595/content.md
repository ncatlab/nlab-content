
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

## Definition
 {#Definition}

### In terms of differential forms
 {#InTermsOfDifferentialForms}

In [[Riemannian geometry]], the **curl** or __rotation__ of a [[vector field]] $v$ over an [[orientation|oriented]] $3$-[[dimension|dimensional]] [[Riemannian manifold]] $(X,g)$ is the vector field denoted $curl(v)$ (or $rot(v)$) defined by

$$
  curl(v) \;\coloneqq\; g^{-1} \left(\star_g d_{dR}\, g(v) \right) 
  \,.
$$

where 

1. $\Gamma(T X) \underoverset{\underset{g}{\longrightarrow}}{\overset{g^{-1}}{\longleftarrow}}{\phantom{AA}\simeq\phantom{AA}} \Omega^1(X)$ is the [[linear isomorphism]] between [[vector fields]] and [[differential 1-forms]] given by the [[metric tensor]] $g$;

1. $d_{dR} \;\colon\; \Omega^n(X) \longrightarrow \Omega^{n+1}(X)$ is the [[de Rham differential]]

1. $\star_g \;\colon\; \Omega^n(X) \to \Omega^{dim(X)-n}(X)$ is the [[Hodge star operator]]. 


Notice that for this to make sense it is crucial that the [[dimension]] of $X$ is 3, for only then is the Hodge dual of the de Rham differential of a 1-form again a 1-form, since $3 - (1 + 1)  = 1$.

### Via integration

Alternatively, the curl/rotation of a vector field $\vec v$ in some point $x\in X$ is calculated (or alternatively defined) by the [[limit of a sequence|limit]] [[integral]] formula 

$$
  \vec{n}\cdot rot \vec v 
  = 
  \lim_{area S\to 0} 
  \frac{1}{area S} 
  \oint_{\partial S} \vec{t}\cdot \vec v d r
$$

where $D$ runs over the smooth (pseudo)-oriented [[surfaces]] (smooth [[submanifolds]] of [[dimension]] $2$) containing the point $x$ and with smooth [[boundary]] $\partial D$, $\vec{n}$ is the unit vector of outer normal to the surface $S$, and $\vec{t}$ is the unit vector tangent to the [[curve]] $\partial S$. 

This formula does not depend on the shape of boundaries taken in limiting process, so one can typically take a [[coordinate chart]] and [[balls]] with decreasing radius in this particular coordinate chart. 

(We use the orientation of $X$ in the [[Hodge dual]], or alternatively in determining the [[direction of a vector|direction]] of $\vec{n}$ from the [[orientation]] of $S$ or the direction of $\vec{t}$ fom the pseudo-orientation of $S$.)

### Via cross products

More generally, if $(X,g)$ is a [[Riemannian manifold]] whose [[cotangent spaces]] (equivalently, [[tangent spaces]]) are smoothly equipped with a binary [[cross product]] $&#10761;\colon \Omega^2(X;\mathbb{R}) \to \Omega^1(X;\mathbb{R})$, then the __curl__ of any vector field $v$ is

$$
  curl(c) 
  \;=\; g^{-1} &#10761; d_{dR} g(v)
$$

However, this is not as general as it may appear:

* in $0$ or $1$ [[dimension]], the cross product, hence the curl, must always be $0$;
* in $3$ dimensions, a smooth choice of cross product is equivalent to a smooth choice of [[orientation]], and we recover the previous formula;
* in $7$ dimensions, if a smooth choice of cross product is possible (as on the [[6-sphere]]), then uncountably many are possible, giving as many different notions of curl;
* in any other number of dimensions, no binary cross product exists at all, hence no curl.

There are also cross products of other [[arities|arity]] in other dimensions; using essentially the same formula, we can take the curl of a $k$-[[multivector field]] if we have a smooth $(k+1)$-ary cross product.


## Examples

If $(M,g)$ is $\mathbb{R}^3$ endowed with the canonical Euclidean metric, then the curl of a vector field $(X^1,X^2,X^3) = X^1\partial_1 + X^2\partial_2 + X^3\partial_3$ is

$$
curl(X)^1 = \frac{\partial X^3}{\partial x^2}-\frac{\partial X^2}{\partial x^3} 
;\qquad
curl(X)^2 = \frac{\partial X^1}{\partial x^3}-\frac{\partial X^3}{\partial x^1} 
;\qquad
curl(X)^3 = \frac{\partial X^2}{\partial x^1}-\frac{\partial X^1}{\partial x^2} 
$$

This is the classical curl from [[vector analysis]].


## Remark

In many classical applications of the curl in [[vector analysis]], the Riemannian structure is actually irrelevant, and the gradient can be replaced with the [[exterior differential|deRham differential]] $d_{dR}$.  That is, $X$ is treated as the $1$-form $g(X)$, its curl is treated as the $2$-form $d_{dR} g(X)$, and once these identifications are made there is no need to involve $g$ at all.


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

* Wikipedia, _<a href="https://en.wikipedia.org/wiki/Curl_(mathematics)">Curl</a>_


[[!redirects curl]]
[[!redirects curls]]
[[!redirects curl of a vector field]]
[[!redirects curls of vector fields]]
[[!redirects rotation of a vector field]]
[[!redirects rotations of vector fields]]
