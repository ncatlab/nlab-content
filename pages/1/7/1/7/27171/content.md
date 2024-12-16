
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

A [[type universe]] $U$ has **impredicative polymorphism**  or is **impredicative** if [[dependent product types]] of $U$-indexed families of $U$-small types are themselves $U$-small. 

For [[Russell universes]], this is given by the [[inference rule]]

$$\frac{\Gamma, X:U \vdash P(X):U}{\Gamma \vdash \prod_{X:U} P(X):U}$$

The situation is a little bit more complicated for [[Tarski universes]]. Like all other conditions on [[Tarski universes]], there is an orthogonal axis for which impredicativity might vary: weak or strict impredicativity, which has to do with whether one uses an [[equivalence of types]] or [[judgmental equality]] to define small types. 

* A Tarski universe $(U, T)$ has **weak impredicative polymorphism** or is **weakly impredicative** if for all functions $P:U \to U$ the [[dependent product type]] $\prod_{X:U} P(X)$ is [[essentially small type|essentially $U$-small]]

$$\prod_{P:U \to U} \sum_{\forall_P:U} T(\forall_P) \simeq \prod_{X:U} T(P(X))$$

* A Tarski universe $(U, T)$ has **strict impredicative polymorphism** or is **strictly impredicative** if for all functions $P:U \to U$ the [[dependent product type]] $\prod_{X:U} P(X)$ is [[small type|$U$-small]]

$$\frac{\Gamma, X:U \vdash P(X):U}{\Gamma \vdash \forall X:U.P(X):U} \qquad \frac{\Gamma, X:U \vdash P(X):U}{\Gamma \vdash T(\forall X:U.P(X)) \equiv \prod_{X:U} T(P(X)) \; \mathrm{type}}$$

## Examples

* The base universe $\mathrm{Set}$ historically had impredicative polymorphism in [[Coq]], according to [Pédrot 2022](#Pédrot22). 

* In [[dependent type theory]] defined using a single [[type]] [[judgment]], the [[universe of all propositions]] is a type universe with impredicative polymorphism if and only if [[weak function extensionality]] holds.  

* More generally, let $\Omega$ be a [[universe of propositions]], and assume [[weak function extensionality]] holds. Then $\Omega$ has impredicative polymorphism if and only if it is closed under [[dependent product types]] of predicates in $\Omega$; i.e. $\Omega$ is an [[inflattice]]. 

## Properties

Impredicative polymorphism of any universe $U$ with a [[type]] which is not a [[mere proposition]] is inconsistent with [[propositional resizing]] for a universe $U$. 

## Related concepts

* [[polymorphism]]

* [[internal parametricity]]

* [[impredicative universe]] 

* [[impredicative dependent type theory]]

* [[propositional resizing]]

* [[taboo]]

* [[type of all propositions]]

* [[weak function extensionality]]

* [[dependent type theory with type variables]]

## References

* [[Andrew Pitts]], *Nontrivial Power Types can't be Subtypes of Polymorphic Types* ([pdf](https://www.cl.cam.ac.uk/~amp12/papers/nontpt/nontpt.pdf))

* [[Taichi Uemura]], *Cubical Assemblies, a Univalent and Impredicative Universe and a Failure of Propositional Resizing*, in 24th International Conference on Types for Proofs and Programs (TYPES 2018). Leibniz International Proceedings in Informatics (LIPIcs), Volume 130, pp. 7:1-7:20, Schloss Dagstuhl – Leibniz-Zentrum für Informatik (2019) ([doi:10.4230/LIPIcs.TYPES.2018.7](https://doi.org/10.4230/LIPIcs.TYPES.2018.7), [arXiv:1803.06649](https://arxiv.org/abs/1803.06649))

* *Dependent Type Theory vs Polymorphic Type Theory*, Category Theory Zulip ([web](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/Dependent.20Type.20Theory.20vs.20Polymorphic.20Type.20Theory))

* {#Pédrot22} Pierre-Marie Pédrot, *Why not have `Prop : Set` in Coq?*, Proof Assistant StackExchange, 27 June 2022. ([web](https://proofassistants.stackexchange.com/questions/1551/why-not-have-prop-set-in-coq))

* *Mere propositions and Consistency with Impredicativity, Excluded Middle and Large Elimination*, Proof Assistant StackExchange ([web](https://proofassistants.stackexchange.com/questions/2456/mere-propositions-and-consistency-with-impredicativity-excluded-middle-and-larg))

[[!redirects impredicative polymorphism]]
[[!redirects weak impredicative polymorphism]]
[[!redirects strict impredicative polymorphism]]

[[!redirects impredicatively polymorphic]]
[[!redirects weakly impredicatively polymorphic]]
[[!redirects strictly impredicatively polymorphic]]