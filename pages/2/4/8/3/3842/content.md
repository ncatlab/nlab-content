
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
* automatic table of contents goes here
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

### Cartesian closed monoidal structure

As every [[topos]], a category of presheaves is a [[cartesian monoidal category|cartesian]] [[closed monoidal category]].

For details on the closed structure see

* [[closed monoidal structure on presheaves]].

### Presheaves on over-categories and over-categories of presheaves {#RelWithOvercategories}

Let $C$ be a [[category]], $c$ an [[object]] of $C$ and let $C/c$ be the [[over category]] of $C$ over $c$. Write
$PSh(C/c) = [(C/C)^{op}, Set]$ for the category of [[presheaf|presheaves]] on $C/c$ and write
$PSh(C)/Y(y)$ for the [[over category]] of [[presheaf|presheaves]] on $C$ over the presheaf $Y(c)$, where $Y : C \to PSh(c)$ is the [[Yoneda embedding]]. 

+-- {: .un_prop}
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

Suppose the presheaf $F \in PSh(C/c)$ does not actually depend on the morphsims to $C$, i.e. suppose that it factors through the forgetful functor from the [[over category]] to $C$:
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



## In higher category theory

For [[(∞,1)-category]] theory see [[(∞,1)-category of (∞,1)-presheaves]].

[[!redirects categories of presheaves]]
[[!redirects presheaf category]]
[[!redirects presheaf categories]]

[[!redirects categories of presheaves]]

[[!redirects presheaf topos]]
[[!redirects presheaf toposes]]
[[!redirects presheaf topoi]]