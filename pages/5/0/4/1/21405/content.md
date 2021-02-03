
### Hodge star operator on Minkowski spacetime
 {#HodgeStarOperatorOnMinkowskiSpacetime}

We spell out component expressions for the [[Hodge star operator]] on $D = d+1$-dimensional [[Minkowski spacetime]].


#### Conventions

We use [[Einstein summation convention]] throughout. With this convention, a generic [[differential p-form]] reads

$$
  \alpha
  \;=\;
  \tfrac{1}{p!}
  \alpha_{ \color{green} \mu_1 \cdots \mu_p }
  d x^{ \color{green} \mu_1}
  \wedge 
  \cdots
  \wedge
  d x^{\color{green} \mu_p}
  \,.
$$

Here $p! \coloneqq 1 \cdot 2 \cdot 3 \cdots p \,\in \mathbb{N} \subset \mathbb{R}$ denotes the [[factorial]] of $p \in \mathbb{N}$.

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



#### Definition

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
  \,,
  \end{aligned}
\]

where in the second line we used (eq:ContractionIntoVolumeForm).

=--

#### Properties

+-- {: .num_prop #HodgePairing} 
###### Proposition
**(Hodge pairing)**

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
    \tfrac{ \color{magenta} -1 }{  
      { p! }
    }
  \alpha_{ \mu_1 \cdots \mu_p }
  \alpha^{ \mu_1 \cdots \mu_p }
  \,
  dvol
  \,.
\]

=--

+-- {: .proof}
###### Proof

We compute as follows:

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
    \tfrac{ \color{magenta} -1 }{  
      { \color{green}  p! }
    }
    \alpha_{ \color{green} \mu_1 \cdots \mu_p }
    \alpha^{ \color{green} \mu_1 \cdots \mu_p }
    \,
    dvol
  \end{aligned}
$$

Here the sign in the last lines arises from the [[Minkowski spacetime|Minkowski]] [[signature of a quadratic form|signature]] via (eq:ContractionofLeviCivitaSymbols).


=--

+-- {: .num_prop #HodgeStarFollowedByHodgeStar}  
###### Proposition
**(double Hodge dual)**

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
  \,.
\]

=--

+-- {: .proof}
###### Proof

We compute as follows:

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

Here the sign in the last lines arises from the [[Minkowski spacetime|Minkowski]] [[signature of a quadratic form|signature]] via (eq:ContractionofLeviCivitaSymbols).


=--

+-- {: .num_prop #WaveOperatorOnMinkowskiSpacetime} 
###### Proposition
**([[Laplace operator]]/[[wave operator]])**

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
$$

(i.e. [[Lorenz gauge]]).

Then the [[Laplace-Beltrami operator]]

$$
  \star d \star d \alpha
  \;=\;
  { \color{magenta} - }
  \partial^\nu \partial_\nu \alpha
$$

is the [[wave operator]] acting on the components of $\alpha$.

=--

+-- {: .proof}
###### Proof

We compute as follows:

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
    \partial^{ \color{magenta} \nu }
    \partial_{ \color{magenta} \nu } 
    \alpha
  \end{aligned}
$$

Here the sign in the last lines arises from the [[Minkowski spacetime|Minkowski]] [[signature of a quadratic form|signature]] via (eq:ContractionofLeviCivitaSymbols).

=--
