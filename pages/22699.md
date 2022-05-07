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

There should be a non-associative version of a [[possibly empty abelian group]], given that one of the axioms in that article states, using only subtraction, that the derived addition binary operation is associative. That leads to the concept of a _possibly empty abelian loop_. 

## Definition

A __possibly empty abelian loop__ is a [[set]] $G$ with a binary operation $(-)-(-):G \times G \to G$ called __[[subtraction]]__ such that:

  * For all $a$ and $b$ in $G$, $a-a=b-b$
  * For all $a$ in $G$, $a-(a-a)=a$
  * For all $a$ in $G$, $(a-a)-((a-a)-a)=a$
  * For all $a$ and $b$ in $G$, $a-((b-b)-b) = b-((a-a)-a)$

For any element $a$ in a possibly empty abelian loop $G$, the element $a-a$ is called an __identity element__, and the element $(a-a)-a$ is called the __inverse element__ of $a$. For all elements $a$ and $b$, __addition__ of $a$ and $b$ is defined as $a-((b-b)-b)$. 

## Examples

* Every abelian [[loop]] is a possibly empty abelian loop. 

* Every possibly empty abelian group is a possibly empty abelian loop. 

* The empty possibly empty abelian loop is an possibly empty abelian loop that is not an abelian loop. 

## Related concepts

* [[possibly empty abelian group]] (associative version)

* [[possibly empty loop]] (non-commutative version)