
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
