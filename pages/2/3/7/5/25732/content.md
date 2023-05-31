
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


If $\mathcal{V}$ is forthermore [[closed monoidal category|closed]] and [[complete category|complete]] so that [[enriched functor category|$\mathcal{V}$-enriched functor categories]] exist, then these constitute the [[internal hom]] [[right adjoint]] to the operation of forming the enriched product category with a given enriched category &lbrack;[Kelly (1982), §2.3](#Kelly82)&rbrack;.

## Examples

\begin{example}
  For $\mathcal{V} = $ [[Set]] equipped with its [[cartesian product]] $\otimes \,\coloneqq\, \times$, the construction of enriched product categories reduces to the ordinary notion of [[product categories]].
\end{example}

## References

* {#Kelly82} [[Max Kelly]], _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press (1982), Reprints in Theory and Applications of Categories **10** (2005) 1-136  &lbrack;[ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029), [tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;

[[!redirects enriched product categories]]

