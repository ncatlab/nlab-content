
\begin{definition}
  For $G$ a [[discrete group]] and $A$ a [[G-space|$G$-space]], and $\tau_b \,\colon \,X_b \xrightarrow{\;\;} B G$ a map, the $\tau$-[[twisted cohomology|twisted]] [[non-abelian cohomology]] of $X_b$ with [[coefficients]] in $A$ is
$$
  A^\tau(X_b)
  \;\coloneqq\;
  H^\tau(X_b;\, A)
  \;\coloneqq\;
  \pi_0
  (p_{B G})_\ast
  Map
  \Big(
    (X_b, \tau_b)
    ,\,
    p_{B}^\ast
    \big(   
      A \times_G E G
      ,\,
      p_{A \times_G E G}
    \big)
  \Big)
$$
\end{definition}

\begin{proposition}
  Given a global twist
  $$
    \tau \,\colon\, X \xrightarrow{\;\;} B G
    \,,
  $$
  the $\tau_b$-twisted $A$-cohomology sets of $X_b$,
as $b \in B$, arrange into a covering space of $B$.
\end{proposition}
\begin{proof}
  now we need that $(p_{B G})_\ast$ is right Quillen... 
\end{proof}


$$
  \begin{aligned}
    kTop_{/B'}
    \Big(
      (U,p_U)
      ,\,
      f^\ast 
      Map
      \big(
        (X,p_X)
        ,\,
        (A,p_A)
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      f_! (U,p_U)
      ,\,
      Map
      \big(
        (X,p_X)
        ,\,
        (A,p_A)
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      (U,f \circ p_U)
      ,\,
      Map
      \big(
        (X,p_X)
        ,\,
        (A,p_A)
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \big(
      (U,f \circ p_U)
      \times
      (X, p_X)
      ,\,
      (A,p_A)
    \big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      f_!
      \big(
        (U, p_U)
        \times
        f^\ast (X, p_X)
      \big)
      ,\,
      (A,p_A)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B'}
    \Big(
        (U, p_U)
        \times
        f^\ast (X, p_X)
      ,\,
      f^\ast
      (A,p_A)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B'}
    \Big(
      (U, p_U)
      ,\,
      Map
      \big(
        f^\ast (X, p_X)
        ,\,
        f^\ast (A,p_A)
      \big)
    \Big)
  \end{aligned}
$$

\linebreak

$$
  \begin{aligned}
    kTop_{/B}
    \Big(
      (U, p_U)
      ,\,
      \Map
      \big(
        p_B^\ast X_0
        ,\,
        p_B^\ast A_0
      \big)
    \Big)
    &
    \;\simeq\;
    kTop_{/B}
    \big(
      (U, p_U) \times (B \times X_0, pr_{B})
      ,\,
      p_B^\ast A_0
    \big)
    \\
    & 
    \;\simeq\;
    kTop_{/B}
    \big(
      (U \times X_0, p_U \circ pr_U)
      ,\,
      p_B^\ast A_0
    \big)
    \\
    &
    \;\simeq\;
    kTop
    \Big(
      U \times X_0
      ,\,
      A_0
    \big)
    \\
    &
    \;\simeq\;
    kTop
    \Big(
      U 
      ,\,
      Map
      \big(
        X_0
        ,\,
        A_0
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop
    \Big(
      (p_B)_!
      (U,p_U)
      ,\,
      Map
      \big(
        X_0
        ,\,
        A_0
      \big)
    \Big)
    \\
    &
    \;\simeq\;
    kTop_{/B}
    \Big(
      (U,p_U)
      ,\,
      p_B^\ast
      Map
      \big(
        X_0
        ,\,
        A_0
      \big)
    \Big)
  \end{aligned}
$$

...