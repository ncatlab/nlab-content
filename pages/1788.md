
\linebreak

\linebreak


### Relation between 5d Maxwell theory and self-dual 3-forms in 6d

Consider 5d- and 6d-dimensional [[Minkowski spacetime]] equipped with global [[orthonormal basis|orthonormal]] [[coordinate charts]]  $\{x^\kappa\}$, $\{x^\alpha\}$, respectively, adapated to an [[isometry|isometric]] [[embedding of smooth manifolds|embedding]]

$$
  \array{
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
  d \widehat{B}
\]

for unique differential forms on $\mathbb{R}^{4,1}$

$$
  \widehat F 
    \;=\; 
  \tfrac{1}{2}\hat F_{\kappa_1 \kappa_2} 
  d x^{\kappa_1} \wedge d x^{\kappa_2} 
$$

and

$$
  \widehat{H}
    \;=\; 
  \tfrac{1}{3!} \widehat{H}_{\kappa_1 \kappa_2 \kappa_3} 
  d x^{\kappa_1} \wedge d x^{\kappa_2} \wedge d x^{\kappa_3} 
  \,.
$$

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

It follows that  the condition that $H_3$ be a [[closed differential form|closed]] and [[self-dual higher gauge theory|self-dual 3-form]] is equivalent to its 5d components $\widehat{H}$ ($\widehat{H}$) being the (dual) [[field strength]]/[[Faraday tensor]] satisfying the [[Maxwell equations]] of [[D=5 Maxwell theory]] (without [[source fields|source]] [[conserved current|current]]):

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
    H_3 = \widehat{F}\wedge d x^5 + \cdots
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

Essentially this relation underlies the [[Perry-Schwarz Lagrangian]] for the [[M5-brane]].


$$
  \sigma^\ast( e_{\mu 5'} )
  \;=\;
  d(
    e^{- x^4 m}  
    A_\mu
  )
  \phantom{AAAA}
  \sigma^\ast( e_{\mu_1 \mu_2} )
  \;=\;
  d(
    e^{ - x^4 m}
    B_{\mu \nu}
  )
$$


$$
  \begin{aligned}
    H_3
    & \coloneqq\;
    \sigma^\ast
    \big(
      e_{a_1 a_2}
     \wedge 
     e^{a_1}
     \wedge 
     e^{a_2}
    \big)
    +
    e_{ a_1 a_2 5'}{}^{4 5}
    \wedge 
    e^{a_1} 
    \wedge 
    e^{a_2}
    \big)
    \\
    & = \;
    e^{- x^4 m}
    \big(
      d A \wedge d x^{5'}
      -
      m\, A \wedge d x^4 \wedge d x^{5'}
      +
      d B 
      -
      m \, B \wedge d x^4
    \big)
  \end{aligned}
$$

$$
  \begin{aligned}
    \Rightarrow \;\;
    \star_{{}_{6'}} H_3 
    & = \;
    e^{- x^4 m}
    \big(
      \star_4 d A \wedge d x^4
      +
      m \, \star_4 A 
      -
      \star_4 d B  \wedge d x^4 \wedge d x^{5'}
      +
      m \, \star_4 B \wedge d x^{5'}
    \big)
  \end{aligned}
$$

$$
  \begin{aligned}
  \star_{{}_{6'}} H_3 
  =\;
  H_3
  & 
  \;\;\;
    \Leftrightarrow
  \;\;\;
  \left\{
    \begin{aligned}
      m \, B & =  - \star_{{}_4} d A
      \\
      \star_{{}_4} d B & = + m \, A
    \end{aligned}
  \right.
  \\
  & 
  \;\;\;
  \Leftrightarrow
  \;\;\;
  \left\{
    \begin{aligned}
      B & = \frac{1}{m} \star_{{}_4} d A
      \\
      \star_{{}_4} d \star_{{}_4} d A & = 
      - m^2 A 
    \end{aligned}
  \right.
  \\
  & 
  \;\;\;
  \Leftrightarrow
  \;\;\;
  \left\{
    \begin{aligned}
      B & = \frac{1}{m} \star_{{}_4} d A
      \\
      \partial_\mu \partial^\mu A & = 
      m^2 A 
    \end{aligned}
  \right.
  \end{aligned}
$$

\linebreak

\linebreak
  
\linebreak

***


\linebreak

\linebreak


If I understand well what you're after, you want to show that a ultracategory is just a $T$-algebra for a suitable monad.

My claim is that the monad acts as follows on objects:

$$ T : \mathcal{A} \mapsto \int^X \beta(X)\times \mathcal{A}^X $$ 

I am basing this conjecture on the fact that an ultracategory consists of maps

$$ i_X : \beta(X)\times \mathcal{A}^X \to \mathcal{A} $$ 

that if this conjecture is correct amount exactly to a functor $T\mathcal{A} \to \mathcal{A}$ (by the universal property of the coend, the $i_X$ forming a cowedge in $X$).

Of course, strictly speaking $T$ does not exist, because as $X$ ranges over all sets the coend I'm taking is on too large a diagram. I kindly ask you to set aside size issues and follow a bit of coend-nonsense: so, just for today $T$ exists and defines a functor.

1. First, the initial cowedge $i_X : \beta(X) \times \mathcal{A}^X \to TA$ has a component at $X=1$, the terminal category; this gives $T$ the structure of a pointed functor (of course, $i$ depends naturally on $\mathcal{A}$).

2. A candidate multiplication map $TT\mathcal{A} \to T\mathcal{A}$ can be obtained as follows:

$$\begin{array}{rl} 
TT\mathcal{A} &= \displaystyle \int^Y \beta(Y) \times T\mathcal{A}^Y \\
&\displaystyle  = \int^Y \beta(Y) \times \left( \int^X \beta(X)\times \mathcal{A}^X \right)^Y \\
&\displaystyle \to \int^Y\int^X \beta(Y) \times  \beta(X)^Y \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \int^Y\int^X \beta(Y) \times  \beta\beta(X)^{\beta Y} \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \int^Y\int^X \beta\beta(X) \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \int^Y\int^X \beta (X) \times \mathcal{A}^{X\times Y} \\
&\displaystyle \to \text{colim}_Y\int^X \beta (X) \times \mathcal{A}^{X\times Y} \\
&\displaystyle \cong \int^X \beta (X) \times \mathcal{A}^{X}
\end{array}$$