
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

_Propositional resizing_ is an [[axiom]] often assumed in [[homotopy type theory]] that states that all [[mere propositions]] are [[essentially small type|small]]. This is a form of [[impredicativity]] since it implies [[propositional impredicativity]] and thus [[power sets]] for successor universes.

Despite that, propositional resizing is a relatively weak axiom, for instance it is implied by the [[law of excluded middle]], which states that the [[small type]] $2$ classifies all propositions. However, it is independent of the other basic axioms of homotopy type theory. 

## Definition

Propositional resizing can be defined for individual type universes ([Gylterud, Stenholm, & Veltri 2020](#GSV20)) or for the type theory as a whole ([[HoTT Book]]).

In dependent type theory where for every type $A$, there is a [[type universe]] $U$ such that $A$ is essentially $U$-small, one can define propositional resizing for the entire type theory: a [[type universe|universe]] $V$ satisfies $U$-propositional resizing if every proposition in $V$ is [[essentially small type|essentially $U$-small]]. Propositional resizing for the entire dependent type theory then is the axiom that all universes $V$ satisfy $U$-resizing for all universes $U$.

If the universe $V$ additionally contains a type classifying all $U$-small types, then the type $\mathrm{Prop}_U$ is a $V$-small type of all $V$-small propositions, making the universe $V$ satisfy [[propositional impredicativity]]. In particular, for a [[natural numbers]]-indexed [[universe hierarchy]] such as those found in the [[HoTT book]] and [[proof assistants]] like [[Lean]], [[Agda]], and [[Rocq]], if propositional resizing holds, then every successor universe $U_{i + 1}$ is a propositionally impredicative universe, while only the base universe $U_0$ is a predicative universe. 

In [[dependent type theory]] with a single type judgment, a [[type universe]] $U$ satisfies propositional resizing if every proposition $P$ in the [[dependent type theory]] is essentially $U$-small. The type $\mathrm{Prop}_U$ is a [[type of all propositions]], making the whole dependent type theory satisfy [[propositional impredicativity]]. 

## See also

* [[resizing axiom]]

* [[essentially small type]]

* [[excluded middle]]

* [[type of all propositions]]

* [[impredicative dependent type theory]]

* [[impredicative universe]]

* [[taboo]]

## References

* Section 3.5 of [[The HoTT Book]]

* [[Taichi Uemura]], *Cubical Assemblies and the Independence of the Propositional Resizing Axiom*, HoTT/UF 2018 [abstract](https://hott-uf.github.io/2018/abstracts/HoTTUF18_paper_6.pdf) [slides](https://hott-uf.github.io/2018/slides/UemuraHoTTUF2018.pdf)

* [[Tom de Jong]], [[Martín Hötzel Escardó]], _Domain Theory in Constructive and Predicative Univalent Foundations_, in: _29th EACSL Annual Conference on Computer Science Logic_, [CSL 2021](https://csl2021.fmf.uni-lj.si/), LIPIcs proceedings 183, 2021 ([doi:10.4230/LIPIcs.CSL.2021.28](https://doi.org/10.4230/LIPIcs.CSL.2021.28), [arXiv:2008.01422](https://arxiv.org/abs/2008.01422))

* {#GSV20} [[Håkon Robbestad Gylterud]], [[Elisabeth Stenholm]], [[Niccolò Veltri]], *Terminal Coalgebras and Non-wellfounded Sets in Homotopy Type Theory* &lbrack;[arXiv:2001.06696](https://arxiv.org/abs/2001.06696)&rbrack;

* [[Benedikt Ahrens]], [[Paige Randall North]], [[Michael Shulman]], [[Dimitris Tsementzis]], *The Univalence Principle* &lbrack;[abs:2102.06275](https://arxiv.org/abs/2102.06275)&rbrack;

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]], Section 2.18 in: *[[Symmetry]]* (2025) $[$[pdf](https://unimath.github.io/SymmetryBook/book.pdf)$]$ 

* [Formalization](https://unimath.github.io/agda-unimath/foundation.propositional-resizing.html) in [[unimath|Agda Unimath]].

[[!redirects propositional resizing]]
[[!redirects weak propositional resizing]]
[[!redirects strict propositional resizing]]

[[!redirects axiom of propositional resizing]]
[[!redirects axiom schema of propositional resizing]]

[[!redirects propositional resizing axiom]]
[[!redirects propositional resizing axiom schema]]