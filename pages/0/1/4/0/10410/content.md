
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **Dwyer map** is a type of [[cofibration]] in the [[Cat|category of small categories]] designed for the purpose of constructing [[homotopy colimit|homotopy invariant colimits]] with respect to weak homotopy equivalences, i.e. weak equivalences created from [[weak homotopy equivalence|weak homotopy equivalences]] of [[simplicial set|simplicial sets]] by the [[nerve]] functor. It plays an essential role in the construction of the [[Thomason model structure]]. Its definition is inspired by [[neighborhood retract|neighborhood deformation retracts]].

A suitable generalization serves a similar purpose in the homotopy theory of [[relative category|relative categories]], see [Barwick, Kan](#BarwickKan).

## Definition

A functor of small categories $i \colon C \to D$ is a **Dwyer map** if it is a [[sieve]] and factors as a composite of $f \colon C \to C'$ and $j \colon C' \to D$ such that

* $f$ admits a deformation retraction, i.e. a functor $r \colon C' \to C$ such that $r f = \id_C$ together with a natural transformation $h \colon f r \to \id_{C'}$ such that $h f = \id_f$,
* $j$ is a [[cosieve]].

In the original definition $r$ was assumed to be a right adjoint of $f$. The definition above is due to Cisinski who called this more general notion a **pseudo-Dwyer map**. Cisinski's definition is now considered more useful and hence usually called by the simpler name "Dwyer map".

## Properties

+-- {: .num_prop }
###### Proposition

Dwyer maps are closed under:

* coproducts,
* pushouts along arbitrary functors,
* [[transfinite composition]],
* retracts.

Moreover, the [[nerve]] functor preserves pushouts along Dwyer maps and transfinite composites of Dwyer maps up to [[weak homotopy equivalence]].
=--

The proofs can be found in [Thomason, Proposition 4.3, Lemma 4.7](#Thomason) and [Cisinski, Lemme 4](#Cisinski).

+-- {: .num_prop }
###### Proposition

Let $c$ denote the left adjoint of the nerve functor and let $Sd$ denote the [[subdivision|barycentric subdivision]] functor. The composite $c Sd^2$ carries injective simplicial maps to Dwyer maps.
=--

This is [Thomason, Proposition 4.2](#Thomason).

So among the Dwyer maps are all cofibrations in the Thomason model structure. But not all Dwyer maps are Thomason cofibrations -- for example, the unique functor $\emptyset \to C$ is always a Dwyer map, but not every category is Thomason-cofibrant.

## References

*  [[Robert Thomason|R. W. Thomason]], _Cat as a closed model category_,
Cahiers Topologie G&#233;om. Diff&#233;rentielle **21**, no. 3 (1980), pp. 305--324. MR0591388 (82b:18005) <a href="http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1980__21_3_305_0">numdam scan</a> {#Thomason}
* [[Denis-Charles Cisinski]], _Les morphisme de Dwyer ne sont pas stables par r&eacute;tractes_, Cahiers Topologie et G&eacute;om. Diff&eacute;rentielle Cat&eacute;goriques, **40** no. 3 (1999), pp. 227--231. ([Numdam](http://www.numdam.org/item?id=CTGDC_1999__40_3_227_0)) {#Cisinski}
* [[Clark Barwick]], [[Daniel Kan]], _Relative categories: Another model for the homotopy theory of homotopy theories_. Indagationes Mathematicae 23 (2012) pp. 42&#8211;68. {#BarwickKan}