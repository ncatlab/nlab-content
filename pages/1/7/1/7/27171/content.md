
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

A [[type universe]] $U$ has **impredicative polymorphism** if [[dependent product types]] of $U$-indexed families of $U$-small types are themselves $U$-small. 

Like all other conditions on [[Tarski universes]], there is an orthogonal axis for which impredicativity might vary: weak or strict impredicativity, which has to do with whether one uses an [[equivalence of types]] or [[judgmental equality]] to define small types. 

* A Tarski universe $(U, T)$ has **weak impredicative polymorphism** or is **weakly impredicative** if for all functions $P:U \to U$ the [[dependent product type]] $\prod_{X:U} P(X)$ is [[essentially small type|essentially $U$-small]]

$$\prod_{P:U \to U} \sum_{\forall_P:U} T(\forall_P) \simeq \prod_{X:U} T(P(X))$$

* A Tarski universe $(U, T)$ has **strict impredicative polymorphism** or is **strictly impredicative** if for all functions $P:U \to U$ the [[dependent product type]] $\prod_{X:U} P(X)$ is [[small type|$U$-small]]

$$\frac{\Gamma, X:U \vdash P(X):U}{\Gamma \vdash \forall X:U.P(X):U} \qquad \frac{\Gamma, X:U \vdash P(X):U}{\Gamma \vdash T(\forall X:U.P(X)) \equiv \prod_{X:U} T(P(X)) \; \mathrm{type}}$$

## Examples

* The base universe $\mathrm{Set}$ historically had impredicative polymorphism in [[Coq]], according to [Pédrot 2022](#Pédrot22). 

## Related concepts

* [[polymorphism]]

* [[internal parametricity]]

* [[impredicative universe]] 

* [[impredicative dependent type theory]]

* [[propositional resizing]]

## References

* {#Pédrot22} Pierre-Marie Pédrot, *Why not have `Prop : Set` in Coq?*, Proof Assistant StackExchange, 27 June 2022. ([web](https://proofassistants.stackexchange.com/questions/1551/why-not-have-prop-set-in-coq))

* *Mere propositions and Consistency with Impredicativity, Excluded Middle and Large Elimination*, Proof Assistant StackExchange ([web](https://proofassistants.stackexchange.com/questions/2456/mere-propositions-and-consistency-with-impredicativity-excluded-middle-and-larg))

[[!redirects impredicative polymorphism]]
[[!redirects weak impredicative polymorphism]]
[[!redirects strict impredicative polymorphism]]

[[!redirects impredicativly polymorphic]]
[[!redirects weakly impredicativly polymorphic]]
[[!redirects strictly impredicativly polymorphic]]