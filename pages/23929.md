
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition ##

A **real cubic function** is a [[cubic function]] in the [[real numbers]]. 

## Properties ##

### Extrema ###

The [[derivative]] of a real cubic function $f:\mathbb{R} \to \mathbb{R}$, $f(x) \coloneqq a x^3 + b x^2 + c x + d$ for real numbers $a \in \mathbb{R}$, $b \in \mathbb{R}$, $c \in \mathbb{R}$, $d \in \mathbb{R}$ is the function $\delta_x f:\mathbb{R} \to \mathbb{R}$, $\delta_x f(x) \coloneqq 3a x^2 + 2b x + c$. The discriminant of the derivative is given by $\Delta_\partial = (2b)^2 - 4 (3a) c = 4b^2 - 12a c$. If the discriminant of the derivative is positive $\Delta_\partial \gt 0$, then there are two local extrema in the cubic function. Otherwise, $f$ is [[monotonic]] on the entire domain of $a \gt 0$, or [[antitonic]] on the entire domain if $a \lt 0$. 

Using the [[smooth quadratic formula]], we find that for positive discriminant the two extrema are located at 

$$x_1 = \frac{-2b + \mathrm{sqrt}_\mathrm{sm}(4b^2 - 12a c)}{6a} = \frac{-2b + 2 \mathrm{sqrt}_\mathrm{sm}(b^2 - 3a c)}{6a} = \frac{-b + \mathrm{sqrt}_\mathrm{sm}(b^2 - 3a c)}{3a}$$

$$x_2 = \frac{-2b - \mathrm{sqrt}_\mathrm{sm}(4b^2 - 12a c)}{6a} = \frac{-2b - 2 \mathrm{sqrt}_\mathrm{sm}(b^2 - 3a c)}{6a} = \frac{-b - \mathrm{sqrt}_\mathrm{sm}(b^2 - 3a c)}{3a}$$

For negative discriminant, there is no extrema. For zero discriminant, there is a [[saddle point]] at 

$$x = -\frac{b}{3a}$$  

### Inflection point ###

The inflection point is to real cubic functions what the extremum was to real quadratic functions. 

### Discriminant ###

A real cubic function $f:\mathbb{R} \to \mathbb{R}$, $f(x) \coloneqq a x^3 + b x^2 + c x + d$ for real numbers $a \in \mathbb{R}$, $b \in \mathbb{R}$, $c \in \mathbb{R}$, $d \in \mathbb{R}$, has [[discriminant]] $\Delta = 18 a b c d - 4 b^3 d + b^2 c^2 - 4 a c^3 - 27a^2 d^2$. 

### In constructive mathematics ###

In [[classical mathematics]], the [[linear order|law of trichotomy]] holds in the real numbers, so the three cases above cover every real number. However, in [[constructive mathematics]], trichotomy does not hold in the real numbers, and as a result, there exists real cubic functions $f:\mathbb{R} \to \mathbb{R}$ such that one cannot decide whether $f$ has two local extrema, a saddle point, or zero local extrema. Similarly, there exists real cubic functions $f:\mathbb{R} \to \mathbb{R}$ such that one cannot decide whether the local minimum occurs before or after the local maximum with respect to the order $\lt$ in the domain, or does not exist due to the degeneracy of $f$. 

## See also ##

* [[real number]]

* [[cubic function]]

* [[real quadratic function]]

## References ##

See also:

* Wikipedia, _[Cubic function](https://en.wikipedia.org/wiki/Cubic_function)_
* Wikipedia, _[Cubic equation](https://en.wikipedia.org/wiki/Cubic_equation)_

[[!redirects real cubic functions]]