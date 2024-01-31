

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $(\mathcal{V}, \otimes)$ a [[symmetric monoidal category]] regarded as a [[cosmos for enrichment]], there is a [[tensor product]] of [[enriched category|$\mathcal{V}$-enriched categories]] which on [[classes]] of [[objects]] is the [[Cartesian product]] and on [[hom-objects]] is given by $\otimes$, with [[composition]] defined factor-wise after using the [[braiding]] in $\mathcal{V}$ to align composable tensor factors.

This operation makes [[VCat|$\mathcal{V}Cat$]] itself into a ([[very large category|very large]]) [[symmetric monoidal category]] &lbrack;[Kelly (1982), §1.4](#Kelly82)&rbrack;.


If $\mathcal{V}$ is furthermore [[closed monoidal category|closed]] and [[complete category|complete]] so that [[enriched functor category|$\mathcal{V}$-enriched functor categories]] exist, then these constitute the [[internal hom]] [[right adjoint]] to the operation of forming the enriched product category with a given enriched category &lbrack;[Kelly (1982), §2.3](#Kelly82)&rbrack;.

## Examples

\begin{example}
  For $\mathcal{V} = $ [[Set]] equipped with its [[cartesian product]] $\otimes \,\coloneqq\, \times$, the construction of enriched product categories reduces to the ordinary notion of [[product categories]].
\end{example}

## Related concepts

* [[bifunctor]]

## References

Textbook accounts:

* {#EilenbergKelly65} [[Samuel Eilenberg]], [[G. Max Kelly]],  §III.3 of: *Closed Categories*, in: *[[Proceedings of the Conference on Categorical Algebra - La Jolla 1965]]*, Springer (1966) 421-562 &lbrack;[doi:10.1007/978-3-642-99902-4](https://doi.org/10.1007/978-3-642-99902-4)&rbrack;


* {#Kelly82} [[Max Kelly]], §2.3 of: _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press (1982), Reprints in Theory and Applications of Categories **10** (2005) 1-136  &lbrack;[ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029), [tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;

See also

* [[Enrico Ghiorzi]], §3.6 *Internal enriched categories*, Applied Categorical Structures **30** (2022) 947–968  &lbrack;[arXiv:2006.07997](https://arxiv.org/abs/2006.07997), [doi:10.1007/s10485-022-09678-w](https://doi.org/10.1007/s10485-022-09678-w)&rbrack;

* [[Haskell]]: [Data-Category-Enriched.html](https://hackage.haskell.org/package/data-category-0.10/docs/Data-Category-Enriched.html)

The tensor product of enriched categories is called the **commuting tensor product** of enriched categories in the following:

* [[Richard Garner]], [[Ignacio López Franco]], _Commutativity_, [arXiv](http://arxiv.org/abs/1507.08710).


[[!redirects enriched product category]]
[[!redirects enriched product categories]]

[[!redirects tensor product of enriched categories]]
[[!redirects tensor products of enriched categories]]

