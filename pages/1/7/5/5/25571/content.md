

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A [[locally small category]] cannot admit all large discrete [[colimits]] unless it is a [[preorder]] (by an argument of [[Peter Freyd|Freyd]] see *[[complete small category]]*). However, many nice locally small categories admit *some* large colimits.

This page is intended to act as a reference for classes of large colimits that are commonly encountered, and the class of categories that admit them.

On this page, categories will be assumed [[locally small]] unless stated otherwise.

## Colimits versus limits

While this page focuses on categories with large *colimit* properties, these often imply strong *[[complete category|completeness]]* properties. For instance, compact categories (below) are [[complete]], but not always [[cocomplete]].

## Cointersections of epimorphims

Many locally small categories admit small colimits and [[E-colimits]] for $E$ a class of epimorphisms, i.e. [[cointersections]] of morphisms in $E$.

Evidently, a small-[[cocomplete category]] that is [[well powered category|co-well-powered]] will admit cointersections of all [[epimorphisms]], though not all relevant examples are co-well-powered.

### Strong epimorphisms

When $E$ is the [[class]] of [[strong epimorphisms]], such a category is called **well-cocomplete**.

### Regular epimorphisms

The [[free cocompletion]] of a locally small category $A$ under small colimits and [[cointersections]] of [[regular epimorphisms]] is the [[full subcategory]] of the [[presheaf category]] $[A^{op}, Set]$ on the [[weak multilimit|weakly multirepresentable presheaves]] (also called **petty** presheaves). See Remark 4.39 of [Lack & Tendas 2024](#LackTendas2023) (such categories are called **well-cocomplete** in this paper, though conflicts with the earlier terminology).

Theorem 1 of [Kelly & Koubek 1981](#KellyKoubek1981) states that every [[functor]] $F \colon K \to A$, where $A$ has such colimits, admits a colimit if $F$ has a [[weakly terminal set]].

## Adjointness

### Total category

A [[total category]] is a category whose [[Yoneda embedding]] admits a [[left adjoint]]. Every total category is compact in the sense below.

### Compact categories

A category $A$ is **[[compact category|compact]]** in the sense of [Isbell (1968)](#Isbell68) if every [[cocontinuous functor]] from $A$ has a [[right adjoint]].

> Beware that this is *un-related* to the notion of [[compact closed category]].

Every compact category has small [[limits]] and [[intersections]] of [[monomorphisms]], but not necessarily small colimits. A [[counterexample]] is mentioned in §3.15 of [Börger et al.](#Borger1981).

## Related pages

* [[total category]]

## References

* {#Isbell68} [[John Isbell]]. _Small subcategories and completeness_. Mathematical systems theory **2** 1 (1968) 27-50 &lbrack;[doi:10.1007/BF01691344](https://doi.org/10.1007/BF01691344)&rbrack;

* {#KellyKoubek1981} [[Max Kelly]] and V. Koubek. _The large limits that all good categories admit_. Journal of Pure and Applied Algebra 22.3 (1981): 253-263.

* {#Borger1981} R. Börger, [[Walter Tholen]], M. B. Wischnewsky & H. Wolff. _Compact and hypercomplete categories_. Journal of Pure and Applied Algebra 21.2 (1981): 129-144.

* {#Kelly1986} [[Max Kelly]], _A survey of totality for enriched and ordinary categories_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 2 (1986), p. 109-132, [numdam](http://www.numdam.org/item?id=CTGDC_1986__27_2_109_0)

* {#LackTendas2023} [[Stephen Lack]] and [[Giacomo Tendas]]. _Virtual concepts in the theory of accessible categories_. Journal of Pure and Applied Algebra 227.2 (2023): 107196.

* [[Martin Brandenburg]]. _Large limit sketches and topological space objects_. [arXiv preprint 2106.11115](https://arxiv.org/abs/0810.1279) (2021).

[[!redirects compact category]]
[[!redirects compact categories]]


