+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

In the same vein that [[commutative rings]] are to [[integral domains]] and [[GCD rings]] are to [[GCD domains]], [[Bézout rings]] are to [[Bézout domains]].

## Definition ##

A **Bézout ring** is a [[GCD ring]] $R$ which satisfies Bézout's identity for cancellative elements: For every element $a \in \mathrm{Can}(R)$ and $b \in \mathrm{Can}(R)$, there exists elements $x \in R$ and $y \in R$ called Bézout coefficients such that $a \cdot x + b \cdot y = \gcd(a, b)$, where $\gcd(a, b)$ is the [[greatest common divisor]] of $a$ and $b$ and $\mathrm{Can}(R)$ is the [[multiplicative submonoid of cancellative elements]] in $R$.

One could posit, instead of the property that for all elements $a \in \mathrm{Can}(R)$ and $b \in \mathrm{Can}(R)$, there exists elements $x \in R$ and $y \in R$ such that $a \cdot x + b \cdot y = \gcd(a, b)$; that the integral domain has the [[structure]] of Bézout coefficient functions $\beta_0:\mathrm{Can}(R) \times \mathrm{Can}(R) \to R$ and $\beta_1:\mathrm{Can}(R) \times \mathrm{Can}(R) \to R$ such that for every cancellative element $a \in \mathrm{Can}(R)$ and $b \in \mathrm{Can}(R)$, $a \cdot \beta_0(a, b) + b \cdot \beta_1(a, b) = \gcd(a, b)$. 

## Properties ##

Every Bézout ring is a [[GCD ring]], and every [[Euclidean ring]] is a Bézout ring. 

## Examples ##

* The [[integers]] $\mathbb{Z}$ are a Bézout ring. 

* A classical Bézout domain $A$ is a Bézout ring where $\mathrm{Can}(A)$ is the multiplicative monoid of elements not equal to zero (where inequality is [[denial inequality]])

$$\mathrm{Can}(A) \cong \{x \in A \vert x \neq 0\}$$

* A Heyting Bézout domain $A$ is a Bézout ring where $\mathrm{Can}(A)$ is the multiplicative monoid of elements apart from zero

$$\mathrm{Can}(A) \cong \{x \in A \vert x \# 0\}$$

* An ordered Bézout domain $A$ is a Bézout ring where $\mathrm{Can}(A)$ is the multiplicative monoid of elements with a positive absolute value

$$\mathrm{Can}(A) \cong \{x \in A \vert 0 \lt \vert x \vert\}$$

* The [[trivial ring]] $0$ is the unique Bézout ring up to unique [[isomorphism]] such that $0 \in \mathrm{Can}(0)$. The [[trivial ring]] is also the [[terminal object|terminal]] Bézout ring. 

## See also ##

* [[commutative ring]]

* [[Euclidean ring]]

* [[GCD ring]]

* [[prefield]]

* [[Bézout domain]]

[[!redirects Bézout rings]]

[[!redirects Bezout ring]]
[[!redirects Bezout rings]]