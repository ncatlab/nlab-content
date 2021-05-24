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

There should be a commutative version of a [[invertible magma]]. That leads to the concept of a _commutative invertible magma_. 

## Definition

A __commutative invertible magma__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ called the __inverse__ such that 

* $a \cdot (b \cdot b^{-1}) = a$
* $(a \cdot b) \cdot b^{-1} = a$
* $(a \cdot b^{-1}) \cdot b = a$ 

for all $a,b \in G$. 


## Properties

* Every commutative invertible magma is a [[commutative quasigroup]] whose __division__ operation is $a / b = a \cdot b^{-1}$. 

## Examples

* Every [[commutative loop]] is a commutative invertible [[unital magma]]. 

* Every commutative invertible semigroup is a commutative invertible magma. 

* Every [[abelian group]] is a commutative invertible monoid.

* The empty magma is a commutative invertible magma. 

## Related concepts

* [[invertible magma]] (non-commutative version)

* [[commutative magma]] (non-invertible version)

* [[commutative loop]] (unital version)

* [[possibly empty abelian group]] (associative version)