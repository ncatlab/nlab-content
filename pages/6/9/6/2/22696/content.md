
> This entry is about [[semigroups]] with two-sided [[inverses]]. For semigroups with a unary operator $i$ such that $s \cdot i(s) \cdot s = s$ and $i(s) \cdot s \cdot i(s) = i(s)$, see instead at *[[inverse semigroup]]*. 



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
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

A [[semigroup]] that is also an [[invertible magma]]. 

## Definition

### With only multiplication

An __invertible semigroup__ is a [[semigroup]] $(G,(-)\cdot(-):G\times G\to G)$ such that for every element $a \in A$, left multiplication and right multiplication by $a$ are both [[bijections]]. 

### With multiplication and inverses

An __invertible semigroup__ is a [[semigroup]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation called the __inverse__ $(-)^{-1}:G \to G$ such that 

* $a \cdot b^{-1} \cdot b = a$
* $b^{-1} \cdot b \cdot a = a$
* $b \cdot b^{-1} \cdot a = a$ 
* $a \cdot b \cdot b^{-1} = a$

for all $a,b \in G$. 

### Torsor-like definition

There is an alternate definition of an invertible semigroup that looks like the usual definition of a [[torsor]] or [[heap]]:

An __invertible semigroup__ is a set $S$ with a binary operation $(-)\cdot(-):S\times S\to S$ called __multiplication__ and a unary operation $(-)^{-1}:S\to S$ called __inverse__ satisfying the following laws:

* [[associativity]]: $a \cdot (b \cdot c) = (a \cdot b) \cdot c$ for all $a,b,c\in S$
* left [[Malcev operation|Malcev identity]]: $b \cdot b^{-1} \cdot a = a$ for all $a,b\in S$
* right [[Malcev operation|Malcev identity]]: $a \cdot b^{-1} \cdot b = a$ for all $a,b\in S$
* [[commutative|commutativity]] with [[inverse elements]]: $a \cdot a^{-1} = a^{-1} \cdot a$ for all $a\in S$

## Pseudo-torsor

Every invertible semigroup $G$ has a canonical structure of a [[pseudo-torsor]], or associative [[Malcev operations|Malcev algebra]], via the ternary operation $t:G^3\to G$ defined as $t(x,y,z)=x\cdot y^{-1}\cdot z$. If the invertible semigroup is inhabited, then its associated pseudo-torsor is actually a [[heap]], or equivalently a [[torsor]]. 

## Properties

* Every invertible semigroup is either a [[group]] or the empty semigroup. 

## Related concepts

* [[invertible magma]] (nonassociative version)

* [[semigroup]] (non-invertible version)

* [[group]] (unital version)

* [[commutative invertible semigroup]] (commutative version)

* [possibly empty heap](heap#empty) (forgetting the unit element)

* [[pseudo-torsor]], [[torsor]]

[[!redirects invertible semigroups]]
