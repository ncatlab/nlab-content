
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
 {#Examples}

The name "fusion category" comes from the central examples of structures whose canonical [[tensor product]] is called a "fusion product", notably [[representations]] of [[loop groups]] and of [[Hopf algebras]] and of [[vertex operator algebras]]. 

Simple examples:

\begin{example}
\label{GradedVectorSpaces}
**(graded vector spaces)**
\linebreak
For 

* $G$ a [[finite group]],

* $\mathbb{K}$ a [[field]],

the category of [[finite-dimensional vector space|finite-dimensional]] $G$-[[graded vector spaces|graded]] $\mathbb{K}$-[[vector spaces]]

$$
  Vect_{G}^{fdim}
$$ 

is a fusion category, with [[tensor product]] given by the [[tensor product of vector spaces]] and the [[binary operation]] of the group:

$$
  V_g \otimes W_h
  \;\;
  \coloneqq
  \;\;
  (V \otimes W)_{g \cdot h}
  \,.
$$

More generally, for 

* $\omega \,\in\, H^3_{Grp}(G, \mathbb{K}^\times)$ a 3-cocycle in the [[group cohomology]] of $G$ with [[coefficients]] in the [[group of units]] $\mathbb{K}^\times$, 

the above construction but with [[associator]] multiplied by the 3-cocycle applied to the $G$-degrees of the 3 factors is again a fusion category


$$
  Vect_{G, \omega}^{fdim}
  \,.
$$ 
\end{example}
([Etingof, Nikshych & Ostrik 2005, item 1. on p. 584](#EtingofNikshychOstrik05))

\begin{example}
For $\mathbb{K}$ a [[field]] and
$G$ a [[finite group]] (or [finite super-group](supergroup#finite_supergroups)), whose [[order of a group|order]] is [[coprime integer|relatively prime]] to the [[characteristic of a field|characteristic]] of $\mathbb{K}$, then the [[category of representations]] $Rep(G, \mathbb{K})$ is a fusion category. 
\end{example}
([Etingof, Nikshych & Ostrik 2005, item 2. on p. 584](#EtingofNikshychOstrik05))


## Properties

### Relation to weak Hopf algebras

Under [[Tannaka duality]], every fusion category $C$ arises as the [[representation category]] of a [[weak Hopf algebra]] ([Ostrik](#Ostrik)). However, this does not mean  that every fusion category admits a [[fiber functor]] to the [[Vect|category of vector spaces]] $\text{Vect}= k-Mod$. 

Given any multi-fusion category $C$, one can always construct a fiber functor $F:C\to RMod$ for $R$ the algebra spanned by a basis of orthogonal idempotents $\{v_i\}_{i\in I}$ for $I$ the equivalence classes of simple objects of $C$. This functor is referred to in some sources as a *generalized* fiber functor. The endomorphisms of this functor then give a weak Hopf algebra that represents $C$. In [Hayashi 1999](#Hayashi99) (see there for the relevant definitions), this is computed as a [[coend]], where one has that $C\cong Rep(A)$ for $A= \text{coend}(F^*\otimes F: C^{op} \times C \to Bmd(E))$, where $E=\dot R\otimes R$ is equipped with a coalgebra structure
$$
\Delta(\dot\lambda \mu) = \sum_{\nu\in I} \dot\lambda \nu\otimes \dot\nu \mu
$$
$$
\epsilon (\dot\lambda \mu) = \delta_{\lambda,\mu}
$$

It is important to note that, generally speaking, $C$ may admit other fiber functor to different module categories $RMod$, as is the case for fusion categories of the form $Rep(H)$ for $H$ a Hopf algebra, which admits both the fiber functor described above, as well as a fiber functor to $\text{Vect}$.


### Relation to pivotal and spherical categories

Fusion categories were first systematically studied by [Etingof, Nikshych & Ostrik 2005](#EtingofNikshychOstrik05). This paper listed many examples and proved many properties of fusion categories. One of the important conjectures made in that paper was the following:

+-- {: .num_theorem}
###### Conjecture (Etingof, Nikshych, and Ostrik)

Every fusion category admits a [[pivotal structure]].

=--

Providing a certain condition is satisfied, a pivotal structure on a fusion category can be shown to correspond to a 'twisted' monoidal natural endotransformation of the identity functor on the category, where the twisting is given by the [[pivotal symbols]].

### Tube (Ocneanu) algebra

Every fusion category $\mathcal{C}$ has a [[tube algebra]], which encodes an action by conjugation of $\mathcal{C}$ on itself. See there for more.


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



## Related concepts

* **fusion category**
  
  * [[unitary fusion category]]

  * [[fusion 2-category]]

  * [[fusion ring]], [[Frobenius-Perron dimension]]

* [[pivotal category]]

* [[spherical category]]

* [[modular tensor category]]

* [[Deligne's theorem on tensor categories]]

* [[graded fusion category]]

* [[Tambara-Yamagami category]]


## References ##

### General

Motivation as generalization of (the [[representation theory]] of) [[finite groups]]:

* [[Greg Kuperberg]] (2009) &lbrack;[MO:a/6183](https://mathoverflow.net/a/6183/381)&rbrack;

Original articles:

* {#EtingofNikshychOstrik05} [[Pavel Etingof]], [[Dmitri Nikshych]], [[Victor Ostrik]], *On fusion categories*, Annals of Mathematics Second Series **162** 2 (2005) 581-642 &lbrack;[arXiv:math/0203060](http://arxiv.org/abs/math/0203060), [jstor:20159926](https://www.jstor.org/stable/20159926)&rbrack;

* [[Pavel Etingof]] and [[Damien Calaque]], [Lectures on tensor categories](http://arxiv.org/abs/math/0401246).

* [[Michael Müger]], [Tensor categories: A selective guided tour](http://arxiv.org/abs/0804.3587).

* [[Pavel Etingof]], D. Nikshych and V. Ostrik, _Fusion categories and homotopy theory_ ,  Quantum Topology, 1(2010), 209-273. (Earlier version available as [ArXiv:0909.3140](http://arxiv.org/PS_cache/arxiv/pdf/0909/0909.3140v2.pdf)

* [[Vladimir Drinfeld]], [[Shlomo Gelaki]], [[Dmitri Nikshych]], [[Victor Ostrik]], *On braided fusion categories I*, Selecta Mathematica. New Series **16** 1 (2010) 1–119 &lbrack;[arXiv:0906.0620](https://arxiv.org/abs/0906.0620), [doi:10.1007/s00029-010-0017-z](https://doi.org/10.1007/s00029-010-0017-z)&rbrack;


Further review:

* [[Bruce Bartlett]], chapter 6 of
*[On unitary 2-representations of finite groups and topological quantum field theory](http://arxiv.org/abs/0901.3975)*.

On the [[Tannaka duality]] to [[weak Hopf algebras]]:

* {#Hayashi99} Takahiro Hayashi, _A canonical Tannaka duality for finite seimisimple tensor categories_ ([arXiv:math/9904073](http://arxiv.org/abs/math/9904073))

* {#Ostrik} [[Victor Ostrik]], _Module categories, weak Hopf algebras and modular invariants_ ([arXiv:math/0111139](http://arxiv.org/abs/math/0111139)) 
 


The relation to [[3d TQFT]] clarified via the [[cobordism hypothesis]]:

* {#DSPS} [[Chris Schommer-Pries]], *The Structure of Fusion Categories via 3D TQFTs* (2001) &lbrack;[[DSSFusionSlides.pdf:file]]&rbrack;
 

* {#DSPS13} [[Chris Douglas]], [[Chris Schommer-Pries]], [[Noah Snyder]], *Dualizable tensor categories*, Memoirs of the AMS **268** 1308 (2021) &lbrack;[arXiv:1312.7188](http://arxiv.org/abs/1312.7188), [ams:memo-268-1308](https://bookstore.ams.org/memo-268-1308)&rbrack;

and for the case of [[modular tensor categories]]:

* [[Bruce Bartlett]], [[Christopher Douglas]], [[Chris Schommer-Pries]], [[Jamie Vicary]], _Modular categories as representations of the 3-dimensional bordism 2-category_ ([arXiv:1509.06811](http://arxiv.org/abs/1509.06811))

Discussion in terms of [[skein relations]]:

* Anup Poudel, [[Sachin J. Valera]], *Skein-Theoretic Methods for Unitary Fusion Categories* &lbrack;[arXiv:2008.07129](https://arxiv.org/abs/2008.07129)&rbrack;


See also:

* Math Overflow, *Why are fusion categories interesting?* &lbrack;[MO:q/6180](https://mathoverflow.net/q/6180/381)&rbrack; 

Further work on their classification using finite groups:

* Agustina Czenky: *Diagramatics for cyclic pointed fusion categories* &lbrack;[arXiv:2404.08084](https://arxiv.org/abs/2404.08084)&rbrack;

On a notion of [[fusion 2-categories]]:

* [[Christopher L. Douglas]], [[David J. Reutter]], *Fusion 2-categories and a state-sum invariant for 4-manifolds* &lbrack;[arXiv:1812.11933](https://arxiv.org/abs/1812.11933)&rbrack;

* {#DY23} [[Thibault Decoppet]], [[Matthew Yu]]. *Fiber 2-Functors and Tambara-Yamagami Fusion 2-Categories*. (2023) &lbrack;[arXiv:2306.08117](https://arxiv.org/abs/2306.08117)&rbrack;

On fusion categories [[invertible object|invertible]] with respect to the [[Deligne tensor product of abelian categories|Deligne tensor product]]:

* Sean Sanford, [[Noah Snyder]]: *Invertible Fusion Categories* &lbrack;[arXiv:2407.02597](https://arxiv.org/abs/2407.02597)&rbrack;






[[!include anyonic topological order via braided fusion categories -- references]]





[[!redirects fusion categories]]

[[!redirects braided fusion category]]
[[!redirects braided fusion categories]]

[[!redirects fusion]]


