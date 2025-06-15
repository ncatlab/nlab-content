
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[dependent type theory]], a _resizing axiom_ or _resizing rule_ is an [[inference rule]] which allows, under suitable conditions, to find a [[type]] that is in some [[type universe]] $U_2$  also in a smaller [[type universe]] $U_1$.

## Examples

* [[propositional resizing]] (resizing all [[mere propositions]])

* [[propositional impredicativity]] (resizing the [[type of small propositions]])

* [[impredicative polymorphism]] (resizing universe-indexed [[dependent product types]] of universe-indexed [[type families]]). 

* [[type theoretic axiom of replacement]] (resizing [[images]] of [[functions]] from a [[small type]] to a [[locally small type]])

* [[axiom of fullness]] (resizing all types of small [[entire relations]])

## Axioms which imply resizing axioms

There are various axioms which imply resizing axioms:

* [[univalence]] implies resizing the [[identity types]] of all [[universes]] by the equivalence with [[equivalence types]], since [[function types]] are small

* [[pushout types]] imply the [[type theoretic axiom of replacement]] for all universes (see theorem 4.6 of [Rijke 2017](#Rijke17)). The same goes for [[coequalizer types]] or [[cofiber types]], since in the presence of [[sum types]] or the [[type of booleans]], one can define pushouts from coequalizers or cofibers. 

* [[excluded middle]] implies [[propositional impredicativity]] and [[propositional resizing]] for all universes

* the [[axiom of choice]] implies [[excluded middle]] and thus [[propositional impredicativity]] and [[propositional resizing]] for all universes

* There are a number of axioms which imply resizing axioms for [[Dedekind cuts]] of universes and the type of small [[Dedekind real numbers]] of universes, since they imply the [[Dedekind real numbers]], which are usually large, are equivalent to the [[Cauchy real numbers]], which are constructible and small. These include:

  * [[countable choice]] 

  * the [[weak countable choice]] axiom $\mathrm{AC}_{\mathbb{N},2}$, 

  * [[analytic LPO]] for [[Dedekind real numbers]]. 

## Related concepts

* [[type universe]]

* [[universe hierarchy]]

## References

* [[Vladimir Voevodsky]], _Resizing Rules - their use and semantic justification_, 2011 ([pdf](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/2011_Bergen.pdf))

* [[Tom de Jong]], [[Martín Hötzel Escardó]], _Domain Theory in Constructive and Predicative Univalent Foundations_, in: _29th EACSL Annual Conference on Computer Science Logic_, [CSL 2021](https://csl2021.fmf.uni-lj.si/), LIPIcs proceedings 183, 2021 ([doi:10.4230/LIPIcs.CSL.2021.28](https://doi.org/10.4230/LIPIcs.CSL.2021.28), [arXiv:2008.01422](https://arxiv.org/abs/2008.01422))

* {#Rijke17} [[Egbert Rijke]], *The join construction*, 26 Jan 2017, ([arXiv:1701.07538](https://arxiv.org/abs/1701.07538))

[[!redirects resizing axiom]]
[[!redirects resizing axioms]]

[[!redirects axiom of resizing]]
[[!redirects axioms of resizing]]

[[!redirects resizing axiom schema]]
[[!redirects resizing axiom schemas]]
[[!redirects resizing axiom schemata]]

[[!redirects axiom schema of resizing]]
[[!redirects axiom schemas of resizing]]
[[!redirects axiom schemata of resizing]]

[[!redirects resizing rule]]
[[!redirects resizing rules]]
