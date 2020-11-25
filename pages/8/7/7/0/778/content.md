
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Differential graded categories_ or _dg-categories_ are linear analogues of [[spectral categories]]. In other words they are [[linear (infinity,1)-category|linear]] [[stable (infinity,1)-categories]]. It is common and useful to view them as [[enhanced triangulated categories]].

## Definition

A _dg-category_ over a [[commutative ring]] $k$ is an [[(infinity,1)-category]] [[enriched (infinity,1)-category|enriched]] in the [[(infinity,1)-category of chain complexes]] of $k$-[[modules]].  Equivalently, it is an ordinary category [[enriched category|strictly enriched]] in [[chain complexes]] (see [Haugseng 13](#Haugseng13)).

Hence a dg-category is a category with [[mapping complexes]] of morphisms between any two objects. By taking the [[homologies]] of these [[chain complexes]] in degree zero, one gets an ordinary category, called the [[homotopy category of a dg-category]].
Notice that a dg-category with a single object is the same thing as a [[dg-algebra]].

## Properties

### The (infinity,1)-category of dg-categories

The [[Dwyer-Kan model structure on dg-categories]] presents the [[(infinity,1)-category of dg-categories]].

### Relation to stable $\infty$-categories

By the [[stable Dold-Kan correspondence]], the [[(infinity,1)-category]] of dg-categories is equivalent to the [[(infinity,1)-category]] of [[(infinity,1)-categories]] [[enriched (infinity,1)-category|enriched]] in the [[symmetric monoidal (infinity,1)-category]] of [[module spectra|modules]] over the [[Eilenberg-Mac Lane spectrum]] $H k$.
The latter is equivalent, at least morally, to the [[(infinity,1)-category]] of $k$-[[linear (infinity,1)-category|linear]] [[stable (infinity,1)-categories]].

More precisely, it is shown in [Cohn 13](#Cohn13) that the [[Morita model structure on dg-categories]] presents the [[(infinity,1)-category]] of [[idempotent complete (infinity,1)-category|idempotent complete]] [[linear (infinity,1)-category|linear]] [[stable (infinity,1)-categories]].

## Aspects of dg-categories

* [[homotopy category of a dg-category]].
* [[equivalence of dg-categories]]
* [[dg-modules]], [[perfect dg-modules]]
* [[derived dg-category]]
* [[dg-Yoneda embedding]]
* [[pretriangulated dg-category]]
* [[dg-localization]], [[dg-quotient]]
* [[dg-nerve]]
* [[Waldhausen K-theory of a dg-category]]
* [[semi-topological K-theory of a dg-category]]
* [[derived moduli stack of objects in a dg-category]]

## Related concepts

* [[enhanced triangulated category]]
* [[A-infinity category]]
* [[spectral category]]
* [[stable (infinity,1)-category]]

## References

Historically, dg-categories were introduced in

* [[G. M. Kelly]], _Chain maps inducing zero homology maps_, Proc. Cambridge Philos. Soc. **61** (1965), 847&#8211;854, doi:[10.1017/S0305004100039207](https://doi.org/10.1017/S0305004100039207)

whilst their modern development can be traced to

*  [[A. I. Bondal]], [[Mikhail Kapranov]], _Enhanced triangulated categories_, &#1052;&#1072;&#1090;&#1077;&#1084;. &#1057;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082;, &#1058;&#1086;&#1084; 181 (1990), No.5, 669--683 (Russian); transl. in USSR Math. USSR Sbornik, vol. 70 (1991), No. 1, pp. 93--107, (MR91g:18010) ([[bondalKaprEnhTRiangCat.pdf:file]])

### Overviews

For concise reviews of the theory, see section 1 of

* [[A. Beilinson]], [[V. Vologodsky]], _DG guide to Voevodsky's motives_.

as well as the introduction and appendices to

* [[V. Drinfeld]], _DG quotients of DG categories_, [pdf](http://www.math.harvard.edu/~gaitsgde/grad_2009/DGquotients.pdf).

For longer surveys, see

* [[Bernhard Keller]], _On differential graded categories_  International Congress of Mathematicians. Vol. II,  151--190, Eur. Math. Soc., Z&#252;rich, 2006. ([arXiv](http://arxiv.org/abs/math/0601185))

and

* [[Bertrand Toën]], _Lectures on dg-categories_ ([pdf](https://perso.math.univ-toulouse.fr/btoen/files/2012/04/swisk.pdf)).

### Homotopy theory of dg-categories

The [[homotopy theory]] of [[dg-categories]] is studied in

* [[Gonçalo Tabuada]], _Homotopy theory of DG categories_, Thesis, Paris, 2007, [pdf](http://people.math.jussieu.fr/~keller/TabuadaThese.pdf).

* [[Gonçalo Tabuada]], _Une structure de cat&#233;gorie de mod&#232;les de Quillen sur la cat&#233;gorie des dg-cat&#233;gories_,  C. R. Math. Acad. Sci. Paris  340  (2005),  no. 1, 15--19.

The equivalence with the [[homotopy theory]] of [[stable (infinity,1)-categories]] is discussed in

* {#Cohn13} [[Lee Cohn]], _Differential Graded Categories are k-linear Stable Infinity Categories_ ([arXiv:1308.2587](http://arxiv.org/abs/1308.2587))

(Note that the proof works over any ring, even though it is stated there for [[characteristic zero]].)

In the following it is shown that the [[homotopy theory]] of [[(infinity,1)-categories]] enriched in the [[(infinity,1)-category]] of [[chain complexes]] is equivalent to the [[homotopy theory]] of ordinary categories strictly enriched in [[chain complexes]].

* {#Haugseng13} [[Rune Haugseng]], _Rectification of enriched infinity-categories_, [arXiv:1312.3881](http://arxiv.org/abs/1312.3881v2).

### Derived noncommutative geometry

The following references discuss the use of dg-categories in [[derived noncommutative algebraic geometry]] and [[noncommutative motives]].

* [[Gonçalo Tabuada]], _Invariants additifs de DG-cat&#233;gories_, Int. Math. Res. Not.  2005,  no. 53, 3309--3339; Addendum in Int. Math. Res. Not.  2006, Art. ID 75853, 3 pp. ; Erratum in Int. Math. Res. Not. IMRN  2007,  no. 24, Art. ID rnm149, 17 pp.

* [[Marco Robalo]], _Th&#233;orie homotopique motivique des espaces noncommutatifs_, [pdf](http://webusers.imj-prg.fr/~marco.robalo/these.pdf).

* S. Mahanta, _Noncommutative geometry in the framework of differential graded categories_, (<a href="http://arxiv.org/abs/0805.1628">arXiv:0805.1628</a>)

* D. Orlov, _Smooth and proper noncommutative schemes and gluing of DG categories_, Adv. Math. 302 (2014) [doi](https://dx.doi.org/10.1016/j.aim.2016.07.014)

### Other aspects

* [[Bernhard Keller]], _Deriving DG categories_,  Ann. Sci. &#201;cole Norm. Sup. (4)  27  (1994),  no. 1, 63--102 (<a href="http://www.numdam.org/item?id=ASENS_1994_4_27_1_63_0">numdam</a>)

* [[Dmitry Tamarkin]], _What do dg-categories form?_,
Compos. Math. 143 (2007), no. 5, 1335--1358. 

* [[Michael Batanin|M. Batanin]], _What do dg-categories form_ (after Tamarkin), talks at Paris 7 and Australian category seminar (<a href="http://www.maths.usyd.edu.au/u/AusCat/abstracts/060726mb.html">abstract</a>), [math.CT/0606553](http://arxiv.org/abs/math.CT/0606553)

* [[Oren Ben-Bassat]], [[Jonathan Block]], _Cohesive DG categories I: Milnor descent_, [arxiv/1201.6118](http://arxiv.org/abs/1201.6118)


[[!redirects dg-category]]
[[!redirects dg-categories]]
[[!redirects dg category]]
[[!redirects dg categories]]
[[!redirects DG-category]]
[[!redirects DG-categories]]
[[!redirects DG category]]
[[!redirects DG categories]]
[[!redirects differential graded category]]
[[!redirects differential graded categories]]