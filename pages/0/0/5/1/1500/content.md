
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

A **fusion category** is a [[rigid monoidal category|rigid]] [[semisimple category|semisimple]] [[linear category|linear]] ([[Vect]]-[[enriched category|enriched]]) [[monoidal category]] ("[[tensor category]]"), with only [[finite number|finitely]] many [[decategorification|isomorphism classes]] of [[simple objects]], such that the [[endomorphisms]] of the unit object form just the [[ground field]] $k$.

=--

Often one also assumes a [[braided monoidal category|braiding]] and speaks of a *braided fusion category*.


## Examples

The name "fusion category" comes from the central examples of structures whose canonical [[tensor product]] is called a "fusion product", notably [[representations]] of [[loop groups]] and of [[Hopf algebras]] and of [[vertex operator algebras]]. 

Some of the easiest examples are:

* Representations of a finite group or ([finite super-group](https://ncatlab.org/nlab/show/supergroup#finite_supergroups))
* For a given finite group $G$ and a 3-cocycle on $G$ with values in (the multiplicative group of units of) a field $k$ (an element of $H^3(G,k^\times)$), take $G$-graded vector spaces with the cocycle as associator.

## Properties

### Relation to weak Hopf algebras

Under [[Tannaka duality]], every fusion category $C$ arises as the [[representation category]] of a [[weak Hopf algebra]]. ([Ostrik](#Ostrik))

### Relation to pivotal and spherical categories

Fusion categories were first systematically studied by [[Etingof]], Nikshych and [[Ostrik]] in [On fusion categories](http://arxiv.org/abs/math/0203060). This paper listed many examples and proved many properties of fusion categories. One of the important conjectures made in that paper was the following:

+-- {: .num_theorem}
###### Conjecture (Etingof, Nikshych, and Ostrik)

Every fusion category admits a [[pivotal structure]].

=--

Providing a certain condition is satisfied, a pivotal structure on a fusion category can be shown to correspond to a 'twisted' monoidal natural endotransformation of the identity functor on the category, where the twisting is given by the [[pivotal symbols]].


### Relation to extended 3d TQFT 
 {#RelationtoTQFT}

Given the data of a [[fusion category]] one can build a 3d [[extended TQFT]] by various means. This is explained by the fact, see below, that fusion categories are (probably precisely) the [[fully dualizable object]]s in the [[3-category]] $MonCat$ of [[monoidal categories]]. By the [[homotopy hypothesis]] this explains how they induce [[3d TQFT]]s.


+-- {: .num_defn #MonCat}
###### Definition

Write $MonCat_{bim}$ for the [[(infinity,n)-category|(infinity,3)-category]] which has as 

* objects [[monoidal categories]], 

* morphism [[bimodule]]s of these, 

* and so on.

=--

+-- {: .num_prop}
###### Proposition

With its natural [[tensor product]], $MonCat$ is a [[symmetric monoidal (infinity,n)-category|symmetric monoidal (infinity,3)-category]].

=--

+-- {: .num_prop #FusionCategoriesAreFullyDualizable}
###### Proposition

A monoidal category which is fusion is [[fully dualizable object|fully dualizable]] in the [[(infinity,n)-category|(infinity,3)-category]] $MonCat_{bim}$, def. \ref{MonCat}.

=--

This is due to ([Douglas & Schommer-Pries & Snyder 13](#DSPS13)).

+-- {: .num_remark}
###### Remark

Via the [[cobordism theorem]] prop. \ref{FusionCategoriesAreFullyDualizable} implies that fusion categories encode [[extended TQFTs]] on 3-dimensional [[framed manifold|framed]] [[cobordisms]], while their $O(3)$-[[homotopy fixed points]] encode extended 3d TQFTs on general (not framed) cobordisms. 

These 3d TQFTs hence arise from similar algebraic data as the [[Turaev-Viro model]] and the [[Reshetikhin-Turaev construction]], however there are various slight differences. See ([Douglas & Schommer-Pries & Snyder 13, p. 5](#DSPS13)).
 
=--


## Suggestions ##

Here are three things such that it'd be awesome if they were sorted out on this page:

1. Kuperberg's theorem saying that [[abelian category|abelian]] semisimple implies [[linear category|linear]] over some field. [Finite, connected, semisimple, rigid tensor categories are linear](http://arxiv.org/abs/math/0209256)

2. Some correct version of the claim that abelian semisimple is the same as [[idempotent complete category|idempotent complete]] and nondegenerate. [Math Overflow question](http://mathoverflow.net/questions/245/are-abelian-nondegenerate-tensor-categories-semisimple)

3. Good notation distinguishing [[simple object|simple]] versus [[absolutely simple object|absolutely simple]] (is $End(V) = k$ or just $V$ has no nontrivial proper subobjects).
 

Together 1 and 2 let you go between the two different obvious notions of semisimple which seem a bit muddled here when I clicked through the links.


## Related concepts

* **fusion category**
  
  * [[unitary fusion category]]

  * [[fusion ring]], [[Frobenius-Perron dimension]]

* [[pivotal category]]

* [[spherical category]]

* [[modular tensor category]]

* [[Deligne's theorem on tensor categories]]

* [[graded fusion category]]

* [[Tambara-Yamagami category]]


## References ##

### General

Original articles:

* {#EtingofNikshychOstrik05} [[Pavel Etingof]], [[Dmitri Nikshych]], [[Victor Ostrik]], *On fusion categories*, Annals of Mathematics Second Series, Vol. 162, No. 2 (Sep., 2005), pp. 581-642 ([arXiv:math/0203060](http://arxiv.org/abs/math/0203060), [jstor:20159926](https://www.jstor.org/stable/20159926))

* [[Pavel Etingof]] and [[Damien Calaque]], [Lectures on tensor categories](http://arxiv.org/abs/math/0401246).

* [[Michael Müger]], [Tensor categories: A selective guided tour](http://arxiv.org/abs/0804.3587).

* [[Pavel Etingof]], D. Nikshych and V. Ostrik, _Fusion categories and homotopy theory_ ,  Quantum Topology, 1(2010), 209-273. (Earlier version available as [ArXiv:0909.3140](http://arxiv.org/PS_cache/arxiv/pdf/0909/0909.3140v2.pdf)

* [[Vladimir Drinfeld]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], *On braided fusion categories I*, Selecta Mathematica. New Series 16 (2010), no. 1, 1–119 ([doi:10.1007/s00029-010-0017-z](https://doi.org/10.1007/s00029-010-0017-z))


Further review:

* [[Bruce Bartlett]], chapter 6 of
*[On unitary 2-representations of finite groups and topological quantum field theory](http://arxiv.org/abs/0901.3975)*.

On the [[Tannaka duality]] to [[weak Hopf algebras]]:

* Takahiro Hayashi, _A canonical Tannaka duality for finite seimisimple tensor categories_ ([arXiv:math/9904073](http://arxiv.org/abs/math/9904073))

* {#Ostrik} [[Victor Ostrik]], _Module categories, weak Hopf algebras and modular invariants_ ([arXiv:math/0111139](http://arxiv.org/abs/math/0111139)) 
 


The relation to [[3d TQFT]] clarified via the [[cobordism hypothesis]]:

* {#DSPS} [[Chris Douglas]], [[Chris Schommer-Pries]], [[Noah Snyder]], _The Structure of Fusion Categories via 3D TQFTs_ ([talk pdf](https://sites.google.com/site/chrisschommerpriesmath/Home/recent-and-upcoming-talks/UPennTalk.pdf?attredirects=0))
 

* {#DSPS13} [[Chris Douglas]], [[Chris Schommer-Pries]], [[Noah Snyder]], _Dualizable tensor categories_ ([arXiv:1312.7188](http://arxiv.org/abs/1312.7188))

and for the case of [[modular tensor categories]]:

* [[Bruce Bartlett]], [[Christopher Douglas]], [[Chris Schommer-Pries]], [[Jamie Vicary]], _Modular categories as representations of the 3-dimensional bordism 2-category_ ([arXiv:1509.06811](http://arxiv.org/abs/1509.06811))

Discussion in terms of [[skein relations]]:

* Anup Poudel, [[Sachin J. Valera]], *Skein-Theoretic Methods for Unitary Fusion Categories* &lbrack;[arXiv:2008.07129](https://arxiv.org/abs/2008.07129)&rbrack;


See also:

* Math Overflow, _[Why are fusion categories interesting?](http://mathoverflow.net/questions/6180/why-are-fusion-categories-interesting)_ .


On a notion of fusion [[2-categories]]:

* [[Christopher L. Douglas]], [[David J. Reutter]], *Fusion 2-categories and a state-sum invariant for 4-manifolds* &lbrack;[arXiv:1812.11933](https://arxiv.org/abs/1812.11933)&rbrack;

* Thibault D. Décoppet, Matthew Yu, *Fiber 2-Functors and Tambara-Yamagami Fusion 2-Categories* &lbrack;[arXiv:2306.08117](https://arxiv.org/abs/2306.08117)&rbrack;







[[!include anyonic topological order via braided fusion categories -- references]]





[[!redirects fusion categories]]

[[!redirects braided fusion category]]
[[!redirects braided fusion categories]]

[[!redirects fusion]]

[[!redirects fusion 2-category]]
[[!redirects fusion 2-categories]]

