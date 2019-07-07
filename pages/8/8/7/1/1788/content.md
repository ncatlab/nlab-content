$\ldots$

[[!-modality]]

***

$$
  \begin{aligned}
    \exp\big(  -t^a \wedge \iota_a \big)
    \big(
      d_{dR} + d_W 
    \big)
    \exp\big( t^a \wedge \iota_a \big)
    & = 
    d_{dR} + d_W 
    + 
    \big[
      d_{dR} + d_W,
      t^a \wedge \iota_a
    \big]
    + 
    \tfrac{1}{2}
    \Big[
    \big[
      d_{dR} + d_W,
      t^a \wedge \iota_a
    \big],
      t^a \wedge \iota_a    
    \Big]
    \\
    & =
    d_{dR} + d_W 
    \\
    & \phantom{=}
    +
    \underset{
       - \tfrac{1}{2}f^a_{b c} t^b \wedge t^c + r^a
    }{
      \underbrace{
        \big[ 
          d_W
          ,
          t^a
       \big]
      }
    }
    \wedge
    \iota_a
    -
    t^a 
     \wedge
    \underset{
      = \mathcal{L}_{a}
    }{
      \underbrace{
        \big[ d_{dR} + d_W,  \iota_a  \big]
      }
    }
    \\
    & \phantom{=}
     + 
    \tfrac{1}{2}
    \Big[
    \underset{
      \mathclap{
         - \tfrac{1}{2}f^a_{b c} t^b \wedge t^c \iota_a
         + r^a \iota_a
         - t^a \mathcal{L}_a
      }
    }{
    \underbrace{
    \big[
      d_{dR} + d_W,
      t^a \wedge \iota_a
    \big]
    }
    }
    ,
      t^a \wedge \iota_a    
    \Big]   
  \end{aligned}
$$

(wait...)


a [[circle-principal bundle]]

\begin{xymatrix}
  S^1 \ar[r] 
  &
  \Sigma^6
  \ar[d]
  \\
  & \Sigma^5
\end{xymatrix}

An [[Ehresmann connection]]

$$
  \theta^5
  \;\in\;
  \Omega^1\big( \Sigma^6 \big)
$$

$$
  H \;\in\; \Omega^3\big(\Sigma^6\big)
$$


$$
  H = d B
$$

$$
  H 
  \;=\;
  \star_6 
  H
$$

$$
  \tilde H
  \coloneqq
  \star_5 H
  \coloneqq
  \star_5 
  \big(
    H - \mathcal{F} \wedge d x^5
  \big)
$$

$$
  A
  \;\coloneqq\;
  \iota_5 B
$$

$$
  B
  \;=\;
  A \wedge d x^5
  +
  B^{\mathrm{bas}}
$$

$$
  F 
  \coloneqq
  d_5 A
$$

$$
  \begin{aligned}
    \mathcal{F}
    &\coloneqq
    \iota_5 H
    \\
    & =
    \iota_5 d B
    \\
    & =
    -d \iota_5 B + [\iota_5, d] B
    \\
    & =
    - d A + \mathcal{L}_5 B
    \\
    & =
    - F - \mathcal{L}_5 A \wedge d x^5 + \mathcal{L}_5 ( A \wedge d x^5 + B^{basic} )
    \\
    & =
    - F + \mathcal{L}_5 B^{bas}
  \end{aligned}
$$

$$
  \star_6 H
  =
  \star_6
  \big(
    \mathcal{F} \wedge d x^5
    +
    (H - \mathcal{F} \wedge d x^5)
  \big)
  =
  \star_5 \mathcal{F}
  + 
  \tilde H \wedge d x^5
$$
