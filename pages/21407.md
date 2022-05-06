

#Contents#
* table of contents
{:toc}


## Idea

The [[Maxwell equations]] were originally formulated on 4-dimensional [[Minkowski spacetime]], but in their formulation where the [[Faraday tensor]] is regarded as a [[differential 2-form]] $F$ with [[Hodge dual]] $\star F$ and [[de Rham differentials]]

$$R e
  \array{
    d F & = 0
    \\
    \star d F & = J
  }
$$

they immediately generalize to make sense on [[Minkowski spacetime]] of any dimension $D$, and in fact to any [[pseudo-Riemannian manifold]]. The case of $D =5$-Maxwell theory plays a role mostly as a subsector of [[D=5 Einstein-Maxwell theory]] and/or of [[D=5 super Yang-Mills theory]], as well as a pre-image under [[Kaluza-Klein compactification]] of [[massive Yang-Mills theory]] in 4-dimensions.

## Properties



[[!include relation between 5d Maxwell theory and self-dual 3-forms in 6d -- section]]



\linebreak




### Relation between 5d Maxwell theory and massive vector mesons in 4d
 {#RelationBetween5dMaxwellTheoryAndMassiveVectorMesons}

In an abelian version of the way the [[Skyrmion]]-model appears in [[holographic QCD]], the [[Kaluza-Klein reduction]] of [[D=5 Maxwell theory]] to 4d yields a theory of a tower of massive vector particles which may be interpreted as [[vector mesons]] ([Sutcliffe 10, Sec. 3](#Sutcliffe10)):

#### Flat space model

Following [Sutcliffe 10, Sec. 3](#Sutcliffe10), we first consider a toy example where the 5d metric is that of flat [[Minkowski spacetime]].

Consider 4d- and 5d-dimensional [[Minkowski spacetime]] equipped with global [[orthonormal basis|orthonormal]] [[coordinate charts]]  $\{x^\mu\}$, $\{x^\kappa\}$, respectively, adapated to an [[isometry|isometric]] [[embedding of smooth manifolds|embedding]]

$$
  \array{
   &
    \mathbb{R}^{3,1}
    &\overset{\;\;\;\iota_5\;\;\;}{\hookrightarrow}&
    \mathbb{R}^{4,1}
    \\
    \mu = &   0, 1, 2, 3\;
    \\
    \kappa = & 0, 1, 2, 3, && 4
  }
$$

With this notation, the [[pullback of differential forms]] along this embedding is notationally implicit.

Assuming that the 5d [[vector potential]] $\widehat A \in \Omega^1(\mathbb{R}^{4,1})$ is [[square integrable function|square-integrable]] along the $x^4$-drection, we may expand it in a [[linear basis]] $\{h_n\}_{n \in \mathbb{N}}$ of [[Hermite functions]] as a sequence of  [[vector potentials]] $V^{(n)} \in \Omega^1(\mathbb{R}^{4,1})$ that do not depend on $x^4$ anymore.

\[
  \label{HermiteExpansionOf5dVectorPotential}
  \widehat{A}
  \big(
    \{x^\mu\}, x^4
  \big)
  \;=\;
  \underset{n}{\sum}
    h_n(x^4)
    \,
    V^{(n)}(\{x^\mu\})
\]

We assume now (*not* following [Sutcliffe 10](#Sutcliffe10) in this) that $V^{(n)}_4 = 0$, hence that the $V^{(n)}$ are [[pullback of differential forms|pulled back]] from 4d spacetime, and we take these 4d [[vector potentials]] to be in 4d [[Lorenz gauge]]

\[
  \label{4dLorenzGauge}
  d \star_4 V^{(n)}
  \;=\;
  0
  \,.
\]

By the differential recursion relation of [[Hermite functions]] (see [there](Hermite+polynomial#eq:DifferentialRecursionRelationForHermiteFunctions))

\[
  \label{DifferentialRecursionRelationOfHermiteFunctions}
  \frac{d}{ d (x^4)^n}
  h_n(x^4)
  \;=\;
  \sqrt{
    \tfrac
      {n}
      {2}
  }
  h_{n-1}(x^4)
  -
  \sqrt{
    \tfrac
      {n-1}
      {2}
  }
  h_{n+1}(x^4)
\]


it follows that the corresponding [[field strength]] is expanded as

\[
  \label{HermiteExpansionOfFieldStrength}
  d \widehat{A}
  \;=\;
  \underset{n}{\sum}
  h_n
  \Big(
    d V^{(n)}
    +
    \big(
      \sqrt{\tfrac{n+1}{2}}
      V^{(n+1)}
      -
      \sqrt{\tfrac{n}{2}}
      V^{(n-1)}
    \big)
    \wedge 
    d x^4
  \Big)
  \,.
\]

The [[Hodge dual]] of that is:

$$
  \star_5 d \widehat{A}
  \;=\;
  \underset{n}{\sum}
  h_n
  \Big(
    \star_4 d V^{(n)} \wedge d x^4
    +
    \sqrt{\tfrac{n}{2}}
    \star_4 V^{(n-1)}    
    -
    \sqrt{\tfrac{n+1}{2}}
    \star_{4} V^{(n+1)}
  \Big)
  \,.
$$

(Notice the sign reversal of the last two terms. A quick way to see this is to notice the [[Hodge pairing]]-relation (see [there](Hodge+star+operator#HodgePairing)) and the fact that commuting the [[differential 3-form|3-form]] $\star_4 V^{(n)}$ past the [[differential 1-form|1-form]] $d x^4$ produces a sign.)

Now using once more the differential recursion relation (eq:DifferentialRecursionRelationOfHermiteFunctions) of the [[Hermite functions]], the [[de Rham differential]] of this Hode dual field strength is

\[
  \label{SystemOfCoupledEquationsIn4d}
  \begin{aligned}
    & d \star_5 d \widehat{A}
    \\
    & 
  \begin{aligned}
  = 
  \underset{n}{\sum}
  h_n
  \Big(
    &
    d \star_4 d V^{(n)} \wedge d x^4
    +
    \sqrt{\tfrac{n}{2}}
    \underset{
      = 0
    }{
      \underbrace{
        d \star_4 V^{(n-1)}    
      }
    }
    -
    \sqrt{\tfrac{n+1}{2}}
    \underset{
      = 0
    }{
      \underbrace{
        d \star_{4} V^{(n+1)}
      }
    }
    \\
    & 
    +
    \;\;
    \sqrt{\tfrac{n+1}{2}}
    \big(
      \star_4 d V^{(n+1)} \wedge d x^4
      +
      \sqrt{\tfrac{n+1}{2}}
      \star_4 V^{(n)}    
      -
      \sqrt{\tfrac{n+2}{2}}
      \star_{4} V^{(n+2)}
    \big) 
    \wedge d x^4
    \\
    &
    -
    \;\;
    \sqrt{\tfrac{\;n\;}{2}}
    \big(
      \star_4 d V^{(n-1)} \wedge d x^4
      +
      \sqrt{\tfrac{n-1}{2}}
      \star_4 V^{(n-2)}    
      -
      \sqrt{\tfrac{\;n\;}{2}}
      \star_{4} V^{(n)}
    \big)
    \wedge d x^4
  \Big)
  \end{aligned}
  \\
  & =
  \underset{n}{\sum}
  h_n
  \Big(
    d \star_4 d V^{(n)} \wedge d x^4
    +
    \left(   
      n + \tfrac{1}{2}
    \right)
    \star_{4} V^{(n)}
    -
    \sqrt{\tfrac{n+2}{2}\tfrac{n+1}{2}}
    \star_{4} V^{(n+2)}
    -
    \sqrt{\tfrac{n}{2}\tfrac{n-1}{2}}
    \star_4 V^{(n-2)}    
  \Big)
  \wedge d x^4
  \end{aligned}
\]

Here the terms over the braces vanish because we have chosen [[Lorenz gauge]] in (eq:4dLorenzGauge).

Hence under the expansion (eq:HermiteExpansionOf5dVectorPotential) the 5d [[Maxwell equations]] $d \star_5 d \widehat A = 0$ become equivalently the following system of coupled equations of [[massive Yang-Mills theory]] in 4d (using, with [this Prop.](Hodge+star+operator#HodgeStarFollowedByHodgeStar) that the [[Hodge star operator]] on 3-forms in 4d squares to unity):

$$
  \star_4
  d \star_4 d V^{(n)}
  \;=\;
  -
    \left(   
      n + \tfrac{1}{2}
    \right)
    V^{(n)}
  +
    \sqrt{\tfrac{n+2}{2}\tfrac{n+1}{2}}
    V^{(n+2)}
  +
    \sqrt{\tfrac{n}{2}\tfrac{n-1}{2}}
    V^{(n-2)}    
  \Big)
$$

Truncating this to the first term yields the [[Klein-Gordon equation]] for a [[field (physics)|field]] of [[mass]] $1/\sqrt{2}$ (by [this Prop.](Hodge+star+operator#WaveOperatorOnMinkowskiSpacetime)):

$$
  \partial^\mu \partial_\mu V^{(1)}  
  \;=\;
  \tfrac{1}{2}
  V^{(1)}
  \,.
$$

More generally, truncating at some higher number $N$ of modes, one may find a [[linear transformation]] among the fields $V^{(n)}$ for $1 \leq n \leq N$ which diagonalizes (eq:SystemOfCoupledEquationsIn4d) to obtain a collection of $N$ [[Klein-Gordon equations]] for $N$ massive fields.

\linebreak

#### Sakai-Sugimoto model
 {#SakaiSugimotoModel}

We discuss 5d Maxwell theory on the 5d spacetime that appears in the [[Sakai-Sugimoto model]] (from [[D4/D8-brane intersections]]), following [Bolognesi-Sutcliffe 13](#BolognesiSutcliffe13), [Sutcliffe 15](#Sutcliffe15).

\linebreak


Consider 4d- and 5d-dimensional [[smooth manifolds]] [[diffeomorphism|diffeomorphic]] to [[Cartesian space]] and equipped with global [[orthonormal basis|orthonormal]] [[coordinate charts]]  $\{\{x^\mu\}, z\}$, , respectively, adapated to an [[isometry|isometric]] [[embedding of smooth manifolds|embedding]]

\[
  \label{SakaiSugimotoSpacetime}
  \array{
   &
    \mathbb{R}^{3,1}
    &\overset{\;\;\;\iota_5\;\;\;}{\hookrightarrow}&
    \mathbb{R}^{4,1}
    \\
    \mu = &   0, 1, 2, 3\;
    \\
    \kappa = & 0, 1, 2, 3, && z
  }
\]

+-- {: .num_prop #SakaiSugimotoMetric} 
###### Definition
**(Sakai-Sugimoto metric)**

On the 5d manifold (eq:SakaiSugimotoSpacetime) the _Sakai-Sugimito metric_ is the [[metric tensor]]

\[
  \label{SakaiSugimotoMetric}
  g
  \;\coloneqq\;
  H^{+1} \, \eta_{\mu \nu} d x^\mu \otimes d x^\nu 
    + 
  H^{-1} d z \otimes d z
\]

where 

* $(\eta_{\mu \nu}) = diag(-1,+1,+1,+1)$ is the metric of 4d [[Minkowski spacetime]],

* $H$ is the [[smooth function]] given by

  $$
    H(\{x^\mu\}, z)
    \;\coloneqq\;
    H(z)
    \;\coloneqq\;
    \left( 
      1 + \frac{z^2}{L^2}
    \right)^{2/3}
  $$

  for some [[real number]] $L$. 

=--

This metric is highlighted in this form in ([Bolognesi-Sutcliffe 13, (2.1), (2.2)](#BolognesiSutcliffe13) [Sutcliffe 15, (39), (40)](#Sutcliffe15)).

+-- {: .num_prop #SakaiSugimotoEquation} 
###### Proposition
**(Sakai-Suimoto equation)**

Let $A \in \Omega^1(\mathbb{R}^{4,1})$ be a [[differential 1-form]] on the spacetime (eq:SakaiSugimotoSpacetime) with vanishing $z$-component and in 4d [[Lorenz gauge]]:

\[
  \label{VanishingzComponentOfVectorPotentialOnSSSpacetime}
  A_z = 0
\]

\[
 \label{LorenzGaugeForVectorPotentialOnSSSpacetime}
  \partial_\mu \eta^{\mu \nu} A_\nu = 0
 \,.
\]

Then the 5d vacuum [[Maxwell equations]] for the [[vector potential]] $A$ with respect to the [[metric tensor]] (eq:SakaiSugimotoMetric) are equivalent to 

\[
 \label{SakaiSugomotoEquation}
  \begin{aligned}
    &
    \star d \star d A
    \;=\;
    0
    \\
    \Leftrightarrow
    \;\;\;
    &
    \eta^{\mu \nu}\partial_\mu \partial_\nu A
    \;+\;
    H^{1/2}
    \partial_z
    \left(
      H^{3/2} \partial_z A
    \right)
    \;=\;
    0
  \end{aligned}
  \,.
\]

=--

This equation is highlighted in [Bolognesi-Sutcliffe 13, (4.14)](#BolognesiSutcliffe13), [Sutcliffe 15, (48)](#Sutcliffe15).

+-- {: .proof}
###### Proof

Here is a somewhat lengthy computation:

First notice the general component formula for the operator $\star d \star d$ applied to 1-forms, akin to, but different from, the component formula  for the [[Laplace-Beltrami operator]] applied to 0-forms/functions (see [there](Laplace+operator#LaplaceOperatorInComponents))

$$
  \begin{aligned}
    \star d \star d A
    & =
    \star d \star (\partial_{j_1} f) A_{j_2} d x^{j_1} \wedge d x^{j_2}
    \\
    & = 
    \star d
    \left( 
      \tfrac{1}{ 2 \color{green}  (D-2)! }
      \sqrt{
        \left\vert
           det\big( (g_{i j}) \big)
        \right\vert
      }
      \,
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
      \,
      \epsilon_{
        i_1 i_2
        {\color{green} k_3 \cdots k_{D} }
      }
      d x^{
        \color{green} k_3
      } 
      \wedge \cdots \wedge 
      d x^{
        \color{green} k_{D}
      }
    \right)
    \\
    & =
    \star
    \partial_{ \color{magenta} k_2}
    \left( 
      \tfrac{1}{ 2 \color{green} (D-2)! }
      \sqrt{
        \left\vert
           det\big( (g_{i j}) \big)
        \right\vert
      }
      \,
      g^{ i_1 j_1 } 
      g^{ i_2 j_2 } 
      (\partial_{j_1} A_{j_2} )
      \,
      \epsilon_{
        i_1 i_2
        {\color{green} k_3 \cdots k_{D} }
      }
      d x^{ \color{magenta} k_2 }
      \wedge 
      d x^{
        \color{green} k_3
      } \wedge \cdots \wedge 
      d x^{
        \color{green} k_{D}
      }
    \right)
    \\
    & =
    \sqrt{
      \left\vert
        det\big( (g_{i j}) \big)
      \right\vert
    }
    \underset{
      = 
      \det\big( (g_{i j})^{-1}  \big)
      \tfrac{1}{2}
      \delta^{ \color{magenta} k_1 k_2 }_{i_1 i_2}
    }{
    \underbrace{
    \tfrac{
      (-1)^{D-1}
    }{ 
       { \color{orange} (D-1)! }
       2 { \color{green} (D-2)! }
    }
    \epsilon_{ 
      l_1
      { \color{orange} l_2 \cdots l_{D} }
    }
    g^{ 
      { \color{orange} l_1 }
      { \color{magenta} k_1  } 
    }
    g^{ 
      { \color{orange} l_2 }
      { \color{magenta} k_2  } 
    }
    g^{ 
      { \color{orange} l_3 }
      { \color{green} k_3  } 
    }
    \cdots
    g^{ 
      { \color{orange} l_D} 
      { \color{green} k_D } 
    }
    \epsilon_{
      i_1 i_2
      {\color{green} k_3 \cdots k_{D} }
    }
    }
    }
    \,
    \partial_{ \color{magenta} k_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \, 
    g_{ {\color{magenta} k_1} r }
    d x^{ \color{magenta} r  }
    \\
    & =
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} k_1 k_2 }_{i_1 i_2}
    \partial_{ \color{magenta} k_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} k_1 } r }
    d x^{  r }
  \end{aligned}
$$

Now specialize this to the the case at hand, where 

1. $A = A_\mu d x^{\mu} A_z d^z $ 

1. $A_z = 0$

1. $\partial_\mu \eta^{\mu \nu} A_\nu = 0$ 

1. $g_{\mu \nu} = H \eta_{\mu \nu}$

1. $\partial_\mu H = 0$.

We get:

$$
  \begin{aligned}
    & 
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} k_1 k_2 }_{i_1 i_2}
    \partial_{ \color{magenta} k_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} k_1 } r }
    d x^{  r }
    \\
    & =
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} \mu_1 \mu_2 }_{i_1 i_2}
    \partial_{ \color{magenta} \mu_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} \mu_1 } r }
    d x^{  r }
    \\
    & \phantom{=}\;
    +
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} \mu_1 z }_{i_1 i_2}
    \partial_{ \color{magenta} z }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} \mu_1 } r }
    d x^{  r }
    \\
    & \phantom{=}\;
    +
    \frac{
      (-1)^{D-1}
    }{  
       \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
    }
    \tfrac{1}{2}
    \delta^{ \color{magenta} z \mu_2 }_{i_1 i_2}
    \partial_{ \color{magenta} \mu_2 }
    \left( 
      \sqrt{
        \left\vert
          det\big( (g_{i j}) \big)
        \right\vert
      }
      g^{ i_1  j_1 } 
      g^{ i_2  j_2 } 
      (\partial_{j_1} A_{j_2})
    \right)    
    \,
    g_{ {\color{magenta} z } r }
    d x^{  r }
    \\
    & =
    \tfrac{
      (-1)^{D-1}
    }{2}
    H^{-2}
    \big(
      \underset{
        = 0
      }{
      \underbrace{
      \partial_{\mu_2}
      \partial_{\mu_1}
      A^{\mu_2}
      }
      }
    \big)
    H^1
    d x^{\mu_1}
    -
    (-1)^{D-1}
    \tfrac{1}{2}
    H^{-2}
    \big(
      \partial_{\mu_2}
      \partial^{\mu_2}
    A^{\mu_1}
    \big)
    H^1
    d x^{\mu_1}
    \\
    & \phantom{=}\;
    (-1)^{D-1}
    \tfrac{1}{2}
    H^{-3/2}
    \partial_z
    \big( 
      H^{3/2}
      \partial_{\mu_1}
      \underset{ = 0}{
      \underbrace{
      A_{z}
      }
      }
    \big)
    H^1
    d x^{\mu_1}
    -
    (-1)^{D-1}
    \tfrac{1}{2}
    H^{-3/2}
    \partial_z
    \left( 
      H^{3/2}
      \partial_{z}
      A_{\mu_1}
    \right)
    H^1
    d x^{\mu_1}
    \\
    & \phantom{=}\;
    +
    (-1)^{D-1}
    \tfrac{1}{2}
    H^{-3/2}
    \underset{
      = 0
    }{
    \underbrace{
    \partial_{\mu_2}
    \left( 
      H^{3/2}
      \partial_z
      A^{\mu_2}
    \right)
    }
    }
    H^{-1} d z
    -
    (-1)^{D-1}
    \tfrac{1}{2}
    H^{-3/2}
    \partial_{\mu_2}
    \big( 
      H^{3/2}
      \partial_{\mu_2}
      \underset{
        = 0
      }{
      \underbrace{
        A_{z}
      }
      }
    \big)
    H^{-1} d z
    \\
    & =
    -
    (-1)^{D-1}
    \tfrac{1}{2}
    H^{-1}
    \,
    \Big(
      \eta^{\mu \nu}\partial_\mu \partial_\nu A
      +
      H^{1/2}
      \partial_z
      \left(
        H^{3/2} \partial_z A
      \right)
    \Big)
  \end{aligned}
$$

Here the terms over the braces vanish, alternatingly, by 
the assumptions (eq:VanishingzComponentOfVectorPotentialOnSSSpacetime) and (eq:LorenzGaugeForVectorPotentialOnSSSpacetime).

=--

\linebreak

(...)


\linebreak




## Related concepts

* [[D=5 Einstein-Maxwell theory]]

* [[D=5 super Yang-Mills theory]]

## References

General:

* [[Paul Wesson]], Chapter 5 of: _Space-Time-Matter: Modern Kaluza-Klein Theory_, World Scientific 1989 ([doi:10.1142/3889](https://doi.org/10.1142/3889))

* [[Paul Wesson]], James M. Overduin, Chapter 6 of: _Principles of Space-Time-Matter: Cosmology, Particles and Waves in Five Dimensions_, World Scientific 2018 ([doi:10.1142/10871](https://doi.org/10.1142/10871))

Relation to [[vector mesons]] and the [[Skyrmion model]] via the [[Sakai-Sugimoto model]] and variants:

* {#Sutcliffe10} [[Paul Sutcliffe]], Section 3 of: _Skyrmions, instantons and holography_, JHEP 1008:019, 2010 ([arXiv:1003.0023](https://arxiv.org/abs/1003.0023))

* {#BolognesiSutcliffe13} [[Stefano Bolognesi]], [[Paul Sutcliffe]], _The Sakai-Sugimoto soliton_, JHEP 1401:078, 2014 ([arXiv:1309.1396](https://arxiv.org/abs/1309.1396))

* {#Sutcliffe15} [[Paul Sutcliffe]], _Holographic Skyrmions_, Mod. Phys. Lett. B29 (2015) no. 16, 1540051 ([spire:1383608](http://inspirehep.net/record/1383608))


[[!redirects 5d Maxwell theory]]

[[!redirects D=5 electromagnetism]]
[[!redirects 5d electromagnetism]]

