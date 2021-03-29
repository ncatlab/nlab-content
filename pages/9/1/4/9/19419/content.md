

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--



[[!redirects Initial Θ-data]]


#Contents#
* table of contents
{:toc}

## Idea

The notion of _initial Θ-theta data_ was introduced by [[Shinichi Mochizuki]] in §3 of [Inter-Universal Teichmüller theory I](#MochizukiIUTTI) as the starting point for [[inter-universal Teichmüller theory]].

## Notation

In order to understand the definition, we recall a little notation. 

1) Given a [[field]] $F$, the notation $E / F$ means that $E$ is a [[field extension]] of $F$. 

2) Given a [[field]] $F$, the notation $\overline{F}$ denotes an [[algebraic closure]] of $F$.  

3) Given a field $F$ and a once-punctured [[elliptic curve]] $E$ over $F$ (see below for a precise definition), the notation $F_{mod}$ denotes the [[field of moduli]] of $E$. 

## Definition

The following is Definition 3.1 in [Inter-Universal Teichmüller theory I](#MochizukiIUTTI), on pg.61 (currently).

+-- {: .num_defn}
###### Definition

_Initial Θ-data_ is a 7-tuple $(\overline{F} / F, X_{F}, \ell, \underline{C}_{K}, \underline{\mathbb{V}}, \mathbb{V}^{bad}_{mod}, \underline{\epsilon})$ given the following data.

1. A [[number field]] $F$ such that $\sqrt{-1} \in F$. In other words, we have a field extension of the [[quotient ring]] $\mathbb{Q}[X] / (X^{2} + 1)$, which itself is a field because $X^{2} + 1$ is irreducible: see [[field extension]] for more details on this.

1. A [[scheme]] $X_{F}$ which is obtained by removing a closed point from an [[elliptic curve]] $E_{F}$ over $F$. The scheme structure on $X_{F}$ is that inherited from $E_{F}$ by virtue of the fact that $X_{F}$ is an open subset of (the underlying topological space of) $E_{F}$, as described at [[open subscheme]]. We require that $X_{F}$ satisfies certain conditions: TODO.

1. A [[prime number|prime]] $l \geq 5$ satisfying certain conditions: TODO

1. The field extension $F / F_{mod}$ is [[Galois extension|Galois]].

(TO BE CONTINUED)

=--

## References

* {#MochizukiIUTTI} [[Shinichi Mochizuki]], _Inter-Universal Teichmüller Theory I: Construction Of Hodge Theaters_, (2017). [Link to paper](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20I.pdf)

* [[Taylor Dupuy]], Anton Hilado, _The Statement of Mochizuki's Corollary 3.12, Initial Theta Data, and the First Two Indeterminacies_, arXiv:[2004.13228](https://arxiv.org/abs/2004.13228)