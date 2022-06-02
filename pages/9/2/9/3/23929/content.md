
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

A **real cubic function** is a [[cubic function]] in the [[real numbers]]. Equivalently, it is a [[solution]] to the fourth-order linear homogeneous [[ordinary differential equation]] 
$$\frac{d^4 f}{d x^4} = 0$$ 
with initial conditions 
$$f(0) = d$$ 
$$\frac{d f}{d x}(0) = c$$
$$\frac{d^2 f}{d x^2}(0) = 2 b$$
$$\frac{d^3 f}{d x^3}(0) = 6 a$$

## Properties ##

### Extrema ###

The [[derivative]] of a real cubic function $f:\mathbb{R} \to \mathbb{R}$, $f(x) \coloneqq a x^3 + b x^2 + c x + d$ for real numbers $a \in \mathbb{R}$, $b \in \mathbb{R}$, $c \in \mathbb{R}$, $d \in \mathbb{R}$ is the function $\delta_x f:\mathbb{R} \to \mathbb{R}$, $\delta_x f(x) \coloneqq 3a x^2 + 2b x + c$. The discriminant of the derivative is given by $\Delta_\partial = (2b)^2 - 4 (3a) c = 4b^2 - 12a c$. If the discriminant of the derivative is positive $\Delta_\partial \gt 0$, then there are two local extrema in the cubic function. Otherwise, $f$ is [[monotonic]] on the entire domain of $a \gt 0$, or [[antitonic]] on the entire domain if $a \lt 0$. 

Using the [[smooth quadratic formula]], we find that for positive discriminant the two extrema are located at 

$$x_1 = \frac{-2b + \mathrm{sqrt}_\mathrm{sm}(4b^2 - 12a c)}{6a} = \frac{-2b + 2 \mathrm{sqrt}_\mathrm{sm}(b^2 - 3a c)}{6a} = \frac{-b + \mathrm{sqrt}_\mathrm{sm}(b^2 - 3a c)}{3a}$$

$$x_2 = \frac{-2b - \mathrm{sqrt}_\mathrm{sm}(4b^2 - 12a c)}{6a} = \frac{-2b - 2 \mathrm{sqrt}_\mathrm{sm}(b^2 - 3a c)}{6a} = \frac{-b - \mathrm{sqrt}_\mathrm{sm}(b^2 - 3a c)}{3a}$$

For negative discriminant, there is no extrema. For zero discriminant, there is a [[saddle point]] at 

$$x = -\frac{b}{3a}$$  

If $a = 0$, the real cubic function is [[degenerate]]; it becomes a [[real quadratic function]]. 

### Inflection point ###

THe inflection point of the real cubic function $f:\mathbb{R} \to \mathbb{R}$, $f(x) \coloneqq a x^3 + b x^2 + c x + d$ for real numbers $a \in \mathbb{R}$, $b \in \mathbb{R}$, $c \in \mathbb{R}$, $d \in \mathbb{R}$ occurs at the zero of the second derivative of $f$: 

$$\partial_x f(x) = 6 a x + 2b = 0$$

which occurs at 

$$x = -\frac{b}{3a}$$

The inflection point is to real cubic functions what the extremum was to real quadratic functions. 

### In constructive mathematics ###

In [[classical mathematics]], the [[linear order|law of trichotomy]] holds in the real numbers, so the three cases above cover every real number. However, in [[constructive mathematics]], trichotomy does not hold in the real numbers, and as a result, there exists real cubic functions $f:\mathbb{R} \to \mathbb{R}$ such that one cannot decide whether $f$ has two local extrema, a saddle point, or zero local extrema. Similarly, there exists real cubic functions $f:\mathbb{R} \to \mathbb{R}$ such that one cannot decide whether the inflection point occurs to the left, the right, or on the $y$-intercept line. 

## Depressed cubic functions ##

An unnormalized depressed cubic function is a real cubic function whose inflection point occurs at $x = 0$, and has the canonical form of $g(x) \coloneqq a x^3 + p x + q$, with $\vert a \vert \gt 0$. $g$ is called a depressed cubic function when $a$ is normalized to $1$. 

Every real cubic function $f:\mathbb{R} \to \mathbb{R}$, $f(x) \coloneqq a x^3 + b x^2 + c x + d$ for real numbers $a \in \mathbb{R}$, $b \in \mathbb{R}$, $c \in \mathbb{R}$, $d \in \mathbb{R}$, is a translation of an unnormalized depressed cubic function $g:\mathbb{R} \to \mathbb{R}$ by the equation

$$g(x) = f\left(x - \frac{b}{3a}\right)$$

$$a x^3 + p x + q = a \left(x - \frac{b}{3a}\right)^3 + b \left(x - \frac{b}{3a}\right)^2 + c \left(x - \frac{b}{3a}\right) + d$$

$$a x^3 + p x + q = a x^3 - 3 a \frac{b}{3a} x^2 + 3 a \left(\frac{b}{3a}\right)^2 x - a \left(\frac{b}{3a}\right)^3 + b x^2 - 2 b \frac{b}{3a} x + b \left(\frac{b}{3a}\right)^2 + c x - c \left(\frac{b}{3a}\right) + d$$

$$a x^3 + p x + q = a x^3 + \frac{b^2}{3a} x - \frac{b^3}{27a^2} - \frac{2 b^2}{3a} x + \frac{b^3}{9 a^2} + c x - \frac{b c}{3a} + d$$

$$a x^3 + p x + q = a x^3 + \frac{3a c - b^2}{3a} x + \frac{2 b^3 - 9 a b c + 27 a^2 d}{27a^2}$$

thus, 

$$p = \frac{3a c - b^2}{3a}$$

$$q = \frac{2 b^3 - 9 a b c + 27 a^2 d}{27a^2}$$

### Discriminant ###

The discriminant of an unnormalized depressed cubic function $g(x) \coloneqq a x^3 + p x + q$ is given by 

$$\Delta = -4 p^3 - 27 a q^2$$

Substituting in the values above for $p$ and $q$, the discriminant of a general real cubic function $f:\mathbb{R} \to \mathbb{R}$, $f(x) \coloneqq a x^3 + b x^2 + c x + d$ for real numbers $a \in \mathbb{R}$, $b \in \mathbb{R}$, $c \in \mathbb{R}$, $d \in \mathbb{R}$ is 

$$\Delta = -4 \left(\frac{3a c - b^2}{3a}\right)^3 - 27 a \left(\frac{2 b^3 - 9 a b c + 27 a^2 d}{27a^2}\right)^2 = \frac{4(b^2 - 3a c)^3 - (2 b^3 - 9 a b c + 27 a^2 d)^2}{27 a^3}$$

## Exact zeroes ##

### Partial inverse functions ###

Given a real cubic function $f(x) \coloneqq a x^3 + b x^2 + c x + d$ for real numbers $a \in \mathbb{R}$, $b \in \mathbb{R}$, $c \in \mathbb{R}$, $d \in \mathbb{R}$ such that $\vert a \vert \gt 0$, the following cases are possible: 

* If the discriminant of the derivative of $f$ is positive, $\Delta_\partial \gt 0$, then there are three branches of the partial inverse function of $f$.

* If the discriminant of the derivative of $f$ is zero, $\Delta_\partial = 0$, then there are two branches of the partial inverse function of $f$.

* If the discriminant of the derivative of $f$ is negative, $\Delta_\partial \lt 0$, then there is only one branch of the partial inverse function of $f$.

In all cases, the partial inverse functions are solutions of the first-order nonlinear [[ordinary differential equation]]

$$(3 a F^2 + 2 b F + c) \frac{d F}{d x} = 1$$

with specific initial conditions. 

## See also ##

* [[real number]]

* [[cubic function]]

* [[real quadratic function]]

* [[real polynomial function]]

## References ##

See also:

* Wikipedia, _[Cubic function](https://en.wikipedia.org/wiki/Cubic_function)_
* Wikipedia, _[Cubic equation](https://en.wikipedia.org/wiki/Cubic_equation)_

[[!redirects real cubic functions]]