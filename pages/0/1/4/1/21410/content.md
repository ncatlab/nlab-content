### Relation between 5d Maxwell theory and self-dual 3-forms in 6d

Consider 5d- and 6d-dimensional [[Minkowski spacetime]] equipped with global [[orthonormal basis|orthonormal]] [[coordinate charts]]  $\{x^\kappa\}$, $\{x^\alpha\}$, respectively, adapated to an [[isometry|isometric]] [[embedding of smooth manifolds|embedding]]

$$
  \array{
   &
    \mathbb{R}^{4,1}
    &\overset{\;\;\;\iota_5\;\;\;}{\hookrightarrow}&
    \mathbb{R}^{5,1}
    \\
    \kappa = &   0, 1, 2, 3, 4\phantom{,}
    \\
    \alpha = & 0, 1, 2, 3, 4, && 5
  }
$$

With this notation, the [[pullback of differential forms]] along this embedding is notationally implicit.


Now any [[differential 3-form]] $H_3$ on $\mathbb{R}^{5,1}$ decomposes as

\[
  \label{5dDecompositionof3Form}
  H_3
  \;=\;
  \widehat{F} \wedge d x^{5}
  +
  \widehat{H}
\]

for unique differential forms of the form

$$
  \widehat F
    \;=\; 
  \tfrac{1}{2}\hat F_{\kappa_1 \kappa_2}(x^\kappa, x^5)
  d x^{\kappa_1} \wedge d x^{\kappa_2} 
$$

and

$$
  \widehat{H}
    \;=\; 
  \tfrac{1}{3!} \widehat{H}_{\kappa_1 \kappa_2 \kappa_3}(x^\kappa, x^5) 
  d x^{\kappa_1} \wedge d x^{\kappa_2} \wedge d x^{\kappa_3} 
  \,.
$$

In the case that $H_3$ has vanishing [[Lie derivative]] along the $x^5$-direction, 

\[
  \label{VanishingLieDerivateiveAlongx5}
  \mathcal{L}_5 H_3 \;=\; 0
\] 

then also these components forms do not depend on $x^5$ are actualls [[pullback of differential forms|pullbacks]] of differential forms on $\mathbb{R}^{4,1}$.

In terms of this decomposition, the 6d [[Hodge dual]] of $H_3$ is equivalently given by the 5d [[Hodge duals]] of these components as (best seen by the relation to [[Hodge pairing]] according to [this Prop.](Hodge+star+operator#HodgePairing))

\[
  \label{6dHodgeDualityInTermsOf5d}
  \star_6 H_3 
  \;=\;
  \big( \star_5 \widehat{H}\big) \wedge d x^{5}
  -
  \star_5 \widehat{F} 
\]

Since the [[Hodge star operator]] squares to unity in the special case that it is applied to differential 3-forms on 6d Minkowski spacetime (by [this Prop.](Hodge+star+operator#HodgeStarFollowedByHodgeStar))

$$
  \star_6 \star_6 H_3 \;=\; + H_3
$$

we may ask for $H_3$ to he [[Hodge duality|Hodge self-dual]]. By (eq:6dHodgeDualityInTermsOf5d) this means equivalently that its 5d components are 5d Hodge duals of each other:


$$
  \big(
    H_3 
    \;=\;
    \star_{6} H_3
  \big)
  \;\;\;
  \overset{
    H_3 = \widehat{F} \wedge d x^5 + \widehat{H}
  }{
    \Leftrightarrow
  }
  \;\;\;
  \big(
    \widehat{H} = \star_5 \widehat{F}
  \big)
  \,.
$$

It follows that if there is no $x^5$-dependence (eq:VanishingLieDerivateiveAlongx5) then the condition that $H_3$ be a [[closed differential form|closed]] and [[self-dual higher gauge theory|self-dual 3-form]] is equivalent to its 5d components $\widehat{F}$ ($\widehat{H}$) being the (dual) [[field strength]]/[[Faraday tensor]] satisfying the [[Maxwell equations]] of [[D=5 Maxwell theory]] (without [[source fields|source]] [[conserved current|current]]):

$$ 
  \underset{
    \color{blue}
    {
    {\phantom{A}}
    \atop
    {\text{D=6 self-dual 3-form theory}}
    }
  }{
  \left.
  \array{
    & 
    d H_3 = 0
    \\
    &
    \star_6 H_3 = H_3
  }
  \right\}
  }
  \;\;\;
  \overset{
    {\mathcal{L}_{5} H_3 = 0}
    \atop
    {H_3 = \widehat{F}\wedge d x^5 + \cdots}
  }{
    \Leftrightarrow
  }
  \;\;\;
  \underset{
    \color{blue}
    {
    {\phantom{A}}
    \atop
    \text{D=5 Maxwell theory}
    }
  }{
  \left\{
  \array{
    & 
    d \widehat{F} = 0
    \\
    &
    d \star_5 \widehat{F} = 0
  }
  \right.  
  }
$$

This may be summarized as saying that the massless part of the [[Kaluza-Klein reduction]] of [[self-dual higher gauge theory|self-dual 3-form theory]] from 6d to 5d  is [[D=5 Maxwell theory]].

Essentially this relation underlies the formulation of the [[M5-brane]] via the [[Perry-Schwarz Lagrangian]].
