
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition 

### In the real numbers

The [[open interval]] in $A$ between elements $a \in A$ and $b \in B$ is the set 

$$\mathrm{OpenInt}(a,b) = \{d \in A \vert a \lt d \lt b\}$$

A **locator** for a real number $c \in \mathbb{R}$ is an element of the indexed [[cartesian product]]

$$l \in \prod_{a \in \mathbb{Q}} \prod_{b \in \mathbb{Q}} \left([\mathrm{OpenInt}(a,c)] \uplus [\mathrm{OpenInt}(c,b)]\right)^{[\mathrm{OpenInt}(a,b)]}$$

where $A \uplus B$ is the [[disjoint union]] of two sets $A$ and $B$, $B^A$ is the [[function set|set of functions]] from $A$ to $B$, $[A]$ is the [[support of a set|support]] of $A$, and the indexed [[cartesian product]] is defined in [[set theory]] as

$$\prod_{a \in A} B(a) = \{f \in \left(\bigcup_{a\in A} B(a)\right)^A \vert \forall a, f(a) \in B(a) \}$$

for [[family of sets]] $(B(a))_{a \in A}$.

### In arbitrary dense linear orders

Given a [[dense linear order]] $(A, \lt_A)$, the [[open interval]] in $A$ between elements $a \in A$ and $b \in B$ is the set 

$$\mathrm{OpenInt}(a,b) = \{c \in A \vert a \lt c \lt b\}$$

Given a [[countable dense linear order]] $(B, \lt_B)$ such that $B \subseteq A$ and for all elements $a \in A$ and $b \in A$ where $a \lt b$, there exists $c \in B$ such that $a \lt c \lt b$, a **$B$-indexed locator** for an [[element]] $c \in A$ is an element of the indexed [[cartesian product]]

$$l \in \prod_{a \in B} \prod_{b \in B} \left([\mathrm{OpenInt}(a,c)] \uplus [\mathrm{OpenInt}(c,b)]\right)^{[\mathrm{OpenInt}(a,b)]}$$

## In dependent type theory

In dependent type theory, given a real number $r:\mathbb{R}$, a locator on the [[Dedekind real numbers]] is a [[dependent function]] 

$$l:\prod_{p:\mathbb{Q}} \prod_{q:\mathbb{Q}} (p \lt q) \to ((p \lt r) + (r \lt q))$$

Locators were originally defined in [Booij 2020](#Booij20) as a [[propositions as types]] formulation of the locatedness property of [[Dedekind cuts]]. However, locators as defined do not fully satisfy [[propositions as types]]: since the [[real numbers]] are [[dense]], the proposition $p \lt q$ is equivalent to the existence of an element $r:\mathbb{R}$ such that $p \lt r$ and $r \lt q$, i.e. $p \lt q$ is equivalent to the [[propositional truncation]] of the [[open interval]] $\mathrm{OpenInt}(p,q) \coloneqq \sum_{r:\mathbb{R}} (p \lt r) \times (r \lt q)$:

$$l:\prod_{p:\mathbb{Q}} \prod_{q:\mathbb{Q}} [\mathrm{OpenInt}(p, q)] \to ([\mathrm{OpenInt}(p, r)] + [\mathrm{OpenInt}(r, q)])$$ 

## Properties 

* A locator is equivalent to having the structure of a [[Cauchy sequence]] with [[modulus of convergence]]. This is stronger than merely being a [[modulated Cauchy real number]].

* That every [[Dedekind real number]] has a $\mathbb{Q}$-indexed locator implies the weak [[limited principle of omniscience]]. 

## Principle of locators

Note: The "principle of locators" or "axiom of locators" are placeholder names for a principle or axiom which may or may not have an already existing name in the mathematics literature. 

The **principle of locators** for a set of real numbers $\mathbb{R}$ state that every real number $x:\mathbb{R}$ merely has a locator (i.e. the [[support]] of the locator has an element), and implies that the [[Cauchy real numbers]] $\mathbb{R}_C$ coincides with $\mathbb{R}$. This is true for the [[Dedekind real numbers]] $\mathbb{R}_D$ in [[classical mathematics]], as is in [[constructive mathematics]] which also uses [[countable choice]]. 

However, in general constructive mathematics, while theorem 6.10.3 of [Booij 2020](#Booij20) states that a real number is a [[Cauchy real number]] if and only if it merely has a locator, not every real number is necessarily a Cauchy real number, so it is not necessarily true that every real number in a given has a locator. In that case, this principle becomes the **axiom of locators** for a set of real numbers $\mathbb{R}$, which says that every element $x:\mathbb{R}$ of the set of real numbers $\mathbb{R}$ merely has a locator, making it coincide with the [[Cauchy real numbers]]. The axiom of locators is equivalent to the order relation on the real numbers $\mathbb{R}$ being [[semi-decidable]], as both imply that $\mathbb{R}$ coincides with the Cauchy real numbers. 

The axiom of locators for the [[Sierpinski semi-decidable]] [[Dedekind real numbers]] $\mathbb{R}_\Sigma$, constructed using [[Sierpinski semi-decidable]] [[Dedekind cuts]] $\mathbb{Q}^\Sigma \times \mathbb{Q}^\Sigma$, is equivalent to the following statements:

* the [[existential quantification]] of a [[sequence]] of [[semi-decidable propositions]] is a semi-decidable proposition

* the [[lattice]] of semi-decidable propositions is a [[dominance]]. 

## Related concepts

* [[Dedekind cut]]
* [[Dedekind cut structure]]
* [[dense linear order]]
* [[lifting to locators]]

## References 

* [[Auke Booij]], *Analysis in univalent type theory* (2020) $[$[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)$]$

* [[Steve Vickers]], *Locators point-free* ([pdf](https://www.cs.bham.ac.uk//~sjv/locatorsPF.pdf))

[[!redirects locators]]

[[!redirects principle of locators]]
[[!redirects axiom of locators]]
