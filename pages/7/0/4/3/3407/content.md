
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


#Contents#
* tableofcontents
{:toc}

## Definition

__$Dist Lat$__ is the [[category]] whose [[objects]] are [[distributive lattices]] and whose [[morphisms]] are lattice [[homomorphisms]], that is [[functions]] which preserve finitary [[meets]] and [[joins]] (equivalently, binary meets and joins and the [[top]] and [[bottom]] elements).  $Dist Lat$ is a [[replete subcategory|replete]] [[subcategory]] of [[Pos]] and a [[full subcategory|full]] and [[replete subcategory|replete]] [[subcategory]] of [[Lat]].

## Properties

$Dist Lat$ is given by a finitary [[variety of algebras]], or equivalently by a [[Lawvere theory]], so has all the usual properties of such categories.  The __[[free object|free]] distributive lattice__ on a [[set]] $X$ is the set of [[finite]] antichains of the [[finite power set]] $\mathcal{P}_{fin}$ of $X$; a collection $\mathcal{C}$ of  [[subsets]] of $X$ is an __antichain__ if, whenever $A \subseteq B$ for $A, B \in \mathcal{C}$, we have $A = B$ (that is, no two distinct elements of $\mathcal{C}$ may be comparable).  Note that $\mathcal{P}_{fin}X$ is the free [[semilattice]] on $X$; we may interpret an element of it as a finitary join of elements of $X$.  Then we interpret an element of $\mathcal{P}_{fin}\mathcal{P}_{fin}X$ as a finitary meet of elements of $\mathcal{P}_{fin}X$.  However, if two of the elements of $\mathcal{P}_{fin}X$ that appear in this meet are comparable, then we need only the smaller of them, so we take only the irredundant elements of $\mathcal{P}_{fin}\mathcal{P}_{fin}X$.  (We could equally well take joins of meets instead of meets of joins; then we keep only the larger of two meets that appear in a given join.)

## Related concepts

* [[coherent category]]

* [[coherent hyperdoctrine]]

* [[Pos]], [[Frm]], [[σFrm]]

category: category

[[!redirects DistLat]]
[[!redirects Dist Lat]]

[[!redirects free distributive lattice]]
