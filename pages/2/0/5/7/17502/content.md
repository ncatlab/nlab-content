# 3-categories with contravariance

* table of contents
{: toc}

## Idea

A *3-category with contravariance* is a [[categorification]] of a [[2-category with contravariance]].  It is an abstract structure that generalizes the structure present on the collection of [[2-categories]] and all four sorts of [[contravariant 2-functor]].

## No mixed-variance transformations

As for [[2-category with contravariance]], the simplest case is when we only consider transformations between functors of the same variance.  Thus for each pair of objects $x,y$ we have four disjoint hom-2-categories $hom^{++}(x,y)$, $hom^{+-}(x,y)$, $hom^{-+}(x,y)$, and $hom^{--}(x,y)$, with sixteen composition 2-functors that act like $\mathbb{Z}/2\times \mathbb{Z}/2$ on the gradings and are appropriately variant on their inputs.

Like [[2-categories with contravariance]], these can be described abstractly (at least in the strict case of [[strict 3-categories]], or the [[semistrict n-category|semistrict]] case of [[Gray-categories]]) as [[enriched categories]], in terms of an action of $\mathbb{Z}/2\times \mathbb{Z}/2$ on $2Cat$.  See [Shulman 2016](#Shulman2016) for a few details.  Depending on whether we use the strict cartesian product on $2 Cat$, the usual "pseudo" Gray tensor product, or its lax or colax versions, we would obtain a structure including strict, pseudo, lax, or colax [[2-natural transformations]] (all between 2-functors of the same variance only).


## Mixed-variance transformations

We can also attempt to include transformations between 2-functors of different variance.  In this case our hom-2-categories will have a $\mathbb{Z}/2\times\mathbb{Z}/2$-grading on their objects, but include morphisms between objects of different variance, yielding sixteen different kinds of natural transformation.  We could also choose to make these transformations strict, lax, colax, or pseudo.  All these kinds of transformation can also be regarded as special cases of [[2-dinatural transformations]]; see there for an example.

It is natural to then conjecture that there is a tensor product on an appropriate category of $\mathbb{Z}/2\times\mathbb{Z}/2$-graded 2-categories giving rise to a notion of enriched category that described this structure.

## References

* [[Mike Shulman]], *Contravariance through enrichment*, [arXiv](https://arxiv.org/abs/1606.05058), 2016
 {#Shulman2016}

[[!redirects 3-categories with contravariance]]
