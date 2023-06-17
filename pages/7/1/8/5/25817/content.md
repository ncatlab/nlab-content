
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

One paradigm of [[dependent type theory]] is **propositions as some types**, in which propositions are identified with particular types, but not all types are regarded as propositions. Generally, the propositions are the "types with at most one [[term]]", i.e. the [[h-propositions]]. This contrasts with the [[propositions as types]] paradigm, where all types are regarded as propositions. 

Propositions as some types is the paradigm usually used in the [[internal logic]] of [[categories]] such as [[toposes]], as well as in [[homotopy type theory]]. In this case, the type-theoretic operations on types either restrict to the propositions to give logical operations (for [[conjunction]], [[implication]], and the [[universal quantifier]]), or have to be "reflected" therein (for [[disjunction]] and the [[existential quantifier]]). The reflector operation is called a [[bracket type]]. 

Furthermore, most structures traditionally involving [[predicates]] or [[relations]] are defined as proposition-valued type families in this restricted sense, where each type of the type family has at most one term. For instance, [[setoids]] or [[Bishop sets]] are usually defined to have an [[equivalence relation]] in the propositions as some types paradigm, rather than a [[pseudo-equivalence relation]] as typical in the [[propositions as types]] paradigm. 

## Related concepts

* [[propositions as types]]

[[!redirects propositions as some types]]