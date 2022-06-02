
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

A **real polynomial function** is a [[polynomial function]] in the [[real numbers]], a [[function]] $f:\mathbb{R} \to \mathbb{R}$ with a [[natural number]] $n \in \mathbb{N}$ and a [[list]] of length $n$ of real numbers $a:[0, n)_\mathbb{N} \to \mathbb{R}$ which satisfy one of these conditions:

* for all $x \in R$, 
$$f(x) = \sum_{i:[0, n)_\mathbb{N}} a(i) \cdot x^i$$
where $x^i$ is the $i$-th [[power function]] for multiplication. 

* $f$ is a [[solution]] to the $n$-th order linear homogeneous [[ordinary differential equation]] 
$$\frac{d^n f}{d x^n} = 0$$ 
with initial conditions 
$$\frac{d^i f}{d x^i}(0) = i! \cdot a(i)$$
for each natural number $i:[0, n)_\mathbb{N}$

## Properties ##

### Degree ###

The **degree** of a real polynomial function is defined as the maximum natural number $i \lt n$ such that $\vert a_i \vert \gt 0$. In [[constructive mathematics]], there exist real polynomial functions for which one cannot prove that a particular natural number $i \lt n$ is the degree of the real polynomial function: i.e. the [[function algebra|function sub-$\mathbb{R}$-algebra]] of real polynomial functions is not a [[Euclidean domain]]. 

### Pointwise continuity ###

Given a [[real polynomial function]] $f:\mathbb{R} \to \mathbb{R}$, $f$ is a [[pointwise continuous function]] with respect to its [[metric topology]] defined through the absolute value function, subtraction, and its strict linear order. 

### Pointwise differentiability ###

Given a [[real polynomial function]] $f:\mathbb{R} \to \mathbb{R}$, $f$ is a [[pointwise differentiable function]] with respect to its [[metric topology]] defined through the absolute value function, subtraction, and its strict linear order. 

### Smoothness ###

Every real polynomial function is a [[smooth function]]. This could be shown [[coinductively]]: A smooth function is a [[pointwise differentiable function]] whose derivative is also smooth, and thus the $n$-th derivative of a smooth function is a smooth function. The zero function $f(x) = 0$ is a smooth function, every real polynomial function is a pointwise differentiable function and the $n$-th derivative of a polynomial function, with a [[natural number]] $n \in \mathbb{R}$ and a [[list]] of length $n$ of real numbers $a:[0, n)_\mathbb{N} \to \mathbb{R}$ such that one of the two conditions above is satisfied, is the zero function. Thus, every polynomial function is a smooth function. 

## See also ##

* [[real number]]

* [[polynomial function]]

* [[real quadratic function]]

* [[real cubic function]]

* [[rational functions are continuous]]

## References ##

The proof of pointwise continuity using [[epsilontic analysis]] is spelled out for instance in

* Kyle Miller, _Polynomials are continuous functions_, 2014 ([pdf](https://math.berkeley.edu/~kmill/math1afa2014/poly.pdf))

See also:

* Wikipedia, _[Polynomial function](https://en.wikipedia.org/wiki/Polynomial_function)_

[[!redirects real polynomial functions]]

[[!redirects real polynomial functions are pointwise continuous]]
[[!redirects polynomials are continuous functions]]
[[!redirects polynomials are continuous]]
