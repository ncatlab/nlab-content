* [[objects]] are [[endomorphisms]] (necessarily [[automorphisms]]) in $\mathcal{X}$

\begin{tikzcd}
  {}
  \ar[
    out=180-50, 
    in=50, 
    looseness=5, 
    "g"
  ]
  x
\end{tikzcd}

* [[morphisms]] are [[conjugations]] of such automorphisms $g$ by morphisms (necessarily: [[isomorphisms]]) $f$ in $\mathcal{X}$:

\begin{tikzcd}
  \ar[
    out=180-50, 
    in=50, 
    looseness=5, 
    "g"
  ]
  x
  \ar[rr, "f"]
  &&
  y
  \ar[
    out=180-50, 
    in=50, 
    looseness=5, 
    "f \circ g \circ f^{-1}"
  ]
\end{tikzcd}
