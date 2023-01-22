\tableofcontents

## Definition

Given a [[field]] $K$ and a [[polynomial]] $p \in K[x]$, a **polynomial modulo $p$** is an element of the [[quotient ring]] $q \in K[x]/p K[x]$. The quotient ring itself is called the **ring of polynomials modulo $p$**.  

## Examples

* The [[Gaussian rationals]] are the rational polynomials $\mathbb{Q}[x]$ modulo $x^2 + 1$. 

* The [[complex numbers]] are the real polynomials $\mathbb{R}[x]$ modulo $x^2 + 1$. 

* The [[dual numbers]] are the real polynomials $\mathbb{R}[x]$ modulo $x^2$. 

## Properties

If $p$ is an [[irreducible element]] in $K[x]$, then the quotient ring $K[x]/p K[x]$ is a [[field]]. 

If $p^n$ is a power of an [[irreducible element]] $p \in K[x]$, then the quotient ring $K[x]/p^n K[x]$ is a [[local ring]]. 

Given an [[irreducible element]] $p \in K[x]$, one could construct the [[completion of a ring]]

$$K[x]_p \coloneqq \underset{n \to \infty}\mathrm{colim} K[x]/p^n K[x]$$

which is a [[discrete valuation ring]], a [[local integral domain]] with a [[Dedekind-Hasse norm]]. In particular, if $p = x - a$ is a [[monic polynomial]] of [[degree of a polynomial|degree]] one with $a \in K$ a constant, then $K[x]_{x - a} \coloneqq K[[x - a]]$ is the ring of [[formal power series]] expanded around $a$. 

If $p$ is a [[square-free element]] of $K[x]$, then the quotient ring $K[x]/p K[x]$ is a [[reduced ring]]. 

In general, the quotient ring $K[x]/p K[x]$ is a [[prefield ring]], whose [[monoid of regular elements]] are the [[equivalence class]] of polynomials $q$ modulo $p$ such that the [[greatest common divisor]] is in the [[group of units]] of the polynomial ring. 

$$\gcd(p, q) \in K[x]^\times$$

## See also

* [[integers modulo n]]

## References

* Garrett Sobczyk, *New Foundations in Mathematics: The Geometric Concept of Number*. (doi:10.1007/978-0-8176-8385-6)