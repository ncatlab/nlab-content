
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Canonical extension provides an algebraic formulation of [[duality]] theory and a tool to derive representation theorems. It may be regarded as an algebraic formulation of [[Stone duality]] (see [Gehrke-Vosmaer, p. 5](#GehrkeVosmaer)).

Originally ([Jonsson-Tarski](#JonssonTarski)) is was formulated for [[Boolean algebras]] with operators, but the notion was later generalized to [[distributive lattices]] and even to arbitrary [[posets]].

## Definition

### For distributive lattices

Given a [[distributive lattice]] $L$, its **canonical extension** $L^\delta$ is the [[downset]] [[lattice]] of the [[poset]] of [[prime filters]] of $L$, ordered by inclusion.

This construction extends to a [[functor]]

$$
  (-)^\delta : DistLattice \to DistLattice^+
$$

from the [[category]] of [[distributive lattices]] to that of [[completely distributive lattice|completely distributive]] [[algebraic lattices]]. This is [[left adjoint]] to the corresponding [[forgetful functor]], exhibiting [[completely distributive algebraic lattices]] as a [[reflective subcategory]] of the distributive lattices

$$
  DistLattice^+ \stackrel{\overset{(-)^\delta}{\leftarrow}}{\hookrightarrow}
  DistLattice
  \,.
$$

### For Heyting algebras
 {#ForHeytingAlgebras}

The canonical extension $L^\delta$ of a [[distributive lattice]] $L$ is a [[complete lattice|complete]] and [[completely distributive lattice]].

In particular the canonical extension is a [[Heyting algebra]]. If $L$ is itself already a Heyting algebra, then $e_L : L \to L^\delta$ preserves the Heyting [[implication]]. Also, canonical extension preserves homomorphisms of Heyting algebras. Hence it restricts to a functor

$$
  (-)^\delta : HeytingAlgebra \to HeytingAlgebra
  \,.
$$


### For coherent categories
 {#ForCoherentCategories}

A [[distributive lattice]] is a [[coherent category|cogerent]] [[(0,1)-category]]. One may therefore ask if there is a generalization of canonical extension to general [[coherent categories]]. 

The following is considered in ([Coumans](#Coumans)).

By the discussion at [[coherent category]] and [[coherent hyperdoctrine]], we have a [[reflective sub-2-category]] embedding

$$
 (\mathcal{A} \dashv \mathcal{S}) : CoherentCat \hookrightarrow CoherentHyperdoctrine
$$

given by sending a coherent category $C$ to its [[indexed category|self-indexing]] $c \mapsto C_{/c}$.

Since a [[coherent hyperdoctrine]] takes values in [[distributive lattices]], we can apply canonical extension of distributive lattices termwise to get a functor

$$
  (-)^\delta : CoherentHyperdoctrine \to CoherentHyperdoctrine
  \,.
$$

Define then canonical extension of coherent categories to be the [[2-functor]] induced from this under the above reflection:

$$
  (-)^\delta : CoherentCat
   \stackrel{\mathcal{S}}{\to}
  CoherentHyperdoctrine
    \stackrel{(-)^\delta}{\to}
  CoherentHyperdoctrine
    \stackrel{\mathcal{A}}{\to}
  CoherentCat
  \,.
$$

Under the restriction along the inclusion $DistLat \hookrightarrow CoherentCat$ this reproduces the canonical extension of distributive lattices: for $L$ a dsitributive lattice there is an equivalence

$$
  \mathcal{A}(\mathcal{S}_L^\delta)
  \simeq
  L^\delta
  \,.
$$

(This is ([Coumans, prop 12](#Coumans))).

### For Heyting categories

There is also a joint generalization of canonical extension for Heyting algebras ([here](#ForHeytingAlgebras)) and for coherent categories ([here](#ForCoherentCategories)).

Write $HeytingCat$ for the [[2-category]] of [[Heyting categories]], and $FirstOrderHyperdoctrine$ for the 2-category of [[first-order hyperdoctrines]] (which are, in particular, [[hyperdoctrines]] with values in [[Heyting algebras]]).

Then the above restricts to a [[reflective sub-2-category]] inclusion

$$
  (\mathcal{A} \dashv \mathcal{S})
  : 
  HeyteingCat
   \hookrightarrow
  FirstOrderHyperdoctrine
$$

This is ([Coumans, prop. 19](#Coumans)).

And the canonical extension of coherent categories accordingly restricts to a functor on Heyting categories

$$
  (-)^\delta : HeytingCat \to HeytingCat
  \,.
$$

Such that for $C$ a Heyting category, also the [[unit of an adjunction|unit]] $C \to C^\delta$ is a morpjism of Heyting categories.

This is ([Coumans, cor. 21](#Coumans)).

## Related concepts

* [[topos of types]]

## References

The study of canonical extensions originates in the articles

* B. J&#243;nsson, [[Alfred Tarski]], _Boolean algebras with operators, I_, Amer. J. Math. 73 (1951), 891&#8211;939.
 {#JonssonTarski}

Reviews include

* Mai Gehrke, Jacob Vosmaer, _A view of canonical extension_ ([arXiv:1009.2803](http://arxiv.org/abs/1009.2803))
 {#GehrkeVosmaer}

* Dion Coumans, _Generalizing canonical extensions to the categorical setting_, [pdf](http://www.math.ru.nl/~coumans/Generalisingcanonicalextensiontothecategoricalsetting-DionCoumans-vs2.pdf), to appear in Annals of Pure and Applied Logic
 {#Coumans}

[[!redirects canonical extensions]]
