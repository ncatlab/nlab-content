$i \boxslash p$

\begin{tikzcd}[column sep=large]
    \Gamma_X
    \;\;\;
    \colon
    &[-40pt]
    \mathbf{H}_{/X}
    \ar[
      rr,
      phantom,
      shift left=10+10pt,
      "{\scalebox{.7}{$\bot$}}"
    ]
    \ar[
      rr,
      phantom,
      shift left=-10+10pt,
      "{\scalebox{.7}{$\bot$}}"
    ]
    \ar[
      rr,
      shift left=20+10pt,
      "{ \sum_X }"{description}
    ]
    \ar[
      rr,
      shift left=-20+10pt,
      "{ \prod_X }"{description}
    ]
    &&
    \mathbf{H}
    \ar[
      ll,
      shift right=+10pt,
      "{ X \times (-) }"{description}
    ]
    \ar[
      rr,
      phantom,
      shift left=10+10pt,
      "{\scalebox{.7}{$\bot$}}"
    ]
    \ar[
      rr,
      phantom,
      shift left=-10+10pt,
      "{\scalebox{.7}{$\bot$}}"
    ]
    \ar[
      rr,
      shift left=20+10pt,
      "{ \mathrm{Shp} }"{description},
      "{\mathclap{\times}}"{description, pos=0}
    ]
    \ar[
      rr,
      shift left=-20+10pt,
      "{ \mathrm{Pnts} }"{description}
    ]
    &&
    \mathrm{Grp}_\infty
    \ar[
      ll,
      hook',
      shift right=+10pt,
      "{ \mathrm{Disc} }"{description}
    ]
    &[-40pt]
    \colon
    \;\;\;
    \mathrm{LConst}_X
\end{tikzcd}


a $\sigma$ a

$$
  \begin{aligned}
    \infty Grpd
    \big( 
      B 
      ,\, 
      \Gamma_X \circ LConst_X(A)  
    \big)
    & 
    \;\simeq\;
    \infty Grpd
    \big( 
      B 
      ,\, 
      \Gamma_X (X \times A)  
    \big)
    \\
    & \;\simeq\;
    \mathbf{H}_{/X}
    \big( 
      X \times B
      ,\, 
      X \times A
    \big)
    \\
    & \;\simeq\;
    \mathbf{H}
    \big( 
      X \times Disc(B)
      ,\, 
      Disc(A)
    \big)    
    \\
    & \;\simeq\;
    \mathbf{H}
    \big( 
      Shp( X ) \times Disc(B)
      ,\, 
      Disc(A)
    \big)    
  \end{aligned}
$$