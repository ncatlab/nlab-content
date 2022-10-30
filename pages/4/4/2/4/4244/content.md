
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

An $n$-dimensional _Calabi-Yau variety_ is an $n$-dimensional [[Kähler manifold]] with ([[holomorphic line bundle|holomorphically]], rather than just topologically) trivial [[canonical bundle]]. This is equivalent to saying that it is real [[Riemannian manifold]] of even [[dimension]] $2 N$ which has [[special holonomy]] in the [[subgroup]] $SU(N)\subset O(2 N, \mathbb{R})$. 

For [[compact topological space|compact]] [[Kähler manifolds]], [[Yau's theorem]] (also known as the  [[Calabi conjecture]]) states any of the above conditions implies the vanishing of the first [[Chern class]].

+--{.query}
Is it also true for non-compact?
=--

Note that $c_1(X) = 0$ implies in general that the canonical bundle is *topologically trivial*. But if $X$ is a simply connected compact K&#228;hler manifold, $c_1(X) = 0$ implies further that the canonical bundle is *holomorphically trivial*.

+--{.query}
The language used in this article is implicitly analytic, rather than algebraic. Is this OK? Or should I make this explicit?
=--

## Definition

A Calabi-Yau variety can be described algebraically as a [[smooth scheme|smooth]] [[proper scheme|proper]] [[variety]] $X$ of [[dimension]] $n$ over a [[field]] $k$ (not necessarily [[algebraically closed field|algebraically closed]] and not necessarily of [[characteristic]] $0$) in which $\omega_X=\wedge^n\Omega^1\simeq \mathcal{O}_X$ and also $H^j(X, \mathcal{O}_X)=0$ for all $1\leq j \leq n-1$.

If the base field is $\mathbb{C}$, then one can form the analyticification of $X$ and obtain a [[compact space|compact]] [[manifold]] that satisfies the first given definition.

Beware that there are slightly different (and inequivalent) definitions in use. Notably in some contexts only the trivialization of the [[canonical bundle]] is required, but not the vanishing of the $H^{0 \lt \bullet \lt n}(X,\mathcal{O}_X)$. To be explicit on this one sometimes speaks for emphasis of "strict" CY varieties when including this condition.

## Examples

* in [[dimension]] 1: [[elliptic curve]]

* In [[dimension]] 2: [[K3 surface]].

## Properties

### In terms of $G$-structure

Calabi-Yau structure is equivalently [[integrability of G-structure|integrable]] [[G-structure]] for $G = $ [[SU(n)]].

Details are in [Prins 16, Prop. 1.3.2](#Prins16). 
See also [Vezzoni 06, p. 24](#Vezzoni06).

### Artin-Mazur formal group

Over an [[algebraically closed field]] of [[positive number|positive]] [[characteristic]] an $n$-dimensional Calabi-Yau variety $X$ has an [[Artin-Mazur formal group]] $\Phi^n_X$ which gives the [[deformation theory]] of the trivial [[line n-bundle]] over $X$.

See also ([Geer-Katsura 03](#GeerKatsura03)).

### As supersymmetric compactification spaces in string theory

* [[supersymmetry and Calabi-Yau manifolds]]

* [[heterotic string theory on CY3-manifolds]]

## Related concepts

[[!include special holonomy table]]


* [[Calabi-Yau object]]

  * [[Calabi-Yau algebra]], **Calabi-Yau manifold**, [[generalized Calabi-Yau manifold]]


* [[Calabi-Yau cohomology]]

* [[moduli space of Calabi-Yau spaces]] 

## References

The original articles are

* [[Shing-Tung Yau]], ...

(...)

Surveys and reviews include

* Scholarpedia, _[Calabi-Yau manifold](http://www.scholarpedia.org/article/Calabi-Yau_manifold)_

In terms of [[G-structure]]:

* {#Vezzoni06} Luigi Vezzoni, _The geometry of some special $SU(n)$-structure_, 2006 ([pdf](https://core.ac.uk/download/pdf/14699671.pdf), [[VezzoniSUnStructure.pdf:file]])

* {#Prins16} [[Daniël Prins]], Section 1.3 of: _On flux vacua, $SU(n)$-structures and generalised complex geometry_, Université Claude Bernard -- Lyon I, 2015.  ([arXiv:1602.05415](https://arxiv.org/abs/1602.05415), [tel:01280717](https://tel.archives-ouvertes.fr/tel-01280717))

Discussion of the case of [[positive number|positive]] [[characteristic]] includes

* {#GeerKatsura03} [[Gerard van der Geer]], T. Katsura, _On the height of Calabi-Yau varieties in positive characteristic_ ([arXiv:math/0302023](http://arxiv.org/abs/math/0302023))


The following page collects information on Calabi-Yau manifolds with an eye to application in [[string theory]] (e.g. [[supersymmetry and Calabi-Yau manifolds]]):

* [[Sheldon Katz]], [[Rolf Schimmrigk]], Andreas Wi&#223;kirchen, _[CALABI-YAU](http://www.th.physik.uni-bonn.de/th/Supplements/cy.html)_

Discussion of the relation between the various shades of definitions includes

* MathOverflow: _[Calabi-Yau manifolds](http://mathoverflow.net/q/42707/381)_

Mathematical review of the relation to  [[quiver representations]] and [[mirror symmetry]] includes

* Yang-Hui He, _Calabi-Yau Varieties: from Quiver Representations to Dessins d'Enfants_ ([arXiv:1611.09398](https://arxiv.org/abs/1611.09398))

Discussion of CYs in [[positive characteristic]] includes

* [[Philip Candelas]], [[Xenia de la Ossa]], Fernando Rodriguez-Villegas, _Calabi-Yau Manifolds Over Finite Fields, I_ ([arXiv:hep-th/0012233](http://arxiv.org/abs/hep-th/0012233))

* [[Philip Candelas]], [[Xenia de la Ossa]], Fernando Rodriguez-Villegas, _Calabi-Yau Manifolds Over Finite Fields, II_ ([arXiv:hep-th/0402133](http://arxiv.org/abs/hep-th/0402133))

Discussion of [[Calabi-Yau orbifolds]]:

* [[Dominic Joyce]], _On the topology of desingularizations of Calabi-Yau orbifolds_ ([arXiv:math/9806146](https://arxiv.org/abs/math/9806146), [spire:485280](https://inspirehep.net/literature/485280))

* [[Dominic Joyce]], _Deforming Calabi-Yau orbifolds_, Asian Journal of Mathematics 3.4 (1999): 853-868 ([doi:10.4310/AJM.1999.v3.n4.a7](https://dx.doi.org/10.4310/AJM.1999.v3.n4.a7) [pdf](https://www.intlpress.com/site/pub/files/_fulltext/journals/ajm/1999/0003/0004/AJM-1999-0003-0004-a007.pdf))

and in view of [[mirror symmetry]]:

* Shi-Shyr Roan, _The mirror of Calabi-Yau orbifold_,  International Journal of Mathematics Vol. 02, No. 04, pp. 439-455 (1991)  ([doi:10.1142/S0129167X91000259](https://doi.org/10.1142/S0129167X91000259))

* Alan Stapledon, _New mirror pairs of Calabi-Yau orbifolds_,  Adv. Math. 230 (2012), no. 4-6, 1557-1596 ([arXiv:1011.5006](https://arxiv.org/abs/1011.5006))

[[!redirects Calabi-Yau]]
[[!redirects Calabi–Yau]]
[[!redirects Calabi--Yau]]

[[!redirects Calabi-Yau structure]]
[[!redirects Calabi-Yau structures]]

[[!redirects Calabi-Yau space]]
[[!redirects Calabi-Yau spaces]]
[[!redirects Calabi–Yau space]]
[[!redirects Calabi–Yau spaces]]
[[!redirects Calabi--Yau space]]
[[!redirects Calabi--Yau spaces]]

[[!redirects Calabi-Yau manifold]]
[[!redirects Calabi-Yau manifolds]]
[[!redirects Calabi–Yau manifold]]
[[!redirects Calabi–Yau manifolds]]
[[!redirects Calabi--Yau manifold]]
[[!redirects Calabi--Yau manifolds]]

[[!redirects Calabi-Yau orbifold]]
[[!redirects Calabi-Yau orbifolds]]
[[!redirects Calabi–Yau orbifold]]
[[!redirects Calabi–Yau orbifolds]]
[[!redirects Calabi--Yau orbifold]]
[[!redirects Calabi--Yau orbifolds]]


[[!redirects Calabi-Yau variety]]
[[!redirects Calabi-Yau varieties]]
[[!redirects Calabi–Yau variety]]
[[!redirects Calabi–Yau varieties]]
[[!redirects Calabi--Yau variety]]
[[!redirects Calabi--Yau varieties]]