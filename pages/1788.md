
$$
  \Delta[n+1]
  \longrightarrow
  [S,\overline{W}] \times S
$$

$$
  (\phi,j)
  \;\in\;
  Hom(\Delta[n+1] \times S, \overline{W}) 
  \times
  Hom(\Delta[n+1], S)
$$


\begin{proposition}
  The [[evaluation map]]
  $$
    [S,\overline{W}G] \times S
    \xrightarrow{\;\;}
    \overline{W}G
  $$
  (out of the [[product of simplicial sets|product]] of the [[simplicial hom complex]] out of $S$ with $S$)
  takes any non-degenerate $n+1$-simplex of $[S,\overline{W}G] \times S$
  $$
    \array{
      (\gamma, [0]) 
      &\xrightarrow{ (g_{n-1}, id) }&
      ( Ad_{n-1}(\gamma), [0]  )
      &\xrightarrow{ (g_{n-2}, id) }&
      \cdots
      &\xrightarrow{ (g_{j}, id) }&
      \big( Ad_{j}(\gamma), [0]  \big)      
      \\
      && && &&
      \big\downarrow {}^{\mathrlap{ (e, [ [0],[1] ]) }}
      \\
      && && &&
      (Ad_j(\gamma), [1])
      &\xrightarrow{ (g_{n-j},id)  }
      &
      \cdots
      &\xrightarrow{ (g_0,id) }&      
      (Ad_0(\gamma), [1])
    }
  $$
  to the following $n+1$ simplex of $\overline{W}G$:
  $$
    \array{
      \bullet
      &\xrightarrow{ g_{n-1} }&
      \bullet
      &\xrightarrow{ g_{n-2} }&
      \cdots
      &\xrightarrow{ g_{j} }&
      \bullet
      \\
      && && &&
      \big\downarrow {}^{\mathrlap{ 
        Ad_j(\gamma)
      }}
      \\
      && && &&
      \bullet
      &\xrightarrow{ g_{n-j} }
      &
      \cdots
      &
      \xrightarrow{ g_0 } 
      &      
      \bullet
      \mathrlap{\,.}
    }
  $$
\end{proposition}


  \begin{tikzcd}
    \scalebox{.8}{$
      \left( {[0]} \atop {[0]} \right)
    $}
    \ar[
      rr,
      "{
        \left(
        {[0,0]}
        \atop
        {[0,1]}
        \right)
      }"{above, scale=.8}
    ]
    \ar[
      dd,
      "{
        \left(
        {[0,1]}
        \atop
        {[0,0]}
        \right)
      }"{left, scale=.8}
    ]
    \ar[
      ddrr,
      "{
        \left(
        { [0,1] }
        \atop
        { [0,1] }
        \right)
      }"{description, scale=.8}
    ]
    &&
    \scalebox{.8}{$
      \left( {[0]} \atop {[1]} \right)
    $}
    \ar[
      dd,
      "{
        \left(
        {[0,1]}
        \atop
        {[1,1]}
        \right)
      }"{right, scale=.8}
    ]
    \ar[
      ddll,
      phantom,
      "{
        \left(
        { [0,0,1] }
        \atop
        { [0,1,1] }
        \right)
      }"{pos=.15, scale=.8}
    ]
    \ar[
      ddll,
      phantom,
      "{
        \left(
        { [0,1,1] }
        \atop
        { [0,0,1] }
        \right)
      }"{pos=.85, scale=.8}
    ]
    \\
    \\
    \scalebox{.8}{$
      \left( {[1]} \atop {[0]} \right)
    $}
    \ar[
      rr,
      "{
        \left(
        {[1,1]}
        \atop
        {[0,1]}
        \right)
      }"{below, scale=.8}
    ]
    &&
    \scalebox{.8}{$
      \left( {[1]} \atop {[1]} \right)    
    $}
  \end{tikzcd}


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
