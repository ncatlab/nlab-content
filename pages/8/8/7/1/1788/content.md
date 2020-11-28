
* Khaled Abdel-Khalek, _The Super P-Brane Scan and S Duality_ ([arXiv:hep-th/9607180v1](https://arxiv.org/abs/hep-th/9607180v1))

* [[Ergin Sezgin]], _Super Yang-Mills in $(11,3)$ Dimensions_, 	Phys.Lett. B403 (1997) 265-272 ([arXiv:hep-th/9703123](https://arxiv.org/abs/hep-th/9703123))


* Itzhak Bars, _A case for 14 dimensions_, Phys. Lett. B403 (1997) 257-264 ([arXiv:hep-th/9704054](https://arxiv.org/abs/hep-th/9704054))

* [[Itzhak Bars]], _Duality Covariant Type IIB Supersymmetry and Nonperturbative Consequences_, Phys. Rev. D 56, 7954 (1997) ([arXiv:hep-th/9706185](https://arxiv.org/abs/hep-th/9706185))

* I. Rudychev, [[Ergin Sezgin]], P. Sundell, _Supersymmetry in Dimensions Beyond Eleven_, Nucl. Phys. Proc. Suppl. 68 (1998) 285-294 ([arXiv:hep-th/9711127](https://arxiv.org/abs/hep-th/9711127))

* [[Hitoshi Nishino]], _Supersymmetric Yang-Mills Theories in $D \geq 12$_, Nucl.Phys. B523 (1998) 450-464 ([arXiv:hep-th/9708064](https://arxiv.org/abs/hep-th/9708064))

* [[Michael Rios]], [[Alessio Marrani]], [[David Chester]], _The Geometry of Exceptional Super Yang-Mills Theories_, Phys. Rev. D 99, 046004 (2019) ([arXiv:1811.06101](https://arxiv.org/abs/1811.06101))







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