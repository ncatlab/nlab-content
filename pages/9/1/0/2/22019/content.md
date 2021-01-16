
### Finite homotopy (co)limits of spectra
  {#FiniteHomotopyLimitsOfSpectra}

\begin{proposition}
  \label{InSpectraHomotopyFiberSequencesAreHomotopyCofiberSequences}

A sequence of [[morphisms]] of [[spectra]] $E \longrightarrow F \longrightarrow G$ is a [[homotopy fiber sequence]] if and only if it is a [[homotopy cofiber sequence]]:

\begin{xymatrix@R=18pt}
  E 
  \ar[rr]_>>>{\ }="s1"
  \ar[dd]
    |-{ 
      \mathclap{\phantom{\vert^{\vert}}}
      \mathrm{fib} 
      \mathclap{\phantom{\vert_{\vert}}}
    }
    ^>>>{\ }="t1"
  &&
  \ast
  \ar[dd]
  &&
  E 
  \ar[rr]_>>>{\ }="s2"
  \ar[dd]^>>>{\ }="t2"
  &&
  \ast
  \ar[dd] 
  \\
  && & \Leftrightarrow
  \\
  F 
  \ar[rr]
  &&
  G
  &&
  F 
  \ar[rr]
   |-{
     \;\mathrm{cofib}\;
   }
  &&
  G
  %
  \ar@{=>}
    %^{ \mbox{\tiny\rm(po)} } 
    "s1"; "t1"
  \ar@{=>}
    %^{ \mbox{\tiny\rm(pb)} } 
    "s2"; "t2"
\end{xymatrix}

\end{proposition}
A **proof** is spelled out at _[[Introduction to Stable homotopy theory]]_ ([this Prop.](Introduction+to+Stable+homotopy+theory+--+1-1#HomotopyCofiberSequencesAreHomotopyFiberSequencesInSpectra), following [Lewis-May-Steinberger 86, chapter III, theorem 2.4](equivariant+stable+homotopy+theory#LewisMaySteinberger86)
)


In fact:

\begin{proposition}
  \label{HomotopyPullbacksOfSpectraAreHomotopyPushouts}

A [[homotopy coherent diagram|homotopy]]-[[commuting square]] in [[Spectra]] is a [[homotopy pullback]] if and only it is a [[homotopy pushout]].

\begin{xymatrix@R=18pt}
  E 
  \ar[rr]_>>>{\ }="s1"
  \ar[dd]^>>>{\ }="t1"
  &&
  H
  \ar[dd]
  &&
  E 
  \ar[rr]_>>>{\ }="s2"
  \ar[dd]^>>>{\ }="t2"
  &&
  H
  \ar[dd] 
  \\
  && & \Leftrightarrow
  \\
  F 
  \ar[rr]
  &&
  G
  &&
  F 
  \ar[rr]
  &&
  G
  %
  \ar@{=>}
    ^{ \mbox{\tiny\rm(po)} } "s1"; "t1"
  \ar@{=>}
    ^{ \mbox{\tiny\rm(pb)} } "s2"; "t2"
\end{xymatrix}


\end{proposition}

This follows from Prop. \ref{InSpectraHomotopyFiberSequencesAreHomotopyCofiberSequences} by the fact that [[Spectra]] is [[additive category|additive]] ([this Prop.](Introduction+to+Stable+homotopy+theory+--+1-1#TheStableHomotopyCategoryIsAdditive)). 

See also [arXiv:1906.04773, Prop. 6.2.11](https://arxiv.org/abs/1906.04773), [MO:q/132347](https://mathoverflow.net/q/132347/381).

\begin{remark}
  This property of Spectra (Prop. \ref{InSpectraHomotopyFiberSequencesAreHomotopyCofiberSequences}, Prop. \ref{HomotopyPullbacksOfSpectraAreHomotopyPushouts}) reflects one of the standard defining [[axioms]] on [[stable (∞,1)-categories]] (see [there](stable+infinity-category#Definition)) and on [[stable derivators]] (see [there](stable+derivator#Definition)).
\end{remark}
