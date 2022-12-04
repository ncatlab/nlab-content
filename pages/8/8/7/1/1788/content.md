

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
