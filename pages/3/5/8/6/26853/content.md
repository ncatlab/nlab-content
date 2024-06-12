+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A **semiflexible limit** is a [[strict 2-limit]] whose [[weighted limit|weight]] is **semiflexible** (defined below). The semiflexible weights are precisely those weights whose limits are [[bilimits]].

All [[flexible limits]], hence also [[PIE-limits]] and [[strict pseudo-limits]], are semiflexible.

The class of semiflexible weights is a [[saturated class of limits]].

## Definition

Let $D$ be a small [[strict 2-category]].  Write $[D,Cat]$ for the strict 2-category of [[strict 2-functors]], [[strict 2-natural transformation|strict 2-natural transformations]], and [[modifications]], and $Ps(D,Cat)$ for the strict 2-category of strict 2-functors, [[pseudonatural transformations]], and modifications.  The inclusion
$$ [D,Cat] \to Ps(D,Cat) $$
(as a [[wide subcategory]]) has a strict [[left adjoint]] $Q$, which is the [[pseudo morphism classifier]] for an appropriate [[strict 2-monad]].  Therefore, for any functor $\Phi \colon D\to Cat$, we have $Q\Phi \colon D\to Cat$ such that pseudonatural transformations $\Phi \to \Psi$ are in natural bijection with strict 2-natural transformations $Q\Phi \to \Psi$.

The [[counit of an adjunction|counit]] of this adjunction is a canonical strict 2-natural transformation $q\colon Q\Phi \to \Phi$.  We say that $\Phi$ is **semiflexible** if this transformation admits a [[pseudo-section]] (equivalent is an [[equivalence]]) in $[D,Cat]$.

## Examples

- Every [[flexible limit]] is semiflexible.

## Related pages

* [[flexible limit]]
* [[PIE-limit]]

## References

* {#BirdKellyPowerStreet89} [[Greg J. Bird]], [[Max Kelly]], [[John Power]], [[Ross Street]], _Flexible limits for 2-categories_, Journal of Pure and Applied Algebra **61** 1 (1989) 1-27 \[<a href="https://doi.org/10.1016/0022-4049(89)90065-0">doi:10.1016/0022-4049(89)90065-0</a>\]

* John Bourke and Richard Garner, _On semiflexible, flexible and pie algebras_, Journal of Pure and Applied Algebra 217.2 (2013): 293-321.

[[!redirects semi-flexible limit]]
[[!redirects semiflexible limits]]
[[!redirects semi-flexible limits]]
[[!redirects semiflexible 2-limit]]
[[!redirects semiflexible 2-limits]]
[[!redirects semi-flexible 2-limit]]
[[!redirects semi-flexible 2-limits]]
[[!redirects semiflexible weight]]
[[!redirects semi-flexible weight]]
[[!redirects semiflexible weights]]
[[!redirects semi-flexible weights]]
