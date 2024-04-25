
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[category]] $C$, we may construct the [[free cocompletion]] of $C$, freely adding some [[class]] of [[colimits]]. Often, however, $C$ will already have some colimits, which we wish to preserve. A **conservative cocompletion** of a category $C$ is a cocompletion that preserves the colimits in $C$.

For a [[small category]] $C$ with $\Phi$-colimits, there is a simple description of the **$\Phi$-conservative completion** (for a class $\Phi$ of colimits). It is the the full subcategory $[C^\circ, Set]_\Phi$ of the [[presheaf category]] on $C$ spanned by the functors sending $\Phi$-colimits in $C$ to limits in the presheaf category.

For a [[large category]], this description does not suffice in general, nor does it suffices to consider categories of [[small presheaves]]: in fact, there are [[locally small categories]] that do not admit locally small conservative cocompletions (see [AV02](#AV02)) (however, they do admit conservative cocompletions that are large and not locally small).

## Related concepts

- [[free cocompletion]]

## References

- J. F Kennison, _On limit-preserving functors_, Illinois Journal of Mathematics 12.4 (1968): 616-619.

- {#AV02} [[Jiřı́ Adámek]] and [[Jiřı́ Velebil]]. _A remark on conservative cocompletions of categories_. Journal of Pure and Applied Algebra 168.1 (2002): 107-124.

See also Theorem 11.5 of:

- [[Marcelo Fiore]]. _Enrichment and representation theorems for categories of domains and continuous functions_. University of Edinburgh.

See section 6.4 (and Theorem 6.4.3 in particular) of:

* {#MakkaiPare} [[Michael Makkai]], [[Robert Paré]],  _Accessible categories: The foundations of categorical model theory_,  Contemporary Mathematics 104. American Mathematical Society, Rhode Island (1989) ([ISBN:978-0-8218-7692-3](https://bookstore.ams.org/conm-104))

[[!redirects conservative cocompletions]]
[[!redirects free conservative cocompletion]]
[[!redirects free conservative cocompletions]]
