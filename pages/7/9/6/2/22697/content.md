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

There should be a version of a [[loop (algebra)|loop]] that may be empty, similar to how a [[possibly empty group]] is a [[group]] that may be empty. That leads to the concept of a _possibly empty loop_, which is an example of [[centipede mathematics]].

## Definition

### As a quasigroup

A __possibly empty loop__ is a [[quasigroup]] $(G,(-)\cdot(-):G\times G\to G,(-)\backslash(-):G\times G\to G,(-)/(-):G\times G\to G)$ that satisfies the following laws: 

* $a \cdot (b \backslash b) = a$
* $(b \backslash b) \cdot a = a$
* $a \cdot (b / b) = a$
* $(b / b) \cdot a = a$

for all $a$ and $b$ in $G$.

### With multiplication and inverses

A __possibly empty loop__ is a set $G$ with a binary operation, __multiplication__ $(-)\cdot(-):G\times G\to G$, and two unary operations, the __left inverse__ ${^{-1}(-)}:G \to G$ and the __right inverse__ $(-)^{-1}:G \to G$, such that $G$ with multiplication and the left inverse is a left [[invertible magma]] and $G$ with multiplication and the right inverse is a right [[invertible magma]]. 

## Properties

* Every __possibly empty commutative loop__ is a [[commutative invertible magma]]. 

## Examples

* Every [[loop (algebra)|loop]] is a possibly empty loop. 

* Every possibly empty group is a possibly empty loop. 

* The empty possibly empty loop is an possibly empty loop that is not a loop. 

## Related concepts

* [[quasigroup]]

* [[invertible magma]], [[commutative invertible magma]]

* [[possibly empty group]] (associative version)

* [[loop (algebra)|loop]]

[[!redirects possibly empty abelian loop]]

[[!redirects possibly empty commutative loop]]