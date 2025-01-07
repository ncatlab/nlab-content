
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

For a [[small category]] $C$ with $\Phi$-colimits, there is a simple description of the **$\Phi$-conservative cocompletion** (for a class $\Phi$ of colimits). It is the the full subcategory $[C^\circ, Set]_\Phi$ of the [[presheaf category]] on $C$ spanned by the functors sending $\Phi$-colimits in $C$ to limits in the presheaf category.

For a [[large category]], this description does not suffice in general, nor does it suffices to consider categories of [[small presheaves]]: in fact, there are [[locally small categories]] that do not admit locally small conservative cocompletions (see [AV02](#AV02)) (however, they do admit conservative cocompletions that are large and not locally small).

## Properties

- For a small category $C$, the conservative cocompletion $Cont(C^op, Set)$ is [[complete]] and [[cocomplete]], and the embedding $C \to Cont(C^op, Set)$ creates limits and colimits. Consequently, every small category may be continuously and cocontinuously fully embedded into a complete and cocomplete locally small category. (Note that $Cont(C^op, Set)$ will rarely be [[closed category|closed]] unless $C$ is ([counterexample](https://mathoverflow.net/a/185024)).) However, not every locally small category admits such an embedding: see Example III.1 of [Trnková 1966](#T66).

## Examples

- The category of finite [[semilattices]] is the conservative cocompletion of the category of [[finite sets]] and [[relations]] under finite colimits (and also its [[free cocompletion]] under [[reflexive coequalisers]]) ([AMMU14](#AMMU14)).
- The category [[Pos]] of [[partial orders]] is the free conservative cocompletion of the category of [[total orders]] ([Tataru24](#Tataru24)).

## Related concepts

- [[free cocompletion]]

## References

- [[Joachim Lambek]], _Completions of categories: Seminar lectures given 1966 in Zürich_, Lecture Notes in Mathematics 24 (1966), Springer.  [doi](https://doi.org/10.1007/BFb0077265), ISBN: 978-3-540-03607-4 (softcover), 978-3-540-34840-5 (electronic).

- {#T66} Věra Trnková, _Limits in categories and limit-preserving functors_, Commentationes Mathematicae Universitatis Carolinae 7.1 (1966): 1-73.

- J. F Kennison, _On limit-preserving functors_, Illinois Journal of Mathematics 12.4 (1968): 616-619.

- [[Max Kelly]], _Basic Concepts of Enriched Category Theory_, Cambridge University Press, Lecture Notes in Mathematics 64 (1982).  [TAC reprint](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf).

- {#AV02} [[Jiřı́ Adámek]] and [[Jiřı́ Velebil]]. _A remark on conservative cocompletions of categories_. Journal of Pure and Applied Algebra 168.1 (2002): 107-124.

See also Theorem 11.5 of:

- [[Marcelo Fiore]]. _Enrichment and representation theorems for categories of domains and continuous functions_. University of Edinburgh.

See section 6.4 (and Theorem 6.4.3 in particular) of:

* {#MakkaiPare} [[Michael Makkai]], [[Robert Paré]],  _Accessible categories: The foundations of categorical model theory_,  Contemporary Mathematics 104. American Mathematical Society, Rhode Island (1989) ([ISBN:978-0-8218-7692-3](https://bookstore.ams.org/conm-104))

For examples:

* {#AMMU14} Adámek, J., Myers, R. S., Urbat, H., & Milius, S. "On continuous nondeterminism and state minimality." Electronic Notes in Theoretical Computer Science 308 (2014): 3-23.

* Mimram, Samuel, and Cinzia Di Giusto. "A categorical theory of patches." Electronic notes in theoretical computer science 298 (2013): 283-307.

* {#Tataru24} Calin Tataru, "Partial orders are the free conservative cocompletion of total orders." [arXiv:2404.12924](https://arxiv.org/abs/2404.12924) (2024).

[[!redirects conservative cocompletions]]
[[!redirects free conservative cocompletion]]
[[!redirects free conservative cocompletions]]
