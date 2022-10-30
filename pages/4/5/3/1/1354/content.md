
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of an _enhanced triangulated category_ is a refinement of that of _[[triangulated category]]_ which remembers more of the full structure of a [[stable (∞,1)-category]] (see [Cohn 13](#Cohn13)).

[[triangulated category|Triangulated categories]] are a somewhat rough sort of a [[localization]], and lack some naturally expected properties, for example the functoriality of the [[mapping cones]]. Therefore, it has been a wish since the 1960s to replace or repair them with a more coherent structure. 

Good candidates at present are $A_\infty$-[[A-infinity-category|categories]], [[dg-categories]] and [[stable (∞,1)-categories]]. In practice, triangulated categories are still used to an extent, so one likes to have both the full structure and the underlying truncation which exists as a triangulated category in all three cases. 

It is known that all 3 approaches give the same result over a field of characteristic zero. The $dg$-enhancement is most documented and studied in genuine applications so far and is the first to be historically understood. 

Triangulated categories may arise as [[homotopy category of an (infinity,1)-category|homotopy categories]] of [[stable (infinity,1)-category|stable (∞,1)-categories]]. 

An _enhancement_ of a triangulated category to a
([[pretriangulated dg-category|pretriangulated]]) [[differential graded category]] may be, in characteristic zero, considered as a way to retain the information in the [[stable (∞,1)-category]]. Therefore in that case, the enhanced triangulated categories are models for [[stable (infinity,1)-category|stable (∞,1)-categories]] in terms of [[differential graded category|dg-categories]], much like [[simplicially enriched category|simplicial categories]] are models for [[(infinity,1)-category|(∞,1)-categories]].

## Related concepts

* [[triangulated category]]

* [[pretriangulated dg-category]], **enhanced triangulated category**

* [[stable derivator]]

* [[stable (∞,1)-category]] 

## References

It is well-known that the concept of a [[triangulated category]] is suffering many deficiencies for the purposes of [[homological algebra]], geometry and topology; and even categorical properties like the non-functoriality of the cones.  For that reason, Bondal and Kapranov in

*  [[Alexey Bondal|A. I. Bondal]], [[Mikhail Kapranov|M. M. Kapranov]], &#1054;&#1089;&#1085;&#1072;&#1097;&#1077;&#1085;&#1085;&#1099;&#1077; &#1090;&#1088;&#1080;&#1072;&#1085;&#1075;&#1091;&#1083;&#1080;&#1088;&#1086;&#1074;&#1072;&#1085;&#1085;&#1099;&#1077; &#1082;&#1072;&#1090;&#1077;&#1075;&#1086;&#1088;&#1080;&#1080;, &#1052;&#1072;&#1090;&#1077;&#1084;. &#1057;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082;, &#1058;&#1086;&#1084; 181 (1990), No.5, 669--683 [pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=sm&paperid=1196&what=fullt&option_lang=rus) (Russian); Engl. transl. _Enhanced triangulated categories_, USSR Math. USSR Sbornik, vol. 70 (1991), No. 1, pp. 93--107, (MR91g:18010) ([[bondalKaprEnhTRiangCat.pdf:file]])

introduce a notion of dg-enhancement of a triangulated category. 

A **dg-enhancement of a triangulated category** $T$ is a ([[pretriangulated dg-category|pretriangulated]]) [[differential graded category]] $A$ together with an equivalence $H^0(A)\to T$. The triangulated
category $T$ with that structure is called __enhanced__. According to the new results presented in

* Valery Lunts, _Uniqueness of enhancement for a triangulated category_, talk at Workshop on triangulated categories, Swansea, Wales, Dec 10-12, 2008, (report on a joint work with D. Orlov)

* [[Valery Lunts|V. A. Lunts]], [[Dmitri Orlov|D. O. Orlov]], _Uniqueness of enhancement for triangulated categories_, J. Amer. Math. Soc. __23__ (2010), 853-908, [journal](http://www.ams.org/journals/jams/2010-23-03/S0894-0347-10-00664-8/home.html), [arXiv:0908.4187](http://arxiv.org/abs/0908.4187).

the triangulated categories of [[quasicoherent sheaf|quasicoherent sheaves]] on quasiprojective varieties and some of their cousins (like categories of perfect complexes on quasiprojective varieties) have essentially unique dg-enhancements. F. Muro has developed an obstruction theory for the existance and measuring non-uniqueness of dg-enhancements in more general setting (unpublished).


The relation to [[stable (infinity,1)-categories]] is discussed in

* {#Cohn13} [[Lee Cohn]], _Differential Graded Categories are k-linear Stable Infinity Categories_ ([arXiv:1308.2587](http://arxiv.org/abs/1308.2587))

[[!redirects enhanced triangulated categories]]

[[!redirects DG enhancement]]
[[!redirects DG enhancements]]

[[!redirects dg enhancement]]
[[!redirects dg enhancements]]

[[!redirects DG-enhancement]]
[[!redirects DG-enhancements]]

[[!redirects dg-enhancement]]
[[!redirects dg-enhancements]]