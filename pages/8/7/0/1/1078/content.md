The __direct sum__, or __weak direct product__, is a concept from algebra that actually makes sense in any [[category]] with [[zero morphism]]s (that is, any category enriched over the [[closed monoidal category]] of [[pointed set]]s).  Note that finitary direct sums are the same as [[product]]s; the infinitary versions are different.

# Terminology #

The name 'weak direct product' comes from the concept of [[direct product]] in algebra for a [[product]] in a [[concrete category]] that is created by the [[forgetful functor]].  Here we will not restrict ourselves to that context.

The term 'direct sum' comes from the (finitary) [[biproduct]] (simultaneously product and coproduct) in [[additive category|additive categories]].  The additive character of these biproducts extends in the infinitary case (where biproducts generally no longer appear) to the direct sum rather than to the product.  (In these cases, the direct sum is often still a [[coproduct]], but the importance of coproducts in algebra was not evident as early.)

# Definition #

Let $C$ be a category with [[zero morphism]]s, and let $(A_i)_{i: I}$ be a family of objects of $C$ indexed by a [[set]] $I$.  Call a _candidate_ for direct sum an object $S$ of $C$ equipped with _projections_ $\pi^i: S \to A_i$ and _inclusions_ $\iota_i: A_i \to S$ such that the composite $A_i \to^{\iota_i} S \to^{\pi^j} A_j$ is the identity if $i = j$ but the zero morphism otherwise; that is,
$$ \pi^j \circ \iota_i = \delta_i^j .$$
Then a __direct sum__, or __weak direct product__, of the family is a candidate
$$ \sum_{i: I} A_i $$
for direct sum with the [[universal property]] that, given any other candidate $S$, there is a unique map $u: \sum A \to S$ such that $\sum A \to^u S \to^{\pi^i} A_i$ equals $\sum A \to^{\pi^i} A_j$ and $A_i \to^{\iota_i} \sum A \to^u S$ equals $A_i \to^{\iota_i} S$; that is,
$$ \pi^i \circ u = \pi^i ; \quad u \circ \iota_i = \iota_i .$$

+--{: .query}
This isn\'t actually right yet ...  ---Toby
=--