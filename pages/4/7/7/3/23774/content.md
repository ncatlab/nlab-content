
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

Given a real quadratic function $f:\mathbb{R} \to \mathbb{R}$, $f(x) \coloneqq a x^2 + b x + c$ for real numbers $a \in \mathbb{R}$, $b \in \mathbb{R}$, $c \in \mathbb{R}$ such that $\vert a \vert \gt 0$, as shown above

$$
  f(x) = a \left(x + \frac{b}{2a}\right)^2 - \frac{b^2 - 4 a c}{4a}
$$

The [[exponential function]] $\exp:\mathbb{R} \to (0, \infty) \hookrightarrow \mathbb{R}$ and [[natural logarithm]] $\ln:(0, \infty) \to \mathbb{R}$ are well defined and are [[inverse functions]] of each other. The square function could be defined on the open interval $(0, \infty)$ as $x^2 = \exp(2 \ln(x))$ and on the open interval $(-\infty, 0)$ as $x^2 = \exp(2 \ln(-x))$. Substituting these definitions into the above formula for the quadratic function results in the following: 

$$
  f(x) = 
\begin{cases}
a \exp\left(2 \ln \left(x + \frac{b}{2a}\right)\right) - \frac{b^2 - 4 a c}{4a} & x \gt -\frac{b}{2a} \\
a \exp\left(2 \ln \left(-\left(x + \frac{b}{2a}\right)\right)\right) - \frac{b^2 - 4 a c}{4a} & x \lt -\frac{b}{2a}
\end{cases}
$$

Suppose that $x \gt -\frac{b}{2a}$. Then the partial inverse function of the right branch of $x^2$, denoted as $g$, is given by the functional equation 

$$x = a \exp\left(2 \ln\left(g(x) + \frac{b}{2a}\right)\right) - \frac{b^2 - 4 a c}{4a}$$

$$x + \frac{b^2 - 4 a c}{4a} = a \exp\left(2 \ln\left(g(x) + \frac{b}{2a}\right)\right)$$

$$\frac{x}{a} + \frac{b^2 - 4 a c}{4a^2} = \frac{4 a x + b^2 - 4 a c}{4a^2} = \exp\left(2 \ln\left(g(x) + \frac{b}{2a}\right)\right)$$

$$\ln\left(\frac{4 a x + b^2 - 4 a c}{4a^2}\right) = \ln(4 a x + b^2 - 4 a c) - 2 \ln(2a) = 2 \ln\left(g(x) + \frac{b}{2a}\right)$$

$$\frac{1}{2} \ln(4 a x + b^2 - 4 a c) - \ln(2a) = \ln\left(g(x) + \frac{b}{2a}\right)$$

$$\exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c) - \ln(2a)\right) = \exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c)\right) \exp(-\ln(2a)) = \frac{1}{2a} \exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c)\right) = g(x) + \frac{b}{2a}$$

$$g(x) = \frac{-b + \exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c)\right)}{2a}$$

Now, suppose that $x \lt -\frac{b}{2a}$. Then the partial inverse function of the left branch of $x^2$, denoted as $h$, is given by the functional equation 

$$x = a \exp\left(2 \ln\left(-\left(h(x) + \frac{b}{2a}\right)\right)\right) - \frac{b^2 - 4 a c}{4a}$$

$$x + \frac{b^2 - 4 a c}{4a} = a \exp\left(2 \ln\left(-\left(h(x) + \frac{b}{2a}\right)\right)\right)$$

$$\frac{x}{a} + \frac{b^2 - 4 a c}{4a^2} = \frac{4 a x + b^2 - 4 a c}{4a^2} = \exp\left(2 \ln\left(-\left(h(x) + \frac{b}{2a}\right)\right)\right)$$

$$\ln\left(\frac{4 a x + b^2 - 4 a c}{4a^2}\right) = \ln(4 a x + b^2 - 4 a c) - 2 \ln(2a) = 2 \ln\left(-\left(h(x) + \frac{b}{2a}\right)\right)$$

$$\frac{1}{2} \ln(4 a x + b^2 - 4 a c) - \ln(2a) = \ln\left(-\left(h(x) + \frac{b}{2a}\right)\right)$$

$$\exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c) - \ln(2a)\right) = \exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c)\right) \exp(-\ln(2a)) = \frac{1}{2a} \exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c)\right) = -\left(h(x) + \frac{b}{2a}\right)$$

$$-\exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c)\right) = h(x) + \frac{b}{2a}$$

$$h(x) = \frac{-b - \exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c)\right)}{2a}$$

If $a \gt 0$, then $g$ and $h$ have domain 

$$\left(c - \frac{b^2}{4a}, \infty\right)$$

and if $a \lt 0$, $g$ and $h$ have domain 

$$\left(-\infty,c - \frac{b^2}{4a}\right)$$ 

### Positive discriminant and the quadratic formula

Provided that zero is in the domain of $g$ and $h$, the **real quadratic formula** is then the evaluation of $g$ and $h$, the two inverse functions of $f$, at zero:

$$g(0) = \frac{-b + \exp\left(\frac{1}{2} \ln(b^2 - 4 a c)\right)}{2a}$$

$$h(0) = \frac{-b - \exp\left(\frac{1}{2} \ln(b^2 - 4 a c)\right)}{2a}$$

\begin{theorem}
Zero is in the domain of $g$ and $h$ if and only if the original real quadratic function $f$ has a positive discriminant. 
\end{theorem}

\begin{proof}
Suppose that zero is in the domain of $g$ and $h$. This means that when $a \gt 0$, $c - \frac{b^2}{4a} \lt 0$, and $b^2 - 4 a c \gt 0$; when $a \gt 0$, $c - \frac{b^2}{4a} \gt 0$, and $b^2 - 4 a c \gt 0$. In both cases, the discriminant $\Delta = b^2 - 4 a c \gt 0$. These algebraic and order theoretic operations are reversible, because $a$ is apart from zero and thus multiplicatively invertible in the real numbers, so the proof runs backwards beginning with a positive discriminant $\Delta = b^2 - 4 a c \gt 0$ and ending with zero being in the domain of $g$ and $h$. Thus, zero is in the domain of $g$ and $h$ if and only if $f$ has a positive discriminant. 
\end{proof}

Thus, the real quadratic formula is only valid for real quadratic functions with positive discriminant. 

### Zero discriminant ###

While the real quadratic formula is only valid for real quadratic functions with positive discriminant, when zero is on the [[boundary]] of the [[open interval]] of the domains of $g$ and $h$ and the discriminant is equal to zero, one could take the limit of the real quadratic formula as the parameter goes to zero and in both cases get 

for $a \gt 0$

$$\lim_{x \to 0^+} g(x) = \lim_{x \to 0^+} \frac{-b + \exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c)\right)}{2a} = - \frac{b}{2a} + \frac{1}{2a} \lim_{x \to 0^+} \exp\left(\frac{1}{2} \ln(4 a x)\right) = -\frac{b}{2a}$$

$$\lim_{x \to 0^+} h(x) = \lim_{x \to 0^+} \frac{-b - \exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c)\right)}{2a} = - \frac{b}{2a} - \frac{1}{2a} \lim_{x \to 0^+} \exp\left(\frac{1}{2} \ln(4 a x)\right) = -\frac{b}{2a}$$

for $a \lt 0$

$$\lim_{x \to 0^-} g(x) = \lim_{x \to 0^-} \frac{-b + \exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c)\right)}{2a} = - \frac{b}{2a} + \frac{1}{2a} \lim_{x \to 0^-} \exp\left(\frac{1}{2} \ln(4 a x)\right) = -\frac{b}{2a}$$

$$\lim_{x \to 0^-} h(x) = \lim_{x \to 0^-} \frac{-b - \exp\left(\frac{1}{2} \ln(4 a x + b^2 - 4 a c)\right)}{2a} = - \frac{b}{2a} - \frac{1}{2a} \lim_{x \to 0^-} \exp\left(\frac{1}{2} \ln(4 a x)\right) = -\frac{b}{2a}$$

Thus, when the discriminant is zero, there is only one zero, which occurs at the [[extremum]] of the real quadratic function. This could also be shown algebraically: 

Suppose that $f$ has zero discriminant. This means that $b^2 - 4ac = 0$, and after [[completing the square]], the resulting function is equal to 

$$f(x) = a \left(x + \frac{b}{2a}\right)^2$$

By definition of an [[ordered field]], there are no multiplicative [[nilpotent elements]] in the real numbers whose absolute value is greater than zero, and thus every nilpotent element is equal to zero. As a result, 

$$f(x) = a \left(x + \frac{b}{2a}\right)^2 = 0$$

$$\left(x + \frac{b}{2a}\right)^2 = 0$$

$$x + \frac{b}{2a} = 0$$

$$x = -\frac{b}{2a}$$

There is only one zero, which occurs at the [[extremum]] of the real quadratic function. 

### Negative discriminant ###

When a real quadratic function $f$ has a negative discriminant, $\Delta \lt 0$, then $f$ is provably always [[tight apartness relation|apart]] from zero: if $a \gt 0$, then $f(x) \gt 0$ for all real numbers $x$, and if $a \lt 0$, then $f(x) \lt 0$ for all real numbers $x$. As a result, $f$ has no zeroes in the real numbers if the discriminant of $f$ is negative. 

### In constructive mathematics ###

In [[classical mathematics]], the [[linear order|law of trichotomy]] holds in the real numbers, so the three cases above cover every real number. However, in [[constructive mathematics]], trichotomy does not hold in the real numbers, and as a result, there exists real quadratic functions $f:\mathbb{R} \to \mathbb{R}$ such that one cannot decide whether the discriminant of $f$ is positive, negative, or zero. As a result, there exist real quadratic functions where one cannot decide the number of zeroes the function has. Furthermore, one cannot prove that a real quadratic function with positive discriminant has exactly two zeroes. 

## Newton's method ##

Given a real quadratic function $f:\mathbb{R} \to \mathbb{R}$, $f(x) \coloneqq a x^2 + b x + c$ for real numbers $a \in \mathbb{R}$, $b \in \mathbb{R}$, $c \in \mathbb{R}$, where $\vert a \vert \gt 0$, suppose we want to approximate a zero of $f$. There is an algorithm called **[[Newton's method]]** which would allow us to do so. The real quadratic function has [[discriminant]] $\Delta = b^2 - 4 a c$ and has 2 zeroes if $\Delta \gt 0$, 1 zero at the extremum if $\Delta = 0$, or no zeroes of $\Delta \lt 0$. (In [[constructive mathematics]], there are real quadratic functions where it isn't possible to determine the number of zeroes the real quadratic function has.)

Assume that $\Delta \gt 0$. Select a real number $x_0 \in \mathbb{R}$ as the initial guess, where $2 a x_0 + b \gt 0$ or $2 a x_0 + b \lt 0$, and the next guess would be defined as 

$$x_{i+1} = x_i - \frac{a x_i^2 + b x_i + c}{2 a x_i + b}$$

Newton's method isn't valid when $2 a x_0 + b = 0$ because of division by zero. When $2 a x_0 + b \gt 0$, Newton's method converges towards the zero at $x \gt -\frac{b}{2a}$, and when $2 a x_0 + b \lt 0$, Newton's method converges towards the zero $x \lt -\frac{b}{2a}$. 

## See also ##

* [[real number]]

* [[quadratic function]]

* [[quadratic formula]]

* [[real square root function]]

* [[real cubic function]]

* [[real polynomial function]]

## References ##

See also:

* Wikipedia, _[Quadratic function](https://en.wikipedia.org/wiki/Quadratic_function)_

[[!redirects real quadratic functions]]

[[!redirects real quadratic formula]]
[[!redirects real quadratic formulae]]
[[!redirects real quadratic formulas]]
[[!redirects continuous quadratic formula]]
[[!redirects continuous quadratic formulae]]
[[!redirects continuous quadratic formulas]]
