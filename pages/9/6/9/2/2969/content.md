A map $i:A\to X$  of topological spaces is said to satisfy the **homotopy extension property** (HEP) with respect to a space $Z$ if for any map $\tilde{f}:X\to Z$ and a homotopy $F:X\times I\to Z$ such that $F(-,0)=\tilde{f}\circ i$, a homotopy $\tilde{F}:X\times I\to Z$ exists such that $\tilde{F}\circ (i\times id_I)=F$. Denote $f:=\tilde{f}\circ i=F(-,0)$; then this is expressed by means of the commutative diagram

$$\array{
A & &\stackrel{i}\to && X\\
&\searrow^f&&\swarrow^{\tilde{f}}&\\
{}^{\sigma_0}\downarrow & &Y&& \downarrow^{\sigma_0}\\
&\nearrow{F}&&\nwarrow{\exists\tilde{F}}&\\
A\times I &&\stackrel{i\times id}\to&&X\times I
}$$

Here we denoted $\sigma_0:x\mapsto (x,0)$, so that $F\circ\sigma_0=F(-,0)$.

Surely it is superfluous to write the arrow $f:A\to Z$ as if we erase it, the commutativity still has a commuting square around it saying $F\circ\sigma_0=\tilde{f}\circ i$, but it is conceptually nice to think of $\tilde{f}$ as extending some $f:=F\circ\sigma_0$. 

One can instead of the diagram above write a diagram involving adjoint maps. In other words, instead of any homotopy $h:A\times I\to Z$ we use the exponential law to write $h':A\to Z^I$ where the correspondence is given by the formula $h'(a)(t)=f(a,t)$. Then the homotopy lifting property is the existence of the diagonal map $\tilde{F}'$ in the diagram:

$$
  \array{
    A &\stackrel{F'}\to& Y^I
    \\
    \downarrow^{i} &{}^{\exists\tilde{F}'}\nearrow&  \downarrow^{ev_0}
    \\
    X&\stackrel{\tilde{f}}{\to}& Y
  }
  \,.
$$

where $ev_0:Y^I\to Y$ is the map of evaluation at zero $u\mapsto u(0)$. This is an instance of [[right lifting property]] with respect to maps $ev_0$. 

A map is [[Hurewicz cofibration]] if it satisfies the homotopy extension property with respect to all spaces.

**Proposition.** If a map $i:A\to X$ has a homotopy extension property with respect to a space $Y$ then for any map $g:A\to Z$, the pushout $g_*(i)=i\coprod_A Z :Z\to X\coprod_A Z$ has the homotopy extension property with respect to the space $Y$. 

*Proof.* we would like to find $\tilde{F}$ to complete the commutative diagram 

$$
  \array{
    A &\stackrel{g}\to&Z&\stackrel{f}\to& Y^I
    \\
    \downarrow^{i}&&\downarrow^{g_*(i)} &\nearrow {\tilde{F}}&  \downarrow^{ev_0}
    \\
    X&\stackrel{i_*(g)}\to&X\coprod_A Z&\stackrel{F}{\to}& Y
  }
  \,.
$$

Consider the external square obtained by composing the horizontal arrows:

$$
  \array{
    A &\stackrel{f\circ g}\to& Y^I
    \\
    \downarrow^{i} &\nearrow {\exists\tilde{G}}&  \downarrow^{ev_0}
    \\
    X&\stackrel{F\circ i_*(g)}{\to}& Y
  }
  \,.
$$

By the assumption on $i$, there is $\tilde{G}$ such that both triangles commute.

If $i:A\to X$ is satisfying the HEP with respect to $Y$ then there is a diagonal in that external square which is some map $\tilde{G}:X\to Y^I$. This map together with $f:Z\to Y^I$, by the universal property of pushout, determines a unique map $\tilde{F}:X\coprod_A Z\to Y^I$ such that $\tilde{F}\circ i_*(g)=\tilde{G}$ and $\tilde{F}\circ g_*(i)=f$. We need to show that 
$ev_0\circ\tilde{F}=F$ and $\tilde{F}\circ g_*(i)=f$.

By the definition of $\tilde{G}$ and the commutativity of the original double square diagram, $ev_0\circ \tilde{F}\circ i_*(g)=ev_0\circ\tilde{G}=F\circ i_*(g)$ and $f\circ g = \tilde{G}\circ i = \tilde{F}\circ i_*(g)\circ i = \tilde{F}\circ g_*(i)\circ g$. This is almost what we wanted except that we precompose the wanted identities with certain maps. If we could cancel $i_*(g)$ in the first and $g$ in the second identity we are done. But we can do this by the uniqueness part of the universal property of pushout. 