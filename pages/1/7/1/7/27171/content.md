
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

## Idea

Given a type family indexed by [[type variables]], impredicative polymorphism states that we can construct the [[dependent function type]] and dependent functions for said type family. If types are represented by elements of a [[type universe]] $U$, then impredicative polymorphism also says that such a type is a $U$-[[small type]]. 

Impredicative polymorphism is important for defining axioms such as [[UIP]], [[excluded middle]], the [[type theoretic axiom of replacement|axiom of replacement]] and the [[axiom of choice]] as actual axioms rather than unjustified rules. Axioms involving type families can be represented using an auxiliary type and a function to the index type, where the type family itself is represented by the [[fiber types]] of the function. 

Impredicative polymorphism is also important for defining impredicative structures in [[dependent type theory]], such as [[frames]], [[Cauchy complete spaces]], [[Grothendieck topoi]], the [[type of all propositions]], etc.

## Definition

### For universes

A [[type universe]] $U$ has **impredicative polymorphism**  or is **impredicative** if [[dependent product types]] of $U$-indexed families of $U$-small types are themselves $U$-small. 

For [[Russell universes]], this is given by the [[inference rule]]

$$\frac{\Gamma, X:U \vdash P(X):U}{\Gamma \vdash \prod_{X:U} P(X):U}$$

The situation is a little bit more complicated for [[Tarski universes]]. Like all other conditions on [[Tarski universes]], there is an orthogonal axis for which impredicativity might vary: weak or strict impredicativity, which has to do with whether one uses an [[equivalence of types]] or [[judgmental equality]] to define small types. 

* A Tarski universe $(U, T)$ has **weak impredicative polymorphism** or is **weakly impredicative** if for all functions $P:U \to U$ the [[dependent product type]] $\prod_{X:U} P(X)$ is [[essentially small type|essentially $U$-small]]

$$\prod_{P:U \to U} \sum_{\forall_P:U} T(\forall_P) \simeq \prod_{X:U} T(P(X))$$

* A Tarski universe $(U, T)$ has **strict impredicative polymorphism** or is **strictly impredicative** if for all functions $P:U \to U$ the [[dependent product type]] $\prod_{X:U} P(X)$ is [[small type|$U$-small]]

$$\frac{\Gamma, X:U \vdash P(X):U}{\Gamma \vdash \forall X:U.P(X):U} \qquad \frac{\Gamma, X:U \vdash P(X):U}{\Gamma \vdash T(\forall X:U.P(X)) \equiv \prod_{X:U} T(P(X)) \; \mathrm{type}}$$

### For dependent type theories

In the presentation of dependent type theory using a hierarchy of universes, **impredicative polymorphism** is a resizing axiom which says that for all [[endofunctions]] $P:U_0 \to U_0$ on the first [[type universe]] $U_0$, the [[dependent product type]] $\prod_{X:U_0} P(X)$ is ([[essentially small type|essentially]]) [[small type|$U_0$-small]]. 

In [[dependent type theory with type variables]], presented without universes but with a single type judgment, while there is no universe $U_0$ to quantify over for the dependent product type, using the type variable we can add an untyped version of the dependent product type $\prod_{X \; \mathrm{type}} P(X)$ or $\Pi X.P(X)$ to the type theory for **impredicative polymorphism**. This type is similar to [[universal quantification]] $\forall X.P(X)$ in untyped [[first-order logic]], and it plays the same role in this presentation of dependent type theory that the type $\prod_{X:U_0} P(X)$ does for the other presentation of dependnet type theory. The rules for $\prod_{X \; \mathrm{type}} P(X)$ are as follows:

Formation rule:

$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type}}{\Gamma \vdash \prod_{X \; \mathrm{type}} P(X) \; \mathrm{type}}$$

Introduction rule:

$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma, X \; \mathrm{type} \vdash p(X):P(x)}{\Gamma \vdash \lambda X.p(X):\prod_{X \; \mathrm{type}} P(X)}$$

Elimination rule:

$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma \vdash p:\prod_{X \; \mathrm{type}} P(X)}{\Gamma, A \; \mathrm{type} \vdash \mathrm{ev}(p, X):P(X)}$$

Computation rules:

* Judgmental computation rule:
$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma, X \; \mathrm{type} \vdash p(X):P(x)}{\Gamma, X \; \mathrm{type} \vdash \mathrm{ev}(\lambda X.p(X), X) \equiv p(X):P(X)}$$
* Typal computation rule:
$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma, X \; \mathrm{type} \vdash p(X):P(x)}{\Gamma, X \; \mathrm{type} \vdash \beta_\Pi^{P, p}(X):\mathrm{ev}(\lambda X.p(X), X) =_{P(X)} p(X)}$$

Uniqueness rules:

* Judgmental uniqueness rule:
$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma \vdash p:\prod_{X \; \mathrm{type}} P(X)}{\Gamma \vdash \lambda X.\mathrm{ev}(p, X) \equiv p:\prod_{X \; \mathrm{type}} P(x)}$$
* Typal uniqueness rule:
$$\frac{\Gamma, X \; \mathrm{type} \vdash P(X) \; \mathrm{type} \quad \Gamma \vdash p:\prod_{X \; \mathrm{type}} P(X)}{\Gamma \vdash \eta_\Pi^P(p):\lambda X.\mathrm{ev}(p, X) =_{\prod_{X \; \mathrm{type}} P(x)} p}$$

## Examples of universes with impredicative polymorphism

* The base universe $\mathrm{Set}$ historically had impredicative polymorphism in [[Coq]], according to [Pédrot 2022](#Pédrot22). 

* In [[dependent type theory]] defined using a single [[type]] [[judgment]], the [[universe of all propositions]] is a type universe with impredicative polymorphism if and only if [[weak function extensionality]] holds.  

* More generally, let $\Omega$ be a [[universe of propositions]], and assume [[weak function extensionality]] holds. Then $\Omega$ has impredicative polymorphism if and only if it is closed under [[dependent product types]] of predicates in $\Omega$; i.e. $\Omega$ is an [[inflattice]]. 

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

[[!redirects impredicatively polymorphic universe]]
[[!redirects impredicatively polymorphic universes]]
[[!redirects weakly impredicatively polymorphic universe]]
[[!redirects weakly impredicatively polymorphic universes]]
[[!redirects strictly impredicatively polymorphic universe]]
[[!redirects strictly impredicatively polymorphic universes]]

[[!redirects dependent type theory with impredicative polymorphism]]
[[!redirects dependent type theories with impredicative polymorphism]]

[[!redirects impredicatively polymorphic dependent type theory]]
[[!redirects impredicatively polymorphic dependent type theories]]