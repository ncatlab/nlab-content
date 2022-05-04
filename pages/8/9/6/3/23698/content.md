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

A **decimal interval coalgebra** is a [[set]] $I$ with a [[linear order]] $\lt$, elements $0 \in I$, $1 \in I$, and a [[partial function]] from $\mathbb{N}$ to the set of [[endofunctions]] in $I$, $I \to I$

$$z:\{m \in \mathbb{N} \vert (m \lt 10)\} \to (I \to I)$$

such that 

* for all elements $a \in I$, $0 \lt a$ or $a \lt 1$

* for all natural numbers $m \in \mathbb{N}$, if $m \lt 10$, then $z(m)(0) = 0$

* for all natural numbers $m \in \mathbb{N}$, if $m \lt 10$, then $z(m)(1) = 1$

* for all natural numbers $m \in \mathbb{N}$, if $m + 1 \lt 10$, then for all elements $a \in I$, it is not true that both $0 \lt z(m+1)(a)$ and $z(m)(a) \lt 1$

## Examples ##

* The initial decimal interval coalgebra is the [[unit interval]] on the [[decimal rational numbers]]

* The terminal decimal interval coalgebra is the [[unit interval]] on the [[Dedekind real numbers]]

## See also ##

* [[decimal rational numbers]]
* [[dyadic interval coalgebra]]
* [[rational interval coalgebra]]
* [[unit interval]]
* [[coalgebra]]