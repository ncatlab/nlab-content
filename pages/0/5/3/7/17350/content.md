# Smothering functor

* table of contents
{:toc}

## Idea

A *smothering functor* is a [[functor]] that is "almost an [[equivalence of categories]]" except that it may not be [[faithful functor|faithful]].  Smothering functors tend to arise when comparing "different [[homotopy categories]]" of the same category that impose more or less refined notions of [[homotopy equivalence]].  Frequently they can be treated more or less like equivalences.

The notion is due to [Riehl and Verity](#RV).

## Definition

A functor $F:C\to D$ is **smothering** if it is

1. [[surjective on objects functor|surjective on objects]],
1. [[full functor|full]], and
1. [[conservative functor|conservative]].

If instead of being surjective on objects $F$ is [[essentially surjective]] on objects, we may say that $F$ is **weakly smothering**.

## Properties

* Each (strict) [[fiber]] of a smothering functor is an [[inhabited]] [[connected]] [[groupoid]]. ([RV, 3.3.2](#RV))
* If $F:C\to D$ is smothering and $x,y\in C$ satisfy $F x \cong F y$ in $D$, then $x \cong y$ in $C$, by fullness combined with conservativity.  In other words, $F$ is "full on isomorphisms" (but since it is not faithful, it is not [[pseudomonic]]).
* Further combining this with surjectivity on objects, every smothering functor is an [[isofibration]].

## Examples

* For any [[model category]] $C$, the functor $Ho(C^{\mathbf{2}}) \to Ho(C)^{\mathbf{2}}$ is weakly smothering, where $\mathbf{2}$ denotes the [[interval category]].  This property appears in the axiom (Der5) for [[derivators]].

## Related pages

* [[smothering 2-functor]]
* [[derivator]]

## References

* [[Emily Riehl]], [[Dominic Verity]], _The 2-category theory of quasi-categories_, Advances in Mathematics 280 (2015) 549 - 642, [arXiv](http://arxiv.org/abs/1306.5144)
 {#RV}

[[!redirects smothering functors]]
[[!redirects weakly smothering functor]]
[[!redirects weakly smothering functors]]
