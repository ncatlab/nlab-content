
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
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

An $\infty$-**cosmos** is a "good place in which to do [[higher category theory]],"  for [[1-categories]], [[(∞,1)-categories]] , [[(∞,n)-categories]], or [[fibered category]]-versions of any of the above.

The word is chosen by analogy with the notion of _[[cosmos]]_ in [[enriched category theory]], which is similarly "a good place to do (ordinary) category theory." The notion is more similar to Street's "fibrational cosmoi" than to B&#233;nabou's cosmoi.

## A source of examples

Roughly speaking, an $\infty$-**cosmos** is a simplicially enriched category of fibrations and fibrant objects.

Let $\mathcal{M}$ be a [[model category]] that is enriched over the Joyal model structure on simplicial sets. Then the full subcategory of fibrant objects defines an **$\infty$-cosmos**. If, as is frequently the case in practice, every fibrant object is cofibrant, then this subcategory defines an **$\infty$-cosmos with all objects cofibrant,** which admits a simpler axiomatization.

## Definition 

For simplicity, we define only an $\infty$-cosmos with all objects cofibrant. See the references below for the general definition.

An **$\infty$-cosmos** (with all objects cofibrant) is a simplicially enriched category $\mathcal{K}$ whose homs $Fun(A,B)$ are quasi-categories equipped with a specified class of [[isofibration|isofibrations]] so that

1. As a simplicially enriched category, $\mathcal{K}$ admits products, cotensors with simplicial sets, pullbacks of isofibrations, splittings of idempotents, and limits of towers of isofibrations.

2. The class of isofibrations is closed under product, pullback, retract, limits of towers, and Leibniz cotensors with monomorphisms of simplicial sets. Furthermore, if $A \twoheadrightarrow B$ is a fibration in $\mathcal{K}$, then for any $X$, $\Fun(X,A) \twoheadrightarrow \Fun(X,B)$ is an isofibration of quasi-categories.

A map $A \to B$ is an **equivalence** if for any $X$, $\Fun(X,A) \rightarrow \Fun(X,B)$ is an equivalence of quasi-categories, and a **trivial fibration** if it is both an isofibration and an equivalence.

3. For any trivial fibration $p\colon E \twoheadrightarrow B$ and any map $f \colon A \to B$ there exists a lift of $f$ along $p$.

## The prototypical example

The category of quasi-categories and isofibrations, inner fibrations that lift also against the inclusion of either endpoint into the nerve of the walking isomorphism, defines an $\infty$-cosmos.

## Related concepts

* [[homotopy 2-category of (∞,1)-categories]]

## References

For an overview:

* {#RiehlVerity16} [[Emily Riehl]], [[Dominic Verity]], _$\infty$-Category theory from scratch_, ([arXiv:1608.05314](https://arxiv.org/abs/1608.05314))

For the most general notion of $\infty$-cosmos and constructions of many examples:

* {#RiehlVerity15} [[Emily Riehl]], [[Dominic Verity]], _Fibrations and Yoneda's lemma in an $\infty$-comos_ ([arXiv:1506.05500](https://arxiv.org/abs/1506.05500))

For a simplified notion with "all objects cofibrant"

* [[Emily Riehl]], [[Dominic Verity]], _Kan extensions and the calculus of modules for $\infty$-categories_ ([arXiv:1507.01460](https://arxiv.org/abs/1507.01460))

Textbook account:

* [[Emily Riehl]], [[Dominic Verity]], _Elements of $\infty$-Category Theory_ (2021) ([pdf](http://www.math.jhu.edu/~eriehl/elements.pdf))


[[!redirects infinity-cosmoi]]

[[!redirects ∞-cosmos]]
[[!redirects ∞-cosmoi]]

