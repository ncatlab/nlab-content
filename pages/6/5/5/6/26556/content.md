+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* tic
{: toc}

## Introduction

In moving from one dimension to two dimensions, there are a proliferation of concepts, with a choice of weakness for each one. For one, there is the notion of (strict) [[2-category]] and [[bicategory]], (strict) [[2-monad]] and [[pseudomonad]], and (strict) 2-algebras and pseudoalgebras. Therefore, while it is clear that "2-algebras for a 2-monad on a 2-category inherit 2-limits (and certain 2-colimits) from the base", it can be tricky to recall which level of strictness is appropriate in each case. On this page, we list the various limit and colimit creation properties for two-dimensional algebras.

## Limits

We shall use the conventional terminology of "2-" for strict concepts and "pseudo" for weak concepts to make it easier to compare with the references.

* The 2-category of 2-algebras and strict morphisms for a 2-monad on a 2-category inherits all 2-limits (this follows from $Cat$-enriched category theory).

* The 2-category of 2-algebras and pseudo morphisms for a 2-monad on a 2-category inherits all [[PIE 2-limits]] (§3 of [BKP89](#BKP89).

* The 2-category of 2-algebras and lax morphisms for a 2-monad on a 2-category inherits all [[oplax limits]], limits of strict morphisms, [[equifiers]] and [[inserters]] where one morphism is strict, [[Eilenberg–Moore objects]] for [[comonads]], [[products]] and [[powers]] (see [Lack05](#Lack05) and [LS11](#LS11)). The page [[rigged limit]] contains more details.

* The 2-category of 2-algebras and pseudo morphisms for a [[flexible 2-monad]] on a 2-category inherits all [[flexible limits]] (see Remark 7.2 of [BKPS89](#BKPS89)).

* The 2-category of pseudoalgebras and pseudo morphisms for a [[pseudomonad]] on a 2-category inherits all [[bilimits]] (see Theorem 6.3.1.6 of [Osmond21](#Osmond21)).

## Related pages

* [[2-monad]]

* [[colimits in categories of algebras]]

## References

* {#BKP89} R. Blackwell, G. M. Kelly, and A. J. Power, _Two-dimensional monad theory_, Jour. Pure Appl. Algebra 59 (1989), 1--41

* {#BKPS89} G. J. Bird, [[Max Kelly]], [[John Power]], [[Ross Street]], _Flexible limits for 2-categories_, Journal of Pure and Applied Algebra **61** Issue 1 (1989) pp 1-27. doi:[10.1016/0022-4049(89)90065-0](http://dx.doi.org/10.1016/0022-4049(89%2990065-0)

* {#Lack05} [[Stephen Lack]], _Limits for lax morphisms_, *Appl. Categ. Structures*,
13(3):189--203, 2005

* {#LS11} [[Stephen Lack]] and [[Mike Shulman]], _Enhanced 2-categories and limits for lax morphisms_, [arXiv](http://arxiv.org/abs/1104.2111).

* {#Osmond21} Axel Osmond, _A categorical study of spectral dualities_, PhD thesis, Université Paris Cité, 2021.