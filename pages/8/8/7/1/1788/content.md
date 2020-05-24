

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