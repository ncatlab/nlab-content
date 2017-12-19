# Poset-valued sets

* table of contents
{: toc}

## Idea

Let $P$ be a [[poset]] and $F:Rel\to Rel$ an endofunctor of [[Rel]].  A **$P_F$-valued set** is a set $A$ equipped with a function $F A\to P$.  The [[morphisms]] of $P_F$-valued sets are certain relations.

The category of $P_F$-valued sets inherits a lot of structure from $P$: if $P$ is [[closed monoidal category|closed]] [[symmetric monoidal category|symmetric monoidal]], [[star-autonomous]], etc., and $F$ is well-behaved, then so is the category of $P_F$-valued sets.  This provides a general method for constructing models of variants of [[linear logic]].

## Examples

If $P=\mathbf{3} = (0\le 1\le 2)$, with the star-autonomous structure where $1$ is both the unit object and the dualizing object, and $F(A) = A\times A$, then the category of $P_F$-valued sets includes the category of [[coherence spaces]] as a full subcategory, preserving the closed monoidal structure as well as products and coproducts.

## References

* [[Andrea Schalk]], [[Valeria de Paiva]], *Poset-valued sets or how to build models for linear logics*, In Theoretical Computer Science, Volume 315, Issue 1, 2004, Pages 83-107, [DOI](https://doi.org/10.1016/j.tcs.2003.11.014).

[[!redirects poset-valued sets]]
