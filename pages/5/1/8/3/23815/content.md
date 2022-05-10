
[[!redirects N-graded vector spaces]]

[[!redirects N-graded modules]]
[[!redirects N-graded prevector space]]
[[!redirects N-graded prevector spaces]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A mathematical structure used to define [[geometric algebras]]. 

## Definition ##

Given a [[commutative ring]] $R$ (usually a [[field]] $F$), an **$\mathbb{N}$-graded $R$-module** is an $R$-[[module]] $V$ (usually a [[vector space]] $V$) with a binary function $\langle - \rangle_{(-)}: A \times \mathbb{N} \to V$ called the **grade projection operator** such that

* for all $v:V$ $v = \sum_{n:\mathbb{N}} \langle v \rangle_n$

* for all $a:R$, $b:R$, $v:V$, $w:V$, and $n:\mathbb{N}$, $\langle a v + b w \rangle_n = a \langle v \rangle_n + b \langle w \rangle_n$

* for all $v:V$ and $n:\mathbb{N}$, $\langle \langle v \rangle_n \rangle_n = \langle v \rangle_n$

* for all $v:V$, $m:\mathbb{N}$, and $n:\mathbb{N}$, $(m \neq n) \times (\langle \langle v \rangle_m \rangle_n = 0)$

Terms of $V$ are called **multivectors**. 

For a natural number $n:\mathbb{N}$, the [[image]] of $\langle - \rangle_n$ under $V$ is called the **space of $n$-vectors** and is denoted as $\langle V \rangle_n$. 

$$\langle V \rangle_n \coloneqq \mathrm{im}(\langle - \rangle_n)$$ 

The terms of $\langle V \rangle_n$ are called **$n$-vectors**. 

We define the **n-truncation operator** $\vert - \vert_{(-)}: V \times \mathbb{N}  \to V$

$$\vert v \vert_n = \sum_{m = 0}^n \langle v \rangle_m$$

For a natural number $n:\mathbb{N}$, the [[image]] of $\vert - \vert_n$ under $V$ is called the **space of $n$-multivectors** and is denoted as $\vert V \vert_n$. 

$$\vert V \vert_n \coloneqq \mathrm{im}(\mathcal{F}_{n})$$ 

The terms of $\vert V \vert_n$ are called **$n$-multivectors**.

The **$n$-multivectors** are exactly those multivectors whose grade projections for all natural numbers $i \gt n$ are all zero.  

## Examples ##

* Every [[polynomial ring]] is an $\mathbb{N}$-graded module, where the $n$-vectors are homogeneous polynomials of degree $n$, and the $n$-multivectors are general polynomials of degree $n$. 

* Every [[geometric algebra]] is an $\mathbb{N}$-graded module. 

* Every [[exterior algebra]] is an $\mathbb{N}$-graded module. 

## See also ##

* [[commutative ring]]

* [[module]]

* [[graded vector space]]

* [[geometric algebra]]

## References ##

* {#AragonEtAl97} G. Aragón, J.L. Aragón, M.A. Rodríguez (1997), Clifford Algebras and Geometric Algebra, _Advances in Applied Clifford Algebras_ Vol. 7 No. 2, pg 91–102, doi:10.1007/BF03041220, S2CID:120860757