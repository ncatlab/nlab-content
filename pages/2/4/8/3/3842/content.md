
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For $C$ a [[small category]], its **category of presheaves** is the [[functor category]] 

$$
  PSh(C) := [C^{op}, Set]
$$

from the [[opposite category]] of $C$ to [[Set]]. 

An object in this category is a [[presheaf]]. See there for more details.

## Properties

### General

* The category of presheaves $PSh(C)$ is the [[free cocompletion]] of $C$.

* the [[Yoneda lemma]] says that the [[Yoneda embedding]] $j : C \to PSh(C)$ is -- in particular -- a [[full and faithful functor]].

* A category of presheaves is a [[topos]].

* The construction of forming (co)-presheaves extends to a [[2-functor]]

  $$
    [-,Set] : Cat \to Topos
  $$

  from the [[2-category]] [[Cat]] to the [[2-category]] [[Topos]]. (See at [[geometric morphism]] the section _<a href="http://nlab.mathforge.org/nlab/show/geometric+morphism#BetweenPresheafToposes">Between presheaf toposes</a>_ for details).

* A [[reflective subcategory]] of a category of presheaves is a [[locally presentable category]] if it is closed under $\kappa$-[[directed colimit]]s for some [[regular cardinal]] $\kappa$ (the embedding is an [[accessible functor]]).

* A [[geometric embedding|sub-topos]] of a category of presheaves is a [[Grothendieck topos]]: a [[category of sheaves]] (see there for details).

### Functoriality

See [[functoriality of categories of presheaves]].

### Characterization

+-- {: .num_thm}
###### Theorem 

A category $E$ is equivalent to a presheaf topos if and only if it is cocomplete, [[atomic category|atomic]], and [[regular category|regular]]. 

=-- 

This is due to [[Marta Bunge]].

### Cartesian closed monoidal structure

As every [[topos]], a category of presheaves is a [[cartesian monoidal category|cartesian]] [[closed monoidal category]].

For details on the closed structure see

* [[closed monoidal structure on presheaves]].

### Presheaves on over-categories and over-categories of presheaves {#RelWithOvercategories}

Let $C$ be a [[category]], $c$ an [[object]] of $C$ and let $C/c$ be the [[over category]] of $C$ over $c$. Write
$PSh(C/c) = [(C/c)^{op}, Set]$ for the category of [[presheaf|presheaves]] on $C/c$ and write
$PSh(C)/Y(c)$ for the [[over category]] of [[presheaf|presheaves]] on $C$ over the presheaf $Y(c)$, where $Y : C \to PSh(C)$ is the [[Yoneda embedding]]. 

+-- {: .num_prop #representable_case}
###### Proposition


There is an [[equivalence]] of categories

$$
  e : PSh(C/c) \stackrel{\simeq}{\to} PSh(C)/Y(c)
  \,.
$$

=--


+-- {: .proof}
###### Proof

The functor $e$ takes $F \in PSh(C/c)$ to the presheaf
$F' : d \mapsto \sqcup_{f \in C(d,c)} F(f)$ which is equipped with the natural transformation $\eta : F' \to Y(c)$ with component map $\eta_d \sqcup_{f \in C(d,c)} F(f) \to C(d,c)$.

A weak inverse of $e$ is given by the functor 
$$
  \bar e : PSh(C)/Y(c) \to PSh(C/c)
$$
which sends
$
  \eta : F' \to Y(C))
$ to $F \in PSh(C/c)$ given by
$$
  F : (f : d \to c) \mapsto F'(d)|_c
  \,,
$$
where $F'(d)|_c$ is the [[pullback]]
$$
  \array{
     F'(d)|_c &\to& F'(d)
     \\
     \downarrow && \downarrow^{\eta_d}
     \\
     pt &\stackrel{f}{\to}& C(d,c)
  }
  \,.
$$ 

=--


+-- {: .un_example}
###### Example

Suppose the presheaf $F \in PSh(C/c)$ does not actually depend on the morphisms to $C$, i.e. suppose that it factors through the forgetful functor from the [[over category]] to $C$:
$$
  F : (C/c)^{op} \to C^{op} \to Set
  \,.
$$

Then
$
  F'(d) = \sqcup_{f \in C(d,c)} F(f)
  = \sqcup_{f \in C(d,c)} F(d)
  \simeq
  C(d,c) \times F(d) 
$
and hence $F ' = Y(c) \times F$ with respect to the [[closed monoidal structure on presheaves]].

=--

See also [[functors and comma categories]].

For the analog statement in [[(∞,1)-category]] theory see

* <a href="http://ncatlab.org/nlab/show/(infinity%2C1)-category+of+(infinity%2C1)-presheaves#interaction_with_forming_overcategories_19">(∞,1)-category of (∞,1)-presheaves -- Interaction with overcategories</a>

+-- {: .un_remark}
###### Remark

Consider $\int_C Y(c)$ , the [[category of elements]] of $Y(c):C^{op}\to Set$. This has objects $(d_1,p_1)$ with $p_1\in Y(c)(d_1)$, hence $p_1$ is just an arrow $d_1\to c$ in $C$. A map from $(d_1, p_1)$ to $(d_2, p_2)$ is just a map $u:d_1\to d_2$ such that $p_2\circ u =p_1$ but this is just a morphism from $p_1$ to $p_2$ in $C/c$.

Hence, the above proposition \ref{representable_case} can be rephrased as $PSh(\int_C Y(c))\simeq PSh(C)/Y(c)$ which is an instance of the following formula:

=--

+-- {: .num_prop}
###### Proposition

Let $P:C^{op}\to Set$ be a presheaf. Then there is an [[equivalence of categories]]

$$
  PSh(\int_C P) \simeq PSh(C)/P
  \,.
$$

=--

For a proof see [Kashiwara-Schapira (2006, p.26)](#KS06). For a more general statement involving slices of Grothendieck toposes see [Mac Lane-Moerdijk (1994, p.157)](#MacLaneMoerdijk).

In particular, this equivalence shows that **slices of presheaf toposes are presheaf toposes**.

### Models in presheaf toposes

See at _[[models in presheaf toposes]]_.

## Related concepts

For [[(∞,1)-category]] theory see [[(∞,1)-category of (∞,1)-presheaves]].

[[!include locally presentable categories - table]]

## References

* {#SGA4} [[Michael Artin|M.Artin]], [[Alexander Grothendieck|A.Grothendieck]], [[J. L. Verdier]] (eds.), _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas - [[SGA 4]]_ , LNM **269** Springer  Heidelberg 1972.

* {#KS06} Masaki Kashiwara, Pierre Schapira, _Categories and Sheaves_ , Springer Heidelberg 2006.

* {#MacLaneMoerdijk} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994.

[[!redirects categories of presheaves]]
[[!redirects presheaf category]]
[[!redirects presheaf categories]]

[[!redirects categories of presheaves]]

[[!redirects presheaf topos]]
[[!redirects presheaf toposes]]
[[!redirects presheaf topoi]]