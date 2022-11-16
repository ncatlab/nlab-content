
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
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A geometric hyperdoctrine is a [[hyperdoctrine]] with respect to [[lattices]] that are [[frames]].

## Definition

Let $C$ be a [[category]] with [[finite limits]]. A **[[geometric logic|geometric]] [[hyperdoctrine]]** over $C$ is a [[functor]]

$$
  P : C^{op} \to Frm
$$

from the [[opposite category]] of $C$ to the category of [[frames]], such that for every [[morphism]] $f : A \to B$ in $C$, the functor $P(A) \to P(B)$ has a [[left adjoint]] $\exists_f$ satisfying

1. [[Frobenius reciprocity]];

1. [[Beck-Chevalley condition]].

## Examples 

Let $OLoc$ be the [[category]] of [[overt locales]], and let $Frm$ be the [[category]] of [[frames]]. The [[functor]] $\mathcal{O}:OLoc^\op \to Frm$ that takes an [[overt locale]] to its [[frame of opens]] is a geometric hyperdoctrine. 

Let $Set$ be the [[category of sets]], defined as a [[Grothendieck topos]] on the [[singleton]], and let $Frm$ be the [[category]] of [[frames]]. The [[subobject poset]] [[functor]] $\mathrm{Sub}:Set^\op \to Frm$ that takes a [[set]] to its [[subobject poset]] is a geometric hyperdoctrine. 

This could be generalized to any [[geometric category]] $C$: the [[subobject poset]] [[functor]] $\mathrm{Sub}:C^\op \to Frm$ that takes an [[object]] of $C$ to its [[subobject poset]] is a geometric hyperdoctrine. 

## See also

[[!include categories and logic - table]]

## References

* Graham Manuell, *Uniform locales and their constructive aspects*, ([arXiv:2106.00678](https://arxiv.org/abs/2106.00678))