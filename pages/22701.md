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

A __possibly empty nonunital ring__ is a [[set]] $R$ with a binary operation $(-)-(-):R \times R \to R$ called __[[subtraction]]__ such that:

  * For all $a$ and $b$ in $R$, $a-a=b-b$
  * For all $a$ in $R$, $(a-a)-((a-a)-a)=a$
  * For all $a$ and $b$ in $R$, $a-((b-b)-b) = b-((a-a)-a)$
  * For all $a$, $b$, and $c$ in $R$, $a-(b-c)=(a-((c-c)-c)-b$

and a binary operation $(-)\cdot(-):R \times R \to R$ called __[[multiplication]]__ such that 

  * For all $a$, $b$, and $c$ in $R$, $a\cdot (b\cdot c)=(a\cdot b)\cdot c$
  * For all $a$, $b$, and $c$ in $R$, $a\cdot (b-c)= a\cdot b - a\cdot c$
  * For all $a$, $b$, and $c$ in $R$, $(a-b)\cdot c= a\cdot c - b\cdot c$

A possibly empty nonunital ring is __commutative__ if for all $a$ and $b$ in $R$, $a\cdot b=b \cdot a$. 

For any element $a$ in a possibly empty nonunital ring $R$, the element $a-a$ is called an __additive identity element__, and the element $(a-a)-a$ is called the __additive inverse element__ of $a$. For all elements $a$ and $b$, __addition__ of $a$ and $b$ is defined as $a-((b-b)-b)$. 

## Examples

* Every [[nonunital ring]] is a possibly empty nonunital ring. 

* The empty possibly empty nonunital ring is an possibly empty nonunital ring that is not a nonunital ring. 

## Related concepts

* [[possibly empty abelian group]]

* [[nonunital ring]]

[[!redirects possibly empty nonunital commutative ring]]
[[!redirects possibly empty commutative nonunital ring]]