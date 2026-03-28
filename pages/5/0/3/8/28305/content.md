
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+--{: .hide}
[[!include (0,1)-category theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


\tableofcontents


## Idea

(Propositional) _dynamic logic_ is an extension of [[propositional logic]] where [[propositions]] can be annotated by [[modal logic|modal]] constructions in order to reason about computer [[programs]].

If $a$ ranges over (possibly non-deterministic) actions and $p$ over propositions, then

- $[a]p$ means '$p$ _always_ holds after executing $a$', and
- $\langle a \rangle p$ [[duality|dually]]
  means '$p$ _sometimes_ holds after executing $a$'.

In particular, an implication of the form $p \to [a]q$ states that whenever a precondition $p$ holds, then after executing an action $a$, the postcondition $q$ will also hold, and is therefore similar to the [[Hoare logic|Hoare triple]] $\{p\} a \{q\}$.

## Syntax

$$ a, b, \dots ::= \alpha | 0 | 1 | a \mathop{;} b | a + b | a{\ast} | p{?} $$

The base actions include **fail** and **skip**, also written $0$ and $1$, respectively, and are axiomatized as follows: $[0]p$ and $[1]p \leftrightarrow p$.

For any two actions $a$ and $b$, their sequential [[composition]] $a \mathop{;} b$ satisfies $[a \mathrel{;} b]p \leftrightarrow [a][b]p$ and the non-deterministic choice $a + b$ satisfies $[a+b]p \leftrightarrow [a]p \wedge [b]p$.  Moreover, $a{\ast}$ is the unbounded iteration of $a$ and it satisfies $[a{\ast}]p \leftrightarrow p \wedge [a][a{\ast}]p$ (fixpoint) and $p \wedge [a{\ast}] (p \to [a]p) \to [a{\ast}]p$ (induction).

To each proposition $p$ is associated a test $p{?}$ which is used to write conditional expressions, i.e., if-statements, and such that $[p{?}]q \leftrightarrow (p \to q)$.

In first-order dynamic logic, actions also include assignments of the form $x := e$ such that $[x := e]p(x) \leftrightarrow p(e)$.

## Semantics

Propositional dynamic logic is typically given a relational semantics via [[Kripke structures]] (labeled transition systems): propositions are interpreted as sets of states and actions as relations.

## Related concepts

- [[Kleene algebra]]
- [[modal logic]]
- [[Hoare logic]]

## References

* Vaughan R. Pratt, _Semantical considerations on Floyd-Hoare logic_, 17th Annual IEEE Symposium on Foundations of Computer Science (1976). &lbrack;[pdf](http://boole.stanford.edu/pub/semcon.pdf)&rbrack;
* David Harel, Dexter Kozen, and Jerzy Tiuryn, _Dynamic Logic_, MIT Press (2000).