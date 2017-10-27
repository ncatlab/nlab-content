


Let $X,Y$ be [[formal smooth sets]] (def. \ref{FormalSmoothSet}). Then a morphism between them is called a _[[local diffeomorphism]]_ or _[[formally étale morphism]]_, denoted 

$$
  f \;\colon\; X \overset{et}{\longrightarrow} Y
$$

if $f$ if for each [[infinitesimally thickened smooth manifold|infinitesimally thickened Cartesian space]] (def. \ref{InfinitesimallyThickendSmoothManifold}) $\mathbb{R}^n \times \mathbb{D}$ we have a natural identification between the $\mathbb{R}^n \times \mathbb{D}$-plots of $X$ with those $\mathbb{R}^n n\times \mathbb{D}$-plots of $Y$ whose [[reduction modality|reduction]] (def. \ref{ReductionAndInfinitesimalShape}) comes from an $\mathbb{R}^n$-plot of $X$, hence if we have a [[natural transformation|natural]] [[fiber product]] of [[sets]] of [[plots]]

$$
  X(\mathbb{R}^n \times \mathbb{D})
  \;\simeq\;
  Y(\mathbb{R}^n \times \mathbb{D})
    \underset{Y(\mathbb{R}^n)}{\times^f}
  X(\mathbb{R}^n)
  \phantom{AAA} \text{i.e.}
  \phantom{AAA}
  \array{
     && X(\mathbb{R}^n \times \mathbb{D})
     \\
     & \swarrow && \searrow
     \\
     Y(\mathbb{R}^n \times \mathbb{D}) && \text{(pb)} && X(\mathbb{R}^n)
     \\
     & \searrow && \swarrow
     \\
     && Y(\mathbb{R}^n \times \mathbb{D})
  }
$$

for all $\mathbb{R}^n \times \mathbb{D} \in InfThCartSp$.

Stated more [[category theory|abstractly]], this means that the
[[naturality square]] of the [[unit of a monad|unit]] of the [[infinitesimal shape]] $\Im$ (def. \ref{ReductionAndInfinitesimalShape}) is a [[pullback square]]

$$
  \array{
    X &\overset{\eta_X}{\longrightarrow}& \Im X
    \\
    {}^{\mathllap{f}}\downarrow &\text{(pb)}& \downarrow^{\mathrlap{\Im f}}
    \\
    Y &\underset{\eta_Y}{\longrightarrow}& \Im Y
  }
$$


$\,$

$$
  \array{
    \mathbb{D}^1 &\overset{i}{\hookrightarrow}& \mathbb{R}^1
    \\
    & {}_{\mathllap{(\epsilon \mapsto f(0) + \frac{\partial f}{\partial x}(0) \epsilon) }}\searrow & \downarrow_{\mathrlap{f}}
    \\
    && \mathbb{R}^1
  }
$$
