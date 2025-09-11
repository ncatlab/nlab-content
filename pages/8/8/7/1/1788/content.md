> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak



***


### Wilson loops in abelian Chern-Simons theory
 {#WilsonLoopsInAbelianChernSimonsTheory}

The traditional reasoning for the definition of [[Wilson loop]]-[[quantum observables]] in [[abelian Chern-Simons theory]] on the [[3-sphere]] [[3-sphere|$S^3$]] goes as follows (such as reviewed in [GMR 1994 §1](#GMR94)).

#### Ingredients

Any $\mathrm{U}(1)$-[[principal connection|connection]] on [[3-sphere|$S^3$]] (or $\mathbb{R}^3$) has [[underlying]] [[trivial bundle]] (since the [[homotopy classes]] of [[maps]] from $S^3$ to the [[classifying space]] $B \mathrm{U}(1)$, being an [[Eilenberg-MacLane space]] $K(\mathbb{Z},2)$, are all trivial: $\pi_0 Map\big(S^3, B \mathrm{U}(1)\big) \simeq \pi_3 B \mathrm{U}(1) \simeq 1$) and hence is represented by a globally defined [[differential 1-form]] 
\[
  \label{1Forms}
  A \in \Omega^1_{dR}\big(S^3\big)
  \mathrlap{\,.}
\]

Given an [[oriented link]] 
\[
  \label{ALink}
  \gamma \colon (S^1)^{n} \longrightarrow \mathbb{R}^3 \to S^3
\] 
(with $n$ [[connected components]] $L_a \colon S^1 \longrightarrow \mathbb{R}^n$, for $a \in [n]$), its  *[[Wilson loop]]*/*[[holonomy]]* with respect to such a connection (eq:1Forms) is:

\[
  \label{Holonomy}
  \exp\left(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    \gamma^\ast A
  \right)
  \;\in\;
  \mathrm{U}(1)
  \,.
\]


The *[[expectation value]] of the $L$-[[Wilson loop]] [[quantum observable]]*, 
$$
  \left\langle
  \exp\left(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    \gamma^\ast A
  \right)
  \right\rangle
  \;\in\;
  \mathbb{C}
  \mathrlap{\,,}
$$
is then meant to be the normalized [[path integral]] "$\int D A$" over the space of [[gauge orbits]] of $A$ (eq:1Forms) of the expression (eq:Holonomy) times the exponentiated [[action functional]] of [[abelian Chern-Simons theory]], suggestively written as
\[
  \label{PathIntegralForAbelianChernSimonsWilsonLoops}
  \left\langle
  \exp\left(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    \gamma^\ast A
  \right)
  \right\rangle
  \;\;
  =
  \;\;
  \multiscripts{^{\text{"}}}{
  \frac{
    \displaystyle{\int D A}
    \;
    \exp\left(
      \tfrac{\mathrm{i}}{k}
      \textstyle{\underset{S^3}{\int}}
      A \wedge \mathrm{d}A
      \;+\;
      \mathrm{i}
      \textstyle{\underset{{(S^1)^n}}{\int}} 
      \gamma^\ast A
    \right)     
  }{
    \displaystyle{\int D A}
    \;
    \exp\left(
      \tfrac{\mathrm{i}}{k}
      \textstyle{\underset{S^3}{\int}}
      A \wedge \mathrm{d}A
    \right)     
  }
  }{^{\text{"}}}
  \mathrlap{\,.}
\]

As usual for [[path integrals]], the expression on the right of (eq:PathIntegralForAbelianChernSimonsWilsonLoops) remains undefined, since a suitable [[measure]] "$D A$" is not known and may not exist. As also usual for path integrals, one proceeds instead by postulating that the expression on the left of (eq:PathIntegralForAbelianChernSimonsWilsonLoops) satisfies enough structural properties that are *suggested* by the symbols on the right as to be uniquely fixed by these conditions --- and then take that to be the definition.

We proceed [below](#AbelianCSWilsonLoopsViaGaussianIntegrals) to discuss the usual such postulates, which proceed by applying expected properties of [[Gaussian integrals]]. 

A slightly different set of postulates, but more explicit than usual, is considered by [Guadagnini & Thuillier 2008 §4.3](#GuadagniniThuillier08).


#### The Gaussian path integral
 {#AbelianCSWilsonLoopsViaGaussianIntegrals}

Since the [[abelian Chern-Simons theory|abelian Chern-Simons]] [[Lagrangian density]] $A \wedge \mathrm{d}A$ is a [[quadratic form]] in $A$, one envisions that this expression follows the transformation rules of [[Gaussian integrals]] over elements $\phi \in \mathbb{R}^n$ of finite-dimensional [[Cartesian spaces]], for which 
$$
  Z(J)
  \;\coloneqq\;
  \int \mathrm{d}^n \phi\;
  \exp\Big(
    - \tfrac{1}{2}
    \phi \cdot M \cdot \phi 
    +
    J \cdot \phi
  \Big)
$$
evaluates to 
\[
  \label{EvaluationOfOrdinaryGaussianIntegral}
  Z(J)
  \;=\;
  Z(0)
  \,
  \exp\Big(
    \tfrac{1}{2}
    \, 
    J \cdot M^{-1} \cdot J
  \Big)
  \,.
\]

Systematically following through this analogy (using [[Fourier transform]] to turn the [[derivative]] in $A \mathrm{d} A$ into a [[multiplication]] operation) with some care (such as with attention to [[gauge fixing]]) suggests the expression
$$
  \left\langle
  \exp\left(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    \gamma^\ast A
  \right)
  \right\rangle
  \;=\;
  \multiscripts{^{\text{"}}}{
  \exp\bigg(
    -\tfrac{1}{2}
    \textstyle{\underset{\gamma}{\int}}
    \textstyle{\underset{\gamma}{\int}}
    \big\langle
      A_\mu(x)
      ,
      A_\nu(y)
    \big\rangle
    \, 
    \mathrm{d} x^\mu\, 
    \mathrm{d} y^\nu
  \bigg)
  }{^{\text{"}}}
  \,,
$$
where the *[[Chern-Simons propagator]]* -- namely the analog of $M^{-1}$ in (eq:EvaluationOfOrdinaryGaussianIntegral) -- is suggested to be
\[
  \label{AbelianCSPropagatorForComputationOfWilsonLoops}
  \big\langle
    A_\mu(x)
    ,
    A_\nu(y)
  \big\rangle
  \;=\;
  \multiscripts{^{\text{"}}}{
  \tfrac{1}{k}
  \epsilon_{\mu \nu \rho}
  \frac{
    x^\rho - y^\rho
  }{
    \left\vert x - y \right\vert^3
  }
  }{^{\text{"}}}
  \,.
\]

In summary, this suggests
\[
  \label{AbelianCSWilsonLoopObservableByNaivePathIntegral}
  \left\langle
  \exp\left(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    L^\ast A
  \right)
  \right\rangle
  \;=\;
  \multiscripts{^{\text{"}}}{
  \exp\bigg(
    -\tfrac{\mathrm{i}}{2k}
    \textstyle{\underset{\gamma}{\int}}
    \textstyle{\underset{\gamma}{\int}}
    \, 
    \mathrm{d} x^\mu\, 
    \mathrm{d} y^\nu
    \epsilon_{\mu \nu \rho}  
    \frac{
      x^\rho - y^\rho
    }{
      \left\vert x - y \right\vert^3
    } 
  \bigg)
  }{^{\text{"}}}
  \,,
\]

This is the proposed expression due to [Polyakov 1988 (3)](#Polyakov88), popularized by [Witten 1989 (2.29)](#Witten89).
It is *almost* the time-honored [[integral]] expression for the [[Gauss linking number]] of the link $\gamma$, except for those contributions where $x$ and $y$ run over the same [[connected component]].

Namely, of course, (eq:AbelianCSWilsonLoopObservableByNaivePathIntegral) is *still* not well-defined, since the propagator (eq:AbelianCSPropagatorForComputationOfWilsonLoops) is ill-defined whenever $x = y$.

In a final step of this traditional argument one applies a [[renormalization]] argument to deal with the "divergencies" of the exponent in (eq:AbelianCSWilsonLoopObservableByNaivePathIntegral) when $x = y$.

#### The renormalization choice

[Polyakov 1988 (5)](#Polyakov88) considered one regularization of (eq:AbelianCSPropagatorForComputationOfWilsonLoops), but [Witten 1989 p. 363](#Witten89) asserted that it is "clear" that another one should be used, as follows, and this has become the commonly accepted choice since:

Choose a [[framed link|framing]] of the link $\gamma$ (eq:ALink), hence a [[vector field]] $n$ in $\mathbb{R}^3$ defined on $\gamma$ which is normal to $\dot \gamma$ and finally define (eq:AbelianCSWilsonLoopObservableByNaivePathIntegral) to be

\[
  \label{AbelianCSWilsonLoopObservableRenormalized}
  \left\langle
  \exp\left(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    L^\ast A
  \right)
  \right\rangle
  \;\coloneqq\;
  \underset{
    \left\vert n \right\vert n \to 0
  }{\lim}
  \exp\bigg(
    -\tfrac{\mathrm{i}}{2k}
    \textstyle{\underset{(S^1)^n}{\int}}
    \textstyle{\underset{(S^1)^n}{\int}}
    \, 
    \mathrm{d} \sigma\, 
    \mathrm{d} \sigma'
    \,
    \frac
      {\partial \gamma^\mu(\sigma)}
      {\partial \sigma}
    \frac
      {\partial (\gamma^\nu + n^\nu)(\sigma')}
      {\partial \sigma'}    
    \epsilon_{\mu \nu \rho}  
    \frac{
      \gamma^\rho(\sigma) 
        - 
      \big(\gamma^\rho(\sigma') + n^\rho(\sigma')\big)
    }{
      \left\vert 
        \gamma(\sigma) 
        - 
        \big(
          \gamma(\sigma') + n(\sigma')
        \big) 
      \right\vert^3
    } 
  \bigg)
  \,,
\]
where the [[limit of a sequence|limit]] $\left\vert n \right\vert n \to 0$ is over normal vector fields that keep the [[direction of a vector|direction]] but shrink in [[length]] (cf. [GMR 1994 (1.5)](#GMR94)).

This expression is finally well-defined. The shift by the framing does not change that part of the integral where $\sigma$ and $\sigma'$ run over distinct [[connected components]] of the link, hence that part now does give the [[linking number]] of the [[oriented link]]. At the same time the shift makes the contributions $\sigma$ and $\sigma'$ do run over the same connected component become the [[linking number]] of that component with its shift by the framing, which is its [[framing number]].

The end result is hence in the exponent the sum of the [[framing number]] with the [[linking number]] of the link, which is its *[[writhe]]*.




(...)
