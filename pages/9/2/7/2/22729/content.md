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

A __left invertible magma__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ called the __left inverse__ such that

* $a \cdot (b^{-1} \cdot b) = a$
* $(b^{-1} \cdot b) \cdot a = a$
* $b \cdot (b^{-1} \cdot a) = a$ 
* $b^{-1} \cdot (b \cdot a) = a$

for all $a,b \in G$. 

A __right invertible magma__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ called the __right inverse__ such that 

* $a \cdot (b \cdot b^{-1}) = a$
* $(b \cdot b^{-1}) \cdot a = a$
* $(a \cdot b) \cdot b^{-1} = a$
* $(a \cdot b^{-1}) \cdot b = a$ 

for all $a,b \in G$. 

A __two-sided invertible magma__ or an __invertible magma__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ that is both a left inverse and a right inverse; such a unary operation is called a __two-sided inverse__ or just an __[[inverse]]__. 

## Properties

* Every invertible magma is a [[quasigroup]]; in fact, every invertible magma is a [[possibly empty loop]] whose left and right inverses are equal. 

* Every [[commutative magma|commutative]] left or right invertible magma is a two-sided invertible magma. 

## Examples

* Every group is an invertible magma. 

* Every [[possibly empty group]] and [[nonassociative group]] is an invertible magma. 

## Related concepts

* [[magma]]

* [[group]]

* [[quasigroup]]

* [[nonassociative group]]

* [[commutative invertible magma]]

* [[possibly empty loop]]

* [[possibly empty group]]

* [[centipede mathematics]]