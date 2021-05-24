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

There should be an [[commutative|abelian]] version of a [[possibly empty group]], in the same way that [[abelian groups]] are the abelian version of [[groups]]. 

In particular, this means that the left and right division operations are the same, and we only need one of them, which is canonically chosen classically as the right division operation. As abelian groups are usually written additively instead of multiplicatively, the binary operation becomes subtraction instead. 

The definition of a possibly empty abelian group given below is a variant of the definition of a [[possibly empty group]], which [first appeared on the heap article](https://ncatlab.org/nlab/revision/diff/heap/13) and is due to [[Toby Bartels]].

## Definition

A __possibly empty abelian group__ is a [[set]] $G$ with a binary operation $(-)-(-):G \times G \to G$ called __[[subtraction]]__ such that:

  * For all $a$ and $b$ in $G$, $a-a=b-b$
  * For all $a$ in $G$, $(a-a)-((a-a)-a)=a$
  * For all $a$ and $b$ in $G$, $a-((b-b)-b) = b-((a-a)-a)$
  * For all $a$, $b$, and $c$ in $G$, $a-(b-c)=(a-((c-c)-c)-b$

For any element $a$ in a possibly empty abelian group $G$, the element $a-a$ is called an __identity element__, and the element $(a-a)-a$ is called the __inverse element__ of $a$. For all elements $a$ and $b$, __addition__ of $a$ and $b$ is defined as $a-((b-b)-b)$. 

## Examples

* Every [[abelian group]] is a possibly empty abelian group. 

* The empty possibly empty abelian group is an possibly empty abelian group that is not an abelian group. 

## Related concepts

* [[possibly empty group]] (non-commutative version)

* [[possibly empty abelian loop]] (non-associative version)

* [[possibly empty nonunital ring]] (semigroup object in the category of possibly empty abelian groups)

* [[abelian group]]