

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
=--
=--


\tableofcontents


## Idea

By *abelian Chern-Simons theory* one means [[Chern-Simons theory]] with [[abelian group|abelian]] [[gauge group]] (typically the [[circle group]] or a [[torus]]-[[product group|product]] of copies of that).

One major application of abelian Chern-Simons theory is as an [[effective field theory]] of the [[fractional quantum Hall effect]], see [below](#AbelianCSTheoryAsEffectiveQFTForFRactionalQuantumHall).


## Definition

### The Lagrangian density and the Level
 {#LagrangianDensityAndLevel}

For the time being we normalize [[connection]] [[differential forms|forms]] according to the common convention in [[theoretical physics]], where the gauge [[curvature]]/[[field strength]]/[[flux density]] $F_A \coloneqq \mathrm{d}A$ is such that
\[
  \label{NormalizationPfFluxDensity}
  \tfrac{1}{2\pi} F_A
  \;\in\;
  \Omega^2_{int}
\]
is an [[integral form]], in that it has [[integer]] [periods](period#InDifferentialGeometry) (cf. *[[Dirac charge quantization]]* and *[[ordinary differential cohomology]]*).


The (local) [[Lagrangian density]] of abelian Chern-Simons theory is a multiple of the [[Chern-Simons form]] of the gauge field
\[
  \label{TheLagrangianDensity}
  L(A)
  \;\coloneqq\;
  \tfrac{K}{4\pi} A \wedge \mathrm{d} A
  \,
\] 
for a numerical parameter $K$, whose admissible values are to be characterized so that for each choice of domain $\Sigma^3$ (a [[closed manifold|closed]] [[smooth manifold|smooth]] [[3-manifold]]) the [[action functional]]
$$
  S(\Sigma^3, A)
  \;\coloneqq\;
  \tfrac{K}{4\pi}
  \textstyle{\int_{\Sigma^3}} 
  A \wedge \mathrm{d}A
$$
has [[gauge invariance|gauge-invariant]] [[exponential]]
\[
  \label{ExponentiatedActionFunctional}
  \exp\Big(
    \mathrm{i} S(A)
  \Big)
  \;=\;
  \exp\Big( 
    \mathrm{i}
    \tfrac{K}{4\pi}
    \textstyle{\int_{\Sigma^3}} 
    A \wedge \mathrm{d}A
  \Big)
  \;\in\;
  \mathrm{U}(1)
  \,.
\]

A transparent way to understand this condition is to consider (in the style of the definition of [[Cheeger-Simons differential characters]], popularized by [[Edward Witten|Witten]]) a [[compact topological space|compact]] [[4-manifold]] $\Sigma^4$ [[manifold with boundary|with boundary]] $\Sigma^3 = \partial \Sigma^4$ and an extension of the $\mathrm{U}(1)$-connection to $\Sigma^4$, where we will denote its [[curvature]]/[[field strength]]/[[flux density]] still by $F$. 

Then [[Stokes' theorem]] gives
$$
  \exp\Big(
    \mathrm{i} S(A)
  \Big)
  \;=\;
  \exp\Big(
    \mathrm{i}
    \tfrac{K}{4\pi}
    \textstyle{\int_{\Sigma^4}}
    F \wedge F
  \Big)
  \;=\;
  \exp\Big(
    K \pi \mathrm{i}
    \textstyle{\int_{\Sigma^4}}
    \frac{F}{2\pi} \wedge \frac{F}{2\pi}
  \Big)
  \,,
$$
which reveals that the expression is well-defined --- in that it takes the same value for any other choice of $\Sigma^4$ --- if for *[[closed manifold|closed]]* $\widehat{\Sigma}^4$ (arising as the gluing of one choice of $\Sigma^4$ with the orientation reversal of any other along their common boundary $\Sigma^3$) we have
$$
  \tfrac{1}{2\pi \mathrm{i}}
  K \pi \mathrm{i}
  \underset{
    c_1^2(\Sigma^4)
  }{
    \underbrace{
      \textstyle{\int_{\widehat{\Sigma}^4}}
      \frac{F}{2\pi} \wedge \frac{F}{2\pi}
    }
  }
  \;\in\;
  \mathbb{Z}
  \,.
$$

If there is no further condition on $\Sigma^3$ and hence on $\widehat{\Sigma}^4$, then by (eq:NormalizationPfFluxDensity), $c_1^2(\Sigma^4) \in \mathbb{Z}$ and the condition is that 
\[
  \label{TheLevel}
  k 
    \;\coloneqq\; 
  \tfrac{K}{2}
    \;\in\;
  \mathbb{Z}
\] 
must be an [[integer]]. 

This $k$ is the *[[Chern-Simons level]]*. On the other hand, $K = 2k$ is the (even, for now) integer that gets promoted to the eponymous [[matrix]] $(K_{i j})$ in "K-matrix Chern-Simons theory" ,where several gauge fields couple to each other (see [below](#HierarchicalKMatrixFormalism)). But beware that conventions differ and that our "$K$" is often denoted "$k$" in the literature.

It is also $K$ that is more fundamental as one restricts attention to [[spin manifolds]] $\Sigma^3$, hence to *[[spin Chern-Simons theory]]* ([Dijkgraaf & Witten 1990 §5](#DijkgraafWitten90)):

from the observation that the [[cobordism ring]] for [[spin  manifolds]] equipped with [[complex line bundles]] is trivial in degree 3, and that 
$$
  \widehat{\Sigma}^4 
  \;
  \text{spin manifold}
  \;\;
  \Rightarrow
  \;\;
  \int_{\widehat{\Sigma}^4}
  \frac{F}{2\pi} \wedge \frac{F}{2\pi}
  \;\in\;
  2\mathbb{Z}
  \,,
$$
it follows that for [[spin Chern-Simons theory]] one may allow also half-integral level $k$ (eq:TheLevel) and hence odd integral $K$:
$$ 
  k 
    \;\in\;
  \tfrac{1}{2}\mathbb{Z} 
  \;\;\;\;\;\;
  \text{equivalently}
  \;\;\;\;\;\;
  K \coloneqq 2k 
  \;\in\;
  \mathbb{Z}
  \,.
$$

Finally, just to note how the resulting expression for the exponentiated action functional (eq:ExponentiatedActionFunctional) changes when one adopts instead of (eq:NormalizationPfFluxDensity) the normalization condition for $F$ that is more common in mathematics, where it is $F$ itself that is [[integral differential form|integral]]:

|  | physics normalization | math normalization |
|--|-----------------------|--------------------|
| integral flux density | $\tfrac{1}{2\pi} F$  | $F$ |
| exponentiated action | $e^{\mathrm{i}S(A)} = \exp\Big( \mathrm{i} \tfrac{K}{4\pi} \textstyle{\int_{\Sigma^3}} A \wedge \mathrm{d}A \Big)$ | $e^{\mathrm{i}S(A)} = \exp\Big( 2\pi\mathrm{i}  \textstyle{\int_{\Sigma^3}} \tfrac{K}{2}\, A \wedge \mathrm{d}A \Big)$ |

Some of the following sections stick to one or the other of these conventions.

### The equation of motion

The [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] associated with the abelian Chern-Simons Lagrangian (eq:TheLagrangianDensity) is immediately found to be
$$
  F = 0
  \,,
$$
saying that the [[on-shell]] gauge fields are precisely the [[flat connections]] with vanishing [[flux density]] $F = \mathrm{d}A$.



## Properties

### Space of quantum states
 {#SpaceOfQuantumStates}

For abelian Chern-Simons theory with $N$ [[gauge fields]] $(a^{(i)})_{i = 1}^N$ and [[Lagrangian density]] of the form (using [[Einstein summation convention]]) $K_{i j} \tfrac{1}{2} a^{(i)} \wedge \mathrm{d} a^{(j)}$ (eq:SecondaryEffectiveLagrangianInKMatrixForm) , for $K$ an $N \times N$ *even* [[integer]] [[symmetric matrix]] (the diagonal entries are [[even numbers]]), the [[dimension of a vector space|dimension]] of the [[Hilbert space|Hilbert]] [[space of quantum states]] $\mathscr{H}_g$ (obtained by [[geometric quantization]], cf. *[[quantization of D=3 Chern-Simons theory]]*) over an [[orientation|orientable]] [[surface]] of [[genus of a surface|genus]] $g$ is the [[absolute value]] of the [[determinant]] of $K$ raised to the $g$th [[exponent|power]]:

$$ 
  dim(\mathscr{H}_g)
  \;=\;
  \left\vert det(K)\right\vert^g
  \,.
$$

(for $g = 1$ this is [Wesolowski, Hosotani & Ho 1994 (3.25)](#WesolowskiHosotaniHo94), for  $N=1$ see [Manoliu 1998a p 40](#Manoliu98a), for general $N$ this goes back to [Wen & Zee 1992 (1.2)](#WenZee92Classification), recalled in [Fradkin 2013 (14.23)](#Fradkin13), [Belov & Moore 2005 p 26](#BelovMoore05)).

For the [[modular group]]-[[group action|action]] on these state spaces see at *[[integer Heisenberg group]]* the section *[Modular automorphisms](integer+Heisenberg+group#ModularAutomorphisms)* (there for $g=1$).


{#DegeneracyOnNonOrientableSurface} For a *non-*orientable surface with $k$ crosscaps, it is 

$$ 
  dim(\mathscr{H}_k)
  \;=\;
  \left\vert det(K)\right\vert^{k-1}
  \,.
$$

(e.g. [arXiv:1509.03920](https://arxiv.org/abs/1509.03920) (73))


\linebreak


### Wilson loop quantum observables
 {#WilsonLoopsInAbelianChernSimonsTheory}


It is physics [[folklore]] that the [[Wilson loop]] [[quantum observables]] of [[abelian Chern-Simons theory]] on the [[3-sphere]] evaluate to the exponentiated [[linking number]] plus [[framing number]] of the given ([[oriented link|oriented]], [[framed link|framed]]) [[link]].

The traditional reasoning via "[[path integral]]" arguments, followed by a point-splitting [[renormalization]] choice via [[framed link|link framing]], is as follows (going back to [Polyakov 1988](#Polyakov88), enshrined since [Witten 1989 §2.1](#Witten89),  reviewed in [GMR 1994 §1](#GMR94)).


#### Wilson loops

The [[gauge field|gauge]] [[field (physics)|field]] of abelian [[circle group|$\mathrm{U}(1)$]] Chern-Simons theory is a [[principal U(1)-bundle]] with [[principal connection]] $\nabla$.

However, on $\Sigma^3 = S^3$ the [[3-sphere]], any such $\mathrm{U}(1)$-[[principal connection|connection]] has [[underlying]] [[trivial bundle]] (since the [[homotopy classes]] of [[maps]] from $S^3$ to the [[classifying space]] $B \mathrm{U}(1)$, being an [[Eilenberg-MacLane space]] $K(\mathbb{Z},2)$, are all trivial: $\pi_0 Map\big(S^3, B \mathrm{U}(1)\big) \simeq \pi_3 B \mathrm{U}(1) \simeq 1$) and hence is represented by a globally defined [[differential 1-form]] 
\[
  \label{1Forms}
  A \in \Omega^1_{dR}\big(S^3\big)
  \mathrlap{\,.}
\]

Given an [[oriented link|oriented]] [[link]] 
\[
  \label{ALink}
  \gamma 
    \colon 
  (S^1)^{n} \longrightarrow \mathbb{R}^3 \to S^3
\] 
with $n$ [[connected components]] 
\[
  \label{ConnectedComponentsOfALink}
  \Big\{
    \gamma_i \colon S^1 \longrightarrow \mathbb{R}^n
  \Big\}_{i \in [n]}
  \,,
\]

its  *[[Wilson loop]]*/*[[holonomy]]* with respect to such a connection (eq:1Forms) is the exponentiated [[integration of differential forms|integral]] of $A$ along the link:

\[
  \label{Holonomy}
  \exp\bigg(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    \gamma^\ast A
  \bigg)
  \;\in\;
  \mathrm{U}(1)
  \,.
\]


The *[[expectation value]] $\langle-\rangle$ of the $\gamma$-[[Wilson loop]] (eq:Holonomy), regarded as a [[quantum observable]]* in abelian Chern-Simons theory, 
$$
  \Bigg\langle
  \exp\bigg(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    \gamma^\ast A
  \bigg)
  \Bigg\rangle
  \;\in\;
  \mathbb{C}
  \mathrlap{\,,}
$$
is traditionally meant to be the normalized "[[path integral]] $\int D A$" over the space of [[gauge orbits]] of $A$ (eq:1Forms) of the expression (eq:Holonomy) weighted by the exponentiated [[action functional]] (eq:ExponentiatedActionFunctional) of [[abelian Chern-Simons theory]], suggestively written as:
\[
  \label{PathIntegralForAbelianChernSimonsWilsonLoops}
  \Bigg\langle
  \exp\bigg(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    \gamma^\ast A
  \bigg)
  \Bigg\rangle
  \;\;
  =
  \;\;
  \multiscripts{^{\text{"}}}{
  \frac{
    \displaystyle{\int D A}
    \;
    \exp\bigg(
      \mathrm{i}
      \tfrac{K}{4\pi}
      \textstyle{\underset{S^3}{\int}}
      A \wedge \mathrm{d}A
      \;+\;
      \mathrm{i}
      \textstyle{\underset{{(S^1)^n}}{\int}} 
      \gamma^\ast A
    \bigg)     
  }{
    \displaystyle{\int D A}
    \;
    \exp\bigg(
      \mathrm{i} 
      \tfrac{K}{4\pi}
      \textstyle{\underset{S^3}{\int}}
      A \wedge \mathrm{d}A
    \bigg)     
  }
  }{^{\text{"}}}
  \mathrlap{\,.}
\]

As usual for [[path integrals]], the expression on the right of (eq:PathIntegralForAbelianChernSimonsWilsonLoops) remains undefined, since a suitable [[measure]] "$D A$" is not known and may not exist. As also usual for path integrals, one proceeds instead by postulating that the expression on the left of (eq:PathIntegralForAbelianChernSimonsWilsonLoops) satisfies enough structural properties that are *suggested* by the symbols on the right as to be uniquely fixed by these conditions --- and then take that to be the definition.

We proceed [below](#AbelianCSWilsonLoopsViaGaussianIntegrals) to discuss the usual such postulates, which proceed by applying expected properties of [[Gaussian integrals]]. 
A slightly different set of postulates, but more explicit than usual, is considered by [Guadagnini & Thuillier 2008 §4.3](#GuadagniniThuillier08).


#### The Gaussian path integral
 {#AbelianCSWilsonLoopsViaGaussianIntegrals}

Since the [[abelian Chern-Simons theory|abelian Chern-Simons]] [[Lagrangian density]] $\tfrac{K}{4\pi} A \wedge \mathrm{d}A$ (eq:TheLagrangianDensity) is a [[quadratic form]] in $A$, one envisions that this expression (eq:PathIntegralForAbelianChernSimonsWilsonLoops) follows the transformation rules of [[Gaussian integrals]] over elements $\phi \in \mathbb{R}^n$ of finite-dimensional [[Cartesian spaces]], for which 
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

Systematically following through this analogy (using [[Fourier transform]] to turn the [[derivative]] in $A \mathrm{d} A$ into a [[multiplication]] operation) with some care (such as with attention to [[gauge fixing]]) suggests the expression:
$$
  \Bigg\langle
  \exp\bigg(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    \gamma^\ast A
  \bigg)
  \Bigg\rangle
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
whereby the *[[Chern-Simons propagator]]* -- namely the analog of $M^{-1}$ in (eq:EvaluationOfOrdinaryGaussianIntegral) -- is suggested to be
\[
  \label{AbelianCSPropagatorForComputationOfWilsonLoops}
  \big\langle
    A_\mu(x)
    ,
    A_\nu(y)
  \big\rangle
  \;=\;
  \multiscripts{^{\text{"}}}{
  \frac{\mathrm{i}}{2K}
  \epsilon_{\mu \nu \rho}
  \frac{
    x^\rho - y^\rho
  }{
    \left\vert x - y \right\vert^3
  }
  }{^{\text{"}}}
  \,.
\]

In summary, this suggests that
\[
  \label{AbelianCSWilsonLoopObservableByNaivePathIntegral}
  \Bigg\langle
  \exp\bigg(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    \gamma^\ast A
  \bigg)
  \Bigg\rangle
  \;=\;
  \multiscripts{^{\text{"}}}{
  \exp\bigg(
    -\tfrac{\mathrm{i}}{4K}
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
  \,.
\]

This is the proposed expression due to [Polyakov 1988 (3)](#Polyakov88), popularized by [Witten 1989 (2.29)](#Witten89).
It is *almost* the time-honored [[integral]] expression for the [[Gauss linking number]] of the link $\gamma$, except for those contributions where $x$ and $y$ run over the same [[connected component]] (eq:ConnectedComponentsOfALink), compare the final expression (eq:AbelianCSWilsonLoopsInTermsOfFramingAndLinkingNumbers) below.

Namely, (eq:AbelianCSWilsonLoopObservableByNaivePathIntegral) is of course *still* not well-defined, since the [[Chern-Simons propagator|propagator]] (eq:AbelianCSPropagatorForComputationOfWilsonLoops) is ill-defined whenever $x = y$.
In a final step of the traditional argument one applies a [[renormalization]] argument to deal with the "divergencies" of the exponent in (eq:AbelianCSWilsonLoopObservableByNaivePathIntegral) when $x = y$.


#### The renormalization choice
 {#AbelianCSWIlsonLoopsTheRenormalizationChoice}

[Polyakov 1988 (5)](#Polyakov88) considered one regularization of (eq:AbelianCSPropagatorForComputationOfWilsonLoops). Another one was by [Leukert & Schäfer 1996 §7](#LeukertSchäfer96) (there on a backdrop of a rigorous construction of the [[path integral]] [[measure]], which however still leaves the Wilson loop observable ill-defined, see also [Hahn 2004a](#Hahn04a) [2004b](#Hahn04b)). 

But [Witten 1989 p. 363](#Witten89) asserted that it is "clear" that the following "point-splitting regularization" should be used instead, and this has become the commonly accepted choice since (cf. [Kaul 1999 (9)](#Kaul99), [Hahn 2004a §9](#Hahn04a), [Hahn 2004b §2.5 & §5](#Hahn04b) [Guadagnini & Thuillier 2008 §3](#GuadagniniThuillier08), [Mezei, Pufu & Wang 2017 (5.1)](#MezeiPufuWang17)):

Choose a [[framed link|framing]] of the link $\gamma$ (eq:ALink), hence a unit [[vector field]] $n$ in $\mathbb{R}^3$ defined on $\gamma$, which is normal to the [[tangent vectors]] $\dot \gamma$ to $\gamma$. 
With that, finally define (eq:AbelianCSWilsonLoopObservableByNaivePathIntegral) by replacing all occurences of $y$ with a shifted version $y + s n$, for arbitrarily small lengths $s \in \mathbb{R}_+$ of the normal/framing vector $s n$:

\[
  \label{AbelianCSWilsonLoopObservableRenormalized}
  \Bigg\langle
  \exp\bigg(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    \gamma^\ast A
  \bigg)
  \Bigg\rangle
  \;\coloneqq\;
  \underset{
    s \to 0
  }{\lim}
  \exp\bigg(
    -\tfrac{\mathrm{i}}{4K}
    \textstyle{\underset{(S^1)^n}{\iint}}
    \, 
    \mathrm{d} x
    \, 
    \mathrm{d} y
    \,
    \epsilon_{\mu \nu \rho}  
    \frac{
      x^\rho
        - 
      \big(y^\rho + p n^\rho\big)
    }{
      \left\vert 
        x 
        - 
        \big(
          y + s n
        \big) 
      \right\vert^3
    } 
  \bigg)
  \,,
\]
where the [[limit of a sequence|limit]] $s \to 0$ is over normal vector fields that keep the given [[direction of a vector|direction]] but shrink in [[length]] (cf. [GMR 1994 (1.5)](#GMR94)).

This expression (eq:AbelianCSWilsonLoopObservableRenormalized) is finally well-defined. 


#### The knot-theoretic expression

The shift along the framing vector in (eq:AbelianCSWilsonLoopObservableRenormalized) does not change that part of the integral, with respect to the naive (eq:AbelianCSWilsonLoopObservableByNaivePathIntegral), where $\sigma$ and $\sigma'$ run over distinct [[connected components]] (eq:ConnectedComponentsOfALink) of the link, hence that part now does give the sum of the [[linking numbers]] among the connected components of the the [[oriented link]]. At the same time, the shift makes the contributions where $\sigma$ and $\sigma'$ do run over the same connected component become the [[linking number]] of that component with its shift by the framing, which is its *self-linking* or *[[framing number]]*.

The end result of this argument is hence, in the exponent, the sum of the [[framing numbers]] $frm(\gamma_i) \in \mathbb{Z}$ of each link component $\gamma_i$ (eq:ConnectedComponentsOfALink) with the [[linking numbers]] $lnk(\gamma_i, \gamma_j) \in \mathbb{Z}$ all pairs of distinct link components, which is its *[[writhe]]* $wrth(\gamma) \in \mathbb{Z}$ of the link:
\[
  \label{AbelianCSWilsonLoopsInTermsOfFramingAndLinkingNumbers}
  \Bigg\langle
  \exp\bigg(
    \mathrm{i}
    \textstyle{\underset{{(S^1)^n}}{\int}} 
    \gamma^\ast A
  \bigg)
  \Bigg\rangle
  \;=\;
  \exp\bigg(
    \tfrac{\pi \mathrm{i}}{K}
    \Big(
      \underset{
        wrth(\gamma)
      }{
      \underbrace{
        \textstyle{\sum_{i}}
        frm(\gamma_i)
        +
        \textstyle{\sum_{i \neq j}}
        lnk(\gamma_i, \gamma_j)
      }
      }
    \Big)
  \bigg)
  \mathrlap{\,.}
\]

([Witten 1989 (2.31) ff](#Witten89), cf. [Kaul 1999 (9)](#Kaul99), [Guadagnini & Thuillier 2008 (5.2)](#GuadagniniThuillier08), [Mezei, Pufu & Wang 2017 (5.1)](#MezeiPufuWang17) [^LevelNormalizationInAbelianWilsonLoopComputation])

[^LevelNormalizationInAbelianWilsonLoopComputation]: Beware that [Witten 1989](#Witten89) drops a factor of 2 in passing from (1.3) to (2.27) there. This amounts to shifting the Chern-Simons level "$k$" --- our $K$ (eq:TheLagrangianDensity) --- by a factor of 2. His end result for the Wilson loop, equation (2.31) there, is expressed with respect to this shifted level. Transforming back to the original and usual normalization in (1.3) there cancels the factor of 2 in (2.31) there, which thereby agrees with our (eq:AbelianCSWilsonLoopsInTermsOfFramingAndLinkingNumbers) (under $k_{there} = K_{here}$). Note also that [Kaul 1999](#Kaul99) follows along with a lost factor of 2 in (1) there and hence gives in (9) there Witten's formula, while [Mezei, Pufu & Wang 2017 (5.1)](#MezeiPufuWang17) appear to have noticed the glitch. Unfortunately, this is all the more confusing as there is generally an ambiguity of a factor of 2 in what one may want to mean by the abelian Chern-Simons level in the first place, as discussed [above](#LagrangianDensityAndLevel).



Note though that none of the intermediate steps towards (eq:AbelianCSWilsonLoopObservableRenormalized) was well-defined, so that this traditional argument --- impactful as it historically was and "correct" as it may be in its conclusion (eq:AbelianCSWilsonLoopsInTermsOfFramingAndLinkingNumbers) --- is somewhat unsatisfactory as a derivation of quantum observables from input data.



\linebreak


### Abelian Chern-Simons as effective QFT for FQH systems
 {#AbelianCSTheoryAsEffectiveQFTForFRactionalQuantumHall}

The following is a streamlined digest of the traditional argument and Ansatz &lbrack;originally culminating in [Zee 1995](#Zee95), [Wen 1995](#Wen95), more recently highlighted by [Witten 2016 pp 30](#Witten16), [Tong 2016 §5](#Tong16)&rbrack; for [[abelian Chern-Simons theory]] at [[level (Chern-Simons theory)|level]] $k \in \mathbb{N}$ as an [[effective field theory]] for [[fractional quantum Hall systems]] at filling fraction $\nu = 1/2k$.


\linebreak


#### Preliminaries

Consider a [[spacetime]] $\Sigma$ of [[dimension of a manifold|dimension]] $1 + 2$, to be thought of as the [[worldvolume]] of the conducting sheet that hosts the [[fractional quantum Hall system]].

On this spacetime, the electric [[current density]] is a [[differential 2-form]] $J$.

Note that the corresponding electric current [[vector field]] $\vec J$ is characterized by its [[tensor contraction|contraction]] into the given [[volume form]] $dvol$ being equal to the density 2-form

$$
  J \;=\; dvol\big(\, \vec J, \cdots \big)
  \,,
$$

and that the conservation law for $\vec J$, hence the vanishing of its [[divergence]] is equivalent to the density 2-form being [[closed differential form]]:

\[
  \label{CurrentConservationLaw}
  div \vec J \;=\; 0
  \;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;
  \mathrm{d} J \;=\; 0
  \,.
\]

We write $A$ for the [[vector potential]] 1-form on $\Sigma$ which encodes the [[background field|background]] [[electromagnetic field]], and $F \,=\, \mathrm{d}A$ for its [[field strength]], the [[Faraday tensor]]. Since we regard this as a fixed [[background field]], we do not (need to) consider the [[Maxwell-Chern-Simons theory|Maxwell]] [[Lagrangian density]] $L_{YM} \,\coloneqq\, F \wedge \star F$.

But we do (need to) consider the interaction term between the electromagnetic field and the electric current density, which is 

\[
  \label{ElectricInteractionTerm}
  L_{int} \,\coloneqq\, A \wedge J
  \,.
\]

Here we assume that $A$ is globally defined, in fact we shall assume that $\Sigma$ has vanishing [[de Rham cohomology]] in degree=2,

\[
  \label{AssumingdeRham2CohomologyVanishes}
  H^2_{dR}(\Sigma) \;=\; 0
  \,.
\]

This means we are focused on the local nature of fields, not on their global properties, as (for better or worse) usual for [[Lagrangian field theory]].
 
\linebreak


#### The Ansatz

**The auxiliary gauge potential.**
With the assumption (eq:AssumingdeRham2CohomologyVanishes) also the conserved current density (eq:CurrentConservationLaw) admits a [[coboundary]], a [[differential 1-form]] to be denoted $a$:

\[
  \label{AuxiliaryGaugePotential}
  J \,=\, \mathrm{d}a
  \,.
\]

The central Ansatz of the approach is to *think of this 1-form as an effective dynamical gauge field for the FQH dynamics*.

\linebreak

**The Lagrangian density.** This in turn suggests that the effective [[Lagrangian density]] should be the sum of

1. the interaction term (eq:ElectricInteractionTerm) already mentioned, which thus specializes to

   $$
     L_{int} \;=\; A \wedge J \;=\; A \wedge \mathrm{d}a
     \,,
   $$

1. a further interaction term for $a$, now regarded as a gauge potential, to its own current density $j$, to be thought of as the current of FQH [[quasi-particles]] (or quasi-holes)

   \[
     \label{QuasiParticleCoupling}
     L_{quas} \;=\; a \wedge j
   \]

1. a kinetic term for $a$ itself, where the only sensible choice is the [[Chern-Simons theory|Chern-Simons form]] at [[level (Chern-Simons theory)|level]] $k = K/2 \in \mathbb{Z}/2$

   $$
     L_{CS} \;=\; K \tfrac{1}{2} a \wedge \mathrm{d}a
     \,.
   $$

In total, the traditional Ansatz for the effective Lagrangian density for "single layer" FQH systems at filling fraction $1/K$ is hence:

\[
  \label{TheEffectiveLagrangianDensity}
  L 
  \,\coloneqq\,
  K \tfrac{1}{2}\, a\wedge \mathrm{d}a
  \,-\,
  A \wedge 
  \underset{J}{
    \underbrace{
      \mathrm{d}a
    }
  }
  \,-\,
  a \wedge j
  \,.
\]

&lbrack;[Wen 1995 (2.11)](#Wen95), reviewed in [Wen 2007 (7.3.10)](#Wen07)&rbrack;

\linebreak

**The equation of motion.**
The [[Euler-Lagrange equation]] [[equation of motion|of motion]] for the effective gauge field $a$ induced by (eq:TheEffectiveLagrangianDensity) is simply

\[
  \label{EquationOfMotion}
  \frac{\delta L}{\delta A}
  \;=\;
  0
  \;\;\;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;\;\;
  J
    \,=\,
  \tfrac{1}{k}\Big(
    F + j
  \Big)
  \,.
\]

> (This means in particular that if, on topologically non-trivial $\Sigma$, one were to insist (which is not a logical necessity) to subject the effective gauge field $a$ to [[Dirac charge quantization]] (as $A$ is), then the ordinary electromagnetic field would have to be assumed to carry magnetic charge being a multiple of $k$.)

\linebreak

#### Reproducing FQH phenomena

**Recovering the Hall conductivity.**
The first plausibility check on the effective model is to observe that its equation of motion (eq:EquationOfMotion) implies the correct Hall conductivity relation for a [[fractional quantum Hall system]] at filling fraction $1/k$:

Namely assuming that the electric field is oriented in the $y$-direction, so that the [[Faraday tensor]] is of the form (cf [there](Maxwell's+equations#InTermsOfFaradayTensor)):

$$
  F 
  \;=\;
  E_y \mathrm{d}t \wedge \mathrm{d}y
  +
  B \mathrm{d}x\wedge \mathrm{d}y
$$

and assuming that the quasi-particles are stationary, so that 

$$
  j 
    \;\propto\; 
  dvol(\partial_0) 
    \;\propto\; 
  \mathrm{d}x \wedge \mathrm{d}y
  \mathrlap{\,,}
$$

the temporal component of the equation of motion (eq:EquationOfMotion) becomes

$$
  J_x \;=\; \tfrac{1}{k} E_y
$$

which is the correct form of the *Hall field* $E_y$ for given longitudinal current $J_X$ at filling fraction $\nu = 1/k$ -- see [there](quantum+Hall+effect#eq:HeightOfFractionalHallPlateaux).

> (Following [Zee 1995 (4.5)](#Zee95), later authors &lbrack;[Witten 2016 §2.3](#Witten16), [Tong 2016 p 161](#Tong16)&rbrack; deduce this in a more roundabout way, by first inserting the equation of motion back into the Lagrangian density and then varying that with respect to $A$. It seems that this unnecessary step is brought about by first tacitly renaming "$J$" to "$f$" and then forgetting that this was just a renaming.)

\linebreak

**Recovering the fractional quasi-particles.**
Second, the spatial component of the equation of motion (eq:EquationOfMotion) says that (1.) the magnetic flux quanta and (2.) the quasi-particles contribute their $k$th fraction to the total charge density:

$$
  J_0 \;=\; \tfrac{1}{K}(B + j_0)
  \,.
$$

Here 

* statement (1) reflects exactly the composite fermion model, where at $k$th filling fraction each electron is bound to $k$ quanta of magnetic flux 

* statement (2) is the desired property of quasi-particles to have $k$th fractional charge.


\linebreak

This largely concludes the traditional justification for the effective abelian Chern-Simons theory (eq:TheEffectiveLagrangianDensity).

\linebreak


#### Hierarchical K-matrix formalism
 {#HierarchicalKMatrixFormalism}

Following the hierarchical picture of [[FQH systems]] at non-unit filling fraction (due to [Haldane 1983](quantum+Hall+effect#Haldane83) and [Halperin 1984](quantum+Hall+effect#Halperin1984), whence "HH-hierachy"), where [[quasiparticles]] at unit filling fractions are imagined to support themselves a secondary FQH effect with secondary quasi-particles, and so on  (a picture that faces various experimental challenges, cf. [Jain 2007 §12.1](quantum+Hall+effect#Jain07), [Jain 2014, esp. p 8](quantum+Hall+effect#Jain14) and Rem. \ref{PhenomenologyOfKMatrixFormalism} below), authors consider abelian Chern Simons theory of multiple gauge fields that are hierarchically coupled to each other, called the "K-matrix formalism" ([Blok & Wen 1990](#BlokWen90), [Wen & Zee 1992](#WenZee92Classification), early review in [Wen 1995 §2.1](#Wen95), textbook account in [Wen 2007 §7.3.3](#Wen07)).

The basic idea is to observe that the above step from (i) introducing a gauge potential (eq:AuxiliaryGaugePotential) for the electron current density $J$ to (ii) the effective Chern-Simons action (eq:TheEffectiveLagrangianDensity) with quasi-particle current density $j$ may be repeated by next introducing also a gauge potential for the quasi-particle current (cf. [Wen 2007 (7.3.13)](#Wen07)), and so on.

Concretely, postulating that the quasi-particle current $j$ (eq:QuasiParticleCoupling) is itself the field strength of a secondary auxiliary gauge field $a^{(2)}$

$$
  j \,=\, \mathrm{d} a^{(2)}
$$

(and renaming the previous auxiliary gauge field to $a^{(1)} \equiv a$)

and then adjoining for that secondary gauge field another Chern-Simons kinetic term, turns the effective Lagrangian density (eq:TheEffectiveLagrangianDensity) into

\[
  \label{TheSecondaryEffectiveLagrangianDensity}
  L_{1,2} 
  \,\coloneqq\,
  K_1 \tfrac{1}{2}\, a^{(1)} \wedge \mathrm{d} a^{(1)}
  \,-\,
  A \wedge 
  \underset{J}{
    \underbrace{
      \mathrm{d} a^{(1)}
    }
  }
  \,-\,
  a^{(1)} 
    \wedge 
  \underset{j}{
    \underbrace{
      \mathrm{d} a^{(2)}
    }
  }
  \,+\,
  K_2 \tfrac{1}{2}\, 
    a^{(2)} \wedge \mathrm{d} a^{(2)}
  \,.
\]

(cf. [Wen 1995 (2.15)](#Wen95), [Wen 2007 (7.3.13)](#Wen07))

meant to be an effective theory at filling fraction

\[
  \label{SecondHierarchyFillingFraction}
  \nu
  \;=\;
  \tfrac
    { 1 }
    { K_1 - \tfrac{1}{K_2} }
  \,.
\]

(cf. [Wen 1995 (2.18)](#Wen95), [Wen 2007 (7.3.15)](#Wen07))


Now this secondary effective Lagrangian (eq:TheSecondaryEffectiveLagrangianDensity) may be rewritten equivalently as (using [[Einstein summation convention]])

\[
  \label{SecondaryEffectiveLagrangianInKMatrixForm}
  L_{1,2}
  \;=\;
  K_{i j} \tfrac{1}{2} a^{(i)} \wedge \mathrm{d} a^{(j)}   
  -
  Q_i \, A \wedge \mathrm{d} a^{(i)}
\]

with the *K-[[matrix]]*

$$
  K
  \;\coloneqq\;
  \left[
  \begin{matrix}
    K_1 & -1
    \\
    -1 & K_2
  \end{matrix}
  \right]
$$

and the *charge vector*

$$
  Q
  \;\coloneqq\;
  \left[
  \begin{matrix}
    1
    \\
    0
  \end{matrix}
  \right]
  \,.
$$

(cf. [Wen 1995 (2.19)](#Wen95), [Wen 2007 (7.3.15)](#Wen07)).

Observing that the [[inverse matrix|inverse]] K-matrix is 

\[
  \label{InverseKMatrixAtSecondLayer}
  K^{-1}
  \,=\,
  \tfrac{1}{K_1 K_2 - 1}
  \left[
  \begin{matrix}
    K_2 & 1
    \\
    1 & K_1
  \end{matrix}
  \right]
\]

the second-layer filling fraction (eq:SecondHierarchyFillingFraction) is recognized as the top left entry of (eq:InverseKMatrixAtSecondLayer) and hence re-expressed in terms of these matrix quantities as

$$
  \nu \,=\, Q^t \cdot K^{-1} \cdot Q
  \,.
$$

(cf. [Wen 2007 (7.3.19)](#Wen07))


\begin{remark}
 \label{PhenomenologyOfKMatrixFormalism}
 The phenomenological (experimental) validity already of the [HH-hierarchy](#HierarchicalKMatrixFormalism) underlying this K-matrix formulation, when applied to ordinary single-component [[FQH systems]], has been called into question ([Jain 2007 §12.1](quantum+Hall+effect#Jain07) and [Jain 2014, esp. p 8](quantum+Hall+effect#Jain14)):  The required assumptions on quasi-particle densities necessary for the hierarchy to be physically plausible seem to be drastically violated, and in any case the experimentally observed filling fractions do not reflect the predicted hierarchy.

On the other hand, the K-matrix formalism may be the natural description of *multi-*component FQH systems, where each column/row of the K-matrix corresponds to one "component" of possible electron modes (e.g. different spin polarizations or different layers in multi-layer materials), cf. [Barkeshli & Wen 2017](#BarkeshliWen17), [Sodemann et al 2017](#SodemannEtAl17), [Zeng 2021](#Zeng21) [Hu, Liu & Zhu 2023](#HuLiuZhu23), [Zeng 2024](#Zeng24).
\end{remark}




\linebreak





## Related concepts

* [[Maxwell-Chern-Simons theory]]

* [[Chern-Simons theory]]

* [[quantization of D=3 Chern-Simons theory]]

* [[fractional quantum Hall effect]]

* [[integer Heisenberg group]]



## References

### General
 {#ReferencesGeneral}

General discussion of abelian Chern-Simons theory:

* Michiel Bos, [[V. Parameswaran Nair]]: *$U(1)$ Chern-Simons theory and $c=1$ conformal blocks*, Physics Letters B **223** 1 (1989) 61-66 \[<a href="https://doi.org/10.1016/0370-2693(89)90920-9">doi:10.1016/0370-2693(89)90920-9</a>\]

* [[Alexios P. Polychronakos]]: *Abelian Chern-Simons theories in $2+1$ dimensions*, Annals of Physics **203** 2 (1990) 231-254 \[<a href="https://doi.org/10.1016/0003-4916(90)90171-J">doi:10.1016/0003-4916(90)90171-J</a>\] 

* Antoine Coste, Michel Makowka: *Abelian Chern-Simons theories on $S^3$*, Nuclear Physics B **342** 3 (1990) 721-736 \[<a href="https://doi.org/10.1016/0550-3213(90)90334-A">doi:10.1016/0550-3213(90)90334-A</a>\]

* [[Sergio Albeverio]], J. Schäfer: *Rigorous Approach to Abelian Chern-Simons Theory*, in *Groups and Related Topics*, Mathematical Physics Studies **13**,  Springer (1992) 143-152 &lbrack;[doi:10.1007/978-94-011-2801-8_12](https://doi.org/10.1007/978-94-011-2801-8_12)&rbrack;

* {#WesolowskiHosotaniHo94} D. Wesolowski, Y. Hosotani, C.-L. Ho: *Multiple Chern-Simons Fields on a Torus*,  	Int. J. Mod. Phys. A **9** (1994) 969-989 &lbrack;[arXiv:hep-th/9302121](https://arxiv.org/abs/hep-th/9302121), [doi:10.1142/S0217751X94000443](https://doi.org/10.1142/S0217751X94000443)&rbrack;

* G. Giavarini, C. P. Martin, [[Fernando Ruiz Ruiz]]: *Abelian Chern-Simons theory as the strong large-mass limit of topologically massive abelian gauge theory: the Wilson loop*, Nucl. Phys. B **412** (1994) 731-750 &lbrack;[arXiv:hep-th/9309049](https://arxiv.org/abs/hep-th/9309049), <a href="https://doi.org/10.1016/0550-3213(94)90397-2">doi:10.1016/0550-3213(94)90397-2</a>, [pdf](https://inis.iaea.org/collection/NCLCollectionStore/_Public/25/053/25053343.pdf)&rbrack;
  > (on the [[renormalization]] of [[Wilson loop]] [[quantum observables|observables]])

* {#LeukertSchäfer96} Peter Leukert, Jörg Schäfer: *A rigorous construction of abelian Chern-Simons path integrals using white noise analysis*,  Reviews in Mathematical Physics **08** 03  (1996) 445-456 &lbrack;[doi:10.1142/S0129055X96000147](https://doi.org/10.1142/S0129055X96000147)&rbrack;

* [[Gerald V. Dunne]]: *Aspects of Chern-Simons Theory*, in: *Topological aspects of low dimensional systems*, Les Houches -- École d'Été de Physique Théorique **69**, Springer (1999) &lbrack;[doi:10.1007/3-540-46637-1_3](https://doi.org/10.1007/3-540-46637-1_3), [arXiv:hep-th/9902115](https://arxiv.org/abs/hep-th/9902115)&rbrack;

* {#Manoliu98a} Mihaela Manoliu: *Abelian Chern-Simons theory*, J. Math. Phys. **39** (1998) 170-206 &lbrack;[arXiv:dg-ga/9610001](https://arxiv.org/abs/dg-ga/9610001), [doi:10.1063/1.532333](https://doi.org/10.1063/1.532333)&rbrack;

* {#Manoliu98b} Mihaela Manoliu: *Abelian Chern-Simons theory. II: A functional integral approach*, J. Math.Phys. **39** (1998) 207-217 &lbrack;[doi:10.1063/1.532312](https://doi.org/10.1063/1.532312)&rbrack;

* {#DijkgraafWitten90} [[Robbert Dijkgraaf]], [[Edward Witten]]: *Topological Spin Theories*, section 5 in: *Topological Gauge Theories and Group Cohomology*, Commun. Math. Phys. **129** (1990) 393 &lbrack;[doi:10.1007/BF02096988](https://doi.org/10.1007/BF02096988), [euclid:cmp/1104180750](https://projecteuclid.org/journals/communications-in-mathematical-physics/volume-129/issue-2/Topological-gauge-theories-and-group-cohomology/cmp/1104180750.full), [pdf](/nlab/files/DW.pdf)&rbrack;
  > (the notion of abelian [[spin Chern-Simons theory]])

* V. S. Alves, [[Ashok Das]], Silvana Perez: *Screening Length in $2+1$-dimensional Abelian Chern-Simons Theories*, Phys. Lett. B **531** (2002) 289-300 &lbrack;[arXiv:hep-th/0201207](https://arxiv.org/abs/hep-th/0201207), <a href="https://doi.org/10.1016/S0370-2693(02)01486-7">doi:10.1016/S0370-2693(02)01486-7</a>&rbrack;


* {#BelovMoore05} Dmitriy Belov, [[Gregory W. Moore]]: *Classification of abelian spin Chern-Simons theories* &lbrack;[arXiv:hep-th/0505235](https://arxiv.org/abs/hep-th/0505235)&rbrack;
  > (with focus on refinement to [[Spin Chern-Simons theory]])

* Spencer D. Stirling: *Abelian Chern-Simons theory with toral gauge group, modular tensor categories, and group categories*, PhD thesis, Austin (2008) &lbrack;[arXiv:0807.2857](http://arxiv.org/abs/0807.2857), [pdf](http://www.spencerstirling.com/papers/thesis_official.pdf), [ProQuest](https://www.proquest.com/docview/304474017?pq-origsite=gscholar&fromopenview=true&sourcetype=Dissertations%20&%20Theses)&rbrack;

* [[Lisa Jeffrey]], Brendan McLellan: *Eta-Invariants and Anomalies in $U(1)$ Chern-Simons Theory* &lbrack;[arXiv:1004.2913](https://arxiv.org/abs/1004.2913)&rbrack;

* {#GuadagniniThuillier08} [[Enore Guadagnini]], [[Frank Thuillier]]: *Deligne-Beilinson cohomology and abelian links invariants*, SIGMA **4** (2008) 078 &lbrack;[arXiv:0801.1445](https://arxiv.org/abs/0801.1445), [doi:10.3842/SIGMA.2008.078](https://doi.org/10.3842/SIGMA.2008.078)&rbrack;

* [[Enore Guadagnini]], [[Frank Thuillier]]: *Three-manifold invariant from functional integration*, J. Math. Phys. **54** (2013) 082302 &lbrack;[arXiv:1301.6407](https://arxiv.org/abs/1301.6407), [doi:10.1063/1.4818738](https://doi.org/10.1063/1.4818738)&rbrack;

* [[Enore Guadagnini]], [[Frank Thuillier]]: *Path-integral invariants in abelian Chern–Simons theory*, Nuclear Physics B **882** (2014) 450-484 &lbrack;[doi:10.1016/j.nuclphysb.2014.03.009](https://doi.org/10.1016/j.nuclphysb.2014.03.009), [arXiv:1402.3140](https://arxiv.org/abs/1402.3140)&rbrack;

* Diego Delmastro, [[Jaume Gomis]]: *Symmetries of Abelian Chern-Simons Theories and Arithmetic*, J. High Energ. Phys. **2021** 6 (2021) &lbrack;<a href="https://doi.org/10.1007/JHEP03(2021)006">doi:10.1007/JHEP03(2021)006</a>, [arXiv:1904.12884](https://arxiv.org/abs/1904.12884)&rbrack;

* Han-Miru Kim, Philippe Mathieu, Michail Tagaris, [[Frank Thuillier]]: *$U(1)^n$ Chern-Simons theory: partition function, reciprocity formula and CS-duality* &lbrack;[arXiv:2409.10734](https://arxiv.org/abs/2409.10734)&rbrack;


Many general reviews of [[Chern-Simons theory]] have a section focused on the abelian case, for instance:

* [[Gregory Moore]], §2 in: *Introduction to Chern-Simons Theories*, TASI lecture notes (2019) &lbrack;[pdf](https://www.physics.rutgers.edu/~gmoore/TASI-ChernSimons-StudentNotes.pdf), [[Moore-IntroChern-Simons.pdf:file]]&rbrack;

* David Grabovsky, §1 in: *Chern–Simons Theory in a Knotshell* (2022) &lbrack;[pdf](https://web.physics.ucsb.edu/~davidgrabovsky/files-notes/CS%20and%20Knots.pdf), [[Grabovsky-CSTheory.pdf:file]]&rbrack;

On the [[light-cone quantization]] of abelian Chern-Simons theory:

* Prem P. Srivastava: *Light-Front Dynamics of Chern-Simons Systems* &lbrack;[arXiv:hep-th/9412239](https://arxiv.org/abs/hep-th/9412239)&rbrack;

* L. R. U. Manssur: *Canonical Quantization of Chern-Simons on the Light-Front*, Phys. Lett. B **480** (2000) 229-236 &lbrack;[arXiv:hep-th/9910127v1](https://arxiv.org/abs/hep-th/9910127), <a href="https://doi.org/10.1016/S0370-2693(00)00380-4">doi:10.1016/S0370-2693(00)00380-4</a>&rbrack;


Via the [[Reshetikhin-Turaev construction]]:

* [[Enore Guadagnini]], Francesco Mancarella: *Abelian link invariants and homology*, J. Math. Phys. **51** (2010) 062301 &lbrack;[arXiv:1004.5211](https://arxiv.org/abs/1004.5211)&rbrack;

* Philippe Mathieu, [[Frank Thuillier]]: *Abelian Turaev-Virelizier theorem and $U(1)$ BF surgery formulas* &lbrack;[arXiv:1706.01845](https://arxiv.org/abs/1706.01845)&rbrack;


On abelian Chern-Simons theory via [[theta functions]] and the [[representation theory]] of the [[integer Heisenberg group]]:

* {#GelcaUribe10} [[Răzvan Gelca]], [[Alejandro Uribe]]: *From classical theta functions to topological quantum field theory*, in: *The Influence of Solomon Lefschetz in Geometry and Topology: 50 Years of Mathematics at CINVESTAV*, Contemporary Mathematics **621**, AMS (2014) 35-68 &lbrack;[arXiv:1006.3252](http://arxiv.org/abs/1006.3252), [doi;10.1090/conm/621](https://doi.org/10.1090/conm/621), [ams:conm-621](https://bookstore.ams.org/conm-621), [slides pdf](http://www.math.ttu.edu/~rgelca/berk.pdf), [[GelcaUribe-ThetaFunctionsTQFT.pdf:file]]&rbrack;

* {#GelcaHamilton12} [[Răzvan Gelca]], [[Alastair Hamilton]]: *Classical theta functions from a quantum group perspective*, New York J. Math. **21** (2015) 93–127 &lbrack;[arXiv:1209.1135](http://arxiv.org/abs/1209.1135), [nyjm:j/2015/21-4](https://nyjm.albany.edu/j/2015/21-4.html)&rbrack;

* {#GelcaHamilton15} [[Răzvan Gelca]], [[Alastair Hamilton]]: *The topological quantum field theory of Riemann’s theta functions*, Journal of Geometry and Physics **98** (2015) 242-261 &lbrack;[doi:10.1016/j.geomphys.2015.08.008](https://doi.org/10.1016/j.geomphys.2015.08.008), [arXiv:1406.4269](https://arxiv.org/abs/1406.4269)&rbrack;

On the [[self-dual gauge theory|chiral]] abelian [[WZW model]] ([[edge modes]]) at the [[boundary field theory|boundary]] of abelian Chern-Simons theory:

* [[Irais Rubalcava-Garcia]]: *Constructing the theory at the boundary, its dynamics and degrees of freedom* &lbrack;[arXiv:2003.06241](https://arxiv.org/abs/2003.06241)&rbrack;


On [[boundary conditions]] and line-[[defect field theory|defects]] in abelian Chern-Simons theory and on the corresponding ground state degeneracy ([[topological order]]) on [[surfaces]] with ("gapped") [[boundary of a manifold|boundaries]]:

* [[Anton Kapustin]], [[Natalia Saulina]]: *Topological boundary conditions in abelian Chern-Simons theory*, Nucl. Phys. B **845** (2011) 393-435 &lbrack;[arXiv:1008.0654](https://arxiv.org/abs/1008.0654), [doi:10.1016/j.nuclphysb.2010.12.017](https://doi.org/10.1016/j.nuclphysb.2010.12.017)&rbrack;

* {#KapustinSaulina} [[Anton Kapustin]], [[Natalia Saulina]],  §3 in: *Surface operators in 3d TFT and 2d Rational CFT*, in: [[Hisham Sati]], [[Urs Schreiber]] (eds.), *[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]*, Proceedings of Symposia in Pure Mathematics **83**, AMS (2011) &lbrack;[arXiv:1012.0911](http://arxiv.org/abs/1012.0911), [ams:pspum-83](https://bookstore.ams.org/pspum-83)&rbrack;

* [Levin 2013](#Levin13)

* [[Anton Kapustin]]: *Ground-state degeneracy for abelian anyons in the presence of gapped boundaries*, Phys. Rev. B **89** (2014) 125307  &lbrack;[arXiv:1306.4254](https://arxiv.org/abs/1306.4254), [doi:10.1103/PhysRevB.89.125307](https://doi.org/10.1103/PhysRevB.89.125307)&rbrack;

* [[Juven C. Wang]], [[Xiao-Gang Wen]]: *Boundary Degeneracy of Topological Order*, Phys. Rev. B **91** (2015) 125124 &lbrack;[doi:10.1103/PhysRevB.91.125124](https://doi.org/10.1103/PhysRevB.91.125124), [arXiv:1212.4863](https://arxiv.org/abs/1212.4863)&rbrack;

* Jackson R. Fliss, Xueda Wen, Onkar Parrikar, Chang-Tse Hsieh, Bo Han, Taylor L. Hughes, Robert G. Leigh: *Interface Contributions to Topological Entanglement in Abelian Chern-Simons Theory*, JHEP 09 (2017) 056 &lbrack;[arXiv:1705.09611](https://arxiv.org/abs/1705.09611), <a href="https://doi.org/10.1007/JHEP09(2017)056">doi:10.1007/JHEP09(2017)056</a>&rbrack;


and with [[fermion|fermionic]] [[boundary field theory|boundary]] [[2d CFT]]:

* Kohki Kawabata, Tatsuma Nishioka, Takuya Okuda, Shinichiro Yahagi: *Fermionic CFTs from topological boundaries in abelian Chern-Simons theories* &lbrack;[arXiv:2502.08084](https://arxiv.org/abs/2502.08084)&rbrack;





Discussion via [[locally covariant AQFT|locally covariant]] [[algebraic quantum field theory]]:

* [[Claudio Dappiaggi]], [[Simone Murro]], [[Alexander Schenkel]]: *Non-existence of natural states for Abelian Chern-Simons theory*, J. Geom. Phys. **116** (2017) 119-123 &lbrack;[arXiv:1612.04080](https://arxiv.org/abs/1612.04080), [arXiv:10.1016/j.geomphys.2017.01.015](https://doi.org/10.1016/j.geomphys.2017.01.015)&rbrack;


On [[lattice gauge theory|lattice formulation]] of abelian Chern-Simons theory:

* Kai Sun, Krishna Kumar, [[Eduardo Fradkin]]: *Discretized Abelian Chern-Simons gauge theory*, Phys. Rev. B **92** (2015) 115148 &lbrack;[doi:10.1103/PhysRevB.92.115148](https://doi.org/10.1103/PhysRevB.92.115148)&rbrack;

* [[Theodore Jacobson]], [[Tin Sulejmanpasic]]: *Modified Villain formulation of abelian Chern-Simons theory*, Phys. Rev. D **107** (2023) 125017 &lbrack;[arXiv:2303.06160](https://arxiv.org/abs/2303.06160), [doi:10.1103/PhysRevD.107.125017](https://doi.org/10.1103/PhysRevD.107.125017)&rbrack;

and its canonical [[quantization of D=3 Chern-Simons theory|quantization]]:

* [[Theodore Jacobson]], [[Tin Sulejmanpasic]]: *Canonical quantization of lattice Chern-Simons theory*, High Energ. Phys. **2024** (2024) 87 &lbrack;[arXiv:2401.09597](https://arxiv.org/abs/2401.09597), <a href="https://doi.org/10.1007/JHEP11(2024)087">doi:10.1007/JHEP11(2024)087</a>&rbrack;




In relation to the [[dilogarithm]]:

* [[Daniel S. Freed]], [[Andrew Neitzke]]: *The dilogarithm and abelian Chern-Simons*, J. Differential Geom. **123**  2  (2023) 241-266 &lbrack;[arXiv:2006.12565](https://arxiv.org/abs/2006.12565), [doi:10.4310/jdg/1680883577](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-123/issue-2/The-dilogarithm-and-abelian-ChernSimons/10.4310/jdg/1680883577.short)&rbrack;

On unoriented manifolds:

* Ippo Orii: *On dimensions of $(2+1)D$ abelian bosonic topological systems on unoriented manifolds* &lbrack;[arXiv:2502.13532](https://arxiv.org/abs/2502.13532)&rbrack;

Coupled to a [[Higgs field]]:

* Yoonbai Kim, O-Kab Kwon, Hanwool Song, Chanju Kim: *Inhomogeneous Abelian Chern-Simons Higgs Model with New Inhomogeneous BPS Vacuum and Solitons* &lbrack;[arXiv:2409.11978](https://arxiv.org/abs/2409.11978)&rbrack;


### Wilson loop observables
 {#ReferencesWilsonLoopObservables}

Discussion of [[Wilson loop]] [[quantum observables]] in abelian Chern-Simons theory, via [[path integral]] arguments followed by [[renormalization]] via [[framed link|framing]]:

* {#Polyakov88} [[Alexander Polyakov]]: *Fermi-Bose Transmutations induced by Gauge Fields*, Modern Physics Letters A **3** 3 (1988) 325-328 &lbrack;[doi:10.1142/S0217732388000398](https://doi.org/10.1142/S0217732388000398), [[Polyakov-MPA-1988.pdf:file]]&rbrack;

* {#Witten89} [[Edward Witten]], §2.1 in: *Quantum Field Theory and the Jones Polynomial*, Commun. Math. Phys. **121** 3 (1989) 351-399 &lbrack;[doi:10.1007/BF01217730](https://doi.org/10.1007/BF01217730), [euclid:cmp/1104178138](http://projecteuclid.org/euclid.cmp/1104178138), MR0990772 &rbrack;

* {#CosteMakowka90} Antoine Coste, Michel Makowka: *Abelian Chern-Simons theories on $S^3$*, Nuclear Physics B **342** 3 (1990) 721-736 \[<a href="https://doi.org/10.1016/0550-3213(90)90334-A">doi:10.1016/0550-3213(90)90334-A</a>\]

* {#GMR94} G. Giavarini, C. P. Martin, [[Fernando Ruiz Ruiz]]: *Abelian Chern-Simons theory as the strong large-mass limit of topologically massive abelian gauge theory: the Wilson loop*, Nuclear Physics B **412** (1994) 731-750 &lbrack;[arXiv:hep-th/9309049](https://arxiv.org/abs/hep-th/9309049), <a href="https://doi.org/10.1016/0550-3213(94)90397-2">doi:10.1016/0550-3213(94)90397-2</a>&rbrack;

* [Leukert & Schäfer 1996 §7](#LeukertSchäfer96)

* {#Hahn04a} [[Atle Hahn]], §9 of: *Chern–Simons theory on $\mathbb{R}^3$ in axial gauge: a rigorous approach*, Journal of Functional Analysis **211** 2 (2004) 483-507 &lbrack;[doi:10.1016/j.jfa.2004.01.006](https://doi.org/10.1016/j.jfa.2004.01.006)&rbrack;

* {#Hahn04b} [[Atle Hahn]]: *The Wilson Loop Observables of Chern-Simons Theory on $\mathbb{R}^3$ in Axial Gauge*,  Commun. Math. Phys. **248** (2004) 467–499 &lbrack;[doi:10.1007/s00220-004-1097-4](https://doi.org/10.1007/s00220-004-1097-4), [inSpire:667450](https://inspirehep.net/literature/667450)&rbrack;

* [Guadagnini & Thuillier 2008](#GuadagniniThuillier08)

Review:

* {#Kaul99} [[Romesh K. Kaul]], section 3 of: *Topological Quantum Field Theories -- A Meeting Ground for Physicists and Mathematicians* &lbrack;[arXiv:hep-th/9907119](https://arxiv.org/abs/hep-th/9907119)&rbrack;

* {#MezeiPufuWang17} [[Márk Mezei]], [[Silviu S. Pufu]], Yifan Wang: *Chern-Simons theory from M5-branes and calibrated M2-branes*,  J. High Energ. Phys. **2019** 165 (2019) \[<a href="https://doi.org/10.1007/JHEP08(2019)165">doi:10.1007/JHEP08(2019)165</a>, [arXiv:1812.07572](https://arxiv.org/abs/1812.07572)\]

Alternative discussion via [[geometry of physics -- flux quantization|proper flux quantization]]:

* [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Cohomotopy and Framed Links|Cohomotopy, Framed Links, and Abelian Anyons]]* &lbrack;[arXiv:2408.11896](https://arxiv.org/abs/2408.11896)&rbrack;

* [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Renormalization of Wilson Loops|Renormalization of Wilson Loop Observables via Proper Flux Quantization in Cohomotopy]]* &lbrack;[arXiv:2509.25336](https://arxiv.org/abs/2509.25336)&rbrack;






[[!include abelian Chern-Simons for fractional quantum Hall effect -- references]]


### Abelian Maxwell-Chern-Simons theory for superconductivity

On 1+2D [[Maxwell-Chern-Simons theory]] as an [[effective field theory|effective]] description of [[superconductivity]]:

* [[M. Cristina Diamantini]], P. Sodano, [[Carlo A. Trugenberger]]: *Gauge Theories of Josephson Junction Arrays*, Nucl. Phys. B **474** (1996) 641-677 \[<a href="https://doi.org/10.1016/0550-3213(96)00309-4">doi:10.1016/0550-3213(96)00309-4</a>, [arXiv:hep-th/9511168](https://arxiv.org/abs/hep-th/9511168)\]

(...)

### For baryons in $N_f=1$ QCD

On [[baryons]] in [[flavor (particle physics)|$N_f = 1$]] [[QCD]] as [[quantum Hall effect|quantum Hall droplets]] [[effective quantum field theory|effectively described]] by abelian Chern-Simons theory:

* [[Zohar Komargodski]]: *Baryons as Quantum Hall Droplets* &lbrack;[arXiv:1812.09253](https://arxiv.org/abs/1812.09253)&rbrack;

* Yong-Liang Ma, [[Maciej A. Nowak]], [[Mannque Rho]], [[Ismail Zahed]], *Baryon as a Quantum Hall Droplet and the Quark-Hadron Duality*, Phys. Rev. Lett. **123** (2019) 172301 &lbrack;[doi:10.1103/PhysRevLett.123.172301](https://doi.org/10.1103/PhysRevLett.123.172301)&rbrack;

* Kentaro Nishimura, Naoki Yamamoto, Ryo Yokokura: *Quantum Hall liquids in high-density QCD* &lbrack;[arXiv:2410.07665](https://arxiv.org/abs/2410.07665)&rbrack;




[[!redirects abelian Chern-Simons theories]]

[[!redirects U(1)-Chern-Simons theory]]
[[!redirects U(1)-Chern-Simons theories]]
