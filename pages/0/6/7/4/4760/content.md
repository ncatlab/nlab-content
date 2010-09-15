+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Duskin nerve_ is the [[nerve]] operation on [[bicategories]]. It is a [[functor]] from [[BiCat]] to [[sSet]].

$$
  N : BiCat \to sSet
  \,.
$$

## Definition

We may think of the [[simplex category]] $\Delta$ as the [[full subcategory]] of [[Cat]] on the categories free on non-empty finite linear graphs. This givbes the canonical inclusion $\Delta \hookrightarrow Cat$ that defines the ordinary nerve of categories. 

There is also the canonical embedding of categories into bicategories. Combined this gives the inclusion 

$$
  \Delta \hookrightarrow Cat \hookrightarrow BiCat
  \,.
$$

The bicategorical nerve is the nerve induced from that. So far $C$ a bicategory we have

$$
  N(C) : [k] \mapsto Hom_{BiCat}(\Delta[k], C)
  \,.
$$
 
## Properties

* The [[simplicial set]]s in the image of the Duskin nerve are 3-[[coskeletal]].

* The Duskin nerve identifies precisely [[bigroupoid]]s with 3-coskeletal [[Kan complex]]es. 

  (This shows in particular that bigroupoids model all [[homotopy 2-type]]s.)


## Example

Any strict 2-category determines both a 'bicategory' in the above sense (since a 'strict' thing is also a 'weak' one)  and a simplicially enriched category.  The latter is found by taking the nerve of each 'hom-category'.  The Duskin nerve of a 2-category is the same as the [[homotopy coherent nerve]] of the corresponding $sSet$-category.  This can also be applied to [[2-groupoid]]s and results in a classifying space construction for [[crossed module]]s. 


## References

* [[John Duskin]], _Simplicial matrices and the nerves of weak n-categories I: nerves of bicategories_ ([tac](http://www.tac.mta.ca/tac/volumes/9/n10/9-10abs.html))

* V. Blanco, M. Bullejos, E. Faro, A Full and faithful Nerve for 2-categories, Applied 
Categorical Structures, Vol 13-3, 223-233, 2005.

[[!redirects bicategory nerve]]
[[!redirects nerve of bicategories]]
[[!redirects nerve of a bicategory]]
