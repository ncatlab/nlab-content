
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

## Definition

### In set theory

Given a [[subobject|sub]]-[[sigma-frame|$\sigma$-frame]] of the [[frame of truth values]] $\Sigma \subseteq \Omega$, an [[Archimedean ordered field]] $F$ is **$\Sigma$-admissible** if and only if there is a function $(-) \lt_\Sigma (-):F \times F \to \Sigma$ such that $(x \lt_\Sigma y) = \top$ if and only if $x \lt y$. 

### In dependent type theory

Let $(\Sigma, T)$ be a [[sigma-frame of propositions|$\sigma$-frame of propositions]]. An [[Archimedean ordered field]] $F$ is **admissible for $\Sigma$** or **$\Sigma$-admissible** if it comes with a function $(-)\lt_\Sigma(-):F \times F \to \Sigma$ such that for all $x:F$ and $y:F$, $T(x \lt_\Sigma y) \simeq (x \lt y)$. 

## Properties

For any given $\sigma$-frame of propositions $(\Sigma, T)$, 

* The [[initial object|initial]] Archimedean ordered field which is admissible for $\Sigma$ is the ordered field of [[rational numbers]]. 

* The [[terminal object|terminal]] Archimedean ordered field which is admissible for $\Sigma$ is the ordered field of two-sided $\Sigma$-[[Dedekind real numbers]], which are constructed out of the [[Dedekind cuts]] valued in $\Sigma$. 

* Assuming the [[limited principle of omniscience]], the [[boolean domain]] $\mathbb{2}$ is a $\sigma$-frame of propositions, which means that every [[discrete field|discrete]] [[Archimedean ordered field]] is admissible for the [[boolean domain]]. In addition, assuming [[LPO]], the [[Cauchy real numbers]], [[HoTT book real numbers]], and the lower, upper, and two-sided $\mathbb{2}$-[[Dedekind real numbers]] are all $\mathbb{2}$-admissible Archimedean ordered fields. 

## Related concepts

* [[sigma-frame of propositions]]

* [[Archimedean ordered field]]

## References

Archimedean ordered fields admissible for $\Sigma$ are defined in section 11.2.3 of:

* [[Univalent Foundations Project]], *[[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]]* (2013)

[[!redirects admissible Archimedean ordered field]]
[[!redirects admissible Archimedean ordered fields]]

[[!redirects admissible archimedean ordered field]]
[[!redirects admissible archimedean ordered fields]]

[[!redirects admissible Archimedean field]]
[[!redirects admissible Archimedean fields]]

[[!redirects admissible archimedean field]]
[[!redirects admissible archimedean fields]]