

\begin{tikzcd}[column sep=large]
  G\mathrm{Spaces}
  \ar[
    rr,
    shift right=7pt,
    "(N(H) \hookrightarrow G)^\ast"{below}
  ]
  \ar[
    rr,
    phantom,
    "\scalebox{.7}{$\bot$}"
  ]
  \ar[
    rrrr,
    rounded corners,
    to path={ 
         -- ([yshift=-20pt]\tikztostart.south) 
         --node[below]{\scalebox{.7}{$(-)^H$}} ([yshift=-20pt]\tikztotarget.south) 
         -- (\tikztotarget.south)}
  ]
  &&
  N\!(H)\mathrm{Spaces}
  \ar[
    ll,
    shift right=7pt,
    "G \times_{N\!(H)} (-)"{above}
  ]
  \ar[
    rr,
    shift right=7pt,
    "{
      \mathrm{Maps}
      (
        N\!(H)\!/H,
        -
      )^{N\!(H)}
    }"{below}
  ]
  \ar[
    rr,
    phantom,
    "\scalebox{.7}{$\bot$}"
  ]
  &&
  \big(
    N\!(H)\!/H
  \big)\mathrm{Spaces}
  \ar[
    ll,
    shift right=7pt,
    "{
      ( N\!(H) \twoheadrightarrow N\!(H)\!/H )^\ast
    }"{above}
  ]
  \ar[
    llll,
    rounded corners,
    to path={
         -- ([yshift=+20pt]\tikztostart.north)
         --node[above]{\scalebox{.7}{$G/H \times_{N\!(H)\!/H}(-)$}} ([yshift=+20pt]\tikztotarget.north)
         -- (\tikztotarget.north)}
  ]
\end{tikzcd}


Throughout, let $G_1, G_2 \in $ [[TopologicalGroups]]
and consider a [[continuous function|continuous]] [[homomorphism]] of [[topological groups]]

$$
  \phi
  \;\colon\;
  G_1 
    \longrightarrow
  G_2
  \,.
$$

\begin{defn}\label{PullbackAction}
  **(pullback action)** \linebreak
  Write
  $$
    Topological G_1 Spaces
      \overset{
        \;\;\;
        \phi^\ast
        \;\;\;
       }{\longleftarrow}
    Topological G_2 Spaces
  $$

for the [[functor]] which takes a [[topological G-space|topological G2-space]] $(X,\rho)$ to the same underlying [[topological space]] $\rho$, equipped with the $G_1$-action $ \rho(\phi(-))$.

\end{defn}

\begin{lemma}

The pullback action functor (Def. \ref{PullbackAction}) is the [[left adjoint]] of a pair of [[adjoint functors]]

$$
  G_1 Spaces
  \underoverset
    {
      \underset{
        Maps
        \big(
          G_2, -
        \big)^{G_1}
      }{\longrightarrow}
    }
    {
      \overset{
         \phi^\ast
      }{
         \longleftarrow
      }
    }
    {\bot}
  G_2 Spaces
$$

where for $X \in Topological G_1 Spaces$ 
the expression $Maps(G_2,-)^{G_1}$ denotes the $G_1$-[[fixed locus]] in the [[mapping space]] between [[topological spaces]] equipped with $G_1$-[[actions]] (on $G_2$ the $\phi$-induced left multiplication action) 
and equipped with the $G_2$-[[group action|action]] given by

\[
  \label{ActionOnG1EquivariantMapsOutOfG2}
  \array{
    G_2 \times Maps(G_2,X)^{G_1}
    &
      \overset{}{\longrightarrow}
    &
    Maps(G_2,X)^{G_1}
    \\   
    (g_2, h)
    &\mapsto&
    h\big(
      (-) \cdot g_2
    \big)
     \,.
  }
\]

\end{lemma}

\begin{proof}

To see the defining [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism), consider a $G_1$-[[equivariant function|equivariant]] [[continuous function]]

$$
  \phi^\ast X
  \overset{
    \;\;\;
    f
    \;\;\;
  }{
    \longrightarrow
  }
  Y
  \,.
$$

From this we obtain the following function

$$
  \array{
    X 
    &
      \overset{
        \tilde f
      }{
        \longrightarrow 
      }
    &
    Maps
    \big(
      G_2,
      Y
    \big)^{G_1}
    \\
    x
    &\mapsto&
    \big(
      g_2
      \mapsto
      f( g_2 \cdot x )
    \big)
    \,,
  }
$$

where $e \in G_2$ denotes the [[neutral element]].

This is manifestly:

* well-defined, due to the $G_1$-equivariance of $f$;

* continuous, being built from composition of continuous map;

* $G_2$-equivariant with respect to the action (eq:ActionOnG1EquivariantMapsOutOfG2).

Conversely, given a $G_2$-equivariant continuous function $X \overset{\tilde f}{\longrightarrow} Maps\big(G_2, Y\big)^{G_1}$, we obtain the following function

$$
  \array{
    \phi^\ast X 
    &\overset{}{\longrightarrow}&
    Y
    \\
    x
    &\mapsto&
     \tilde f(x)(e)
    \,.
  }
$$

This is:

* continuous, being the composition of continuous functions;

* $G_1$-equivariant due to the equivariance properties of $\tilde f$:

  $$
    \begin{aligned}
      \phi(g_1) \cdot x
      & \mapsto
      \tilde f
      \big( 
        \phi(g_1)\cdot x
      \big) 
      (e)
      \\
      & = 
      \tilde f
      ( 
        x
      ) 
      \big(
         e \cdot \phi(g_1)
      \big)
      \\
      & =
      \tilde f
      ( 
        x
      ) 
      \big(
         \phi(g_1)
         \cdot 
         e
      \big)
      \\
      & =
      g_1
        \cdot
      \big(
      \tilde f
      ( 
        x
      ) 
      (
         e
      )
      \big)
    \end{aligned} 
  $$

Finally, it is clear that these transformations $f \leftrightarrow \tilde f$ are [[natural transformation|natural]], hence it only remains to see that they are [[bijective]]:

Plugging in the above constructions we find indeed:

$$
 \widetilde 
  {\tilde f}
  \;\colon\;
  x \mapsto f(e \cdot x) = f(x)
$$

and

$$
  \begin{aligned}
    \widetilde {\widetilde {\tilde f}}
    \;\colon\;
    x 
    & 
    \mapsto 
    \big(
      g_2 \mapsto \tilde f(g_2 \cdot x)(e) 
    \big)
    \\
    & =
    \big(
      g_2 \mapsto \tilde f(x)(e \cdot g_2) 
    \big)  
    \\
    & =
    \big(
      g_2 \mapsto \tilde f(x)(g_2) 
    \big)  
    \,.
  \end{aligned}
$$

\end{proof}

\begin{tikzcd}
  G \times P
  \ar[
    drr,
    bend left=20,
    "\rho"
  ]
  \ar[
    ddr,
    bend right=20,
    "\mathrm{pr}_2\;\;\;"{below}
  ]
  \ar[
    dr,
    dashed,
    "\simeq"{description}
  ]
  \\
  & 
  P \times_X P
  \ar[
    r
  ]
  \ar[d]
  \ar[
    dr,
    phantom,
    "\mbox{\tiny\rm(pb)}"{description}
  ]
  &
  P 
  \ar[
    d,
    "p"
  ]
  \\
  &
  P 
  \ar[
    r,
    "p"{below}
  ]
  & 
  X
\end{tikzcd}



$$
  \array{
    \widehat G 
      \times_{\widehat H} 
    S
    &\longrightarrow&
    \widehat G \times_{\widehat H} \widehat H
    &{\phantom{}}&
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    G \times_H S
    &\longrightarrow&
    G \times_H H
  }
$$


$$
  \array{
    \big(
      \Gamma \rtimes_\alpha G
    \big)
      \times_{\widehat H}    
    S
    &
      \longrightarrow
    &
    \big(
      \Gamma \rtimes_\alpha G
    \big)
    / \widehat H
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    G \times_H S
    &
    \underoverset
      {}{}{\longrightarrow}
    &
    G/H
  }
$$

\linebreak

\linebreak


$$
  \array{
    \big(
      \Gamma \rtimes_\alpha G
    \big)
      \times_{\widehat H}    
    S
    &
      \longrightarrow
    &
    \big(
      \Gamma \rtimes_\alpha G
    \big)
    \times_{\hat H} \hat H
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    G \times_{\hat H} S
    &
    \underoverset
      {}{}{\longrightarrow}
    &
    G \times_{\hat H} \widehat H
  }
$$



$\ldots$

$\infty$


Please do not delete the following example for the moment!

An article by \cite{vandenBergGarner2011} and another by \cite{MarraReggio2020}.



\section{References}

\bibitem{MarraReggio2020}

\bibitem{vandenBergGarner2011}

\bibitem{AdámekRosícky2020}

\bibitem{FongSpivakTuyeras2017}

\linebreak

\bibitem{Witten1995}

\linebreak

$$
  \frac{13}{48}
  (
    p_2 - \frac{1}{4} p_1^2
  )
  -
  \frac{1}{4}
  (\frac{1}{4} p_1^2)
$$

$$
  \frac{13}{12}
  (
    p_2 - \frac{1}{4} p_1^2
  )
  -
  (\frac{1}{4} p_1^2)
$$

$$
  \frac{13}{12}
    p_2 

  -
  \frac{25}{12}
  (\frac{1}{4} p_1^2)
$$

$$
  13
  p_2 
  -
  5
  p_1^2
$$

$\Eta$

Write

$$
  \array{
    Q
    \\
    \mathllap{
      {}^{{}_{
        h \mapsto (\phi(h),h)
      }}
    }
    \big\uparrow
    \\ 
    H
  }
$$

$$
  (\phi(g_1 g_2), g_1 g_2)
  =
  (\phi(g_1), g_1)
  \cdot
  (\phi(g_2), g_2)  
  =
  \big(
    \phi(g_1) \cdot \alpha(g_1)(\phi(g_2)),
    g_1 \cdot g_2
  \big)
$$

$$
  \array{
    (\gamma, u)
    &\mapsto&
    [\gamma, \sigma(u)]
    \\
    \Gamma \times U 
    &
    \underoverset{}{[id \times \sigma]}{
      \rightleftarrows
    }
    &
    \big(
      \Gamma \rtimes_\alpha G_{\vert U} 
    \big)/ Q
    \\
    \gamma 
    \phi(\sigma(u)),
    u
    &&
    [\gamma, g]
  }
$$


$$
  [\gamma,g]
  \;=\;
  (\gamma,g)
    \cdot
  ( \phi(g^{-1} \sigma(u)),  g^{-1} \sigma(u)  )
  \;=\;
  (
    \gamma
    \alpha(g)(\phi(g^{-1} \sigma(u)))
  )
$$

$$
    \gamma
    \alpha(g)(\phi(g^{-1} \sigma(u)))
   =
    \gamma
    \alpha(g)(  \phi(g^{-1}) \alpha(g^{-1})(\phi(\sigma(u)))  )
  =
  \gamma
  \alpha(g)(\phi(g^{-1}))
  \phi(\sigma(u))
$$

$$
  \array{   
    G
    \times_H
    (S \times \Gamma)
    &
    \longrightarrow
    &
    G \times_H \Gamma
    & 
    =
    &
    (\Gamma \times G)
    \big/
    ( graph(H \to \Gamma) )
    \\
    \big\downarrow
    &&
    \big\downarrow
    & 
    \swarrow
    \\
    G \times_H S
    &
    \underoverset
      {}
      {}
      {\longrightarrow}
    &
    G \times_H H
  }
$$


