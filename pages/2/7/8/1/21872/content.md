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

Mildly context-sensitive grammar is a kind of formal grammar with an expressivity between that of [[context-free grammar]] and [[context-sensitive grammar]].
They have enough expressive power to capture natural languages, but not too much so that they are still parsable efficiently.

## Definition

While there has been no consensus on the definition of “mild”, there is an
equivalence [VW94] between several independent definitions, see [Weir (1988)](#Weir88).
Borrowing the definition from [Genkin et al. (2010)](#GenkinEtAl10), a grammar formalism is mildly context-sensitive if the languages it
generates are [[semilinearity|semilinear]], it is parsable in polynomial time, it contains all context-free languages as well as the following:

* multiple agreement $L1 = \{ a^n b^n c^n | a, b, c \in V, n \in \mathbb{N} \},$
* crossed dependency $L2 = \{ a^n b^m c^n d^m | a, b, c, d \in V, m, n \in \mathbb{N} \}$,
* duplication $L3 = \{ww | w \in V^\star\}$.

## References

* {#Shieber85} Shieber, Stuart M. _Evidence against the context-freeness of natural language._ Philosophy, Language, and Artificial Intelligence. Springer, Dordrecht, 1985.
* {#Weir88} Weir, David Jeremy. _Characterizing mildly context-sensitive grammar formalisms_, 1988.
* {#GenkinEtAl10} Daniel Genkin, Nissim Francez, and Michael Kaminski. _Mildly Context-Sensitive Languages via Buffer Augmented Pregroup Grammars_, In Essays in Memory of Amir Pnueli, 2010.