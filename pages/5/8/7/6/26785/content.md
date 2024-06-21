

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A *Riemannian immersion* or *isometric immersion* of [[Riemannian manifolds]] is an [[immersion]] $\Sigma \hookrightarrow X$ of their [[underlying]] [[smooth manifolds]] which is also an [[isometry]] with respect to their [[Riemannian metrics]].

Similarly, an *isometric embedding* is an isometric immersion which is also an [[embedding of smooth manifolds]], hence [[embedding of topological spaces|of the underlying topological spaces]].

The *isometric immersion/embedding problem* is to find isometric immersions/embeddings of Riemannian manifolds into large-dimensional but flat ([[Euclidean spaces|Euclidean]]) spaces (e.g. [Han & Hong 2006](#HanHong06), [Han & Lewicka 2023](#HanLewicka23)).



## Properties
 {#Properties}

Key properties of Riemannian immersion --- such as [whether](#HarmonicImmersion) they are [[harmonic map|harmonic]] --- are encoded in a [[tensor]] called their "[second fundamental form](#SecondFundamentalForm)", which is most immediately expressed in terms of a [local Darboux coframe field](#AdaptedDarbouxCoframes) adapted to the immerison.

\linebreak

For the following purpose:

\begin{definition}
\label{LocalCoFrameField}
A (local) **[[co-frame field]]** on a [[smooth manifold]] $X$ is

1. an [[open cover]] $\widehat{X} \twoheadrightarrow X$

1. [[differential 1-forms]] $E = (E^a)_{a=1}^{dim(X)} \,\in\, \Omega^1_{dR}(\widehat{X})$

such that on double intersections

$$
  \widehat{X} \!\times_X\! \widehat{X}
  \underoverset{pr_2}{pr_1}{\rightrightarrows}
  X
$$

the induced [[metric tensors]] agree:

$$
  \delta_{a b} 
  \,
  pr_1^\ast E^a 
  \otimes
  pr_1^\ast E^b
  \;\;
  =
  \;\;
  \delta_{a b} 
  \,
  pr_2^\ast E^a 
  \otimes
  pr_2^\ast E^b
$$

where we use the [[Einstein summation convention]], throughout.

A [[pair]] of such local co-frames is regarded as equivalent if their induced metric tensors agree on the common [refinement](refinement#RefinementOfOpenCovers) of their respective [[open covers]].
\end{definition}

\linebreak

### Local Darboux (co-)frame field
 {#AdaptedDarbouxCoframes}

Given a [[Riemannian manifold]] $(X,g)$ of [[dimension of a manifold|dimension]] $D$, then 

* an **orthonormal local frame** is an [[open cover]] $p \colon \widehat{X} \twoheadrightarrow X$ equipped with a $D$-[[tuple]] of [[vector fields]]

  $$
    V
    \;\colon\;
    \mathbb{R}^{D} \xrightarrow{\;\;} T \widehat X
  $$

  such that at each point $\widehat x \,\in\, \widehat{X}$ we have that

  $$
    g\big(V,V\big)(x)
  $$

  is the canonical [[inner product]] on $\mathbb{R}^D$, hence in components

  $$
    g\big(V_a, V_b\big)(x)
    \;=\;
    \delta_{a b}
    \,;
  $$

* an **orthonormal local co-frame** is an [[open cover]] $p \colon \widehat{X} \twoheadrightarrow X$ equipped with a $\mathbb{R}^D$-valued [[differential 1-form]]

  $$
    E
    \;\colon\;
    T\widehat{X}
    \xrightarrow{\;\;}
    \mathbb{R}^D
  $$

  such that at each point $\widehat x \,\in\, \widehat{X}$ we have

  $$
    \delta_{a b} \, E^a \otimes E^b
    \;=\;
    g
    \,.
  $$

Now given moreover an [[immersion]] $\phi \colon \Sigma \hookrightarrow X$ into a [[Riemannian manifold]]

* such an orthonormal local frame $V$ is called *adapted* or *Darboux* (generalizing terminology originating in the [[differential geometry of curves and surfaces]], cf. [Guggenheimer 1977, p. 210](#Guggenheimer77), [Petrunin & Barrera 2020, p. 107](differential+geometry+of+curves+and+surfaces#PetruninBarrera20)) for $\phi$ if for each $\sigma \in \Sigma$ and each lift $\widehat{\phi(\sigma)} \in \widehat{X}$ of $\phi(\sigma) \in X$ its first $dim(\Sigma)$ components are tangent to $\Sigma$:

  \[
    \label{DarbouxFrameProperty}
    \underset
      { a \leq dim(\Sigma) }
      {\forall}
    \;\;\;\;\;
    V_a(\sigma) 
      \,\in\, 
    T_\sigma \Sigma
      \subset
    T_{\widehat{\phi(\sigma)}} \widehat{X}
  \]

  ([Sternberg 1964, Def. 2.1 on p. 244](#Sternberg64); [Griffiths & Harris 1979 (1.12)](#GriffithsHarris79); [Berger, Bryant & Griffiths 1983, p. 818](#BergerBryantGriffiths83); [Yang 1992, p. 157](#Yang92))

* such an orthonormal local co-frame $E$ is called *adapted* or *Darboux* (generalizing again the terminology from [[differential geometry of curves and surfaces]], [Cartan 1926, p. 211](#Cartan26)) for $\phi$ if its last $dim(X)-dim(\Sigma)$-components are transversal to $\Sigma$:

  \[
    \label{DarbouxCoFrameProperty}
    \underset
      { a \gt dim(\Sigma) }
      {\forall}
    \;\;\;\;\;
    \phi^\ast E^a
    \;=\;
    0
  \]
  
  ([Sternberg 1964, (2.11) on p. 246](#Sternberg64); [Zandi 1988, p. 426](#Zandi88); [Mastrolia, Rigoli & Setti 2012, Def. 1.17](#MastroliaRigoliSetti12); [Giron 2020, §3.2.2](#Giron20); [Chen & Giron 2021, §2.4](#ChenGiron21))

\begin{remark}
  \label{DarbouxCoFramePullingBackToCoframeOnImmersedManifold}
  The Darboux co-frame property (eq:DarbouxCoFrameProperty) immediately implies that the pullback of the remaining frame components 
$$
  e
  \;\coloneqq\;
  \big(
    e^a 
    \;\coloneqq\;
    \phi^\ast E^a
  \big)_{
    a \leq dim(\Sigma)  
  }
$$
constitute a local frame on $\Sigma$. We may summarize this by saying that a local Darboux co-frame $E$ gives
\[
  \label{DarbouxCoframePullsBackToCoframe}
  \phi^\ast E^a 
  \;=\;
  \left\{
  \begin{array}{ll}
    e^a & \text{for}\; a \leq dim(\Sigma)
    \\
    0 & \text{for}\; a \geq dim(\Sigma)
    \,.
  \end{array}
  \right.
\]
(cf. [Griffiths & Harris 1979 (1.13)](#GriffithsHarris79)).

Incidentally, we may observe with [GSS24, §2](superembedding+formalism#GSS24) that this situation (eq:DarbouxCoframePullsBackToCoframe) of Darboux co-frames, when lifted/applied to the bosonic coframe components of [[super spacetimes]], has later come to be known as the "embedding condition" in the "[[super-embedding approach]]" to [[super p-branes]] &lbrack;[Sorokin 2000 (4.36-37)](super-embedding+approach#Sorokin00); [Bandos 2011 (2.6-2.9)](super-embedding+approach#Bandos11); [Bandos & Sorokin 2023 (5.13-14)](super-embedding+approach#BandosSorokin23)&rbrack;, strenghtening the original "geometrodynamical condition" of [Bandos et al. 1995 (2.23)](super-embedding+formalism#BPSTV95), which is just the first condition in (eq:DarbouxCoframePullsBackToCoframe).
\end{remark}


\begin{proposition}
\label{ExistenceOfDarbouxFrames}
Given an immersion into a Riemannian manifold, local Darboux (co-)frames always exist. 
\end{proposition}
\begin{proof}
  Given an immersion $\iota \colon \Sigma \to X$, consider any point $\sigma \in \Sigma$. Since the immersion is *locally* an [[embedding of smooth manifolds|embedding]] (see [here](immersion+of+smooth+manifolds#ImmersionsAreLocalEmbeddings)), there exists an [[open neighbourhood]] $ \sigma \in U \subset \Sigma$ such that $\phi_{\vert U} \colon U \to X$ is the [[embedding of smooth manifolds|embedding]] of a [[submanifold]]. Therefore (by [this Prop.](submanifold#ExistenceOfSiceCharts)) there exists an [[open neighbourhood]] $U' \subset X$ of $\iota(\sigma) \in X$ which serves as a [[coordinate chart]] $X \supset U' \xrightarrow{\phi} \mathbb{R}^n$ for $X$ and a slice chart for $\Sigma \subset X$ in that it exhibits $\Sigma \cap U'$ as a rectilinear [[hyperplane]] in $\phi(U') \subset \mathbb{R}^n$.

Hence in this slice [[coordinate chart]] a local frame for $X$ is given by the $n$ canonical coordinate [[vector fields]], with the first $k$ of them forming a local frame field on $\Sigma$

$$
  \big\{ \partial_1, \cdots, \partial_{k} \big\}
  \hookrightarrow
  \big\{ 
    \partial_1, \cdots, \partial_{k}, 
    \,
    \partial_{k+1}, \cdots, \partial_n 
  \big\}
  \,.
$$

From this local frame the [[Gram-Schmidt process]] produces an *orthonormal* frame, first for $\Sigma$ and then extended to $X$:
$$
  \big\{ v_1, \cdots, v_{k} \big\}
  \hookrightarrow
  \big\{ 
    v_1, \cdots, v_{k}, 
    \,
    v_{k+1}, \cdots, v_n 
  \big\}
  \,,
  \;\;\;
  g(v_a, v_b) = \delta_{a b}
  \,
$$
This demonstrates the existence of orthonormal local frame fields (cf. [Kayban 2021, Prop. 3.1](#Kayban21)).

To obtain the desired orthonormal local co-frame field we just dualize this local frame field:

By construction, the matrix $\big(v_a^\mu\big)_{a,\mu}$ of components of the above frame (given by $v_a^\mu \partial_\mu = v_a$) is block diagonal (the upper diagonal block being the local frame on $\Sigma$).

This means (cf. e.g. [here](inverse+matrix#SD23)) that also the [[inverse matrix]] 
$$
  \big(e^a_\mu\big)_{\mu,a}
    \,\coloneqq\, 
  \Big(\big(v_a^\mu\big)_{\mu,a}\Big)^{-1}
$$
is block diagonal, with its upper diagonal block being the inverse matrix of the original upper left block.

This gives the desired [[coframe field]]:
$$
  e^{a} 
    \,\coloneqq\,
  e^a_\mu \, \mathrm{d}x^\mu
$$
which is orthonormal on $X$
$$
  e^a \otimes e_a
  \;=\;
  g(-,-)
$$
because
$$
  v_a^\mu g_{\mu \nu} v_b^\nu
  \;=\;
  \delta_{a b}
  \;\;\;\;
    \Leftrightarrow
  \;\;\;\;
  g_{\mu \nu}
  \;=\;
  e^a_\mu 
  \delta_{a b}
  e^b_\nu
  \,.
$$
and which is Darboux by the block-diagonal structure of $\big(e^a_\mu\big)$. 
\end{proof}

(For the further generality of [[sequences]] of Darboux frames for suitable [[sequences]] of immersions, see [Giron 2020](#Giron20) and [Chen & Giron 2021, Thm. 2.2](#ChenGiron21).)

\begin{remark}
In particular, an immersion $\iota \colon \Sigma \hookrightarrow X$ of Riemannian manifolds is isometric iff around each point $\iota(\sigma)$ any of its Darboux coframe fields pull back to locally induce the given metric on $\Sigma$.
\end{remark}

\linebreak

### Second fundamental form
 {#SecondFundamentalForm}

The "second fundamental form" (on the terminology cf. Rem. \ref{TerminologySecondFundamentalForm} below) of a Riemannian  immersion $\Sigma \xrightarrow{\phantom{-}} X$ measures the transversal change of [[tangent vectors]] to $\Sigma$, under their tangential [[parallel transport|transport]] along $\Sigma$ inside $X$.

We first discuss the second fundamental form in terms of [local Darboux co-frame fields](#AdaptedDarbouxCoframes), where its definition is most immediate, and then extract equivalent expressions in terms of [[covariant derivatives]].

\linebreak

Given $X$ a [[Riemannian manifold]] and $\phi \colon \Sigma \to X$ an [[immersion]], choose a Darboux co-frame field $E \equiv (E^a)_{a =1}^{dim(X)}$ (which exists by Prop. \ref{ExistenceOfDarbouxFrames}), hence so that

$$
  \begin{array}{l}
  \phi^\ast E^a \;=\; 0
  &
  \text{for}
  \;
  a \in \big\{dim(\Sigma)+1, \cdots, dim(X)\big\}
  \\
  \big( 
    e^a \;\coloneqq\; \phi^\ast E^a
  \big)_{a = 1}^{dim(\Sigma)}
  &
  \text{is a co-frame on}\; \Sigma
  \end{array}
$$


For brevity we will say that $a \in \{1, \cdots, dim(X)\}$ is

* *tangential* if $a \in \big\{1, \cdots, dim(\Sigma)\big\}$

* *transversal* if $a \in \big\{dim(\Sigma)+1, \cdots, dim(X)\big\}$.


Now let $\Omega$ be the unique [[torsion of a metric connection|torsion]]-free connection for $E$, in that

\[
  \label{TorsionConstraintOnTarget}
  \mathrm{d} E^a 
  -
  \Omega^a{}_b E^b 
  \;=\;
  0
  \,.
\]


and denote the [[pullback of differential forms|pullback]] of its tangential and transversal components, respectively, by

\[
  \label{SecondFundamentalFormViaCoframeFields}
  \begin{array}{cccl}
    \omega^a{}_b 
      &\coloneqq& 
    \phi^\ast \Omega^a{}_b
    &
    \text{for tangential}\;\text{and tangential}\;b
    \\
    {&#8545;}^a_{b_1 b_2} e^{b_1}
      &\coloneqq& 
    \phi^\ast \Omega^a{}_{b_2}
    &
    \text{for transversal}\;a\;\text{and tangential}\;b_2
    \,.
  \end{array}
\]

Then the [[pullback of differential forms|pullback]] of the torsion constraint (eq:TorsionConstraintOnTarget) is equivalent to the following pair of conditions on $\Sigma$:

$$
  \left\{
  \begin{array}{ll}
    \mathrm{d} e^a - \omega^a{}_b \, e^b \;=\; 0
    &
    \text{for tangential}\;a
    \\
    {&#8545;}^a_{b_1 b_2} e^{b_1} e^{b_2} \;=\; 0
    &
    \text{for transversal}\;a
  \end{array}
  \right.
$$

The first one just says that $\omega$ is the torsion-free connection with respect to the induced coframe $e$ on $\Sigma$.

The second one says that the skew symmetric part ${&#8545;}^a_{[b_1 b_2]} = 0$ vanishes, hence that

\[
  \label{TheSecondFundamentalForm}
  {&#8545;}^a_{b_1 b_2}
  \;=\;
  {&#8545;}^a_{b_2 b_1}
\]

is symmetric in its tangential indices $b_i$. This symmetric [[tensor]] on $\Sigma$ is called the **second fundamental form** of the immersion $\phi$.

(e.g. [Willmore 1996, p. 125-126](#Willmore96), [Berger, Bryant & Griffiths 1983, p. 819](#BergerBryantGriffiths83); [Chavel 1993 (II.2.12)](#Chavel93); [Wang 2024, Def. 2.2](#Wang24))


\begin{remark}\label{TerminologySecondFundamentalForm}
**(terminology)**
Historically, by the "first fundamental form" authors used to refer to the pullback of the [[metric tensor]] along an immersion. While this usage is no longer practiced, the term "second fundamental form" for (eq:TheSecondFundamentalForm) has become standard.
\end{remark}
(cf. [Chavel 1993, Rem. II..1](#Chavel93); [Lee 2018, pp. 227](Riemannian+geometry#Lee18))


{#SecondFundamentalFormViaCovDerOfVectorFields} In much of the literature the second fundamental form is alternatively  expressed instead in terms of [[covariant derivatives]] of and along tangential [[vector fields]] (e.g.: [Chavel 1993 §II.2](#Chavel93); [Baird & Wood 2003, §3.2](#BairdWood03); [Lee 2018, pp. 225](Riemannian+geometry#Lee18)), via the following proposition

> (which is well-known but seems hard to cite explicitly, cf. maybe [Willmore 1996, p. 126](#Willmore96)):

\begin{proposition}
  \label{FromCoframeVersionOfScndFundFormToCoDevVersion}
  The second fundamental form obtained from a local Darboux coframe field as in (eq:SecondFundamentalFormViaCoframeFields),
when regarded as a [[tensor]], namely as a morphism of [[vector bundles]] from the [[tensor product of vector bundles|tensor product]] of the [[tangent bundle]] of $\Sigma$ to the [[normal bundle]] of $X$ relative to $\phi$
  $$
    {&#8545;} \;\colon\;
    T\Sigma \otimes T \Sigma 
      \xrightarrow{\;}
    N_\phi X
    \,,
  $$
  is given by [[covariant derivatives]] of [[vector fields]] as follows:

\[
  \label{SecondFundamentalFormAsDifferenceOfCovariantDerivatives}
  {&#8545;}(v,w) 
    \;=\;
  \nabla^X_{v} \, \mathrm{d}\phi(w) 
  \;-\;
  \mathrm{d}\phi\big( \nabla^\Sigma_v \, w \big) 
  \,.
\]
\end{proposition}
\begin{proof}
  Let $(v_a)_{a = 1}^{dim X}$ be a local Darboux *frame* of $X$, so that $(v_a)_{a =1}^{dim \Sigma}$ is a local frame on $\Sigma$ (called the *tangential* frame vectors, the others being the *transversal* ones).

It follows that pushforward of vector field in this Darboux basis is just the canonical injection

\[
  \label{PushforwardOfDarbouxFrame}
  \begin{array}{rcc}
    \mathrm{d}\phi_\sigma 
      \;\colon\; 
    T_\sigma \Sigma
    &\xrightarrow{\phantom{--}}&
    T_{\phi(\sigma)} X
    \\
    v_a(\sigma) &\mapsto& v_a(\sigma)
  \end{array}
\]

(shown for any $\sigma \in \Sigma$ inside the given chart).

Remembering that for tangential $b_1, b_2$ we set
\begin{equation}
  \label{PullbackOfConnection}
  \phi^\ast \Omega_{b_1}{}^a{}_{b_2}
  \;\equiv\;
  \left\{
  \begin{array}{ll}
    \omega_{b_1}{}^a{}_{b_2} & \text{tangential}\; a
    \\   
    {&#8545;}^a_{b_1 b_2} & \text{transversal}\; a
  \end{array}
  \right.
\end{equation}

this makes it immediate that

\[
  \label{ComputingScndFundFormViaCovDerivatives}
  \begin{array}{l}
    \nabla^X_{b_1} \mathrm{d}\phi(v_{b_2})
    -
    \mathrm{d}\phi\big( \nabla^\Sigma_{b_1} v_{b_2} \big)
    \\
    \;=\;
    \nabla^X_{b_1} v_{b_2} 
    -
    \nabla^\Sigma_{b_1} v_{b_2}
    \\
    \;=\;
    \phi^\ast \Omega_{b_1}{}^{a}{}_{b_2} v_a
    -
    \omega_{b_1}{}^a{}_{b_2} v_a
    \\
    \;=\;
    \text{II}^a_{b_1 b_2} v_a
    \mathrlap{\,.}
  \end{array}
\]
In words, the computation (eq:ComputingScndFundFormViaCovDerivatives) shows that the covariant derivative on $X$ of and along tangent vectors to $\Sigma$ is that on $\Sigma$ plus the contribution of the second fundamental form, hence their difference extracts the latter. 
\end{proof}

\begin{remark}
**(further alternative expressions)**
\linebreak
As the proof (eq:ComputingScndFundFormViaCovDerivatives) of Prop. \ref{FromCoframeVersionOfScndFundFormToCoDevVersion} shows, the second fundamental form extracts the normal component of the ambient covariant derivative of and along tangential vectors:
$$
  \text{II}(v,w) 
  \;=\;
  (\nabla^X_v w)^\perp
  \,.
$$
In this form it appears for instance in [Kobayashi & Nomizu 1963 §VII.3](#KobayashiNomizu63), [Chavel 1993 (II.2.2)](#Chavel93), the relation to (eq:SecondFundamentalFormAsDifferenceOfCovariantDerivatives) is made explicit by [Baird & Wood 2003 Def. 3.2.3](#BairdWood03), cf also [Willmore 1996, p. 126](#Willmore96). 



Alternatively, the [[pushforward of vector fields]] $\mathrm{d}\phi$ may be understood as a [[section]] of the [[tensor product of vector bundles|tensor product]] [[vector bundle]]
$$
  \mathrm{d}\phi
  \;\in\;
  \Gamma\big(
    T\Sigma^\ast \otimes \phi^\ast T X
  \big)
  \,,
$$
whence the expression (eq:SecondFundamentalFormAsDifferenceOfCovariantDerivatives) may be understood as the induced [[covariant derivative]] on that tensor bundle
$$ 
  (\nabla \mathrm{d}\phi)(v,w)
  \;\coloneqq\;
  \nabla^X_{v} \mathrm{d}\phi(w) 
  \;-\;
  \mathrm{d}\phi\big( \nabla^\Sigma_v w \big) 
  \,.
$$
In this sense the second fundamental form is simply expressed as
$$
  {&#8545;}
  \;=\;
  \nabla \mathrm{d}\phi
  \,.
$$
This is how it appears in [Eells & Sampson 1964 p. 123](#EellsSampson64), [Baird & Wood 2003 (3.2.1)](#BairdWood03).

Finally, one may write out the covariant derivatives in a [[coordinate chart]] in terms of the [[Christoffel symbols]] $L_{l}{}^m{}_n$ for the [[Levi-Civita connection]] on $X$, and those $\Gamma_i{}^l{}_j$ of the pullback connection to $\Sigma$:

\[
  \label{SecondFundamentalFormInCoordinates}
  \begin{array}{l}
    {&#8545;}^k_{i j}
    \\
    \;=\;
    \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
    \nabla^X_{\partial_i}
    \mathrm{d}\phi(
      \partial_j
    )
    \;\;\;\;\;\;\;\;\;\;\;\;
    -
    \mathrm{d}\phi\big(
      \nabla^\Sigma_{\partial_i} \partial_j
    \big)
    \\
    \;=\;
    \overbrace{
      \partial_i 
      \partial_j \phi^l
      +
      L_{m}{}^l{}_n 
      (\partial_i \phi^m) (\partial_j \phi^n)
    }
    -
    \overbrace{
       \Gamma_{i}{}^k{}_j \partial_k \phi^l
    }
    \\
    \;=\;
    \partial_i 
    \partial_j \phi^l
    -
    \Gamma_{i}{}^k{}_j \partial_k \phi^l
    +
    L_{m}{}^l{}_n 
    (\partial_i \phi^m) (\partial_j \phi^n)
    \,.
  \end{array}
\]
In this guise the second fundamental form was originally given in [Eells & Sampson 1964 (p. 118 & 123 with p. 111)](#EellsSampson64) following [Eisenhart 1925, §43](#Eisenhart25), reviewed by [Baird & Wood 2003 (3.2.2)](#BairdWood03).
\end{remark}

\begin{remark}
If the fundamental form &#8545; of a Riemannian immersion $\phi \colon, \Sigma \to X$ vanishes, then [[geodesics]] in $\Sigma$ are taken by $\phi$ to geodesics in $X$, hence such $\phi$ is said to be *totally geodesic* &lbrack;[Eells & Sampson 1964 p. 126](#EellsSampson64), [Baird & Wood 2003 Def. 3.2.1](#BairdWood03)&rbrack;.
\end{remark}

\linebreak

### Tension field

\begin{definition}
\label{TensionField}
The *tension field* of the immersion $\phi$ is the contraction (trace) of the [second fundamental form](#SecondFundamentalForm):

$$
  \tau^k
  \;\coloneqq\;
  \eta^{a b} \, {&#8545;}^k_{a b}
    \;=\;
  g^{i j} \, {&#8545;}^k_{i j}
  \,.
$$
From (eq:SecondFundamentalFormInCoordinates) we have immediately the coordinate expression
  $$
    \begin{array}{l}
      \tai^k
      \;=\;
      \eta^{a b} \, {&#8545;}^k_{a b}
      \;=\;
      g^{i j} \, {&#8545;}^k_{i j}
      \\
      \;=\;
      \underset
      {\Delta \phi^l}
      {
        \underbrace{
          g^{i j}
          \big(
            \partial_i 
            \partial_j \phi^l
            -
            \Gamma_{i}{}^k{}_j \partial_k \phi^l
          \big)
        }
      }
        +
      g^{i j}
      (\partial_i \phi^m) (\partial_j \phi^n)    
      L_{m}{}^l{}_n 
      \,,
    \end{array}
  $$ 
  where "$\Delta$" denotes the [[Laplace operator]] on $\Sigma$.
\end{definition}
([Eells & Sampson 1964 (5)](#EellsSampson64), [Baird & Wood 2003 Def. 3.2.4](#BairdWood03))

\linebreak

### Harmonic immersions
  {#HarmonicImmersion}

\begin{theorem}\label{HarmonicEquation}
**(harmonic equation)**
\linebreak
The vanishing of the tension field $\tau$ (Def. \ref{TensionField}) characterizes Riemannian immersion which are [[harmonic maps]].
\end{theorem}
([Eells & Sampson 1964 pp. 116](#EellsSampson64), [Baird & Wood 2003 Thm. 3.3.3](#BairdWood03))


\linebreak


## Literature
 {#Literature}


* {#Eisenhart25} [[Luther P. Eisenhart]], Chapter IV of: *Riemannian Geometry*, Princeton University Press (1925, 1950) &lbrack;[ISBN:9780691023533](https://press.princeton.edu/books/paperback/9780691023533/riemannian-geometry), [ark:/13960/t47q47r0k](https://archive.org/details/in.ernet.dli.2015.524829), [pdf](http://www.uop.edu.pk/ocontents/Eisenhart-RiemannianGeometry.pdf)&rbrack;

* {#Cartan26} [[Élie Cartan]] (translated by Vladislav Goldberg from Cartan's lectures at the Sorbonne in 1926–27): Part E of: *Riemannian Geometry in an Orthogonal Frame*, World Scientific (2001) &lbrack;[doi:10.1142/4808](https://doi.org/10.1142/4808), [pdf](https://softbank.iust.ac.ir/MathBooks/c/Cartan%20-%20Riemannian%20Geometry%20in%20an%20Orthogonal%20Frame.pdf)&rbrack;


* {#KobayashiNomizu63} [[Shoshichi Kobayashi]], [[Katsumi Nomizu]], Chapter VII in: _Foundations of differential geometry_, Volume 1 (1963), Volume 2 (1969) Interscience Publishers, reprint: Wiley Classics Library (1996) &lbrack;[ISBN:978-0-470-55558-3](https://www.wiley.com/en-us/Foundations+of+Differential+Geometry%2C+2+Volume+Set-p-9780470555583), [Wikipedia entry](https://en.wikipedia.org/wiki/Foundations_of_Differential_Geometry)&rbrack; 


* {#Sternberg64} [[Shlomo Sternberg]], _Lectures on differential geometry_, Prentice-Hall (1964), AMS (1983) &lbrack;ISBN:978-0-8218-1385-0, [ams:chel-316](https://bookstore.ams.org/chel-316), [ark:/13960/t1pg9dv6k](https://archive.org/details/lecturesondiffer0000ster)&rbrack;

* {#EellsSampson64} [[James Eells]], [[Joseph H. Sampson]], *Harmonic Mappings of Riemannian Manifolds*, American Journal of Mathematics **86** 1 (1964) 109-160 &lbrack;[doi:10.2307/2373037](https://doi.org/10.2307/2373037), [jstor:2373037](https://www.jstor.org/stable/2373037)&rbrack;



* {#Guggenheimer77} [[Heinrich W. Guggenheimer]], *Differential Geometry*, Dover (1977) &lbrack;[isbn:9780486634333](https://store.doverpublications.com/products/9780486634333), [ark:/13960/t9t22sk9n](https://archive.org/details/differentialgeom0000gugg/)&rbrack;


* {#GriffithsHarris79} [[Phillip Griffiths]], [[Joseph Harris]], *Algebraic geometry and local differential geometry*, Annales scientifiques de l'École Normale Supérieure, Serie 4, Volume 12 no. 3 (1979) 355-452 &lbrack;[numdam:ASENS_1979_4_12_3_355_0](http://www.numdam.org/item/?id=ASENS_1979_4_12_3_355_0)&rbrack;

* {#BergerBryantGriffiths83} [[Eric Berger]], [[Robert Bryant]], [[Phillip Griffiths]], *The Gauss equations and rigidity of isometric embeddings*, Duke Math. J. **50** 3 (1983) 803-892 &lbrack;[doi:10.1215/S0012-7094-83-05039-1](http://dx.doi.org/10.1215/S0012-7094-83-05039-1)&rbrack;

* {#Zandi88} Ahmad Zandi, *Minimal immersions of surfaces in quaternionic projective space*, Tsukuba Journal of Mathematics **12** 2 (1988) 423-440 &lbrack;[jstor:43686661](https://www.jstor.org/stable/43686661)&rbrack;

* {#Yang92} Kichoon Yang, *Embeddings of $G$-Structures*, chapter VII in: *Exterior Differential Systems and Equivalence Problems*, Mathematics and its Applications **73**, Kluwer (1992), Spinger (1992) &lbrack;[doi:10.1007/978-94-015-8068-7_7](https://doi.org/10.1007/978-94-015-8068-7_7)&rbrack;

* {#Chavel93} [[Isaac Chavel]], *Riemannian Submanifolds*, §II.2 in: *Riemannian geometry -- A modern introduction*, Cambridge University Press (1993) &lbrack;[doi:10.1017/CBO9780511616822](https://doi.org/10.1017/CBO9780511616822)&rbrack;

* {#Willmore96} [[Thomas J. Willmore]], Chapter 4 in: *Riemannian Geometry*, Oxford University Press (1996) &lbrack;[ISBN:9780198514923](https://global.oup.com/academic/product/riemannian-geometry-9780198514923?cc=de&lang=en&), [ark:/13960/t4jn0093w](https://archive.org/details/riemanniangeomet0000will)&rbrack;


* {#BairdWood03} [[Paul Baird]], [[John C. Wood]]: *Harmonic Morphisms Between Riemannian Manifolds*, Oxford University Press (2003) &lbrack;[doi:10.1093/acprof:oso/9780198503620.001.0001](https://doi.org/10.1093/acprof:oso/9780198503620.001.0001)&rbrack;



* {#HanHong06} Qing Han, Jia-Xing Hong: *Isometric Embedding of Riemannian Manifolds in Euclidean Spaces*, Mathematical Surveys and Monographs **130**, AMS (2006) &lbrack;[ISBN:0821840711](https://maa.org/press/maa-reviews/isometric-embedding-of-riemannian-manifolds-in-euclidean-spaces)&rbrack;


* {#MastroliaRigoliSetti12} Paolo Mastrolia, Marco Rigoli, Alberto G. Setti, §1.3 *Some formulas for immersed submanifolds* in: *Yamabe-type Equations on Complete, Noncompact Manifolds*, Birkhäuser (2012) &lbrack;[doi:10.1007/978-3-0348-0376-2](https://doi.org/10.1007/978-3-0348-0376-2)&rbrack;

* {#Giron20} Tristan Pierre Giron, *On the Analysis of Isometric Immersions of Riemannian Manifolds*, PhD thesis (2020) &lbrack;[uuid:cae2f41d-c5a1-4138-9dec-5e824d21044e](https://ora.ox.ac.uk/objects/uuid:cae2f41d-c5a1-4138-9dec-5e824d21044e), [pdf](https://ora.ox.ac.uk/objects/uuid:cae2f41d-c5a1-4138-9dec-5e824d21044e/download_file?safe_filename=ThesisGironTristan.pdf&type_of_work=Thesis)&rbrack;

* {#ChenGiron21} Gui-Qiang G. Chen, Tristan P. Giron, *Weak continuity of curvature for connections in $L^p$* &lbrack;[arXiv:2108.13529](https://arxiv.org/abs/2108.13529)&rbrack;

* {#Kayban21} Nicholas Kayban, *Riemannian Immersions and Submersions* (2021) &lbrack;[pdf](https://www.math.uwaterloo.ca/~karigian/training/M11-kayban-final-project.pdf), [[Kayban-RiemannianImmersions.pdf:file]]&rbrack;

* {#HanLewicka23} Qing Han, Marta Lewicka, *Isometric immersions and applications*, Notices of the AMS 2023 &lbrack;[arXiv:2310.02566](https://arxiv.org/abs/2310.02566)&rbrack;

* {#Wang24} [[Zuoqin Wang]], *The method of moving frames*, Lecture 11 in: *Riemannian geometry* (2024) &lbrack;[webpage](http://staff.ustc.edu.cn/~wangzuoq/Courses/24S-RiemGeom/), [pdf](http://staff.ustc.edu.cn/~wangzuoq/Courses/24S-RiemGeom/Notes/Lec11.pdf), [[Wang-MovingFrames.pdf:file]]&rbrack;


\linebreak


[[!redirects Riemannian immersions]]

[[!redirects isometric immersion]]
[[!redirects isometric immersions]]

[[!redirects isometric embedding]]
[[!redirects isometric embeddings]]

[[!redirects Darboux frame]]
[[!redirects Darboux frames]]

[[!redirects Darboux coframe]]
[[!redirects Darboux coframes]]

[[!redirects second fundamental form]]
[[!redirects second fundamental forms]]

[[!redirects tension field]]
[[!redirects tension fields]]



