## Lagrangians
  {#Lagrangians}


Given any [[type]] of [[field (physics)|fields]] (def. \ref{FieldsAndFieldBundles}), those [[field histories]] that
are to be regarded as "physically realizable" (if we think of the field theory as a description of the [[observable universe]])
should satisfy some [[differential equation]] -- the _[[equation of motion]]_ -- meaning that realizability of any field histories may
be checked upon restricting the configuration to the [[infinitesimal neighbourhoods]] (example \ref{InfinitesimalNeighbourhood}) of each spacetime point. This expresses the physical absence of "action at a distance" and is one aspect of what it means to have
a _[[local field theory]]_. By remark \ref{JetBundleInTermsOfSyntheticDifferentialGeometry} this means that
[[equations of motion]] of a field theory are [[equations]] among the [[coordinates]] of the [[jet bundle]] of the [[field bundle]].

For many field theories of interest, their [[differential equation|differential]] [[equation of motion]]
is not a random [[partial differential equations]], but is of the special kind that exhibits the "[[principle of extremal action]]" (prop. \ref{PrincipleOfExtremalAction} below)
determined by a _[[local Lagrangian density]]_
(def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below). These are called _[[Lagrangian field theories]]_, and this is what we consider here.

Namely among all the [[variational differential forms]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime})
two kinds stand out, namley the 0-forms in $\Omega^{0,0}_\Sigma(E)$ -- the smooth functions -- and the horizontal $p+1$-forms
$\Omega^{p+1,0}_\Sigma(E)$ -- to be called the _[[Lagrangian densities]] $\mathbf{L}$_ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} below) -- since these occupy the two "corners" of the [[variational bicomplex]] (eq:VariationalBicomplexDiagram).
There is not much to say about the 0-forms, but the [[Lagrangian densities]] $\mathbf{L}$ do inherit special structure
from their special position in the [[variational bicomplex]]:

Their [[variational derivative]] $\delta \mathbf{L}$ uniquely decomposes as

1.  the _[[Euler-Lagrange derivative]]_ $\delta_{EL} \mathbf{L}$ which is proportional to the variation of the fields
(instead of their derivatives)

1.  the [[total derivative|total spacetime derivative]] $d \Theta_{BFV}$
of a potential $\Theta_{BFV}$ for a _[[presymplectic current]]_ $\Omega_{BFV} \coloneqq \delta \Theta_{BFV}$.

This is prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime} below:

$$
  \delta \mathbf{L}
    \;=\;
  \underset{ \text{Euler-Lagrange variation}
  }{\underbrace{\delta_{EL}\mathbf{L}}} - d \underset{\text{presymplectic current}}{\underbrace{\Theta_{BFV}}}
  \,.
$$

These two terms play a pivotal role in the theory: The condition that the first term vanishes
on [[field histories]] is a [[differential equation]] on field histories,
called the _[[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]]_ (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime} below).
The space of solutions to this [[differential equation]], called the _[[on-shell]] [[space of field histories]]_

$$
  \label{InclusionOfOnShellSpaceOfFieldHistories}
  \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
    \overset{\phantom{AAA}}{\hookrightarrow}
  \Gamma_\Sigma(E)
$$

has the interpretation of the space of "physically realizable field histories".
This is the key object of study in the following chapters. Often this is
referred to as the space of _[[classical field theory|classical]] field histories_,
indicating that this does not yet reflect the full [[quantum field theory]].

Indeed, there is also the second term in the variational derivative of the Lagrangian density,
the [[presymplectic current]] $\Theta_{BFV}$, and this implies a [[presymplectic structure]] on
the on-shell space of field histories (def. \ref{PhaseSpaceAssociatedWithCauchySurface} below)
which encodes [[deformations]] of the algebra of
smooth functions on $\Gamma_\Sigma(E)$. This deformation is the _[[quantization]]_ of the field
theory to an actual [[quantum field theory]], which we discuss [below](#Quantization).

$$
  \array{
     &&& \delta \mathbf{L}
     \\
     &&& =
     \\
     &  & \delta_{EL}\mathbf{L} &- & d \Theta_{BFV}   &
     \\
     & \swarrow && && \searrow
     \\
     \array{
       \text{classical}
       \\
       \text{field theory}
     }
     && && &&
     \array{
       \text{deformation to}
       \\
       \text{quantum}
       \\
       \text{field theory}
     }
  }
$$



$\,$

+-- {: .num_defn #LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}
###### Definition
**([[local Lagrangian density]])**

Given a [[field bundle]] $E$ over a $(p+1)$-dimensional [[Minkowski spacetime]] $\Sigma$ as in example \ref{TrivialVectorBundleAsAFieldBundle}, then a _[[local Lagrangian density]]_ $\mathbf{L}$ (for the type of field thus defined) is a [[horizontal differential form]] of degree $(p+1)$ (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}) on the corresponding [[jet bundle]]
(def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}):

$$
  \mathbf{L} \;\in \; \Omega^{p+1,0}_{\Sigma}(E)
  \,.
$$

By example \ref{BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle}
in terms of the given [[volume form]] on spacetimes, any such Lagrangian density may uniquely be written as

$$
  \label{LagrangianFunctionViaVolumeForm}
  \mathbf{L} = L \, dvol_\Sigma
$$

where the [[coefficient]] function (the _Lagrangian function_)
is a smooth function on the spacetime and field coordinates:

$$
  L = L((x^\mu), (\phi^a), (\phi^a_{,\mu}), \cdots )
  \,.
$$

where by prop. \ref{JetBundleIsLocallyProManifold} $L((x^\mu), \cdots)$ depends locally on an arbitrary but finite
order of derivatives $\phi^a_{,\mu_1 \cdots \mu_k}$.

We say that a [[field bundle]] $E \overset{fb}{\to} \Sigma$ (def. \ref{FieldsAndFieldBundles}) equipped with a [[local Lagrangian density]] $\mathbf{L}$
is (or defines) a _[[prequantum field theory|prequantum]] [[Lagrangian field theory]]_ on the [[spacetime]] $\Sigma$.

=--


+-- {: .num_remark #ParameterizedLagrangianDensities}
###### Remark
**(parameterized and [[physical unit]]-less [[Lagrangian densities]])**

More generally we may consider parameterized collections of [[Lagrangian densities]], i.e. functions

$$
  \mathbf{L}_{(-)}
  \;\colon\;
  U \longrightarrow \Omega^{p+1,0}_\Sigma(E)
$$

for $U$ some [[Cartesian space]] or generally some [[super Cartesian space]].

For example all [[Lagrangian densities]] considered in [[relativistic field theory]] are naturally [[smooth functions]] of the scale of the [[metric]] $\eta$ (def. \ref{SpacetimeAsMatrices})

$$
  \array{
    \mathbb{R}_{\gt 0}
      &\overset{}{\longrightarrow}&
    \Omega^{p+1,0}_\Sigma(E)
    \\
    r &\mapsto& \mathbf{L}_{r^2\eta}
  }
$$

But by the discussion in remark \ref{MinkowskiMetricAndPhysicalUnitOfLength}, in [[physics]] a rescaling of the [[metric]] is interpreted as reflecting but a change of [[physical units]] of [[length]]/[[distance]]. Hence if a [[Lagrangian density]] is supposed to express intrinsic content of a [[theory (physics)|physical theory]], it should remain unchanged under such a change of [[physical units]].

This is achieved by having the Lagrangian be parameterized by _further_ parameters, whose corresponding [[physical units]] compensate that of the metric such as to make the Lagrangian density "[[physical unit]]-less".

This means to consider parameter spaces $U$ equipped with an [[action]] of the multiplicative [[group]] $\mathbb{R}_{\gt 0}$ of [[positive real numbers]], and parameterized Lagrangians

$$
  \mathbf{L}_{(-)} \;\colon\; U \longrightarrow \Omega^{p+1,0}_\Sigma(E)
$$

which are [[invariant]] under this [[action]].

=--


+-- {: .num_remark #LocallyVariationalFieldTheory}
###### Remark
**([[locally variational field theory]] and Lagrangian [[circle n-bundle with connection|p-gerbe connection]])**

If the [[field bundle]] (def. \ref{FieldsAndFieldBundles}) is not just a [[trivial vector bundle]] over [[Minkowski spacetime]] (example \ref{TrivialVectorBundleAsAFieldBundle}) then a Lagrangian density for a given [[equation of motion]] may not exist
as a globally defined differential $(p+1)$-form, but only as a [[circle n-bundle with connection|p-gerbe connection]].
This is the case for _[[locally variational field theories]]_ such as the _[[charged particle]]_, the _[[WZW model]]_
and generally theories involving _[[higher WZW terms]]_. For more on this see the exposition at _[[schreiber:Higher Structures|Higher Structures in Physics]]_.

=--


+-- {: .num_example #LagrangianForFreeScalarFieldOnMinkowskiSpacetime}
###### Example
**([[local Lagrangian density]] for [[free field|free]] [[real scalar field]] on [[Minkowski spacetime]])**

Consider the [[field bundle]] for the [[real scalar field]] from example \ref{RealScalarFieldBundle},
i.e. the [[trivial line bundle]] over [[Minkowski spacetime]].

According to def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}
its [[jet bundle]] $J^\infty_\Sigma(E)$ has canonical coordinates

$$
  \left\{
     \{x^\mu\}, \phi, \{\phi_{,\mu}\}, \{\phi_{,\mu_1 \mu_2}\}, \cdots
  \right\}
  \,.
$$

In these coordinates, the [[local Lagrangian density]] $L \in \Omega^{p+1,0}(\Sigma)$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
defining the [[free field|free]] [[real scalar field]] of [[mass]] $m \in \mathbb{R}$ on $\Sigma$ is

$$
  L
    \coloneqq
  \tfrac{1}{2}
  \left(
    \eta^{\mu \nu} \phi_{,\mu} \phi_{,\nu}
    -
    m^2 \phi^2
  \right)
  \mathrm{dvol}_\Sigma
  \,.
$$

This is naturally thought of as a collection of Lagrangians smoothly parameterized by the
[[metric]] $\eta$ and the [[mass]] $m$. For this to be [[physical unit]]-free in the sense of
remark \ref{ParameterizedLagrangianDensities} the [[physical unit]] of the parameter $m$ must be
that of the inverse metric, hence must be an inverse [[length]] according to remark \ref{MinkowskiMetricAndPhysicalUnitOfLength}
This is the _inverse [[Compton wavelength]]_  $\ell_m = \hbar / m c$ (eq:ComptonWavelength) and hence
the [[physical unit]]-free version of the Lagrangian density for the free scalar particle is

$$
  \mathbf{L}_{\eta,\ell_m}
  \:\coloneqq\;
  \tfrac{\ell_m^2}{2}
  \left(
    \eta^{\mu \nu} \phi_{,\mu} \phi_{,\nu}
    -
    \left( \tfrac{m c}{\hbar} \right)^2 \phi^2
  \right)
  \mathrm{dvol}_\Sigma
  \,.
$$


=--


+-- {: .num_example #ElectromagnetismLagrangianDensity}
###### Example
**([[local Lagrangian density]] for [[free field|free]] [[electromagnetism]])**

Consider the [[field bundle]] $T^\ast \Sigma \to \Sigma$ for the [[electromagnetic field]] on [[Minkowski spacetime]] from example \ref{Electromagnetism},
i.e. the [[cotangent bundle]], which over Minkowski spacetime happens to be a [[trivial vector bundle]] of [[rank of a vector bundle|rank]]
$p+1$. With [[fiber]] coordinates taken to be $(a_\mu)_{\mu = 0}^p$, the induced fiber coordinates on the
corresponding [[jet bundle]] $J^\infty_\Sigma(T^\ast \Sigma)$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) are
$( (x^\mu), (a_\mu), (a_{\mu,\nu}), (a_{\mu,\nu_1 \nu_2}), \cdots )$.

Consider then the [[local Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) given by

$$
  \label{ElectromagnetismLagrangian}
  \mathbf{L}
    \;\coloneqq\;
  \tfrac{1}{2}
  f_{\mu \nu} f^{\mu \nu} dvol_\Sigma
  \;\in\;
  \Omega^{p+1,0}_\Sigma(T^\ast \Sigma)
  \,,
$$

where $f_{\mu \nu} \coloneqq \tfrac{1}{2}(a_{\nu,\mu} - a_{\mu,\nu})$ are the components of the universal [[Faraday tensor]] on the [[jet bundle]] from example \ref{JetFaraday}.

This is the [[Lagrangian density]] that defines the Lagrangian field theory of _[[free field|free]] [[electromagnetism]]_.

Here for $A \in \Gamma_\Sigma(T^\ast \Sigma)$ an [[electromagnetic field]] history ([[vector potential]]),
then the [[pullback of differential forms|pullback]] of $f_{\mu \nu}$ along its [[jet prolongation]] (def. \ref{JetProlongation})
is the corresponding component of the [[Faraday tensor]] (eq:TensorFaraday):

$$
  \begin{aligned}
    \left(
      j^\infty_\Sigma(A)
    \right)^\ast(f_{\mu \nu})
    & =
    (d A)_{\mu \nu}
    \\
    & = F_{\mu \nu}
  \end{aligned}
$$

It follows that the pullback of the Lagrangian (eq:ElectromagnetismLagrangian) along the
jet prologation of the electromagnetic field is

$$
  \begin{aligned}
    \left(
      j^\infty_\Sigma(A)
    \right)^\ast \mathbf{L}
    & =
    \tfrac{1}{2}
    F_{\mu \nu} F^{\mu \nu} dvol_\Sigma
    \\
    & =
    \tfrac{1}{2} F \wedge \star_\eta F
  \end{aligned}
$$

Here $\star_\eta$ denotes the [[Hodge star operator]] of [[Minkowski spacetime]].

=--

More generally:

+-- {: .num_example #YangMillsLagrangian}
###### Example
**([[Lagrangian density]] for [[Yang-Mills theory]] on [[Minkowski spacetime]])**

Let $\mathfrak{g}$ be a [[finite number|finite]] [[dimension|dimensional]] [[Lie algebra]] which is [[semisimple Lie algebra|semisimple]]. This means that the [[Killing form]] [[invariant polynomial]]

$$
  k \colon \mathfrak{g} \otimes \mathfrak{g} \longrightarrow \mathbb{R}
$$

is a non-degenerate [[bilinear form]]. Examples include the [[special unitary Lie algebras]] $\mathfrak{so}(n)$.

Then for $E = T^\ast \Sigma \otimes \mathfrak{g}$
the [[field bundle]] for [[Yang-Mills theory]] as in example \ref{YangMillsFieldOverMinkowski},
the [[Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) $\mathfrak{g}$-[[Yang-Mills theory]] on [[Minkowski spacetime]] is

$$
  \mathbf{L}
    \;\coloneqq\;
  \tfrac{1}{2}
  k_{\alpha \beta} f^\alpha_{\mu \nu} f^{\beta \mu \nu} dvol_\Sigma
  \;\in\;
  \Omega^{p+1,0}_\Sigma(T^\ast \Sigma)
  \,,
$$

where

$$
  f^\alpha_{\mu \nu}
  \;=\;
  \tfrac{1}{2}
  \left(
    a^\alpha_{\nu,\mu}
    -
    a^\alpha_{\mu,\nu}
    +
    \gamma^{\alpha}{}_{\beta \gamma}
    a^\beta_{\mu} a^\gamma_{\nu}
 \right)
  \;\in\;
  \Omega^{0,0}_\Sigma(E)
$$

is the universal [[Yang-Mills theory|Yang-Mills]] [[field strength]] (eq:YangMillsJetFieldStrengthMinkowski).

=--




+-- {: .num_example #BFieldLagrangianDensity}
###### Example
**([[local Lagrangian density]] for [[free field|free]] [[B-field]])**

Consider the [[field bundle]] $\wedge^2_\Sigma T^\ast \Sigma \to \Sigma$ for the [[B-field]] on [[Minkowski spacetime]] from example \ref{BField}. With [[fiber]] coordinates taken to be $(b_{\mu \nu})$ with

$$
  b_{\mu \nu} = - b_{\nu \mu}
  \,,
$$

the induced fiber coordinates on the
corresponding [[jet bundle]] $J^\infty_\Sigma(T^\ast \Sigma)$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) are
$( (x^\mu), (b_{\mu \nu}), (b_{\mu \nu, \mu_1}), (b_{\mu \nu, \mu_1 \mu_2}), \cdots )$.

Consider then the [[local Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) given by

$$
  \label{LagrangianForBField}
  \mathbf{L}
    \;\coloneqq\;
  \tfrac{1}{2}
  h_{\mu_1 \mu_2 \mu_3} h^{\mu_1 \mu_2 \mu_3} \, dvol_\Sigma
  \;\in\;
  \Omega^{p+1,0}_\Sigma(\wedge^2_\Sigma T^\ast \Sigma)
  \,,
$$

where $h_{\mu_1 \mu_2 \mu_3}$ are the components of the universal [[B-field|B-]][[field strength]] on the [[jet bundle]] from example \ref{BFieldJetFaraday}.

=--


+-- {: .num_example #LagrangianDensityForDiracField}
###### Example
**([[Lagrangian density]] for [[free field theory|free]] [[Dirac field]] on [[Minkowski spacetime]])**

For $\Sigma$ [[Minkowski spacetime]] of [[dimension]] $p + 1 \in \{3,4,6,10\}$ (def. \ref{MinkowskiSpacetime}),
consider the [[field bundle]] $\Sigma \times S_{odd} \to \Sigma$ for the [[Dirac field]] from example \ref{DiracFieldBundle}.
With the two-component [[spinor]] [[field fiber]] coordinates from remark \ref{TwoComponentSpinorNotation}, the [[jet bundle]] has induced fiber coordinates as follows:

$$
  \left(
   \left(\psi^\alpha\right)
   ,
   \left(
      \psi^\alpha_{,\mu}
   \right)
   ,
   \cdots
  \right)
   \;=\;
  \left(
     \left(
         (\chi_a), (\chi_{a,\mu}), \cdots
     \right),
     \left(
        ( \xi^{\dagger \dot a}), (\xi^{\dagger \dot a}_{,\mu}), \cdots
     \right)
  \right)
$$

All of these are odd-graded elements (def. \ref{SupercommutativeSuperalgebra}) in a [[Grassmann algebra]] (example \ref{GrassmannAlgebra}), hence anti-commute with each other, in generalization of (eq:DiracFieldCoordinatesAnticommute):

$$
  \label{DiracFieldJetCoordinatesAnticommute}
  \psi^\alpha_{,\mu_1 \cdots \mu_r}
  \psi^\beta_{,\mu_1 \cdots \mu_s}
  \;=\;
  -
  \psi^\beta_{,\mu_1 \cdots \mu_s}
  \psi^\alpha_{,\mu_1 \cdots \mu_r}
  \,.
$$

The  [[Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
of the _massless [[free field theory|free]] [[Dirac field]]_ on [[Minkowski spacetime]] is

$$
  \label{DiracFieldLagrangianMassless}
  \mathbf{L}
    \;\coloneqq\;
   \overline{\psi} \, \gamma^\mu \psi_{,\mu}\, dvol_\Sigma
   \,,
$$

given by the bilinear pairing $\overline{(-)}\Gamma(-)$ from prop. \ref{RealSpinorPairingsViaDivisionAlg}
of the field coordinate with its first spacetime derivative and
expressed here in two-component spinor field coordinates as in (eq:TwoComponentNotationForSpinorToVectorPairing), hence with the [[Dirac conjugate]] $\overline{\psi}$ (eq:DiracConjugate) on the left.

Specifically in [[spacetime]] [[dimension]] $p + 1 = 4$, the [[Lagrangian function]] for the _massive [[Dirac field]]_
of [[mass]] $m \in \mathbb{R}$ is

$$
  \begin{aligned}
    L
    & \coloneqq
    \underset{
      \text{kinetic term}
    }{
    \underbrace{
      i \, \overline{\psi} \, \gamma^\mu \, \psi_{,\mu}
    }
    }
    +
    \underset{
      \text{mass term}
    }{
    \underbrace{
      m \overline{\psi} \psi
    }}
  \end{aligned}
$$


This is naturally thought of as a collection of Lagrangians smoothly parameterized by the
[[metric]] $\eta$ and the [[mass]] $m$. For this to be [[physical unit]]-free in the sense of
remark \ref{ParameterizedLagrangianDensities} the [[physical unit]] of the parameter $m$ must be
that of the inverse metric, hence must be an inverse [[length]] according to remark \ref{MinkowskiMetricAndPhysicalUnitOfLength}
This is the _inverse [[Compton wavelength]]_  $\ell_m = \hbar / m c$ (eq:ComptonWavelength) and hence
the [[physical unit]]-free version of the Lagrangian density for the free Dirac field is

$$
  \mathbf{L}_{\eta,\ell_m}
    \;\coloneqq\;
  \ell_m
  \left(
    i \overline{\psi} \gamma^\mu \psi_{,\mu} + \left( \tfrac{m c}{\hbar} \right) \overline{\psi} \psi
  \right) dvol_\Sigma
  \,.
$$

=--

+-- {: .num_remark #RealityOfLagrangianDensityOfTheDiracField}
###### Remark
**([[real part|reality]] of the [[Lagrangian density]] of the [[Dirac field]])**

The kinetic term of the [[Lagrangian density]] for the [[Dirac field]] form def. \ref{LagrangianDensityForDiracField}
is a sum of two contributions, one for each [[chiral spinor]] component in the full [[Dirac spinor]] (remark \ref{TwoComponentSpinorNotation}):

$$
  \begin{aligned}
    i \overline{\psi} \gamma^\mu \psi_{,\mu}
    & =
    i
    \underset{
      -(\partial_\mu \xi^a ) \sigma^\mu_{a \dot c} \xi^{\dagger \dot c}
      + \partial_\mu(\chi^a \sigma^\mu_{a \dot c} \chi^{\dagger \dot c})
    }{
    \underbrace{
      \xi^a \sigma^\mu_{a \dot c} \partial_\mu \xi^{\dagger \dot c}
    }
    }
    +
    \xi^\dagger_{\dot a} \tilde \sigma^{\mu \dot a c} \partial_\mu \xi_c
    \\
    & =
    \xi^\dagger \tilde \sigma^\mu \partial_\mu \xi
    +
    \chi^\dagger \tilde \sigma^\mu \partial_\mu \chi
    +
    \partial_\mu(\xi \sigma^\mu \xi^\dagger)
  \end{aligned}
$$

Here the computation shown under the brace crucially uses that all these jet coordinates
for the Dirac field are anti-commuting, due to their [[supergeometry|supergeometric]] nature (eq:DiracFieldJetCoordinatesAnticommute).

Notice that a priori this is a function on the jet bundle with values in $\mathbb{K}$.
But in fact for $\mathbb{K} = \mathbb{C}$ it is real up to a [[total spacetime derivative]]:, because

$$
  \begin{aligned}
    \left(
      i \chi^\dagger \tilde \sigma^\mu  \partial_\mu\chi
    \right)^\dagger
    & =
    -i \left( \partial_\mu \chi\right)^\dagger \sigma^\mu \chi
    \\
    & =
    i \chi^\dagger \sigma^\mu \partial_\mu \chi + i \partial_\mu\left( \chi^\dagger \sigma^\mu \chi \right)
  \end{aligned}
$$

and similarly for $i \xi^\dagger \tilde \sigma^\mu  \partial_\mu\xi$

=--

(e.g. [Dermisek I-9](Dirac+field#DermisekI9))

$\,$

The beauty of [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) is that a choice of [[Lagrangian density]] determines
both the [[equations of motion]] of the fields as well as a [[presymplectic manifold|presymplectic structure]]
on the space of solutions to this equation (the "[[shell]]"), making it the "[[covariant phase space]]" of the theory.
All this we discuss [below](#PhaseSpace). But in fact all this key structure of the field theory is
nothing but the shadow (under "[[transgression of variational differential forms]]", def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces} below) of the following
simple relation in the [[variational bicomplex]]:


+-- {: .num_prop #EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}
###### Proposition
**([[Euler-Lagrange form]] and [[presymplectic current]])**

Given a [[Lagrangian density]] $\mathbf{L} \in \Omega^{p+1,0}_\Sigma(E)$ as in def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}, then its de Rham differential
$\mathbf{d}\mathbf{L}$, which by degree reasons equals $\delta \mathbf{L}$, has a _unique_ decomposition as a sum of two terms

$$
  \label{dLDecomposition}
  \mathbf{d} \mathbf{L}
  =
  \delta_{EL} \mathbf{L}
  -
  d \Theta_{BFV}
$$

such that $\delta_{EL}\mathbf{L}$ is proportional to the [[variational derivative]] of the fields (but not their derivatives, called a "[[source form]]"):

$$
  \delta_{EL} \mathbf{L}
    \;\in\;
  \Omega^{p+1,0}_{\Sigma}(E) \wedge \delta C^\infty(E)
    \;\subset\;
  \Omega^{p+1,1}_{\Sigma}(E)
  \,.
$$

The map

$$
   \delta_{EL} \;\colon\; \Omega^{p+1,0}_{\Sigma}(E) \longrightarrow \Omega^{p+1,0}_{\Sigma}(E) \wedge \delta \Omega^{0,0}_{\Sigma}(E)
$$

thus defined is called the _[[Euler-Lagrange operator]]_ and is explicitly given by the _[[Euler-Lagrange derivative]]_:

$$
  \label{EulerLagrangeEquationGeneral}
  \begin{aligned}
    \delta_{EL} L \, dvol_\Sigma
    & \coloneqq
    \frac{\delta_{EL} L}{\delta \phi^a}
    \delta \phi^a \wedge dvol_\Sigma
    \\
    & \coloneqq
    \left(
      \frac{\partial L}{\partial \phi^a}
      -
      \frac{d}{d x^\mu}
      \frac{\partial L}{\partial \phi^a_{,\mu}}
      +
      \frac{d^2}{d x^{\mu_1} d x^{\mu_2}}
      \frac{\partial L}{\partial \phi^a_{\mu_1, \mu_2}}
      -
      \cdots
    \right)
    \delta \phi^a
    \wedge
    dvol_\Sigma
    \,.
  \end{aligned}
$$

The [[smooth space|smooth subspace]] of the [[jet bundle]] on which the [[Euler-Lagrange form]]
vanishes

$$
  \label{ShellInJetBundle}
  \mathcal{E}
   \;\coloneqq\;
  \left\{
    x \in J^\infty_\Sigma(E)
    \;\vert\;
    \delta_{EL}\mathbf{L}(x) = 0
  \right\}
  \;\overset{i_{\mathcal{E}}}{\hookrightarrow}\;
  J^\infty_\Sigma(E)
  \,.
$$

is called the _[[shell]]_. The smaller subspace on which also all [[total spacetime derivatives]]
vanish (the "[[formally integrable PDE|formally integrable prolongation]]")
is the _prolonged [[shell]]_

$$
  \label{ProlongedShellInJetBundle}
  \mathcal{E}^\infty
   \;\coloneqq\;
  \left\{
    x \in J^\infty_\Sigma(E)
    \;\vert\;
    \left(
      \frac{d^k}{d x^{\mu_1} \cdots d x^{\mu_k}}
      \delta_{EL}\mathbf{L}
    \right)(x) = 0
  \right\}
   \overset{i_{\mathcal{E}^\infty}}{\hookrightarrow}
  J^\infty_\Sigma(E)
  \,.
$$

Saying something holds  "[[on-shell]]" is to mean that it holds after restriction to this
subspace. For example a [[variational differential form]] $\alpha \in \Omega^{\bullet,\bullet}_\Sigma(E)$
is said to _vanish on shell_ if $\alpha\vert_{\mathcal{E}^\infty} = 0$.


The remaining term $d \Theta_{BFV}$ in (eq:dLDecomposition) is unique, while the _presymplectic potential_

$$
  \label{PresymplecticPotential}
  \Theta_{BFV} \in \Omega^{p,1}_{\Sigma}(E)
$$

is not unique.

(For a [[field bundle]] which is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}
over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}), prop. \ref{HorizontalVariationalComplexOfTrivialFieldBundleIsExact} says
that $\Theta_{BFV}$ is unique up to addition of total spacetime derivatives $d \kappa$, for $\kappa \in \Omega^{p-1,1}_\Sigma(E)$.)

One possible choice for the presymplectic current $\Theta_{BFV}$ is

$$
  \label{StandardThetaForTrivialVectorFieldBundleOnMinkowskiSpacetime}
  \begin{aligned}
    \Theta_{BFV}
    & \coloneqq \phantom{+}
      \frac{\partial L}{\partial \phi^a_{,\mu}}
      \delta \phi^a
      \; \wedge \iota_{\partial_\mu} dvol_\Sigma
    \\
    & \phantom{=}
      +
      \left(
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}}
        \delta \phi^a_{,\nu}
        -
        \frac{d}{d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu \nu}}
        \delta \phi^a_{,\mu}
      \right)
    \wedge \iota_{\partial_\mu} dvol_\Sigma
    \\
    & \phantom{=} + \cdots
  \,,
  \end{aligned}
$$

where

$$
  \iota_{\partial_{\mu}} dvol_\Sigma
  \;\coloneqq\;
  (-1)^{\mu} d x^0 \wedge \cdots d x^{\mu-1} \wedge d x^{\mu+1} \wedge \cdots \wedge d x^p
$$

denotes the contraction (def. \ref{ContractionOfFormsWithVectorFields}) of the [[volume form]] with the [[vector field]] $\partial_\mu$.

The [[vertical derivative]] of a chosen presymplectic potential $\Theta_{BFV}$ is called a _[[pre-symplectic current]]_ for $\mathbf{L}$:

$$
  \label{PresymplecticCurrent}
  \Omega_{BFV}
   \;\coloneqq\;
   \delta \Theta_{BFV} \;\;\; \in \Omega^{p,2}_{\Sigma}(E)
  \,.
$$

Given a choice of $\Theta_{BFV}$ then the sum

$$
  \label{TheLepage}
  \mathbf{L} + \Theta_{BFV} \;\in\; \Omega^{p+1,0}_\Sigma(E) \oplus \Omega^{p,1}_\Sigma(E)
$$

is called the corresponding _[[Lepage form]]_. Its de Rham derivative is the sum of
the Euler-Lagrange variation and the presymplectic current:

$$
  \label{DerivativeOfLepageForm}
  \mathbf{d}( \mathbf{L} + \Theta_{BFV} )
  \;=\;
  \delta_{EL} \mathbf{L} + \Omega_{BFV}
  \,.
$$

(Its conceptual nature will be elucidated after the introduction of the [[local BV-complex]]
in example \ref{DerivedPresymplecticCurrentOfRealScalarField} below.)

=--


+-- {: .proof}
###### Proof

Using $\mathbf{L} = L dvol_\Sigma$ and that $d \mathbf{L} = 0$ by degree reasons (example \ref{BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle}), we find

$$
  \begin{aligned}
    \mathbf{d}\mathbf{L}
    & =
    \left(
      \frac{\partial L}{\partial \phi^a} \delta \phi^a
      +
      \frac{\partial L}{\partial \phi^a_{,\mu}} \delta \phi^a_{,\mu}
      +
      \frac{\partial L}{\partial \phi^a_{,\mu_1 \mu_2}} \delta \phi^a_{,\mu_1 \mu_2}
      +
      \cdots
    \right)
    \wedge dvol_{\Sigma}
  \end{aligned}
  \,.
$$

The idea now is to have $d \Theta_{BFV}$ pick up those terms that would appear as [[boundary]] terms under the [[integral]]
$\int_\Sigma j^\infty_\Sigma(\Phi)^\ast \mathbf{d}L$ if we were to consider [[integration by parts]] to remove
spacetime derivatives of $\delta \phi^a$.

We compute, using example \ref{BasicFactsAboutVarationalCalculusOnJetBundleOfTrivialVectorBundle},
the total horizontal derivative of $\Theta_{BFV}$ from (eq:StandardThetaForTrivialVectorFieldBundleOnMinkowskiSpacetime) as follows:

$$
  \begin{aligned}
    d \Theta_{BFV}
    & =
    \left(
      d
      \left(
        \frac{\partial L}{\partial \phi^a_{,\mu}}
        \delta \phi^a
      \right)
      +
      d
      \left(
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}}
        \delta \phi^a_{,\nu}
        -
        \frac{d}{d x^\nu} \frac{\partial L}{\partial \phi^a_{\mu \nu}}
        \delta \phi^a
      \right)
      +
      \cdots
  \right)
  \wedge \iota_{\partial_\mu} dvol_\Sigma
  \\
    & =
    \left(
      \left(
        \left(
           d \frac{\partial L}{\partial \phi^a_{,\mu}}
        \right) \wedge  \delta \phi^a
        -
        \frac{\partial L}{\partial \phi^a_{,\mu}} \delta d \phi^a
      \right)
      +
      \left(
        \left(d \frac{\partial L}{\partial \phi^a_{,\nu \mu}}\right) \wedge \delta \phi^a_{,\nu}
        -
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}} \delta d \phi^a_{,\nu}
        -
        \left( d \frac{d}{d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu \nu}} \right) \wedge
        \delta \phi^a
        +
        \frac{d}{d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu \nu}}
        \delta d \phi^a
      \right)
          +
      \cdots
    \right)
    \wedge \iota_{\partial_\mu} dvol_\Sigma
    \\
    & =
    -
    \left(
      \left(
        \frac{d}{d x^\mu} \frac{\partial L}{\partial \phi^a_{,\mu}}
        \delta \phi^a
        +
        \frac{\partial L}{\partial \phi^a_{,\mu}}
        \delta \phi^a_{,\mu}
      \right)
      +
      \left(
        \frac{d}{d x^\mu}
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}}
        \delta \phi^a_{,\nu}
        +
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}}
        \delta \phi^a_{,\nu \mu}
        -
        \frac{d^2}{ d x^\mu d x^\nu}
        \frac{\partial L}{\partial \phi^a_{,\mu \nu}}
        \delta \phi^a
        -
        \frac{d}{d x^\nu}
        \frac{\partial L}{\partial \phi^a_{,\mu \nu}}
        \delta \phi^a_{,\mu}
      \right)
      + \cdots
    \right)
    \wedge dvol_\Sigma
    \,,
  \end{aligned}
$$

where in the last line we used that

$$
  d x^{\mu_1} \wedge \iota_{\partial_{\mu_2}} dvol_\Sigma
  =
  \left\{
    \array{
      dvol_\Sigma &\vert& \text{if}\, \mu_1 = \mu_2
      \\
      0 &\vert& \text{otherwise}
    }
  \right.
$$

Here the two terms proportional to $\frac{d}{d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu \nu}} \delta \phi^a_{,\mu}$
cancel out, and we are left with

$$
  d \Theta_{BFV}
  \;=\;
    -
      \left(
        \frac{d}{d x^\mu} \frac{\partial L}{\partial \phi^a_{,\mu}}
        -
        \frac{d^2}{ d x^\mu d x^\nu}
        \frac{\partial L}{\partial \phi^a_{,\mu \nu}}
        +
        \cdots
      \right)
      \delta \phi^a \wedge dvol_\Sigma
        -
      \left(
        \frac{\partial L}{\partial \phi^a_{,\mu}}
        \delta \phi^a_{,\mu}
        +
        \frac{\partial L}{\partial \phi^a_{,\nu \mu}}
        \delta \phi^a_{,\nu \mu}
        +
        \cdots
      \right)
      \wedge dvol_\Sigma
$$


Hence $-d \Theta_{BFV}$ shares with $\mathbf{d} \mathbf{L}$ the terms that are proportional to
$\delta \phi^a_{,\mu_1 \cdots \mu_k}$ for $k \geq 1$,
and so the remaining terms are proportional to $\delta \phi^a$, as claimed:

$$
  \mathbf{d}L + d \Theta_{BFV}
  =
  \underset{
    = \delta_{EL}\mathbf{L}
  }{
  \underbrace{
  \left(
    \frac{\partial L}{\partial \phi^a}
    -
    \frac{d}{d x^\mu}\frac{\partial L}{\partial \phi^a_{,\mu}}
    +
    \frac{d^2}{d x^\mu d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu\nu}}
    +
    \cdots
  \right)
  \delta \phi^a \wedge dvol_\Sigma
  }}
  \,.
$$


=--


The following fact is immediate from prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime},
but of central importance, we futher amplify this in remark \ref{PresymplecticCurrentInterpretation} below:


+-- {: .num_prop #HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell}
###### Proposition
**([[total derivative|total spacetime derivative]] of [[presymplectic current]] vanishes [[on-shell]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).
Then the [[Euler-Lagrange form]] $\delta_{EL} \mathbf{L}$ and the [[presymplectic current]]
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) are related by

$$
  d \Omega_{BFV} = - \delta(\delta_{EL}\mathbf{L})
  \,.
$$

In particular this means that restricted to the prolonged shell $\mathcal{E}^\infty \hookrightarrow J^\infty_\Sigma(E)$ (eq:ProlongedShellInJetBundle) the total spacetime derivative of the [[presymplectic current]] vanishes:

$$
  \label{HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell}
  d \Omega_{BFV} \vert_{\mathcal{E}^\infty} \;=\; 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime} we have

$$
  \delta \mathbf{L} = \delta_{EL} \mathbf{L} - d \Theta_{BFV}
  \,.
$$

The claim follows from applying the [[variational derivative]] $\delta$ to both sides,
using (eq:HorizontalAndVerticalDerivativeAnticommute): $\delta^2 = 0$ and $\delta \circ d = - d \circ \delta$.

=--



Many examples of interest fall into the following two special cases of prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}:

+-- {: .num_prop #ShellForSpacetimeIndependentLagrangians}
###### Example
**([[Euler-Lagrange form]] for [[spacetime]]-independent [[Lagrangian densities]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] $E \simeq \Sigma \times F$ over [[Minkowski spacetime]] $\Sigma$
(example \ref{TrivialVectorBundleAsAFieldBundle}).

In general the [[Lagrangian density]] $\mathbf{L}$ is a function of all the spacetime and field coordinates

$$
  \mathbf{L} = L((x^\mu), (\phi^a), (\phi^a_{,\mu}), \cdots) dvol_\Sigma
  \,.
$$

Consider the special case that $\mathbf{L}$ is _[[spacetime]]-independent_ in that the Lagrangian funtion $L$
is independent of the spacetime coordinate $(x^\mu)$.
Then the same evidently holds for the [[Euler-Lagrange form]] $\delta_{EL}\mathbf{L}$
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}).
Therefore in this case the [[shell]] (eq:ProlongedShellInJetBundle) is itself a [[trivial bundle]] over spacetime.

In this situation every point $\varphi$ in the jet fiber defines a constant section of the shell:

$$
  \label{ConstantSectionOfTrivialShellBundle}
  \Sigma \times \{\varphi\} \subset \mathcal{E}^\infty
  \,.
$$


=--


+-- {: .num_example #CanonicalMomentum}
###### Example
**([[canonical momentum]])**

Consider a [[Lagrangian field theory]] $(E, \mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) whose [[Lagrangian density]] $\mathbf{L}$

1. does not depend on the [[spacetime]]-[[coordinates]] (example \ref{ShellForSpacetimeIndependentLagrangians});

1. depends on spacetime derivatives of [[field (physics)|field]] coordinates (hence on [[jet bundle]] coordinates) at most to first order.

Hence if the [[field bundle]] $E \overset{fb}{\to} \Sigma$ is a [[trivial vector bundle]] over [[Minkowski spacetime]] (example \ref{TrivialVectorBundleAsAFieldBundle}) this means to consider the case that

$$
  \mathbf{L}
    \;=\;
   L\left(
     (\phi^a), (\phi^a_{,\mu})
   \right) \wedge dvol_\Sigma
  \,.
$$

Then the [[presymplectic current]] (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) is (up to possibly a horizontally exact part) of the form

$$
  \label{CanonicalMomentumPresymplecticCurrent}
  \Omega_{BFV}
   \;=\;
  \delta p_a^\mu
  \wedge
  \delta \phi^a
  \wedge
  \iota_{\partial_\mu} dvol_\Sigma
$$

where

$$
  \label{CanonicalMomentumInCoordinates}
  p_a^\mu
    \;\coloneqq\;
  \frac{\partial L}{ \partial \phi^a_{,\mu}}
$$

denotes the [[partial derivative]] of the [[Lagrangian density|Lagrangian function]] with respect to the spacetime-[[derivatives]] of the [[field (physics)|field]] [[coordinates]].

Here

$$
  \begin{aligned}
    p_a
      & \coloneqq
    p_a^0
    \\
      & =
    \frac{\partial L}{\partial \phi^a_{,0}}
  \end{aligned}
$$

is called the _[[canonical momentum]]_ corresponding to the "[[canonical coordinate|canonical field coordinate]]" $\phi^a$.

In the language of [[multisymplectic geometry]] the full expression

$$
  p_a^\mu \wedge \iota_{\partial_\mu} dvol_\Sigma
  \;\in\;
  \Omega^{p,1}_\Sigma(E)
$$

is also called the "canonical multi-momentum", or similar.

=--

+-- {: .proof}
###### Proof

We compute:

$$
  \begin{aligned}
    \mathbf{d} \mathbf{L}
    & =
    \left(
      \frac{\partial L}{\partial \phi^a} \delta \phi^a
      +
      \frac{\partial L}{\partial \phi^a_{,\mu}} \delta \phi^a_{,\mu}
    \right)
    \delta \phi^a
    \wedge
    dvol_\Sigma
    \\
    & =
    \left(
      \frac{\partial L}{\partial \phi^a}
      -
      \frac{d}{d x^\mu} \frac{\partial L}{\partial \phi^a_{,\mu}}
    \right)
    \wedge
    dvol_\Sigma
    -
    d
    \underset{
      \Theta_{BFV}
    }{
    \underbrace{
      \left(
        \frac{\partial L}{\partial \phi^a_{,\mu}} \delta \phi^a
      \right)
      \wedge
      \iota_{\partial_\mu} dvol_\Sigma
    }
    }
  \end{aligned}
  \,.
$$

Hence

$$
  \begin{aligned}
    \Omega_{BFV}
    & \coloneqq
    \delta \Theta_{BFV}
    \\
    & =
    \delta
    \left(
      \frac{\partial L}{\partial \phi^a_{,\mu}}
      \delta \phi^a_{,\mu}
      \wedge \iota_{\partial_\mu} dvol_\Sigma
    \right)
    \\
    & =
     \delta
      \frac{\partial L}{\partial \phi^a_{,\mu}}
     \wedge
      \delta \phi^a_{,\mu}
      \wedge
      \iota_{\partial_\mu} dvol_\Sigma
    \\
    & =
    \delta p_a^\mu \wedge \delta \phi^a \wedge \iota_{\partial_\mu} dvol_\Sigma
  \end{aligned}
$$

=--


+-- {: .num_remark #PresymplecticCurrentInterpretation}
###### Remark
**([[presymplectic current]] is local version of ([[presymplectic form|pre-]])[[symplectic form]] of [[Hamiltonian mechanics]])**

In the simple but very common situation of example \ref{CanonicalMomentum} the [[presymplectic current]] (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) takes the form (eq:CanonicalMomentumInCoordinates)

$$
  \Omega_{BFV}
   \;=\;
  \delta p_a^\mu
  \wedge
  \delta \phi^a
  \wedge
  \iota_{\partial_\mu} dvol_\Sigma
$$

with $\phi^a$ the [[field (physics)|field]] [[coordinates]] ("[[canonical coordinates]]")
and $p_a^\mu$ the "[[canonical momentum]]" (eq:CanonicalMomentumInCoordinates).

Notice that this is of the schematic form "$(\delta p_a \wedge \delta q^a) \wedge dvol_{\Sigma_p}$",
which is reminiscent of the wedge product of a [[symplectic form]] expressed in [[Darboux coordinates]] with
a [[volume form]] for a $p$-dimensional [[manifold]]. Indeed, below in _[Phase space](#PhaseSpace)_
we discuss that this [[presymplectic current]]  "[[transgression of variational differential forms|transgresses]]" (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces} below)
to a [[presymplectic form]] of the schematic form "$d P_a \wedge d Q^a$" on the [[on-shell]] [[space of field histories]] (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime})
by [[integration of differential forms|integrating]] it over a [[Cauchy surface]] of [[dimension]] $p$. In good situations
this [[presymplectic form]] is in fact a [[symplectic form]] on the [[on-shell]] [[space of field histories]] (theorem \ref{PPeierlsBracket} below).

This shows that the [[presymplectic current]] $\Omega_{BFV}$ is the [[local field theory|local]] (i.e. [[jet bundle|jet level]]) avatar of the
[[symplectic form]] that governs the formulation of [[Hamiltonian mechanics]] in terms of [[symplectic geometry]].

In fact prop. \ref{HorizontalDerivativeOfPresymplecticCurrentVanishesOnShell} may be read as saying that
the [[presymplectic current]] is a _[[conserved current]]_ (def. \ref{SymmetriesAndConservedCurrents} below),
only that it takes values not in [[smooth functions]] of the field coordinates and jets, but in
[[variational differential form|variational 2-forms]] on fields. There is a [[conserved charge]] associated with
every [[conserved current]] (prop. \ref{ConservedCharge} below) and the conserved charge associated with the
[[presymplectic current]] is the ([[presymplectic form|pre-]])[[symplectic form]] on the [[phase space]]
of the field theory (def. \ref{PhaseSpaceAssociatedWithCauchySurface} below).

=--

+-- {: .num_example #FreeScalarFieldEOM}
###### Example
**([[Euler-Lagrange form]] and [[presymplectic current]] for [[free field|free]] [[real scalar field]])**

Consider the [[Lagrangian field theory]] of the [[free field|free]] [[real scalar field]]
from example  \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}.

Then the [[Euler-Lagrange operator|Euler-Lagrange form]] and [[presymplectic current]]
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) are

$$
  \label{RealScalarFieldLEForm}
  \delta_{EL}\mathbf{L}
  \;=\;
  \left(\eta^{\mu \nu} \phi_{,\mu \nu} - m^2 \right) \delta \phi \wedge dvol_\sigma
  \;\in\;
  \Omega^{p+1,1}_{\Sigma}(E)
  \,.
$$

and

$$
  \Omega_{BFV}
  \;=\;
  \left(\eta^{\mu \nu} \delta \phi_{,\mu} \wedge \delta \phi \right) \wedge \iota_{\partial_\nu} dvol_{\Sigma}
  \;\in\;
  \Omega^{p,2}_{\Sigma}(E)
  \,,
$$

respectively.

=--

+-- {: .proof}
###### Proof

This is a special case of example \ref{CanonicalMomentum}, but we spell it out in detail again:

We need to show that [[Euler-Lagrange operator]] $\delta_{EL} \colon \Omega^{p+1,0}(\Sigma) \to \Omega^{p+1,1}_S(\Sigma)$ takes the [[local Lagrangian density]] for the [[free field|free]] [[scalar field]] to

$$
  \delta_EL L
  \;=\;
  \left(
    \eta^{\mu \nu} \phi_{,\mu \nu} - m^2 \phi
  \right)
  \delta \phi \wedge \mathrm{dvol}_\Sigma
  \,.
$$

First of all, using just the [[variational derivative]] ([[vertical derivative]]) $\delta$ is a graded [[derivation]],
the result of applying it to the local Lagrangian density is

$$
  \delta L
    \;=\;
  \left(
    \eta^{\mu \nu} \phi_{,\mu} \delta \phi_{,\nu}
      -
    m^2 \phi \delta \phi
  \right)
  \wedge \mathrm{dvol}_\Sigma
  \,.
$$

By definition of the [[Euler-Lagrange operator]], in order to find $\delta_{EL}\mathbf{L}$ and $\Theta_{BFV}$, we need to exhibit this as the
sum of the form $(-) \wedge \delta \phi  - d \Theta_{BFV}$.

The key to find $\Theta_{BFV}$ is  to realize $\delta \phi_{,\nu}\wedge \mathrm{dvol}_\Sigma$ as a
[[total derivative|total spacetime derivative]] ([[horizontal derivative]]). Since $d \phi = \phi_{,\mu} d x^\mu$ this is accomplished by

$$
  \delta \phi_{,\nu} \wedge \mathrm{dvol}_\Sigma
  =
  \delta d \phi \wedge \iota_{\partial_\nu} \mathrm{dvol}_\Sigma
  \,,
$$

where on the right we have the contraction (def. \ref{ContractionOfFormsWithVectorFields}) of the [[tangent vector field]]
along $x^\nu$ into the [[volume form]].

Hence we may take the presymplectic potential (eq:PresymplecticPotential) of the free scalar field to be

$$
  \label{PresymplecticPotentialOfFreeScalarField}
  \Theta_{BFV}
    \coloneqq
  \eta^{\mu \nu} \phi_{,\mu} \delta \phi \wedge \iota_{\partial_\nu}
  \mathrm{dvol}_\Sigma
  \,,
$$

because with this we have

$$
  d \Theta_{BFV}
  =
  \eta^{\mu \nu}
  \left(
    \phi_{,\mu \nu} \delta \phi
    -
    \eta^{\mu \nu} \phi_{,\mu} \delta \phi_{,\nu}
  \right) \wedge \mathrm{dvol}_\Sigma
  \,.
$$

In conclusion this yields the decomposition of the vertical differential of the Lagrangian density

$$
  \delta L
  =
  \underset{
    = \delta_{EL} \mathcal{L}
  }{
  \underbrace{
    \left(
      \eta^{\mu \nu} \phi_{,\mu \nu}  - m^2 \phi
    \right)
    \delta \phi \wedge \mathrm{dvol}_\Sigma
  }
  }
  -
  d \Theta_{BFV}
  \,,
$$

which shows that $\delta_{EL} L$ is as claimed, and that $\Theta_{BFV}$ is a presymplectic potential current (eq:PresymplecticPotential).
Hence the presymplectic current itself is

$$
  \begin{aligned}
    \Omega_{BFV} &\coloneqq \delta \Theta_{BFV}
    \\
    & =
    \delta \left( \eta^{\mu \nu} \phi_{,\mu} \delta \phi \wedge \iota_{\partial_\nu} \mathrm{dvol}_\Sigma \right)
    \\
    & =
    \left(\eta^{\mu \nu} \delta \phi_{,\mu} \wedge \delta \phi \right) \wedge \iota_{\partial_\nu} dvol_{\Sigma}
  \end{aligned}
  \,.
$$

=--


+-- {: .num_example #ElectromagnetismEl}
###### Example
**([[Euler-Lagrange form]] for [[free field|free]] [[electromagnetic field]])**

Consider the [[Lagrangian field theory]] of [[free field|free]] [[electromagnetism]] from example \ref{ElectromagnetismLagrangianDensity}.

The [[Euler-Lagrange variational derivative]] is

$$
  \delta_{EL} \mathbf{L}
  \;=\;
  f^{\mu \nu}_{,\mu} \delta a_\nu
  \,.
$$

Hence the [[shell]] (eq:ShellInJetBundle) in this case is

$$
  \mathcal{E}
    =
  \Sigma \times
  \left\{
    \left(
       (a_\mu) , (a_{\mu,\mu_1}), (a_{\mu,\mu_1 \mu_2}), \cdots
     \right)
     \;\vert\;  f^{\mu \nu}{}_{,\mu} = 0 \right\}
  \;\subset\;
  J^\infty_\Sigma(T^\ast \Sigma)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By (eq:EulerLagrangeEquationGeneral) we have

$$
  \begin{aligned}
    \frac{\delta_{EL} L}{\delta a_\mu} \delta a_\mu
    & =
    \left(
      \underset{
        = 0
      }{
      \underbrace{
        \frac{\partial}{\partial a_\mu}
        \tfrac{1}{2} a_{[\mu,\nu]} a^{[\mu,\nu]}
      }
      }
      -
      \frac{d}{d x^\rho}
      \frac{\partial}{\partial a_{\alpha,\rho}}
      \tfrac{1}{2} a_{[\mu,\nu]} a^{[\mu,\nu]}
    \right)
    \delta a_\alpha
    \\
    & =
      -
      \tfrac{1}{2}
     \left(
      \frac{d}{d x^\rho}
      \frac{\partial}{\partial a_{\alpha,\rho}}
      a_{\mu,\nu} a^{[\mu,\nu]}
    \right)
    \delta a_\alpha
    \\
    & =
    -
    \left(
      \frac{d}{d x^\rho}
      a^{[\alpha,\rho]}
    \right)
    \delta a_{\alpha}
    \\
    & =
    - f^{\mu \nu}{}_{,\mu} \delta a_{\nu}
    \,.
  \end{aligned}
$$

=--

More generally:


+-- {: .num_example #YangMillsOnMinkowskiEl}
###### Example
**([[Euler-Lagrange form]] for [[Yang-Mills theory]] on [[Minkowski spacetime]])**

Let $\mathfrak{g}$ be a [[semisimple Lie algebra]]
and consider the [[Lagrangian field theory]] $(E,\mathbf{L})$ of $\mathfrak{g}$-[[Yang-Mills theory]] from example \ref{YangMillsLagrangian}.

Its [[Euler-Lagrange form]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) is

$$
  \begin{aligned}
  \delta_{EL}\mathbf{L}
  & =
  \left(
    f^{\mu \nu \alpha}_{,\mu} + \gamma^\alpha{}_{\beta \gamma} a_\mu^\beta f^{\mu \nu \gamma}
  \right)
  k_{\alpha \beta}
  \,\delta a_\mu^\beta
  \, dvol_\Sigma
  \,,
  \end{aligned}
$$

where

$$
  f^\alpha_{\mu \nu}
  \;\in\;
  \Omega^{0,0}_\Sigma(E)
$$

is the universal [[Yang-Mills theory|Yang-Mills]] [[field strength]] (eq:YangMillsJetFieldStrengthMinkowski).

=--


+-- {: .proof}
###### Proof

With the explicit form (eq:EulerLagrangeEquationGeneral) for the [[Euler-Lagrange derivative]] we compute as follows:

$$
  \begin{aligned}
    \delta_{EL}
    \left(
      \tfrac{1}{2}
      k_{\alpha \beta} f^\alpha_{\mu\nu} f^{\beta \mu \nu}
    \right)
    & =
    \left(
    \left(
      \frac{\partial}{\partial a_{\mu'}^{\alpha'}}
      \left(
        a_{\nu,\mu}^\alpha
        +
        \tfrac{1}{2}
        \gamma^{\alpha}{}_{\alpha_2 \alpha_3}
        a_{\mu}^{\alpha_2} a_\nu^{\alpha_3}
      \right)
    \right)
    k_{\alpha \beta}
    f^{\beta \mu \nu}
    -
    \left(
      \frac{d}{d x^{\nu'}}
      \frac{\partial}{\partial a_{\mu',\nu'}^{\alpha'}}
      \left(
        a_{\nu,\mu}^\alpha
        +
        \tfrac{1}{2}
        \gamma^{\alpha}{}_{\alpha_2 \alpha_3}
        a_{\mu}^{\alpha_2} a_\nu^{\alpha_3}
      \right)
    \right)
    k_{\alpha \beta}
    f^{\beta \mu \nu}
    \right)
    \delta a_{\mu'}^{\alpha'}
    \\
    & =
    \gamma^{\alpha}{}_{\alpha' \alpha_3} a_\nu^{\alpha_3}
    f^{\beta \mu \nu}
    k_{\alpha \beta}
    \delta a_{\mu}^{\alpha'}
    -
    \left(
      \frac{d}{d x^{\mu}} f^{\beta \mu \nu}
    \right)
    k_{\alpha \beta}
    \delta a_{\nu}^{\alpha}
    \\
    &=
    -
    \left(
      f^{\alpha \mu \nu}_{,\mu}
      +
      \gamma^\alpha{}_{\beta \gamma} a_\mu^\beta f^{\gamma \mu \nu}
    \right)
    k_{\alpha \beta}
    \delta a_\nu^\beta
  \end{aligned}
$$

In the last step we used that for a [[semisimple Lie algebra]] $\gamma_{\alpha \beta \gamma} \coloneqq k_{\alpha \alpha'} \gamma^{\alpha'}{}_{\beta \gamma}$ is totally skew-symmetric in its indices (this being the coefficients of the [[Lie algebra cocycle]])
which is in transgression with the [[Killing form]] [[invariant polynomial]] $k$.

=--


+-- {: .num_example #EulerLagrangeFormBField}
###### Example
**([[Euler-Lagrange form]] of [[free field|free]] [[B-field]])**

Consider the [[Lagrangian field theory]] of the [[free field|free]] [[B-field]] from example \ref{BField}.

The [[Euler-Lagrange variational derivative]] is

$$
  \delta_{EL} \mathbf{L}
  \;=\;
  h^{\mu \nu \rho}{}_{,\rho} \delta b_{\mu \nu}
  \,,
$$

where $h_{\mu_1 \mu_2 \mu_3}$ is the universal [[B-field|B-]][[field strength]] from example \ref{BFieldJetFaraday}.

=--

+-- {: .proof}
###### Proof

By (eq:EulerLagrangeEquationGeneral) we have

$$
  \begin{aligned}
    \frac{\delta_{EL} L}{\delta b_{\mu \nu}} \delta b_{\mu \nu}
    & =
    \left(
      \underset{
        = 0
      }{
      \underbrace{
        \frac{\partial}{\partial b_{\mu \nu}}
        \tfrac{1}{2} b_{[\mu_1 \mu_2, \mu_3]} b^{[\mu_1 \mu_2, \mu_3]}
      }
      }
      -
      \frac{d}{d x^\rho}
      \frac{\partial}{\partial b_{\mu \nu, \rho}}
        \tfrac{1}{2} b_{[\mu_1 \mu_2, \mu_3]} b^{[\mu_1 \mu_2, \mu_3]}
    \right)
    \delta b_{\mu \nu}
    \\
    & =
    -
    \left(
      \frac{d}{d x^\rho}
      \frac{\partial}{\partial b_{\mu \nu, \rho}}
        \tfrac{1}{2} b_{\mu_1 \mu_2, \mu_3} b^{[\mu_1 \mu_2, \mu_3]}
    \right)
    \delta b_{\mu \nu}
    \\
    & =
    -
    \left(
      \frac{d}{d x^\rho}
      b^{[\mu \nu, \rho]}
    \right)
    \delta b_{\mu \nu}
    \\
    & =
    -
    h^{\mu \nu \rho}{}_{,\rho} \delta b_{\mu \nu}
    \,.
  \end{aligned}
$$


=--


+-- {: .num_example #PresymplecticCurrentDiracField}
###### Example
**([[Euler-Lagrange form]] and [[presymplectic current]] of [[Dirac field]])**

Consider the [[Lagrangian field theory]] of the [[Dirac field]] on [[Minkowski spacetime]] of [[dimension]] $p + 1 \in \{3,4,6,10\}$ (example \ref{LagrangianDensityForDiracField}).

Then

* the [[Euler-Lagrange variational derivative]] (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) in the case of vanishing [[mass]] $m$ is

  $$
    \delta_{EL} \mathbf{L}
    \;=\;
    2 i\,
    \overline{\delta \psi}
    \,\gamma^\mu\, \psi_{,\mu}
    \,
    \wedge dvol_\Sigma
  $$

  and in the case that [[spacetime]] [[dimension]] is $p +1 = 4$ and arbitrary [[mass]] $m\in \mathbb{R}$, it is

  $$
    \delta_{EL} \mathbf{L}
     \;=\;
     \left(
       \overline{\delta \psi}
       \left(
          i \gamma^\mu \psi_{,\mu} + m \psi
       \right)
       +
       \left(
         - i \gamma^\mu\overline{\psi_{,\mu}} + m \overline{\psi}
       \right)
       (\delta \psi)
     \right)
     \,
     dvol_\Sigma
  $$


* its [[presymplectic current]] (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) is

  $$
    \Omega_{BFV}
    \;=\;
    \overline{\delta \psi}\,\gamma^\mu \,\delta \psi \, \iota_{\partial_\mu} dvol_\Sigma
  $$


=--


+-- {: .proof}
###### Proof

In any case the [[canonical momentum]] of the [[Dirac field]] according to example \ref{CanonicalMomentum} is

$$
  \begin{aligned}
    p^\alpha_\mu
    & \coloneqq
    \frac{\partial }{\partial \psi^\alpha_{,\mu}}
    \left(
      i \overline {\psi} \, \gamma^\nu \, \psi_{,\nu}
      +
      m \overline{\psi} \psi
    \right)
    \\
    & =
    \overline{\psi}^\beta (\gamma^\mu)_\beta{}^\alpha
  \end{aligned}
$$

This yields the [[presymplectic current]] as claimed, by example \ref{CanonicalMomentum}.

Now regarding the [[Euler-Lagrange form]], first consider the massless case in spacetime dimension $p+1 \in \{3,4,6,10\}$, where

$$
  L
  \;=\;
  i \overline{\psi} \, \gamma^\mu \, \psi_{,\mu}
  \,.
$$

Then we compute as follows:

$$
  \begin{aligned}
    \delta_{EL} L
    & =
    i \,\overline{\delta \psi} \, \gamma^\mu \, \psi_{,\mu}
    \underset{
      = +
      i \,\overline{\delta \psi} \, \gamma^\mu \, \psi_{,\mu}
    }{
    \underbrace{
    -
    i \overline{\psi_{,\mu}} \, \gamma^\mu \, \delta \psi
    }
    }
    \\
    & =
    2 i \, \overline{\delta \psi} \, \gamma^\mu \, \psi_{,\mu}
  \end{aligned}
$$

Here the first equation is the general formula (eq:EulerLagrangeEquationGeneral) for the Euler-Lagrange variation, while the identity under the braces combines two facts (as in remark \ref{LagrangianDensityOfDiracFieldSupergeometricNature} above):

1. the symmetry (eq:SpinorToVectorPairingIsSymmetric) of the spinor pairing $\overline{(-)}\gamma^\mu(-)$ (prop. \ref{RealSpinorPairingsViaDivisionAlg});

1. the anti-commutativity (eq:DiracFieldJetCoordinatesAnticommute) of the Dirac field and jet coordinates, due to their [[supergeometry|supergeometric]] nature (remark \ref{DiracFieldSupergeometric}).

Finally in the special case of the massive Dirac field in spacetime dimension $p+1 = 4$ the Lagrangian function is

$$
  L
  \;=\;
  i \, \overline{\psi} \gamma^\mu \psi_{,\mu} + m \overline{\psi}\psi
$$

where now $\psi_\alpha$ takes values in the [[complex numbers]] $\mathbb{C}$ (as opposed to in $\mathbb{R}$, $\mathbb{H}$ or $\mathbb{O}$). Therefore we may now form the [[derivative]] equivalently by treeating $\psi$ and $\overline{\psi}$ as independent components of the field. This immediately yields the claim.

=--


+-- {: .num_example #TrivialLagrangianDensities}
###### Example
**(trivial [[Lagrangian densities]] and the [[Euler-Lagrange complex]])**

If a [[Lagrangian density]] $\mathbf{L}$ (def. \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime})
is in the image of the [[total spacetime derivative]], hence horizontally exact (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime})

$$
  \mathbf{L} \;=\; d \mathbf{\ell}
$$

for any $\mathbf{\ell} \in \Omega^{p,0}_\Sigma(E)$, then both its [[Euler-Lagrange form]] as well as its [[presymplectic current]]
(def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) vanish:

$$
  \delta_{EL}\mathbf{L} = 0
  \phantom{AA}
  \,,
  \phantom{AA}
  \Omega_{BFV} = 0
  \,.
$$

This is because with $\delta \circ d = - d \circ \delta$ (eq:HorizontalAndVerticalDerivativeAnticommute) the defining unique decomposition (eq:dLDecomposition) of $\delta \mathbf{L}$ is given by

$$
  \begin{aligned}
    \delta \mathbf{L}
    & =
    \delta d \mathbf{\ell}
    \\
    & =
    \underset{= \delta_{EL}\mathbf{L}}{\underbrace{0}}
     -
    d \underset{\Theta_{BFV}}{\underbrace{\delta \mathbf{l}}}
  \end{aligned}
$$

which then implies with (eq:PresymplecticCurrent) that

$$
  \begin{aligned}
    \Omega_{BFV}
    & \coloneqq
    \delta \Theta_{BFV}
    \\
    & =
    \delta \delta \mathbf{\ell}
    \\
    & =
    0
  \end{aligned}
$$

Therefore the [[Lagrangian densities]] which are [[total spacetime derivatives]]
are also called _trivial Lagrangian densities_.

If the [[field bundle]] $E \overset{fb}{\to} \Sigma$ is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle})
over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}) then also the converse is true:
Every Lagrangian density whose [[Euler-Lagrange form]] vanishes is a total spacetime derivative.

Stated more [[category theory|abstractly]], this means that the [[exact sequence]] of the total spacetime from prop. \ref{HorizontalVariationalComplexOfTrivialFieldBundleIsExact} extends to the right via the [[Euler-Lagrange variational derivative]]
$\delta_{EL}$ to an [[exact sequence]] of the form

$$
  \mathbb{R}
    \overset{}{\hookrightarrow}
  \Omega^{0,0}_\Sigma(E)
    \overset{d}{\longrightarrow}
  \Omega^{1,0}_\Sigma(E)
    \overset{d}{\longrightarrow}
  \Omega^{2,0}_\Sigma(E)
    \overset{d}{\longrightarrow}
    \cdots
    \overset{d}{\longrightarrow}
  \Omega^{p,0}_\Sigma(E)
    \overset{d}{\longrightarrow}
  \Omega^{p+1,0}_\Sigma(E)
    \overset{\delta_{EL}}{\longrightarrow}
  \Omega^{p+1,0}_\Sigma(E) \wedge \delta(C^\infty(E))
    \overset{\delta_{H}}{\longrightarrow}
  \cdots
  \,.
$$

In fact, as shown, this [[exact sequence]] keeps going to the right;
this is also called the _[[Euler-Lagrange complex]]_.

([Anderson 89, theorem 5.1](Euler-Lagrange+complex#Anderson89))

The next [[differential]] $\delta_{H}$ after the [[Euler-Lagrange variational derivative]] $\delta_{EL}$
is known as the _[[Helmholtz operator]]_. By definition of [[exact sequence]], the
[[Helmholtz operator]] detects whether a [[partial differential equation]] on [[field histories]],
induced by a [[variational differential form]] $P \in \Omega^{p+1,0}_\Sigma(E) \wedge \delta(C^\infty(E))$
as in (eq:EquationOfMotionEL) comes from varying a [[Lagrangian density]], hence whether it is the
[[equation of motion]] of a [[Lagrangian field theory]] via def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}.

This way [[homological algebra]] is brought to bear on core questions of [[field theory]].
For more on this see the exposition at _[[schreiber:Higher Structures|Higher Structures in Physics]]_.

=--

+-- {: .num_remark #LagrangianDensityOfDiracFieldSupergeometricNature}
###### Remark
**([[supergeometry|supergeometric]] nature of [[Lagrangian density]] of the [[Dirac field]])**

Observe that the [[Lagrangian density]] for the [[Dirac field]] (def. \ref{LagrangianDensityForDiracField}) makes sense (only) due to the [[supergeometry|supergeometric]] nature of the [[Dirac field]] (remark \ref{DiracFieldSupergeometric}): If the field jet coordinates $\psi_{,\mu_1 \cdots \mu_k}$ were not anti-commuting (eq:DiracFieldJetCoordinatesAnticommute) then the
Dirac's field Lagrangian density (def. \ref{LagrangianDensityForDiracField}) would be a [[total spacetime derivative]]
and hence be trivial according to example \ref{TrivialLagrangianDensities}.

This is because

$$
  d \left(
    \tfrac{1}{2}
    \overline{\psi} \,\gamma^\mu\, \psi
    \,
    \iota_{\partial_\mu} dvol_\Sigma
  \right)
  =
  \tfrac{1}{2} \overline{\psi_{,\mu}} \,\gamma^\mu\, \psi \, dvol_\Sigma
  +
  \underset{ = (-1) \tfrac{1}{2} \overline{\psi_{,\mu}} \,\gamma^\mu\, \psi \, dvol_\Sigma  }{
  \underbrace{
  \tfrac{1}{2}\overline{\psi} \,\gamma^\mu\, \psi_{,\mu} \, dvol_\Sigma
  }}
  \,.
$$

Here the identification under the brace uses two facts:

1. the symmetry (eq:SpinorToVectorPairingIsSymmetric) of the spinor bilinear pairing $\overline{(-)}\Gamma (-)$;

1. the anti-commutativity (eq:DiracFieldJetCoordinatesAnticommute) of the Dirac field and jet coordinates, due to their [[supergeometry|supergeometric]] nature (remark \ref{DiracFieldSupergeometric}).

The second fact gives the minus sign under the brace, which makes the total expression vanish, if the
Dirac field and jet coordinates indeed are anti-commuting (which, incidentally, means that we found
an "[[off-shell]] [[conserved current]]" for the Dirac field, see example \ref{DiracCurrent} below).

If however the Dirac field and jet coordinates did commute with each other, we would instead
have a plus sign under the brace, in which case the total horizontal derivative expression
above would equal the massless Dirac field Lagrangian (eq:DiracFieldLagrangianMassless),
thus rendering it trivial in the sense of example \ref{TrivialLagrangianDensities}.

The same [[supergeometry|supergeometric]] nature of the [[Dirac field]] will be necessary
for its intended [[equation of motion]], the _[[Dirac equation]]_ (example \ref{EquationOfMotionOfDiracFieldIsDiracEquation}) to derive from a
[[Lagrangian density]]; see the proof of example \ref{PresymplecticCurrentDiracField} below, and see remark \ref{SupergeometricNatureOfDiracEquation} below.

=--



$\,$

The key implication of the [[Euler-Lagrange form]] on the [[jet bundle]] is that it induces
the _[[equation of motion]]_ on the [[space of field histories]]:


+-- {: .num_defn #EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}
###### Definition
**([[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]])**

Given a [[Lagrangian field theory]] $(E,\mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} then the corresponding _[[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]_ is the condition on [[field histories]] (def. \ref{SupergeometricSpaceOfFieldHistories})

$$
  \Phi_{(-)} \;\colon\; U \longrightarrow \Gamma_\Sigma(E)
$$

to have a [[jet prolongation]] (def. \ref{JetProlongation})

$$
  j^\infty_\Sigma(\Phi_{(-)}(-) ) \;\colon\; U \times \Sigma \longrightarrow J^\infty_\Sigma(E)
$$

that factors through the [[shell]] inclusion $\mathcal{E} \overset{i_{\mathcal{E}}}{\hookrightarrow} J^\infty_\Sigma(E)$
(eq:ShellInJetBundle) defined by vanishing of the [[Euler-Lagrange form]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime})

$$
  \label{EquationOfMotionEL}
  j^\infty_\Sigma(\Phi_{(-)}(-))
    \;\colon\;
  U \times \Sigma
    \longrightarrow
  \mathcal{E}
    \overset{i_{\mathcal{E}}}{\hookrightarrow}
  J^\infty_\Sigma(E)
  \,.
$$

(This implies that $j^\infty_\Sigma(\Phi_{(-)})$ factors even through the prolonged shell $\mathcal{E}^\infty \overset{i_{\mathcal{E}^\infty}}{\hookrightarrow} J^\infty_\Sigma(E)$ (eq:ProlongedShellInJetBundle).)

In the case that the field bundle is a [[trivial vector bundle]] over [[Minkowski spacetime]] as in example \ref{TrivialVectorBundleAsAFieldBundle} this is the condition that
$\Phi_{(-)}$ satisfies the following [[differential equation]] (again using prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}):

$$
  \left(
    \frac{\partial L}{\partial \phi^a}
      -
    \frac{d}{d x^\mu}
    \frac{\partial L}{\partial \phi^a_{,\mu}}
    +
    \frac{d^2}{d x^\mu d x^\nu} \frac{\partial L}{\partial \phi^a_{,\mu\nu}}
    -
    \cdots
  \right)
  \left(
     (x^\mu),
     (\Phi^a),
     \left( \frac{\partial \Phi^a_{(-)}}{\partial x^\mu}\right),
     \left( \frac{\partial^2 \Phi^a_{(-)}}{\partial x^\mu \partial x^\nu} \right),
     \cdots
  \right)
  \;=\;
  0
  \,.
$$

The _[[on-shell]] [[space of field histories]]_ is the space of solutions to this condition, namely the
the sub-[[super formal smooth set|super smooth set]] (def. \ref{SuperFormalSmoothSet})
of the full [[space of field histories]] (eq:SpaceOfFieldHistories) (def. \ref{SupergeometricSpaceOfFieldHistories})

$$
  \label{OnShellFieldHistories}
  \Gamma_\Sigma(E)_{\delta_{EL} L = 0}
    \overset{\phantom{AAA}}{\hookrightarrow}
  \Gamma_\Sigma(E)
$$

whose plots are those $\Phi_{(-)} \colon U \to \Gamma_\Sigma(E)$ that factor through the shell (eq:EquationOfMotionEL).

More generally for $\Sigma_r \hookrightarrow \Sigma$ a [[submanifold]] of [[spacetime]], we write

$$
  \label{OnShellFieldHistoriesInHigherCodimension}
  \Gamma_{\Sigma_r}(E)_{\delta_{EL} L = 0}
    \overset{\phantom{AAA}}{\hookrightarrow}
  \Gamma_{\Sigma_r}(E)
$$

for the sub-[[super formal smooth set|super smooth ste]] of on-shell field histories restricted to the [[infinitesimal neighbourhood]]
of $\Sigma_r$ in $\Sigma$ (eq:SpaceOfFieldHistoriesInHigherCodimension).

=--

+-- {: .num_defn #FreeFieldTheory}
###### Definition
**([[free field theory]])**

A [[Lagrangian field theory]] $(E, \mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
with [[field bundle]] $E \overset{fb}{\to} \Sigma$ a [[vector bundle]]
(e.g. a [[trivial vector bundle]] as in example \ref{TrivialVectorBundleAsAFieldBundle})
is called a _[[free field theory]]_ if its [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]
(def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}) is a
[[differential equation]] that is _[[linear differential equation]]_, in that with

$$
  \Phi_1, \Phi_2 \;\in\; \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
$$

any two [[on-shell]] [[field histories]] (eq:OnShellFieldHistories) and $c_1, c_2 \in \mathbb{R}$
any two [[real numbers]], also the [[linear combination]]

$$
  c_1 \Phi_1 + c_2 \Phi_2 \;\in\; \Gamma_\Sigma(E)
  \,,
$$

which a priori exists only as an element in the off-shell [[space of field histories]],
is again a solution to the [[equations of motion]] and hence an element of $\Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}$.

A [[Lagrangian field theory]] which is not a [[free field theory]] is called an _[[interaction|interacting]]_ [[field theory]].

=--

+-- {: .num_remark #FreeFieldTheoryRelevance}
###### Remark
**(relevance of [[free field theory]])**

In [[perturbative quantum field theory]] one considers [[interaction|interacting]] [[field theories]]
in the [[infinitesimal neighbourhood]] (example \ref{InfinitesimalNeighbourhood}) of [[free field theories]] (def. \ref{FreeFieldTheory})
inside some [[super formal smooth set|super smooth set]] of general [[Lagrangian field theories]].
While [[free field theories]] are typically of limited interest in themselves,
this [[perturbative quantum field theory|perturbation theory]] around them exhausts much of what is
known about [[quantum field theory]] in general, and therefore [[free field theories]] are of paramount importance
for the general theory.

We discuss the [[covariant phase space]] of [[free field theories]] below in _[Propagators](#Propagators)_
and their [[quantization]] below in _[Free quantum fields](#FreeQuantumFields) _.

=--

+-- {: .num_prop #EquationOfMotionOfFreeRealScalarField}
###### Example
**([[equation of motion]] of [[free field|free]] [[real scalar field]] is [[Klein-Gordon equation]])**

Consider the [[Lagrangian field theory]] of the [[free field|free]] [[real scalar field]]
from example \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}.

By example \ref{FreeScalarFieldEOM} its [[Euler-Lagrange form]] is

$$
  \delta_{EL}\mathbf{L}
    \;=\;
  \left(\eta^{\mu \nu} \phi_{,\mu \nu} - m^2 \right) \delta \phi \wedge dvol_\sigma
$$

Hence for $\Phi \in \Gamma_\Sigma(E) = C^\infty(X)$ a [[field history]],
its [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]]
according to def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime} is

$$
  \eta^{\mu \nu} \frac{\partial^2 }{\partial x^\mu \partial x^\nu} \Phi - m^2 \Phi \;=\; 0
$$

often abbreviated as

$$
  \label{KleinGordonEquation}
  (\Box - m^2) \Phi \;=\; 0
  \,.
$$

This [[PDE]] is called the _[[Klein-Gordon equation]]_ on Minowski spacetime. If the [[mass]] $m$
vanishes, $m = 0$, then this is the _relativistic [[wave equation]]_.

Hence this is indeed a [[free field theory]] according to def. \ref{FreeFieldTheory}.

The corresponding [[linear differential operator]] (def. \ref{DifferentialOperator})

$$
  \label{KleinGordonOperator}
  (\Box - m^2)
    \;\colon\;
  \Gamma_\Sigma(\Sigma \times \mathbb{R})
     \longrightarrow
  \Gamma_\Sigma(\Sigma \times \mathbb{R})
$$

is called the _[[Klein-Gordon operator]]_.

=--

For later use we record the following basic fact about the [[Klein-Gordon equation]]:

+-- {: .num_example #FormallySelfAdjointKleinGordonOperator}
###### Example
**([[Klein-Gordon operator]] is [[formally adjoint differential operator|formally self-adjoint]] )**

The [[Klein-Gordon operator]] (eq:KleinGordonOperator)
is its own [[formal adjoint differential operator|formal adjoint]] (def. \ref{FormallyAdjointDifferentialOperators}) witnessed by the bilinear differential operator (eq:FormallyAdjointDifferentialOperatorWitness) given by

$$
  \label{WitnessForFormalSelfadjointnessOfKleinGordonEquation}
  K(\Phi_1, \Phi_2)
  \;\coloneqq\;
  \left(
    \frac{\partial \Phi_1}{\partial x^\mu} \Phi_2
    -
    \Phi_1 \frac{\partial \Phi_2}{\partial x^\mu}
  \right)
  \eta^{\mu \nu}\iota_{\partial_\nu} dvol_\Sigma
  \,.
$$

=--

+-- {: .proof}
###### Proof

$$
  \begin{aligned}
    d K(\Phi_1, \Phi_2)
    & =
    d
    \left(
      \frac{\partial \Phi_1}{\partial x^\mu} \Phi_2
      -
      \Phi_1 \frac{\partial \Phi_2}{\partial x^\mu}
    \right)
    \eta^{\mu \nu}\iota_{\partial_\nu} dvol_\Sigma
    \\
    &=
    \left(
    \left(
      \eta^{\mu \nu}\frac{\partial^2 \Phi_1}{\partial x^\mu \partial x^\nu} \Phi_2
      +
      \eta^{\mu \nu} \frac{\partial \Phi_1}{\partial x^\mu} \frac{\partial \Phi_2}{\partial x^\nu}
    \right)
    -
    \left(
      \eta^{\mu \nu}
      \frac{\partial \Phi_1}{\partial x^\nu} \frac{\partial \Phi_2}{\partial x^\mu}
      +
      \Phi_1 \eta^{\mu \nu} \frac{\partial^2 \Phi_2}{\partial x^\nu \partial x^\mu}
    \right)
    \right)
    dvol_\Sigma
    \\
    & =
    \left(
      \eta^{\mu \nu}\frac{\partial^2 \Phi_1}{\partial x^\mu \partial x^\nu} \Phi_2
      -
      \Phi_1 \eta^{\mu \nu} \frac{\partial^2 \Phi_2}{\partial x^\nu \partial x^\mu}
    \right)
    dvol_\Sigma
    \\
    & =
    \Box(\Phi_1) \Phi_2 - \Phi_1 \Box (\Phi_2)
  \end{aligned}
$$

=--



+-- {: .num_prop #MaxwellVacuumEquation}
###### Example
**([[equations of motion]] of [[vacuum]] [[electromagnetism]] are [[vacuum]] [[Maxwell's equations]])**

Consider the [[Lagrangian field theory]] of [[free field|free]] [[electromagnetism]]
on [[Minkowski spacetime]] from example \ref{ElectromagnetismLagrangianDensity}.

By example \ref{ElectromagnetismEl} its [[Euler-Lagrange form]] is

$$
  \delta_{EL}\mathbf{L}
    \;=\;
  \frac{d}{d x^\mu}f^{\mu \nu} \delta a_\nu
  \,.
$$

Hence for $A \in \Gamma_{\Sigma}(T^\ast \Sigma) = \Omega^1(\Sigma)$ a [[field history]] ("[[vector potential]]"),
its [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]]
according to def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime} is

$$
  \begin{aligned}
    & \frac{\partial}{\partial x^\mu} F^{\mu \nu} = 0
    \\
    \Leftrightarrow\;\;  &
    d \star_\eta F = 0
  \end{aligned}
  \,,
$$

where $F = d A$ is the [[Faraday tensor]] (eq:TensorFaraday).
(In the coordinate-free formulation in the second line "$\star_\eta$" denotes
the [[Hodge star operator]] induced by the [[pseudo-Riemannian metric]] $\eta$ on [[Minkowski spacetime]].)

These [[PDEs]] are called the _[[vacuum]] [[Maxwell's equations]]_.

This, too, is a [[free field theory]] according to def. \ref{FreeFieldTheory}.

=--



+-- {: .num_example #EquationOfMotionOfDiracFieldIsDiracEquation}
###### Example
**([[equation of motion]] of [[Dirac field]] is [[Dirac equation]])**

Consider the [[Lagrangian field theory]] of the [[Dirac field]]
on [[Minkowski spacetime]] from example \ref{LagrangianDensityForDiracField},
with [[field fiber]] the [[spin representation]] $S$ regarded as a [[superpoint]] $S_{odd}$ and
[[Lagrangian density]] given by the spinor bilinear pairing

$$
  L
   \;=\;
  i \overline{\psi} \gamma^\mu \partial_\mu \psi + m \overline{\psi}\psi
$$

(in spacetime dimension $p+1 \in \{3,4,6,10\}$ with $m = 0$ unless $p+1 = 4$).

From example \ref{PresymplecticCurrentDiracField} it follows that
the corresponding [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}) is

$$
  \label{DiracEquation}
  \left(-i \gamma^\mu \partial_\mu + m\right)\psi \;=\; 0
  \,.
$$

This is the _[[Dirac equation]]_. In terms of the _[[Feynman slash notation]]_ from (eq:FeynmanSlashNotationForMasslessDiracOperator)
the corresponding [[differential operator]], the _[[Dirac operator]]_ reads

$$
  \left(
    - i \partial\!\!\!/\, + m
  \right)
  \psi = 0
  \,.
$$

Hence this is a [[free field theory]] according to def. \ref{FreeFieldTheory}.

Observe that the "square" of the [[Dirac operator]] is the [[Klein-Gordon operator]] $\Box - m^2$ (eq:KleinGordonEquation)

$$
  \begin{aligned}
    \left(
      +i \gamma^\mu \partial_\mu + m
    \right)
    \left(-i \gamma^\mu \partial_\mu + m\right)\psi
    &
    =
    \left(\partial_\mu \partial^\mu - m^2\right) \psi
    \\
    & =
    \left(\Box - m^2\right) \psi
  \end{aligned}
  \,.
$$

This means that a [[Dirac field]] which solves the [[Dirac equations]] is
in particular (on [[Minkowski spacetime]]) componentwise a [[solution]] to the [[Klein-Gordon equation]].

=--


+-- {: .num_prop #SupergeometricNatureOfDiracEquation}
###### Remark
**([[supergeometry|supergeometric]] nature of the [[Dirac equation]] as an [[Euler-Lagrange equation]])**

While the [[Dirac equation]] (eq:DiracEquation) of example \ref{EquationOfMotionOfDiracFieldIsDiracEquation}
would make sense in itself also if the field coordinates $\psi$ and jet coordinates $\psi_{,\mu}$ of the [[Dirac field]]
were not anti-commuting (eq:DiracFieldJetCoordinatesAnticommute), due to their [[supergeometry|supergeometric]] nature (remark \ref{DiracFieldSupergeometric}), it would,
by remark \ref{LagrangianDensityOfDiracFieldSupergeometricNature}, then no longer be the [[Euler-Lagrange equation]] of a [[Lagrangian density]],
hence then Dirac field theory would not be a [[Lagrangian field theory]].

=--

+-- {: .num_example #DiracOperatorOnDiracSpinorsIsFormallySelfAdjointDifferentialOperator}
###### Example
**([[Dirac operator]] on [[Dirac spinors]] is [[formally self-adjoint differential operator]])**

The _[[Dirac operator]], hence the [[differential operator]] corresponding to the [[Dirac equation]] of example \ref{EquationOfMotionOfDiracFieldIsDiracEquation} via def. \ref{DifferentialOperator}
is a [[formally self-adjoint differential operator|formally anti-self adjoint]] (def. \ref{FormallyAdjointDifferentialOperators}):

$$
  D^\ast = - D
  \,.
$$

=--

+-- {: .proof}
###### Proof


Regard the Dirac operator as taking values in the [[dual vector bundle|dual]] [[spin bundle]] by using the [[Dirac conjugate]] $\overline{(-)}$ (eq:DiracConjugate):

$$
  \array{
    \Gamma_\Sigma(\Sigma \times S)
      &\overset{D}{\longrightarrow}&
    \Gamma_\Sigma(\Sigma \times S^\ast)
    \\
   \Psi &\mapsto&
   \overline{(-)} \gamma^\mu \partial_\mu  \Psi
  }
$$

Then we need to show that there is $K(-,-)$ such that for all [[pairs]] of [[spinor]] [[sections]] $\Psi_1, \Psi_2$ we have

$$
  \overline{\Psi_2}\gamma^\mu (\partial_\mu \Psi_1)
  -
  \overline{\Psi_1}\gamma^\mu (-\partial_\mu \Psi_2)
  \;=\;
  d K(\psi_1, \psi_2)
  \,.
$$

But the spinor-to-vector pairing is symmetric (eq:SpinorToVectorPairingIsSymmetric),  hence this is equivalent to

$$
  \overline{\partial_\mu \Psi_1}\gamma^\mu \Psi_2
  +
  \overline{\Psi_1}\gamma^\mu (\partial_\mu \Psi_2)
  \;=\;
  d K(\psi_1, \psi_2)
  \,.
$$

By the [[product law]] of [[differentiation]], this is solved, for all $\Psi_1, \Psi_2$, by

$$
  K(\Psi_1, \Psi_2)
    \;\coloneqq\;
  \left( \overline{\Psi_1} \gamma^\mu \Psi_2\right)
  \,
  \iota_{\partial_\mu} dvol
  \,.
$$

=--



$\,$

This concludes our discussion of [[Lagrangian densities]] and their [[variational calculus]].
In the [next chapter](#Symmetries) we consider the [[infinitesimal symmetries of Lagrangians]].
