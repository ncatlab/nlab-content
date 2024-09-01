
$$
  I
    \,\,\,\colon\,\,\,
  B
$$

$A \;\;\; B$

[[RibbonAxiomsToDiagramMoves.jpg:file]]

\begin{imagefromfile}
    "file_name": "RibbonAxiomsToDiagramMoves.jpg",
    "float": "right",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

\begin{tikzcd}
    \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \times
    T_{\!{}_{\mathrm{odd}}}
    \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \ar[
      r,
      hook
    ]
    \ar[
      rr,
      rounded corners,
      to path={
           ([yshift=+00pt]\tikztostart.north)  
        -- ([yshift=+10pt]\tikztostart.north)  
        -- node[yshift=5pt] {
           \scalebox{.7}{$
             \mathrm{act}
           $}
        }
           ([yshift=+10pt]\tikztotarget.north)  
        -- ([yshift=+00pt]\tikztotarget.north)  
      }
    ]
    &
    T_{\!{}_{\mathrm{odd}}}
    \times
    T_{\!{}_{\mathrm{odd}}}
    \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \ar[
      r,
      "{ \mathrm{prd}_\ast }"
    ]
    &    
    T_{\!{}_{\mathrm{odd}}}
    \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
\end{tikzcd}


\begin{tikzcd}
    C^\infty
    \big(
      \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \big)
    \,\widehat{\otimes}\,
    \Omega^\bullet_{\mathrm{dR}}
    \big(
      \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \big)
    \ar[
      r,
      <<-
    ]
    \ar[
      rr,
      <-,
      rounded corners,
      to path={
           ([yshift=+00pt]\tikztostart.north)  
        -- ([yshift=+08pt]\tikztostart.north)  
        -- node[yshift=4pt]
           {
             \scalebox{.7}{$
               \mathrm{act}^\ast
             $}
           }
           ([yshift=+08pt]\tikztotarget.north)  
        -- ([yshift=+00pt]\tikztotarget.north)  
      }
    ]
    &
    \Omega^\bullet_{\mathrm{dR}}
    \big(
      \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \big)
    \,\widehat{\otimes}\,
    \Omega^\bullet_{\mathrm{dR}}
      \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \big)
    \ar[
      r,
      <-,
      "{ \mathrm{prd}^{\mathrlap{\ast}} }"
    ]
    &
    \Omega^\bullet_{\mathrm{dR}}
    \big(
      \mathbb{R}^{1,d\,\vert\,\mathbf{N}}
    \big)
\end{tikzcd}
