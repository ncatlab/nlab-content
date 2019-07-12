
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[model structure on simplicial sets]] valid in [[constructive mathematics]].

The original [[proofs]] of the existence of the [[classical model structure on simplicial sets]] are based in [[classical mathematics]] as they use the [[principle of excluded middle]] and the [[axiom of choice]], and are hence not valid in [[constructive mathematics]]. This becomes more than a philosophical issue with the relevance of this [[model category]]-[[structure]] in [[homotopy type theory]], where [[internalization]] into the [[type theory]] requires [[constructive mathematics|constructive]] methods for interpreting [[proofs as programs]].

A constructively valid model structure on simplicial sets and coinciding with the [[classical model structure on simplicial sets|classical model structure]] if [[excluded middle]] and [[axiom of choice]] are assumed was found in [Henry 19](#Henry19). Alternative simpler proofs were found in [Gambino-Sattler-Szumiło 19](#GambinoSattlerSzumilo19)

## Properties

### Cofibrant objects

While in the [[classical model structure on simplicial sets]] all [[objects]] ([[simplicial sets]]) are [[cofibrant object|cofibrant]], a [[simplicial set]] is [[cofibrant]] in the constructive model structure
if and only if the inclusion of degenerate $n$-[[simplices]]
into all $n$-simplices is a [[decidable inclusion]] of sets.

Likewise, [[cofibrations]] $A\to B$ are [[simplicial maps]]
such that $A_n\to B_n$ is a [[decidable inclusion]] of sets
and the inclusion of degenerate $n$-simplices as a subset into $B_n\setminus A_n$
is also a [[decidable inclusion]].

Since not all objects are [[cofibrant]], [[proper model category|left properness]] is no longer automatic, but can still be established through nontrivial arguments.

This model structure is also [[right proper]].

See [Henry 19](#Henry19) and [Gambino-Sattler-Szumiło 19](#GambinoSattlerSzumilo19)
for a proof of these claims.

## References

* {#Henry19} [[Simon Henry]], _A constructive account of the Kan-Quillen model structure and of Kan's $Ex^\infty$ functor_ ([arXiv:1905.06160](https://arxiv.org/abs/1905.06160))

* {#GambinoSattlerSzumilo19} [[Nicola Gambino]], [[Christian Sattler]], [[Karol Szumiło]], _The constructive Kan-Quillen model structure: two new proofs_ ([arXiv:1907.05394](https://arxiv.org/abs/1907.05394))

[[!redirects constructive model structures on simplicial sets]]
