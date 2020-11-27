
\begin{xymatrix}
    S^{2n-1}
    \ar@/^1.7pc/[drr]_-{\ }="s"
    \ar@/_1.7pc/[drr]^-{\ }="t"
    \\
    && 
    E_8
    %
    \ar@{=>}^-{
      \Sigma^{2n-1} \! \kappa
    } "s"; "t"
\end{xymatrix}

\begin{xymatrix}
   S^{2n-1}
   \ar[dd]_-{ f }
   \ar[rr]
   \ar@{}[ddrr]|-{
     \rotatebox[origin=c]{-45}{$\big\Downarrow$}
     \mbox{\tiny (po)}
   }
   &&
   \ast
   \ar[dr]
   \ar[dd]
   \\
   && &  
   \ast
   \ar[dd]^-{0}
   \\
   S^n
   \ar[dd]
   \ar[rr]
   \ar@{}[ddrr]|-{
     \rotatebox[origin=c]{-45}{$\big\Downarrow$}
     \mbox{\tiny (po)}
   }
   \ar@/_.7pc/[drrr]|<<<<<<<{ \;\Sigma^4 1\; }|>>>>>>>{ {\phantom{AA}} \atop {\phantom{AA}} }
   &&
   C_f
   \ar[dd]
   \ar@{-->}[dr]^-{ c }
   \\
   && &
   E_n
   \ar[dd]^-{ (-)^{2_{\cup}} }
   \\
   \ast
   \ar@/_.7pc/[drrr]|-{ \;0\; }
   \ar[rr]
   &&
   S^{2n}
   \ar@{-->}[dr]|-{ 
     \mathclap{\phantom{\vert^{\vert}}}
     \Sigma^{2n} \kappa 
     \mathclap{\phantom{\vert_{\vert}}}
   }
   \\
   && & 
   E_{2n}
\end{xymatrix}



$$
  \array{
    S^7 
      &\longrightarrow& 
    \ast
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    S^4 
    &\longrightarrow& 
    \mathbb{H}P^2
    &\longrightarrow& 
    E_4
    \\
    \big\downarrow
    &&
    \big\downarrow
    &&
    \big\downarrow
    \\
    \ast 
    &\longrightarrow& 
    S^8
    &\longrightarrow& 
    E_8
  }
$$

\linebreak 

\linebreak

\begin{tikzcd}
X \arrow[rdd, "{(id,f)}", bend right] \arrow[rrrd, "f", bend left] \arrow[rd, "\exists ! j", dashed] &                                                                                                                                                          &                                            &                                         \\
                                                                                                     & Z \arrow[d, "\pi_1^Z"] \arrow[r, "\pi_0^Z"] \arrow[dr, phantom, "\lrcorner", very near start]                                                            & Y^I \arrow[d, "e"]                         & Y \arrow[l, "c"'] \arrow[ld, "\Delta"'] \\
                                                                                                     & X \times Y \arrow[r, "f \times id"] \arrow[d, "\pi_0^{X \times Y}"] \arrow[ld, "\pi_1^{X \times Y}"']  \arrow[dr, phantom, "\lrcorner", very near start] & Y \times Y \arrow[d, "\pi_0^{Y \times Y}"] &                                         \\
Y                                                                                                    & X \arrow[r, "f"]                                                                                                                                         & Y                                          &                                        
\end{tikzcd}