
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--
#Contents#
* table of contents
{:toc}

## Definition

Let $C$ be a [[category]] with [[finite limits]]. A **[[coherent logic|coherent]] [[hyperdoctrine]]** over $C$ is a [[functor]]

$$
  P : C^{op} \to DistLattice
$$

from the [[opposite category]] of $C$ to the category of [[distributive lattices]], such that for every [[morphism]] $f : A \to B$ in $C$, the functor $P(f) : P(B) \to P(A)$ has a [[left adjoint]] $\exists_f$ satisfying

1. [[Frobenius reciprocity]];

1. [[Beck-Chevalley condition]].

## Properties
 {#Properties}

The assignment ([here](#OverACoherentCategory)) of a coherent hyperdoctrine $S(C)$ to a [[coherent category]] $C$ extends to a [[2-adjunction]]

$$
  (A \dashv S)
  :
  CoherentCat 
   \stackrel{\overset{A}{\leftarrow}}{\underset{S}{\hookrightarrow}}
  CoherentHyperdoctrine
$$

with the [[right adjoint]] being a [[full and faithful 2-functor]], hence exhibiting $CoherentCat$ as a [[reflective sub-2-category]] of $CoherentHyperdoctrine$.

(Here $CoherentCat$ has as [[2-morphisms]] those [[natural transformations]] that preserve finite products.)

This appears as ([Coumans, prop. 8](#Coumans)).

Coherent hyperdoctrines are closed under [[canonical extension]] $(-)^\delta : DistLattice \to DistLattice$, in that for $P : C^{op} \to DistLattic$ a coherent hyperdoctrine, so is $(-)^\delta \circ P$.

This appears as ([Coumans, prop. 9](#Coumans)).


## Examples

### Powersets

The [[powerset]] functor

$$
  P := \{0,1\}^{(-)} : Set^{op} \to DistLattice
$$

(sending a [[set]] to its [[power set]] and a [[function]] to the [[preimage]]-assignment) is a coherent hyperdoctrine. 

### Over a coherent category
 {#OverACoherentCategory}

Let $C$ be a [[coherent category]]. For every [[object]] $A \in C$ the [[poset of subobjects]] $Sub_C(A)$ is a [[distributive lattice]]. 

The corresponding [[functor]]

$$
  C^{op} \to DistLattice
$$ 

from the [[opposite category]] of $C$ to the category of distributive lattices is called the **coherent hyperdoctrine** of $C$.

### For a coherent theory

Accordingly, there is a coherent hyperdoctrine associated with any [[coherent theory]], where the objects of $C$ are lists of [[free variables]] in the theory, and the lattice assigned to them is that of [[propositions]] of the theory in this [[context]].

## Related concepts

[[!include categories and logic - table]]

## References

* Dion Coumans, _Generalizing canonical extensions to the categorical setting_ ([Arxiv](http://arxiv.org/abs/1204.3745))
 {#Coumans}

* Graham Manuell, *Quantalic spectra of semirings*, ([arXiv:2201.06408](https://arxiv.org/abs/2201.06408))

[[!redirects coherent hyperdoctrines]]