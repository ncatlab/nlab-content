

  $$
    \underset{
      \sigma \in Sym(n)
    }{
      \sum
    }
    e^{ \beta \cdot \left\vert Cycles(\sigma) \right\vert }
    \;=\;
    \underoverset    
      {k = 0}
      {n-1}
      {\prod}
    \big(
      e^{\beta} + k
    \big)
    \,.
  $$

\linebreak

\linebreak

$$
  \begin{aligned}
    \underoverset    
      {k = 0}
      {n-1}
      {\prod}
    \big(
      e^{\beta} - k
    \big)
    & 
    \;=\;
    (-1)^n
    \underoverset    
      {k = 0}
      {n-1}
      {\prod}
    \big(
      - e^{\beta} + k
    \big)
    \\
    & 
    \;=\;
    (-1)^n
    \underset{
      \sigma \in Sym(n)
    }{\sum}
    (-e^\beta)^{\#\left\vert Cycles(\sigma)\right\vert}
    \\
    & \;=\;
    \underset{
      \sigma \in Sym(n)
    }{\sum}
    (-1)^{n - \#\left\vert Cycles(\sigma)\right\vert}
    (e^\beta)^{\#\left\vert Cycles(\sigma)\right\vert}
    \\
    & \;=\;
    \underset{
      \sigma \in Sym(n)
    }{\sum}
    (-1)^{\#\left\vert EvenCycles(\sigma)\right\vert}
    (e^\beta)^{\#\left\vert Cycles(\sigma)\right\vert}
    \\
    & \;=\;
    \underset{
      \sigma \in Sym(n)
    }{\sum}
    sgn(\sigma)
    (e^\beta)^{\#\left\vert Cycles(\sigma)\right\vert}
  \end{aligned}
$$



[[topos|$x$]]

\begin{example}\label{CayleyDistanceKernelOnSym3}
**(Cayley distance kernel on Sym(4))**

Similar analysis shows that the eigenvalues of the Cayley distance kernel $e^{- \beta \cdot d_C}$ on $Sym(4)$ are the following:

$$
  \array{
    eigenvalue & multiplicity
    \\
    e^{-3 \beta}
    \big(
      \;
      + (e^{\beta})^3 + 6 (e^{\beta})^2 + 11 (e^{\beta}) + 6
      \;
    \big)
    & 
    1
    \\
    e^{-3 \beta}
    \big(
      \;
      + (e^{\beta})^3 - 6 (e^{\beta})^2 + 11 (e^{\beta}) - 6
      \;
    \big)
    &
    1
    \\
    e^{-3 \beta}
    \big(
      \;
      + (e^{\beta})^3 \phantom{\; + 0 (e^{\beta})^2 \;} - 1 (e^{\beta}) \phantom{ + 0 }
      \;
    \big)
    &
    4
    \\
    e^{-3 \beta}
    \big(
      \;
      + (e^{\beta})^3 + 2 (e^{\beta})^2 - 1 (e^{\beta}) - 2
      \;
    \big)
    &
    9
    \\
    e^{-3 \beta}
    \big(
      \;
      + (e^{\beta})^3 - 2 (e^{\beta})^2 - 1 (e^{\beta}) + 2
      \;
    \big)
    &
    9
  }
$$

\end{example}
