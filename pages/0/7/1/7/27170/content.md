


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--

\tableofcontents


## Definition

A *$(k,n)$-Grassmann necklace* $I = (I_1, I_2,\ldots, I_n)$ is an $n$-tuple of $k$-element
subsets of $[n]$ such that for each $a \in [n]$, 

(1) $I_{a+1} = I_a$ if $a\notin I_a$

(2) $I_{a+1} = I_a \backslash \{a\}\cup \{b\}$ for some $b\in [n]$ if $a\in I_a$

with subscripts taken modulo $n$.

Note that we allow $b=a$ in case (2), but we cannot have $b \in I_\{a\}\backslash \{a\}$, or else I_{a+1} would not have $k$ elements.

## Properties

* Grassmann necklaces parameterize [[total positivity|totally nonnegative]] points in [[Grassmannian]].

* Grassmann necklaces are in [[bijection]] with [[decorated permutations]].

## Literature

Introduced in

* [[Alexander Postnikov]]: _Total positivity, Grassmannians, and networks_ &lbrack;[arXiv:math/0609764](https://arxiv.org/abs/math/0609764)&rbrack;

category: combinatorics

[[!redirects Grassmann necklaces]]
