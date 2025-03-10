
> For more see also at _[[CW-complex]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _cell complex_ is an [[object]] in a [[category]] which is obtained by successively "gluing cells" via [[pushouts]].

## Definition

Let $C$ be a [[category]] with [[colimits]] and equipped with a [[set]] $\mathcal{I} \subset Mor(C)$ of [[morphisms]].

In practice $C$ is usually a [[cofibrantly generated model category]] with set $\mathcal{I}$ of generating cofibrations and set $\mathcal{J}$ of acyclic generating cofibrations. 

An _$\mathcal{I}$-cell complex_ in $C$ is an [[object]] $X$ which is connected to the [[initial object]] $\emptyset \to X$  by a [[transfinite composition]] of [[pushouts]] of the generating cofibrations in $\mathcal{I}$.

A _relative $\mathcal{I}$-cell complex_ (relative to any object $A$) is any morphism $A \to X$ obtained like this starting from $A$.

A _finite cell complex_ or _countable cell complex_ is a cell complex with a [[finite set]] or a [[countable set]] of cells, respectively.

## Examples

* A [[CW-complex]] is a cell complex in [[Top]] with respect to the generating cofibrations in the standard [[model structure on topological spaces]].

* Every [[simplicial set]] is a cell complex with respect to the generating cofibrations in the standard [[model structure on simplicial sets]].

* A [[Sullivan model]] is a cell complex with respect to the generating cofibrations in the standard [[model structure on dg-algebras]].

* A [[cell spectrum]] is a cell complex in the category of topological [[sequential spectra]].

## Related concepts

* [[cellular category]]

* [[cellular map]]

* [[CW complex]]

* [[vertex]], [[edge]], [[face]]

* [[dimension of a cell complex]]

* [[locally finite cell complex]]

[[!include universal constructions of topological spaces -- table]]


## References

Textbook account:

* {#FritschPiccinini90} [[Rudolf Fritsch]], [[Renzo Piccinini]], _Cellular structures in topology_, Cambridge University Press (1990) &lbrack;[doi:10.1017/CBO9780511983948](https://doi.org/10.1017/CBO9780511983948), [pdf](https://epub.ub.uni-muenchen.de/4493/1/4493.pdf)&rbrack;


A discussion in the context of [[algebraic model categories]] is in 

* [[Emily Riehl]], _Cellularity in algebraic model structures_ ([blog post](http://golem.ph.utexas.edu/category/2011/12/cellularity_in_algebraic_model.html))

[[!redirects cell complexes]]

[[!redirects relative cell complex]]
[[!redirects relative cell complexes]]

[[!redirects cellular complex]]
[[!redirects cellular complexes]]

[[!redirects finite cell complex]]
[[!redirects finite cell complexes]]

[[!redirects countable cell complex]]
[[!redirects countable cell complexes]]


[[!redirects cell]]
[[!redirects cells]]

[[!redirects n-cell]]
[[!redirects n-cells]]

