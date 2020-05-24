
$$
  \widehat V_{1}
  \;\coloneqq\;
  V
$$

For $n \leq 0 \in \mathbb{Z}$ define, [[recursion|recursively]], the component space in degree $n-1$ to be the vector space of [[linear maps]] from $V$ to the component space in degree $n$:

$$
  \widehat V_{n-1}
  \;\coloneqq\;
  Hom_k( V, \widehat V_n )
  \,.
$$

Hence

$$
  \begin{aligned}
    \widehat V_1 & = V
    \\
    \widehat V_0 & = Hom_k(V,V) = \mathfrak{gl}(V)
    \\
    \widehat V_{-1} & =  Hom_k(V, Hom_k(V,V)) \simeq  Hom_k(V \otimes V, V)
    \\
    \widehat V_{-2} & = Hom_k(V, Hom_k(V, Hom_k(V,V))) \simeq  Hom_k(V \otimes V \otimes V, V)
    \\
    \vdots
  \end{aligned}
$$

The [[super Lie bracket]] is defined for $v \in \widehat V_1 = V$ and for any $f \in \widehat V_{n \leq 0}$ by [[evaluation]]

$$
  [f, v]
  \;\coloneqq\;
  f(v)
$$

and for homogeneously graded elements $f\in \widehat V_{ deg(f) \leq 0 }$ and $g\in \widehat V_{deg(g) \leq 0}$, [[recursion|recursively]] by

$$
  \begin{aligned}
  [f, g]
  &
  \colon\;
  v 
  \;\mapsto\;
  [f, g(v)]
  -
  (-1)^{
    deg(f) deg(g)
  }
  [ g, f(v) ]
  \\
  \end{aligned}
$$

hence

$$
  [ [f,g],v ]
  \;=\;
  [f, [g,v] ]
  -
  (-1)^{
    deg(f) deg(g)
  }
  [ g, [f,v] ]
$$

So, for $f,g \in \widehat V_0 = \mathfrak{gl}(V)$ we have

$$
  [f,g](v)
  \;=\;
  [f,g(v)] - [g,f(v)]
  \;=\;
  f(g(v)) - g(f(v))
$$

which is the Lie bracket of the [[general linear Lie algebra]].

\linebreak

To check the [super Jacobi identity](super+Lie+algebra#eq:GradedJacobiIdentity)

by [[induction]].

It holds for $deg(f_3) \geq 0$ , by spring

Now assume it holds for $deg \geq n$

and consider $deg(f_i) \geq n - 1$


\linebreak

\linebreak

$$
  \begin{aligned}
    [f_1, [f_2, f_3] ] (v)
    & 
    =
    [ f_1,  [f_2, f_3](v) ] 
    -
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3))}
    [  [ f_2, f_3 ], f_1(v)  ]
    \\
    & =
    [ f_1,  [  f_2, f_3(v) ] ] 
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_2)deg(f_3)}
    [ f_1,  [  f_3, f_2(v) ] ] 
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3))}
    [  f_2,  [ f_3,  f_1(v) ] ]
    \\
    & \phantom{=}
    +    
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3)) + deg(f_2)deg(f_3)}
    [  f_3,  [ f_2,  f_1(v) ] ]
    \\
    & = 
    [ f_1,  [  f_2, f_3(v) ] ] 
    -
    (-1)^{deg(f_1) deg(f_2)}
    {
    \color{green}
    [ f_2,  [  f_1, f_3(v) ] ] 
    }
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_2) deg(f_3)}
    \big(
    [ f_1,  [  f_3, f_2(v) ] ] 
    -
    (-1)^{deg(f_1) deg(f_2)}
    {
    \color{orange}
    [ f_3,  [  f_1, f_2(v) ] ] 
    }
    \big)
    \\
    & \phantom{=}
    -
    (-1)^{deg(f_1)(deg(f_2) + deg(f_3))}
    \big(
    [  f_2,  [ f_3,  f_1(c) ] ]
    -
    (-1)^{deg(f_1)deg(f_3)}
    {
    \color{blue}
    [  f_2,  [ f_1,  f_3(v) ] ]   
    }
    \big)
    \\
    & \phantom{=}
    +    
    (-1)^{deg(f_1) deg(f_2 ) + deg(f_1) deg(f_3) + deg(f_2) deg(f_3)}
    \big(
    [  f_3,  [ f_2,  f_1(v) ] ]
    -
    (-1)^{deg(f_1) deg(f_2)}
    {
    \color{cyan}
    [  f_3,  [ f_1,  f_2(c) ] ]
    }
    \big)
    \\
    & \phantom{=}
    (-1)^{deg(f_1) deg(f_2)}
    \big(
    \underset{
      = 0
    }{
    \underbrace{
    +
    {
    \color{green}
    [ f_2,  [  f_1, f_3(v) ] ] 
    }
    -
    {
    \color{blue}
    [  f_2,  [ f_1,  f_3(v) ] ]
    }
    }
    }
    \big)
    \\
    & \phantom{=}
    +
    (-1)^{deg(f_1) deg(f_2) + deg(f_2) deg(f_3)}
    \big(
    \underset{
      = 0
    }{
    \underbrace{
    {
    \color{orange}
    [  f_3,  [ f_1,  f_2(v) ] ]
    }
    -
    {
    \color{cyan}
    [ f_3,  [  f_1, f_2(v) ] ] 
    }
    }
    }
    \big)
  \end{aligned}
$$


\linebreak


\linebreak



$$
  v \cdot w
  \;\coloneqq\;
  [\partial v, w]
$$

\linebreak
\linebreak

$$
  \begin{aligned}
    v_1 \cdot (v_2 \cdot v_3)
    & =
    \big[
      \partial v_1
      ,
      [
        \partial
        v_2, 
        v_3
      ]
    \big]
    \\
    & =
    \big[
      [
        \partial v_1
        , 
        \partial v_2
      ],
      v_3
    \big]
    \;+\;
    (-1)^{
      (deg(v_1)-1)
      (deg(v_2)-2)
     }
     \big[
       \partial v_2,
       [\partial v_1, v_3] 
     \big]
    \\
    & =
    \big[
      \partial
      [
        v_1
        , 
        \partial v_2
      ],
      v_3
    \big](w)
    \;+\;
    (-1)^{
      (deg(v_1)-1)
      (deg(v_2)-2)
     }
     \big[
       \partial v_2,
       [\partial v_1, v_3] 
     \big]
     (w)
  \end{aligned}
$$

\linebreak
\linebreak


$$
  \begin{aligned}
    v_1 \cdot (v_2 \cdot v_3)
    & =
    \rho_{\Theta(v_1)}
    \big(
      \rho_{\Theta(v_2)}(v_3)
    \big)
    \\
    & = 
    \rho_{
      \underset{
        = \rho_{\Theta(v_1)}(v_2)
      }{
        \underbrace{
          [\Theta(v_1), \Theta(v_2)]
        }
      }
    }(v_3)
    +
    \rho_{\Theta(v_2)}
    \big(
      \rho_{\Theta(v_1)}(v_3)
    \big)
    \\
    & = 
    (v_1 \cdot v_2) \cdot v_3
    +
    v_2 \cdot (v_1 \cdot v_3)
  \end{aligned}
$$


