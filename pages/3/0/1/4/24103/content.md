
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

### Without scalar coefficients

A **real polynomial function** is a [[polynomial function]] in the [[real numbers]], a [[function]] $f:\mathbb{R} \to \mathbb{R}$ such that 

* $f$ is in the image of the [[function]] $j:\mathbb{R}^* \to (\mathbb{R} \to \mathbb{R})$ from the [[free monoid]] $\mathbb{R}^*$ on $\mathbb{R}$, i.e. the set of lists of real numbers, to the [[function algebra]] $\mathbb{R} \to \mathbb{R}$, such that 

  * $j(\epsilon) = 0$, where $0$ is the zero function. 
  * for all $a \in \mathbb{R}^*$ and $b \in \mathbb{R}^*$, $j(a b) = j(a) + j(b) \cdot (-)^{\mathrm{len}(a)}$, where $(-)^n$ is the $n$-th power function for $n \in \mathbb{N}$
  * for all $r \in \mathbb{R}$, $j(r) = c_r$, where $c_r$ is the constant function whose value is always $r$. 

* $f$ is in the image of the canonical [[ring homomorphism]] $i:\mathbb{R}[x] \to (\mathbb{R} \to \mathbb{R})$ from the real polynomial ring in one indeterminant $\mathbb{R}[x]$ to the [[function algebra]] $\mathbb{R} \to \mathbb{R}$, which takes constant polynomials in $\mathbb{R}[x]$ to constant functions in $\mathbb{R} \to \mathbb{R}$ and the indeterminant $x$ in $\mathbb{R}[x]$ to the identity function $\mathrm{id}_\mathbb{R}$ in $\mathbb{R} \to \mathbb{R}$

* There exists a natural number $n$ such that the $n$-th order derivative of $f$ is equal to the zero function: 
$$\frac{d^n f}{d x^n} = 0$$ 

### With scalar coefficients

A **real polynomial function** is a [[function]] $f:\mathbb{R} \to \mathbb{R}$ with a [[natural number]] $n \in \mathbb{N}$ and a [[list]] of length $n$ of real numbers $a:[0, n)_\mathbb{N} \to \mathbb{R}$ which satisfy one of these conditions:

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

#### Without scalar coefficients

Given a non-zero real polynomial function $f:\mathbb{R} \to \mathbb{R}$, the **degree** of $f$ is the maximum [[natural number]] $n$ where the $n$-th [[derivative]] of $f$ is not the zero-function:
$$\mathrm{deg}(f) \coloneqq \max_{n \in \mathbb{N}, \frac{d^{n} f}{d x^{n}} \neq 0}(n)$$

#### With scalar coefficients

The **degree** of a real polynomial function, with additional data of a [[natural number]] $n \in \mathbb{N}$ and a [[list]] of length $n$ of real numbers $a:[0, n)_\mathbb{N} \to \mathbb{R}$, is defined as the maximum natural number $i \lt n$ such that $\vert a_i \vert \gt 0$. 

#### In constructive mathematics

In [[constructive mathematics]], there exist real polynomial functions for which one cannot prove that a particular natural number $i \lt n$ is the degree of the real polynomial function: i.e. the [[function algebra|function sub-$\mathbb{R}$-algebra]] of real polynomial functions is not a [[Euclidean domain]]. 

### Pointwise continuity ###

Given a [[real polynomial function]] $f:\mathbb{R} \to \mathbb{R}$, $f$ is a [[pointwise continuous function]] with respect to its [[metric topology]] defined through the absolute value function, subtraction, and its strict total order. 

### Pointwise differentiability ###

Given a [[real polynomial function]] $f:\mathbb{R} \to \mathbb{R}$, $f$ is a [[pointwise differentiable function]] with respect to its [[metric topology]] defined through the absolute value function, subtraction, and its strict total order. 

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
