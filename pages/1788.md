
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
