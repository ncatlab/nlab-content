
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


A [[manifold]] is a [[topological space]] that is locally isomorphic to a [[Cartesian space]] $\mathbb{R}^n$.

A **manifold with [[boundary]]** is a topological space that is locally isomorphic either to an $\mathbb{R}^n$ or to a **half-space** $H^n = \{ \vec x \in \mathbb{R}^n | x^n \geq 0\}$.

A **manifold with corners** is a topological space that is locally isomorphic to an $H^n_i = \{ \vec x \in \mathbb{R}^n | x^{i+1}, \cdots, x^n \geq 0\}$ for $0 \leq i \leq n$.

For details see at _[[manifold]]_.

## Properties

### Collar neighbourhood theorem

* [[collar neighbourhood theorem]]

### Embedding into the category of diffeological spaces

+-- {: .num_prop #SmoothManifoldsWithBoundaryEmbedIntoDiffeologicalSpaces}
###### Proposition
**([[manifolds with boundaries and corners]] form [[full subcategory]] of [[diffeological spaces]])**

The evident [[functor]]

$$
  SmthMfdWBdrCrn \overset{\phantom{AAAA}}{\hookrightarrow} DiffeologicalSpaces
$$

from the [[category]] of [[smooth manifold|smooth]] [[manifolds with boundaries and corners]] to that of [[diffeological spaces]] is [[fully faithful functor|fully faithful]], hence is a [[full subcategory]]-embedding.

=--

([Iglesias-Zemmour 13, 4.16](#IglesiasZemmour13), [Gürer & Iglesias-Zemmour 19](#GurerIZ19))

## Related concepts

* [[asymptotic boundary]]

* [[manifold with corners]]

* [[closed manifold]]



## References


* _Manifolds with boundary_ ([pdf](http://math.ucr.edu/~res/math260s10/manwithbdy.pdf), [[ManifoldsWithBoundary.pdf:file]])

* [[Dominic Joyce]], _On manifolds with corners_ ([arXiv:0910.3518](http://arxiv.org/abs/0910.3518))

The [[full subcategory]]-embedding of manifolds with boundaries and corners into that of [[diffeological spaces]] is discussed in:

* {#IglesiasZemmour13} [[Patrick Iglesias-Zemmour]], section 4.16 of _Diffeology_, Mathematical Surveys and Monographs, AMS (2013) ([web](http://math.huji.ac.il/~piz/Site/The%20Book.html), [publisher](http://www.ams.org/bookstore-getitem/item=SURV-185))

* {#GurerIglesiasZemmour17} [[Serap Gürer]],  [[Patrick Iglesias-Zemmour]], _Differential forms on corners_, 2017  ([pdf](http://math.huji.ac.il/~piz/documents/DBlog-Rmk-DFOC.pdf))

* {#GurerIZ19} [[Serap Gürer]],  [[Patrick Iglesias-Zemmour]], _Differential forms on manifolds with boundary and corners_, Indagationes Mathematicae, Volume 30, Issue 5, September 2019, Pages 920-929 ([doi:10.1016/j.indag.2019.07.004](https://doi.org/10.1016/j.indag.2019.07.004))

[[!redirects manifolds with boundary]]

[[!redirects manifold with corners]]
[[!redirects manifolds with corners]]

[[!redirects manifold with boundaries and corners]]
[[!redirects manifolds with boundaries and corners]]

[[!redirects smooth manifold with boundaries and corners]]
[[!redirects smooth manifolds with boundaries and corners]]


