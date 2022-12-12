
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

Given a set $V$ with an [[extensional relation]] $\prec$, a **proto-union structure** is a [[function]] $U:V \to V$ such that

* for all elements $a \in V$, $b \in V$, and $c \in V$, if $a \prec b$ and $b \prec c$, then $a \prec U(c)$. 

Given a set $V$ with an [[extensional relation]] $\prec$, a **union structure** is a proto-union structure where additionally

* for all elements $a \in V$ and $c \in V$, if $a \prec U(c)$, then there exists $b \in V$ such that $a \prec b$ and $b \prec c$.

Uniqueness of $U(c)$ follows from $\prec$ being an [[extensional relation]]. 

## Foundational concerns

In any [[material set theory]], instead of postulating the mere existence of a set $U$ in which $a \in b$ and $b \in c$ implies that $a \in U$, one could add a primitive unary operation $U(c)$ which takes material sets $c$ and returns a material set $U(c)$ such that for all $a$ and $b$, $a \in b$ and $b \in c$ implies that $a \in U(c)$. 

## See also

* [[axiom of union]]

* [[pairing structure]]

* [[powerset structure]]

[[!redirects union structure]]
[[!redirects union structures]]