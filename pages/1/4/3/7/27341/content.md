
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
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

A *$\sigma$-frame of propositions* is a $\sigma$-[[subframe]] $\Sigma \subseteq \Omega$ of the [[frame of truth values]] $\Omega$. 

However, in [[dependent type theory]], many times we do not have access to the [[frame of truth values]] $\Omega$ - which is the [[type of all propositions]] $\mathrm{Prop}$ in [[dependent type theory]] - because, for example, we want to have [[canonicity]] in the dependent type theory, which [[propositional resizing]] violates. 

Thus, it is beneficial to be able to define a $\sigma$-frame of propositions $\Sigma$ without the need for a [[type of all propositions]] $\mathrm{Prop}$, because it will allow us to define lower, upper, and two-sided $\Sigma$-[[Dedekind cuts]] as well as $\Sigma$-[[admissible Archimedean ordered fields]], key concepts in [[predicative mathematics|predicative]] [[constructive real analysis]]. 

## Definition

A **$\sigma$-frame of propositions** consists of 

* a type $\Sigma$ 

* a type family $(T(x))_{x:\Sigma}$ satisfying the [[univalence axiom]] such that each $T(x)$ is a [[subsingleton]] or [[h-proposition]], 

* an element $\top:\Sigma$ such that $T(\top)$ is an [[singleton]] or [[contractible type]]

* a function $(-)\wedge(-):\Sigma \times \Sigma \to \Sigma$ such that for all $P:\Sigma$ and $Q:\Sigma$, $T(P \wedge Q) \simeq (T(P) \times T(Q))$

* an element $\bot:\Sigma$ such that $T(\bot) \simeq \emptyset$

* a function $(-)\vee(-):\Sigma \times \Sigma \to \Sigma$ such that for all $P:\Sigma$ and $Q:\Sigma$, $T(P \vee Q) \simeq (T(P) \vee T(Q))$

* a function $V:(\mathbb{N} \to \Sigma) \to \Sigma$ such that for all sequences $f:\mathbb{N} \to \Sigma$, $T(V(f)) \simeq \exists n:\mathbb{N}.T(f(n))$

## Examples

* The [[initial object|initial]] [[sigma-frame|$\sigma$-frame]] is the initial $\sigma$-frame of propositions. 

* The [[type of all propositions]], if it exists, is the [[terminal object|terminal]] $\sigma$-frame of propositions. 

* Assuming the [[limited principle of omniscience]], the [[type of booleans]] is a $\sigma$-frame of propositions. 

## Related concepts

* [[sigma-frame]]

* [[type of propositions]]

* [[dominance]]

* [[Dedekind cut]]

* [[admissible Archimedean ordered field]]

[[!redirects sigma-frame of propositions]]
[[!redirects sigma-frames of propositions]]
