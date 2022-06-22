

\begin{tikzcd}[
  sep=small
]
    &
    A^\tau(\mathrm{X}_{b_2})
    \ar[
      ddr,
      "{\sim}"{sloped},
      shorten=-2pt
    ]
    \\[-27pt]
    &&&
    \mathrm{X}
    \ar[
      dddd,
      "{p_{\mathrm{X}}}"
    ]
    \ar[
      dr,
      "{\tau}"{swap, xshift=1pt}
    ]
    \ar[
      rr,
      dashed
    ]
    &&
    \mathrm{A} \times_G E G
    \ar[
      dl,
      shorten=-2pt,
      "{
        p_{\mathrm{A} \times_G E G}
      }"
    ]
    \\[-12pt]
    A^\tau(\mathrm{X}_{b_1})
    \ar[
      uur,
      shorten=-2pt,
      "{
        \sim
      }"{sloped}
    ]
    \ar[
      rr,
      "{\sim}"{swap}
    ]
    &&
    A^\tau(\mathrm{X}_{b_3})
    &&
    B G
    \ar[
      dddd,
      "{
        p_{B G}
      }"
    ]
    \\
    \\
    &
    \{b_2\}
    \ar[
      ddr,
      "{
        [\gamma_{23}]
      }"
    ]
    \\[-27pt]
    &&&
    \mathrm{B}
    \ar[
      dr,
      "{p_{\mathrm{B}}}"{swap}
    ]
    \\[-12pt]
    \{b_1\}
    \ar[
      uur,
      "{
        [\gamma_{12}]
      }"
    ]
    \ar[
      rr,
      "{
        [\gamma_{23} \circ \gamma_{12}]
      }"{swap}
    ]
    &&
    \{b_3\}
    &
    &
    \ast
\end{tikzcd}


$$
  \begin{array}{ll}
    kTop
    \Big(
      U
      ,\,
      (p_{B G})_\ast
      Map
      \big(
        (X_b, \tau_b)
        ,\,
        (A \times_G E G, p_{A \times_G E G})
      \big)
    \Big)
    \\
    \;\simeq\;
    kTop_{/ B G}
    \Big(
      (p_{B G})^\ast
      U
      ,\,
      Map
      \big(
        (X_b, \tau_b)
        ,\,
        (A \times_G E G, p_{A \times_G E G})
      \big)
    \Big)
    \\
    \;\simeq\; 
    kTop_{/ B G}
    \Big(
      \big(
        (p_{B G})^\ast U
      \big)
      \times
      (X_b, \tau_b)
      ,\,
      (A \times_G E G, p_{A \times_G E G})
    \Big)
    \\
    \;\simeq\; 
    kTop_{/ B G}
    \Big(
      (\tau_b)_!
      (U \times X_b, pr_{X_b})
      ,\,
      (A \times_G E G, p_{A \times_G E G})
    \Big)
    &
    \text{by (eq:APullback)}
    \\
    \;\simeq\; 
    kTop_{/ X_b}
    \Big(
      (U \times X_b, pr_{X_b})
      ,\,
      (\tau_b)^\ast
      (A \times_G E G, p_{A \times_G E G})
    \Big)
    \\
    \;\simeq\; 
    kTop
    \big(
      U \times X_b
      ,\,
      (\tau_b)^\ast (A \times_G E G)
    \big)
    \underset{
      kTop
      \big(
        U \times X_b
        ,\,
        X_b
      \big)
    }{\times}
    \big\{
      pr_{X_b}
    \big\}
    \\
    \;\simeq\; 
    kTop
    \Big(
    U 
    ,\,
    Map
    \big(
      X_b
      ,\,
      (\tau_b)^\ast (A \times_G E G)
    \big)
    \underset{
      Map
      \big(
        X_b
        ,\,
        X_b
      \big)
    }{\times}
    \big\{
      \mathrm{id}_{X_b}
    \big\}
    \Big)
    \\
    \;\simeq\;
    kTop
    \Big(
      U
      ,\,
      \Gamma_X
      \big(
        (\tau_b)^\ast
        ( A \times_G E G )
      \big)
    \Big)
  \end{array}
$$

\[
  \label{APullback}
  \array{
    U \times X_b
    &\overset{pr_{X_b}}{\longrightarrow}&
    X_b
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow\mathrlap{{}^{\tau_b}}
    \\
    U \times B G
    &\underset{pr_{B G}}{\longrightarrow}&
    B G
  }
\]

