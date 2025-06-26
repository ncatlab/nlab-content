
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

Let $C$ be a [[category]] with [[colimits]] and equipped with a [[set]] $\mathcal{I} \subset Mor(C)$ of [[morphisms]], to be called the *generating cofibrations*.

In practice, $C$ is usually a [[cofibrantly generated model category]] with set $\mathcal{I}$ of [[generating cofibrations]] and set $\mathcal{J}$ of [[generating acyclic cofibrations]]. 

Now: 

\begin{definition}\label{TheAbstractDefinition}

An _$\mathcal{I}$-cell complex_ in $C$ is an [[object]] $X$ which is connected to the [[initial object]] $\emptyset \to X$  by a [[transfinite composition]] of [[pushouts]] ([[cell attachments]]) of ([[coproducts]] of) the generating cofibrations in $\mathcal{I}$.

More generally, a _relative $\mathcal{I}$-cell complex_ (relative to any object $A$) is any morphism $A \to X$ obtained like this starting from $A$.

A _finite cell complex_ or _countable cell complex_ is a cell complex with a [[finite set]] or a [[countable set]] of cells, respectively.

\end{definition}

\begin{remark}\label{OnTheAppearanceOfCoproducts}
  Definition \ref{TheAbstractDefinition} is often stated without explicitly allowing forming [[coproducts]] of generating cofibrations (formed in the [[arrow category]]) before taking their [[pushouts]] (e.g. [Hovey 1999 Def. 2.1.9](#Hovey99) and [Hirschhorn 2002 Def. 10.5.8](#Hirschhorn02)) while in practice authors often do consider this (e.g. [Hirschhorn 2015 Rem. 4.4](#Hirschhorn15)).

The two variants are equivalent assuming the [[axiom of choice]] in the form of the [[well-ordering theorem]]: With that theorem/assumption, the set of [[coproducts]] to be pushed out may be equipped with a [[well-order]] and with that the pushout of the coproduct is equivalently the transfinite composition of pushouts of summands of the coproduct in that order.

(Note that the [[axiom of choice]] is used already for basic statements in this context, like the very existence of the [[classical model structure on topological spaces]], see there [this Lemma](classical+model+structure+on+topological+spaces#CompactSubsetsAreSmallInCellComplexes)).

\end{remark}


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

Textbook account in [[general topology]]:

* {#FritschPiccinini90} [[Rudolf Fritsch]], [[Renzo Piccinini]], _Cellular structures in topology_, Cambridge University Press (1990) &lbrack;[doi:10.1017/CBO9780511983948](https://doi.org/10.1017/CBO9780511983948), [pdf](https://epub.ub.uni-muenchen.de/4493/1/4493.pdf)&rbrack;

and in the context of the [[classical model structure on topological spaces]]:

* {#Hirschhorn15} [[Philip Hirschhorn]], §4 in: *The Quillen model category of topological spaces*, Expositiones Mathematicae **37** 1 (2019) 2-24 &lbrack;[arXiv:1508.01942](http://arxiv.org/abs/1508.01942), [doi:10.1016/j.exmath.2017.10.004](https://doi.org/10.1016/j.exmath.2017.10.004)&rbrack;

and in the general context of ([[cofibrantly generated model category|cofibrantly generated]]) [[model category theory]]:

* {#Hovey99} [[Mark Hovey]], Def. 2.1.9 in: *[[Model Categories]]*, Mathematical Surveys and Monographs, **63** AMS (1999) &lbrack;[ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover)&rbrack;

* {#Hirschhorn02} [[Philip Hirschhorn]], Def. 10.5.8 in: *[[Model Categories and Their Localizations]]*, Math. Survey and Monographs **99**, AMS (2002) &lbrack;[ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/pshmain.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf)&rbrack;


A discussion in the context of [[algebraic model categories]]:

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

