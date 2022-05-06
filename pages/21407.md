

#Contents#
* table of contents
{:toc}


## Idea

The [[Maxwell equations]] were originally formulated on 4-dimensional [[Minkowski spacetime]], but in their formulation where the [[Faraday tensor]] is regarded as a [[differential 2-form]] $F$ with [[Hodge dual]] $\star F$ and [[de Rham differentials]]

$$
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

\linebreak

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

We assume now (*not& following [Sutcliffe 10](#Sutcliffe10) in this) that $V^{(n)}_4 = 0$, hence that the $V^{(n)}$ are [[pullback of differential forms|pulled back]] from 4d spacetime, and we take these 4d [[vector potentials]] to be in 4d [[Lorenz gauge]]

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




## Related concepts

* [[D=5 Einstein-Maxwell theory]]

* [[D=5 super Yang-Mills theory]]

## References

General:

* [[Paul Wesson]], Chapter 5 of: _Space-Time-Matter: Modern Kaluza-Klein Theory_, World Scientific 1989 ([doi:10.1142/3889](https://doi.org/10.1142/3889))

* [[Paul Wesson]], James M. Overduin, Chapter 6 of: _Principles of Space-Time-Matter: Cosmology, Particles and Waves in Five Dimensions_, World Scientific 2018 ([doi:10.1142/10871](https://doi.org/10.1142/10871))

Relation to [[vector mesons]] and the [[Skyrmion model]]:

* {#Sutcliffe10} [[Paul Sutcliffe]], Section 3 of: _Skyrmions, instantons and holography_, JHEP 1008:019, 2010 ([arXiv:1003.0023](https://arxiv.org/abs/1003.0023))



[[!redirects 5d Maxwell theory]]

[[!redirects D=5 electromagnetism]]
[[!redirects 5d electromagnetism]]

