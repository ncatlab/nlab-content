
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A __$(-1)$-groupoid__ or **[[homotopy n-type|(-1)-type]]** is a [[truth value]], or equivalently an [[n-truncated object of an (infinity,1)-category|(-1)-truncated object]] in [[∞Grpd]].  By [[excluded middle]], this is either [[the]] empty groupoid (false) or the [[terminal category|terminal groupoid]] (true, the [[point]]).


## Remarks

Compare the concept of [[0-groupoid]] (a [[set]]) and [[(-2)-groupoid]] (which is trivial). The point of $(-1)$-groupoids is that they complete some patterns in the [[periodic table]] of $n$-categories. (They also shed light on the theory of [[homotopy group]]s and [[n-stuff]].)

For example, there should be a $0$-[[0-category|category]] of $(-1)$-groupoids; a $0$-category is also a set, and this set is the set of [[truth value|truth values]]: classically
$$
  (-1)Grpd := \{\bot, \top\}
$$

Actually, since for other values of $n$, [[n-groupoid]]s form not just an $(n+1)$-category but an $(n+1,1)$-category, we should expect the $0$-category of $(-1)$-groupoids to be a $(0,1)$-category, or $1$-[[1-poset|poset]].  This simply means a [[partial order|poset]], and indeed truth values do always form a poset, classically ($\bot \leq \top$).

If we equip the category of $(-1)$-groupoids with the [[monoidal category|monoidal structure]] of [[logical conjunction|conjunction]] (the logical AND operation), then a [[enriched category|groupoid enriched]] over this is a [[symmetric proset]], and a category enriched over it is a [[preorder|proset]].  Up to [[equivalence of categories]], these are the same as a [[set]] (a $0$-[[0-groupoid|groupoid]]) and a [[partial order|poset]] (a (0,1)-[[1-poset|category]]); this fits the patterns of the periodic table.

See [[(-1)-category]] for more on this sort of [[negative thinking]].

## Related concepts

[[!include homotopy n-types - table]]


[[!redirects (-1)-groupoid]]
[[!redirects (-1)-groupoids]]
[[!redirects (-1)-groupoid]]
[[!redirects (-1)-groupoids]]

[[!redirects (-1)-type]]
[[!redirects (-1)-types]]
[[!redirects (-1)-type]]
[[!redirects (-1)-types]]
