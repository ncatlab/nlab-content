
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

An [[open interval]] between [[real numbers]] $a \in \mathbb{R}$ and $b \in \mathbb{R}$ is the set 

$$\mathrm{OpenInt}(a,b) = \{c \in \mathbb{R} \vert a \lt c \lt b\}$$

A **locator** for a real number $c \in \mathbb{R}$ is an element of the indexed [[cartesian product]]

$$l \in \prod_{a \in \mathbb{Q}} \prod_{b \in \mathbb{Q}} (\mathrm{OpenInt}(a,c) \uplus \mathrm{OpenInt}(c,b))^{\mathrm{OpenInt}(a,b)}$$

where $A \uplus B$ is the [[disjoint union]] of two sets $A$ and $B$, $B^A$ is the [[function set|set of functions]] from $A$ to $B$, and the indexed [[cartesian product]] is defined in [[set theory]] as

$$\prod_{a \in A} B(a) = \{f \in \left(\bigcup_{a\in A} B(a)\right)^A \vert \forall a, f(a) \in B(a) \}$$

for [[family of sets]] $(B(a))_{a \in A}$.

Equivalently, a **locator** is an element of the indexed [[cartesian product]]

$$l \in \prod_{a \in \mathbb{Q}} \prod_{b \in \mathbb{Q}} \mathrm{OpenInt}(a,c)^{\mathrm{OpenInt}(a,b)} \times \mathrm{OpenInt}(c,b)^{\mathrm{OpenInt}(a,b)}$$

### In arbitrary dense linear orders

Given a [[dense linear order]] $(A, \lt_A)$, the [[open interval]] in $A$ between elements $a \in A$ and $b \in B$ is the set 

$$\mathrm{OpenInt}(a,b) = \{c \in A \vert a \lt c \lt b\}$$

Given a [[countable dense linear order]] $(B, \lt_B)$ such that $B \subseteq A$, a **$B$-indexed locator** for an [[element]] $c \in A$ is an element of the indexed [[cartesian product]]

$$l \in \prod_{a \in B} \prod_{b \in B} (\mathrm{OpenInt}(a,c) \uplus \mathrm{OpenInt}(c,b))^{\mathrm{OpenInt}(a,b)}$$

## In dependent type theory

In dependent type theory, given a real number $r:\mathbb{R}$, a locator on the [[Dedekind real numbers]] is a [[dependent function]] 

$$l:\prod_{p:\mathbb{Q}} \prod_{q:\mathbb{Q}} (p \lt q) \to ((p \lt r) + (r \lt q))$$

## Properties 

* A locator is equivalent to having the structure of a [[Cauchy sequence]] with [[modulus of convergence]]. This is stronger than merely being a [[modulated Cauchy real number]].

* That every [[Dedekind real number]] has a $\mathbb{Q}$-indexed locator implies the weak [[limited principle of omniscience]]. 

## Related concepts

* [[Dedekind cut]]
* [[Dedekind cut structure]]
* [[dense linear order]]
* [[lifting to locators]]

## References 

* [[Auke Booij]], *Analysis in univalent type theory* (2020) $[$[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)$]$

* [[Steve Vickers]], *Locators point-free* ([pdf](https://www.cs.bham.ac.uk//~sjv/locatorsPF.pdf))

[[!redirects locators]]

