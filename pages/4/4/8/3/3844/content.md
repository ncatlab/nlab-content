
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


* [[algebraic theory]] / [[Lawvere theory]] / [[2-Lawvere theory]] /  **$(\infty,1)$-algebraic theory**

* [[monad]] / [[(∞,1)-monad]]

* [[operad]] / [[(∞,1)-operad]]

***


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

## Models {#Models}

There are various [[model category]] [[presentable (∞,1)-category|presentations]] of $Alg_{(\infty,1)}(C) \hookrightarrow PSh_{(\infty,1)}(C^{op})$.

Recall that the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C^{op})$ itself is modeled by the [[model structure on simplicial presheaves]]

$$
  PSh_{(\infty,1)}(C^{op})
  \simeq
  [C, sSet]^\circ
  \,,
$$

where we regard $C$ as a [[Kan complex]]-[[enriched category]] and have on the right the [[sSet]]-[[enriched functor category]] with the projective or injective model structure, and $(-)^\circ$ denoting the full enriched subcategory on fibrant-cofibrant objects.

This says in particular that every weak $(\infty,1)$-functor $f : C \to \infty \mathrm{Grp}$ is equivalent to a _rectified_ on $F : C \to KanCplx$. And $f \in PSh_{(\infty,1)}(C^{op})$ belongs to $Alg_{(\infty,1)}(C)$ if $F$ preserves finite products _weakly_  in that for $\{c_i \in C\}$ a finite collection of objects, the canonical natural morphism

$$
  F(c_1 \times \cdots, \c_n)
  \to
  F(c_1) \times \cdots \times F(c_n)
$$ 

is a [[homotopy equivalence]] of [[Kan complex]]es.

We now look at model category structure on _strictly_ product preserving functors $C \to sSet$, which gives an equivalent model for $Alg_{(\infty,1)}(C)$. See [[model structure on simplicial algebras]].

+-- {: .un_prop}
###### Proposition

Let $C$ be a [[category]] with finite [[product]]s, and let $sAlg(C) \subset Func(C,sSet)$ be the [[full subcategory]] of the [[functor category]] from $C$ to [[sSet]] on those functors that preserve these products.  

Then $sAlg(C)$ carries the structure of a [[model category]] $sAlg(C)_{proj}$ where the weak equivalences and the fibrations are objectwise those in the standard [[model structure on simplicial sets]]. 

=--

This is due to 

* [[Dan Quillen]], _Homotopical Algebra_ Lectures Notes in Mathematics 43, SpringerVerlag, Berlin, (1967)

The inclusion $i : sAlg(C) \hookrightarrow sPSh(C^{op})_{proj}$ into the projective [[model structure on simplicial presheaves]] evidently preserves fibrations and acylclic fibrations and gives a [[Quillen adjunction]]

$$
  sAlg(C)_{proj}
  \stackrel{\leftarrow}{\underset{i}{\hookrightarrow}}
  sPSh(C^{op})
  \,.
$$


+-- {: .un_prop}
###### Proposition

The total right [[derived functor]] 

$$
  \mathbb{R}i : Ho(sAlg(C)_{proj}) \to Ho(sPSh(C^{op})_{proj})
$$ 

is a [[full and faithful functor]] and an object $F \in sPSh(C^{op})$ belongs to the [[essential image]] of $\mathbb{R}i$ precisely if it preserves product up to [[weak homotopy equivalence]].

=--

This is due to

* [[Julie Bergner]], _Rigidification of algebras over multi-sorted theories_ , Algebraic and Geometric Topoogy 7, 2007.

It follows that the natural $(\infty,1)$-functor

$$
  (sAlg(C)_{proj})^\circ \stackrel{}{\to}
  PSh_{(\infty,1)}(C^{op})
$$

is an [[equivalence of quasi-categories|equivalence]].

A comprehensive statement of these facts is in [[Higher Topos Theory|HTT, section 5.5.9]].

## Examples

### Simplicial 1-algebras

For $T$ (the [[syntactic category]] of) an ordinary [[algebraic theory]] (a [[Lawvere theory]]) let $T Alg$ be the category of its ordinary algebras, the ordinary product-preserving functors $T \to Set$.

We may regard $T$ as an $(\infty,1)$-category and consider its $(\infty,1)$-algebras. By the above discussion, these are modeled by product-presering functors $T \to sSet$. But this are equivalently [[simplicial object]]s in $T$-algebras

$$
  [T, sSet]_\times \simeq T Alg^{\Delta^{op}}
  \,.
$$

So we find that simplicial $T$-1-algebras model $T$-$(\infty,1)$-algebras.

For emphasis, in the following we say this again for special choices of $T$.

#### Simplicial rings

Let $T$ be the [[syntactic category]] of the [[Lawvere theory]] of [[ring]], regarded as an $(\infty,1)$-category. Then by the above [[simplicial ring]]s are models for the $T$-$(\infty,1)$-algebras.

#### Simplicial smooth algebras

The [[Lawvere theory]] whose syntactic category with finite products is [[CartSp]] has as algebra [[smooth algebra]]s. The same theory, regarded as an $(\infty,1)$-algebraic theory, has as algebras **[[smooth (∞,1)-algebra]]s. 

These  were considered for the discussion of [[derived smooth manifold]]s in

* [[David Spivak]], _Derived smooth manifolds_ ([arXiv:0810.5174](http://arxiv.org/abs/0810.5174))


### Simplicial theories

There is a notion of _simplicial algebraic theory_ that captures some class of $(\infty,1)$-algebraic theories. For the moment see section 4 of ([Rezk](#Rezk))

## References

The model structure presentation for the $(\infty,1)$-category of  $(\infty,1)$-algebras goes back all the way to

* [[Dan Quillen]], _Homotopical Algebra_ Lectures Notes in Mathematics 43, SpringerVerlag, Berlin, (1967)

A characterization of $(\infty,1)$-categories of $(\infty,1)$-algebras in terms of [[sifted colimit]]s is given in

* J. Rosicky _On homotopy varieties_ ([pdf](http://www.math.muni.cz/~rosicky/papers/infty6.pdf))

using the incarnation of $(\infty,1)$-categories as [[simplicially enriched categories]].

An $(\infty,1)$-categorical perspective on these homotopy-algebraic theories is given in

* [[Andre Joyal]], _The theory of quasi-categories and its applications_, lectures at CRM Barcelona February 2008, draft [hc2.pdf](http://www.crm.cat/HigherCategories/hc2.pdf#page=44)_

from page 44 on.

A detailed account in the context of a general theory of [[(∞,1)-category of (∞,1)-presheaves]] is the context of section 5.5.8 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .

The [[model category]] [[presentable (infinity,1)-category|presentations]] of $(\infty,1)$-algebras is studied in 

* [[Charles Rezk]], _Every homotopy theory of simplicial algebras admits a proper model_ ([math/0003065](http://arxiv.org/abs/math/0003065)) ,
{#Rezk}

where it is shown that every such model is [[Quillen equivalence|Quillen equivalent]] to a left [[proper model category]]. The article uses a monadic definition of $(\infty,1)$-algebras.

[[!redirects (infinity,1)-algebraic theory]]
[[!redirects (infinity,1)-algebraic theories]]
[[!redirects (∞,1)-algebraic theories]]