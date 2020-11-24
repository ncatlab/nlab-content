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

## Idea

Regular languages are a simple kind of [[formal grammar|formal languages]], the least expressive in [[Chomsky hierarchy]].

## Definition

Fix a finite vocabulary $V$ and denote its free monoid by $V^\star$. A language $L \subseteq V^\star$ is regular whenever there is a [[formal grammar]] $G = (V, X, R, s)$ that generates it (i.e. $L(G) = L$) such that all rules in $R$ are of the form $x \to w x'$ for a terminal $w \in V$ and non-terminal symbols $x, x' \in X$.

## Properties

Regular languages can be characterised by _regular expressions_:

* the empty language $\emptyset$ is regular,
* every terminal symbol $\{w \in V\}$ is regular,

if $L$ and $L'$ are regular, then:

* their union $L \cup L' = \{\alpha \in V^\star \vert \alpha \in L \vee \alpha \in L' \}$ is regular,
* their concatenation $LL' = \{\alpha \in V^\star \vert \exists \beta \in L, \gamma \in L' \cdot \alpha = \beta \gamma \}$ is regular,
* the Kleene star $L^\star = \{ \alpha \in V^\star \vert \exists \beta \in L, n \in \mathbb{N} \cdot \alpha = \beta^n \}$ is regular.

Every regular language can be generated in that way.

A language is regular whenever it can be recognised by a finite-state [[automaton]].

## Related entries

* [[context-free grammar]]