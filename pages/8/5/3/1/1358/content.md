
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable Homotopy theory
+-- {: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea


Pretriangulated dg-categories are models for [[stable (∞,1)-category|stable (∞,1)-categories]] in terms of [[differential graded category|dg-categories]], much like [[simplicially enriched category|simplicial categories]] are models for [[(∞,1)-category|(∞,1)-categories]] (see ([Cohn 13](#Cohn13))).

The zeroth cohomology category of a pretriangulated dg-category is an ordinary [[triangulated category]], hence a morphism from $H^0(C)\to D$ where $C$ is a pretriangulated dg-category and $D$ a triangulated category is called an [[enhanced triangulated category|enhanced triangulated categories]].


## Definition

Let $E$ be a [[DG category]].

+-- {: .un_defn}
###### Definition
The **$n$-translation** of an object $X \in E$ is an object $X[n] \in E$ representing the functor
  $$ \Hom(\cdot, X)[n]. $$
The **cone** of a closed morphism $f : X \to Y$ of degree zero is an object $\Cone(f) \in E$ representing the functor
  $$ \Cone(\Hom(\cdot, X) \stackrel{f_*}{\to} \Hom(\cdot, Y)). $$
=--

+-- {: .un_defn}
###### Definition
$E$ is called **strongly pretriangulated** if it admits a [[zero object]], all translations of all objects, and all cones of all morphisms.
=--

+-- {: .num_prop}
###### Proposition
For every DG category $E$, there exists a strongly pretriangulated DG category $\PreTr(E)$ and a [[fully faithful]] DG functor $E \hookrightarrow \PreTr(E)$ such that for any DG functor $F: E \to E'$ to a strongly pretriangulated DG category $E'$, there exists a unique lift $\hat F : \PreTr(E) \to E'$.
=--

See below for a construction of $\PreTr(E)$.

+-- {: .un_defn}
###### Definition
The DG category $E$ is called **pretriangulated** if the induced functor $\H^0(E) \to \H^0(\PreTr(E))$ is an [[equivalence]].
=--

+-- {: .num_prop}
###### Proposition
For $E$ a pretriangulated dg-category, the homotopy category $H^0(E)$ is naturally a [[triangulated category]].
=--

+-- {: .num_prop}
###### Proposition
The morphism

$$
  H^0(PreTr(E)) \to H^0(E)
$$

is an [[equivalence of categories|equivalence]] of [[triangulated category|triangulated categories]].
=--

+-- {: .num_prop}
###### Proposition
If $F : E \to E'$ is a DG functor between two pretriangulated DG categories, then

* $F$ commutes with translation and preserves cones;
* the induced functor $H^0(F)$ is a [[triangulated category|triangulated functor]] on the [[homotopy category|homotopy categories]];
* $F$ is a [[quasi-equivalence of DG categories|quasi-equivalence]] if and only if $H^0(F)$ is a triangulated equivalence.
=--


## Definition using twisted complexes

For $E$ a [[differential graded category|dg-category]] let $PreTr(E)$ be its dg-category of [[twisted complex]]es.

$E$ is **pretriangulated** if for every [[twisted complex]] $K \in PreTr(E)$ the corresponding dg-functor

$$
  PreTr(-,K) : E^{op} \to C(Ab)
$$

is [[representable functor|representable]].

In other words, twisted complexes in $PreTr(E)$ have representatives in $E$.


## Related concepts

* [[triangulated category]]

* [[enhanced triangulated category]]

* [[stable derivator]]

* [[stable (∞,1)-category]]

## References

* A. I. Bondal, [[Mikhail Kapranov]], Enhanced triangulated categories, &#1052;&#1072;&#1090;&#1077;&#1084;. &#1057;&#1073;&#1086;&#1088;&#1085;&#1080;&#1082;, &#1058;&#1086;&#1084; 181 (1990), No.5, 669&#8211;683 (Russian); transl. in USSR Math. USSR Sbornik, vol. 70 (1991), No. 1, pp. 93&#8211;107, (MR91g:18010) ([[bondalKaprEnhTRiangCat.pdf:file]])

See _[[enhanced triangulated category]]_ for more links to references.

The relation to [[stable (infinity,1)-categories]] is discussed in

* {#Cohn13} [[Lee Cohn]], _Differential Graded Categories are k-linear Stable Infinity Categories_ ([arXiv:1308.2587](http://arxiv.org/abs/1308.2587))

[[!redirects pre-triangulated dg-category]]
[[!redirects pretriangulated dg-categories]]