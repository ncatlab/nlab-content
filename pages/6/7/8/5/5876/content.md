Let $D=(D_1, D_0)$ be a [[double category]].  A **connection** on $D$ is given by a pair of functions $\Gamma, \Gamma' \colon \mathrm{arr} D_0 \to \mathrm{arr} D_1$, that assign to each vertical morphism $f \colon Y \to X$ cells of the form
$$
\begin{matrix}
  Y & \overset{f^*X}{\to} & X \\
  \mathllap{f} \downarrow & \mathllap{\Gamma f} \Downarrow &   \downarrow \mathrlap{1} \\
  X & \underset{\iota_X}{\to} & X
\end{matrix}
\qquad \qquad
\begin{matrix}
  Y & \overset{\iota_Y}{\to} & Y \\
  \mathllap{1} \downarrow & \Downarrow \mathrlap{\Gamma' f} & \downarrow \mathrlap{f} \\
  Y & \underset{f^*X}{\to} & X
\end{matrix}
$$
(where $\iota_X$ is the horizontal identity on $X$) such that $\Gamma$ and $\Gamma'$ behave suitably with respect to composition and identities in $D_0$:

...

(that is, they are identity-on-objects functors) and such that the vertical composite $\Gamma'(f) \cdot \Gamma(f) = \iota_f$ and the horizontal composite $\Gamma(f) \circ \Gamma'(f) = 1_{f^*X}$, (that is, $f$ and $f^*X$ are [[companions]]).

