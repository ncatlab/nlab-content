
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

One paradigm of [[dependent type theory]] is **propositions as some types**, in which propositions are identified with particular types, but not all types are regarded as propositions. Generally, the propositions are the "types with at most one [[term]]", i.e. the [[h-propositions]] or [[subsingletons]], and the paradigm can thus also be called **propositions as subsingletons**. This contrasts with the [[propositions as types]] paradigm, where all types are regarded as propositions. 

Propositions as some types is the paradigm usually used in the [[internal logic]] of [[categories]] such as [[toposes]]. In this case, the type-theoretic operations on types either restrict to the propositions to give logical operations (for [[conjunction]], [[implication]], and the [[universal quantifier]]), or have to be "reflected" therein (for [[disjunction]] and the [[existential quantifier]]). The reflector operation is called a [[bracket type]]. The [[law of excluded middle]] and the [[law of double negation]] in [[classical mathematics]] similarly has to be restricted to propositions, unlike the case in the [[propositions as types]] paradigm - where the law of excluded middle and the law of double negation are both represented by a [[global choice operator]]. 

Furthermore, most structures traditionally involving [[predicates]] or [[relations]] are defined as proposition-valued type families in this restricted sense, where each type of the type family has at most one term. 

* For instance, [[setoids]] or [[Bishop sets]] are usually defined to have an [[equivalence relation]] in the propositions as some types paradigm, rather than a [[pseudo-equivalence relation]] as typical in the [[propositions as types]] paradigm. 

* Another example is the notion of [[propositional equality]], which is typically used in the sense of a [[h-proposition]] valued [[identity type]], rather than as a synonym of [[typal equality]] as typical in the [[propositions as types]] paradigm. 

Dependent type theory support various [[foundations of mathematics]] via the [[propositions as some types]] interpretation of [[dependent type theory]]. 

* One can add a [[cumulative hierarchy]] to the dependent type theory and work entirely in the cumulative hierarchy for [[material set theory]]

* One can add a [[category of sets]] to the dependent type theory and work entirely in the category of sets for [[structural set theory]]

* One can add a [[type universe]] satisfying certain [[axioms]] and [[axiom schemata]], such as [[universe extensionality]], closure under identity types, closure under dependent sum types, closure under dependent product types, [[propositional resizing]], [[axiom of replacement|replacement]], [[axiom of infinity|infinity]], and [[axiom of choice|choice]], to the dependent type theory and work entirely in the universe for [[univalent type theory]] or [[univalent foundations]]. Adding internal universe types as [[small]] [[object classifiers]] as well as all [[higher inductive types|higher inductive]] and [[coinductive types]] to the universe results in [[homotopy type theory]]. 

* One can add a [[Russell type of all propositions]] and a [[natural numbers type]] and work in the dependent type theory itself for [[higher-order logic]].

On the other hand, if one only has a [[Coquand universe|Coquand]]/[[Tarski type of all propositions]] for [[higher-order logic]], then propositions and subsingletons are not the same thing, and one is following the philosophy of **propositions as codes for subsingletons**, similar to [[set theory]] with the [[axiom schema of separation]]. 

### Propositions as subsingletons in set theory

There is an analogue of the "propositions as some types" in [[set theory]], called **propositions as subsingletons**. Instead of working in the external logic, one interprets certain set-theoretic operations as representing the predicate logic:

* Any [[subsingleton]] represents a proposition

* The [[empty set]] represents [[falsehood]]

* Any [[singleton]] represents [[truth]]

* The binary cartesian product of two subsingletons is [[conjunction]] of propositions

* The function set between two subsingletons is [[implication]] of propositions

* The function set from a subsingleton to the empty set is [[negation]] of propositions

* Given a family of subsingletons, the indexed [[cartesian product]] of the family of subsingletons is [[universal quantification]]

* One can turn any set into a subsingleton by taking the [[image]] of the unique function into a [[singleton]]. This is useful for constructing the internal disjunction and existential quantifier:

* The image of the unique function from the [[disjoint union]] of two subsingletons to any singleton is the [[disjunction]] of propositions

* The image of the unique function from the indexed [[disjoint union]] of a family of subsingletons to any singleton is the [[existential quantifier]]

* The [[propositional equality]] is given by the [[diagonal subset]]

Compare with [[propositions as sets]], which is the [[BHK interpretation]] of the internal logic of a set theory via set-theoretic operations on sets.

## Related concepts

[[!include notions of type]]

[[!redirects propositions as some types]]
[[!redirects propositions as subsingletons]]
[[!redirects propositions as (-1)-truncated types]]
[[!redirects propositions as codes for subsingletons]]
[[!redirects propositions as codes for (-1)-truncated types]]