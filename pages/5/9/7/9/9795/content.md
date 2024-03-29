
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A subset $B$ of a [[vector space]] $V$ over $\mathbb{R}$ or $\mathbb{C}$ is **absolutely convex** if $\lambda x + \mu y \in B$ whenever $x, y \in B$ and ${|\lambda|} + {|\mu|} \le 1$.

## Properties

Absolutely convex subsets are closely related to [[semi-norms]].
Given a vector space $V$ and an absolutely convex subset $B \subseteq V$, we define $V_B$ to be the linear span of $B$ in $V$.  Then let $\mu_B \colon V_B \to \mathbb{R}$ be the [[Minkowski functional]] of $B$.  That is, $\mu_B$ is given by:

$$
\mu_B(v) = \inf\{ t \gt 0 : t v \in B\}
$$

Then $\mu_B$ is a semi-norm on $V_B$ and $E_B \coloneqq V_B/\ker \mu_B$ is a [[normed space]].

# Related concepts

* [[convex set]]
* [[balanced set]]


[[!redirects absolutely convex]]
[[!redirects absolutely convex set]]
[[!redirects absolutely convex sets]]
[[!redirects absolutely convex subset]]
[[!redirects absolutely convex subsets]]
