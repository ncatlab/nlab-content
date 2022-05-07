
$$
  \begin{array}{lll}
    &
    \mathbf{H}
    \bigg(
      (-)
      ,\,
      Maps
      \Big(
        \underset{\longrightarrow}{\lim}
        \,
        LConst(S_\bullet)
        ,\,
        X
      \Big)
    \bigg)
    \\
    & \;\simeq\;
    \mathbf{H}
    \Big(
      (-)
      \times
      \underset{\longrightarrow}{\lim}
      \,
      LConst(S_\bullet)
      ,\,
      X
    \Big)
    &
    \text{ (eq:MappingStackAdjunction) }
    \\
    & \;\simeq\;
    \mathbf{H}
    \Big(
      \underset{\longrightarrow}{\lim}
      \big(
        (-)
        \times
        LConst(S_\bullet)
      \big)
      ,\,
      X
    \Big)
    &
    \text{ [[universal colimits]] }
    \\
    & \;\simeq\;
    \underset{\longleftarrow}{\lim}
    \,
    \mathbf{H}
    \big(
      (-)
      \times
      LConst(S_\bullet)
      ,\,
      X
    \big)
    \\
    & \;\simeq\;
    \underset{\longleftarrow}{\lim}
    \,
    \mathbf{H}
    \Big(
      (-)
      ,\,
      Maps
      \big(
        LConst(S_\bullet)
        ,\,
        X
      \big)
    Big)
    \\
    & \;\simeq\;
    \mathbf{H}
    \Big(
      (-)
      ,\,
      \underset{\longleftarrow}{\lim}
      \,
      Maps
      \big(
        LConst(S_\bullet)
        ,\,
        X
      \big)
    Big)
  \end{array}
$$



\[
  \label{MappingStackAdjunction}
\]

$$
  \begin{array}{lll}
    & (eq:MappingStackAdjunction)
    \\
    & \text{(eq:MappingStackAdjunction)}
    \\
    & 
    \text{
    <a href="https://ncatlab.org/nlab/show/terminal+geometric+morphism#DirectImageOfTerminalGeometricMoprhismIsHomOutOfTerminalObject">here</a>}
  \end{array}
$$

For the first statement:
$$
  \begin{array}{lll}
     \mathbf{H}
     \Big(
       X
       ,\,
       Maps
       \big(
         LConst(S)
         ,\,
         A
       \big)
     \Big)
     &
     \;\simeq\;   
     \mathbf{H}
     \big(
       X 
       \times
       LConst(S)
       ,\,
       A
     big)
     \\
     & \;\simeq\;
     \mathbf{H}
     \Big(
       LConst(S)
       ,\,
       Maps
       \big(
         X
         ,\,
         A
       \big)
     \Big)
     \\
     & \;\simeq\;
     Grpd_\infy
     \Big(
       S
       ,\,
       \Gamma
       \,
       Maps
       \big(
         X
         ,\,
         A
       \big)
     \Big)
     \\
     & \;\simeq\;
     Grpd_\infy
     \Big(
       S
       ,\,
       \mathbf{H}
       \big(
         X
         ,\,
         A
       \big)
     \Big)
  \end{array}
$$
