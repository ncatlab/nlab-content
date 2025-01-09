+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A **procomonad** or **profunctor comonad** is a [[comonad]] in the [[bicategory]] [[Prof]] of [[small categories]], [[profunctors]], and [[natural transformations]].

## Examples

- Every [[monad]] on a category $C$ induces a *corepresentable* procomonad on $C$.
- Every [[comonad]] on a category $C$ induces a *representable* procomonad on $C$.

## Properties

- The **procomonadic** functors (i.e. the forgetful functors from categories of coalgebras for procomonads) are the closure of the comonadic functors under pullback (Corollary 11 of [Street 2023](#Street23)).
- The procomonadic functors are closed under exponentiating by a fixed category (Proposition 12 of [Street 2023](#Street23)).

## Related pages

* [[promonad]]
* [[comonad]]
* [[profunctor]]

## References

* Michel Thiébaud, _Self-dual structure-semantics and algebraic categories_, PhD thesis (1971)

* Manfred Bernd Wischnewsky, _Aspects of categorical algebra in initialstructure categories_, Cahiers de topologie et géométrie différentielle 15.4 (1974): 419-444.

* [[Peter Johnstone]] and [[André Joyal]], _Continuous categories and exponentiable toposes_, Journal of Pure and Applied Algebra 25.3 (1982): 255-296.

* [[Bob Paré]], [[Bob Rosebrugh]], and [[R. J. Wood]], _Idempotents in bicategories_, Bulletin of the Australian Mathematical Society 39.3 (1989): 421-434.

* [[Ross Street]], _Wood fusion for magmal comonads_, [arXiv:2311.07088](https://arxiv.org/abs/2311.07088) (2023)

[[!redirects procomonads]]
