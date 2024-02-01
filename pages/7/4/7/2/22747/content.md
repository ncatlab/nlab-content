# Ordered integral domains
* table of contents
{: toc}

## Idea

An ordered integral domain is an [[integral domain]] equipped with a compatible [[strict total order]].

Note that while the adjective 'ordered' usually refers to a [[total order]], which by default is non-strict, it is traditionally used more strictly when placed before 'integral domain'.

## Definition

An __ordered integral domain__ is an [[integral domain]] $R$ equipped with a [[strict total order]] $\lt$ such that:

* $0 \lt 1$

* for all $a \in R$ and $b \in R$, $0 \lt a$ and $0 \lt b$ implies that $0 \lt a + b$; alternatively, $0 \lt a + b$ implies that $0 \lt a$ or $0 \lt b$. 

* for all $a \in R$ and $b \in R$, if $0 \lt a$ and $0 \lt b$, then $0 \lt a \cdot b$

## Examples

The integral domain $\mathbb{R}$ of [[real numbers]], the integral domain $\mathbb{Z}$ of [[integers]], and the integral domain $\mathbb{Q}$ of rational numbers are all ordered integral domains. 

## Properties

Every ordered integral domain must have [[characteristic]] $0$, since we can prove by [[induction]] that $n \gt 0$ for every positive [[natural number]] $n$.

The [[archimedean integral domain|archimedean]] ordered integral domain are precisely the [[subobject|integral subdomains]] of [[real number|the integral domain of real numbers]].

Every [[localization of a commutative ring|localization]] of the integral domain of integers away from a subset not containing zero is a [[dense linear order]], and the [[Dedekind completion]] of the resulting integral domain is the integral domain of real numbers. In particular, the Dedekind completions of the [[dyadic rational numbers]] and the [[decimal rational numbers]] are both the real numbers. 

## Related concepts

* [[pseudo-ordered ring]]

* [[ordered field]]

* [[protoring]]

[[!redirects ordered integral domain]]
[[!redirects ordered integral domains]]
