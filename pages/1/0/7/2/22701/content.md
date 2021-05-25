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

A __possibly empty nonunital ring__ is a [[set]] $R$ with a binary operation $(-)+(-):R \times R \to R$ called __addition__ and a unary operation $-:R \to R$ such that:

  * For all $a$ and $b$ in $R$, $a+b+(-b)=a$
  * For all $a$, $b$, and $c$ in $R$, $a+(b+c)=(a+b)+c$
  * For all $a$ and $b$ in $R$, $a+b=b+a$

and a binary operation $(-)\cdot(-):R \times R \to R$ called __[[multiplication]]__ such that 

  * For all $a$, $b$, and $c$ in $R$, $a\cdot (b\cdot c)=(a\cdot b)\cdot c$
  * For all $a$, $b$, and $c$ in $R$, $a\cdot (b+c)= a\cdot b + a\cdot c$
  * For all $a$, $b$, and $c$ in $R$, $(a+b)\cdot c= a\cdot c + b\cdot c$
  * For all $a$ and $b$ in $R$, $(-a)\cdot b= -(a\cdot b)$
  * For all $a$ and $b$ in $R$, $a\cdot (-b)= -(a\cdot b)$

A possibly empty nonunital ring is __commutative__ if for all $a$ and $b$ in $R$, $a\cdot b=b \cdot a$. 

## Examples

* Every [[nonunital ring]] is a possibly empty nonunital ring. 

* The empty possibly empty nonunital ring is an possibly empty nonunital ring that is not a nonunital ring. 

## Related concepts

* [[commutative invertible semigroup]]

* [[nonunital ring]]

* [[possibly empty field]]

[[!redirects possibly empty nonunital commutative ring]]
[[!redirects possibly empty commutative nonunital ring]]