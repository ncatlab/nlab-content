[[!redirects hyperbolic functions]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Trigonometry
+-- {: .hide}
[[!include trigonometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

The hyperbolic functions (or sometimes *hyperbolic trigonometric functions*) are analogues of the usual [[trigonometric functions]], but adapted to the [[hyperbola]] $x^2 - y^2 = 1$ rather than the [[circle]] $x^2 + y^2 = 1$. 

## Definition 

There are multiple ways of introducing the hyperbolic functions. Probably the most straightforward is to use the following definitions based on the [[exponential function]] $\exp$: 

* $\cosh(x) \coloneqq \frac1{2} (\exp(x) + \exp(-x))$ (*hyperbolic cosine*, sometimes pronounced as "kosh"). This can be interpreted as a function $\mathbb{R} \to \mathbb{R}$, or as a function $\mathbb{C} \to \mathbb{C}$. 

* $\sinh(x) \coloneqq \frac1{2} (\exp(x) - \exp(-x))$ (*hyperbolic sine*, sometimes pronounced as "cinch"). This also can be interpreted as a function $\mathbb{R} \to \mathbb{R}$, or as a function $\mathbb{C} \to \mathbb{C}$. 

* The remaining hyperbolic functions are defined by $\tanh \coloneqq \frac{\sinh}{\cosh}$, $\coth = \frac{\cosh}{\sinh}$, $\sech = \frac1{\cosh}$, $\csch = \frac1{\sinh}$. 

Note that $(\cosh(t), \sinh(t))$ (as a pair of real-valued functions) lies on the hyperbola $x^2 - y^2 = 1$, and in fact this is a parametrization of the hyperbola, much as $(\cos(t), \sin(t))$ parametrizes the unit circle $x^2 + y^2 = 1$. 

It is straightforward to establish the following further properties by exploiting properties of the exponential function: 

* $\cosh(x + y) = \cosh(x)\cosh(y) + \sinh(x)\sinh(y)$ and $\sinh(x+y) = \sinh(x)\cosh(y) - \cosh(x)\sinh(y)$ ("addition formulas"), 

* $(\cosh)' = \sinh$ and $(\sinh)' = \cosh$, 

* $\cosh(x + 2\pi i) = \cosh(x)$ and $\sinh(x + 2\pi i) = \sinh(x)$ for all $x \in \mathbb{C}$, 

* $\cosh(x) = \sum_{n \geq 0} \frac{x^{2 n}}{(2 n)!}$ and $\sinh(x) = \sum_{n \geq 0} \frac{x^{2 n + 1}}{(2 n + 1)!}$. 

### Alternative presentation 

Another avenue is first to introduce the _inverse_ hyperbolic functions as [[integrals]] of suitable [[algebraic functions]], e.g., 

$$\sinh^{-1}(t) = \int_0^t \; \frac{d x}{y}$$ 

where $y = \sqrt{x^2 + 1}$. Or, what is essentially the same, construct a solution $p(t)$ to the [[differential equation]] 

$$(p')^2 = p^2 + 1, \qquad p(0) = 0$$ 

so that $(p'(t), p(t))$ parametrizes the curve $x^2 - y^2 = 1$; the approach by invoking an integral is in accordance with an elementary method in differential equations that goes by the name "separation of variables". 

This particular approach is similar to the way that [[elliptic functions]] were introduced historically, by studying integrals of algebraic functions 

$$\int \; \frac{d x}{y}$$ 

where $y$ is related to $x$ via an algebraic relation such as $y^2 = x^3 + a x + b$. For suitable such relations these give the various so-called _elliptic integrals_; for more on what this has to do with ellipses, see Wikipedia, e.g., [here](http://en.wikipedia.org/wiki/Elliptic_integral#Incomplete_elliptic_integral_of_the_first_kind). Elliptic functions are then suitable inverses of elliptic integrals, following Jacobi, Abel, and others throughout the nineteenth century (e.g., Weierstrass; see also [[Weierstrass elliptic function]]). 

### Area parametrization 

The way that hyperbolic functions $(\cosh t, \sinh t)$ parametrize the hyperbola $x^2 - y^2 = 1$ is not through an arc length parametrization (the usual way that circular functions $(\cos t, \sin t)$ parametrize the circle $x^2 + y^2 = 1$), but rather through an area parametrization. In fact, both circular and hyperbolic functions may be parametrized in unison through area, as follows. 

Consider, for a parameter $t \in [0, \infty)$, the area $A$ of the planar region which is bounded on three sides by 

* The line segment from $(0, 0)$ to $(1, 0)$, 

* The line segment from $(0, 0)$ to $(\cosh t, \sinh t)$, 

* The arc along the hyperbola $x^2 - y^2 = 1$ that is between the points $(1, 0)$ and $(\cosh t, \sinh t)$. 

Then $t = 2A$ for positive $t$. (Negative $t$ can also be accommodated under this scheme if we consider oriented area.) 

Likewise, consider for a parameter $t \in [0, \pi)$ the area $A$ of the planar region which is bounded on three sides by 

* The line segment from $(0, 0)$ to $(1, 0)$, 

* The line segment from $(0, 0)$ to $(\cos t, \sin t)$, 

* The arc along the circle $x^2 + y^2 = 1$ that is between the points $(1, 0)$ and $(\cos t, \sin t)$. 

Then $t = 2A$. (Other values of $t$ can be accommodated by considering [[orientation]], as well as areas swept out multiple times if need be.) 

## Related entries

* [[trigonometry]]

[[!redirects hyperbolic functions]] 

[[!redirects hyperbolic trigonometric function]]
[[!redirects hyperbolic trigonometric functions]]
