
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

## Idea

Abstracting the von Neumann ordinals and the Zermelo ordinals, amongst other definitions of the [[natural numbers]], in [[material set theory]]. 

## Definition

Given a set $V$ with an [[extensional relation]] $\prec$, a **natural numbers structure** is an element $\mathbb{N} \in V$, an element $0 \in V$, and a function $s:V \to V$ such that 

* $0 \prec \mathbb{N}$
* for all $x \in V$, if $x \prec \mathbb{N}$, then $s(x) \prec \mathbb{N}$
* for all $z \in V$, if $0 \prec z$ and for all $x \in V$, if $x \prec z$, then $s(x) \prec z$, then for all $x \in V$, $x \prec \mathbb{N}$ implies that $x \prec z$. 

## Foundational concerns

Usually in [[material set theory]], $0$ is defined to be the [[empty set]] $\emptyset$, $\mathbb{N}$ is defined to be the [[von Neumann ordinal]] $\omega$, and $s$ is defined to be the operation $x \mapsto x \cup \{x\}$. However, there are alternative options, such as using the Zermelo ordinals, where the operation $s$ is given by $x \mapsto \{x\}$, amongst others. 

One could avoid having to choose amongst the definitions and abstract it all by adding primitive constants $\mathbb{N}$ and $0$ and primitive unary operation $s$ to the set theory, satisfying the axiom 

* $0 \in \mathbb{N}$; for all sets $x$, if $x \in \mathbb{N}$, then $s(x) \in \mathbb{N}$; and for all sets $z$, if $0 \in z$ and for all sets $x$, if $x \in z$, then $s(x) \in z$, then for all sets $x$, $x \in \mathbb{N}$ implies that $x \in z$. 

## See also

* [[axiom of infinity]]
* [[pairing structure]]
* [[union structure]]
* [[powerset structure]]