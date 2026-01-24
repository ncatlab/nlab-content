
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
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

### Extremal epimorphisms

When $E$ is the [[class]] of [[extremal epimorphisms]], such a category is called **Isbell-cocomplete** in §2.2 of [BKR15](#BKR15).

### Strong epimorphisms

When $E$ is the [[class]] of [[strong epimorphisms]], such a category is called **well-cocomplete**.

### Regular epimorphisms

The [[free cocompletion]] of a locally small category $A$ under small colimits and [[cointersections]] of [[regular epimorphisms]] is the [[full subcategory]] of the [[presheaf category]] $[A^{op}, Set]$ on the [[weak multilimit|weakly multirepresentable presheaves]] (also called **petty** presheaves). See Remark 4.39 of [Lack & Tendas 2024](#LackTendas2023) (such categories are called **well-cocomplete** in this paper, though conflicts with the earlier terminology).

Theorem 1 of [Kelly & Koubek 1981](#KellyKoubek1981) states that every [[functor]] $F \colon K \to A$, where $A$ has such colimits, admits a colimit if $F$ has a [[weakly terminal set]].

### Cointersections in total categories

Proposition 4.1 of [Börger and Tholen](#Borger1990) states that every [[total category]] admits arbitrary [[cointersections]] of [[regular epimorphisms]].

Example 4.3 of [Börger and Tholen](#Borger1990) shows that a [[total category]] need not admit arbitrary [[cointersections]] of [[extremal epimorphism|extremal]] or [[strong epimorphisms]], even if it admits a small extremal [[separator]].

## Other examples

- The [[terminal object]] in a category $A$ is a colimit of the [[identity functor]] on $A$.

- A **local state classifier** in a category $A$ is a colimit of the [[wide subcategory]] $A_{mono} \to A$ of [[monomorphisms]] in $A$ ([Hora 2024](#Hora2024)). Proposition 3.17 ibid. states that every [[Grothendieck topos]] admits a local state classifier.

## Adjointness

### Total category

A [[total category]] is a category whose [[Yoneda embedding]] admits a [[left adjoint]]. Every total category is compact in the sense below.

### Compact categories

A category $A$ is **[[compact category|compact]]** in the sense of [Isbell (1968)](#Isbell68) if every (large-)[[cocontinuous functor]] from $A$ has a [[right adjoint]].

> Beware that this is *unrelated* to the notion of [[compact closed category]].

Every compact category has small [[limits]] and [[intersections]] of [[monomorphisms]], but not necessarily small colimits. A [[counterexample]] is mentioned in §3.15 of [Börger et al.](#Borger1981).

A category $A$ is called **strongly compact** in [Brandenburg](#Brandenburg2021) if every small-[[cocontinuous functor]] from $A$ has a [[right adjoint]]. Every strongly compact category is consequently compact.

## All large colimits

Despite its ill behaviour, it is possible to describe the cocompletion of a locally small category $A$ under large colimits (assuming the [[law of excluded middle]]): it is given by the [[functor category]] $[A^{op}, 2]$ where $2$ is the [[interval category]]. In particular, this gives rise to a [[lax-idempotent pseudomonad]] whose unit components are (unusually) not [[representably fully faithful]]. (One might argue this disqualifies it from being a "cocompletion" in the traditional sense.) See the discussion following Example 26 of [Walker](#Walker2019).

## Related pages

* [[total category]]

## References

* {#Isbell68} [[John Isbell]]. _Small subcategories and completeness_. Mathematical systems theory **2** 1 (1968) 27-50 &lbrack;[doi:10.1007/BF01691344](https://doi.org/10.1007/BF01691344)&rbrack;

* {#KellyKoubek1981} [[Max Kelly]] and V. Koubek. _The large limits that all good categories admit_. Journal of Pure and Applied Algebra 22.3 (1981): 253-263.

* {#Borger1981} [[Reinhard Börger]], [[Walter Tholen]], M. B. Wischnewsky & H. Wolff. _Compact and hypercomplete categories_. Journal of Pure and Applied Algebra 21.2 (1981): 129-144.

* {#Borger1990} [[Reinhard Börger]], [[Walter Tholen]]. _Total categories and solid functors_. Canadian Journal of Mathematics 42.2 (1990): 213–229.

* {#Kelly1986} [[Max Kelly]], _A survey of totality for enriched and ordinary categories_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 2 (1986), p. 109-132, [numdam](http://www.numdam.org/item?id=CTGDC_1986__27_2_109_0)

* {#BKR15} [[Michael Barr]], [[John Kennison]], [[Robert Raphael]], *On reflective and coreflective hulls*, [[Cahiers|Cahiers Topologie Géométrie Différentielle Catégorique]] **56** (2015) 162–208 &lbrack;[pdf](https://www.math.mcgill.ca/barr/papers/biref.pdf), [[BarrKennisonRaphael-Reflective.pdf:file]]&rbrack;

* {#Walker2019} [[Charles Walker]]. *Distributive laws via admissibility, Applied Categorical Structures **27** 6 (2019) 567-617

* {#LackTendas2023} [[Stephen Lack]] and [[Giacomo Tendas]]. _Virtual concepts in the theory of accessible categories_. [Journal of Pure and Applied Algebra 227.2 (2023): 107196.](https://doi.org/10.1016/j.jpaa.2022.107196)

* {#Brandenburg2021} [[Martin Brandenburg]]. _Large limit sketches and topological space objects_. [arXiv preprint 2106.11115](https://arxiv.org/abs/2106.11115) (2021).

* {#Hora2024} [[Ryuya Hora]], _Internal parameterization of hyperconnected quotients_, Theory and Applications of Categories 42.11 (2024): 263-313.

[[!redirects compact category]]
[[!redirects compact categories]]

[[!redirects local state classifier]]
[[!redirects local state classifiers]]
