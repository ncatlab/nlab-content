

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Algbraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _causal propagator_ or _Pauli-Jordan distribution_ ([Jordan-Pauli 27](#JordanPauli27)) or _commutator function_ is a [[distribution]] which gives the [[integral kernel]] for the [[Poisson bracket]] on the [[covariant phase space]] of a [[free field|free]] [[local field theory]] (also known as the _[[Peierls bracket]]_).

Specifcally for the [[free field|free]] [[scalar field]] on a [[spacetime]] $\Sigma$, its [[phase space]] is the space $ker(\Box + m^2) \hookrightarrow C^\infty(\Sigma)$ of solutions of the [[Klein-Gordon equation]] (the [[wave equation]] for vanishing [[mass]] $m$). For any  point $x \in \Sigma$ we denote by $\phi(x) \colon ker(\Box + m^2) \to \mathbb{R}$ the point [[evaluation]] [[functional]] which sends $\Phi \in C^\infty(\Sigma)$ to $\Phi(x)$. An [[observable]] of the scalar field is then a [[functional]] of the form $\phi(b) \coloneqq \int b(x) \phi(x) dvol(x)$, for $b$ a [[bump function]] on $\Sigma$. On the algebra of these observables there is a canonical [[Poisson bracket]] pairing defined (also known as the _[[Peierls bracket]]_ see at _[[scalar field]]_ for details), taking $\phi(b_1)$ and $\phi(b_2)$ to a new observable denoted $\{\phi(b_1), \phi(b_2)\}$. While a priori this Poisson bracket is defined only on the "smeared" observables $\phi(b)$, not on the point observables $\phi(x)$, nevertheless it has a [[distributional density|distributional]] [[integral kernel]] $\{\phi(x), \phi(y)\}$ such that

$$
  \{ \phi(b_1), \phi(b_2) \}
  = 
  \int b_1(x) b_2(y) \{\phi(x), \phi(y)\} dvol_{\Sigma}(x) dvol_\Sigma(y)
  \,.
$$

This [[distribution|distributional]] [[integral kernel]] 

$$
  \Delta(x,y) \coloneqq \{\phi(x), \phi(y)\}
$$ 

is the _causal propagator_ or _Pauli-Jordan distribution_ (also "commutator function", see [this prop.](scalar+field#IntegralKernelForPoissonBracketOfFreeScalarFieldOnMinkowskiSpacetime)). This happens to be a [[fundamental solution]]/[[Green function]] to the [[Klein-Gordon operator]] $\Box + m^2$, whence a "[[propagator]]".

For other [[free fields|free]] [[field (physics)|fields]] the [[integral kernel]] of their [[Poisson bracket]] is a more complicated expression, but it is typically still an expression in terms of the causal propagator of the scalar field.

What is _causal_ about the causal propagator is that (on [[globally hyperbolic spacetimes]] such as [[Minkowski spacetime]]) its [[support of a distribution|support as a distribution]], is, for one of the two arguments fixed, the [[causal cone]] of that point (cor. \ref{CausalSupportOfTheCausalPropagatorOnMinkowskiSpacetime} below). Moreover, the causal propagator splits, as a distribution, as a sum

$$
  \Delta = \Delta_R - \Delta_A
$$

where the [[retarded propagator]] $\Delta_R$ and the [[advanced propagator]] $\Delta_A$ are such that their [[support of a distribution|support]] is, for fixed second argument, in the [[past causal cone]] and in the [[future causal cone]], respectively.


## Definition

+-- {: .num_defn #CompactlySourceCausalSupport}
###### Definition
**(compactly sourced causal support)

Given a [[vector bundle]] $E \overset{}{\to} \Sigma$ over a manifold $\Sigma$ with [[conal causal structure|causal structure]]

Write $\Gamma_{\Sigma}(-)$ for [[space of sections|spaces of smooth sections]], and write

$$
  \array{
    \Gamma_{cp}(-) & \text{compact support}
    \\
    \Gamma_{\Sigma,\pm cp}(-) & \text{compactly sourced future/past support}
    \\
    \Gamma_{\Sigma,scp}(-) & \text{spacelike compact support}
    \\
    \Gamma_{\Sigma,(f/p)cp}(-) & \text{future/past compact support}
    \\
    \Gamma_{\Sigma,tcp}(-) & \text{timelike compact support}
  }
$$

for the [[linear subspaces]] on those smooth sections whose [[support]] is

1. ($cp$) inside a [[compact subset]]

1. ($\pm cp$) inside the [[closed future cone]]/[[closed past cone]], respectively, of a [[compact subset]],

1. ($scp$) inside the [[closed causal cone]] of a [[compact subset]], which equivalently means that the [[intersection]] with every ([[spacelike]]) [[Cauchy surface]] is compact ([Sanders 13, theorem 2.2](#Sanders12)),

1. ($fcp$) inside the past of a Cauchy surface ([Sanders 13, def. 3.2](#Sanders12)),

1. ($pcp$) inside the future of a Cauchy surface ([Sanders 13, def. 3.2](#Sanders12)),

1. ($tcp$) inside the future of one Cauchy surface and the past of another ([Sanders 13, def. 3.2](#Sanders12))

=--

([B&#228;r 14, section 1](#Baer14), [Khavkine 14, def. 2.1](#Khavkine14))


+-- {: .num_defn #AdvancedAndRetardedGreenFunctions}
###### Definition
**([[advanced and retarded Green functions]], [[causal Green function]] and [[propagators]])**

Let $\Sigma$ be a [[smooth manifold]] with [[causal structure]], let $E \to \Sigma$ be a [[smooth vector bundle]] and let
$P \;\colon\;\Gamma_\Sigma(E) \to \Gamma_\Sigma(\tilde E^\ast)$ be a [[differential operator]] on its [[space of smooth sections]].

Then a [[linear map]]

$$
  \mathrm{G}_{P,\pm}
    \;\colon\;
  \Gamma_{\Sigma, cp}(\tilde E^\ast)
    \longrightarrow
  \Gamma_{\Sigma, \pm cp}(E)
$$

from spaces of sections of [[compact support]] to spaces of sections of causally sourced future/past support (def. \ref{CompactlySourceCausalSupport}) is called an _[[advanced or retarded Green function]]_ for $P$, respectively, if

1. for all $\Phi \in \Gamma_{\Sigma,cp}(E_1)$ we have

   $$
     \label{AdvancedRetardedGreenFunctionIsLeftInverseToDiffOperator}
     G_{P,\pm} \circ P(\Phi) = \Phi
   $$

   and

   $$
     \label{AdvancedRetardedGreenFunctionIsRightInverseToDiffOperator}
     P \circ G_{P,\pm}(\Phi) = \Phi
   $$

1. the [[support]] of $G_{P.\pm}(\Phi)$ is in the [[closed future cone]] or [[closed past cone]] of the support of $\Phi$, respectively.

If the advanced/retarded Green functions $G_{P\pm}$ exists, then the difference

$$
  \mathrm{G}_P \coloneqq \mathrm{G}_{P,+} - \mathrm{G}_{P,-}
$$

is called the _[[causal Green function]]_.

If there are [[integral kernel]], hence [[distributions in two variables]]

$$
  \Delta_{P,\pm} \in \Gamma'\Sigma( \tilde E^\ast \boxtimes_\Sigma E )
$$

such that these Green functions are given by the corresponding [[integral transform]], in that
(in [[generalized function]]-notation)

$$
  (G_{P,\pm} \Phi)(x)
   \;=\;
  \underset{y \in \Sigma}{\int}
   \Delta_{P, \pm}(x,y) \cdot \Phi(y)
$$

then these integral kernels are called the advanced/retarded _[[propagators]]_; similarly then their difference

$$
  \Delta_P \coloneqq \Delta_{P,+} - \Delta_{p,-}
$$

is the corresponding _[[causal propagator]]_.

=--

(e.g. [B&#228;r 14, def. 3.2, cor. 3.10](#Baer14}))


## Properties

### Existence and uniqueness

+-- {: .num_prop #AdvancedAndRetardedGreenFunctionsForGreenHyperbolicOperatorAreUnique}
###### Proposition
**([[advanced and retarded Green functions]] of [[Green hyperbolic differential operator]] are unique)**

The [[advanced and retarded Green functions]] (def. \ref{AdvancedAndRetardedGreenFunctionsForGreenHyperbolicOperatorAreUnique}) of a [[Green hyperbolic differential operator]] are unique.

=--

([B&#228;r 14, cor. 3.12](#Baer14})

### Continuity
 {#Continuity}

+-- {: .num_defn #TVSStructureOnSpacesOfSmoothSections}
###### Definition
**([[Fréchet space|Fréchet]] [[topological vector space]] on [[spaces of smooth sections]] of a [[smooth vector bundle]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[smooth vector bundle]]. On its [[real vector space]] $\Gamma_\Sigma(E)$ [[space of sections|of smooth sections]] consider the [[seminorms]] indexed by a [[compact subset]] $K \subset \Sigma$ and a [[natural number]] $N \in \mathbb{N}$ and given by

$$
  \array{
    \Gamma_\Sigma(E) &\overset{p_K^N}{\longrightarrow}&
    [0,\infty)
    \\
    \Phi &\mapsto&  \underset{n \leq N}{max} \left( \underset{x \in K}{sup} {\vert \nabla^n \Phi(x)\vert}\right) \,,
  }
$$

where on the right we have the [[absolute values]] of the [[covariant derivatives]] of $\Phi$ for any fixed choice of [[connection on a bundle|connection]] on $E$ and [[norm]] on the [[tensor product of vector bundles]] $(T^\ast \Sigma)^{\otimes_\Sigma^n} \otimes_\Sigma E $.

This makes $\Gamma_\Sigma(E)$ a [[Fréchet space|Fréchet]] [[topological vector space]].

For $K \subset \Sigma$ any [[closed subset]] then the sub-space of sections

$$
  \Gamma_{\Sigma,K}(E) \hookrightarrow \Gamma_\Sigma(E)
$$

of sections whose [[support]] is inside $K$ becomes a [[Fréchet space|Fréchet]] [[topological vector spaces]] with the induced [[subspace topology]], which makes these be [[closed subspaces]].

=--

([B&#228;r 14, 2.1, 2.2](#Baer14))



+-- {: .num_defn #DistributionalSections}
###### Definition
**([[distribution|distributional]] [[sections]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[smooth vector bundle]] over a [[smooth manifold]] with [[causal structure]].

The [[vector space|vector]] [[spaces of smooth sections]] with restricted support from def. \ref{CompactlySourceCausalSupport} structures of [[topological vector spaces]] via def. \ref{TVSStructureOnSpacesOfSmoothSections}. We denote the topological [[dual spaces]] by

$$
  \Gamma'_{\Sigma}(\tilde{E}^*) \coloneqq (\Gamma_{\Sigma,cp}(E))^*
$$

etc.

This is the space of _distributional sections_ of the bundle $\tilde{E}^*$.

With this notations, smooth compactly supported sections of the same bundle, regarded as the [[non-singular distributions]], constitute a [[dense subset]]

$$
  \Gamma_{\Sigma,cp}(\tilde{E}^*)
    \underset{\text{dense}}{\hookrightarrow}
  \Gamma'_{\Sigma}(\tilde{E}^*)
  \,.
$$

Imposing the same restrictions to the [[supports of distributions]] as in def. \ref{CompactlySourceCausalSupport}, we have the following subspaces of distributional sections:

$$
  \Gamma'_{\Sigma,cp}(\tilde E^\ast) ,
  \Gamma'_{\Sigma,\pm cp}(\tilde E^\ast) ,
  \Gamma'_{\Sigma,scp}(\tilde E^\ast) ,
  \Gamma'_{\Sigma,fcp}(\tilde E^\ast) ,
  \Gamma'_{\Sigma,pcp}(\tilde E^\ast) ,
  \Gamma'_{\Sigma,tcp}(\tilde E^\ast)
  \subset
  \Gamma'_{\Sigma}(\tilde E^\ast) .
$$


=--

([Sanders 13](#Sanders12), [B&#228;r 14](#Baer14))

+-- {: .num_prop #GreenFunctionsAreContinuous}
###### Proposition
**([[causal Green functions]] of [[Green hyperbolic differential operators]] are [[continuous linear maps]])**


Given a [[Green hyperbolic differential operator]] $P$ (def. \ref{GreenHyperbolicDifferentialOperator}), the advanced, retarded and causal Green functions of $P$ (def. \ref{AdvancedAndRetardedGreenFunctions}) are [[continuous linear maps]] with respect to the [[topological vector space]] structure from def. \ref{TVSStructureOnSpacesOfSmoothSections} and also have a unique continuous extension to the spaces of sections with .larger support (def. \ref{CompactlySourceCausalSupport}) as follows:

$$
\begin{aligned}
  \mathrm{G}_{P,+}
    &\;\colon\;
  \Gamma_{\Sigma, pcp}(\tilde E^\ast)
    \longrightarrow
  \Gamma_{\Sigma, pcp}(E) ,
  \\
  \mathrm{G}_{P,-}
    &\;\colon\;
  \Gamma_{\Sigma, fcp}(\tilde E^\ast)
    \longrightarrow
  \Gamma_{\Sigma, fcp}(E) ,
  \\
  \mathrm{G}_{P}
    &\;\colon\;
  \Gamma_{\Sigma, tcp}(\tilde E^\ast)
    \longrightarrow
  \Gamma_{\Sigma}(E) ,
\end{aligned}
$$

such that we still have the relation

$$
  \mathrm{G}_P = \mathrm{G}_{P,+} - \mathrm{G}_{P,-}
$$

and

$$
  P \circ \mathrm{G}_{P,\pm} = \mathrm{G}_{P,\pm} \circ P = id
$$

and

$$
  supp \mathrm{G}_{P,\pm}(\tilde{\alpha}^*) \subseteq J^\pm(supp \tilde{\alpha}^*)
  \,.
$$

=--

([B&#228;r 14, thm. 3.8, cor. 3.11](#Baer14))


## Examples

### On Minkowski spacetime
 {#On}

On [[Minkowski spacetime]] $\mathbb{R}^{p,1}$ consider the [[Klein-Gordon operator]]

$$
  \eta^{\mu \nu} \frac{\partial}{\partial x^\mu} \frac{\partial}{\partial x^\nu} \Phi -  \left( \tfrac{m c}{\hbar} \right)^2 \Phi \;=\; 0 \,.
$$


+-- {: .num_prop #AdvancedRetardedPropafatorsForKleinGordonOnMinkowskiSpacetime}
###### Proposition
**(mode expansion of [[advanced and retarded propagators]] for [[Klein-Gordon operator]] on [[Minkowski spacetime]])**

The [[advanced and retarded Green functions]] $G_\pm$ of the [[Klein-Gordon operator]] on [[Minkowski spacetime]] are given by [[integral kernels]] ("[[propagators]]")

$$
  \Delta_\pm \in \mathcal{D}'(\mathbb{R}^{p,1}\times \mathbb{R}^{p,1})
$$

by (in [[generalized function]]-notation)

$$
  G_\pm(\Phi)
    \;=\;
  \underset{\mathbb{R}^{p,1}}{\int}
    \Delta_{\pm}(x,y) \Phi(y) \, dvol(y)
$$

where $\Delta_{\pm}(x,y)$ have the following equivalent expressions:

$$
  \label{ModeExpansionForMinkowskiAdvancedRetardedPropagator}
  \begin{aligned}
    \Delta_\pm(x-y)
     & =
     \frac{1}{(2\pi)^{p+1}}
     \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
     \int \int
     \frac{
       e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
     }{
       (k_0 \mp i\epsilon)^2 - {\vert \vec k\vert}^2  -\left( \tfrac{m c}{\hbar}\right)^2
     }
     \, d k_0 \, d^p \vec k
     \\
     & =
     \left\{
       \array{
          \frac{\pm i}{(2\pi)^{p}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{+i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)(x^0 - y^0)/c  + i \vec k \cdot (\vec x - \vec  y) }
            \right)
          d^p \vec k
          & \vert & \text{if} \,  \pm (x^0 - y^0) \gt 0
          \\
          0 & \vert & \text{otherwise}
       }
     \right.
  \end{aligned}
$$

=--

+-- {: .proof}
###### Proof

The [[Klein-Gordon operator]] is a [[Green hyperbolic differential operator]] ([this example](Green+hyperbolic+partial+differential+equation#GreenHyperbolicKleinGordonOperator)) therefore its advanced and retarded Green functions exist uniquely (prop. \ref{AdvancedAndRetardedGreenFunctionsForGreenHyperbolicOperatorAreUnique}).
and prop. \ref{GreenFunctionsAreContinuous} says that they are [[continuous linear functionals]] with respect to the [[topological vector space]] [[structures]] on [[spaces of smooth sections]] (def. \ref{TVSStructureOnSpacesOfSmoothSections}). In the case of the [[Klein-Gordon operator]] this just means that

$$
  G_{\pm}
    \;\colon\;
  C^\infty_{cp}(\mathbb{R}^{p,1})
    \longrightarrow
  C^\infty_{\pm cp}(\mathbb{R}^{p,1})
$$

are [[continuous linear functionals]] in the standard sense of [[distributions]]. Therefore the
[[Schwartz kernel theorem]]  implies the existence of [[integral kernels]] being [[distributions in two variables]]

$$
  \Delta_{\pm} \in \mathcal{D}(\mathbb{R}^{p,1} \times \mathbb{R}^{p,1})
$$

such that, in the notation of [[generalized functions]],

$$
  (G_\pm \alpha)(x)
  \;=\;
  \underset{\mathbb{R}^{p,1}}{\int} \Delta_{\pm}(x,y) \alpha(y) \, dvol(y)
  \,.
$$

These integral kernels are the advanced/retarded "[[propagators]]".

Since the [[Klein-Gordon operator]] is invariant under [[translations]] in $\mathbb{R}^{p,1}$ it is clear that the propagators, as a [[distribution in two variables]], depend only on the difference of its two arguments

$$
  \Delta_{\pm}(x,y) = \Delta_{\pm}(x-y)
  \,.
$$

Since moreover the [[Klein-Gordon operator]] is [[formally adjoint differential operator|formally self-adjoint]] ([this prop.](Klein-Gordon+equation#FormallySelfAdjointKleinGordonOperator)) this implies that for $P$ the Klein the equation (eq:AdvancedRetardedGreenFunctionIsRightInverseToDiffOperator)

$$
  P \circ G_\pm  = id
$$

is equivalent to the equation (eq:AdvancedRetardedGreenFunctionIsLeftInverseToDiffOperator)

$$
  G_\pm \circ P = id
  \,.
$$

Therefore it is sufficient to solve for the first of these two equation, subject to
the defining support conditions. In terms of the [[propagator]] [[integral kernels]] this means that we have to solve the [[distribution|distributional]] equation

$$
  \label{KleinGordonEquationOnAdvacedRetardedPropagator}
  \left(
    \eta^{\mu \nu}
    \frac{\partial}{\partial x^\mu}
    \frac{\partial}{\partial x^\nu}
     -
     \left( \tfrac{m c}{\hbar} \right)^2
  \right)
  \Delta_\pm(x-y)
  \;=\;
  \delta(x-y)
$$

subject to the condition that the [[support of a distribution|distributional support]] is

$$
  supp\left( \Delta_{\pm}(x-y) \right)
  \subset
  \left\{
    {\vert x-y\vert^2_\eta}\lt 0
    \;\,,\;
    \pm(x^0 - y^ 0) \gt 0
  \right\}
  \,.
$$


We make the _Ansatz_ that we assume that $\Delta_{\pm}$, as a distribution in a single variable $x-y$, is a [[tempered distribution]]

$$
  \Delta_\pm \in \mathcal{S}'(\mathbb{R}^{p,1})
  \,,
$$

hence amenable to [[Fourier transform of distributions]]. If we do find a solution this way, it is guaranteed to be the unique solution by prop. \ref{AdvancedAndRetardedGreenFunctionsForGreenHyperbolicOperatorAreUnique}.

By [this prop.](Fourier+transform#BasicPropertiesOfFourierTransformOverCartesianSpaces)
the [[Fourier transform of distributions|distributional Fourier transform]] of equation (eq:KleinGordonEquationOnAdvacedRetardedPropagator) is

$$
  \begin{aligned}
    \label{FourierVersionOfPDEForKleinGordonAdvancedRetardedPropagator}
    \left(
      - \eta^{\mu \nu} k_\mu k_\nu - \left( \tfrac{m c}{\hbar} \right)^2
    \right)
    \widehat{\Delta_{\pm}}(k)
    & =
    \widehat{\delta}(k)
    \\
    & =
    1
  \end{aligned}
  \,,
$$

where in the second line we used the [[Fourier transform of distributions|Fourier transform]] of the [[delta distribution]]
from [this example](Dirac+distribution#FourierTransformOfDeltaDistribution).

Notice that this implies that the the [[Fourier transform]] of the [[causal propagator]]

$$
  \Delta \coloneqq \Delta_+ - \Delta_-
$$

satisfies the homogeneous equation:

$$
  \label{FourierVersionOfPDEForKleinGordonCausalPropagator}
  \left(
    - \eta^{\mu \nu} k_\mu k_\nu - \left( \tfrac{m c}{\hbar} \right)^2
  \right)
  \widehat{\Delta}(k)
  \;=\;
  0
  \,,
$$


Hence we are now reduced to finding solutions $\widehat{\Delta_\pm} \in \mathcal{S}'(\mathbb{R}^{p,1})$ to (eq:FourierVersionOfPDEForKleinGordonAdvancedRetardedPropagator) such that their [[Fourier inversion theorem|Fourier inverse]] $\Delta_\pm$ has the required [[support of a distribution|support]] properties.

There are various ways to solve this:

1. direct solution of (eq:FourierVersionOfPDEForKleinGordonAdvancedRetardedPropagator) via [[Cauchy principal values]];

1. solution of (eq:FourierVersionOfPDEForKleinGordonCausalPropagator) via [[delta distributions]] followed by [[splitting of distributions]].

**1)**

Suppose the following [[limit of a sequence|limit]] of [[non-singular distributions]] in the variable $k \in \mathbb{R}^{p,1}$
exists in the space of [[distributions]]

$$
  \label{LimitOverImaginaryOffsetForFourierTransformedAdvancedRetardedPropagator}
  \underset{ {\epsilon \in (0,\infty)} \atop { \epsilon \to 0 } }{\lim}
  \frac{1}{ (k_0 \mp i \epsilon)^2  - {\vert \vec k\vert^2} - \left( \tfrac{m c}{\hbar} \right)^2 }
  \;\in\;
  \mathcal{D}'(\mathbb{R}^{p,1})
$$

meaning that for each [[bump function]] $b \in C^\infty_{cp}(\mathbb{R}^{p,1})$ the [[limit of a sequence|limit]] in $\mathbb{C}$

$$
 \underset{ {\epsilon \in (0,\infty)} \atop { \epsilon \to 0 }   }{\lim}
 \underset{\mathbb{R}^{p,1}}{\int} \frac{b(k)}{ (k_0\mp i \epsilon)^2 - {\vert \vec k\vert}^2 - \left( \tfrac{m c}{\hbar} \right)^2  }
   d^{p+1}k
 \;\in\;
 \mathbb{C}
$$

exists. Then this limit is clearly a solution to the distributional equation (eq:FourierVersionOfPDEForKleinGordonAdvancedRetardedPropagator)
because on those bump functions $b(k)$ which happen to be products with $\left(-\eta^{\mu \nu}k_\mu k-\nu - \left( \tfrac{m c}{\hbar}\right)^2\right)$
we clearly have

$$
  \begin{aligned}
    \underset{ {\epsilon \in (0,\infty)} \atop { \epsilon \to 0 }   }{\lim}
    \underset{\mathbb{R}^{p,1}}{\int}
    \frac{
       \left( -\eta^{\mu \nu} k_\mu k_\nu - \left( \tfrac{m c}{\hbar} \right)^2 \right) b(k)
    }{
      (k_0\mp i \epsilon)^2 - {\vert \vec k\vert}^2 - \left( \tfrac{m c}{\hbar} \right)^2
    }
     d^{p+1}k
    & =
    \underset{\mathbb{R}^{p,1}}{\int}
    \underset{= 1}{
    \underbrace{
     \underset{ {\epsilon \in (0,\infty)} \atop { \epsilon \to 0 }   }{\lim}
     \frac{
         \left( -\eta^{\mu \nu} k_\mu k_\nu - \left( \tfrac{m c}{\hbar} \right)^2 \right) }{
     (k_0\mp i \epsilon)^2 - {\vert \vec k\vert}^2 - \left( \tfrac{m c}{\hbar} \right)^2  }
    }
    }
    b(k)\, d^{p+1}k
    \\
    & =
    \langle 1, b\rangle
  \end{aligned}
$$

Moreover, if the limiting distribution (eq:LimitOverImaginaryOffsetForFourierTransformedAdvancedRetardedPropagator)
exists, then it is clearly a [[tempered distribution]], hence we may apply [[Fourier inversion theorem|Fourier inversion]]
to  obtain [[Green functions]]

$$
  \label{AdvancedRetardedPropagatorViaFourierTransformOfLLimitOverImaginaryOffsets}
  \Delta_{\pm}(x,y)
  \;\coloneqq\;
   \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
  \frac{1}{(2\pi)^{p+1}}
  \underset{\mathbb{R}^{p,1}}{\int}
   \frac{e^{i k_\mu (x-y)^\mu}}{
      (k_0 \mp i \epsilon  )^2 - {\vert \vec k\vert}^2  - \left(\tfrac{m c}{\hbar}\right)^2
   }
   d k_0 d^p \vec k
  \,.
$$

To see that this is the correct answer, we need to check the support property.

Finally by the [[Fourier inversion theorem]], to show that the limit (eq:LimitOverImaginaryOffsetForFourierTransformedAdvancedRetardedPropagator) indeed exists it is sufficient to show that the
limit in (eq:AdvancedRetardedPropagatorViaFourierTransformOfLLimitOverImaginaryOffsets) exists.

To that end, consider the the [[non-negative number|non-negative]] [[square root]] (see at _[[plane wave]]_)

$$
  \omega(\vec k)
  \;\coloneqq\;
  c \sqrt{ \vert \vec k\vert^2 + \left( \tfrac{m c}{\hbar} \right)^2  }
  \;\in\; [0,\infty)
$$

and compute as follows:

$$
  \label{TheSupportOfTheCandidateAdvancedRetardedPropagatorIsinTheFutureOrPastRespectively}
  \begin{aligned}
    \Delta_\pm(x-y)
     & =
     \frac{1}{(2\pi)^{p+1}}
     \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
     \int \int
     \frac{
       e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
     }{
       (k_0 \mp i\epsilon)^2 - {\vert \vec k\vert}^2  -\left( \tfrac{m c}{\hbar}\right)^2
     }
     \, d k_0 \, d^p \vec k
     \\
     & =
     \frac{1}{(2\pi)^{p+1}}
     \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
     \int \int
     \frac{
       e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
     }{
       (k_0 \mp i \epsilon)^2 - \left(\omega(\vec k)/c\right)^2
     }
     \, d k_0 \, d^p \vec k
     \\
     &=
     \frac{1}{(2\pi)^{p+1}}
     \underset{ {\epsilon \in (0,\infty)} \atop {\epsilon \to 0} }{\lim}
     \int \int
     \frac{
       e^{i k_0 (x^0 - y^0)} e^{i \vec k \cdot (\vec x - \vec y)}
     }{
       \left(
         (k_0 \mp i\epsilon) - \omega(\vec  k)/c
       \right)
       \left(
          (k_0 \mp i \epsilon) + \omega(\vec k)/c
       \right)
     }
     \, d k_0 \, d^p \vec k
     \\
     & =
     \left\{
       \array{
          \frac{\pm i}{(2\pi)^{p}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
            \right)
          d^p \vec k
          & \vert & \text{if} \,  \pm (x^0 - y^0) \gt 0
          \\
          0 & \vert & \text{otherwise}
       }
     \right.
  \end{aligned}
$$

Here the key step is the application of [[Cauchy's integral formula]] in the fourth step. We discuss this now for $\Delta_+$, the discussion for $\Delta_-$ is the same, just with the appropriate signs reversed.

1. If  $(x^0 - y^0) \gt 0$ thn the expression $e^{ik_0 (x^0 - y^0)}$ decays with _[[positive number|positive]] [[imaginary part]]_ of $k_0$, so that we may expand the [[integration]] [[domain]] into the [[upper half plane]] as

   $$
     \begin{aligned}
       \int_{-\infty}^\infty d k_0
       & = \phantom{+}
         \int_{-\infty}^0 d k_0 + \int_{0}^{+ i \infty} d k_0
       \\
       & = + \int_{+i \infty}^0 d k_0  + \int_0^\infty d k_0
       \,;
     \end{aligned}
   $$

   Conversely, if $(x^0 - y^0) \lt 0$ then we may analogously expand into the [[lower half plane]].

1. This integration domain may then further be completed to two [[contour integrations]]. For the expansion into the [[upper half plane]] these encircle counter-clockwise the [[poles]] at $\pm \omega(\vec k)+ i\epsilon \in \mathbb{C}$, while for expansion into the [[lower half plane]] no poles are being encircled.

   <img src="https://ncatlab.org/nlab/files/ContourForAdvancedPropagator.png" height="280">


1. Apply [[Cauchy's integral formula]] to find in the case $(x^0 - y^0)\gt 0$ the sum of the [[residues]] at these two [[poles]] times $2\pi i$, zero in the other case. (For the retarded propagator we get $- 2 \pi i$ times the residues, because now the contours encircling non-trivial poles go clockwise).

1. The result does not depend on $\epsilon$ anymore, therefore the [[limit of a sequence|limit]] $\epsilon \to 0$ is now computed trivially.

This computation shows a) that the limiting distribution indeed exists, and b) that the [[support of a distribution|support]]
of $\Delta_+$ is in the future, and that of $\Delta_-$ is in the past.

Hence it only remains to see now that the support of $\Delta_\pm$ is inside the [[causal cone]].
But this follows from the previous argument, by using that the [[Klein-Gordon equation]] is invariant under
[[Lorentz transformations]].

$\,$

**2)**

A solution to the homogeneous equation (eq:FourierVersionOfPDEForKleinGordonCausalPropagator) is
clearly given by the following [[delta distribution]] in the variable $k \in \mathbb{R}^{p,1}$

$$
  \delta\left( -\eta^{\mu \nu} k_\mu k_\nu - \left( \tfrac{m c}{\hbar} \right)^2 \right)
  \;\in\;
  \mathcal{D}'(\mathbb{R}^{p,1})
  \,.
$$

This is a  [[tempered distribution]] (...)
and so its [[Fourier transformation of distributions]] exist. We claim that this distribution

$$
  \Delta(x-y)
  \;\coloneqq\;
  \frac{1}{(2\pi)^{p+1}}
  \underset{\mathbb{R}^{p,1}}{\int}
  e^{i k_\mu (x^\mu - y^\mu)}
  \delta\left( -\eta^{\mu \nu} k_\mu k_\nu - \left( \tfrac{m c}{\hbar} \right)^2 \right)
  \, d^{p+1}k
$$

has [[support of a distribution|support]] in the [[causal cone]] of the origin $x-y = 0$, and hence is the
[[causal propagator]].

(...)

=--


+-- {: .num_cor}
###### Corollary

Under reversal of arguments the [[advanced and retarded causal propagators]] are related by

$$
  \Delta_{\pm}(y-x) = \Delta_\mp(x-y)
  \,.
$$

It follows that the [[causal propagator]] $\Delta \coloneqq \Delta_+ - \Delta_-$ is skew-symmetric in its arguments:

$$
  \Delta(x-y) = - \Delta(y-x)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{AdvancedRetardedPropafatorsForKleinGordonOnMinkowskiSpacetime} we have with (eq:ModeExpansionForMinkowskiAdvancedRetardedPropagator)


$$
  \begin{aligned}
    \Delta_\pm(y-x)
     & =
     \left\{
       \array{
          \frac{\pm i}{(2\pi)^{p}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{-i \omega(\vec k)(x^0 - y^0)/c -  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{+i \omega(\vec k)(x^0 - y^0)/c  - i \vec k \cdot (\vec x - \vec  y) }
            \right)
          d^p \vec k
          & \vert & \text{if} \,  \mp (x^0 - y^0) \gt 0
          \\
          0 & \vert & \text{otherwise}
       }
     \right.
     \\
     & =
     \left\{
       \array{
          \frac{\pm i}{(2\pi)^{p}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{-i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{+i \omega(\vec k)(x^0 - y^0)/c  - i \vec k \cdot (\vec x - \vec  y) }
            \right)
          d^p \vec k
          & \vert & \text{if} \,  \mp (x^0 - y^0) \gt 0
          \\
          0 & \vert & \text{otherwise}
       }
     \right.
     \\
     & =
     \left\{
       \array{
          \frac{\mp i}{(2\pi)^{p}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{+i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)(x^0 - y^0)/c  - i \vec k \cdot (\vec x - \vec  y) }
            \right)
          d^p \vec k
          & \vert & \text{if} \,  \mp (x^0 - y^0) \gt 0
          \\
          0 & \vert & \text{otherwise}
       }
     \right.
     \\
     & =
     \Delta_\mp(x-y)
  \end{aligned}
$$

Here in the second step we applied [[change of integration variables]] $\vec k \mapsto - \vec k$ (which introduces _no_ sign because in addition to $d \vec k \mapsto - d \vec k$ the integration domain reverses [[orientation]]).

=--


+-- {: .num_prop #ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski}
###### Proposition
**(mode expansion of [[causal propagator]] for [[Klein-Gordon equation]] on [[Minkowski spacetime]])**

The [[causal propagator]] for the [[Klein-Gordon equation]] for [[mass]] $m$ on [[Minkowski spacetime]] $\mathbb{R}^{p,1}$ is given, in [[generalized function]] notation, by 


$$
  \begin{aligned}
    \Delta(x,y)
     & =
     \frac{+ i}{(2\pi)^{p}}
     \int
     \frac{1}{2\omega(\vec k)/c}
     \left(
         e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
         -
         e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
       \right)
     d^p \vec k
     \\
     & =
     \int
     \frac{1}{\omega(\vec k)/c}
     \sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
     \left(
         e^{i \vec k \cdot (\vec x -\vec y)}
         -
         e^{i \vec k \cdot (\vec x - \vec  y)}
       \right)
     d^p \vec k   
     \,,
  \end{aligned}
$$

where in the second line we used the [[trigonometric identity]] $sin(\alpha)= \tfrac{1}{2}\left( e^{i \alpha} - e^{-i \alpha} \right)$.


=--


+-- {: .proof}
###### Proof

By definition and using the expression from prop. \ref{AdvancedRetardedPropafatorsForKleinGordonOnMinkowskiSpacetime} for the [[advanced and retarded causal propagators]] we have

$$
  \begin{aligned}
  \Delta(x,y)
  & \coloneqq
  \Delta_+(x,y) - \Delta_-(x,y)
  \\
  & =
      \left\{
       \array{
          \frac{+ i}{(2\pi)^{p}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
            \right)
          d^p \vec k
          & \vert & \text{if} \,  + (x^0 - y^0) \gt 0
          \\
          \frac{(-1) (-1) i}{(2\pi)^{p}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
            \right)
          d^p \vec k
          & \vert & \text{if} \,  - (x^0 - y^0) \gt 0
       }
     \right.
     \\
     & =
          \frac{+ i}{(2\pi)^{p}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{i \omega(\vec k)(x^0 - y^0)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)(x^0 - y^0)/c + i \vec k \cdot (\vec x - \vec  y)}
            \right)
          d^p \vec k
  \end{aligned}
$$


=--



+-- {: .num_prop #CausalPropagatorAsFourierTransformOfDeltaDistributionOnTransformedKGOperator}
###### Proposition
**([[causal propagator]] as [[Fourier transform]] of [[delta distribution]]  on the [[Fourier transform|Fourier transformed]] [[Klein-Gordon operator]])**


The [[causal propagator]] for the [[Klein-Gordon equation]] at [[mass]] $m$ on [[Minkowski spacetime]] has the following equivalent expression, as a [[generalized function]]:


$$
 \Delta(x,y)
 \;=\;
  i (2\pi)^{-p} \int \delta\left( k_\mu k^\mu + \left( \tfrac{m c}{\hbar}\right)^2 \right) sgn( k_0 ) e^{ i k_\mu (x-y)^\mu } d^{p+1} k
  \,,
$$

where the [[integrand]] is the product of the [[sign function]] of $k_0$ with the [[delta distribution]] of the [[Fourier transform]] of the [[Klein-Gordon operator]] and a [[plane wave]] factor.

=--

+-- {: .proof}
###### Proof

By decomposing the integral over $k_0$ into its negative and its positive half, and applying the [[change of integration variables]] $k_0 = \pm\sqrt{h}$ we get

$$
  \begin{aligned}
    i (2\pi)^{-p} \int \delta\left( k_\mu k^\mu + \left( \tfrac{m c}{\hbar}\right)^2 \right) sgn( k_0 ) e^{ i k_\mu (x-y)^\mu } d^{p+1} k
     & = 
     + i (2\pi)^{-p} \int \int_0^\infty \delta\left( -k_0^2 + \vec k^2 + \left( \tfrac{m c}{\hbar}\right)^2 \right) e^{ i k_0 (x^0 - y^0) + i \vec k \cdot (\vec x - \vec y)}  d k_0 \, d^p \vec k
     \\
     & \phantom{=} 
     - i (2\pi)^{-p} \int \int_{-\infty}^0 \delta\left( -k_0^2 + \vec k^2 + \left(\tfrac{m c}{\hbar}\right)^2 \right)  e^{ i k_0 (x^0 - y^0)+ i \vec k \cdot (\vec x - \vec y) } d k_0 \, d^{p} \vec k
     \\
     & = 
     +i (2\pi)^{-p} \int \int_0^\infty \frac{1}{2 \sqrt{h}} \delta\left( -h + \omega(\vec k)^2/c^2  \right) e^{ + i \sqrt{h} (x^0 - y^0) + i \vec k \cdot \vec x } d h \, d^{p} \vec k
     \\
     & \phantom{=} 
     - i (2\pi)^{-p} \int \int_0^\infty  \frac{1}{2 \sqrt{h}} \delta\left( - h + \omega(\vec k)^2/c^2 \right) e^{ - i \sqrt{h} (x^0 - y^0) + i \vec k \cdot \vec x }  d h \, d^{p} \vec k
     \\
     & = 
     +i (2\pi)^{-p} \int \frac{1}{2 \omega(\vec k)/c} e^{ i \omega(\vec k) (x-y)^0/c + i \vec k \cdot \vec x}  d^{p} \vec k
     \\
     & \phantom{=} 
     - i (2\pi)^{-p} \int \frac{1}{2 \omega(\vec k)/c} e^{ - i \omega(\vec k) (x-y)^0/c + i \vec k \cdot \vec x }  d^{p} \vec k
     \\
     & = i (2 \pi)^{-p} \int \frac{1}{\omega(\vec k)/c} 
      sin\left( \omega(\vec k)(x-y)^0/c \right)
      e^{i \vec k \cdot (\vec x - \vec y)} 
  \end{aligned}
$$

The last line is the expression for the causal propagator from prop. \ref{ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski}.


=--


+-- {: .num_prop #Smooth0TypeIsSheavesOnSmoothMfd}
###### Proposition


The [[causal propagator]] for the [[Klein-Gordon equation]] at [[mass]] $m$ on [[Minkowski spacetime]] has the following equivalent expression, as a [[generalized function]], given as a [[contour integral]] along a curve $C(\vec k)$ going counter-clockwise around the two [[poles]] at $k_0 = \pm \omega(\vec k)/c$:


$$
  \Delta(x,y)
  \;=\;
    (2\pi)^{-(p+1)}
    \int
    \underset{C(\vec k)}{\oint}
     \frac{e^{i k_\mu (x-y)^\mu}}{ k_\mu k^\mu + m^2 }
    \,d k_0
    \,d^{p} k
  \,.
$$

=--


<img src="https://ncatlab.org/nlab/files/ContourForCausalPropagator.png" height="160">

> graphics grabbed from [Kocic 16](#Kocic16)


+-- {: .proof}
###### Proof


By [[Cauchy's integral formula]] we compute as follows:

$$
  \begin{aligned}
    (2\pi)^{-(p+1)}
    \int
    \underset{C(\vec k)}{\oint}
     \frac{e^{i k_\mu (x-y)^\mu}}{ k_\mu k^\mu + m^2 }
    \,d k_0
    \,d^{p} k
    & =
    (2\pi)^{-(p+1)}
    \int
    \underset{C(\vec k)}{\oint}
      \frac{
        e^{i k_0 x^0} e^{ i \vec k \cdot (\vec x - \vec y)}
      }{
        - k_0^2 + \omega(\vec k)^2/c^2
      } 
    \,d k_0
    \,d^p \vec k 
    \\
    & =   
    (2\pi)^{-(p+1)}
    \int
    \underset{C(\vec k)}{\oint}
      \frac{
        e^{i k_0 (x-y)^0} e^{i \vec k \cdot (\vec x - \vec y)}
      }{
        ( \omega(\vec k)/c + k_0 )
        ( \omega(\vec k)/c - k_0 )
      } 
    \,d k_0
    \,d^p \vec k
    \\
    & = 
    (2\pi)^{-(p+1)}
     2\pi i
     \int
     \left(
     \frac{
       e^{i \omega(\vec k) (x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
     }
     {
       2 \omega(\vec k)/c
     }
     -
     \frac{
       e^{ - i \omega(\vec k) (x^0 - y^0)/c} e^{i \vec k \cdot (\vec x - \vec y)}
     }{
       2 \omega(\vec k)/c
     }
    \right)
    \,d^p \vec k
    \\
    & = 
    i 
    (2\pi)^{-p}
    \int
      \frac{1}{\omega(\vec k)/c}
      sin\left( \omega(\vec k)(x^0 - y^0)/c \right)
      e^{i \vec k \cdot (\vec x - \vec y)}
     \,d^p \vec k
     \,.
  \end{aligned}
$$

The last line is the expression for the causal propagator from prop. \ref{ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski}

=--


### On general globally hyperbolic spacetimes

Let $(X,g)$ be a [[time orientation|time-oriented]] [[globally hyperbolic spacetime]] and let $m \in \mathbb{R}_{\geq 0}$ (the "[[mass]]"). Then the [[Klein-Gordon equation]]

$$
  (\Box_g - m^2) \phi = 0
$$

(a [[partial differential equation]] on [[smooth functions]] $f \in C^\infty(X,\mathbb{R})$ ) has unique advanced and retarded [[Green functions]] $E^{R/A}$, namely [[continuous linear functionals]]

$$
  E^{A/R} 
   \;\colon\;
  C^\infty_c(X)
   \longrightarrow
  C^\infty(X)
$$

(from [[bump functions]] to general [[smooth functions]]) which are [[fundamental solutions]] in that 

$$
  (\Box_g - m^2) \circ E^{A/R} = \delta
  \phantom{AAAA}
  E^{A/R} \circ (\Box_g - m^2) = \delta
$$

and which have advanced/retarded [[support of a distribution]] when viewed (via the [[Schwartz kernel theorem]]) as [[distributions]] on the [[Cartesian product]] manifold $X \times X$

$$
  supp( E^{A/R}) \subset \{ (x_1, x_2) \in X \times X  \;\vert\; x_1 \in J^{\mp} (x_2) \}
 \,.
$$

In fact these two fundamental solutions are related by switching their arguments 

$$
  E^{A/R}(x_1, x_2) = E^{R/A}(x_2, x_1)
  \,.
$$

The difference

$$
  E \;\coloneqq\; E^R - E^A
$$

is the _causal propagator_ on the given spacetime.

[[!include propagators - table]]


## Properties

The causal propagator yields the [[Peierls bracket]], which is the [[Poisson bracket]] on the [[covariant phase space]] of the [[free field|field]] [[scalar field|scalar]] [[field (physics)|field]]. The [[Moyal deformation quantization]] of this [[covariant phase space]] yields the [[Wick algebra]] of [[quantum observables]] of the free scalar field.


## Related concepts

* [[Feynman propagator]]

* [[Hadamard propagator]]

* [[Green hyperbolic differential operator]]

## References

The causal propagator was first considered (in the context of [[quantum electrodynamics]]) in 

* {#JordanPauli27} [[Pascual Jordan]], [[Wolfgang Pauli]], _Zur Quantenelektrodynamik ladungsfreier Felder_, Zeitschrift f&#252;r Physik 47, 151 (1928)

whence often called the _Jordan-Pauli distribution_.

General discussion includes

* {#Baer14} [[Christian Bär]], _Green-hyperbolic operators on globally hyperbolic spacetimes_, Communications in Mathematical Physics 333, 1585-1615 (2014) ([doi](http://dx.doi.org/10.1007/s00220-014-2097-7), [arXiv:1310.0738](https://arxiv.org/abs/1310.0738))

* {#Khavkine14} [[Igor Khavkine]], _Covariant phase space, constraints, gauge and the Peierls formula_, Int. J. Mod. Phys. A, 29, 1430009 (2014) ([arXiv:1402.1282](https://arxiv.org/abs/1402.1282))

based on 

* {#Sanders12} [[Ko Sanders]], _A note on spacelike and timelike compactness_, Classical and Quantum Gravity 30, 115014 (2012) ([doi](http://dx.doi.org/10.1088/0264-9381/30/11/115014), [arXiv:1211.2469](https://arxiv.org/abs/1211.2469))


Textbook discussion for [[free fields]] in [[Minkowski spacetime]] is in

* {#Scharf95} [[Günter Scharf]],  section 2.3 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Springer 1995

* {#Scharf01} [[Günter Scharf]], section 1 of  _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

(there denoted "$-i D_m(x-y)$" and called the "Jordan-Pauli function").


An overview of the [[Green functions]] of the [[Klein-Gordon operator]], hence of the [[Feynman propagator]], [[advanced propagator]], [[retarded propagator]], [[causal propagator]] etc. is given in

* {#Kocic16} [[Mikica Kocic]], _Invariant Commutation and Propagation Functions Invariant Commutation and Propagation Functions_, 2016 ([[KGPropagatorsOnMinkowskiTable.pdf:file]])


For more see the references at _[[wave equation]]_.

[[!redirects causal propagators]]

[[!redirects causal Green function]]
[[!redirects causal Green functions]]

[[!redirects Jordan-Pauli distribution]]
[[!redirects Jordan-Pauli distributions]]


[[!redirects Pauli-Jordan distribution]]
[[!redirects Pauli-Jordan distributions]]

[[!redirects commutator function]]
[[!redirects commutator functions]]
