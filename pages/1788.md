

Such morphisms may hence be represented by [[paths]] 

* on a $(p+1)\times(q+1)$-lattice,

* from one corner to its opposite corner,

* consisting of $p+q$ unit steps, 

* each either horizontally or vertially:


\begin{proof}

From Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise} 
it

is clear (Rem. \ref{DegenerateSimplicesInProductOfSimplicialSets}) that a 

simplex $\sigma$ (eq:GenericSimplexInProductOfSimplices) is degenerate 

precisely if, when regarded as a path as above, it contains a [[constant function|constant]] step, i.e. one which moves neither horizontally nor vertically. But then -- by degree reasons, since we are looking at paths of $p + q$ steps in a lattice of side length $p$ and $q$ -- it must be that the path proceeds by $p + q$ unit steps. 

\end{proof}


Here is another way to think of these non-degenerate simplices:


\begin{definition}
For $X$ some [[simplicial set]] $x \in X_p$ some $p$-cell and 
for $\mu = (\mu_1 \lt  \mu_2, \lt \cdots \lt \mu_q)$ a sequence of [[natural numbers]] in $\{0, \cdots p+q\}$, write

$$
  s_\mu \colon X_p \to X_{p+q}
$$

for the map dual to the sequence 

$$
  [p+q] 
    \stackrel{\sigma_{\mu_q}}{\to}
  [p+q-1]
    \stackrel{\sigma_{\mu_{q-1}}}{\to}
  \cdots
   \stackrel{\sigma_{\mu_1}}{\to}
   [p]
  \,,
$$

where $\sigma_i$ is the surjective monotone map that repeats the index $i$.

\end{definition}



\linebreak

Such morphisms may hence be represented by [[paths]] 

* on a $(p+1)\times(q+1)$-lattice,

* from one corner to its opposite corner,

* consisting of $p+q$ unit steps, 

* each either horizontally or vertially:


\begin{proof}

From Prop. \ref{CartesianProductOfSimplicialSetsIsComponentwise} 
it

is clear (Rem. \ref{DegenerateSimplicesInProductOfSimplicialSets}) that a 

simplex $\sigma$ (eq:GenericSimplexInProductOfSimplices) is degenerate 

precisely if, when regarded as a path as above, it contains a [[constant function|constant]] step, i.e. one which moves neither horizontally nor vertically. But then -- by degree reasons, since we are looking at paths of $p + q$ steps in a lattice of side length $p$ and $q$ -- it must be that the path proceeds by $p + q$ unit steps. 

\end{proof}

\begin{tikzcd}
  [
    row sep=large
  ]
    {(0,0)}
    \ar[r]
    \ar[d]
    \ar[
      r,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    %
    {(1,0)}
    \ar[r]
    \ar[d]
    \ar[
      d,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,0)}
    \ar[rr,dotted]
    \ar[d]
    &
    &
    {(p,0)}
    \ar[d]
    \\
    {(0,1)}
    \ar[r]
    \ar[d]
    &
    {(1,1)}
    \ar[r]
    \ar[d]
    \ar[
      d,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,1)}
    \ar[rr, dotted]
    \ar[d]
    &
    \cdots
    &
    {(p,1)}    
    \ar[d]
    \\
    {(0,2)}
    \ar[r]
    \ar[dd, dotted]
    &
    {(1,2)}
    \ar[r]
    \ar[dd, dotted]
    \ar[
      r,-,
      color=blue,
      opacity=.25,
      line width=6pt
    ]
    &
    {(2,2)}
    \ar[rr, dotted]
    \ar[dd, dotted]
    \ar[ddrr, dotted]
    \ar[
      ddrr,-,
      color=blue,
      opacity=.25,
      line width=6pt,
      dotted
    ]
    &
    &
    {(p,2)}
    \ar[dd, dotted]
    \\
    &
    &
    &&
    \\
    {(0,q)}
    \ar[r]
    &
    {(1,q)}
    \ar[r]
    &
    {(2,q)}
    \ar[rr, dotted]
    &
    &
    {(p,q)}
\end{tikzcd}



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
