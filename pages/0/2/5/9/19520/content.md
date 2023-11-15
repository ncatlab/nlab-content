+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

*This page is about double categories. For the use of 'tight' and 'loose' in the context of [[F-categories]], see there.*

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[double category|double category theory]], *vertical/horizontal* or *tight/loose* are terminologies used to distinguish the two kinds of 1-cells comprising a [[double category]].

Since a double category $\mathbb{D}$ is a [[internal category|category internal to]] $\mathbf{Cat}$, it comes with two kinds of 1-cells: the ones between objects of $\mathbb{D}_0$ (called *tight*) and the ones which are the objects of $\mathbb{D}_1$ (called *loose*).
As explained in [[double category]], *loose* cells are the protagonists in the specification of the internal category structure, since such structure tells us (1) what are their boundaries, (2) which one are the identities and (3) how they compose.

Historically, double categories were defined to be *strict* internal categories hence you could freely swap tight and loose directions without mathematical consequences (see (§3.2.2, §3.2.5, [Grandis 2019](#Grandis19)). Recently, however, double categories are more commonly defined to be [[internal pseudocategories]], meaning the category structure on the loose arrows is associative and unital only up to coherent isomorphism. As a consequence, loose cells do not organize in a category anymore, instead yielding a bicategory. Thus loose and tight cells are nowadays qualitatively different kinds of 1-cells and cannot be swapped (loose morphisms couldn't form an object of $\mathbf{Cat}$).

The interplay between the weakness of loose cells and the strictness of tight cells is a major principle of double category theory (extending to [[multiple categories|multiple category theory]] too). Since the lack of strictness in the loose direction is described in terms of tight cells instead of other loose cells, double categories are tamer 2-dimensional structures than [[bicategories]]. For instance [[monoidal double categories]] (and other algebraic structures) are generally easier to define than [[monoidal bicategories]] (see refs [[monoidal double categories|here]]), or the fact lax [[double functors]] form a double category in a more natural way than lax [[2-functors]] form a 2-category (see at [[icons]]).

## Notation and terminology
Since 2-cells in double categories are naturally denoted by squares, their boundary 1-cells are predominantly referred to of 'horizontal' and 'vertical'.
This terminology is the most common in the published literature, albeit used inconsistently (i.e. sometimes vertical corresponds to loose, chiefly in Grandis and Parè's papers, sometimes to tight). As discussed above, the modern usage of double categories doesn't allow one to swap loose and tight cells freely, hence confusing vertical for horizontal is not just a nuisance but could make the difference between a true and a false theorem.

The terminology 'tight' and 'loose' comes from the world of [[F-categories]], in particular from ([Lack and Shulman, 2012](#LackShulman12)). In that setting tight arrows are a special kind of loose arrows, but in the broader setting of double category theory that doesn't have to be the case.

Relatedly, in a [[framed bicategory]] loose 1-cells are called 'proarrows' and tight 1-cells are called arrows. That's because framed bicategories present [[proarrow equipments]].

|**1-cells in $\mathbb{D}_0$**|**0-cells in $\mathbb{D}_1$**| |
|--|--|--|
|longitudinal|lateral|([Ehresmann 1963](#Ehresmann63))|
|horizontal|vertical|Dawson and Paré; Grandis and Paré|
|vertical|horizontal|([Leinster 2004](#Lein04)), ([Cruttwell and Shulman, 2010](#CS10))|
|tight|loose|([Lack and Shulman 2012](#LackShulman12))|
|dynamic|static|([Grandis 2019](#Grandis19))|
|transversal|1-objects|([Grandis 2019](#Grandis19))|

## Examples

1. In the double category [[Rel|$\mathbf{\mathbb{R}el}$]] of sets, functions, relations and inclusions, functions are the tight cells and relations are the loose ones
2. In the double category [[profunctors|$\mathbf{\mathbb{P}rof}$]] of small categories, functors, profunctors and natural transformations, functors are the tight cells and profunctors are the loose ones

## Related concepts

* [[double category]]
* [[framed bicategory]]

## References

(Strict) double categories were introduced in

* [[Charles Ehresmann]], *Catégories double et catégories structurées*, C.R. Acad. Paris 256 (1963) 1198-1201 &lbrack;[[Ehresmann-CategoriesDoubles.pdf:file]], [gallica](https://gallica.bnf.fr/ark:/12148/bpt6k3208j/f1246)&rbrack;

where the two kinds of 1-cells were called longitudinal and lateral.

The less notationally-bound terminology tight/loose was introduced by

* {#LackShulman12} [[Steve Lack]], [[Mike Shulman]], _Enhanced 2-categories and limits for lax morphisms_, Advances in Mathematics, vol. 229, 2012, ([arxiv:1104.2111](https://arxiv.org/abs/1104.2111), [doi:j.aim.2011.08.014](https://doi.org/10.1016/j.aim.2011.08.014))

Other references:

* {#Grandis19} [[Marco Grandis]], _Higher dimensional categories: from double to multiple categories_, World Scientific, 2019. ([doi:10.1142/11406](https://doi.org/10.1142/11406))

* {#CS10} [[Geoffrey Cruttwell]], [[Mike Shulman]], _A unified framework for generalized multicategories_, TAC, vol. 24, 21, 2010, ([arxiv:0907.2460](https://arxiv.org/abs/0907.2460)), ([tac](http://www.tac.mta.ca/tac/volumes/24/21/24-21abs.html))

* {#Lein04} [[Tom Leinster]], *Higher operads, higher categories*, London Math. Soc. Lec. Note Series **298**, Cambridge University Press (2004) &lbrack;[math.CT/0305049](http://arxiv.org/abs/math.CT/0305049), [doi:10.1017/CBO9780511525896](https://doi.org/10.1017/CBO9780511525896)&rbrack;

[[!redirects horizontal morphism]]
[[!redirects horizontal morphisms]]
[[!redirects vertical morphism]]
[[!redirects vertical morphisms]]
[[!redirects loose morphism]]
[[!redirects tight morphism]]
[[!redirects loose morphisms]]
[[!redirects tight morphisms]]
[[!redirects tight]]
[[!redirects loose]]
