
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Dominant functors
* table of contents
{: toc}

## Idea

A [[functor]] $F\colon C \to D$ is **dominant** if it is "surjective on objects up to retracts".


## Definition

$F\colon C \to D$ is **dominant** if for every [[object]] $y$ of $D$, there exists an object $x$ of $C$ for which $y$ is a [[retract]] of $Fx$, i.e. there is a pair of morphisms $y \to Fx \to y$ composing to the identity.

## Examples

* Every [[essentially surjective on objects functor]] is dominant.

## Properties

* Let $L \dashv R I$ be an [[adjunction]]. If $R$ is dominant and [[full]], then $I L \dashv R$. In this case, the two adjunctions induce the same [[monad]]. This is Proposition 1.5 of [DFP75](#DFP75).

* Let $L \dashv R$. If $L$ is dominant, then $R$ is [[faithful]]. $R$ is [[full]] if it is full on the image of $L$. This is Proposition 1.7 of [DFP75](#DFP75).

* Let $G : A \to B$ be a functor between small categories. The induced functor $[G^{op}, Set] : [B^{op}, Set] \to [A^{op}, Set]$ between [[presheaf categories]] is a [[surjective geometric morphism]] if and only if $G$ is dominant, if and only if $[G^{op}, Set]$ is [[monadic]]. This is Example A4.2.7(b) of [[Sketches of an Elephant]].

## Related concepts

[[!include properties of functors -- contents]]

## References

* {#DFP75} [[Aristide Deleanu]], [[Armin Frei]], and [[Peter Hilton]]. _Idempotent triples and completion_. Mathematische Zeitschrift 143 (1975): 91-104.

[[!redirects dominant functors]]