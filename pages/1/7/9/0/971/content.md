<div class="rightHandSide toc">
[[!include compact object - contents]]
</div>


# Contents
* automatic table of contents
{:toc}

## Idea 

An accessible [[category]] is a possibly [[large category]] which is however essentially determined by a [[small category]] in that it behaves like the category of [[ind-object]]s of a small category.

Accessible categories are the categories of models of [[sketch|sketches]].

## Definition 

A [[locally small category]] is accessible if for some [[regular cardinal]] $\kappa$:

* the category has $\kappa$-[[directed colimit]]s,
* there is a set of $\kappa$-[[compact object]]s that generate the category under $\kappa$-directed colimits.

## Relation to other concepts ##

If an accessible category in addition has all (small) [[colimit]]s (or, equivalently, [[limits]]), then it is a [[locally presentable category]].

## Properties {#Properties}

+-- {: .un_prop}
###### Proposition (preservation of accessibility under inverse images)

Let $F : C \to D$ be a [[functor]] between [[presentable category|presentable categories]] which preserves $\kappa$-[[filtered category|filtered]] [[colimit]], and let $D_0 \subset D$ be an accessible subcategory. Then the inverse image $f^{-1}(D_0) \subset C$ is a $\kappa$-accessible subcategory.

=--

+-- {: .proof}
###### Proof

This appears as [[Higher Topos Theory|HTT, corollary A.2.6.5]].
=--



+-- {: .un_prop}
###### Proposition (accessibility of fibrations and weak equivalences in a combinatorial model category)

Let $C$ be a [[combinatorial model category]], $Arr(C)$ its [[arrow category]], $W \subset Arr(C)$ the [[full subcategory]] on the weak equivalences and $F \subset Arr(C)$ the full subcategory on the fibrations. Then $F$, $W$ and $F \cap W$ are accessible subcategories of $Arr(C)$

=--

+-- {: .proof}
###### Proof

This appears as [[Higher Topos Theory|HTT, corollary A.2.6.6]].
=--


## References 

The term _accessible category_ is due to

* Makkai, Par&eacute; 1989. 

The standard textbook on the theory of accessible categories is

* Ad&aacute;mek and Rosicky, _Locally Presentable and Accessible Categories_. Cambridge University Press, Cambridge,
1994. 

A discussion of [[accessible (infinity,1)-category|accessible (infinity,1)-categories]] is in [section 5.4, p. 341](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=341)
of

* Jacob Lurie, _Higher Topos Theory_ ([arXiv](http://arxiv.org/abs/math.CT/0608040))

[[!redirects accessible categories]]
