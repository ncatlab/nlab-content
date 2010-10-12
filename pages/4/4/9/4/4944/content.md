
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _homotopy $T$-algebra_ over a [[Lawvere theory]] $T$ is a model for an $\infty$-algebra over $T$, when the latter is regarded as an [[(∞,1)-algebraic theory]]

## Definition

For $T$ (the syntactic category of) a [[Lawvere theory]] with generating object $x$ an ordinary [[algebra over a Lawvere theory]]  [[functor]] $T \to Set$ that preserves products, in that for all $n \in \mathbb{N}$ the canonical morphism

$$
  \prod_{i = 1}^n A(p_i) :  A(x^n) \to (A(x))^n
$$ 

is an [[isomorphism]].

A **homotopy $T$-algebra** is a functor $A : T \to $ [[Top]] such that for all $n \in \mathbb{N}$ this canonical morphism is a [[weak homotopy equivalence]].

## Properties

**Theorem.** Every homotopy $T$-algebra is weakly equivalent to a strictly product-preserving functor.

This is theorem 1.3 in ([Badzioch](#Badzioch))

## References

In 

* [[Bernard Badzioch]], _Algebraic theories in homotopy theory_ Annals of Mathematics, 155 (2002), 895-913 ([JSTOR](http://www.jstor.org/stable/3062135))
{#Badzioch}

the model structure on homotopy $T$-algebras is discussed and it is shown that every homotopy $T$-algebra is weakly equivalent to a strictly product-preserving functor $T \to Top$.

For multi-sorted theories this is discussed in

* [[Julie Bergner]], _Rigidification of algebras over multi-sorted theories_ , Algebraic and Geometric Topoogy 7, 2007.
{#Bergner}
