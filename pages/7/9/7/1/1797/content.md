# Adjoint equivalences
* table of contents
{: toc}

## Definition

An **adjoint equivalence** between [[categories]] is an [[adjunction]] in which the unit and counit are [[natural isomorphisms]].  It follows that it is an [[equivalence of categories]].

There is an identical definition internal to any [[2-category]], which reproduces the above notion when applied in [[Cat]].

## Remarks

An adjoint equivalence is a more "coherent" or "structured" notion of equivalence, in which the isomorphisms relating composites to identities are required to satisfy coherence laws (the triangle identities for an adjunction).  This is sometimes useful; for instance, the "free-living adjoint equivalence" 2-category is equivalent to the [[point]], and thus can be used as an [[interval object]] in $2Cat$, but this is not true of the "free-living non-adjoint equivalence."

However, being "adjoint equivalent" is no stronger a condition than being "equivalent," since every equivalence may be refined to an adjoint equivalence by modifying one of the natural isomorphisms involved.

## In higher category theory

In [[higher category theory]], one expects to have a similar "fully coherent" notion of "adjoint equivalence" in any [[n-category]] or [[infinity-category]], and one hopes to prove a similar theorem that any [[equivalence]] can be refined to an adjoint equivalence.  This is known to be true at least in the following cases:

* For [[Gray-categories]], the statement and proof is in [[Steve Lack]]'s paper [1001.2366](http://arxiv.org/abs/1001.2366) on the [[model structure for Gray-categories]].

* For [[strict omega-categories]], more or less this fact can be found in the study of "generic squares" in the paper [0712.0617](http://arxiv.org/abs/0712.0617) on the [[model structure for strict omega-categories]].

* For [[quasicategories]], the theorem is true, where an "adjoint equivalence" means simply a map out of the [[nerve]] of the [[interval groupoid]]; see [[equivalence in a quasicategory]].

[[!redirects adjoint equivalences]]
