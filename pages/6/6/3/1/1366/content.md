<div class="rightHandSide toc">
[[!include higher category theory - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The collection of all [[(∞,1)-categories]] forms naturally the [[(∞,2)-category]] [[(∞,1)Cat]]. 

But for many purposes it is quite sufficient to regard only invertible [[natural transformation]]s between [[(∞,1)-functor]], which means that one needs just the maximal [[(∞,1)-category]] inside that $(\infty,2)$-category of all $(\infty,1)$-categories.

Given that an $(\infty,1)$-category is a context for abstract [[homotopy theory]], the $(\infty,1)$-category of $(\infty,1)$-categories is also called the the **homotopy theory of homotopy theories**.

## Definition

### Intrinsic definition

The full [[SSet]]-[[enriched category theory|enriched]]-[[subcategory]] of [[SSet]] on those simplicial sets which are [[quasi-categories]] is -- by the properties discussed at [[(∞,1)-category of (∞,1)-functors]] --  iself a [[quasi-category]]-[[enriched category]]. This is the [[(∞,2)-category]] of [[(∞,1)-categories]].

The [[sSet]]-[[subcategory]] of that obtained by picking of each [[hom-object]] the [[core]], i.e. the maximal [[∞-groupoid]]/[[Kan complex]] yields an [[∞-groupoid]]/[[Kan complex]]-[[enriched category]]. This is the **$(\infty,1)$-category of $(\infty,1)$-categories** in its incarnation as a [[simplicially enriched category]]. Forming its [[homotopy coherent nerve]] produces the **quasi-category of quasi-categories** .

### Models

The [[Andre Joyal|Joyal]]-[[model structure for quasi-categories]] is an $sSet_{Joyal}$-[[enriched model category]] and hence its full [[SSet]]-[[subcategory]] on cofibrant-fibrant objects is the $(\infty,2)$-category of $(\infty,1)$-categories.

An $SSet_{Quillen}$-[[enriched model category]] (i.e. enriched over the ordinary [[model structure on simplicial sets]]) whose full subcategory of fibrant-cofibrant objects is the $(\infty,1)$-category $(\infty,1)Cat$ is the [[model structure on marked simplicial over-sets|model structure on marked simplicial sets]] (over the terminal set). Its underlying plain model category is [[Quillen equivalence|Quillen equivalent]] to the Joyal-model structure, but it is indeed $sSet_{Quillen}$-enriched.

Other model structures that present the $(\infty,1)$-category of all $(\infty,1)$-categories are

* [[model structure on categories with weak equivalences]]

* [[model structure on simplicially enriched categories]]

* [[model structure for complete Segal spaces]].


## Applications

* of particular interest is the $(\infty,1)$-subcategory $(\infty,1)PresCat_1 \hookrightarrow (\infty,1)Cat_1$ of [[presentable (infinity,1)-category|presentable (∞,1)-categories]].

## References

chapter 3 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects (∞,1)-category of (∞,1)-categories]]