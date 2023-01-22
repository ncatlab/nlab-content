\tableofcontents

## Idea

The generalization of [[square-free integer]] and [[square-free polynomial]] to arbitrary [[unique factorization domains]]. 

## Definition

Let $R$ be a [[unique factorization domain]]. An element $r \in R$ is **square-free** if for all [[irreducible elements]] $x \in R$, $r$ is not in the [[ideal]] $x^2 R$. 

## Examples

* A [[square-free integer]] is a square-free element in the integers $\mathbb{Z}$. 

* Let $F$ be a [[discrete field]] and let $\overline{F}$ be the [[algebraic closure]] of $F$. A univariate [[square-free polynomial]] with coefficients in $\overline{F}$ is a square-free element in the polynomial ring $\overline{F}[x]$. 

## Properties

Given a [[unique factorization domain]] $R$ such that for every [[irreducible element]] $p \in R$, the [[ideal]] $p R$ is a [[maximal ideal]], and a square-free element $x \in R$, the [[quotient ring]] $R/x R$ is a [[reduced ring]]. Since for every non-zero element $r \in R$, $R/x R$ is a [[prefield ring]], $R/x R$ is an [[integral domain]] and thus a [[field]] if and only if $x$ is an [[irreducible element]] in $R$.  

## Square-free factorization

Given a non-zero element of a [[unique factorization domain]] $r \in R$, the **square-free factorization** or **square-free decomposition** of $r$ is a factorization of $r$ into powers of square-free elements $r_i$

$$r = \prod_{i = 0}^{n} r_i^i$$

where each of the elements $r_i$ are pairwise [[coprime]] and not in the [[group of units]]. 

## See also

* [[square-free integer]] 

* [[square-free polynomial]]