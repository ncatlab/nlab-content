
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

One paradigm of [[dependent type theory]] is **propositions as some types**, in which propositions are identified with particular types, but not all types are regarded as propositions. Generally, the propositions are the "types with at most one [[term]]", i.e. the [[h-propositions]] or [[subsingletons]], and can thus also be called **propositions as subsingletons**. This contrasts with the [[propositions as types]] paradigm, where all types are regarded as propositions. 

Propositions as some types is the paradigm usually used in the [[internal logic]] of [[categories]] such as [[toposes]]. In this case, the type-theoretic operations on types either restrict to the propositions to give logical operations (for [[conjunction]], [[implication]], and the [[universal quantifier]]), or have to be "reflected" therein (for [[disjunction]] and the [[existential quantifier]]). The reflector operation is called a [[bracket type]]. The [[law of double negation]] in [[classical mathematics]] similarly has to be restricted to propositions, unlike the case in the [[propositions as types]] paradigm - where the law of double negation is represented by a [[global choice operator]]. 

Furthermore, most structures traditionally involving [[predicates]] or [[relations]] are defined as proposition-valued type families in this restricted sense, where each type of the type family has at most one term. For instance, [[setoids]] or [[Bishop sets]] are usually defined to have an [[equivalence relation]] in the propositions as some types paradigm, rather than a [[pseudo-equivalence relation]] as typical in the [[propositions as types]] paradigm. 

Dependent type theory support various [[foundations of mathematics]] via the [[propositions as some types]] interpretation of [[dependent type theory]]. 

* One can add a [[cumulative hierarchy]] to the dependent type theory and work entirely in the cumulative hierarchy for [[material set theory]]

* One can add a [[category of sets]] to the dependent type theory and work entirely in the category of sets for [[structural set theory]]

* One can add a [[type universe]] satisfying certain [[axioms]] and [[axiom schemata]], such as [[universe extensionality]], closure under identity types, closure under dependent sum types, closure under dependent product types, [[propositional resizing]], [[axiom of replacement|replacement]], [[axiom of infinity|infinity]], and [[axiom of choice|choice]], to the dependent type theory and work entirely in the universe for [[univalent type theory]] or [[univalent foundations]]. Adding internal universe types as [[small]] [[object classifiers]] as well as all [[higher inductive types|higher inductive]] and [[coinductive types]] to the universe results in [[homotopy type theory]]. 

* One can add a [[Russell type of all propositions]] and a [[natural numbers type]] and work in the dependent type theory itself for [[higher-order logic]].

On the other hand, if one only has a [[Tarski type of all propositions]], then propositions and subsingletons are not the same thing, and one is following the philosophy that **propositions are codes for subsingletons**, similar to [[set theory]] with the [[axiom schema of separation]]. 

## Related concepts

[[!include notions of type]]

[[!redirects propositions as some types]]
[[!redirects propositions as subsingletons]]
[[!redirects propositions as (-1)-truncated types]]