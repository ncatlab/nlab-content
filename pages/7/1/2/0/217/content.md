
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

The **Elementary Theory of the Category of Sets**, or _ETCS_ for short, is an axiomatic formulation of [[set theory]] in a [[category theory|category-theoretic]] spirit.  As such, it is the prototypical [[structural set theory]]. Proposed shortly after [[ETCC]] in ([Lawvere 64](#Lawvere64)) it is also the paradigm for a [[foundations|categorical foundation]] of mathematics.[^Law]

The theory intends to capture in an invariant way the notion of a (constant) _'abstract set'_ whose elements lack internal structure and whose only external property is cardinality with further external relations arising from _mappings_. The membership relation is _local_ and _relative_ i.e. membership is meaningful only between an element of a set and a subset of the very same set. (See [Lawvere (1976, p.119)](#Lawvere76) for a detailed description of the notion 'abstract set'.[^cantor] [^dedekind] [^schoenflies] [^vonneumann])

[^cantor]: It has been pointed out by John Myhill that Cantor's concept of 'cardinal' as a set of abstract units should be viewed as a structural set theory and a precursor to Lawvere's concept of an 'abstract set'. This view is endorsed and expanded in [Lawvere 1994](#Lawvere94). 

[^dedekind]: [[Richard Dedekind| R. Dedekind's]] views are also anticipating 'abstract sets' e.g. Bernstein reports in Dedekind's works vol.3 (1932, p.449) that Dedekind gave as his intuition of a set: "a closed bag, containing determinate things that one can not see and of which one knows nothing beyond their existence and determinateness".

[^schoenflies]: The first axiomatic set theory without primitive membership relation $\in$ was presumably proposed by A. Schoenflies in 1920: he modeled elements of sets as indecomposable subsets. See A. Schoenflies, _Zur Axiomatik der Mengenlehre_ , Math. Ann. **83** (1921) pp.173-200; and _Bemerkung zur Axiomatik der Gr&#246;ssen und Mengen_ , Math. Ann. **85** (1922) pp.60-64.

[^vonneumann]: The first axiomatic set theory based on the notion of function was [[John von Neumann|von Neumann]]'s 1925 version of what later became the set based [[NBG]] theory of classes.

[^Law]: For a comparative discussion of its virtues as foundation see [[foundations of mathematics]] , the [texts by Todd Trimble](#ExpositionByTrimble) or the informative paper by [McLarty (2004)](#McLarty04).

More in detail, ETCS is a [[first-order theory]] axiomatizing [[elementary toposes]] and specifically those which are [[well-pointed topos|well-pointed]], have a [[natural numbers object]] and satisfy the [[axiom of choice]]. The theory omits the [[axiom of replacement]], however.

The idea is, first of all, that much of traditional mathematics naturally takes place "[[internal logic|inside]]" such a topos of _constant_ sets, and second that this perspective generalizes beyond ETCS proper to toposes of _variable_ and _cohesive_ sets by varying the axioms: for instance omitting the [[well-pointed topos|well-pointedness]] and the [[axiom of choice]] but adding the [[Kock-Lawvere axiom]] gives a [[smooth topos]] inside which [[synthetic differential geometry]] takes place.

That is, ETCS locates the category of sets by the well-pointedness axiom as the discrete zero point on a 'continuous' range of toposes eligible for foundations. In particular, whereas ZF mainly provides 'substance' for mathematics, ETCS lives as a special type of form within the continuum of mathematical form itself.

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

## A constructive view

[[Erik Palmgren]] ([Palmgren 2012](#Palmgren)) has a [[constructive mathematics|constructive]] [[predicative mathematics|predicative]] variant of ETCS, which can be summarized as:

$Set$ is a [[well-pointed topos|well-pointed]] $\Pi$-[[Π-pretopos|pretopos]] with a [[NNO]] and [[enough projectives]] (i.e. [[COSHEP]] is satisfied). Here "well-pointed" must be taken in its constructive sense, as including that the [[terminal object]] is indecomposable and projective.

## A contemporary perspective

Modern mathematics with its emphasis on concepts from [[homotopy theory]] would more directly be founded in a similar spirit by an axiomatization not just of [[elementary toposes]] but of [[elementary (∞,1)-toposes]]. This is roughly what [[univalence|univalent]] [[homotopy type theory]] accomplishes -- for more on this see at _[relation between type theory and category theory -- Univalent HoTT and Elementary infinity-toposes](relation+between+type+theory+and+category+theory#HomotopyWithUnivalence)_.

Instead of increasing the [[higher category theory|higher categorical dimension]] [[(n,r)-category|(n,r)]] in the first argument, one may also, in this context of elementary foundations, consider raising the second argument. 
The case $(2,2)$ is the elementary theory of the 2-category of categories ([[ETCC]]).


## Todd Trimble's exposition of ETCS
 {#ExpositionByTrimble}

[[Todd Trimble]] has a series of expository writings on ETCS which provide a very careful introduction and at the same time a wealth of useful details.

* Todd Trimble, _ZFC and ETCS: Elementary Theory of the Category of Sets_ ([[Trimble on ETCS I|nLab entry]],  [original blog entry](http://topologicalmusings.wordpress.com/2008/09/01/zfc-and-etcs-elementary-theory-of-the-category-of-sets/))

* Todd Trimble, _ETCS: Internalizing the logic_ ([[Trimble on ETCS II|nLab entry]], [original blog entry](http://topologicalmusings.wordpress.com/2008/09/10/etcs-internalizing-the-logic/))

* Todd Trimble, _ETCS: Building joins and coproducts_
([[Trimble on ETCS III|nLab entry]], [original blog entry](http://topologicalmusings.wordpress.com/2008/12/15/etcs-building-joins-and-coproducts/))

## Related entries

* [[fully formal ETCS]]
* [[structural set theory]]
* [[ZFC|Zermelo Fraenkel set theory]]
* [[Cohesive Toposes and Cantor's "lauter Einsen"]]
* [[axiom of replacement]]
* [[ETCC]]
* [[practical foundations of mathematics]]
* [[foundations of mathematics]]

## References

ETCS grew out of Lawvere's experiences of teaching undergraduate foundations of analysis at Reed college in 1963 and was originally published in 

* {#Lawvere64} [[William Lawvere]], _An elementary theory of the category of sets_ , Proceedings of the National Academy of Science of the U.S.A **52** pp.1506-1511 (1964). ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC300477/pdf/pnas00186-0196.pdf))

A more or less contemporary review is

* C.C. Elgot, _Review_,  JSL **37** no.1 (1972) pp. 191-192.

A longer version of Lawvere's 1964 paper appears in

* [[William Lawvere]], [[Colin McLarty]], _An elementary theory of the category of sets (long version) with commentary_ , Reprints in Theory and Applications of Categories **11** (2005) pp. 1-35. ([TAC](http://tac.mta.ca/tac/reprints/articles/11/tr11abs.html))

An undergraduate set-theory textbook using it is

* {#LawvereRosebrugh} [[William Lawvere]], [[Robert Rosebrugh]], _[[Sets for Mathematics]]_ , CUP  2003. ([web](http://books.google.de/books?id=h3_7aZz9ZMoC&pg=PP1&dq=sets+for+mathematics))

Lawvere explains in detail his views on constant and variable 'abstract sets' on pp.118-128 of 

* {#Lawvere76} [[William Lawvere]], _Variable Quantities and Variable Structures in Topoi_ , pp.101-131 in Heller, Tierney (eds.), _Algebra, Topology and Category Theory: a Collection of Papers in Honor of Samuel Eilenberg_ , Academic Press New York 1976.

See also ch. 2,3 of 

* [[William Lawvere]], _Variable Sets Entendu and Variable Structure in Topoi_ , lecture notes University of Chicago 1975.

On the anticipation of 'abstract sets' in [[Georg Cantor|Cantor]]:

* {#Lawvere94}[[William Lawvere]],  _[[Cohesive Toposes and Cantor's "lauter Einsen"]]_, Philosophia Mathematica **2** no.3 (1994) pp.5-15. ([[LawvereCohesiveToposes.pdf:file]]) {#law94}

A short overview article on ETCS:

* [[Tom Leinster]], _Rethinking set theory_ [arXiv](http://arxiv.org/abs/1212.6543).

An insightful and non-partisan view of ETCS can be found in a section of:

* [[Andreas Blass]], Yuri Gurevich, _Why Sets ?_ , Bull. Europ. Assoc. Theoret. Comp. Sci. **84** (2004) 139-156.  ([draft](http://www.math.lsa.umich.edu/~ablass/set.pdf))

An extended discussion from a philosophical perspective is in

* {#McLarty04}[[Colin McLarty]], _Exploring Categorical Structuralism_ , Phil. Math. **12** (2004) 37-53.

* Øystein Linnebo, Richard Pettigrew, _Category theory as an autonomous foundation_, Phil. Math. **19** (2011) 227–254 ([doi:10.1093/philmat/nkr024](https://doi.org/10.1093/philmat/nkr024),  [preprint version (pdf)](http://philsci-archive.pitt.edu/5392/1/onlyuptoiso.pdf)) 

For a more recent review from a critical perspective containing additional recent references see

* [[Solomon Feferman]], _Foundations of Unlimited Category Theory: What Remains to be Done_ , Review of Symbolic Logic **6** no.1 (2013) 6-15. ([pdf](http://math.stanford.edu/~feferman/papers/FCT-RSL-2013.pdf))

An informative discussion of the pros and cons of Lawvere's approach can be found in

* [[Jean-Pierre Marquis]], _Kreisel and Lawvere on Category Theory and the Foundations of Mathematics_ . ([pdf-slides](http://www.math.mcgill.ca/rags/seminar/Marquis_KreiselLawvere.pdf))

Palmgren's ideas can be found here:

*  [[Erik Palmgren]], _Constructivist and Structuralist Foundations: Bishop's and Lawvere's Theories of Sets_ , Ann. Pure. App. Logic **163** no.10 (2012) 1384-1399. ([pdf](http://www.math.uu.se/~palmgren/cetcs.pdf)) {#Palmgren}

For the relation between the theory of well-pointed toposes and **weak Zermelo set theory** as elucidated by work of [[Julian Cole|J. Cole]], [[Barry Mitchell]], and [[Gerhard Osius|G. Osius]] in the early 1970s see

* [[Peter Johnstone]], _Topos Theory_ , Academic Press New York 1977 (Dover reprint 2014). (sections 9.2-3)

* [[Barry Mitchell]], _Boolean Topoi and the Theory of Sets_ ,  JPAA **2** (1972) pp.261-274.

* [[Gerhard Osius]], _Categorical Set Theory: A Characterization of the Category of Sets_,  JPAA **4** (1974) 79-119.


[[!redirects ETCS]]
[[!redirects etcs]]
[[!redirects elementary theory of the category of sets]]