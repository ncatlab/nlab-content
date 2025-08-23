

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--


\tableofcontents


## Idea

The notion of *Fox pairings* in [[group theory]]/[[algebra]] was introduced by [Massuyeau & Turaev 2013](#MassuyeauTuraev13), who used them to define [[automorphisms]] of the [[Malcev completions]] of [[groups]].
These automorphisms generalize to the algebraic setting the action of the [[Dehn twists]] in the [[group algebras]] of the [[fundamental groups]] of [[surfaces]].


## Definition

By a *Fox pairing* in an [[augmented algebra]], $A$, over a [[commutative ring]] $K$, we mean a $K$-[[bilinear map]] $\eta : A \times A \to A$, which is a left [[Fox derivative]] with respect to the first [[variable]] and a right [[Fox derivative]] with respect to the second variable. 

## Properties

\begin{proposition} Given a Fox pairing $\eta$, the following *product formulas* hold:
$$
  \eta(a_1 a_2, b) = \eta(a_1, b) aug(a_2) + a_1\eta(a_2, b)
$$ 
for all $a_1, a_2, b\in A$; and
$$
  \eta(a, b_1b_2) = \eta(a, b_1)b_2 + aug(b_1)\eta(a, b_2)
$$ 
for all $a, b_1, b_2 \in A$.
\end{proposition}

## References 

* {#MassuyeauTuraev13} [[Gwénaël Massuyeau]], [[Vladimir Turaev]]: *Fox pairings and generalized Dehn twists*, Annales de l'Institut Fourier **63** 5 (2013) 2403-2456 &lbrack;[doi:10.5802/wbln.38](https://doi.org/10.5802/wbln.38), [arXiv:1109.5248](https://arxiv.org/abs/1109.5248)&rbrack;


[[!redirects Fox pairings]]

