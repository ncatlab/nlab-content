\tableofcontents

\section{Idea}

Recall that an [[elliptic curve]] $E$ is an [[abelian variety]]; in particular, its set of points admits a group structure. A point of $E$ is a torsion point if it is a [[torsion element]] of this group structure.

If $E$ is defined over a [[number field]] $F$, the [[Galois theory]] of $F$ interacts very well with the torsion points of $E$, as we describe below.

\section{Definition}

\begin{defn} Let $E$ be an [[elliptic curve]] over a field $F$, and let $l \geq 2$ be an integer. An _$l$-torsion point of $E$_ is a point $x$ of $E$ such that $l x = 0$, that is, $\underbrace{x + x + \cdots + x}_{l} = 0$ in the (abelian) group structure on (the set of points of) $E$, where $0$ denotes the identity element of the group structure (often taken to be the point at infinity). 

A _torsion point_ of $E$ is a point of $E$ which is an $l$-torsion point of $E$ for some integer $l \geq 2$.
\end{defn}    

\begin{rmk} For a fixed integer $l \geq 2$, the set of $l$-torsion points of $E$ assembles into an [[abelian group]] with respect to the group structure of $E$. The same is true of the set of all torsion points of $E$. \end{rmk}

\begin{notn} For a fixed integer $l \geq 2$, the set of $l$-torsion points of $E$ is often denoted $E[l]$. \end{notn}

\section{Splitting}

The following observation is used frequently when working with torsion points of an elliptic curve over a [[number field]].

\begin{proposition} Let $E$ be an elliptic curve defined over $\mathbb{Q}$, the [[rational number|rationals]]. Then for any integer $l \geq 2$, there is an [[isomorphism]] of [[abelian group|abelian groups]] $E[l] \cong \mathbb{Z} / l\mathbb{Z} \oplus \mathbb{Z} / l\mathbb{Z}$. \end{proposition}

\begin{rmk} \label{RemarkAutomorphismsOfTorsionPointsAsMatrixGroup} Thus if $l$ is a [[prime number|prime]], so that $\mathbb{Z} / l \mathbb{Z}$ is a [[field]] $\mathbb{F}_{l}$, we can think of the set of automorphisms of the abelian group $E[l]$ as the [[matrix group]], specifically the [[general linear group]], $GL_2\left( \mathbb{F}_{l} \right)$. \end{rmk}

\section{Galois theory}

Given an elliptic curve $E$ defined over a [[number field]] $F$, the following observation ties the Galois theory of $F$ to the torsion points of $E$. We shall denote the algebraic closure of $F$ by $\overline{F}$.

\begin{proposition} \label{PropositionGaloisGroupActsOnEllipticCurveAndItsTorsionPoints} Let $E$ be an elliptic curve defined over a [[number field]] $F$. Let $F'$ be an [[field extension|extension]] of $F$. The [[Galois group]] $Gal\left(F' / F \right)$ acts on all of (the set of points of) $E / F'$, the (abelian group of) torsion points of $E / F'$, and the (abelian group of) $l$-torsion points of $E / F'$ for any fixed integer $l \geq 2$, in the obvious way: given an automorphism $\sigma$ of $F'$ which fixes $F$, we send a point $x$ of $E / F'$ to $\sigma(x)$. \end{proposition}

\begin{rmk} The principal point is that given $\sigma$ and $x$ as in Proposition \ref{PropositionGaloisGroupActsOnEllipticCurveAndItsTorsionPoints}, one can check that $\sigma(x)$ is still a point of $E$, and is still an $l$-torsion point for some $l \geq 2$ if $x$ is. \end{rmk}

Given Remark \ref{RemarkAutomorphismsOfTorsionPointsAsMatrixGroup}, we can, as with any [[group action]], reformulate Proposition \ref{PropositionGaloisGroupActsOnEllipticCurveAndItsTorsionPoints} in the case of $l$-torsion points for a fixed prime $l \geq 2$ as follows. 

\begin{corollary} \label{CorollaryHomomorphismFromGaloisGroupToTorsionPoints} Let $l \geq 2$ be a [[prime number|prime]]. Let $E$ be an elliptic curve defined over a [[number field]] $F$. Let $F'$ be an [[field extension|extension]] of $F$. Then the application of automorphisms of $F'$ to points of $E$ determines a [[homomorphism|group homomorphism]] $Gal\left(F' / F\right) \rightarrow GL_2\left( \mathbb{F}_{l} \right)$. \end{corollary}

\begin{rmk} Given the homomorphism of Corollary \ref{CorollaryHomomorphismFromGaloisGroupToTorsionPoints}, we can take its kernel. This subgroup of $Gal\left( F' / F \right)$ determines, by [[Galois theory]], a [[field extension]] of $F$. Let us denote it by $K$. In fact, $K$ is simply the [[tensor product]] of $E[l]$ with $F$; from that point of view, we have demonstrated that this tensor product is a finite [[Galois extension]] of $F$. \end{rmk}
