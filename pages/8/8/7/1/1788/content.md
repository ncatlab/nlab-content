
$$
  \array{
    V^{cpt}
    &
      \longrightarrow
    &
    k P
   \big(
     V \oplus \mathbf{1}
   \big)
    \\
    v &\mapsto&
    \left\{
    \array{
      [v,1] &\vert& v \in V
      \\
      [1,0] &\vert& v = \infty
    }
    \right.
  }
$$


$$
  \array{
    \mathcal{L}_v
    & \coloneqq & 
    \frac{
      (V \setminus \{0\}) \times k^\ast
    }{
      k^\times
    }
    &
      \overset{
        [ v, z ]
        \mapsto 
        \big(
          [v], v \cdot z 
        \big)
      }{\longrightarrow}
    &
      \frac
      { V \setminus \{0\} }
      { k^\times }
      \times
      V
    \\
    \big\downarrow
    &&
    \big\downarrow{}^{\mathrlap{
       \frac{id \times pt}{ k^\times }
    }}
    \\
    k P(V)
    &=&
    \frac{
      (V \setminus \{0\}) \times \ast
    }{
      k^\times
    }
  }
$$


a daisy

\begin{tikzpicture}[scale=3]
\fill (0,0) circle[radius=1pt];
\draw (0,0)  to[in=-30,out=30,loop] (0,0);
\draw (0,0)  to[in=60,out=120,loop] (0,0);
\draw (0,0)  to[in=150,out=210,loop] (0,0);
\draw (0,0)  to[in=-60,out=-120,loop] (0,0);
\end{tikzpicture}

