#Contents#
* automatic table of contents goes here
{:toc}

## Definition 

An [[ordered field]] $F$ is **real closed** if it satisfied the following two properties: 

* Any positive element $x \gt 0$ in $F$ is a square of an element in $F$; 

* Any odd degree polynomial with coefficients in $F$ has a root in $F$. 

Notice that the order on a real closed field is definable from the algebraic structure: $x \leq y$ if and only if $\exists_z x + z^2 = y$. Thus the category of real closed fields is a full subcategory of the category of [[field]]s. 

## Properties 

Real closed fields can be equivalently characterized by any of the following properties: 

1. $F$ is not algebraically closed, but some finite extension is. This extension is necessarily $F[\sqrt{-1}]$. See also [[fundamental theorem of algebra]]. 

1. As a field, $F$ is [[elementary equivalence|elementarily equivalent]] to the field of real numbers. 

1. The [[intermediate value theorem]] holds for all polynomials with coefficients in $F$. 

1. $F$ is an ordered field that has no ordered algebraic extension. 

+-- {: .query}
Colin: Is it true that real closure is an adjoint construction to the forgetful functor from real closed fields to orderable fields?
=--

## Examples 

1. The [[real number]]s form a real closed field. 

1. Real [[algebraic number]]s form a real closed field. 

1. A field of nonstandard real numbers (as in Robinson [[nonstandard analysis]]) is real closed. 

1. [[surreal number|Surreal numbers]] form a (large) real closed field. 

1. If $F$ is real closed, then the field of [[Puiseux series]] over $F$ is also real closed. 

1. More generally, given a real closed field $F$, the field of [[Hahn series]] over $F$ with [[valuation ring|value group]] $G$ (an ordered group) is real closed provided that $G$ is divisible. 

1. Any [[o-minimal structure|o-minimal]] ordered ring structure $R$ is a real closed field. 

1. Given an o-minimal ordered ring $R$, the field of [[germ]]s at infinity of definable functions $R \to R$ in any o-minimal expansion of $(R, 0, 1, +, -, \cdot, \lt)$ is real closed. (By "germ at infinity", we mean an equivalence class of functions for which $f \equiv g$ if and only if $f(x) = g(x)$ for all sufficiently large $x$.)
