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

An __invertible magma__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ called the __inverse__ such that

* $a \cdot (b^{-1} \cdot b) = a$
* $(b^{-1} \cdot b) \cdot a = a$
* $b \cdot (b^{-1} \cdot a) = a$ 
* $b^{-1} \cdot (b \cdot a) = a$
* $a \cdot (b \cdot b^{-1}) = a$
* $(b \cdot b^{-1}) \cdot a = a$
* $(a \cdot b) \cdot b^{-1} = a$
* $(a \cdot b^{-1}) \cdot b = a$ 

for all $a,b \in G$. 

## Properties

* Every invertible magma is a [[quasigroup]]. 

## Examples

* Every group is an invertible magma. 

* Every [[invertible semigroup]] and [[nonassociative group]] is an invertible magma. 

## Related concepts

* [[magma]] (noninvertible version)

* [[nonassociative group]] (unital version)

* [[commutative invertible magma]] (commutative version)

* [[invertible semigroup]] (associative version)

* [[centipede mathematics]]

[[!redirects invertible magmas]]