
Let $\mathcal{C}$ be a [[small category]]. Let $\mathcal{D}$ be a [[category]] with all [[colimits]].

$$
  \array{
    && \mathcal{C}
    \\
    & {}^{y}\swarrow &\swArrow& \searrow^{\mathrlap{F}}
    \\
    \mathrlap{ \!\!\!\!\!\!\!\!\!\!\!\!\! [\mathcal{C}^{op}, Set] }
      && \underset{ \widetilde F }{\longrightarrow} &&
    \mathcal{D}
  }
$$

$$
  \begin{aligned}
    \widetilde F(\mathbf{X})
    & =
    \widetilde F
    \left(
      \int^{c \in \mathcal{C}} y(c) \cdot \mathbf{X}(c)
    \right)
    & \coloneqq 
    \int^{c \in \mathcal{C}} F(c) \cdot \mathbf{X}(c)
  \end{aligned}
$$