+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

A **rational interval coalgebra** is a [[set]] $I$ with a [[linear order]] $\lt$, elements $0\in I$, $1 \in I$, and a [[partial function]] from $\mathbb{N} \times \mathbb{N}$ to the set of [[endofunctions]] in $I$, $I \to I$

$$z:\{(m,n) \in \mathbb{N} \times \mathbb{N} \vert isPrime(n) \wedge (m \lt n)\} \to (I \to I)$$

such that 

* for all elements $a \in I$, $0 \lt a$ or $a \lt 1$

* for all natural numbers $n \in \mathbb{N}$ and $m \in \mathbb{N}$, $n$ is a [[prime number]], and if $m \lt n$, then $z(n,m)(0) = 0$

* for all natural numbers $n \in \mathbb{N}$ and $m \in \mathbb{N}$, $n$ is a [[prime number]], and if $m \lt n$, then $z(n,m)(1) = 1$

* for all natural numbers $n \in \mathbb{N}$ and $m \in \mathbb{N}$, $n$ is a [[prime number]], and if $m + 1 \lt n$, then for all elements $a \in I$, it is not true that both $0 \lt z(n,m+1)(a)$ and $z(n,m)(a) \lt 1$. 

## Examples ##

* The initial rational interval coalgebra is the [[unit interval]] on the [[rational numbers]]

* The terminal rational interval coalgebra is the [[unit interval]] on the [[Dedekind real numbers]]

## See also ##

* [[dyadic interval coalgebra]]
* [[decimal interval coalgebra]]
* [[unit interval]]
* [[coalgebra]]