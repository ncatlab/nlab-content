

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The collection of all [[(∞,1)-categories]] forms naturally the [[(∞,2)-category]] [[(∞,1)Cat]]. 
But for many purposes it is quite sufficient to regard only invertible [[natural transformations]] between [[(∞,1)-functor]], which means that one needs just the maximal [[(∞,1)-category]] inside that $(\infty,2)$-category of all $(\infty,1)$-categories.

Given that an $(\infty,1)$-category is a context for abstract [[homotopy theory]], the $(\infty,1)$-category of $(\infty,1)$-categories is also called the the _homotopy theory of homotopy theories_ ([Rezk 98](#Rezk98), [Bergner 07](#Bergner07)).

(Another, complementary, truncation is to the [[homotopy 2-category of (∞,1)-categories]].)


## Definition

### Intrinsic definition

The full [[SSet]]-[[enriched category theory|enriched]]-[[subcategory]] of [[SSet]] on those simplicial sets which are [[quasi-categories]] is -- by the properties discussed at [[(∞,1)-category of (∞,1)-functors]] --  itself a [[quasi-category]]-[[enriched category]]. This is the [[(∞,2)-category]] of [[(∞,1)-categories]].

The [[sSet]]-[[subcategory]] of that obtained by picking of each [[hom-object]] the [[core]], i.e. the maximal [[∞-groupoid]]/[[Kan complex]] yields an [[∞-groupoid]]/[[Kan complex]]-[[enriched category]]. This is the **$(\infty,1)$-category of $(\infty,1)$-categories** in its incarnation as a [[simplicially enriched category]]. Forming its [[homotopy coherent nerve]] produces the **quasi-category of quasi-categories** .

### Models

The [[Andre Joyal|Joyal]]-[[model structure for quasi-categories]] is an $sSet_{Joyal}$-[[enriched model category]] and hence its full [[SSet]]-[[subcategory]] on cofibrant-fibrant objects is the $(\infty,2)$-category of $(\infty,1)$-categories.

An $SSet_{Quillen}$-[[enriched model category]] (i.e. enriched over the ordinary [[model structure on simplicial sets]]) whose full subcategory of fibrant-cofibrant objects is the $(\infty,1)$-category $(\infty,1)Cat$ is the [[model structure on marked simplicial over-sets|model structure on marked simplicial sets]] (over the terminal set). Its underlying plain model category is [[Quillen equivalence|Quillen equivalent]] to the Joyal-model structure, but it is indeed $sSet_{Quillen}$-enriched.

Other model structures that present the $(\infty,1)$-category of all $(\infty,1)$-categories are

* [[model structure on categories with weak equivalences]]

* [[model structure on simplicially enriched categories]]

* [[model structure for complete Segal spaces]].

### The nerve into simplicial spaces

The nerve functor

$$
  N : (\infty,1)Cat_1 \to PSh(\Delta, \infty Gpd) : C \mapsto n \mapsto Core(C^{[n]})
$$

is fully faithful. Thus, the $(\infty,1)$-category of $(\infty,1)$-categories can be identified with the $(\infty,1)$-category of [[category object in an (infinity,1)-category#GrpdInCatIsChoiceOfGroupoidObjects|internal categories in $\infty Gpd$]]

This is closely related to the complete Segal space model.

$N$ is, in fact, the embedding of a [[reflective sub-(infinity,1)-category]]. The $(\infty,1)$-categories can be identified with the subcategory of $PSh(\Delta, \infty Gpd)$ of local objects with respect to the spine inclusions $Sp^n \subseteq \Delta^n$ and with the map $J \to 1$, where $J$ is the indiscrete simplicial space on two discrete objects.

Alternatively, the map $J \to 1$ can be replaced with the projection from the simplicial discrete space formed from the union of two 2-simplices expressing the idea of a morphism with a left and right inverse $fg \simeq 1$ and $gh \simeq 1$.



## Applications

* of particular interest is the $(\infty,1)$-subcategory $(\infty,1)PresCat_1 \hookrightarrow (\infty,1)Cat_1$ of [[presentable (infinity,1)-category|presentable (∞,1)-categories]].

## Related concepts

* [[homotopy 2-category of (∞,1)-categories]]


## References

In terms of [[complete Segal spaces]]:

* {#Rezk98} [[Charles Rezk]], _A model for the homotopy theory of homotopy theory_, Trans. Amer. Math. Soc. 353 (2001), 973-1007 ([arXiv:math/9811037](https://arxiv.org/abs/math/9811037), [doi:10.1090/S0002-9947-00-02653-2](https://doi.org/10.1090/S0002-9947-00-02653-2))

* {#Bergner07} [[Julia Bergner]], _Three models for the homotopy theory of homotopy theories_, Topology Volume 46, Issue 4, September 2007, Pages 397-436 ([arXiv:math/0504334](https://arxiv.org/abs/math/0504334), [doi:10.1016/j.top.2007.03.002](https://doi.org/10.1016/j.top.2007.03.002))

In terms of [[quasi-categories]]:

* [[Jacob Lurie]], Chapter 3 of: _[[Higher Topos Theory]]_ (2009)



[[!redirects (∞,1)-category of (∞,1)-categories]]

[[!redirects homotopy theory of homotopy theories]]
[[!redirects homotopy theory of homotopy theory]]

[[!redirects homotopy theories of homotopy theories]]
[[!redirects homotopy theories of homotopy theory]]
