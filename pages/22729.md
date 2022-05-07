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

A __left invertible magma__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ called the __left inverse__ or __retraction__ such that

* $a \cdot (b^{-1} \cdot b) = a$
* $(b^{-1} \cdot b) \cdot a = a$

for all $a,b \in G$. 

A __right invertible magma__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ called the __right inverse__ or __section__ such that

* $a \cdot (b \cdot b^{-1}) = a$
* $(b \cdot b^{-1}) \cdot a = a$

for all $a,b \in G$. 

An __invertible magma__ is a [[magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ called the __[[inverse]]__ such that

* $a \cdot (b^{-1} \cdot b) = a$
* $(b^{-1} \cdot b) \cdot a = a$
* $a \cdot (b \cdot b^{-1}) = a$
* $(b \cdot b^{-1}) \cdot a = a$

for all $a,b \in G$. 

## Properties

Every invertible magma is a [[cancellative magma]]. 

The submagma of every [[power-associative]] invertible magma $M$ [[generator|generated]] by an element $a \in M$ is a [[cyclic group]]. This means in particular there is a $\mathbb{Z}$-[[action]] on $M$ $(-)^{(-)}:M\times\mathbb{Z}\to M$ called the __[[power]]__. 

## Examples

* Every group is an invertible magma. 

* Every [[invertible semigroup]] and [[nonassociative group]] is an invertible magma. 

## Related concepts

* [[magma]] (noninvertible version)

* invertible [[unital magma]] (unital version)

* [[commutative invertible magma]] (commutative version)

* [[invertible semigroup]] (associative version)

* [[invertible quasigroup]] (divisible version)

* [[reciprocal algebra]]

* [[centipede mathematics]]

[[!redirects invertible magmas]]