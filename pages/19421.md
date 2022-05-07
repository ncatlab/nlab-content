
#Contents#
* table of contents
{:toc}

## Idea

The localisation of a commutative ring $A$ away from an element $a\in A$ is a universal means to 'invert $a$'.  The resulting ring captures information that is relevant 'away from $a$', i.e. 'locally on the complement of $a$'.

Algebraically, it might make more sense to call this localization *at* $a$, but in [[algebraic geometry]] it really does correspond to "local behavior on the complement of (the zero-set of) $a$", and the "away from" terminology is traditional.

## Definition

Let $A$ be a commutative ring, and let $a$ be an element of $A$.

+-- {: .num_defn}
###### Definition

The _localisation of $A$ away from $a$_, usually denoted $A_{a}$ or $A[1/a]$, is the commutative ring $A[x] / (a x - 1)$. 

=--

Here (the equivalence class of) $x$ is to be thought of as $a^{-1}$.

Equivalently, we can define $A_{a}$ to be the localisation of $A$ with respect to the multiplicative system $S = { a, a^{2}, a^{3}, \ldots }$. This general notion of localisation is discussed at [[localisation of a commutative ring]].

+-- {: .num_remark}
###### Example

If $A$ is the ring of integers $\mathbb{Z}$, and $a$ is $10$, then $A_{a}$ is the ring of [[decimal rational numbers]] $\mathbb{Z}[1/10]$. 

=--

+-- {: .num_remark}
###### Example

If $A$ is the polynomial ring $\mathbb{Z}[x]$, and $a$ is $x$, then $A_{a}$ is the ring of [[Laurent polynomials|Laurent polynomial]] $\mathbb{Z}[x, x^{-1}]$. 

=--


[[!redirects localisation of a commutative ring at an element]]
[[!redirects localization of a commutative ring at an element]]
[[!redirects localisation of a commutative ring away from an element]]
[[!redirects localization of a commutative ring away from an element]]

[[!redirects localisation of a ring at an element]]
[[!redirects localization of a ring at an element]]
[[!redirects localisation of a ring away from an element]]
[[!redirects localization of a ring away from an element]]

[[!redirects localisation at an element]]
[[!redirects localization at an element]]
[[!redirects localisation away from an element]]
[[!redirects localization away from an element]]
