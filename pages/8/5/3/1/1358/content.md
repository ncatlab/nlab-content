
#Contents#
* automatic table of contents goes here
{:toc}

## Idea


Pretriangulated dg-categories are models for [[stable (∞,1)-category|stable (∞,1)-categories]] in terms of [[differential graded category|dg-categories]], much like [[simplicially enriched category|simplicial categories]] are models for [[(∞,1)-category|(∞,1)-categories]].

The zeroth cohomology category of a pretriangulated dg-category is an ordinary [[triangulated category]], hence a morphism from $H^0(C)\to D$ where $C$ is a pretriangulated dg-category and $D$ a triangulated category is called an [[enhanced triangulated category|enhanced triangulated categories]].


## Definition

For $E$ 
a [[differential graded category|dg-category]]
let $PreTr(E)$ be its dg-category of [[twisted complex]]es.

$E$ is **pretriangulated** if for every [[twisted complex]] $K \in PreTr(E)$ the corresponding dg-functor

$$
  PreTr(-,K) : E^{op} \to C(Ab)
$$

is [[representable functor|representable]].

(is that right??)

**Proposition**

For $E$ a pretriangulated dg-category, the homotopy category $H^0(E)$ is naturally a [[triangulated category]]. 

The morphism

$$
  H^0(PreTr(E)) \to H^0(E)
$$

is an [[equivalence of categories|equivalence]] of [[triangulated category|triangulated categories]].


## References

* A. I. Bondal, [[Mikhail Kapranov]], Enhanced triangulated categories, &#1052;&#1072;&#1090;&#1077;&#1084;. &#1057;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082;, &#1058;&#1086;&#1084; 181 (1990), No.5, 669&#8211;683 (Russian); transl. in USSR Math. USSR Sbornik, vol. 70 (1991), No. 1, pp. 93&#8211;107, (MR91g:18010) ([[bondalKaprEnhTRiangCat.pdf:file]])

See [[enhanced triangulated category]] for more links to references.


[[!redirects pre-triangulated dg-category]]
[[!redirects pretriangulated dg-categories]]