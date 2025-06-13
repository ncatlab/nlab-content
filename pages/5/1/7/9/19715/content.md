
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

Propositional resizing can be defined for individual type universes ([Gylterud, Stenholm, & Veltri 2020](#GSV20)) or for the type theory as a whole ([[HoTT Book]]).

A [[type universe]] $U$ satisfies **propositional resizing** if every proposition $P$ in the [[dependent type theory]] is [[essentially small type|essentially $U$-small]]. 

In dependent type theory where for every type $A$, there is a [[type universe]] $U$ such that $A$ is essentially $U$-small, one can define propositional resizing for the entire type theory: a [[type universe|universe]] $\mathcal{V}$ satisfies $\mathcal{U}$-propositional resizing if every $\mathcal{V}$ proposition is essentially $\mathcal{U}$-small. Propositional resizing is then the axiom that all universes $\mathcal{V}$ satisfy $\mathcal{U}$ resizing for all universes $\mathcal{U}$.

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

* [[Tom de Jong]], [[Martín Hötzel Escardó]], _Domain Theory in Constructive and Predicative Univalent Foundations_, in: _29th EACSL Annual Conference on Computer Science Logic_, [CSL 2021](https://csl2021.fmf.uni-lj.si/), LIPIcs proceedings 183, 2021 ([doi:10.4230/LIPIcs.CSL.2021.28](https://doi.org/10.4230/LIPIcs.CSL.2021.28), [arXiv:2008.01422](https://arxiv.org/abs/2008.01422))

* {#GSV20} [[Håkon Robbestad Gylterud]], [[Elisabeth Stenholm]], [[Niccolò Veltri]], *Terminal Coalgebras and Non-wellfounded Sets in Homotopy Type Theory* &lbrack;[arXiv:2001.06696](https://arxiv.org/abs/2001.06696)&rbrack;

* [Formalization](https://unimath.github.io/agda-unimath/foundation.propositional-resizing.html) in [[unimath|Agda Unimath]].

[[!redirects propositional resizing]]
[[!redirects weak propositional resizing]]
[[!redirects strict propositional resizing]]

[[!redirects axiom of propositional resizing]]
[[!redirects axiom schema of propositional resizing]]

[[!redirects propositional resizing axiom]]
[[!redirects propositional resizing axiom schema]]