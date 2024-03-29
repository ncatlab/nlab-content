
# Closure algebras
* table of contents
{: toc}

## Idea

Closure algebras are type one [[modal algebras]], in which  the single operator behaves like a [[topological closure|closure]] operation in a [[topological space]].


## Definitions

+-- {: .un_defn}
###### Definition

A **closure algebra** is a [[Boolean algebra]] with operator, $(\mathbb{B}, m)$, which satisfies:
for all $x$, $x + m m x \leq m x$.
=--

In general, if $(\mathbb{B}, m)$ is a closure algebra and $x \in B$, we say that $x$ is _closed_ if $m x = x$ and _open_ if $l x = x$, where $l$ is the [[de Morgan duality|dual]] operator of $m$.

A closure algebra is sometimes written in terms of $l$ instead of $m$ and is then called an **interior algebra**.


## Examples

Let $X$ be a [[topological space]] and $\mathbb{P}(X)$ the [[powerset]] Boolean algebra of the underlying set of $X$.  Set $m T$ to be the [[topological closure]] of the set $T \subseteq X$ in the topology of $X$, then $(\mathbb{P}(X), m)$ is a closure algebra.


## Properties

*  If $\mathfrak{B} = (\mathbb{B}, m)$ is a closure algebra, let $Open(\mathfrak{B})$ be the set of open elements in $\mathfrak{B}$, then $Open(\mathfrak{B})$ has the natural structure of a [[Heyting algebra]].  Moreover any Heyting algebra can be represented as the algebra of open elements of a closure algebra.

*  Closure algebras underly the algebraic semantic models of the [[epistemic logic]] $S4$.

*  The algebraic semantics of $S4(n)$ uses [[polyclosure algebra]]s. Here there are many different closure operators on the Boolean algebra.


[[!redirects closure algebra]]
[[!redirects closure algebras]]
[[!redirects interior algebra]]
[[!redirects interior algebras]]
