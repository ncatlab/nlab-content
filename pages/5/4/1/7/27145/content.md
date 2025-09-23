+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### 2-Category theory
+-- {: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


* table of contents
{: toc}

## Idea

A **probicategory** is a "[[horizontal categorification|many-object]]" generalisation of a [[promonoidal category]], in the same way that a [[bicategory]] is a "many-object" generalisation of a [[monoidal category]].

Just as a promonoidal category in the most general context in which we can perform [[Day convolution]] to obtain a monoidal structure on the category of presheaves, a probicategory is the most general context in which we can perform convolution locally to obtain a bicategory structure on the [[local cocompletion]].

## Definition

A **probicategory** is a [[bicategory]] [[enriched bicategory|enriched]] in the [[monoidal bicategory]] [[Prof]].

## Properties

Given a probicategory, we may form a bicategory by [[change of base]] along the [[pseudofunctor]] from [[Prof]] to [[Cat]] given by taking [[free cocompletion]]. When applied to a one-object probicategory (i.e. a promonoidal category), this produces the (monoidal) presheaf category obtained through [[Day convolution]].

## Related pages

* [[promonoidal category]]
* [[bicategory]]
* [[Day convolution]]
* [[local cocompletion]]

## References

* {#Day70} [[Brian Day]], _Construction of Biclosed Categories_ (PhD Thesis)

A summary of the results of the thesis may be found in:

* [[Brian Day]], _Biclosed bicategories: localisation of convolution_, [arXiv:0705.3485](https://arxiv.org/abs/0705.3485)

[[!redirects probicategories]]
