
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Trigonometry
+-- {: .hide}
[[!include trigonometry -- contents]]
=--
=--
=--



# Contents 
* table of contents
{: toc} 

## Idea 

A _trigonometric function_ is one derived from the basic [[functions]] of [[trigonometry]], $\cos$, $\sin$ ([[cosine]] and [[sine]]), which themselves are the standard [[coordinate functions]] (equivalently: [[Cartesian product|product projections]] $pr_i$) of the [[Cartesian space]] $\mathbb{R}^2$, [[restriction|restricted]] to the unit [[circle]]:

$$
  \array{
    & 
    && \mathbb{R}
    \\
    &
    &
    {}^{\mathllap{cos}}\nearrow
    & \big\uparrow{}^{ \mathrlap{pr_1} }
    \\
    \mathbb{R}
    \overset{exp}{\longrightarrow}
    &
    S^1 
    &\hookrightarrow&
    \mathbb{R}^2 
    &\simeq&
    \mathbb{R} \times \mathbb{R}
    \\
    &
    & {}_{\mathllap{sin}}\searrow & \big\downarrow{}^{ \mathrlap{pr_2} }
    \\
    &
    && \mathbb{R}
  }
  \,,
$$

or rather the result of [[composition|composing]] these restrictions with an [[arc length]] parametrization $\mathbb{R} \overset{\exp}{\to} S^1$. They are also called _circular functions_. 

In elementary [[mathematics]], there are six traditional trigonometric functions; 

1. [[sine]] $\;$ $sin$

1. [[cosine]] $\;$ $cos$

1. [[tan|tangent]] $\;$ $\tan = \frac{\sin}{\cos}$, 

1. [[cotan|cotangent]] $\;$ $\cot = \frac{\cos}{\sin}$, 

1. [[secant]] $\;$ $\sec = \frac1{\cos}$, 

1. [[cosecant]] $\;$ $\csc = \frac1{\sin}$.

The early view was that these functions measured the six possible [[ratios]] of side [[lengths]] of right [[triangles]] (as a basic case in terms of which other triangles can be analyzed; "trigonometry" = "triangle measure"). 

These six functions figure prominently in [[Euclidean geometry]] where the angles of a triangle sum to [[arc length]] $\pi$. 

There are more elaborate offshoots such as [[spherical trigonometry]] (see [[elliptic geometry]]) which was historically important for terrestrial navigation. Moreover, there are the related [[hyperbolic functions]] (see [[hyperbolic geometry]]) which result from a projective change of [[conic section]] (from a circle to a [[hyperbola]]). 

## Definition 

The most useful modern approach to [[cos]] and [[sin]] comes from taking [[Euler's formula]] as a working definition:

Let 

$$
  \exp 
  \;\colon\; 
  \mathbb{C} 
    \longrightarrow 
   \mathbb{C}^\ast
$$ 

be the [[complex number|complex]] [[exponential function]], defined by the [[exponential]] [[power series]] formula 

$$
  \exp(z) 
    \;\coloneqq\; 
  \sum_{n \geq 0} \frac{z^n}{n!}
  \,.
$$ 

These satisfy the following fundamental exponential identities: 

* $\exp(z+w) = \exp(z) \cdot \exp(w)$ ([[homomorphism]] from an additive [[group]] to a multiplicative group), 

* $\widebar{\exp(z)} = \exp(\widebar{z})$ (because [[complex conjugation]] $\widebar{(-)}$ is a [[continuous map|continuous]] [[field]] [[automorphism]]). 

As a result, if $z + \widebar{z} = 0$ (i.e., if $z$ is [[imaginary number|purely imaginary]]: $z = i t$ for some $t \in \mathbb{R}$), we have 

$$\exp(z) \cdot \widebar{\exp(z)} = 1$$ 

so that $w = \exp(z)$ lies on the unit circle defined by $w\widebar{w} = 1$. 

+-- {: .num_defn} 
###### Definition 
The _cosine function_ $\cos: \mathbb{R} \to \mathbb{R}$ is defined by $\cos(t) = Re(\exp(i t))$ ([[real part]]); the _sine function_ $\sin: \mathbb{R} \to \mathbb{R}$ is defined by $\sin(t) = Im(\exp(i t))$ ([[imaginary part]]). In other words: $\exp(i t) = \cos(t) + i\sin(t)$ (Euler). 
=-- 

This implies that $\cos(t) = \frac1{2}(\exp(i t) + \exp(-i t))$ and $\sin(t) = \frac1{2 i}(\exp(i t) - \exp(-i t))$; these equations suggest the simple [[analytic continuation]] of $\cos$ and $\sin$ to functions $\mathbb{C} \to \mathbb{C}$ on the entire complex plane. 

## Properties 

More or less immediate consequences of the definition include 

* $(\cos t)^2 + (\sin t)^2 = 1$ ("[[Pythagorean theorem]]"), since $\exp(i t)$ lies on the unit circle. This is traditionally written as $\cos^2(t) + \sin^2(t) = 1$; 

* $\cos(x + y) = \cos(x)\cos(y) - \sin(x)\sin(y)$ and $\sin(x + y) = \sin(x)\cos(y) + \cos(x)\sin(y)$ ("addition formulas"), by taking real and imaginary parts of the identity that says $\exp$ is a homomorphism; 

* $(\sin)' = \cos$ and $(\cos)' = -\sin$ (by [[differentiation|differentiating]] $\exp(i t)$); the connection with the arc length parametrization of the unit circle is that the derivative of the position vector $p'(t) = (\exp(i t))'$ is a velocity vector $i\exp(i t)$ of unit length; 

* $\cos(x + 2\pi) = \cos(x)$ and $\sin(x+2\pi) = \sin(x)$ ("[[periodicity]]"), according to the modern definition of [[pi]]; 

* $\cos(x) = \sum_{n \geq 0} (-1)^n \frac{x^{2 n}}{(2 n)!}$ and $\sin(x) = \sum_{n \geq 0} (-1)^n \frac{x^{2 n + 1}}{(2 n + 1)!}$, by exploiting the power series representation of the exponential function. 

These name but a few of many [[trigonometric identities]], facility in which can serve as a modern-day shibboleth or barrier of passage in high school or lower-level undergraduate courses in mathematics. They seem also to be popular in mathematics education in India and appear regularly in entrance examinations there. But the ones listed above are the most fundamental. 

There is no question that the trigonometric functions are rich in significance; for example; various representations of the tangent, cotangent, secant, etc. appear in [[enumerative combinatorics]] (as in the problem of counting alternating [[permutations]]), representations of [[Bernoulli numbers]], and so on. 

## Related concepts

* [[inverse trigonometric function]]

* [[trigonometry]]

* [[trigonometric identity]]

* [[hyperbolic function]] 

* [[elliptic function]] 

## References

* Wikipedia, _[Trigonometric function](https://en.wikipedia.org/wiki/Trigonometric_functions)_

* Springer [[eom]]: V.I. Bityutskov, _[Trigonometric functions](http://www.encyclopediaofmath.org/index.php?title=Trigonometric_functions&oldid=14919)_

[[!redirects trigonometric functions]]