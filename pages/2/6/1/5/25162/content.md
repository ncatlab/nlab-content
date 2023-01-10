
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
=--
=--


\tableofcontents

## Definition

Given sets $A$ and $B$, the **injection set** $\mathrm{Inj}(A, B)$ is the set of [[injection]] between the set $A$ and $B$. In the [[foundations]] of mathematics, the existence of such a set may be taken to follow from the existence of [[power sets]], from the axiom of [[subset collection]], from the existence of [[function sets]], or as an axiom (the __axiom of injection sets__) in its own right.

## Properties

If the set theory has [[function sets]], then the injection set between $A$ and $B$ is a [[subset]] of the function set between $A$ and $B$: $\mathrm{Inj}(A, B) \subseteq B^A$. 

The internal [[subset]] [[relation]] is defined as the [[support set|support]] of the injection set between $A$ and $B$: $A \subseteq B \coloneqq [\mathrm{Inj}(A, B)]$. 

The [[universal property]] of the bijection set states that given a function $X \to \mathrm{Inj}(A, B)$ from a set $X$ to the injection set between sets $A$ and $B$, there exists a injection $A \times X \hookrightarrow B \times X$ in the [[slice category]] $\mathrm{Set}/X$. 

## Related concepts

* [[subset]]

* [[embedding type]]

* [[object of monomorphisms]]

* [[function set]], [[bijection set]]

[[!redirects injection set]]
[[!redirects injection sets]]
[[!redirects set of injections]]
[[!redirects sets of injections]]

[[!redirects axiom of injection sets]]