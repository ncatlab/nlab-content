#Contents#
* table of contents
{:toc}

## Idea

The localisation of a commutative ring $A$ at an element $a$ of it is a universal means to 'invert $a$' . The resulting ring captures information that is relevant 'at $a$', i.e. 'locally at $a$'. 

## Definition

Let $A$ be a commutative ring, and let $a$ be an element of $A$.

+-- {: .num_defn}
###### Definition

The _localisation of $A$ at $a$_, usually denoted $A_{a}$ or $A[1/a]$, is the commutative ring $A[x] / (ax - 1)$. 

=--

Here (the equivalence class of) $x$ is to be thought of as $a^{-1}$.

Equivalently, we can define $A_{a}$ to be the localisation of $A$ with respect to the multiplicative system $S = { a, a^{2}, a^{3}, \ldots }$. This general notion of localisation is discussed at [[localisation of a commutative ring]].


+-- {: .num_remark}
###### Example

If $A$ is the polynomial ring $\mathbb{Z}[x]$, and $a$ is $x$, then $A_{a}$ is the ring of [[Laurent polynomials|Laurent polynomial]] $\mathbb{Z}[x, x^{-1}]$. 

=--



