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

A context-sensitive grammar is a tuple $(V, X, R, s)$ where $V$ and $X$ are finite sets of terminal and non-terminal symbols with $s \in X$, $R$ is a finite set of rules $\alpha x \gamma \to \alpha \beta \gamma$ for a non-terminal symbol $x \in X$ and strings of symbols $\alpha, \beta, \gamma \in (V + X)^\star$.

## Example

Any context-free language is also context-sensitive. The language $L=\{a^m b^m c^m| m\geq 1\}$ is context-sensitive but a classical application of the [[pumping lemma]] shows that $L$  is not context-free.

## Related entries

* [[context-free grammar]]

* [[mildly context-sensitive grammar]]