
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A [[functor]] from a [[category]] to itself is called an **endofunctor**.

Given any category $C$, the [[functor category]] 

$$End(C) = C^C $$

is called the **endofunctor category** of $C$.  The objects of $End(C)$ are endofunctors $F: C \to C$, and the morphisms are [[natural transformations | natural transformation]] between such endofunctors.  

## Properties

### Monoidal structure

The endofunctor category is a [[strict monoidal category|strict]] [[monoidal category]], thanks to our ability to compose endofunctors:

$$\circ : End(C) \times End(C) \to End(C)$$

The unit object of this monoidal category is the identity functor from $C$ to itself:

$$1_C \in End(C) $$

### Monoids

A [[monoid]] in this endofunctor category is called a [[monad]] on $C$.

## Related concepts

* [[algebra over an endofunctor]]

* [[coalgebra over an endofunctor]]

* [[pointed endofunctor]]



[[!redirects endofunctors]]
[[!redirects endofunctor category]]
[[!redirects endofunctor categories]]
