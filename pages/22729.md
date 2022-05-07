+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

It is possible to define inverses in a magma without defining an [[identity element]] first, yielding a notion of _invertible magma_

## Definition

### With multiplication and inverses

A __left invertible magma__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ called the __left inverse__ such that

* $a \cdot (b^{-1} \cdot b) = a$
* $(b^{-1} \cdot b) \cdot a = a$
* $b \cdot (b^{-1} \cdot a) = a$ 
* $b^{-1} \cdot (b \cdot a) = a$

for all $a,b \in G$. For any element $a$ in a left invertible magma $G$, the element $a^{-1} \cdot a$ is called a __identity element__, and for all elements $a$ and $b$ in $G$, __left division__ is defined as $a / b = a \cdot b^{-1}$. As a result, every left invertible magma is a left [[quasigroup]]. 

A __right invertible magma__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ called the __right inverse__ such that 

* $a \cdot (b \cdot b^{-1}) = a$
* $(b \cdot b^{-1}) \cdot a = a$
* $(a \cdot b) \cdot b^{-1} = a$
* $(a \cdot b^{-1}) \cdot b = a$ 

for all $a,b \in G$. For any element $a$ in a possibly empty right loop $G$, the element $a \cdot a^{-1}$ is called a __identity element__, and for all elements $a$ and $b$ in $G$, __right division__ is defined as $a / b = a \cdot b^{-1}$. As a result, every right invertible magma is a right [[quasigroup]]. 

A __two-sided invertible magma__ or an __invertible magma__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ that is both a left inverse and a right inverse; such a unary operation is called a __two-sided inverse__ or just an __[[inverse]]__. Since, with a left and right inverse, left and right division can be defined that satisfy the [[quasigroup]] axioms, every invertible magma is a quasigroup. 

### As a quasigroup

A __left invertible quasigroup__ is a left [[quasigroup]] $(G,(-)\cdot(-):G\times G\to G),(-)\backslash(-):G\times G\to G)$ such that

* $a \cdot (b \backslash b) = a$
* $(b \backslash b) \cdot a = a$

for all $a$ and $b$ in $G$. For any element $a$ in $G$, the element $a\backslash a$ is called a __right identity element__, and the element $a\backslash (a\backslash a)$ is called the __right inverse element__ of $a$. 

A __right invertible quasigroup__ is a [[quasigroup]] $(G,(-)\cdot(-):G\times G\to G),(-)/(-):G\times G\to G)$ such that 

* $a \cdot (b / b) = a$
* $(b / b) \cdot a = a$

for all $a$ and $b$ in $G$. For any element $a$ in $G$, the element $a/a$ is called a __left identity element__, and the element $(a/a)/a$ is called the __left inverse element__ of $a$. 

A __two-sided invertible quasigroup__ or an __invertible quasigroup__ is a [[quasigroup]] $(G,(-)\cdot(-):G\times G\to G),(-)\backslash(-):G\times G\to G,(-)/(-):G\times G\to G)$ that is both left invertible and right invertible and whose left and right inverses are equal: $a\backslash (a\backslash a) = (a/a)/a$. 

### With division only

An __left invertible magma__ is a [[magma]] $(G,(-)\backslash(-):G\times G\to G)$ such that:

  * For all $a$ and $b$ in $G$, $a\backslash a=b\backslash b$
  * For all $a$ in $G$, $(a\backslash (a\backslash a))\backslash (a\backslash a)=a$

For any element $a$ in $G$, the element $a\backslash a$ is called a __right identity element__, and the element $a\backslash (a\backslash a)$ is called the __right inverse element__ of $a$. For all elements $a$ and $b$ in $G$, __left multiplication__ of $a$ and $b$ is defined as $(a\backslash (a\backslash a))\backslash b$. 

A __right invertible magma__ is a [[magma]] $(G,(-)/(-):G\times G\to G)$ such that:

  * For all $a$ and $b$ in $G$, $a/a=b/b$
  * For all $a$ in $G$, $(a/a)/((a/a)/a)=a$

For any element $a$ in a possibly empty right loop $G$, the element $a/a$ is called a __left identity element__, and the element $(a/a)/a$ is called the __left inverse element__ of $a$. For all elements $a$ and $b$, __right multiplication__ of $a$ and $b$ is defined as $a/((b/b)/b)$. 

An __invertible magma__ is a left and right invertible magma as defined above such that the following are true:

* left and right identity elements are equal (i.e. $a/a = a \backslash a$) for all $a$ in $G$

* left and right inverse elements are equal (i.e. $(a/a)/a=a\backslash (a\backslash a)$) for all $a$ in $G$

* left and right multiplications are equal (i.e. $a/((b/b)/b) = (a\backslash (a\backslash a))\backslash b$) for all $a$ and $b$ in $G$. 

## Properties

* Every invertible magma is a [[quasigroup]]. 

* Every [[commutative magma|commutative]] left or right invertible magma is a two-sided invertible magma. 

## Examples

* Every group is an invertible magma. 

* Every [[possibly empty group]] and [[nonassociative group]] is an invertible magma. 

## Related concepts

* [[magma]]

* [[group]]

* [[quasigroup]]

* [[nonassociative group]]

* [[possibly empty group]]

* [[centipede mathematics]]