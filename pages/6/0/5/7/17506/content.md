# Duality involutions

* table of contents
{: toc}

## Idea

A **duality involution** is an abstract operation that generalizes the notion of [[opposite category]].  What this means precisely depends on the underlying abstract structure.

## On 2-categories

A **duality involution** on a [[2-category]] $K$ is a 2-functor $(-)^\circ : K^{co} \to K$ that is coherently (or strictly) self-inverse.  A precise definition, and [[coherence theorem]], can be found in [Shulman 2016](#Shulman2016).  This sort of duality involution is [[stuff, structure, property|structure rather than a property]], but it can be given a universal property relative to a [[2-category with contravariance]].

## On bicategories

In the [[bicategory]] [[Prof]] of categories and profunctors, $A^{op}$ is the [[dual object]] of $A$ relative to a monoidal structure, making $Prof$ a [[compact closed bicategory]].  Thus, in any compact closed bicategory, the operation taking each object to its dual may be called a **duality involution**.  Note that being compact closed is a property and not a structure on a bicategory.

## On equipments

It should be possible to combine a duality involution on a 2-category and on a bicategory to obtain a notion of duality involution on a [[proarrow equipment]], but it is not clear exactly what the coherence conditions should be.  [Weber 2007](#Weber2007) extends a duality involution on a 2-category to its [[virtual equipment]] of discrete [[two-sided fibrations]] by asking for equivalences $DFib(A\times B,C) \simeq DFib(A,B^{\circ}\times C)$ that are pseudonatural in $A,B,C$.  But perhaps in general some compatibility with the composition of profunctors should also be assumed?

## References

* [[Mike Shulman]], *Contravariance through enrichment*, [arXiv](https://arxiv.org/abs/1606.05058), 2016
 {#Shulman2016}

* [[Mark Weber]], *Yoneda structures from 2-toposes*,  Applied Categorical Structures, Vol. 15, p259-323, 2007, [web](https://sites.google.com/site/markwebersmaths/home/yoneda-structures-from-2-toposes)

[[!redirects duality involutions]]
