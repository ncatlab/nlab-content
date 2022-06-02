
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

A **real quadratic function** is a [[quadratic function]] in the [[real numbers]]. Equivalently, it is a [[solution]] to the third-order linear homogeneous [[ordinary differential equation]] 
$$\frac{d^3 f}{d x^3} = 0$$ 
with initial conditions 
$$f(0) = c$$ 
$$\frac{d f}{d x}(0) = b$$
$$\frac{d^2 f}{d x^2}(0) = 2 a$$

## Properties ##
 {#Properties}

### Extrema ###

Given a real quadratic function $f(x) \coloneqq a x^2 + b x + c$, if $\vert a \vert \gt 0$, after [[completing the square]], the quadratic function may be written as 

$$
  f(x) = a \left(x + \frac{b}{2a}\right)^2 - \frac{b^2 - 4 a c}{4a}
$$

The [[extremum]] occurs at 

$$x = -\frac{b}{2a}$$

and the extremum is a [[minimum]] if $a \gt 0$ and a [[maximum]] if $a \lt 0$. The value of $f$ at the extremum is 

$$f(x) = \frac{4 a c - b^2}{4a}$$

When $a \gt 0$, the real quadratic function is said to be concave up, while when $a \lt 0$, the real quadratic function is said to be concave down. 

If $a = 0$, the real quadratic function is [[degenerate]]; it becomes a real [[affine function]]. 

### In constructive mathematics ###

In [[classical mathematics]], the [[linear order|law of trichotomy]] holds in the real numbers, so the three cases above cover every real number. However, in [[constructive mathematics]], trichotomy does not hold in the real numbers, and as a result, there exists real quadratic functions $f:\mathbb{R} \to \mathbb{R}$ such that one cannot decide whether $f$ is concave up, concave down, or degenerate. Similarly, there exists real quadratic functions $f:\mathbb{R} \to \mathbb{R}$ such that one cannot decide whether the extremum is a minimum, is a maximum, or does not exist due to the degeneracy of $f$. 

## Exact zeroes ##

### Partial inverse functions ###

Given a real quadratic function $f:\mathbb{R} \to \mathbb{R}$, $f(x) \coloneqq a x^2 + b x + c$ for real numbers $a \in \mathbb{R}$, $b \in \mathbb{R}$, $c \in \mathbb{R}$ such that $\vert a \vert \gt 0$, there are two branches of the partial inverse function of $f$, $g$ and $h$, such that if $a \gt 0$, then $g$ and $h$ have domain 

$$\left(c - \frac{b^2}{4a}, \infty\right)$$

and if $a \lt 0$, $g$ and $h$ have domain 

$$\left(-\infty,c - \frac{b^2}{4a}\right)$$ 

In both cases, $g$ and $h$ are defined as solutions to the first-order nonlinear [[ordinary differential equation]]

$$(2 a F + b) \frac{d F}{d x} = 1$$

with the initial conditions for the principal branch $g$ are

$$g\left((a + b + c) + \left(c - \frac{b^2}{4a}\right)\right) = 1 - \frac{b}{2a}$$

and the initial conditions for the reflected branch $h$ are

$$h\left((a - b + c) + \left(c - \frac{b^2}{4a}\right)\right) = -1 - \frac{b}{2a}$$

As a result, $g$ and $h$ are automatically pointwise [[smooth functions]], and in fact [[analytic functions]], and for every $x$ in the domain of $g$ and $h$,

$$g(x) \gt -\frac{b}{2a}$$ 

$$h(x) \lt -\frac{b}{2a}$$ 

Since this differential equation is separable, one could use separation of variables to see that $g$ and $h$ satisfy the [[functional equations]] $a g(x)^2 + b g(x) + c = x$ and $a h(x)^2 + b h(x) + c = x$. 

If the discriminant $\Delta = b^2 - 4 a c$ is greater than zero $\Delta \gt 0$, then the quadratic function $f$ has two zeroes apart from each other. The larger of the two zero of $f(x)$ is at $g(0)$ and the smaller zero of $f(x)$ is at $h(0)$. If the discriminant is less than or equal to zero $\Delta \leq 0$, then zero isn't in the domain of either $g$ and $h$. 

+-- {: .query}
This is overkill, one could use the [[inverse function theorem]] which only requires the quadratic function to be continuously differentiable at real numbers apart from the extrema, and the real numbers to be sequentially Cauchy complete, provable from the [[Banach fixed point theorem]] in the real numbers. 
=--

### Square roots ###

If $a = 1$, $b = 0$, and $c = 0$, then the real quadratic function above is the square function $f(x) \coloneqq x^2$. The principal branch of the smooth partial inverse function of the square function is called the [[smooth principal square root]] or [[analytic principal square root]] $\mathrm{sqrt}_\mathrm{sm}:(0, \infty) \to \mathbb{R}$, and is the solution to the differential equation 

$$(2 \mathrm{sqrt}_\mathrm{sm}) \frac{d \mathrm{sqrt}_\mathrm{sm}}{d x} = 1$$

with initial condition $\mathrm{sqrt}_\mathrm{sm}(1) = 1$. The reflected branch of the smooth partial inverse function of the square function is simply the negation of the principal square root $-\mathrm{sqrt}_\mathrm{sm}:(0, \infty) \to \mathbb{R}$. 

### Quadratic formula ###

For any quadratic function $f$, the principal branch of its inverse has a canonical definition in terms of the smooth principal square root:

$$g(x) = \frac{-b + \mathrm{sqrt}_\mathrm{sm}(4ax + b^2 - 4ac)}{2a}$$

and the reflected branch has a canonical definition in terms of the smooth principal square root as well:

$$h(x) = \frac{-b - \mathrm{sqrt}_\mathrm{sm}(4ax + b^2 - 4ac)}{2a}$$

The **smooth quadratic formula** or **analytic quadratic formula** is the evaluation of the two branches at zero, if zero is in the domain of $g$ and $h$:

$$g(0) = \frac{-b + \mathrm{sqrt}_\mathrm{sm}(b^2 - 4ac)}{2a}$$

$$h(0) = \frac{-b - \mathrm{sqrt}_\mathrm{sm}(b^2 - 4ac)}{2a}$$

The smooth quadratic formula is only valid for real quadratic functions with positive discriminant, unlike the [[quadratic formula]] in the [[discrete field]] of [[quadratic irrational numbers]], which is valid for [[quadratic functions]] with [[rational number|rational]] [[coefficients]] and a non-negative discriminant. But there's an analytic reason for why the quadratic formula should be restricted to real quadratic functions with positive discriminant: for any real quadratic function $f$ with a non-positive discriminant $\Delta \leq 0$, there is no interval on the real numbers such that the conditions required for the [[intermediate value theorem]] are fulfilled: if $a \gt 0$, then $f(x) \geq 0$ for all real numbers $x$, and if $a \lt 0$, then $f(x) \leq 0$ for all real numbers $x$. 

### Negative and zero discriminant ###

As stated above, when a real quadratic function $f$ has a non-positive discriminant, $\Delta \leq 0$, if $a \gt 0$, then $f(x) \geq 0$ for all real numbers $x$, and if $a \lt 0$, then $f(x) \leq 0$ for all real numbers $x$. When $f$ has a negative discriminant, $\Delta \lt 0$, then $f$ is provably always [[tight apartness relation|apart]] from zero: if $a \gt 0$, then $f(x) \gt 0$ for all real numbers $x$, and if $a \lt 0$, then $f(x) \lt 0$ for all real numbers $x$. As a result, $f$ has no zeroes in the real numbers if the determinant of $f$ is negative. 

Now, suppose that $f$ has zero discriminant. This means that $b^2 - 4ac = 0$, and after [[completing the square]], the resulting function is equal to 

$$f(x) = a \left(x + \frac{b}{2a}\right)^2$$

By definition of an [[ordered field]], there are no multiplicative [[nilpotent elements]] in the real numbers whose absolute value is greater than zero, and thus every nilpotent element is equal to zero. As a result, 

$$f(x) = a \left(x + \frac{b}{2a}\right)^2 = 0$$

$$\left(x + \frac{b}{2a}\right)^2 = 0$$

$$x + \frac{b}{2a} = 0$$

$$x = -\frac{b}{2a}$$

There is only one zero, which occurs at the [[extremum]] of the real quadratic function. 

### In constructive mathematics ###

In [[classical mathematics]], the [[linear order|law of trichotomy]] holds in the real numbers, so the three cases above cover every real number. However, in [[constructive mathematics]], trichotomy does not hold in the real numbers, and as a result, there exists real quadratic functions $f:\mathbb{R} \to \mathbb{R}$ such that one cannot decide whether the discriminant of $f$ is positive, negative, or zero. As a result, there exist real quadratic functions where one cannot decide the number of zeroes the function has. Furthermore, one cannot prove that a real quadratic function with positive determinant has exactly two zeroes. 

## Newton's method ##

Given a real quadratic function $f:\mathbb{R} \to \mathbb{R}$, $f(x) \coloneqq a x^2 + b x + c$ for real numbers $a \in \mathbb{R}$, $b \in \mathbb{R}$, $c \in \mathbb{R}$, where $\vert a \vert \gt 0$, suppose we want to approximate a zero of $f$. There is an algorithm called **[[Newton's method]]** which would allow us to do so. The real quadratic function has [[discriminant]] $\Delta = b^2 - 4 a c$ and has 2 zeroes if $\Delta \gt 0$, 1 zero at the extremum if $\Delta = 0$, or no zeroes of $\Delta \lt 0$. (In [[constructive mathematics]], there are real quadratic functions where it isn't possible to determine the number of zeroes the real quadratic function has.)

Assume that $\Delta \gt 0$. Select a real number $x_0 \in \mathbb{R}$ as the initial guess, where $2 a x_0 + b \gt 0$ or $2 a x_0 + b \lt 0$, and the next guess would be defined as 

$$x_{i+1} = x_i - \frac{a x_i^2 + b x_i + c}{2 a x_i + b}$$

Newton's method isn't valid when $2 a x_0 + b = 0$ because of division by zero. When $2 a x_0 + b \gt 0$, Newton's method converges towards the zero at $x \gt -\frac{b}{2a}$, and when $2 a x_0 + b \lt 0$, Newton's method converges towards the zero $x \lt -\frac{b}{2a}$. 

## See also ##

* [[real number]]

* [[quadratic function]]

* [[quadratic formula]]

* [[real square root]]

* [[real cubic function]]

* [[real polynomial function]]

## References ##

See also:

* Wikipedia, _[Quadratic function](https://en.wikipedia.org/wiki/Quadratic_function)_

[[!redirects real quadratic functions]]

[[!redirects real quadratic formula]]
[[!redirects smooth quadratic formula]]
[[!redirects analytic quadratic formula]]
