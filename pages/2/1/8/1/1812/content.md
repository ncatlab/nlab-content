
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **cosmos** is a "good place in which to do category theory," including both ordinary [[category theory]] as well as [[enriched category]] theory.

The word is chosen by analogy with [[topos]] which can be regarded as "a good place to do set theory," but there are notable differences between the two situations; a more direct [[vertical categorification|categorification]] of a topos is, unsurprisingly, a [[2-topos]].  In contrast, cosmoi also include [[enriched category]] theory, while toposes do not allow non-[[cartesian monoidal category|cartesian]] enrichment.

There are a number of different, inequivalent, definitions of "cosmos" in the literature.

## B&#233;nabou's definition

Jean B&#233;nabou\'s original definition was that a **cosmos** $V$ is a [[complete category|complete]] and [[cocomplete category|cocomplete]] [[closed monoidal category|closed]] [[symmetric monoidal category]].  This is an ideal situation for studying categories [[enriched category|enriched]] over $V$.

## Street's "fibrational cosmoi"

[[Ross Street]] has taken a different tack, defining a "cosmos" to be the collection of (enriched) categories and relevant structure for doing category theory, rather than the "base" category $V$ over which the enrichment occurs.

In his paper "Elementary cosmoi," Street defined a **(fibrational) cosmos** to be a 2-category in which internal [[Grothendieck fibrations|fibrations]] are well-behaved and representable by a structure of "presheaf objects" (later realized to be a special sort of [[Yoneda structure]]).  Note that while this includes $Cat$, it does *not* include $V$-$Cat$ for non-cartesian $V$, since internal fibrations are poorly behaved there.

## Street's second definition

In his paper "Cauchy characterization of enriched categories," Street instead defined a "cosmos" to be a [[2-category]] that behaves like the 2-category $V$-$Mod$ of enriched categories and [[profunctors]].  The precise definition: a cosmos is a 2-category (or [[bicategory]]) such that:
* Small ([[2-limit|weak, or bi-]]) [[coproduct]]s exist.
* Each [[monad]] admits a [[Kleisli construction]] (analogous to the [[exact category|exactness]] of a topos).
* It is locally small-[[cocomplete category|cocomplete]], i.e. its hom-categories have small colimits that are preserved by composition on each side.
* There exists a small "Cauchy generator".

These hypotheses imply that it is equivalent to the bicategory of categories and [[profunctors]] [[enriched category|enriched]] over some "base" *bicategory*.  (Note the generalization from enrichment over a monoidal category to enrichment over a bicategory.)

Defined in this way, cosmoi are closed under [[opposite category|dualization]], parametrization and [[localization]], suitably defined.
