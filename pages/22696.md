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

Possibly empty groups arise from [[pseudo-torsors]], or equivalently from associative [[Malcev operations|Malcev algebras]], [[heaps]]/[[torsors]] being [[inhabited]] [[associative Malcev algebra]]s and giving rise to [[groups]]. 

## Definition

### With division only

This definition of [first appeared on the heap article](https://ncatlab.org/nlab/revision/diff/heap/13) and is due to [[Toby Bartels]].

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

### With multiplication and inverses

A __possibly empty left group__ is a [[semigroup]] $(G,(-)\cdot(-):G\times G\to G)$ and a unary operation called the __left inverse__ $^{-1}(-):G \to G$ such that 

* ${^{-1}a} \cdot a = {^{-1}b} \cdot b$
* $b \cdot ({^{-1}b} \cdot a) = a$ 
* ${^{-1}b} \cdot (b \cdot a) = a$

for all $a,b \in G$. For any element $a$ in a possibly empty left group $G$, the element ${^{-1}a} \cdot a$ is called a __right identity element__, and for all elements $a$ and $b$ in $G$, __left division__ is defined as $b \backslash a = {^{-1}}b \cdot a$.

A __possibly empty right group__ is a [[semigroup]] $G,(-)\cdot(-):G\times G\to G)$ and a unary operation called the __right inverse__ $(-)^{-1}:G \to G$ such that 

* $a \cdot a^{-1} = b \cdot b^{-1}$
* $(a \cdot b^{-1}) \cdot b = a$ 
* $(a \cdot b) \cdot b^{-1} = a$

for all $a,b \in G$. For any element $a$ in a possibly empty right group $G$, the element $a \cdot a^{-1}$ is called a __right identity element__, and for all elements $a$ and $b$ in $G$, __left division__ is defined as $a / b = a \cdot b^{-1}$.

A __possibly empty two-sided group__ or just __possibly empty group__ is a semigroup $(G,(-)\cdot(-):G\times G\to G)$ that is both a possibly empty left group and a possibly empty right group such that left and right identity elements are the same: $a \cdot a^{-1} = {^{-1}a} \cdot a$ for all $a$ in $G$, and left and right inverse elements are the same: $a^{-1} = {^{-1}a}$ for all $a$ in $G$.

### Torsor-like definition

There is an alternate definition of a possibly empty group that looks like the usual definition of a [[torsor]] or [[heap]]:

A __possibly empty group__ is a set $S$ with a binary operation $(-)\cdot(-):S\times S\to S$ called __multiplication__ and a unary operation $(-)^{-1}:S\to S$ called __inverse__ satisfying the following laws:

* [[associativity]]: $a \cdot (b \cdot c) = (a \cdot b) \cdot c$ for all $a,b,c\in S$
* left [[Malcev operation|Malcev identity]]: $b \cdot b^{-1} \cdot a = a$ for all $a,b\in S$
* right [[Malcev operation|Malcev identity]]: $a \cdot b^{-1} \cdot b = a$ for all $a,b\in S$
* [[commutative|commutativity]] with [[inverse elements]]: $a \cdot a^{-1} = a^{-1} \cdot a$ for all $a\in S$

One could then define __left division__ to be $a \backslash b = a^{-1} \cdot b$ and __right division__ to br $a / b = a \cdot b^{-1}$. 

## Pseudo-torsor

Every possibly empty group $G$ has a pseudo-torsor $t:G^3\to G$ defined as $t(x,y,z)=x\cdot y^{-1}\cdot z$. If the possibly empty group is inhabited, then those pseudo-torsors are actually [[torsors]]. 

## Examples

* Every [[group]] is a possibly empty group. 

* The empty possibly empty group is an possibly empty group that is not a group. 

## Related concepts

* [[possibly empty loop]]

* [[invertible magma]] (nonassociative version)

* [[semigroup]] (non-invertible version)

* [[group]] (unital version)

* [[commutative invertible semigroup]] (commutative version)

* [possibly empty heap](heap#empty) (forgetting the unit element)

* [[pseudo-torsor]], [[group]], [[torsor]]


