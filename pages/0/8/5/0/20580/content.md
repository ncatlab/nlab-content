
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

A [[model structure on simplicial sets]] valid in [[constructive mathematics]]
that reduced to the [[classical model structure on simplicial sets]]
in presence of the [[law of excluded middle]] and [[axiom of choice]].

The original [[proofs]] of the existence of the [[classical model structure on simplicial sets]] are based in [[classical mathematics]] as they use the [[principle of excluded middle]] and the [[axiom of choice]], and are hence not valid in [[constructive mathematics]]. This becomes more than a philosophical issue with the relevance of this [[model category]]-[[structure]] in [[homotopy type theory]], where [[internalization]] into the [[type theory]] requires [[constructive mathematics|constructive]] methods for interpreting [[proofs as programs]].

A constructively valid model structure on simplicial sets and coinciding with the [[classical model structure on simplicial sets|classical model structure]] if [[excluded middle]] and [[axiom of choice]] are assumed was found in [Henry 19](#Henry19). Alternative simpler proofs were found in [Gambino-Sattler-Szumiło 19](#GambinoSattlerSzumilo19)

## Properties

### Fibrations and lifting properties

[[Fibrations]] and [[acyclic fibrations]]
are defined using the [[right lifting property]]
with respect to the usual sets of [[horn inclusions]] and [[boundary inclusions]].
However, the meaning of this definition is more refined:
due to the constructive nature of the [[existential quantifier]],
being an (acyclic) fibration means we have a section
of the map from the set of solutions to lifting problems to the set of
lifting problems.

### Weak equivalences

[[Simplicial weak equivalences]] must also be defined more carefully.

We follow \cite{GambinoSattlerSzumilo19}.
Suppose $f\colon X\to Y$ is a [[simplicial map]].

* If $X$ and $Y$ are [[cofibrant]] [[Kan complexes]], then $f$ is a weak equivalence if it is a [[simplicial homotopy equivalence]];
* If $X$ and $Y$ are [[Kan complexes]], then $f$ is a weak equivalence
if there is a [[simplicial map]] $f'\colon X'\to Y'$ and
[[acyclic fibrations]] with [[cofibrant]] domains $X'\to X$ and $Y'\to Y$ such that $f'$ is a weak equivalence in the previous sense and the square with $f$ and $f'$ commutes;
* If $X$ and $Y$ are [[cofibrant]], then $f$ is a weak equivalence
if for any [[Kan complex]] $K$ the map $Hom(f,K)$ is a weak equivalence in the previous sense (notice that its domain and codomain are [[Kan complexes]]);
* If $X$ and $Y$ are arbitrary, then $f$ is a weak equivalence
if it has a replacement $f'\colon X'\to Y'$ like above, with $f'$ being a weak equivalence in the previous sense.

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

* [[Simon Henry]], _Weak model categories in classical and constructive mathematics_ ([arXiv:1807.02650](https://arxiv.org/abs/1807.02650))

* {#Henry19} [[Simon Henry]], _A constructive account of the Kan-Quillen model structure and of Kan's $Ex^\infty$ functor_ ([arXiv:1905.06160](https://arxiv.org/abs/1905.06160))

* [[Nicola Gambino]], [[Simon Henry]], _Towards a constructive simplicial model of Univalent Foundations_ ([arXiv:1905.06281](https://arxiv.org/abs/1905.06281))

* {#GambinoSattlerSzumilo19} [[Nicola Gambino]], [[Christian Sattler]], [[Karol Szumiło]], _The constructive Kan-Quillen model structure: two new proofs_ ([arXiv:1907.05394](https://arxiv.org/abs/1907.05394))

[[!redirects constructive model structures on simplicial sets]]
