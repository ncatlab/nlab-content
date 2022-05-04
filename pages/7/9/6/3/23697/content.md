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

A **dyadic interval coalgebra** is a [[set]] $I$ with a [[linear order]] $\lt$, elements $0 \in I$ and $1 \in I$ and functions $z_0:I \to I$ and $z_1:I \to I$, such that $z_0(0) = 0$, $z_1(0) = 0$, $z_0(1) = 1$, $z_1(1) = 1$, * for all elements $a \in I$, $0 \lt a$ or $a \lt 1$, and for all elements $a \in I$, it is false that both $0 \lt z_0(a)$ and $z_1(a) \lt 1$. 

This is called simply an interval coalgebra by Peter Freyd, however there exist similarly defined interval coalgebras with $n+1$ terms and $n$ zooming operations, such as the [[decimal interval coalgebra]]. 

## Examples ##

* The initial dyadic interval coalgebra is the [[unit interval]] on the [[dyadic rational numbers]]

* The terminal dyadic interval coalgebra is the [[unit interval]] on the [[Dedekind real numbers]]

## See also ##

* [[dyadic rational number]]
* [[rational interval coalgebra]]
* [[decimal interval coalgebra]]
* [[unit interval]]
* [[coalgebra]]

## References ##

* Peter Freyd, Algebraic real analysis, Theory and Applications of Categories, Vol. 20, 2008, No. 10, pp 215-306 ([tac:20-10](http://www.tac.mta.ca/tac/volumes/20/10/20-10abs.html))