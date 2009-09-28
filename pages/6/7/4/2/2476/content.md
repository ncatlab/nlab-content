A [[morphism]] $f : X \to Y$ of [[stack]]s over a [[site]] $C$ is called **representable** if for all [[representable functor|representable objects]] $U \in C \stackrel{Y}{\hookrightarrow} Stacks(C)$ and all [[morphism]]s $U \to Y$ the [[pullback]] $X \times_Y U$ in

$$
  \array{
    X \times_Y U &\to& X
    \\
    \downarrow && \downarrow^f
    \\
    U &\to& Y
  }
$$

is again representable.