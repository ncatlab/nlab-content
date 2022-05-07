[[!redirects possibly empty nonunital ring]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

By replacing every element in the definition with a constant function to the element, the empty set vacuously satisfies the axioms of any algebraic structure. 

## Definition

A __possibly empty ring__ is a [[set]] $R$ with a binary operation $(-)+(-):R \times R \to R$, a unary operation $-:R \to R$, a unary operation $0:R \to R$, a binary operation $(-)\cdot(-):R \times R \to R$, and a unary operation $1:R \to R$ such that that:

  * For all $a$, $b$, and $c$ in $R$, $a+(b+c)=(a+b)+c$
  * For all $a$ and $b$ in $R$, $a+b=b+a$
  * For all $a$ and $b$ in $R$, $a+0(b)=a$
  * For all $a$ and $b$ in $R$, $a+(-a)=0(b)$
  * For all $a$, $b$, and $c$ in $R$, $a\cdot (b\cdot c)=(a\cdot b)\cdot c$
  * For all $a$ and $b$ in $R$, $a\cdot 1(b)=a$
  * For all $a$ and $b$ in $R$, $1(a)\cdot b=b$
  * For all $a$, $b$, and $c$ in $R$, $a\cdot (b+c)= a\cdot b + a\cdot c$
  * For all $a$, $b$, and $c$ in $R$, $(a+b)\cdot c= a\cdot c + b\cdot c$

A possibly empty ring is __commutative__ if for all $a$ and $b$ in $R$, $a\cdot b=b \cdot a$. 

## Examples

* Every [[ring]] is a possibly empty ring. 

* The empty possibly empty ring is an possibly empty ring that is not a ring. 

## Related concepts

* [[ring]]

* [[possibly empty field]]

[[!redirects possibly empty commutative ring]]
[[!redirects possibly empty commutative rings]]