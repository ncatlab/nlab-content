
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

Given sets $A$ and $B$, the **bijection set** $\mathrm{Bij}(A, B)$ is the set of [[bijections]] between the set $A$ and $B$. In the [[foundations]] of mathematics, the existence of such a set may be taken to follow from the existence of [[power sets]], from the axiom of [[subset collection]], from the existence of [[function sets]], or as an axiom (the __axiom of bijection sets__) in its own right.

## Properties

If the set theory has [[function sets]], then the bijection set between $A$ and $B$ is a [[subset]] of the function set between $A$ and $B$: $\mathrm{Bij}(A, B) \subseteq B^A$. 

The bijection set between $A$ and itself is the [[symmetric group]] on $A$, $\mathrm{Sym}(A) \coloneqq \mathrm{Bij}(A, A)$. 

In the context of the [[axiom of choice]] or stronger axioms such as a [[choice operator]] satisfying the [[axiom schemata of existence]], having [[bijection sets]] implies having [[power sets]] in the foundations, since the axiom of choice implies that for every set $A$, there is a [[bijection]] $\mathcal{P}(A) \cong \mathrm{Sym}(A)$ between the [[power set]] of $A$ and the symmetric group on $A$. Thus, bijection sets are a form of [[impredicativity]] from the point of view of mathematics with the axiom of choice. 

The [[universal property]] of the bijection set states that given a function $X \to \mathrm{Bij}(A, B)$ from a set $X$ to the bijection set between sets $A$ and $B$, there exists a bijection $A \times X \cong B \times X$ in the [[slice category]] $\mathrm{Set}/X$. 

## Generalisations

Thinking of [[Set]] as a [[locally small category]], this is a special case of the [[hom-set]] of the [[core]] of [[Set]]. 

## Related concepts

* [[equivalence type]]

* [[object of isomorphisms]]

* [[symmetric group]]

[[!redirects bijection set]]
[[!redirects bijection sets]]
[[!redirects set of bijections]]
[[!redirects sets of bijections]]

[[!redirects axiom of function sets]]