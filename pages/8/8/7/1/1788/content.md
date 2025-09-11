> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak



***


The traditional argument for the computation of [[Wilson loop]]-[[quantum observables]] in [[abelian Chern-Simons theory]] on [[3-sphere|$S^3$]].

Any $\mathrm{U}(1)$-[[principal connection|connection]] on [[3-sphere|$S^3$]] (or $\mathbb{R}^3$) has [[underlying]] [[trivial bundle]] (since the [[homotopy classes]] of [[maps]] from $S^3$ to the [[classifying space]] $B \mathrm{U}(1)$, being an [[Eilenberg-MacLane space]] $K(\mathbb{Z},2)$, are all trivial: $\pi_0 Map\big(S^3, B \mathrm{U}(1)\big) \simeq \pi_3 B \mathrm{U}(1) \simeq 1$) and hence is represented by a globally defined [[differential 1-form]] 
\[
  \label{1Forms}
  A \in \Omega^1_{dR}\big(S^3\big)
  \mathrlap{\,.}
\]

Given an [[oriented link]] 
\[
  \label{ALink}
  L \colon (S^1)^{n} \longrightarrow \mathbb{R}^3 \to S^3
\] 
(with $n$ [[connected components]] $L_a \colon S^1 \longrightarrow \mathbb{R}^n$, for $a \in [n]$), its  *[[Wilson loop]]*/*[[holonomy]]* with respect to such a connection (eq:1Forms) is:

\[
  \label{Holonomy}
  \exp\left(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    L^\ast A
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
    L^\ast A
  \right)
  \right\rangle
  \;\in\;
  \mathbb{C}
  \mathrlap{\,,}
$$
is then meant to be the normalized [[path integral]] "$\int D A$" over the space of [[gauge orbits]] of $A$ (eq:1Forms) of the expression (eq:Holonomy) times the exponentiated [[action functional]] of [[abelian Chern-Simons theory]], suggestively written as
$$
  \left\langle
  \exp\left(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    L^\ast A
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
      L^\ast A
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
$$


Since the [[Lagrangian density]] $A \wedge \mathrm{d}A$ is a [[quadratic form]] in $A$, one envisions that this expression follows the transformation rules of [[Gaussian integrals]] over elements $\phi \in \mathbb{R}^n$ of finite-dimensional [[Cartesian spaces]], for which 
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
$$
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
$$


