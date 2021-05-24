+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Possibly empty groups arise from [[pseudo-torsors]], or equivalently from associative [[Malcev operations|Malcev algebras]], [[heaps]]/[[torsors]] being [[inhabited]] [[associative Malcev algebra]]s and giving rise to [[groups]]. The definition of a possibly empty group given below [first appeared on the heap article](https://ncatlab.org/nlab/revision/diff/heap/13) and is due to [[Toby Bartels]].

## Definition

A __possibly empty left group__ is a [[set]] $G$ with a binary operation $(-)\backslash(-):G \times G \to G$ (a [[magma]]) such that:

  * For all $a$ and $b$ in $G$, $a\backslash a=b\backslash b$
  * For all $a$ in $G$, $(a\backslash (a\backslash a))\backslash (a\backslash a)=a$
  * For all $a$, $b$, and $c$ in $G$, $(a\backslash b)\backslash c= b\backslash ((a\backslash (a\backslash a))\backslash c)$. 

For any element $a$ in a possibly empty left group $G$, the element $a\backslash a$ is called a __right identity element__, and the element $a\backslash (a\backslash a)$ is called the __right inverse element__ of $a$. For all elements $a$ and $b$ in $G$, __left multiplication__ of $a$ and $b$ is defined as $(a\backslash (a\backslash a))\backslash b$. 

A __possibly empty right group__ is a [[set]] $G$ with a binary operation $(-)/(-):G \times G \to G$ such that:

  * For all $a$ and $b$ in $G$, $a/a=b/b$
  * For all $a$ in $G$, $(a/a)/((a/a)/a)=a$
  * for all $a$, $b$, and $c$ in $G$, $a/(b/c)=(a/((c/c)/c)/b$

For any element $a$ in a possibly empty right loop $G$, the element $a/a$ is called a __left identity element__, and the element $(a/a)/a$ is called the __left inverse element__ of $a$. For all elements $a$ and $b$, __right multiplication__ of $a$ and $b$ is defined as $a/((b/b)/b)$. 

A __possibly empty group__ is a possibly empty left and right group as defined above such that the following are true:

* left and right identity elements are equal (i.e. $a/a = a \backslash a$) for all $a$ in $G$

* left and right inverse elements are equal (i.e. $(a/a)/a = a\backslash (a\backslash a)$) for all $a$ in $G$

* left and right multiplications are equal (i.e. $a/((b/b)/b) = (a\backslash (a\backslash a))\backslash b$) for all $a$ and $b$ in $G$. 

## Pseudo-torsor

Every possibly empty left group $G$ has a [[pseudo-torsor]] $t_G:G^3 \to G$ defined as $t_G(x,y,z) = x \cdot (y \backslash z)$. Every possibly empty right group $H$ has a pseudo-torsor $t_H:H^3 \to H$ defined as $t_H(x,y,z) = (x / y) \cdot z$. This means every possibly empty group has two pseudo-torsors. If the (left or right) possibly empty group is inhabited, then those pseudo-torsors are actually [[torsors]]. 

## Examples

* Every [[group]] is a possibly empty group. 

* The empty possibly empty group is an possibly empty group that is not a group. 

## Related concepts

* [[possibly empty loop]] (non-associative version)

* [[possibly empty abelian group]] (commutative version)

* [possibly empty heap](heap#empty) (forgetting the unit element)

* [[pseudo-torsor]], [[group]], [[torsor]]


