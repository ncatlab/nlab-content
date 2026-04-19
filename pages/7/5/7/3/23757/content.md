
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

### In dependent type theory

In dependent type theory, given a real number $r:\mathbb{R}$, a locator on the [[Dedekind real numbers]] is a [[dependent function]] 

$$l:\prod_{p:\mathbb{Q}} \prod_{q:\mathbb{Q}} (p \lt q) \to ((p \lt r) + (r \lt q))$$

Locators were originally defined in [Booij 2020](#Booij20) as a [[propositions as types]] formulation of the locatedness property of [[Dedekind cuts]]. However, locators as defined do not fully satisfy [[propositions as types]]: since the [[real numbers]] are [[dense]], the proposition $p \lt q$ is equivalent to the existence of an element $r:\mathbb{R}$ such that $p \lt r$ and $r \lt q$, i.e. $p \lt q$ is equivalent to the [[propositional truncation]] of the [[open interval]] $\mathrm{OpenInt}(p,q) \coloneqq \sum_{r:\mathbb{R}} (p \lt r) \times (r \lt q)$:

$$l:\prod_{p:\mathbb{Q}} \prod_{q:\mathbb{Q}} [\mathrm{OpenInt}(p, q)] \to ([\mathrm{OpenInt}(p, r)] + [\mathrm{OpenInt}(r, q)])$$ 

## Properties 

### Relation to the Cauchy real numbers

Every [[Cauchy real number]] merely has a rational-indexed locator; that is, for each Cauchy real number, the set of its rational-indexed locators is [[inhabited]]. This is different from every [[Cauchy real number]] carrying the structure of a rational-indexed locator, which implies the weak [[limited principle of omniscience]]. This is because a rational-indexed locator is equivalent to having the structure of a [[Cauchy sequence]] with [[modulus of convergence]]. On the other hand, a [[Cauchy real number]] by definition merely has a [[Cauchy sequence]] with [[modulus of convergence]]; that is, for each Cauchy real number, the set of its [[Cauchy sequence]] with [[modulus of convergence]] that converge on it is [[inhabited]]. 

In addition, we have the following theorems that say under what conditions the [[Dedekind real numbers]] coincide with the [[Cauchy real numbers]]:

+-- {: .num_theorem}
###### Theorem
The following statements are equivalent:

1. The [[Dedekind real numbers]] coincide with the [[Cauchy real numbers]].

1. Every [[Dedekind real number]] $r$ merely has a rational-indexed locator.

1. The order relation $\lt$ on the [[Dedekind real numbers]] is [[semi-decidable]].
=--

This means that any of these statements can be used to make the [[Cauchy real numbers]] and [[Dedekind real numbers]] coincide with each other. This is the case in [[classical mathematics]], as is in [[constructive mathematics]] which also uses [[countable choice]]. 

We can also consider the subset of [[Sierpinski semi-decidable]] [[Dedekind real numbers]] $\mathbb{R}_\Sigma$, constructed using [[Sierpinski semi-decidable]] [[Dedekind cuts]] $\mathbb{Q}^\Sigma \times \mathbb{Q}^\Sigma$. 

+-- {: .num_theorem}
###### Theorem
The following statements are equivalent:

1. The [[Sierpinski semi-decidable]] [[Dedekind real numbers]] coincide with the [[Cauchy real numbers]].

1. Every [[Sierpinski semi-decidable]] [[Dedekind real number]] $r$ merely has a rational-indexed locator.

1. The order relation $\lt$ on the [[Sierpinski semi-decidable]] [[Dedekind real numbers]] is [[semi-decidable]].

1. The [[existential quantification]] of a [[sequence]] of [[semi-decidable propositions]] is a semi-decidable proposition.

1. The [[lattice]] of semi-decidable propositions is a [[dominance]], the [[Rosolini dominance]]. 
=--

This means that any of these statements can be used to make the [[Cauchy real numbers]] and [[Sierpinski semi-decidable]] [[Dedekind real numbers]] coincide with each other. 

## Related concepts

* [[Dedekind cut]]
* [[Dedekind cut structure]]
* [[dense linear order]]
* [[lifting to locators]]

## References 

* [[Auke Booij]], *Analysis in univalent type theory* (2020) $[$[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)$]$

* [[Steve Vickers]], *Locators point-free* ([pdf](https://www.cs.bham.ac.uk//~sjv/locatorsPF.pdf))

[[!redirects locators]]
