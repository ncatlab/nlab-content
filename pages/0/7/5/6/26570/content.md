
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

## Definition

A [[proposition]] or [[truth value]] $P$ is **semi-decidable** or **semidecidable** if and only if [[existential quantifier|there exists]] a [[sequence]] of [[booleans]] $f \in 2^\mathbb{N}$ such that $P$ if and only if there exists a natural number $x \in \mathbb{N}$ such that $f(x) = 1$. 

$$\mathrm{isSemiDecidable}(P) \coloneqq \exists f \in 2^\mathbb{N}.P \iff \exists x \in \mathbb{N}.f(x) = 1$$

The [[limited principle of omniscience]] for the [[natural numbers]] $\mathrm{LPO}_\mathbb{N}$ implies that every semi-decidable proposition is a [[decidable proposition]]. 

### In dependent type theory

In dependent type theory, the definition of semi-decidable makes sense for any type, not just the mere propositions. However, like many other definitions in [[dependent type theory]], one has to make sure to use an [[equivalence of types]] instead of [[logical equivalence]] in the definition of a semi-decidable type; this ensures that, like for decidable types, all semi-decidable types are propositions. 

\begin{definition}
A type $P$ is semi-decidable if [[existential quantifier|there exists]] a [[sequence]] of [[booleans]] $f:\mathbb{N} \to \mathrm{bool}$ such that $P$ is equivalent to that there exists a natural number $x:\mathbb{N}$ such that $f(x) = 1$. 

$$\mathrm{isSemiDecidable}(P) \coloneqq \left[\sum_{f:\mathbb{N} \to \mathrm{bool}} P \simeq \left[ \sum_{x:\mathbb{N}}f(x) =_{\mathrm{bool}} 1\right]\right]$$
\end{definition}

where $[A]$ is the [[bracket type]] of the type $A$. 

There is also a partially untruncated version of this, which is the type 

$$\sum_{f:\mathbb{N} \to \mathrm{bool}} P \simeq \left[\sum_{x:\mathbb{N}}f(x) =_{\mathrm{bool}} 1\right]$$

of all boolean sequences $f$ for which $P$ is equivalent to there exists a natural number $x:\mathbb{N}$ such that $f(x) = 1$. 

## Set of semi-decidable truth values

The set of all semi-decidable truth values $\Sigma_0^1$ is defined as a [[subset]] of the [[set of truth values]] $\Omega$ containing all the semi-decidable truth values:

$$\Sigma_0^1 \coloneqq \{P \in \Omega \vert \exists f \in 2^\mathbb{N}.(P = \top) \iff \exists x \in \mathbb{N}.f(x) = 1$$

In [[predicative mathematics]], the set of *all* [[truth values]] may not exist, so instead in order to construct the set of all semi-decidable truth values, we take any [[subobject|sub]]-[[sigma-frame|$\sigma$-frame]] of truth values $\Sigma$ and collect the ones that are semi-decidable:

$$\Sigma_0^1 \coloneqq \{P \in \Sigma \vert \exists f \in 2^\mathbb{N}.(P = \top) \iff \exists x \in \mathbb{N}.f(x) = 1$$

Such [[sigma-frame|$\sigma$-frames]] $\Sigma$ are usually found by collecting the [[subsingletons]] of a [[universe of sets]] $U$ in the theory into a set $\Omega_U$, or minimally, by the set of quasi-decidable truth values defined later in this article. 

The set of all semi-decidable truth values is typically called the **[[Rosolini dominance]]**, though it is a [[dominance]] [[if and only if]] semi-decidable truth values are closed under [[existential quantification]] over the [[natural numbers]], which follows from certain assumptions such as [[countable choice]] or [[excluded middle]]. 

## Relation to Cauchy real numbers

Let $\mathbb{R}_C$ denote the [[Cauchy real numbers]]. Then a [[proposition]] $P$ is semideciable if and only if there exists a Cauchy real number $x \in \mathbb{R}_C$ such that $P$ if and only if $x \gt 0$.

$$\mathrm{isSemiDecidable}(P) \coloneqq \exists x \in \mathbb{R}_C.P \iff x \gt 0$$

This implies that the [[Cauchy real numbers]] are an [[Archimedean ordered field]] [[admissible Archimedean ordered field|admissible]] for the set of semi-decidable truth values $\Sigma_0^1$, and in fact that the [[Cauchy real numbers]] are the terminal [[Archimedean ordered field]] that is admissible for $\Sigma_0^1$. 

Furthermore, this implies that any Archimedean ordered [[field extension]] of the Cauchy real numbers whose order relation $\lt$ is semi-decidable is isomorphic to the [[Cauchy real numbers]]. This can be used to make the [[Dedekind real numbers]] and Cauchy real numbers coincide, by stipulating that the order relation $\lt$ on the [[Dedekind real numbers]] is semi-decidable. 

## Generalizations

### Ordinal decidable propositions

Given an [[ordinal]] $\alpha$, there exists a notion of **$\alpha$-decidable propositions** ([de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26)), where the usual notion of semi-decidable proposition is an $(\omega + 1)$-decidable proposition. 

### Sierpiński semi-decidable propositions

One can also consider the closure of semi-decidable propositions under existential quantification over the [[natural numbers]]; these are the *[[quasi-decidable propositions]]* or the *Sierpiński semi-decidable propositions*. 

## Related concepts

* [[decidable proposition]]

* [[proposition]], [[truth value]]

## References

* [[Andrej Bauer]], [[Davorin Lešnik]], _Metric Spaces in Synthetic Topology_, 2010 ([pdf](http://math.andrej.com/wp-content/uploads/2010/01/csms_in_synthtop.pdf))

* {#JKMF26} [[Tom de Jong]], [[Nicolai Kraus]], [[Aref Mohammadzadeh]], [[Fredrik Nordvall Forsberg]], *Generalized Decidability via Brouwer Trees* ([arXiv:2602.10844](https://arxiv.org/abs/2602.10844))

[[!redirects semi-decidable]]

[[!redirects semidecidable]]

[[!redirects semi-decidable proposition]]
[[!redirects semi-decidable propositions]]

[[!redirects semidecidable proposition]]
[[!redirects semidecidable propositions]]

[[!redirects semi-decidable truth value]]
[[!redirects semi-decidable truth values]]

[[!redirects semidecidable truth value]]
[[!redirects semidecidable truth values]]

[[!redirects set of semi-decidable propositions]]
[[!redirects set of semidecidable propositions]]

[[!redirects set of semi-decidable truth values]]
[[!redirects set of semidecidable truth values]]

[[!redirects semi-decidable type]]
[[!redirects semi-decidable types]]

[[!redirects semidecidable type]]
[[!redirects semidecidable types]]