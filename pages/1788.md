
| [[singularity]] | [[mass]] |
|----|-----|
| $2 D_4$ | $8$ | 
| $2 D_6$ | $12$ |
| $2 D_{8}$ | $16$ | 
| $2 D_{10}$ | $20$ | 
| $2 D_{12}$ | $24$ | 
| $2 D_{14}$ | $28$ | 
| $2 D_{16}$ | $32$ | 



***

Let 

\begin{tikzcd}
  R_{\mathbb{C}}(-)
  \arrow[r, phantom, "\colon" marking]
  &
  \mathrm{FinGrp}^{\mathrm{op}}
  \arrow[rr]
    &&
  \mathrm{CRing}
  \\
  &
  G
  \arrow[rr, phantom, "\mapsto" marking]
  \arrow[d, "\phi"]
  &&
  R_{\mathbb{C}}\big(G\big)
  \\
  &
  G'
  \arrow[rr, phantom, "\mapsto" marking]
  &&
  R_{\mathbb{C}}\big(G'\big)
  \arrow[u, "\phi^\ast"]
\end{tikzcd}

be the [[functor]] from the [[opposite category]] of the [[category]] [[FinGrp]] of [[finite groups]] to the [[category]] [[CRing]] of [[commutative rings]], which sends a group to its [[representation ring]] and a [[group homomorphism]] to the corresponding [[restricted representation]]-assignment.

\begin{centre}

\begin{tikzpicture}

\fill (0,0) circle[radius=2em];

\end{tikzpicture}

\end{centre}

An XY-Matrix diagram:

\begin{centre}

\xymatrix{A \ar[r] \ar[dr] & B \ar[d] \\ & C}

\end{centre}