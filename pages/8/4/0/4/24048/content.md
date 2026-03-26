


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

An object $P$ of a [[category]] $C$ is a __compact projective object__, also known as __strongly of finite presentation__,
if its [[corepresentable functor]] $Hom(P,-)\colon C\to Set$ [[preserved colimit|preserves]] all [[small colimit|small]] [[sifted colimits]].

Thus $Hom(P,-)$ preserves all small [[filtered colimits]] (i.e., it is a [[compact object]]) and all [[reflexive coequalizers]]. The converse holds if $C$ is [[finitely cocomplete category|finitely cocomplete]], see [Adamek, Rosicky, Vitale, Theorem 2.1](#AdamekRosickyVitale10).

In the case of cocomplete [[Barr-exact categories]], it is equivalently an [[object]] that is 

1. a [[compact object]] 

   ($Hom(P,-)$ preserves all small [[filtered colimits]]),

1. a [[projective object]] 

   ($Hom(P,-)$ preserves [[regular epimorphisms]], which follows from its preservation of [[coequalizers]]).


## Examples

In the category of [[algebra over an algebraic theory|algebras over]] an [[algebraic theory]],
compact projective objects are [[retracts]] of [[free construction|free]] algebras.

Conversely, if a [[locally small category]] has enough compact projective objects
(meaning that there is a set of compact projective objects that
generates it under small [[colimits]] and reflects isomorphisms),
then this category is equivalent to the category of algebras over an [[algebraic theory]].
Such a category is also known as a [[locally strongly finitely presentable category]]

## References

* Kęstutis Česnavičius and Peter Scholze, *Purity for Flat Cohomology*

* {#AdamekRosickyVitale10} [[Jiri Adamek]], [[Jiri Rosicky]], [[Enrico Vitale]], _What are sifted colimits?_, TAC **23** (2010) pp. 251&#8211;260. ([web](http://www.tac.mta.ca/tac/volumes/23/13/23-13abs.html)) 

## Related concepts

* [[sifted colimit]]

* [[algebraic theory]]

* [[locally strongly finitely presentable category]]

[[!redirects compact projective objects]]