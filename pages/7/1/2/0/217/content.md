
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The **Elementary Theory of the Category of Sets** ([Lawvere 65](#Lawvere65)), or _ETCS_ for short, is an axiomatic formulation of [[set theory]] in a [[category theory|category-theoretic]] spirit.  As such, it is the prototypical [[structural set theory]].  Supplemented with an axiomatization for categories it could be viewed as an approach to [[foundations]].[^Law]

[^Law]: It appears that Lawvere had intended ETCS more as a practical tool taking over the role of material sets in real mathematics i.e. a lightweight axiomatics providing _sets for mathematics_. Given his views on foundations (cf. [[practical foundations of mathematics]]) this claim is somewhat delicate to establish definitely but in general
foundational loads lie rather with his axiomatics [[ETCC]] for the [[CAT|category of category]] and in the context of his theory of [[cohesion]] he occasionally stresses the point that the base topos of structureless sets could actually be viewed as derived from within the cohesive [[gros topos]] thereby turning 'foundations' upside down. In any case, it seems useful to view ETCS not only as a competitor to ZFC foundations but also from a more relaxed vantage point as a regional axiomatics for (naive) set theory akin to e.g. [[Lawvere theories]] as categorified [[universal algebra]], that makes manifest the _structural side_ present in set theory since Cantor as suggested in ([Lawvere 94](#law94)).

More in detail, ETCS is a [[first-order theory]] axiomatizing [[elementary toposes]] and specifically those which are [[well-pointed topos|well-pointed]], have a [[natural numbers object]] and satisfy the [[axiom of choice]]. The idea is, first of all, that traditional mathematics naturally takes place "[[internal logic|inside]]" such a topos, and second that by varying the axioms much of mathematics may be done inside more general toposes: for instance omitting the [[well-pointed topos|well-pointedness]] and the [[axiom of choice]] but adding the [[Kock-Lawvere axiom]] gives a [[smooth topos]] inside which [[synthetic differential geometry]] takes place.

## Definition

The axioms of ETCS can be summed up in one sentence as:

+-- {: .num_defn}
###### Definition

The [[Set|category of sets]] is [[generalized the|the]] [[topos]] which

1. is a [[well-pointed topos]] 

1. has a [[natural numbers object]]

1. and satisfies the [[axiom of choice]].

=--

For more details see 

* [[fully formal ETCS]].

## A contemporary perspective

Modern mathematics with its emphasis on concepts from [[homotopy theory]] would more directly be founded in a similar spirit by an axiomatization not just of [[elementary toposes]] but of [[elementary (∞,1)-toposes]]. This is roughly what [[univalence|univalent]] [[homotopy type theory]] accomplishes -- for more on this see at _[relation between type theory and category theory -- Univalent HoTT and Elementary infinity-toposes](relation+between+type+theory+and+category+theory#HomotopyWithUnivalence)_.

Instead of increasing the [[higher category theory|higher categorical dimension]] [[(n,r)-category|(n,r)]] in the first argument, one may also, in this context of elementary foundations, consider raising the second argument. The case $(2,2)$ is the elementary theory of the 2-category of categories ([[ETCC]]).

## A Constructive View

[[Erik Palmgren]] ([Palmgren 2012](#Palmgren)) has a [[constructive mathematics|constructive]] [[predicative mathematics|predicative]] variant of ETCS, which can be summarized as:

$Set$ is a [[well-pointed topos|well-pointed]] $\Pi$-[[Π-pretopos|pretopos]] with a [[NNO]] and [[enough projectives]] (i.e. [[COSHEP]] is satisfied). Here "well-pointed" must be taken in its constructive sense, as including that the [[terminal object]] is indecomposable and projective.


## Todd Trimble's exposition of ETCS
 {#ExpositionByTrimble}

[[Todd Trimble]] has a series of expositional writings on ETCS which provide a very careful introduction and at the same time a wealth of useful details.

* Todd Trimble, _ZFC and ETCS: Elementary Theory of the Category of Sets_ ([[Trimble on ETCS I|nLab entry]],  [original blog entry](http://topologicalmusings.wordpress.com/2008/09/01/zfc-and-etcs-elementary-theory-of-the-category-of-sets/))

* Todd Trimble, _ETCS: Internalizing the logic_ ([[Trimble on ETCS II|nLab entry]], [original blog entry](http://topologicalmusings.wordpress.com/2008/09/10/etcs-internalizing-the-logic/))

* Todd Trimble, _ETCS: Building joins and coproducts_
([[Trimble on ETCS III|nLab entry]], [original blog entry](http://topologicalmusings.wordpress.com/2008/12/15/etcs-building-joins-and-coproducts/))

## Related entries

* [[fully formal ETCS]]
* [[structural set theory]]
* [[ZFC|Zermelo Fraenkel set theory]]
* [[ETCC]]

## References

ETCS grew out of Lawvere's experiences of teaching undergraduate set theoretic foundations at Reed college in 1963 and was originally published in 

* {#Lawvere65} [[William Lawvere]], _An elementary theory of the category of sets_, Proceedings of the National Academy of Science of the U.S.A **52** pp.1506-1511 (1965). ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC300477/pdf/pnas00186-0196.pdf))

A more or less contemporary review is

* C.C. Elgot , _Review_,  JSL **37** no.1 (1972) pp.191-192.

A longer version of Lawvere's 1965 paper appears in

* [[William Lawvere]], [[Colin McLarty]], _An elementary theory of the category of sets (long version) with commentary_, Reprints in Theory and Applications of Categories **11** (2005) pp. 1-35. ([TAC](http://tac.mta.ca/tac/reprints/articles/11/tr11abs.html))

An undergraduate set-theory textbook using it is

* [[William Lawvere]], [[Bob Rosebrugh|Robert Rosebrugh]], _Sets for Mathematics_ , Cambridge UP  2003. ([web](http://books.google.de/books?id=h3_7aZz9ZMoC&pg=PP1&dq=sets+for+mathematics))
{#LawvereRosebrugh}

On the anticipation of 'structural sets' in [[Georg Cantor|Cantor]]:

* [[William Lawvere]],  _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_, Philosophia Mathematica **2** no.3 (1994) pp.5-15. ([[LawvereCohesiveToposes.pdf:file]]) {#law94}

An informative discussion of the pros and cons of Lawvere's approach can be found in

* [[Jean-Pierre Marquis]], _Kreisel and Lawvere on Category Theory and the Foundations of Mathematics_ ([pdf-slides](http://www.math.mcgill.ca/rags/seminar/Marquis_KreiselLawvere.pdf))

Palmgren's ideas can be found here:

*  [[Erik Palmgren]], _Constructivist and Structuralist Foundations: Bishop's and Lawvere's Theories of Sets_ , Ann. Pure. App. Logic **163** no.10 (2012) pp.1384-1399. ([pdf](http://www.math.uu.se/~palmgren/cetcs.pdf)) {#Palmgren}

For the relation between the theory of well-pointed toposes and **weak Zermelo set theory** as elucidated by work of [[Julian Cole|J. Cole]], [[Barry Mitchell]], and [[Gerhard Osius|G. Osius]] in the early 1970s see

* [[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977 (Dover reprint 2014). (sections 9.2-3)

* [[Barry Mitchell]], _Boolean Topoi and the Theory of Sets_ , JPAA **2** (1972) pp.261-274.

* [[Gerhard Osius]], _Categorical Set Theory: A Characterization of the Category of Sets_ , JPAA **4** (1974) pp.79-119.


[[!redirects ETCS]]
[[!redirects etcs]]

[[!redirects elementary theory of the category of sets]]