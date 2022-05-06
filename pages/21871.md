+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linguistics
+-- {: .hide}
[[!include linguistics - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

Context-sensitive grammar is a kind of [[formal grammar]] with an expressive power between that of [[context-free grammar]] and [[formal grammar#unrestrictedgrammar|unrestricted grammar]], they are at the second level of [[Chomsky hierarchy]].

## Definition

A context-sensitive grammar is a tuple $(V, X, R, s)$ where $V$ and $X$ are disjoint finite sets of terminal and non-terminal symbols with $s \in X$, $R$ is a finite set of rules $\alpha x \gamma \to \alpha \beta \gamma$ for a non-terminal symbol $x \in X$, strings of symbols $\alpha, \gamma \in (V + X)^\star$ and a non-empty string $\beta \in (V + X)^+$.

In order to make the [[context-free language|context-free languages]] a proper subset of the context-sensitive languages, the rule $s \to 1$ is allowed for $1$ the empty string.

## Example

Any [[context-free language]] is also context-sensitive. The language $L=\{a^m b^m c^m| m\geq 1\}$ is context-sensitive but a classical application of the [[pumping lemma]] shows that $L$  is not context-free.

## Properties

The parsing problem, i.e. given a grammar $G$ and a string $\alpha \in V^\star$ decide whether $\alpha \in L(G)$ is [[PSPACE]]-complete. Thus, it is suspected to be infeasible to solve efficiently. This motivated the definition of [[mildly context-sensitive grammar]].

## Related entries

* [[context-free grammar]]

* [[mildly context-sensitive grammar]]