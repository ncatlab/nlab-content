
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

An $n$-dimensional _Calabi-Yau variety_ is an $n$-dimensional [[Kähler manifold]] with (holomorphically, rather than topologically) trivial [[canonical bundle]]. This is equivalent to saying that it is real [[Riemannian manifold]] of even [[dimension]] $2 N$ which has [[special holonomy]] in the [[subgroup]] $SU(N)\subset O(2 N, \mathbb{R})$. 

For [[compact topological space|compact]] [[Kähler manifolds]], [[Yau's theorem]] (also known as the  [[Calabi conjecture]]) implies that the above conditions are also equivalent to the vanishing of the first [[Chern class]].

+--{.query}
Is it also true for non-compact?
=--

Note that $c_1(X) = 0$ implies in general that the canonical bundle is *topologically trivial*. But if $X$ is a compact K&#228;hler manifold, $c_1(X) = 0$ implies further that the canonical bundle is *holomorphically trivial*.

+--{.query}
The language used in this article is implicitly analytic, rather than algebraic. Is this OK? Or should I make this explicit?
=--

## Definition

A Calabi-Yau variety can be described algebraically as a [[smooth scheme|smooth]] [[proper scheme|proper]] [[variety]] $X$ of [[dimension]] $n$ over a [[field]] $k$ (not necessarily [[algebraically closed field|algebraically closed]] and not necessarily of [[characteristic]] $0$) in which $\omega_X=\wedge^n\Omega^1\simeq \mathcal{O}_X$ and also $H^j(X, \mathcal{O}_X)=0$ for all $1\leq j \leq n-1$.

If the base field is $\mathbb{C}$, then one can form the analyticification of $X$ and obtain a [[compact space|compact]] [[manifold]] that satisfies the first given definition.

Beware that there are slighlty different (and inequivalent) definitions in use. Notably in some contexts only the trivialization of the [[canonical bundle]] is required, but not the vanishing of the $H^{0 \lt \bullet \lt n}(X,\mathcal{O}_X)$. To be explicit on this one sometimes speaks for emphasis of "strict" CY varieties when including this condition.

## Examples

* in [[dimension]] 1: [[elliptic curve]]

* In [[dimension]] 2: [[K3 surface]].

## Properties

### Artin-Mazur formal group

Over an [[algebraically closed field]] of [[positive number|positive]] [[characteristic]] an $n$-dimensional Calabi-Yau variety $X$ has an [[Artin-Mazur formal group]] $\Phi^n_X$ which gives the [[deformation theory]] of the trivial [[line n-bundle]] over $X$.

See also ([Geer-Katsura 03](#GeerKatsura03)).

### As supersymmetric compactification spaces in string theory

* [[supersymmetry and Calabi-Yau manifolds]]


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

Discussion of the case of [[positive number|positive]] [[characteristic]] includes

* {#GeerKatsura03} [[Gerard van der Geer]], T. Katsura, _On the height of Calabi-Yau varieties in positive characteristic_ ([arXiv:math/0302023](http://arxiv.org/abs/math/0302023))


The following page collects information on Calabi-Yau manifolds with an eye to application in [[string theory]] (e.g. [[supersymmetry and Calabi-Yau manifolds]]):

* [[Sheldon Katz]], [[Rolf Schimmrigk]], Andreas Wi&#223;kirchen, _[CALABI-YAU](http://www.th.physik.uni-bonn.de/th/Supplements/cy.html)_

Discussion of the relation between the various shades of definitions includes

* MathOverflow: _[Calabi-Yau manifolds](http://mathoverflow.net/q/42707/381)_

[[!redirects Calabi-Yau]]
[[!redirects Calabi–Yau]]
[[!redirects Calabi--Yau]]

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

[[!redirects Calabi-Yau variety]]
[[!redirects Calabi-Yau varieties]]
[[!redirects Calabi–Yau variety]]
[[!redirects Calabi–Yau varieties]]
[[!redirects Calabi--Yau variety]]
[[!redirects Calabi--Yau varieties]]