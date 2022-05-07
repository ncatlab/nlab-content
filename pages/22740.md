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

There should be a commutative version of a [[invertible quasigroup]] or an invertible version of a [[commutative quasigroup]]. That leads to the concept of a _commutative invertible quasigroup_. 

## Definition

A __commutative invertible quasigroup__ is a [[commutative quasigroup]] $(G,\cdot,/)$ with a unary operation $(-)^{-1}:G \to G$ called the __inverse__ such that 

* $a \cdot (b \cdot b^{-1}) = a$

for all $a,b \in G$. 

### Without division

A __commutative invertible quasigroup__ is a [[commutative magma]] $(G,(-)\cdot(-):G\times G\to G)$ with a unary operation $(-)^{-1}:G \to G$ called the __inverse__ such that 

* $a \cdot (b \cdot b^{-1}) = a$
* $(a \cdot b) \cdot b^{-1} = a$
* $(a \cdot b^{-1}) \cdot b = a$ 

for all $a,b \in G$. 

## Examples

* Every [[commutative loop]] is a commutative invertible unital quasigroup. 

* Every commutative invertible semigroup is a commutative [[associative quasigroup]]. 

* Every [[abelian group]] is a commutative invertible monoid.

* The empty quasigroup is a commutative invertible quasigroup. 

## Related concepts

* [[invertible quasigroup]] (non-commutative version)

* [[commutative quasigroup]] (non-invertible version)

* [[commutative loop]] (unital version)

* [[commutative invertible semigroup]] (associative version)