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

* The category of presheaves $PSh(C)$ is the [[free cocompletion]] of $C$.

* the [[Yoneda lemma]] says that the [[Yoneda embedding]] $j : C \to PSh(C)$ is -- in particular -- a [[full and faithful functor]].

* A category of presheaves is a [[topos]].

* A [[reflective subcategory]] of a category of presheaves is a [[locally presentable category]].

* A [[geometric embedding|sub-topos]] of a category of presheaves is a [[Grothendieck topos]]: a [[category of sheaves]].

+--{: .query}
[[David Roberts]]: so the only sub-topoi of $PSh(C)$ are categories of sheaves? Do these need to be sheaves on $C$ with some Grothendieck topology, or can they be sheaves on other sites? Isn't there some way of cooking up a sub-topos using a subcategory of $C$?
=--

## In higher category theory

For [[(∞,1)-category]] theory see [[(∞,1)-category of (∞,1)-presheaves]].

[[!redirects categories of presheaves]]
[[!redirects presheaf category]]
[[!redirects presheaf categories]]
