
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

* [[MOFr]], [[MUFr]], [[MSUFr]]


## References

### On manifolds with boundary

* _Manifolds with boundary_ ([pdf](http://math.ucr.edu/~res/math260s10/manwithbdy.pdf), [[ManifoldsWithBoundary.pdf:file]])

On [[cobordism theory]] of [[MUFr]]-[[manifolds with boundaries]], their [[e-invariant]] and their appearance in the first line of the [[Adams-Novikov spectral sequence]]:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Section 16 of: _The relation of cobordism to $K$-theories_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))



### On manifolds with corners

* [[Klaus Jänich]], Section 1.2 of: _On the classification of $O(n)$-manifolds_, Math. Ann. 176, 53–76 (1968) ([doi:10.1007/BF02052956](https://doi.org/10.1007/BF02052956))


* [[Dominic Joyce]], _On manifolds with corners_ ([arXiv:0910.3518](http://arxiv.org/abs/0910.3518))

The [[full subcategory]]-embedding of manifolds with boundaries and corners into that of [[diffeological spaces]] is discussed in:

* {#IglesiasZemmour13} [[Patrick Iglesias-Zemmour]], section 4.16 of _Diffeology_, Mathematical Surveys and Monographs, AMS (2013) ([web](http://math.huji.ac.il/~piz/Site/The%20Book.html), [publisher](http://www.ams.org/bookstore-getitem/item=SURV-185))

* {#GurerIglesiasZemmour17} [[Serap Gürer]],  [[Patrick Iglesias-Zemmour]], _Differential forms on corners_, 2017  ([pdf](http://math.huji.ac.il/~piz/documents/DBlog-Rmk-DFOC.pdf))

* {#GurerIZ19} [[Serap Gürer]],  [[Patrick Iglesias-Zemmour]], _Differential forms on manifolds with boundary and corners_, Indagationes Mathematicae, Volume 30, Issue 5, September 2019, Pages 920-929 ([doi:10.1016/j.indag.2019.07.004](https://doi.org/10.1016/j.indag.2019.07.004))


On [[cobordism theory]] of [[manifolds with corners]]:

* Gerd Laures, _On cobordism of manifolds with corners_, Trans. Amer. Math. Soc. 352 (2000) ([doi:10.1090/S0002-9947-00-02676-3](https://doi.org/10.1090/S0002-9947-00-02676-3))

  > (their [[f-invariant]] and their appearance in the second line of the [[Adams-Novikov spectral sequence]])

* {#Genauer12} Josh Genauer, _Cobordism categories of manifolds with corners_, Transactions of the American Mathematical Society Vol. 364, No. 1 (2012), pp. 519-550 ([arXiv:0810.0581](https://arxiv.org/abs/0810.0581), [jstor:41407770](https://www.jstor.org/stable/41407770), [doi:10.1090/S0002-9947-2011-05474-7](https://doi.org/10.1090/S0002-9947-2011-05474-7))


[[!redirects manifold with boundaries]]
[[!redirects manifolds with boundary]]
[[!redirects manifolds with boundaries]]


[[!redirects manifold with corners]]
[[!redirects manifolds with corners]]

[[!redirects manifold with boundaries and corners]]
[[!redirects manifolds with boundaries and corners]]

[[!redirects smooth manifold with boundaries and corners]]
[[!redirects smooth manifolds with boundaries and corners]]


