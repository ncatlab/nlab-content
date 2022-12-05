
Let $G  \,\in\, Grp(Set)$ be a [[discrete group]] and write $\mathbf{B}G \,=\,\big( G \rightrightarrows \ast\big)$ for its [[delooping groupoid]]. The [[functor category]]

$$
  \Lambda \mathbf{B}G
  \;\coloneqq\;
  Maps(\mathbf{B}\mathbb{Z}, \, \mathbf{B}G)
$$

is also known as the *[[inertia groupoid]]* of $G$.

By the discussion [here](natural+transformation#InTermsOfCartMon) at *[[natural transformation]]* that its [[nerve]] may be described as

$$
  \big(
    N \Lambda \mathbf{B}G
  \big)_n
  \;\;
  =
  \;\;
  Hom\big(
    \mathbf{B}\mathbb{Z} 
    \,\times\,
    [n]
    ,\;
    \mathbf{B}G
  \big)
  \,,
$$

where $ (-) \times [n]$ denotes forming the [[product category]] with the [[poset]] $\big\{ 0 \lt 1 \lt \cdots \lt n \big\}$, regarded as a category. 

We may denote the elements in this nerve by

$$
  \big(
    \gamma;
    \,
    g_{n-1}
    ,\,
    g_{n-1}
    ,\,
    \cdots
    ,\,
    g_0
  \big)
  \;\;
  \in
  \;\;
  \big(
    N \Lambda \mathbf{B}G
  \big)_n
$$

$$
  \begin{array}{ccc}
    \big(
      N \mathbf{B}\mathbb{Z}
    \big)_n
      \,\times\,     
     \overset{
        \mathclap{
          \big(
           N
           Maps(\mathbf{B}\mathbb{Z},\, \mathbf{B}G) 
         \big)_n
       }
     }{
     \overbrace{
     Hom\big(
        \mathbf{B}\mathbb{Z} \times [n]
        ,\,
        \mathbf{B}G
     \big)
     }
    }
    &
    \xrightarrow{\;\;\; \;\;\;}
    &
    N\big(
      \mathbf{B}G
    \big)_n
    \\
    \begin{array}{ccccccccccc}
      \big(\bullet;
      &
      0,
      &
        \cdots, 
      &
        \overset{ 
          \mathclap{
            \mathrm{step} \; j+1 
          }
        }{
          \overbrace{\;1\;}
        }, 
        &
        \cdots, 
        &
      0,
        &
      0
      \big)
      \\
      \big(
        \gamma
        ;
        &
        g_{n-1}, 
        &
        \cdots, 
        &
        \mathrm{e}
        , 
        &
        \cdots 
        ,
        &
        g_1
        , 
        &
        g_0
      \big)
    \end{array}
    &\mapsto&
    \big(
      g_{n-1}
      ,\,
      \cdots
      ,\,
      g_{n-j}
      ,\,
      Ad_j(\gamma)
      ,\,
      g_{n - j - 1}
      ,\,
      \cdots
      ,\,
      g_0
    \big)
  \end{array}
$$

\linebreak

\linebreak

\linebreak

\linebreak

$$
  Hom\big(
    \Delta[n]
    ,\,
    [X, A] \times X
    \xrightarrow{\; ev \;}
    X
  \big)
  \;\; \simeq \;\;
  Hom\big(
    \Delta[n]
    ,\,
    [X, A] \times X
    \xrightarrow{\; ev \;}
    X
  \big)
  \;\; \colon \;\;
  Hom\big(
    X \times \Delta[n]
    ,\,
    A
  \big)
  \times
  Hom\big(
    \Delta[n]
    ,\,
    X
  \big)
  \to
  Hom\big(
    \Delta[n]
    ,\,
    A
  \big)
$$


$$
  \begin{array}{cc}
  \text{path} & (1,n)\text{-shuffle}
  \\
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
  &
  \Big(
    1
    ,
    \;
    2, 3, \cdots, n
  Big)
  \,,
  \end{array}
$$


\begin{tikzcd}[
  row sep=0pt
  ]
  7 &[-20pt] 
  {} \ar[rr, -, line width=5pt, blue, opacity=.3] &[-10pt] {}  &[+25pt] {} &[-10pt] {}
  &[+30pt]
  5 &[-20pt] {} &[-10pt] {} \ar[rr, -, line width=5pt, blue, opacity=.3] &[+25pt] {} &[-10pt] {}
  \\
  6 & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {}  & {} & {}
  &
  3 & {} & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {}
  \\
  5 & {} & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {}
  &
  2 & {} & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {}
  \\
  4 & {}  \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {} & {}
  &
  7 &
  {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {}  & {} & {}
  \\
  3 & {} & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {}
  &
  6 & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {}  & {} & {}
  \\
  2 & {} & {} \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {}
  &
  4 & {}  \ar[rr, -, line width=5pt, blue, opacity=.3] & {} & {} & {}
  \\
  1 & {} \ar[rr, -, line width=5pt, blue, opacity=.3]  & {} & {} & {} 
  &
  1 & {} \ar[rr, -, line width=5pt, blue, opacity=.3]  & {} & {} & {} 
\end{tikzcd}



\begin{tikzcd}[
    sep=30pt
  ]
    &[-12pt]
    &
    \mathclap{
      \color{gray}
      \mu_1 = 1
    }
    &
    \mathclap{
      \color{gray}
      \mu_2 = 4
    }
    &
    \color{gray}
    \cdots
    \\[-20pt]
    &
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
    \color{gray}
    \nu_1 = 2
    &
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
    &
    {(p,1)}
    \ar[d]
    \\
    \color{gray}
    \nu_2 = 3
    &
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
    \color{gray}
    \vdots
    &
    &
    &
    &&
    \\
    &
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
  \begin{array}{cc}
    \text{positions of horizontal steps}
    &
    \text{positions of vertical steps}
    \\
    \mu_1 \lt \mu_2 \lt \cdots \lt \mu_p
    &
    \nu_1 \lt \nu_2 \lt \cdots \lt \nu_p
  \end{array}  
$$


***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--

\begin{definition}([ScholzeWeinstein20](#ScholzeWeinstein20), Definition 6.2.1)

Let $R$ be a perfectoid ring. The _tilt_ of $R$ is

$$R^{\flat}=\underset
    {\underset{x\mapsto x^{p}}{\leftarrow}}
    {\lim}R$$

A priori this is a topological multiplicative monoid, so turn it into a topological ring we equip it with the addition structure given by

$$(x+y)^{(i)}=\lim_{n\to\infty}(x^{(i+n)}+y^{(i+n)})^{p^{n}}.$$

\end{definition}
