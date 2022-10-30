

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

What are called _advanced_ and _retarded causal Green functions_ $\Delta_{A/R}$ are [[Green functions]] for [[hyperbolic differential operators]] on manifolds with [[causal structure]] (e.g. [[spacetimes]]) whose [[support]] is in the [[future cone]] or [[past cone]], respectively, of the source excitation. The corresponding [[integral kernels]] hence say how a [[delta distribution|point excitation]] _propagates_ into the future or past, respectively, via the given [[differential equation]], and therefore these are also called the advanced/future _propagators_.

If both advanced and retarded Green functions exist for a differential operator as well as for its [[formally adjoint differential operator|formal adjoint]], then the differental operator is called a _[[Green hyperbolic differential operator]]_.  The archetypical examples are, on [[globally hyperbolic spacetimes]]:

1. [[normally hyperbolic differential operators]] such as the [[wave operator]] and the [[Klein-Gordon operator]];

1. [[Dirac operators]] on [[spinor bundles]] whose square is a normally hyperbolic differential operator as above.

The advanced/retarded [[integral kernel]]

$$
  \Delta_{A/R}
  \in \mathcal{D}'(X \times X)
$$

is such that

1. $(x,y) \in supp(\Delta_R)$ precisely if $x$ is in the [[causal future]] of $y$;

1. $(x,y) \in supp(\Delta_A)$ precisely if $x$ is in the [[causal past]] of $y$.

Written as [[generalized functions]] these satisfy

$$
  \Delta_A(x,y) = \Delta_R(y,x)
  \,.
$$

This implies in particular that

1. the _[[causal propagator]]_, which is the difference of the two

   $$
     \Delta_S \coloneqq \Delta_R - \Delta_A
   $$

   is skew-symmetric in its arguments (reflecting the fact that this is the [[integral kernel]] for the [[Peierls-Poisson bracket]] for the [[free field|free]] [[scalar field]] on the given spacetime);

1. the _[[Dirac propagator]]_, which is the sum of the two

   $$
     \Delta_D \coloneqq \Delta_R + \Delta_A
   $$

   is symmetric in its arguments, reflecting the fact that this is the integral kernel for [[time-ordered products]] away from the [[diagonal]].

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


Given a [[Green hyperbolic differential operator]] $P$ (def. \ref{GreenHyperbolicDifferentialOperator}), the advanced, retarded and causal Green functions of $P$ (def. \ref{AdvancedAndRetardedGreenFunctions}) are [[continuous linear maps]] with respect to the [[topological vector space]] structure from def. \ref{TVSStructureOnSpacesOfSmoothSections} and also have a unique continuous extension to the spaces of sections with larger support (def. \ref{CompactlySourceCausalSupport}) as follows:

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

### For Klein-Gordon operator on Minkowski spacetime

On [[Minkowski spacetime]] $\mathbb{R}^{p,1}$ consider the [[Klein-Gordon operator]]

$$
  \eta^{\mu \nu} \frac{\partial}{\partial x^\mu} \frac{\partial}{\partial x^\nu} \Phi -  \left( \tfrac{m c}{\hbar} \right)^2 \Phi \;=\; 0 \,.
$$


+-- {: .num_prop #AdvancedRetardedPropafatorsForKleinGordonOnMinkowskiSpacetime}
###### Proposition
**([[advanced and retarded propagators]] for [[Klein-Gordon operator]] on [[Minkowski spacetime]])**

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
          \frac{1}{(2\pi)^{p+1}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{i \omega(\vec k)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)/x} + i \vec k \cdot (\vec x - \vec  y)
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

Since the [[Klein-Gordon operator]] is invariant under [[translations]] in $\mathbb{R}^{p,1}$ it is clear that the propagators, as a [[distribution in two variables]], depends only on the difference of its two arguments

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

We discuss two ways to solve this:

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
          \frac{1}{(2\pi)^{p+1}}
          \int
           \frac{1}{2\omega(\vec k)/c}
            \left(
              e^{i \omega(\vec k)/c +  i \vec k \cdot (\vec x -\vec y)}
              -
              e^{-i \omega(\vec k)/x} + i \vec k \cdot (\vec x - \vec  y)
            \right)
          d^p \vec k
          & \vert & \text{if} \,  \pm (x^0 - y^0) \gt 0
          \\
          0 & \vert & \text{otherwise}
       }
     \right.
  \end{aligned}
$$

Here key step is the application of [[Cauchy's integral formula]] in the fourth step.
We discuss this for $\Delta_+$, the discussion for $\Delta_-$ is the same, just with the appropriate signs reversed.

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


1. Apply [[Cauchy's integral formula]] to find in the case $(x^0 - y^0)\gt 0$ the sum of the [[residues]] at these two [[poles]], zero in the other case.

1. The result does not depend on $\epsilon$ anymore, therefore the [[limit of a sequence|limit]] $\epsilon \to 0$ is now computed trivially.

This computation shows a) that the limiting distribution indeed exists, and b) that the [[support of a distribution|support]]
of $\Delta_+$ is in the future, and that of $\Delta_-$ is in the past.

Hence it only remains to see now that the support of $\Delta_\pm$ is inside the [[causal cone]]. 
This follows by (...?...).

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

This is a [[compactly supported distribution]], hence in particular a  [[tempered distribution]]
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


## Related concepts


[[!include propagators - table]]


$\,$

* [[Green hyperbolic differential operator]]


## References

General discussion includes

* {#Baer14} [[Christian Bär]], _Green-hyperbolic operators on globally hyperbolic spacetimes_, Communications in Mathematical Physics 333, 1585-1615 (2014) ([doi](http://dx.doi.org/10.1007/s00220-014-2097-7), [arXiv:1310.0738](https://arxiv.org/abs/1310.0738))

* {#Khavkine14} [[Igor Khavkine]], _Covariant phase space, constraints, gauge and the Peierls formula_, Int. J. Mod. Phys. A, 29, 1430009 (2014) ([arXiv:1402.1282](https://arxiv.org/abs/1402.1282))


Textbook discussion for [[free fields]] in [[Minkowski spacetime]] is in

* {#Scharf95} [[Günter Scharf]],  section 2.3 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Springer 1995

* {#Scharf01} [[Günter Scharf]], section 1 of  _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

An overview of the [[Green functions]] of the [[Klein-Gordon operator]], hence of the [[Feynman propagator]], [[advanced propagator]], [[retarded propagator]], [[causal propagator]] etc. is given in

* {#Kocic16} [[Mikica Kocic]], _Invariant Commutation and Propagation Functions Invariant Commutation and Propagation Functions_, 2016 ([[KGPropagatorsOnMinkowskiTable.pdf:file]])

Discussion on general [[globally hyperbolic spacetimes]] includes

* F. Friedlander, _The Wave Equation on a Curved Space-Time_, Cambridge: Cambridge University Press, 1975

* {#BaerGinouxPfaeffle07} [[Christian Bär]], [[Nicolas Ginoux]], [[Frank Pfäffle]], _Wave Equations on Lorentzian Manifolds and Quantization_, ESI Lectures in Mathematics and Physics, European Mathematical Society Publishing House, ISBN 978-3-03719-037-1, March 2007, Softcover ([arXiv:0806.1036](https://arxiv.org/abs/0806.1036))


* {#Ginoux08} [[Nicolas Ginoux]], _Linear wave equations_,  Ch. 3 in [[Christian Bär]], [[Klaus Fredenhagen]], _Quantum Field Theory on Curved Spacetimes: Concepts and Methods_, Lecture Notes in Physics, Vol. 786, Springer, 2009

Review in the context of [[perturbative algebraic quantum field theory]] includes

* [[Katarzyna Rejzner]], sections 4.1 and 6.2.3 of _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([pdf](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))


[[!redirects retarded and advanced causal propagators]]

[[!redirects advanced and retarded propagators]]
[[!redirects retarded and advanced propagators]]


[[!redirects advanced and retarded propagator]]
[[!redirects retarded and advanced propagator]]


[[!redirects advanced propagator]]
[[!redirects advanced propagators]]

[[!redirects retarded propagator]]
[[!redirects retarded propagators]]

[[!redirects advanced causal propagator]]
[[!redirects advanced causal propagators]]

[[!redirects retarded causal propagator]]
[[!redirects retarded causal propagators]]

[[!redirects advanced Green function]]
[[!redirects advanced Green functions]]

[[!redirects retarded Green function]]
[[!redirects retarded Green functions]]

[[!redirects retarded and advanced Green functions]]
[[!redirects advanced and retarded Green functions]]

[[!redirects advanced Green's function]]
[[!redirects advanced Green's functions]]

[[!redirects retarded Green's function]]
[[!redirects retarded Green's functions]]

[[!redirects advanced or retarded Green function]]
[[!redirects advanced or retarded Green functions]]

[[!redirects retarded and advanced Green's functions]]
[[!redirects advanced and retarded Green's functions]]

