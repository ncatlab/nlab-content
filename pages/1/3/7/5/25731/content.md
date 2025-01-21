
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

A [[functor]] $F\colon C \to D$ is **dominant** if it is "surjective on objects up to retracts". Such functors are also called **co-conservative** or **liberal** (see [[codiscrete cofibration ]]).


## Definition

$F\colon C \to D$ is **dominant** if for every [[object]] $y$ of $D$, there exists an object $x$ of $C$ for which $y$ is a [[retract]] of $F x$, i.e. there is a pair of morphisms $y \to F x \to y$ composing to the identity.

## Examples

* Every [[essentially surjective on objects functor]] is dominant.

## Properties

* Let $L \dashv R I$ be an [[adjunction]]. If $I$ is dominant and [[full]], then $I L \dashv R$. In this case, the two adjunctions induce the same [[monad]]. This is Proposition 1.5 of [DFH75](#DFH75). (For a converse, see [[fully faithful functor]].)

* Let $L \dashv R$. If $L$ is dominant, then $R$ is [[faithful]]. $R$ is [[full]] if it is full on the image of $L$. This is Proposition 1.7 of [DFH75](#DFH75).

* Let $G : A \to B$ be a functor between small categories. The induced functor $[G^{op}, Set] : [B^{op}, Set] \to [A^{op}, Set]$ between [[presheaf categories]] is a [[surjective geometric morphism]] if and only if $G$ is dominant, if and only if $[G^{op}, Set]$ is [[monadic]]. This is Example A4.2.7(b) of [[Sketches of an Elephant]].

## Related concepts

[[!include properties of functors -- contents]]

## References

* {#DFH75} [[Aristide Deleanu]], [[Armin Frei]], [[Peter Hilton]], _Idempotent triples and completion_, Mathematische Zeitschrift **143** (1975) 91-104 &lbrack;[doi:10.1007/BF01173053](https://doi.org/10.1007/BF01173053)&rbrack;

Called **liberal** in:

* [[Aurelio Carboni]] and [[Scott Johnson]] and [[Ross Street]] and [[Dominic Verity]], "Modulated bicategories" (MB 1994) [MR](http://www.ams.org/mathscinet-getitem?mr=1285544).

Called **quasi-surjective on objects functors** in:

* [[Gabriella Böhm]], [[Steve Lack]], [[Ross Street]], _Idempotent splittings, colimit completion, and weak aspects of the theory of monads_, Journal of Pure and Applied Algebra __216__:2 (2012) 385--403 [doi](https://doi.org/10.1016/j.jpaa.2011.07.003)

[[!redirects dominant functors]]
[[!redirects liberal functor]]
[[!redirects liberal functors]]
[[!redirects coconservative functor]]
[[!redirects coconservative functors]]
[[!redirects co-conservative functor]]
[[!redirects co-conservative functors]]
