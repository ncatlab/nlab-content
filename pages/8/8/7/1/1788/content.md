

\begin{tikzcd}[sep=large]
  D 
    \ar[
      rr,
      equals
    ] 
    \ar[
      dd,
      equals
    ]
    &&  
  D
  \ar[
    dd,
    dashed,
    "{  
      \mathrm{trans}^{ \mathrm{Id} \to \mathcal{E} }_D
      \,=\,
      \mathrm{ret}^{\mathcal{E}}_D
    }"{description}
  ]
  \\
  \\
  D
  \ar[
    rr,
    "{
      \mathrm{ret}^{\mathcal{E}}_D
    }"{swap}
  ]
  &&
  \mathcal{E}(D)
\end{tikzcd}





\begin{tikzcd}
  D 
  \ar[
    rr,
    "{
      \mathrm{ret}^{\mathcal{E}}_D
    }"
  ]
  \ar[
    dd,
    equals
  ]
  &&
  \mathcal{E}(D)
  \ar[
    rr,
    "{
      \mathrm{ret}^{\mathcal{E}}_{\mathcal{E}(D)}
    }"
  ]
  &&
  \mathcal{E}\big(
    \mathcal{E}(D)
  \big)
  \ar[
    dd,
    "{ 
      \mathrm{join}^{\mathcal{E}}_D
    }"
  ]
  \\
  \\
  D
  \ar[
    rrrr,
    "{
      \mathrm{ret}^{\mathcal{E}}_{D}
    }"{swap}
  ]
  &&
  &&
  \mathcal{E}(D)
\end{tikzcd}


