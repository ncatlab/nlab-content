
The non-degenerate (n+1)-simplices of 
$\begin{aligned} & \Delta[1] \\ \times & \Delta[n] \end{aligned}$ are

$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 1 & 1 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 0 & 1 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
$$

$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 1 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 1 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
$$


$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 0 & 1 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 2 & 2 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
$$



$$
  \left(
  \;\,
  \array{
    \mathllap{[}
    0 & 0 & 0 & 0 & 1 & \cdots & 1 & 1
    \mathrlap]
    \\
    \mathllap[
    0 & 1 & 2 & 3 & 3 & \cdots & n-1 & n
    \mathrlap]
  }
  \;\,
  \right)
$$



$$
  \array{
    Hom(\Delta[1] \times \Delta[n], \overline{W}G)
    \times
    Hom(\Delta[n],\Delta[1])
    &&
    Hom(\Delta[n],\overline{W}G)  
    \\
    (\gamma, g_{n-1}, \cdots, g_0), 
    (0,\cdots, 0, 1, \cdots, 1)
    &&
  }
$$

$$
  \array{
    (\gamma, g_{n-1}, \cdots, g_1, g_0)
    \;\colon\;
    &
    \Delta[1] \times \Delta[n]
    &\longrightarrow&
    \overline{W}G
    \\
    &
    \big(
       [0, \cdots, 0, 1, \cdots, 1], ([0,1,\cdots, n])
    \big)
    &\mapsto&
    ( )
  }
$$
   

$$
  \begin{aligned}
    H^n
    \big(
      B G; A
    \big)
    &
    \;=\;
    Ho(sSet)
    \big(
      N \circ \mathbb{Z}(\overline{W}G),
      \,
      A[n]
    \big)
    \\
    &
    \;\simeq\;
    Ho(sSet)
    \big(
      \overline{W}G; \, undrlg \circ DK\big( A[n] \big)
    \big)
    \\
    &
    \;\overset{[S,-]}{\to}\;
    Ho(sSet)
    \big(
      [S,\overline{W}G];\, \, \big[S,undrlg \circ DK\big( A[n] \big)\big]
    \big)
    \\
    & 
    \;\simeq\;
    Ho(sSet)
    \Big(
      [S,\overline{W}G] \times S,
      \, undrlg \circ DK\big( A[n] \big)  
    \Big)
    \\
    &
    \;\simeq\;
    Ho(sAbGrp)
    \Big(
      \mathbb{Z}\big( [S, \overline{W}G] \times S \big),
      \,
      DK\big(A[n]\big)
    \Big)
    \\
    &
    \;\simeq\;
    Ho(Ch_{\geq 0}(\mathbb{Z}))
    \Big(
      N \circ \mathbb{Z}\big( [S, \overline{W}G] \times S \big),
      \,
      A[n]
    \Big)    
    \\
    &
    \;\overset{EZ}{\simeq}\;
    Ho(Ch_{\geq 0}(\mathbb{Z}))
    \Big(
      N\circ \mathbb{Z}\big([S, \overline{W}G]\big) 
        \otimes 
      \underset{\mathbb{Z}[1]}{\underbrace{N \circ \mathbb{Z}(S)}},
      \,
      A[n]
    \Big)    
    \\
    &
    \;\simeq\;
    Ho(Ch_{\geq 0}(\mathbb{Z}))
    \Big(
      N\circ \mathbb{Z}\big([S, \overline{W}G]\big),
      \,
      A[n] \oplus A[n-1]
    \Big)    
    \\
    & 
    \;\overset{pr_2}{\to}\;
    Ho(Ch_{\geq 0}(\mathbb{Z}))
    \Big(
      N\circ \mathbb{Z}\big([S, \overline{W}G]\big),
      \,
      A[n-1]
    \Big)    
    \\
    & \;=\;
    H^{n-1}
    \big(
      \Lambda B G;
      \,
      A
    \big)        
  \end{aligned}
$$
