+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Arithmetic
+-- {: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition ##

### For polynomial functions ###
The **rational zero theorem** or **rational root theorem** states:

Given a [[natural number]] $n$ and a degree $n$ [[polynomial function]] $f \colon \mathbb{Q} \to \mathbb{Q}$ on the [[rational numbers]] with [[integers]] valued [[coefficients]] $a \colon [0,n] \to \mathbb{Z} \hookrightarrow \mathbb{Q}$ and $a_n \neq 0$, defined as

$$
  f(x) \coloneqq \sum_{i = 0}^{n} a_i \, x^i
  \,,
$$

then the [[fiber]] of $f$ at $0$ is [[inhabited set|inhabited]] if one of the following is true:

* $a_0 = 0$,

* $a_0 \neq 0$ and there exists integers $m$ and $p$ such that $gcd(\vert m \vert, \vert p \vert) = 1$, $m \vert a_0$, and $p \vert a_n$. 

### For polynomials ###
The **rational root theorem for polynomials** states:

Given a natural number $n$ and a degree $n$ univariate [[polynomial]] on the [[rational numbers]] $a:\mathbb{Q}[x]$ where $a_{n} = 1$, there exists a degree $1$ univariate polynomial $b:\mathbb{Q}[x]$ where $b_{1} = 1$ such that $b | a$ if and only if there exists an integer $m$ such that $gcd(\vert m \vert, \vert b_0 \vert) = 1$ and $m \cdot a_0 = b_0$. 

## See also ##

* [[Gauss's lemma for polynomials]]
* [[polynomial function]]
* [[rational numbers]]
* [[integers]]

## References ##

* Wikipedia, _[Rational zero theorem](https://en.wikipedia.org/wiki/Rational_zero_theorem)_

[[!redirects rational root theorem]]