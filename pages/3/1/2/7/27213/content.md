
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

The notions of [[coherence theorems]] and of [[strictification theorems]] are strongly related. In the case of [[monoidal categories]], the coherence theorem states that every formal diagram in a monoidal category commutes, while the strictification theorem says that every monoidal category is monoidally equivalent to a strict monoidal category (see [[coherence and strictification for monoidal categories]]).

It is often possible to prove a strictification theorem using a coherence theorem and vice versa. The usual approach to proving both typically involves proving one directly, then proving the other from the first. Here, we shall sketch each approach, in the prototypical example of [[monoidal categories]].

An explicit description of the free algebras for a doctrine is often helpful, if not essential, in proving a [[strictification theorem]], since in a strict structure where constraints become equalities, many more diagrams will turn out to commute (being composed of identities).  On the other hand, given a [[strictification theorem]], if we have an explicit description of the strict structure (which is generally easier to come by), we can often deduce a characterization of the free algebras for the weak structure.

One thing to beware of is that, even for structures whose free-algebra coherence theorem is of the form "all diagrams commute", it does not necessarily follow that all such algebras can be fully strictified.

Confusing, the terms [[coherence theorem]] and [[strictification theorem]] are often interchanged. While they are related, and many structures of interest satisfy both coherence and strictification theorems, they are distinct.

## Coherence without strictification

For now, see section VII.2 of [Mac Lane](#MacLane) and [[Mac Lane's proof of the coherence theorem for monoidal categories ]].

## Strictification without coherence

For now, see [Heunen](#Heunen).

## Coherence from strictification

For now, see Theorem XI.3.2 (page 259) of [Mac Lane](#MacLane).

## Strictification from coherence

For now, see Theorem XI.3.1 (page 257) of [Mac Lane](#MacLane).

## Related pages

* [[coherence theorem]]
* [[strictification theorem]]

## References

* {#MacLane} [[Categories for the Working Mathematician]], [[Mac Lane]]

* {#Heunen} [[Chris Heunen]], _Categories and Quantum Informatics: Coherence_, (2018), ([url](https://www.inf.ed.ac.uk/teaching/courses/cqi/3bonus-coherence.pdf))

[[!redirects strictification versus coherence]]
[[!redirects coherence versus strictification]]
[[!redirects strictification and coherence]]