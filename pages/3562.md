
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea

The analog of the notion of [[opposite category]] for [[(∞,1)-categories]].

## Definition

For $C$ an [[(∞,1)-category]] regard it in its incarnation as a [[∞-groupoid]]-[[enriched category]]. Then its opposite is the $(\infty,1)$-category $C^{op}$ with the same objects and with [[hom-object]]s given by

$$
  C^{op}(X,Y) := C(Y,X)
$$

with the obvious composition law.

With $C$ incarnated as a [[quasi-category]], the [[simplicial set]] $C^{op}$ is that obtained by reversing the order of all the face and degeneracy maps. See [[opposite quasi-category]].


## Properties

The operation extends to an [[automorphism|automorphic]] [[(∞,1)-functor]] 

$$
  op : (\infty,1)Cat \to (\infty,1)Cat
$$

from [[(∞,1)Cat]] to itself. Up to equivalence, this is the only nontrivial such automorphism. For more on this see [[(∞,1)Cat]].

## Related concepts

* [[opposite model category]]


[[!redirects opposite quasi-category]]
[[!redirects opposite (∞,1)-category]]