
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

### Pairing structure

Given a [[set]] $V$ with an [[extensional relation]] $\prec$ on $V$, a **pairing structure** is a [[binary function]] $P:V \times V \to V$ such that

* for all $a \in V$ and $b \in V$, $a \prec P(a, b)$ and $b \prec P(a, b)$

### Unordered pairing structure

An **unordered pairing structure** on $V$ is pairing structure $\{-,-\}:V \times V \to V$ where additionally

* for all sets $z$, $z \in \{x, y\}$ implies that $z = x$ or $z = y$. 

Uniqueness of $\{x, y\}$ follows from $\prec$ being an [[extensional relation]]. 

### Ordered pairing structure

An **ordered pairing structure** on $V$ is a pairing structure $(-,-):V \times V \to V$ which satisfies [[product extensionality]]: 

* for all $a \in V$, $a' \in V$, $b \in V$, $b' \in V$, $P(a, b) = P(a', b')$ if and only if $a = a'$ and $b = b'$

## Foundational concerns

In any [[material set theory]], instead of postulating the mere existence of a set $P$ in which $a \in P$ and $b \in P$ one could add a primitive binary operation $P(a, b)$ which takes material sets $a$ and $b$ and returns a material set $P(a, b)$ such that for all $a$ and $b$, $a \in P(a, b)$ and $b \in P(a, b)$

## See also

* [[axiom of pairing]] 

* [[union structure]]

* [[powerset structure]]

* [[natural numbers structure]]

* [[product extensionality]]

## References

* [[Håkon Robbestad Gylterud]], [[Elisabeth Stenholm]], [[Niccolò Veltri]] *Terminal Coalgebras and Non-wellfounded Sets in Homotopy Type Theory* &lbrack;[arXiv:2001.06696](https://arxiv.org/abs/2001.06696)&rbrack;

[[!redirects pairing structure]]
[[!redirects pairing structures]]

[[!redirects unordered pairing structure]]
[[!redirects unordered pairing structures]]

[[!redirects ordered pairing structure]]
[[!redirects ordered pairing structures]]