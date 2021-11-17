
[[separating family#fibered|fibered separating family]]

\begin{tikzcd}[column sep={between origins, 50pt}]
    &[-10pt]
    &[-10pt]
    &&[+30pt]
    P \times \Gamma
    \ar[d, shift right=2.5pt, "\mathrm{pr}_1"{swap}]
    \ar[d, shift left=2.5pt, "\rho"]
    \ar[rr]
    &&
    \big(
      P \times_X P'
    \big) \times \Gamma
    \ar[d, shift right=2.5pt, "\mathrm{pr}_1"{swap}]
    \ar[d, shift left=2.5pt, "\rho"]
    \\
    &&&&
    P 
    \ar[d]
    \ar[rr, "{ (\mathrm{id},f) }"{description}]
    &&
    P \times_X P'
    \ar[d]
    \\
    P
      \ar[out=180-66, in=66, looseness=3.5, "\scalebox{.77}{$\,\mathclap{
        G
      }\,$}"{description},shift right=1]
    \ar[rr, "f"]
    \ar[dr]
    &
    &
    P'
      \ar[out=180-66, in=66, looseness=3.5, "\scalebox{.77}{$\,\mathclap{
        G
      }\,$}"{description},shift right=1]
    \ar[dl]
    &\leftrightarrow&
    P/G
    \ar[rr, dashed]
    \ar[dr, -, shift left=1pt]
    \ar[dr, -, shift right=1pt]
    &&
    \big(
      P
        \times_{X}
      P'
    \big) / G
    \ar[dl]
    \\
    &
    X
    &
    &&
    &
    X
\end{tikzcd}




\begin{tikzcd}
  G_{\mathrm{e}}
  \ar[r, -, shift left=1pt]
  \ar[r, -, shift right=1pt]
  \ar[d, hook]
  &
  G_{\mathrm{e}}
  \\
  G
  \ar[ur, dashed]
\end{tikzcd}

\begin{tikzcd}
  G_{\mathrm{e}}
  \ar[r, hook, "i"{below}]
  &
  G
  \ar[r, ->>]
  \ar[l, bend right=30, "p"{below}]
  &
  G/G_{\mathrm{e}}
\end{tikzcd}



$$
  \delta_i^\ast F
  \;=\;
  d A_i
$$

$$
  a_{i j} 
  \;\coloneqq\;
  \delta_j^\ast A_i
  -
  \delta_i^\ast A_j
$$

$$
  d a_{i j}
  \;=\;
  \delta_j^\ast \delta_i^\ast F
  -
  \delta_i^\ast \delta_j^\ast F
  \;=\;
  0
$$

\linebreak

$$
  \delta_i a_{j k}
  + 
  \cdots
  \;=\;
  0
$$

$$
  (0, a_{i j})
  + 
  D (A_i, 0)
  \;=\;
  ( \underset{i_0}{\sum}  (d \rho_{i_0}) \wedge a_{i_0 i} )
$$

$$
  A_i
  \;\coloneqq\;
  \underset{i_0}{\sum}
  \rho_{i_0} \cdot a_{i_0 i}
$$

$$
  \delta_j^\ast A_i
  -
  \delta_i^\ast A_j
  \;=\;
  \underset{i_0}{\sum}
  (d \rho_{i_0}) \wedge a_{i j}  
$$


$$
  d A_i
  \;=\;
  \underset{i_0}{\sum}
  (d \rho_{i_0}) a_{i_0 i}
$$


\linebreak

$$
  \underset{i_0}{\sum} \rho_{i_0} \cdot a_{i_0 i}
  -
  \underset{i_0}{\sum} \rho_{i_0} \cdot a_{i_0 j}
  \;=\;
  \underset{i_0}{\sum} \rho_{i_0} \cdot a_{i j}  
  \;=\;
  a_{i j}
$$

