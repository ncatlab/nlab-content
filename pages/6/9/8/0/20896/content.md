

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

## Idea

Commutative monoidal categories are [[symmetric monoidal categories]] whose  [[tensor product]] is _strictly_ [[associative]] and [[unital]] (as for [[permutative categories]]), but also strictly [[commutative monoid|commutative]], in that the [[associators]], [[unitors]], and [[braidings]] are all the  [[identity natural transformation]]. 

Notice that the [[coherence theorem for symmetric monoidal categories]] only says that [[symmetric monoidal categories]] are symmetric monoidally equivalent to [[strict monoidal categories]] whose [[braidings]], however, may not be given by the identity.

## Examples

Commutative monoidal categories are the natural type of category that [[Petri nets]] freely generate ([Meseguer-Montanari 90](#MeseguerMontanari90), [Baez-Master 18, Section 2](#BaezMaster18)).   

The symmetric monoidal category of [[line bundles]] on a topological space, or [[smooth line bundles]] on a manifold, or [[invertible sheaf|invertible sheaves]] on a variety or scheme, is symmetric monoidally equivalent to a commutative monoidal category under the usual tensor product of these structures.

Any abelian group object in $Cat$ is a commutative monoidal category.

## Definition

A commutative monoidal category is a [[commutative monoid object]]  in [[Cat]]  with its [[cartesian product]].  Equivalently, it is an [[internal category]] in the category of [[commutative monoids]].

Explicitly, the data of a commutative monoidal category are:

* A commutative monoid of objects $C_1$,

* a commutative monoid of morphisms $C_0$,

* source and target [[monoid homomorphisms]] $s,t \colon C_1 \to C_0$,

* an identity assigning monoid homomorphism $i \colon C_0 \to C_1$ and,

* a homomorphism $\circ \colon C_1 \times_C_0 C_1 \to C_1$ representing composition.

These homorphisms are required to satisfy the axioms of a [[category]]. In particular, because composition is a commutative monoid homomorphism, it satisfies the [[interchange law]]

$$ (g \circ f) + (h \circ k) = (g + h) \circ (f + k) $$

whenever all composites are defined.

## Characterization up to equivalence

One might [[conjecture]] that a symmetric monoidal category is symmetric monoidally equivalent to a commutative monoidal category iff all its self-braidings

$$   B_{x,x} \colon x \otimes x \to x \otimes x $$

are identity morphisms.  Note that since a commutative monoidal category has this property, and this property is invariant under symmetric-monoidal equivalence, the "only if" part of the characterization is certainly true.

This conjecture was proved in [Kim 16](#Kim16) under the assumption that the objects of the monoidal category can be [[totally ordered]] (which is true, for instance, assuming the [[axiom of choice]], or assuming the weaker [[ultrafilter principle]] which states that every [[filter]] extends to an [[ultrafilter]]).

## References

* {#MeseguerMontanari90} [[José Meseguer]], [[Ugo Montanari]], _Petri Nets are Monoids_ ([pdf](https://core.ac.uk/download/pdf/82342688.pdf))

* {#BaezMaster18} [[John Baez]], [[Jade Master]], Section 2 of: _Open Petri Nets_ ([arXiv:1808.05415](https://arxiv.org/abs/1808.05415))

* [[James Dolan]], _[[jamesdolan:Algebraic Geometry|Doctrines of Algebraic Geometry]]_

* {#Kim16}[[Youngsoo Kim]], _A Note on Strict Commutativity of a Monoidal Product_, Pure and Applied Mathematics Journal Volume 5, Issue 5, October 2016, pp. 155-159, [url](https://doi.org/10.11648/j.pamj.20160505.13)


[[!redirects commutative monoidal categories]]
[[!redirects Commutative monoidal category]]
[[!redirects Commutative monoidal categories]]


