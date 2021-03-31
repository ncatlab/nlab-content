+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


\tableofcontents

\section{Idea}

The notion of _initial Θ-data_ or _initial theta-data_ was introduced by [[Shinichi Mochizuki]] in §3 of [Inter-Universal Teichmüller theory I](#MochizukiIUTTI) as the starting point for [[inter-universal Teichmüller theory]]. In essence, initial Θ-data consists of an [[elliptic curve]] $E$ over a [[number field]] $F$ such that the [[Galois theory]] of $F$ and the geometry of $E$ interact well.   

\section{Notation}

In order to understand the definition, we recall a little notation. 

1. Given a [[field]] $F$, the notation $E / F$ means that $E$ is a [[field extension]] of $F$. 

1. Given a [[field]] $F$, the notation $\overline{F}$ denotes an [[algebraic closure]] of $F$.  

1. Given a [[field]] $F$ and a once-punctured [[elliptic curve]] $X$ over $F$ (see below for a precise definition), the notation $F_{mod}$ denotes the [[field of moduli]] of $X$. 

1. Given a field $F$, an [[elliptic curve]] $E$ over $F$, and a [[prime number|prime]] $l \geq 2$, let us write $\phi_l: Gal\left(\overline{F} / F\right) \rightarrow GL_{2}\left( \mathbb{F}_{l} \right)$ for the [[homomorphism|group homomorphism]] from the [[Galois group]] of $F$ to the [[general linear group]] of 2x2 invertible matrices with values in $\mathbb{F}_{l}$ determined by the $l$-torsion points of $E$ (see [[torsion points of an elliptic curve]] for details of this homomorphism).

1. Given a field $F$ and an [[elliptic curve]] $E$ over $F$, 
 the notation $K_F$ denotes the [[field]], a [[Galois extension|finite Galois extension]] of $F$, corresponding (by [[Galois theory]]) to the kernel of $\phi_l$.

1. Given a [[number field]] $F$, the notation $\mathbb{V}(F)$ denotes the set of [[absolute value|valuations]] on $F$, both archimedean and non-archimedean. 

1. Given a [[number field]] $F$ and a [[absolute value|valuation]] $v \in \mathbb{V}\left(F\right)$ on $F$, the notation $F_{v}$ denotes the [[completion of a field at an absolute value|completion]] of $F$ with respect to $v$. 

\section{Definition}

The following is Definition 3.1 in [Inter-Universal Teichmüller theory I](#MochizukiIUTTI), on pg.61 (currently).

\begin{defn} _Initial Θ-data_ is a 7-tuple $(\overline{F} / F, X_{F}, l, \underline{C}_{K}, \underline{\mathbb{V}}, \mathbb{V}^{bad}_{mod}, \underline{\epsilon})$ consisting of the following data.

1. A [[number field]] $F$ such that $\sqrt{-1} \in F$. In other words, we have a field extension of the [[quotient ring]] $\mathbb{Q}[X] / (X^{2} + 1)$, which itself is a field because $X^{2} + 1$ is irreducible: see [[field extension]] for more details on this.

1. A [[scheme]] $X_{F}$ which is obtained by removing a closed point from an [[elliptic curve]] $E_{F}$ over $F$. The scheme structure on $X_{F}$ is that inherited from $E_{F}$ by virtue of the fact that $X_{F}$ is an open subset of (the underlying topological space of) $E_{F}$, as described at [[open subscheme]]. We require that $X_{F}$ satisfies certain conditions: TODO.

1. A [[prime number|prime]] $l \geq 5$ such that $\phi_l$ as defined above contains $SL_2\left( \mathbb{F}_{l} \right)$ in its [[image]].

1. The field extension $F / F_{mod}$ is [[Galois extension|Galois]].

1. A [[subset]] $\mathbb{V}$ of $\mathbb{V}\left(K_F\right)$ which is [[bijection|isomorphic]] to $\mathbb{V}\left(F_{mod}\right)$. In other words, observing that $F_{mod}$ is a sub-field of $K_F$, a [[section]] of the map $V\left( K_F \right) \rightarrow V\left( F_{mod} \right)$ determined by the inclusion of $F_{mod}$ into $K_F$. 

(TO BE CONTINUED)

\end{defn}

\section{References}

* {#MochizukiIUTTI} [[Shinichi Mochizuki]], _Inter-Universal Teichmüller Theory I: Construction Of Hodge Theaters_, (2017). [Link to paper](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20I.pdf)

* [[Taylor Dupuy]], Anton Hilado, _The Statement of Mochizuki's Corollary 3.12, Initial Theta Data, and the First Two Indeterminacies_, arXiv:[2004.13228](https://arxiv.org/abs/2004.13228)

* [[Taylor Dupuy]], _Initial Theta Data_, video series.

   * [Some Prerequisites, and The Easy Part of Initial Theta Data](https://youtu.be/FTv5TnXR1HQ)
   * [Transvections](https://youtu.be/4QEntmb2xyE)
   * [Local Global l-torsion Compatibility](https://youtu.be/gcuqYsrCR5A)
   * [Existence and Examples](https://youtu.be/sUGXfC8LwwI)


[[!redirects Initial Θ-data]]
