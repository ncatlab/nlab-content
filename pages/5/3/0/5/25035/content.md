
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

Given a set $V$ with an [[extensional relation]] $\prec$, a **proto-powerset structure** is a [[function]] $\mathcal{P}:V \to V$ such that

* for all elements $b \in V$, and $c \in V$, if for all elmemets $a \in V$, $a \prec b$ implies $a \prec c$, then $b \prec \mathcal{P}(c)$. 

A **powerset structure** is a function $\mathcal{P}:V \to V$ such that

* for all elements $b \in V$, and $c \in V$, $b \prec \mathcal{P}(c)$ if and only if for all elements $a \in V$, $a \prec b$ implies $a \prec c$. 

Uniqueness of $\mathcal{P}(c)$ follows from $\prec$ being an [[extensional relation]]. 

## Foundational concerns

In any [[material set theory]], instead of postulating the mere existence of a set $\mathcal{P}$ in which for all sets $b$, if for all sets $a$, $a \in b$ implies $a \in c$, then $b \in \mathcal{P}$, one could add a primitive unary operation $\mathcal{P}(c)$ which takes material sets $c$ and returns a material set $\mathcal{P}(c)$ such that for all $b$, if for all $a$, $a \in b$ implies $a \in c$, then $b \in \mathcal{P}(c)$. 

## See also

* [[axiom of power sets]]

* [[pairing structure]]

* [[union structure]]

[[!redirects powerset structure]]
[[!redirects powerset structures]]