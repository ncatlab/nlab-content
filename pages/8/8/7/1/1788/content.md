
### Hodge star operator on Minkowski spacetime

We spell out component expressions for the [[Hodge star operator]] on $D = d+1$-dimensional [[Minkowski spacetime]].

### Conventions

We use [[Einstein summation convention]] throughout. Hence a generic [[differential p-form]] is 

$$
  \alpha
  \;=\;
  \tfrac{1}{p!}
  \alpha_{ \mu_1 \cdots \mu_p }
  d x^{\mu_1}
  \wedge 
  \cdots
  \wedge
  d x^{\mu_p}
  \,.
$$

Here $p! \coloneqq 1 \cdot 2 \cdot 3 \cdots p$ is the [[factorial]] of $p$.

We take the [[Minkowski metric]] to be the $D \times D$ [[diagonal matrix]] of the form

$$
  \eta 
  \;=\;
  (\eta_{\mu \nu})
  \;=\;
  (\eta^{\mu \nu})
  \;\coloneqq\;
  diag(-1,+1, +1 , \cdots , +1)
  \,.
$$


We normalize the [[Levi-Civita symbol]] as

\[
  \label{LCSymbolDown}
  \epsilon_{0 1 2 \cdots d}
  \;\coloneqq\;
  + 1
\]

which means that 

\[
  \label{LCSymbolUp}
  \epsilon^{0 1 2 \cdots d}
  \;=\;
  - 1
  \,.
\]

We normalize the sign of the [[volume form]] as

\[
  \label{VolumeForm}
  \begin{aligned}
  dvol
  & \coloneqq\;
  d x^0 \wedge d x^1 \wedge \cdots \wedge d x^d
  \\
  & = 
  \tfrac{1}{D!} 
  \epsilon_{
    \color{green}
    \mu_1 \cdots \mu_D
  } 
  d x^{\color{green}\mu_1} 
   \wedge 
   \cdots 
   \wedge 
  d x^{\color{green}\mu_D}
  \end{aligned}
\]


We write 

\[
  \label{GeneralizedKroneckerDelta}
  \delta^{ \mu_1 \cdots \mu_p }_{ \nu_1 \cdots \nu_p }
  \;\coloneqq\;
  \left\{
  \array{
    sgn(\sigma) 
     &\vert&  
    \underset{ \sigma \in Sym(p) }{\exists} 
    \left(
      \underset{1 \leq i \leq p}{\forall}
      \left(
        \nu_{\sigma(i)} = \mu_i
      \right)
    \right)
    \\
    0 &\vert& \text{otherwise}
  }
  \right.
\]

for the generalized [[Kronecker delta]], whose value is the [[signature of a permutation|signature]] of the [[permutation]] that takes the upper indices to the lower indices, if any such exists, and [[zero]] otherwise.

This appears whenever the [[Levi-Civita symbol]] is contracted with itself:

\[
  \label{ContractionofLeviCivitaSymbols}
  \epsilon_{
     { \color{green} \mu_1 \cdots \mu_p }
     {\color{blue} \mu_{p+1} \cdots \mu_{D} }
  }
  \epsilon^{ 
    { \color{orange} \nu_1 \cdots \nu_p } 
    { \color{blue} \mu_{p+1} \cdots \mu_D }
  }
  \;=\;
  { \color{magenta} - }
  (D-p)!
  \;
  \delta_{ 
    \color{green} \mu_1 \cdots \mu_p 
  }^{
    \color{orange} \nu_1 \cdots \nu_p
  }
\]

Notice the minus sign in (eq:ContractionofLeviCivitaSymbols), which comes, via (eq:LCSymbolUp), from the [[Minkowski spacetime|Minkowski]] [[signature of a quadratic form|signature]].


We write $\iota_\mu$ for the operator of contraction of [[differential forms]] with the [[vector field]] $d/d x^\mu$, hence the [[linear operator]] on [[differential forms]] with [[anticommutator]]

$$
  \big\{
    \iota_\mu, d x^\nu \wedge
  \big\}
  \;=\;
  \delta_\mu^\nu
$$


With the [[volume form]] as in (eq:VolumeForm) it follows that
(notice the reversion of the index ordering in the contraction operators $\iota$)

\[
  \label{ContractionIntoVolumeForm}
  \alpha^{
    \color{green}
    \mu_1 \cdots \mu_p
  }
  \iota_{\color{green} \mu_p} 
     \cdots 
   \iota_{ \color{green} \mu_1}
  dvol
  \;=\;
  \epsilon_{ 
    { \color{green} \mu_1 \cdots \mu_p }
    { \color{orange} \nu_1 \cdots \nu_{(D-p)}  }
  }
  d x^{\color{orange} \nu_1} 
    \wedge 
    \cdots 
    \wedge 
  d x^{\color{orange} \nu_{(D-p)}}
\]



### Definition

+-- {: .num_defn} 
###### Definition

For a [[differential p-form]]

$$
  \alpha
  \;\coloneqq\;
  \tfrac{1}{ \color{green} p! }
  \alpha_{ \color{green} \mu_1 \cdots \mu_p}
  d x^{ \color{green} \mu_1 }
    \wedge \cdots \wedge
  d x^{ \color{green} \mu_p }
$$

its [[Hodge dual]] is:

\[
  \label{HodgeStar}
  \begin{aligned}
  \star 
  \alpha
  & \coloneqq
  \tfrac{1}{ 
    { \color{green} p! }
    { \color{orange} (D-p)! }
  }
  \,
  \alpha^{ \color{green} \mu_1 \cdots \mu_p }
  \iota_{ \color{green} \mu_p }
  \cdots 
  \iota_{ \color{green} \mu_1 }
  \, 
  dvol
  \\
  & =
  \tfrac{1}{ 
    { \color{green} p! }
    { \color{orange} (D-p)! }
  }
  \,
  \alpha^{ \color{green} \mu_1 \cdots \mu_p }
  \epsilon_{ 
     { \color{green} \mu_1 \cdots \mu_p }
     { \color{orange} \mu_{p+1} \cdots \mu_D }
  }
  \, 
  d x^{ \color{orange} \mu_{p+1} }
  \wedge
  \cdots
  \wedge
  d x^{ \color{orange} \mu_D }
  \end{aligned}
\]

=--

## Properties

+-- {: .num_prop} 
###### Proposition

For a [[differential p-form]]
$
  \alpha
  \;\coloneqq\;
  \tfrac{1}{p!}
  \alpha_{\mu_1 \cdots \mu_p}
  d x^{\mu_1}
    \wedge \cdots \wedge
  d x^{\mu_p}
$
on $D$-dimensional [[Minkowski spacetime]]
its [[wedge product]] with its [[Hodge dual]] (eq:HodgeStar) is


\[
  \label{AlphaWedgeStarAlpha}
  \alpha \wedge \star \alpha
  \;=\;
  { \color{magenta} - } 
  \alpha_{ \mu_1 \cdots \mu_p }
  \alpha^{ \mu_1 \cdots \mu_p }
  \,
  dvol
\]

=--

+-- {: .proof}
###### Proof

$$
  \begin{aligned}
    \alpha \wedge \star \alpha
    & =
    \tfrac{1}{  
      { \color{green}  p! }
      { \color{orange} p! } 
      { \color{blue} (D-p)! }
    }
    \alpha_{ \color{green} \mu_1 \cdots \mu_p }
    d x^{ \color{green} \mu_1 }
    \wedge \cdots \wedge
    d x^{ \color{green} \mu_p }
    \wedge
    \alpha^{ \color{orange} \nu_1 \cdots \nu_p }
    \iota_{ \color{orange} \nu_p }
    \cdots
    \iota_{ \color{orange} \nu_1 }
    dvol
    \\
    & = 
    \tfrac{1}{  
      { \color{green}  p! }
      { \color{orange} p! } 
      { \color{blue} (D-p)! }
    }
    \alpha_{ \color{green} \mu_1 \cdots \mu_p }
    \alpha^{ \color{orange} \nu_1 \cdots \nu_p }
    \epsilon_{ 
      { \color{orange} \nu_1 \cdots \nu_p }
      { \color{blue} \nu_{p+1} \cdots \nu_D  }
    }
    d x^{ \color{green} \mu_p }
    \wedge \cdots \wedge
    d x^{ \color{green} \mu_1 }
    \wedge
    d x^{ \color{blue} \nu_{p+1} }
    \wedge
    \cdots
    d x^{ \color{blue} \nu_{D} }
    \\
    & =
    \tfrac{1}{  
      { \color{green}  p! }
      { \color{orange} p! } 
      { \color{blue} (D-p)! }
    }
    \alpha_{ \color{green} \mu_1 \cdots \mu_p }
    \alpha^{ \color{orange} \nu_1 \cdots \nu_p }
    \epsilon_{ 
      { \color{orange} \nu_1 \cdots \nu_p }
      { \color{blue} \nu_{p+1} \cdots \nu_D  }
    }
    \epsilon^{ 
      { \color{green} \mu_p \cdots \mu_1 } 
      { \color{blue} \nu_{p+1} \cdots \nu_{D} }
    }
    \, 
    dvol
    \\
    & =
    \tfrac{ \color{magenta} -1 }{  
      { \color{green}  p! }
      { \color{orange} p! } 
    }
    \alpha_{ \color{green} \mu_1 \cdots \mu_p }
    \alpha^{ \color{orange} \nu_1 \cdots \nu_p }
    \delta^{ \color{green} \mu_1 \cdots \mu_p }_{ \color{orange} \nu_1 \cdots \nu_p }
    \, 
    dvol
    \\
    & =
    {\color{magenta} -}
    \alpha_{ \mu_1 \cdots \mu_p }
    \alpha^{ \mu_1 \cdots \mu_p }
    \,
    dvol
  \end{aligned}
$$

=--

+-- {: .num_prop} 
###### Proposition

For a [[differential p-form]] 
$
  \alpha 
  \;=\; 
  \tfrac{1}{p!}
  \alpha_{\mu_1 \cdots \mu_p} 
  d x^{\mu_1} \wedge \cdots \wedge d x^{\mu_p}
$ 
on $D$-dimensional [[Minkowski spacetime]], its double [[Hodge dual]] (eq:HodgeStar) is

\[
  \label{DoubleHodgeDual}
  \star \star \alpha
  \;=\;
  {\color{magenta} -} 
  (-1)^{ p (D - p) }
  \,
  \alpha
\]

=--

+-- {: .proof}
###### Proof

$$
  \begin{aligned}
    & 
    \star \star 
    \tfrac{1}{ \color{green} p! }
    \alpha_{ \color{green} \mu_1 \cdots \mu_p}
    d x^{ \color{green} \mu_1 } 
      \wedge 
      \cdots 
      \wedge 
    d x^{ \color{green} \mu_p }
    \\
    & =
    \star 
    \tfrac{1}{
      { \color{green} p! }
      { \color{orange} (D-p)! }
    }
    \alpha^{ \color{green} \mu_1 \cdots \mu_p} 
    \iota_{ \color{green} \mu_p} \cdots \iota_{ \color{green} \mu_1} 
    dvol
    \\
    & = 
    \star 
    \tfrac{1}{
      { \color{green} p! }
      { \color{orange} (D-p)! }
    }
    \alpha^{ \color{green} \mu_1 \cdots \mu_p } 
    \epsilon_{
       { \color{green} \mu_1 \cdots \mu_p }
       { \color{orange} \mu_{p+1} \cdots \mu_D }
    }
    d x^{\color{orange} \mu_{p+1}} \wedge \cdots d x^{ \color{orange} \mu_d}
    \\
    & =
    \tfrac{1}{
      { \color{green} p! }
      { \color{orange} (D-p)! }
      { \color{blue} p! }
    }
    \alpha_{ \color{green} \mu_1 \cdots \mu_p } 
    \epsilon^{
       { \color{green} \mu_1 \cdots \mu_p }
       { \color{orange} \mu_{p+1} \cdots \mu_D }
    }
    \epsilon_{
      { \color{orange} \mu_{p+1} \cdots \mu_D }
      { \color{blue} \nu_1 \cdots \nu_p  }
    }
    \,
    d x^{ \color{blue} \nu_1} 
      \wedge 
        \cdots 
      \wedge 
    d x^{ \color{blue} \nu_D }
    \\
    \\
    & =
    \tfrac{
     (-1)^{ {\color{green} p} { \color{orange}  (D-p) } }
    }{
      { \color{green} p! }
      { \color{orange} (D-p)! }
      { \color{blue} p! }
    }
    \alpha_{ \color{green} \mu_1 \cdots \mu_p } 
    \epsilon^{
       { \color{green} \mu_1 \cdots \mu_p }
       { \color{orange} \mu_{p+1} \cdots \mu_D }
    }
    \epsilon_{
      { \color{blue} \nu_1 \cdots \nu_p  }
      { \color{orange} \mu_{p+1} \cdots \mu_D }
    }
    \,
    d x^{ \color{blue} \nu_1} 
      \wedge 
        \cdots 
      \wedge 
    d x^{ \color{blue} \nu_D }
    \\
    & =
    {\color{magenta} -}
    \tfrac{
      (-1)^{ {\color{green}p} {\color{orange} (D-p) } }
    }{
      { \color{green} p! }
      { \color{blue} p! }
    }
    \alpha_{ \color{green} \mu_1 \cdots \mu_p } 
    \delta^{
       { \color{green} \mu_1 \cdots \mu_p }
    }_{
      { \color{blue} \nu_1 \cdots \nu_p  }
    }
    \,
    d x^{ \color{blue} \nu_1} 
      \wedge 
        \cdots 
      \wedge 
    d x^{ \color{blue} \nu_D }
    \\
    & =
    {\color{magenta} -}
    (-1)^{ {\color{green}p} {\color{orange} (D-p) } }
    \,
    \alpha
  \end{aligned}
$$


=--

+-- {: .num_prop} 
###### Proposition

Let 
$
  \alpha
  =
  \tfrac{1}{p!}
  \alpha_{\mu_1 \cdots \mu_p}
  d x^{\mu_1} 
    \wedge
    \cdots
    \wedge
  d x^{\mu_p}
$
be a [[differential p-form]] 
on $D$-dimensional [[Minkowski spacetime]]
such that 
$$
  \partial^\nu \alpha_{\nu \mu_1 \cdots \mu_{p-1}}
  \;=\;
  0
  \,.
$$

Then

$$
  \star d \star d \alpha
  \;=\;
  { \color{magenta} - }
  \partial^\nu \partial_\nu \alpha
  \,.
$$

=--

+-- {: .proof}
###### Proof

$$
  \begin{aligned}
    &
    \star d \star d 
    \tfrac{1}{ \color{green} p! }
    \alpha_{ \color{green} \mu_1 \cdots \mu_p }
    d x^{ \color{green} \mu_1 }
      \wedge
      \cdots
      \wedge
    d x^{ \color{green} \mu_p }
    \\
    & =
    \star d \star 
    \tfrac{1}{ \color{green} p! }
    \partial_{ \color{magenta} \nu } 
    \alpha_{ \color{green} \mu_1 \cdots \mu_p }
    d x^{ \color{magenta} \nu }
    \wedge
    d x^{ \color{green} \mu_1 }
      \wedge
      \cdots
      \wedge
    d x^{ \color{green} \mu_p }    
    \\
    & =
    \star d 
    \tfrac{1}{ 
      { \color{green} p! } 
      { \color{orange} (D-(p+1))! }
    }
    \partial^{ \color{magenta} \nu } 
    \alpha^{ \color{green} \mu_1 \cdots \mu_p }
    \epsilon_{
      { \color{magenta} \nu }
      { \color{green} \mu_1 \cdots \mu_{p} }
      { \color{orange} \mu_{p+2} \cdots \mu_D }
    }
    \,
    d x^{ \color{orange} \mu_{p+2} }
      \wedge
      \cdots
      \wedge
    d x^{ \color{orange} \mu_D }
    \\
    & =
    \star
    \tfrac{1}{ 
      { \color{green} p! } 
      { \color{orange} (D-(p+1))! }
    }
    \partial_{ \color{red} \nu' }
    \partial^{ \color{magenta} \nu } 
    \alpha^{ \color{green} \mu_1 \cdots \mu_p }
    \epsilon_{
      { \color{magenta} \nu }
      { \color{green} \mu_1 \cdots \mu_p }
      { \color{orange} \mu_{p+2} \cdots \mu_D }
    }
    \,
    d x^{ \color{red} \nu' }
    \wedge
    d x^{ \color{orange} \mu_{p+2} }
      \wedge
      \cdots
      \wedge
    d x^{ \color{orange} \mu_D }
    \\
    & =
    \tfrac{1}{ 
      { \color{green} p! } 
      { \color{orange} (D-(p+1))! }
      { \color{blue} p! }
    }
    \partial^{ \color{red} \nu' }
    \partial_{ \color{magenta} \nu } 
    \alpha_{ \color{green} \mu_1 \cdots \mu_p }
    \epsilon^{
      { \color{magenta} \nu }
      { \color{green} \mu_1 \cdots \mu_p }
      { \color{orange} \mu_{p+2} \cdots \mu_D }
    }
    \epsilon_{
      { \color{red} \nu' }
      { \color{orange} \mu_{p+2} \cdots \mu_D }
      { \color{blue} \kappa_1 \cdots \kappa_p }
    }
    \,
    d x^{\color{blue} \kappa_1} \wedge \cdots d x^{\color{blue}\kappa_p}
    \\
    & =
    { \color{magenta} - }
    \tfrac{1}{ 
      { \color{green} p! } 
      { \color{blue} p! }
    }
    \partial^{ \color{red} \nu' }
    \partial_{ \color{magenta} \nu } 
    \alpha_{ \color{green} \mu_1 \cdots \mu_p }
    \delta^{
      { \color{magenta} \nu }
      { \color{green} \mu_1 \cdots \mu_p }
    }
    _{
      { \color{red} \nu' }
      { \color{blue} \kappa_1 \cdots \kappa_p }
    }
    \,
    d x^{\color{blue} \kappa_1} \wedge \cdots d x^{\color{blue}\kappa_p}
    \\
    & =
    { \color{magenta} - }
    \tfrac{1}{ 
      { \color{green} p! } 
      { \color{blue} p! }
    }
    \partial^{ \color{magenta} \nu }
    \partial_{ \color{magenta} \nu } 
    \alpha_{ \color{green} \mu_1 \cdots \mu_p }
    \delta^{
      { \color{green} \mu_1 \cdots \mu_p }
    }
    _{
      { \color{blue} \kappa_1 \cdots \kappa_p }
    }
    \,
    d x^{\color{blue} \kappa_1} \wedge \cdots d x^{\color{blue}\kappa_p}
    \\
    & =
    { \color{magenta} - }
    \tfrac{1}{ 
      { \color{green} p! } 
      { \color{blue} p! }
    }
    \partial^{ \color{magenta} \nu }
    \partial_{ \color{magenta} \nu } 
    \alpha
  \end{aligned}
$$

=--

\linebreak

\linebreak




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

$$
  \mathbf{A}_\mu
  \;=\;
  e^{- x^4} A_\mu
$$

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