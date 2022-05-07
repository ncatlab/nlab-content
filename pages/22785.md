+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contenta
* table of contents
{: toc}

## Idea

Pythagorean rings are rings in which all elements satisfy the common Pythagorean identity, generalizing from the [[real numbers]]. 

## Definitions

Let $R$ be a (possibly [[nonassociative ring|nonassociative]] and/or possibly [[nonunital ring|nonunital]]) [[ring]]. Then $R$ is a __Pythagorean ring__ if it has a binary operation $p:R \times R \to R$ such that for every element $a$ and $b$ in $R$, $a^2 + b^2 = p(a,b)^2$. (Note all binary operations $\cdot$ have an associated cartesian square $(-)^2$ defined as $a^2 = a \cdot a$.)

There is also a $n$-[[arity|ary]] version of $p$, which is a finite sum 

$$\sum_{i=0}^n a_i^2 = p_n(a_0,a_1,\ldots,a_n)^2$$

for a natural number $n:\mathbb{N}$. 

## Properties

Due to the nature of addition in an [[abelian group]], the set $R$ with the binary operation $p$ is a [[commutative magma|commutative]] [[semigroup]]. 

Every [[finitely generated]] $R$-[[module]] $A$ for a Pythagorean ring $R$ by a set of finite cardinality $n$ has an absolute value $\vert (-) \vert: A \to R$ given by the $n$-ary version of $p$ in $R$ for the scalars $a_i$ of an element $a$ in $A$, and a [[quadratic form]] given by $\vert(-)\vert^2$. As a result, for every [[finitely generated]] $R$-[[module]] $A$ for a Pythagorean ring $R$ there is an associated [[Clifford algebra]] $Cl(R,\vert(-)\vert^2)$. 

## Examples

* The real numbers are a Pythagorean ring. 

* A Pythagorean ring that is a [[field]] is a __Pythagorean field__. 

## Related concepts

* [[Euclidean geometry]]

* [[absolute value]]

* [[Clifford algebra]]

* [[exponential ring]]

## External links

* Wikipedia, *[Pythagorean field](https://en.wikipedia.org/wiki/Pythagorean_field)*