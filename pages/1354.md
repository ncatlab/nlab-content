
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

Any [[stable (∞,1)-category]] $C$ gives rise to a canonical [[triangulated category]] $ho(C)$, its [[homotopy category of an (∞,1)-category|homotopy category]].  Much of the information contained in $C$ is still present in $ho(C)$, so that in many situations it can be enough to work at the level of [[triangulated categories]].  However, in general various problems with [[triangulated categories]] require one to work with some sort of higher structure lying above $ho(C)$.  Such a structure is often called an _enhancement_ of the [[triangulated category]] $ho(C)$.  Examples of enhanced triangulated categories are, in order of increasing information:

* [[stable derivators]],
* [[pretriangulated dg-categories]] or [[pretriangulated A-∞-categories]],
* and [[stable (∞, 1)-categories]] themselves.

## History

After [[Jean-Louis Verdier]] started the development of the theory of triangulated categories in his 1963 thesis, it was quickly recognized that some sort of enhancements were necessary to get the full picture.  For this purpose, [[Alexandre Grothendieck]] suggested the notion of [[derivator]] in the early 1980's, while [[Alexei Bondal]] and [[Mikhail Kapranov]] developed the notion of [[pretriangulated dg-category]] in 1990.  In 2006 [[Jacob Lurie]] developed the notion of [[stable (∞,1)-category]].

## Problems with triangulated categories

* non-functoriality of the [[mapping cone]],
* more generally, non-existence of [[homotopy colimits]] and [[homotopy limits]],
* ...

(to be expanded on)

## Comparison results

In [[pretriangulated dg-category#Cohn13|(Cohn 13)]] it is shown that the [[(∞,1)-category]] of  [[idempotent complete (infinity,1)-category|idempotent complete]] [[pretriangulated dg-categories]] over a [[commutative ring]] $k$ is equivalent to the [[(∞,1)-category]] of [[stable (∞,1)-category|stable]] [[k-linear (∞,1)-categories]].  See [[pretriangulated dg-category]] for details.

In [[derivator#Renaudin|(Renaudin 2006)]] it is shown that the [[2-category]] of locally presentable [[derivators]] is equivalent to the [[localization]] of the [[2-category]] of [[combinatorial model categories]] at the [[Quillen equivalences]].  [[combinatorial model categories|Combinatorial model categories]] are equivalent to [[locally presentable (∞,1)-categories]] in a sense made precise there.  However, a comparison between the stability conditions in the derivator and (∞,1)-category settings seems still to be open.

## Related concepts

* [[triangulated category]]

* [[stable derivator]]

* [[pretriangulated dg-category]], [[pretriangulated A-infinity category]]

* [[stable (∞,1)-category]] 

## References

* {#BondalKapranov91} [[Alexei Bondal]], [[Mikhail Kapranov]], _Enhanced Triangulated Categories_, Sbornik: Mathematics, Volume 70, Issue 1, pp. 93-107 (1991) ([doi:10.1070/SM1991v070n01ABEH001253](http://dx.doi.org/10.1070/SM1991v070n01ABEH001253))

* [[Valery Lunts|Valery A. Lunts]], [[Dmitri Orlov|Dmitri O. Orlov]], _Uniqueness of enhancement for triangulated categories_, J. Amer. Math. Soc. 23 (2010), no. 3, 853–908

* [[Benjamin Antieau]], _On the uniqueness of infinity-categorical enhancements of triangulated categories_, [arxiv/1812.01526](https://arxiv.org/abs/1812.01526)

Brief overview and list of further references:

* {#SchwedeHausmann19} [[Stefan Schwede]], [[Markus Hausmann]], _Enhancements of triangulated categories_, Graduate Seminar Topology, Bonn 2019-2020 ([[Schwede_EnhancedSeminar.pdf:file]])


[[!redirects enhanced triangulated categories]]

[[!redirects DG enhancement]]
[[!redirects DG enhancements]]

[[!redirects dg enhancement]]
[[!redirects dg enhancements]]

[[!redirects DG-enhancement]]
[[!redirects DG-enhancements]]

[[!redirects dg-enhancement]]
[[!redirects dg-enhancements]]