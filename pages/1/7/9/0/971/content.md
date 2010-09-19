
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--



# Contents
* automatic table of contents
{:toc}

## Idea 

An accessible [[category]] is a possibly [[large category]] which is however essentially determined by a [[small category]], in a certain way.  There are several ways to make this precise, all equivalent.

## Definition 

A [[locally small category]] $C$ is **accessible** if for some [[regular cardinal]] $\kappa$:

* the category has $\kappa$-[[directed colimit]]s (or, equivalently, $\kappa$-filtered colimits), and
* there is a set of $\kappa$-[[compact object]]s that generate the category under $\kappa$-directed colimits.

If $C$ satisfies these properties for some $\kappa$, we say that it is **$\kappa$-accessible**.  Unlike for [[locally presentable categories]], it does not follow that if $C$ is $\kappa$-presentable and $\kappa\lt \lambda$ then $C$ is also $\lambda$-presentable.  It is true, however, that for any accessible category, there are arbitrarily large cardinals $\lambda$ such that $C$ is $\lambda$-presentable.

Equivalent characterizations include that $C$ is accessible iff:

* it is the category of models (in $Set$) of some small [[sketch]].
* it is of the form $Ind_\kappa(S)$ for $S$ small, i.e. the $\kappa$-[[ind-object|ind-completion]] of a small category, for some $\kappa$.
* it is of the form $\kappa\,Flat(S)$ for $S$ small and some $\kappa$, i.e. the category of $\kappa$-[[flat functor|flat]] functors from some small category to $Set$.
* it is the category of models (in $Set$) of a suitable type of logical theory.

The important notion of functor between accessible categories is an **[[accessible functor]]**, meaning a functor $F\colon C\to D$ such that there exists a $\kappa$ such that $C$ and $D$ are both $\kappa$-accessible and $F$ preserves $\kappa$-filtered colimits.

## Relation to other concepts ##

* If an accessible category in addition has all (small) [[colimit]]s (or, equivalently, [[limits]]), then it is a [[locally presentable category]].

* A [[small category]] is accessible precisely when it is [[idempotent complete category|idempotent complete]].  Makkai--Par&#233; say that this means accessibility is an "almost pure smallness condition."

* A functor out of an accessible category that is $\kappa$-continuous for some [[regular cardinal]] $\kappa$ is an [[accessible functor]].

## Properties {#Properties}

+-- {: .un_prop}
###### Proposition (preservation of accessibility under inverse images)

Let $F : C \to D$ be a [[functor]] between [[locally presentable categories]] which preserves $\kappa$-[[filtered category|filtered]] [[colimits]], and let $D_0 \subset D$ be an accessible subcategory. Then the inverse image $f^{-1}(D_0) \subset C$ is a $\kappa$-accessible subcategory.

=--

+-- {: .proof}
###### Proof

This appears as [[Higher Topos Theory|HTT, corollary A.2.6.5]].
=--



+-- {: .un_prop}
###### Proposition (accessibility of fibrations and weak equivalences in a combinatorial model category)

Let $C$ be a [[combinatorial model category]], $Arr(C)$ its [[arrow category]], $W \subset Arr(C)$ the [[full subcategory]] on the weak equivalences and $F \subset Arr(C)$ the full subcategory on the fibrations. Then $F$, $W$ and $F \cap W$ are accessible subcategories of $Arr(C)$.

=--

+-- {: .proof}
###### Proof

This appears as [[Higher Topos Theory|HTT, corollary A.2.6.6]].
=--

In addition:

* The [[2-category]] $Acc$ of accessible categories, accessible functors, and natural transformations has all small [[2-limits]].

* Every accessible functor satisfies the [[solution-set condition]], and every left or right adjoint between accessible categories is accessible.  Therefore, the [[adjoint functor theorem]] takes an especially pleasing form for accessible categories: a functor is a left (resp. right) adjoint iff it is accessible and preserves all small colimits (resp. limits).


## References 

The term _accessible category_ is due to

* Makkai, Par&#233; 1989. 

The standard textbook on the theory of accessible categories is

* Ad&#225;mek and Rosicky, _Locally Presentable and Accessible Categories_. Cambridge University Press, Cambridge,
1994. 

A discussion of [[accessible (infinity,1)-category|accessible (infinity,1)-categories]] is in [section 5.4, p. 341](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=341)
of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

[[!redirects accessible categories]]
