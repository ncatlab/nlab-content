
#Contents#
* automatic table of contents goes here
{:toc}


## Idea

In [[model theory]], a __model__ of a [[theory]] is a realization of the types, operations, relations, and axioms of that theory.  In ordinary model theory one usually studies mainly models in [[sets]], but in [[categorical logic]] we study models in other [[categories]], especially in [[topoi]].

The term **structure** is often used to mean a realization of types, operations, and relations in some [[signature]], but not satisfying any particular axioms.  This is of course the same as a model for the "empty theory" in that signature, which has the same types, operations, and relations, but no axioms at all.  One then talks about whether a given structure is, or is not, a *model* of a given theory in a given signature.


## Definition

...

### For Lawvere theories

For $Syn(T)$ the [[syntactic category]] of a [[Lawvere theory]], and for $C$ any category with finite [[limit]]s, a _model_ for $T$ in $C$ is a product-preserving functor

$$
  N : Syn(T) \to C
  \,.
$$

The **category of models** in this case is hence the [[full subcategory]] of the [[functor category]] $[Syn(T),C]$ on product-preserving functors.

[[!redirects models]]
[[!redirects category of models]]
[[!redirects categories of models]]
