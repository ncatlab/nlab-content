
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Generally, a **coherence theorem** in [[category theory]] and [[higher category theory]] asserts that a [[coherence law]] is satisfied: it is a means of getting a handle on categorical structures where laws only hold up to [[isomorphism]] or higher [[k-morphism]] equivalences.

Given a [[doctrine]], such as the doctrine for monoidal categories, a coherence theorem may provide a full or partial algorithm for deciding equality in free algebras.  Usually such a doctrine is specified only by certain "generating" operations and constraint morphisms between them; the coherence question then consists in determining exactly what additional operations and morphisms are derivable from these, and in particular when two such derived morphisms are equal.  For instance, one may be interested in the coherence problem for closed categories: how does one decide equality of morphisms in freely generated closed categories, or in other words, how does one decide which diagrams (generated from the closed structure) commute?

The first, and perhaps easiest, coherence theorem is Mac Lane's, which says that in a free [[monoidal category]], *every* diagram of constraint morphisms commutes.  The especially nice form of this theorem should not lead one to expect that all coherence theorems are of the form "every diagram commutes"---in many categorical structures, it is *not* the case that all diagrams of constraints commute, and so the coherence question must address more precisely *which* diagrams of constraints commute.  For instance, in a [[braided monoidal category]] not every diagram of constraints commutes, but the coherence theorem gives a concise classification of those that do in terms of their underlying braids.

Coherence theorems are often useful when working with algebras in a doctrine, since it provides a way to tell whether two particular composites of constraints which may arise in practice are actually equal.  One should beware, however, that coherence theorems only relate to the behavior of *free* algebras, or equivalently to the equality of *formally defined* composites.  Even in a structure having a coherence theorem of the "every diagram commutes" sort, it may happen in a *particular* algebra that there exist diagrams of constraints which do not commute.  For instance, one can find a monoidal category containing objects $x,y,z$ such that $x\otimes (y\otimes z) = (x\otimes y)\otimes z$ on the nose, but such that the [[associator]] isomorphism $a_{x,y,z}:x\otimes (y\otimes z) \stackrel{\simeq}{\to} (x\otimes y)\otimes z$ is not the identity.  (For example, [[skeletons]] of naturally occurring monoidal categories often have this property.  This issue also arises in the classification of [[2-groups]] via cohomology.)

## Coherence versus strictification

See [[coherence versus strictification]].

## List of coherence theorems
 {#ListOfTheorems}

* [[coherence theorem for monoidal categories]]
* [[coherence theorem for symmetric monoidal categories]]
* [[coherence theorem for braided monoidal categories]]
* [[coherence theorem for tortile categories]]
* [[coherence theorem for closed symmetric monoidal categories]]

* [coherence theorem for bicategories](/nlab/show/bicategory#Coherence)
* [coherence theorem for tricategories](/nlab/show/tricategory#Coherence)
* [[coherence theorem for monoidal bicategories]]
* [[coherence theorem for braided monoidal bicategories]]
* [[coherence theorem for symmetric monoidal bicategories]]

## Related pages

* [[strictification theorem]]

## References

[[Saunders Mac Lane]] discusses some of the history of the coherence problem in section 5 of

* [[Saunders Mac Lane]], Topology and Logic as a Source of Algebra (Retiring Presidential Address), _Bulletin of the AMS_ 82:1, January 1976. ([euclid](https://projecteuclid.org/euclid.bams/1183537593))

An account of some of the history of (proofs of) coherence theorems is at 

* [linear type theory -- History of categorical semantics](linear+type+theory#HistoryCategoricalSemantics) .

See also at _[[Kelly-Mac Lane graph]]_, at _[[proof net]]_ and at _[[Trimble rewiring]]_ for more on the [[syntax|syntactic]] proofs of coherence.

For specific references see at the above sub-entries in the [List of coherence theorems](#ListOfTheorems).

For some general frameworks, see the following.

* [[Thomas Fiore]], Po Hu, and Igor Kriz. _Laplaza sets, or how to select coherence diagrams for pseudo algebras_, Advances in mathematics 218.6 (2008): 1705-1722.
* Miles Gould. _Coherence for categorified operadic theories_, PhD thesis, [arXiv:1002.0879](https://arxiv.org/abs/1002.0879) (2010).

[[!redirects coherence theorems]]