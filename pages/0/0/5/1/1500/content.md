
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--
#Contents#
* table of contents 
{:toc}


## Definition ## 

+-- {: .num_defn}
###### Definition

A **fusion category** is a [[rigid monoidal category|rigid]] [[semisimple category|semisimple]] [[linear category|linear]] ([[Vect]]-[[enriched category|enriched]]) [[monoidal category]], with only finitely many [[decategorification|isomorphism classes]] of simple objects, such that the [[endomorphism]]s of the unit object form just the [[ground field]] $k$.

=--


## Examples

The name "fusion category" comes from the central examples of structures whose canonical [[tensor product]] is called a "fusion product", notably [[representation]]s of [[loop group]]s and of [[Hopf algebra]]s and of [[vertex operator algebra]]s. 


## Properties

### Relation to pivotal and spherical categories

Fusion categories were first systematically studied by Etingof, Nikshych and Ostrik in [On fusion categories](http://arxiv.org/abs/math/0203060). This paper listed many examples and proved many properties of fusion categories. One of the important conjectures made in that paper was the following:

+-- {: .un_theorem}
###### Conjecture (Etingof, Nikshcych and Ostrik)

Every fusion category admits a [[pivotal structure]].

=--

Providing a certain condition is satisfied, a pivotal structure on a fusion category can be shown to correspond to a 'twisted' monoidal natural transformation of the identity functor on the category, where the twisting is given by the [[pivotal symbols]].


### Relation to extended 3d TQFT 
 {#RelationtoTQFT}

Given the data of a [[fusion category]] one can build a 3d [[extended TQFT]] by various means. This is explained by the fact, see below, that fusion categories are (probably precisely) the [[fully dualizable object]]s in the [[3-category]] $MonCat$ of [[monoidal categories]]. This implies by the [[homotopy hypothesis]] that and how they induce 3d [[TQFT]]s.


+-- {: .num_defn #MonCan}
###### Definition

Write $MonCaT$ for the [[(infinity,n)-category|(infinity,3)-category]] has as 

* objects [[monoidal categories]], 

* as morphism [[bimodule]]s of these, 

* and so on.

=--

+-- {: .num_prop}
###### Proposition

With its natural [[tensor product]], $MonCat$ is a [[symmetric monoidal (infinity,n)-category|symmetric monoidal (infinity,3)-category]].

=--

+-- {: .num_prop}
###### Proposition

A monoidal category which is fusion is [[fully dualizable object|fully dualizable]] in $MonCat$

=--

This is due to ([DouglasSchommer-PriesSnyder](#DSPS))

## Suggestions ##

Here are three things such that it'd be awesome if they were sorted out on this page:

1. Kuperberg's theorem saying that [[abelian category|abelian]] semisimple implies [[linear category|linear]] over some field. [Finite, connected, semisimple, rigid tensor categories are linear](http://arxiv.org/abs/math/0209256)

2. Some correct version of the claim that abelian semisimple is the same as [[idempotent complete category|idempotent complete]] and nondegenerate. [Math Overflow question](http://mathoverflow.net/questions/245/are-abelian-nondegenerate-tensor-categories-semisimple)

3. Good notation distinguishing [[simple object|simple]] versus [[absolutely simple object|absolutely simple]] (is $End(V) = k$ or just $V$ has no nontrivial proper subobjects).
 

Together 1 and 2 let you go between the two different obvious notions of semisimple which seem a bit muddled here when I clicked through the links.


## Related concepts

* **fusion category**

* [[pivotal category]]

* [[spherical category]]

## References ##

Some classical references include

* [[P. Etingof]], D. Nikshych and V. Ostrik, [On fusion categories](http://arxiv.org/abs/math/0203060).

* [[P. Etingof]] and D. Calaque, [Lectures on tensor categories](http://arxiv.org/abs/math/0401246).

* [[Michael Müger]], [Tensor categories: A selective guided tour](http://arxiv.org/abs/0804.3587).

* [[Pavel Etingof]], D. Nikshych and V. Ostrik, _Fusion categories and homotopy theory_ ,  Quantum Topology, 1(2010), 209-273. (Earlier version available as [ArXiv:0909.3140](http://arxiv.org/PS_cache/arxiv/pdf/0909/0909.3140v2.pdf)

A review is also in chapter 6 of

* [[Bruce Bartlett]], [On unitary 2-representations of finite groups and topological quantum field theory](http://arxiv.org/abs/0901.3975).


The relation to 3d TQFT is fully clarified in

* [[Chris Douglas]], [[Chris Schommer-Pries]], [[Noah Snyder]], _The Structure of Fusion Categories via 3D TQFTs_
 {#DSPS}

For some discussion see

* Math Overflow, _[Why are fusion categories interesting?](http://mathoverflow.net/questions/6180/why-are-fusion-categories-interesting)_ .


[[!redirects fusion categories]]