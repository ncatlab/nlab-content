
$\ldots$

\begin{tikzcd}
  & g_2 g_1
  \ar[
    dr,
    "{(g_2 g_1, g_0)}"{sloped, near start},
    ""{name=s, below, pos=0.01}
  ]
  \\
  g_2
  \ar[
    ur,
    "{(g_2, g_1)}"{sloped, near end}
  ]
  \ar[
    rr,
    "{(g_2, g_1 g_0)}"{below},
    ""{name=t, above}
  ]
  &
  {}
  &
  g_2 g_1 g_0
  \ar[
    from=s, to=t,
    Rightarrow,
    "{(g_2, g_1, g_0)}"{description}
  ]
\end{tikzcd}

$$
  \big(X \times_{\overline{W}G} W G\big)
  \times \Delta[k]
  \;\simeq\;
  \big(
    X \times \Delta[k]
  \big) 
  \times_{\overline{W}G} W G
$$

\begin{tikzcd}
  {
    { (X \times_{\overline{W}G} W G) \times \Delta[k] } 
    \atop
    { \mathllap{\simeq} (X \times \Delta[k]) \times_{\overline{W}G} W G  } 
  }
  \ar[r]
  \ar[d]
  \ar[dr,phantom,"\mbox{\tiny\rm(pb)}"]
  & 
  X \times \Delta[k]
  \ar[
    d,
    "\mathrm{pr}_1"
  ]
  \\
  X \times_{\overline{W}G} W G
  \ar[r]
  \ar[d]
  \ar[dr,phantom,"\mbox{\tiny\rm(pb)}"]
  & 
  X 
  \ar[
    d
  ]
  \\
  W G
  \ar[r]
  &
  \overline{W}G
\end{tikzcd}

\begin{tikzcd}[column sep=5pt]
  \ast 
  \ar[r]
  &
  \mathbf{B}G
  \ar[dr]
  \ar[rr, dashed]
  &&
  X /\!/ G
  \ar[dl]
  &
  X
  \ar[l]
  \\
  &
  & 
  \mathbf{B}G
  &
\end{tikzcd}

$$
  \begin{aligned}
  \underset{1 \leq j \leq n}{\prod}
  \frac
    {j}
    {N + j - 1}
  & 
  \;=\;
  \left(
    { N + n  - 1 }
    \atop
    { n }
  \right)^{-1}
  \end{aligned}
$$

$$
 \begin{aligned}
  \left\vert
    sYT_n(N)
  \right\vert  
  &
  \;
  \overset{
    n \to \infty
  }{\sim}
  \;
  \left(
    \frac{N}{n}
  \right)^{ \tfrac{1}{4} N(N-1) }
  \cdot
  \frac
    {N^n}
    {N!}
  \cdot
   2^N
   \cdot
   \pi^{ - \tfrac{1}{2} N }
  \cdot
  \Gamma
  \left(
    1 + \tfrac{N}{2}
  \right)  
  \cdot
  \underset{
    \mathclap{
    \Gamma
    \left( 
      N
    \right)
      \cdot
    (2\pi)^{ \tfrac{1}{2}(N-1) }
    \cdot
    N^{ \tfrac{1}{2} - N }
    }
  }{
  \underbrace{
  \underoverset
    {j=0}
    {N-1}
    {\prod}
    \Gamma
    \left(
      1 + \tfrac{1}{2}j
    \right)  
   }
   }
   \\
   & \;=\;
  \left(
    \frac{N}{n}
  \right)^{ \tfrac{1}{4} N(N-1) }
  \cdot
  \frac
    {N^n}
    {N!}
  \cdot
   2^N
   \cdot
   \pi^{ - \tfrac{1}{2} N }
  \cdot
  \underset{
    \tfrac{N}{2}\Gamma(N/2)
  }{
    \underbrace{
    \Gamma
    \left(
      1 + \tfrac{N}{2}
    \right)  
  }
  }
  \cdot
  \Gamma
  \left( 
    N
  \right)
    \cdot
  (2\pi)^{ \tfrac{1}{2}(N-1) }
    \cdot
  N^{ \tfrac{1}{2} - N }
  \\
  & 
  \;=\;
  \tfrac{1}{\pi}
  \left(
    \frac{N}{n}
  \right)^{ \tfrac{1}{4} N(N-1) }
  \cdot
  \frac
    {N^{n-1}}
    {N!}
  \cdot
   2^{\tfrac{3}{2}(N-1)}
  \cdot
  \Gamma
  \left(
    \tfrac{N}{2}
  \right)  
  \cdot
  \Gamma
  \left( 
    N
  \right)
    \cdot
  N^{ \tfrac{1}{2} - N }
  \end{aligned}
$$
