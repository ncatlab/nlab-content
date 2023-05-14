
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An [[object]] in a [[model category]] is *bifibrant* if it is both [[fibrant object|fibrant]] as well as [[cofibrant object|cofibrant]].

To some extent a [[model category]]-[[structure]] on a [[homotopical category]]/[[relative category]] may be understood as a device for finding/forming the [[full subcategory]] of bifibrant objects and with it a convenient presentation of the *[[localization]]* at the given class of [[weak equivalences]]:

* Equipped with the [[homotopy equivalence]]-[[equivalence classes|classes]] of its [[morphisms]], the [[full subcategory]] of bifibrant objects is [[equivalence of categories|equivalently]] the [[homotopy category of a model category|homotopy category]], hence the [[localization of a category|localization]] of the original category at the given class of [[weak equivalences]], see [here](homotopy+category+of+a+model+category#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory). 

* Better yet, if the model structure is [[simplicial model category|sSet-enriched]] and otherwise good enough (for instance: [[combinatorial model category|combinatorial]]), then the full [[sSet-enriched category|sSet-enriched]] category on the bifibrant objects is [[equivalence of (infinity,1)-categories|equivalently]] the [[(infinity,1)-category|$(\infty,1)$-category]] which is the [[simplicial localization]] at the given class of [[weak equivalences]], see [here](locally+presentable+infinity1-category#EquivalentCharacterizations).

This makes bifibrant objects a convenient notion for abstract reasoning about ([[simplicial localization|simplicial]]) [[localization of a category|localizations]]. 

On the other hand, in most model categories the bifibrant objects are not the ones that are conveniently handled in practice (often they can be produced only by abstract [[fibrant resolution|fibrant]]+[[cofibrant resolution]]-machines which tend to produce unwieldy results). But the tools provided by [[model category]]-[[structure]] also allow to reason about bifibrant objects without necessarily constructing them. For example, a [key lemma](homotopy+category+of+a+model+category#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory) says that for computing [[homotopy classes]] of maps between bifibrant objects it is actually sufficient to use an equivalent [[cofibrant object]] for the [[domain]] and an equivalent [[fibrant object]] for the [[codomain]].

## Related concepts

* [[fibrant object]], [[cofibrant object]]

* [[fibrant resolution]], [[cofibrant resolution]]

* [[fibration]], [[cofibration]]


## References

See at *[[model category]]*.


[[!redirects bifibrant objects]]

[[!redirects bi-fibrant object]]
[[!redirects bi-fibrant objects]]


