
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In as far as an [[algebraic theory]] or [[Lawvere theory]] is nothing but a [[small category]] with finite [[product]]s and an [[algebra]] for the theory a product-preserving [[functor]] to [[Set]], the notion has an evident generalization to [[higher category theory]] and in particular to [[(∞,1)-category]] theory.

## Definition

+-- {: .un_defn}
###### Definition

An **$(\infty,1)$-Lawvere theory** is (given by a syntactic $(\infty,1)$-category that is) an [[(∞,1)-category]] $C$ with finite [[limit in a quasi-category|(∞,1)-product]]s. An $(\infty,1)$-algebra for the theory is an [[(∞,1)-functor]] $C \to $ [[∞Grpd]] that preserves these products.

The $(\infty,1)$-category of $(\infty,1)$-algebras is the full [[sub-quasi-category|(∞,1)-subcategory]]

$$
  Alg_{(\infty,1)}(C) \hookrightarrow PSh_{(\infty,1)}(C^{op})
$$

of the [[(∞,1)-category of (∞,1)-presheaves]] on $C^{op}$ on the product-preserving $(\infty,1)$-functors

=--

In a full $(\infty,1)$-category theoretic context this appears as [[Higher Topos Theory|HTT, def. 5.5.8.8]]. A definition in terms of [[simplicially enriched categories]] and the [[model structure on sSet-categories]] to present $(\infty,1)$-categories is in [Ros]((http://www.math.muni.cz/~rosicky/papers/infty6.pdf). The introduction of that article lists further and older occurences of this definition.

## Properties


+-- {: .un_prop}
###### Proposition

Let $C$ be an [[(∞,1)-category]] with finite [[limit in a quasi-category|product]]s. Then 

* $Alg_{(\infty,1)}(C)$ is an [[accessible (∞,1)-functor|accessible]] [[localization of an (∞,1)-category|localization]] of the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C^{op})$ (on the [[opposite (∞,1)-category|opposite]]).

  So in particular it is a [[locally presentable (∞,1)-category]].

* $Alg_{(\inft)}$ is a [[compactly generated (∞,1)-category]].

* The $(\infty,1)$-[[Yoneda embedding]] $j : C^{op} \to PSh_{(\infty,1)}(C^{op})$ factors through $Alg_{(\infty,1)}(C)$.

* The full subcategory $Alg_{(\infty,1)}(C) \hookrightarrow PSh_{(\infty,1)}(C)$ is stable under [[sifted colimit]]s.


=--

This is [[Higher Topos Theory|HTT, prop. 5.5.8.10]].


## Examples

### Smooth $(\infty,1)$-algebras

The [[Lawvere theory]] whose syntactic category with finite products is [[CartSp]] has as algebra [[smooth algebra]]s. The same theory, regarded as an $(\infty,1)$-algebraic theory, has as algebras **smooth $(\infty,1)$-algebras. 

These  were considered for the discussion of [[derived smooth manifold]]s in

* [[David Spivak]], _Derived smooth manifolds_ ([arXiv:0810.5174](http://arxiv.org/abs/0810.5174))


## References

A characterization of $(\infty,1)$-categories of $(\infty,1)$-algebras in terms of [[sifted colimit]]s is given in

* J. Rosicky _On homotopy varieties_ ([pdf](http://www.math.muni.cz/~rosicky/papers/infty6.pdf))

using the incarnation of $(\infty,1)$-categories as [[simplicially enriched categories]].

An account of this characterization in the context of a general theory of [[(∞,1)-category of (∞,1)-presheaves]] is the context of section 5.5.8 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

The [[model category]] [[presentable (infinity,1)-category|presentations]] of $(\infty,1)$-algebras is studied in 

* [[Charles Rezk]], _Every homotopy theory of simplicial algebras admits a proper model_ ([math/0003065](http://arxiv.org/abs/math/0003065)) ,

where it is shwon that every such model is [[Quillen equivalence|Quillen equivalent]] to a left [[proper model category]]. The article uses a mondaic definition of $(\infty,1)$-algebras.

[[!redirects (infinity,1)-algebraic theory]]
[[!redirects (infinity,1)-algebraic theories]]
[[!redirects (∞,1)-algebraic theories]]