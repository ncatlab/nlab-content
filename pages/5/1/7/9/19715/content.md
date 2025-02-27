
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

_Propositional resizing_ is an [[axiom]] often assumed in [[homotopy type theory]] that states that all [[mere propositions]] are [[essentially small type|small]]. This is a form of [[impredicativity]]: without it, no [[type universe|universes]] can be shown to be closed under forming [[power sets]].

Propositional resizing is a relatively weak axiom, for instance it is implied by the [[law of excluded middle]], which states that the [[small type]] $2$ classifies all propositions. However, it is independent of the other basic axioms of homotopy type theory.

## Definition

A [[type universe|universe]] $\mathcal{V}$ satisfies $\mathcal{U}$-propositional resizing if every $\mathcal{V}$ proposition is essentially $\mathcal{U}$-small. Propositional resizing is then the axiom that all universes $\mathcal{V}$ satisfy $\mathcal{U}$ resizing for all universes $\mathcal{U}$.

If $\mathcal{V}$ contains a type classifying all $\mathcal{U}$ types, then the type $Prop_{\mathcal{U}}$ is a $\mathcal{V}$-small type of all $\mathcal{V}$ propositions, making $\mathcal{V}$ an impredicative universe.


## See also

* [[essentially small type]]

* [[excluded middle]]

* [[type of all propositions]]

* [[impredicative dependent type theory]]

* [[impredicative universe]]


## References

* Section 3.5 of [[The HoTT Book]]

* [[Taichi Uemura]], *Cubical Assemblies and the Independence of the Propositional Resizing Axiom*, HoTT/UF 2018 [abstract](https://hott-uf.github.io/2018/abstracts/HoTTUF18_paper_6.pdf) [slides](https://hott-uf.github.io/2018/slides/UemuraHoTTUF2018.pdf)

* [Formalization](https://unimath.github.io/agda-unimath/foundation.propositional-resizing.html) in [[unimath|Agda Unimath]].

[[!redirects propositional resizing]]
[[!redirects weak propositional resizing]]
[[!redirects strict propositional resizing]]

[[!redirects axiom of propositional resizing]]
[[!redirects axiom schema of propositional resizing]]

[[!redirects propositional resizing axiom]]
[[!redirects propositional resizing axiom schema]]