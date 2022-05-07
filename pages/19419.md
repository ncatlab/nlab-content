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
 the notation $K_E$ denotes the [[field]], a [[Galois extension|finite Galois extension]] of $F$, corresponding (by [[Galois theory]]) to the kernel of $\phi_l$.

1. Given a [[number field]] $F$, the notation $\mathbb{V}(F)$ denotes the set of [[absolute value|valuations]] on $F$, both archimedean and non-archimedean. 

1. Given a [[number field]] $F$ and a [[absolute value|valuation]] $v \in \mathbb{V}\left(F\right)$ on $F$, the notation $F_{v}$ denotes the [[completion of a field at an absolute value|completion]] of $F$ with respect to $v$. 

\section{Definition}

The following is Definition 3.1 in [Inter-Universal Teichmüller theory I](#MochizukiIUTTI), on pg.61 (currently).

\begin{defn} _Initial Θ-data_ is a 7-tuple $(\overline{F} / F, X_{F}, l, \underline{C}_{K}, \underline{\mathbb{V}}, \mathbb{V}^{bad}_{mod}, \underline{\epsilon})$ consisting of the following data.

1. A [[number field]] $F$ such that $\sqrt{-1} \in F$. In other words, we have a field extension of the [[quotient ring]] $\mathbb{Q}[X] / (X^{2} + 1)$, which itself is a field because $X^{2} + 1$ is irreducible: see [[field extension]] for more details on this.

1. A [[scheme]] $X_{F}$ which is obtained by removing a closed point from an [[elliptic curve]] $E_{F}$ over $F$. The scheme structure on $X_{F}$ is that inherited from $E_{F}$ by virtue of the fact that $X_{F}$ is an open subset of (the underlying topological space of) $E_{F}$, as described at [[open subscheme]]. We require that $X_{F}$ satisfies certain conditions: TODO.

1. A [[prime number|prime]] $l \geq 5$ such that $\phi_l$ as defined above contains $SL_2\left( \mathbb{F}_{l} \right)$ in its [[image]].

1. The field extension $F / F_{mod}$ is [[Galois extension|Galois]].

1. A [[subset]] $\underline{\mathbb{V}}$ of $\mathbb{V}\left(K_E\right)$ which is [[bijection|isomorphic]] to $\mathbb{V}\left(F_{mod}\right)$. In other words, observing that $F_{mod}$ is a sub-field of $K_E$, a [[section]] of the map $V\left( K_E \right) \rightarrow V\left( F_{mod} \right)$ determined by the inclusion of $F_{mod}$ into $K_E$. 

(TO BE CONTINUED)

\end{defn}

\section{Examples of the kind in IUTT}

Only one family of examples of initial Θ-data is given in the IUTT series of papers, pertaining directly to the [[abc conjecture]]. These examples are described in Corollary 2.2 of [IUTT IV](#IUTTIV). The language of stacks is used, but it seems possible to construct the examples without this. 

We shall assume that we have defined the notion of a _compactly bounded_ subset of $\overline{\mathbb{Q}}$, the algebraic closure of $\mathbb{Q}$ (namely the [[algebraic numbers]]). This notion is due to Mochizuki. 

\begin{defn} A _Mochizuki elliptic curve_ $E$ is one of the form $y^{2} = x(x-1)(x - \lambda)$ for some $\lambda \in \mathbb{Q}$ satisfying the following conditions:

1. $\lambda$ belongs to a compactly bounded subset $K_V$ of $\overline{\mathbb{Q}}$ with certain properties (omitted here for the moment);

1. $\lambda$ belongs to an [[field extension|extension]] of $\mathbb{Q}$ of degree less than or equal to a given positive integer $d$ (the choice of which comes from the statement of the [[abc conjecture]]);

1. $\lambda$ does not belong to a certain subset of $K_V$, denoted $\mathfrak{Crc}_{d}$, where $d$ is as in 2., which Mochizuki constructs (details omitted for the moment here too);

1. it is defined over a number field $F$ which is isomorphic to that obtained by beginning with the minimal field of definition of $E$ (regarded as defined over $\overline{\mathbb{Q}}$ for example) and then adjoining the fields of definition of the $30$-torsion points, that is, the $2$-torsion, $3$-torsion, and $5$-torsion points, as well as adjoining $\sqrt{-1}$;

1. there is a prime $l \geq 5$ satisfying certain properties for which $E$ does not admit a sub-group scheme which as a group is isomorphic to the [[cyclic group]] $\mathbb{Z} / l \mathbb{Z}$. 

\end{defn}

\begin{rmk} The first part of Corollary 2.2 in [IUTT IV](#IUTTIV) precisely concerns the construction, given $K_{V}$ (whose construction with the required properties is standard), of $\mathfrak{Crc}_{d}$. The properties of $\mathfrak{Crc}_{d}$ are such that can one apply the theory of IUTT to deduce that the [[abc conjecture]] holds. \end{rmk}

\begin{rmk} Given a Mochizuki elliptic curve $E$, one can show that one can construct initial Θ-data whose elliptic curve is $E$. TODO: details. \end{rmk} 

\section{References}

* {#MochizukiIUTTI} [[Shinichi Mochizuki]], _Inter-Universal Teichmüller Theory I: Construction Of Hodge Theaters_, (2017). [Link to paper](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20I.pdf)

* {#IUTTIV} [[Shinichi Mochizuki]], _Inter-universal Teichmüller theory IV, Log-volume computations and set-theoretic foundations_ (2012) ([pdf](http://www.kurims.kyoto-u.ac.jp/~motizuki/Inter-universal%20Teichmuller%20Theory%20IV.pdf))

* [[Taylor Dupuy]], Anton Hilado, _The Statement of Mochizuki's Corollary 3.12, Initial Theta Data, and the First Two Indeterminacies_, arXiv:[2004.13228](https://arxiv.org/abs/2004.13228)

* [[Taylor Dupuy]], _Initial Theta Data_, video series.

   * [Some Prerequisites, and The Easy Part of Initial Theta Data](https://youtu.be/FTv5TnXR1HQ)
   * [Transvections](https://youtu.be/4QEntmb2xyE)
   * [Local Global l-torsion Compatibility](https://youtu.be/gcuqYsrCR5A)
   * [Existence and Examples](https://youtu.be/sUGXfC8LwwI)


[[!redirects Initial Θ-data]]
