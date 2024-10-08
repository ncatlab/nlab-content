+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A non-associative [[group]], or an [[invertible quasigroup|invertible]] [[loop]]. Nonassociative is used in the sense of not-necessarily associative, in the same sense that a [[nonassociative algebra]] is not-necessarily associative. 

## Definition

A __nonassociative group__ or __invertible loop__ is a [[loop]] $(G,\backslash,/,1)$ with a unary operation called the __inverse__ $(-)^{-1}:G \to G$ such that 

* $a^{-1} \cdot a = 1$
* $a \cdot a^{-1} = 1$

for all $a \in G$. 

### Without division

A __nonassociative group__ or __invertible loop__ is a [[unital magma]] $(G,(-)\cdot(-):G\times G\to G),1:G)$ with a unary operation called the __inverse__ $(-)^{-1}:G \to G$ such that 

* $a^{-1} \cdot a = 1$
* $a \cdot a^{-1} = 1$
* $(a \cdot b^{-1}) \cdot b = a$ 
* $(a \cdot b) \cdot b^{-1} = a$
* $b \cdot (b^{-1} \cdot a) = a$ 
* $b^{-1} \cdot (b \cdot a) = a$

for all $a,b \in G$. 

## Properties

Every non-associative group is a [[loop (algebra)|loop]] with a two-sided [[inverse]]. 

## Examples

* Every group is a nonassociative group. 

## Related concepts

* [[group]] (associative version)

* [[loop]] (non-invertible version)

* [[invertible quasigroup]] (non-unital version)

* [[commutative loop]] (commutative version)

* [[centipede mathematics]]

[[!redirects nonassociative group]]
[[!redirects nonassociative groups]]

[[!redirects invertible unital magma]]
[[!redirects invertible unital magmas]]