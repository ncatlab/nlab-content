

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

Commutative monoidal categories are the natural type of category that [[Petri nets]] freely generate ([Baez-Master 18, Section 2](#BaezMaster18))

## Definition

A commutative monoidal category is a [[commutative monoid object]]  in [[Cat]]  with its [[cartesian product]].  Explicitly, the data of a commutative monoidal category is:

* A commutative monoid of objects $C_1$,

* a commutative monoid of morphisms $C_0$,

* source and target [[monoid homomorphisms]] $s,t \colon C_1 \to C_0$,

* an identity assigning monoid homomorphism $i \colon C_0 \to C_1$ and,

* a homomorphism $\circ \colon C_1 \times_C_0 C_1 \to C_1$ representing composition.

These homorphisms are required to satisfy the axioms of a [[category]]. In particular, because composition is a commutative monoid homomorphism, it satisfies the [[interchange law]]

$$ (g \circ f) + (h \circ k) = (g + h) \circ (f + k) $$

whenever all composites are defined.

## References

* {#BaezMaster18} [[John Baez]], [[Jade Master]], Section 2 of: _Open Petri Nets_ ([arXiv:1808.05415](https://arxiv.org/abs/1808.05415))


[[!redirects commutative monoidal categories]]


