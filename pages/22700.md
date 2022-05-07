[[!redirects possibly empty abelian group]]
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

There should be an associative version of a [[commutative invertible magma]]. That leads to the concept of a _commutative invertible semigroup_. 

## Definition

A __commutative invertible semigroup__ is a [[commutative magma|commutative]] [[semigroup]] $(G,(-)+(-):G\times G\to G)$ with a unary operation $-:G \to G$ called the __inverse__ such that $a + b + (-b) = a$ for all $a,b \in G$.

### With subtraction only

A __commutative invertible semigroup__ is a [[set]] $G$ with a binary operation $(-)-(-):G \times G \to G$ called __[[subtraction]]__ such that:

  * For all $a$ and $b$ in $G$, $a-a=b-b$
  * For all $a$ in $G$, $(a-a)-((a-a)-a)=a$
  * For all $a$ and $b$ in $G$, $a-((b-b)-b) = b-((a-a)-a)$
  * For all $a$, $b$, and $c$ in $G$, $a-(b-c)=(a-((c-c)-c)-b$

For any element $a$ in a commutative invertible semigroup $G$, the element $a-a$ is called an __identity element__, and the element $(a-a)-a$ is called the __inverse element__ of $a$. For all elements $a$ and $b$, __addition__ of $a$ and $b$ is defined as $a-((b-b)-b)$. 

## Properties

* Every commutative invertible semigroup is a [[commutative quasigroup]]..

## Examples

* Every [[abelian group]] is a commutative invertible semigroup. 

* The empty magma is a commutative invertible semigroup that is not an abelian group. 

## Related concepts

* [[invertible semigroup]] (non-commutative version)

* [[commutative invertible magma]] (non-associative version)

* [[commutative semigroup]] (non-invertible version)

* [[abelian group]] (unital version)

* [[possibly empty nonunital ring]] (semigroup object in the category of possibly empty abelian groups)