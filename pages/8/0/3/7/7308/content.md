
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The notion of _[[operad]]_ comes in two broad flavors (apart from the choice of enriching category): _planar operads_ and _[[symmetric operads]]_. Accordingly, planar operads are also called _non-symmetric operads_. Another term is _nonpermutative operads_.

A planar operad is a collection ([[set]]/[[object]] in some enriching category) of $n$-ary operations for all $n \in \mathbb{N}$, equipped with a suitable notion of _composition_. In contrast, a _[[symmetric operad]]_ in addition carries an [[action]] of the [[symmetric group]] $\Sigma_n$ on the object on $n$-ary operations, and all structures are required to respect this action.

The notion of planar operads takes its name from the fact that the operations in a planar operad may naturally be drawn as [[planar trees]] without, in general, a relation between two trees that cannot be related by a planar deformation into each other.

Multi-coloured planar operads over [[Set]] are equivalently known as _[[multicategories]]_.

## Definition

In the context of [[(∞,1)-operads]] $\mathcal{O}$ exhibited by their [[(∞,1)-categories of operators]] $\mathcal{O}^\otimes$, a **planar $(\infty,1)$-operad** is a [[fibration of (∞,1)-operads]]

$$
  \mathcal{O}^\otimes \to Assoc^\otimes
$$

to the [[associative operad]]/[[A-∞ operad]]. ([Lurie, def. 4.1.1.6](#Lurie))

## Properties

### Relation to symmetric operads
 {#RelationToSymmetricOperads}

Planar operads embed into [[symmetric operads]] by [[slice category|slicing]] over the [[associative operad]] (regarded as a symmetric operad). For more details see at [Symmetric operad -- Relation to planar operads](symmetric+operad#RelationToPlanarOperads).



## Examples

* The operad [[Assoc]] for associative [[monoids]] is the [[terminal object]] in the category of planar $V$-operads, for choices such as $V = $  [[Set]], [[sSet]], [[Top]], etc.


## Related concepts

* [[symmetric operad]]

* [[multicategory]]

## References

Discussion in the context of the [[higher algebra]] of [[(∞,1)-operads]] is in section 4.1.1 of

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}


[[!redirects planar operads]]

[[!redirects non-symmetric operad]]
[[!redirects non-symmetric operads]]

[[!redirects nonpermutative operad]]
[[!redirects nonpermutative operads]]

[[!redirects non-permutative operad]]
[[!redirects non-permutative operads]]

[[!redirects planar (∞,1)-operad]]
[[!redirects planar (∞,1)-operads]]
[[!redirects planar (infinity,1)-operad]]
[[!redirects planar (infinity,1)-operads]]
