


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



\tableofcontents

## Definition

An object $P$ of a [[category]] $C$ is a __compact projective object__
if its [[corepresentable functor]] $Hom(P,-)\colon C\to Set$ [[preserved colimit|preserves]] all [[small colimit|small]] [[sifted colimits]].

Equivalently, it is an [[object]] that is 

1. a [[compact object]] 

   ($Hom(P,-)$ preserves all small [[filtered colimits]]),

1. a [[projective object]] 

   ($Hom(P,-)$ preserves [[epimorphisms]], which follows from its preservation of [[coequalizers]]).


## Examples

In the category of [[algebra over an algebraic theory|algebras over]] an [[algebraic theory]],
compact projective objects are [[retracts]] of [[free construction|free]] algebras.

Conversely, if a [[locally small category]] has enough compact projective objects
(meaning that there is a set of compact projective objects that
generates it under small [[colimits]] and reflects isomorphisms),
then this category is equivalent to the category of algebras over an [[algebraic theory]].
Such a category is also known as a [[locally strongly finitely presentable category]]

## Related concepts

* [[sifted colimit]]

* [[algebraic theory]]

* [[locally strongly finitely presentable category]]

[[!redirects compact projective objects]]