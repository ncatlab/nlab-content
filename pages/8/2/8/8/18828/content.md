

## Gauge fixing
 {#GaugeFixing}

While in the [previous chapter](#ReducedPhaseSpace) we had constructed the [[reduced phase space]] of a [[Lagrangian field theory]], embodied by the [[local BV-BRST complex]] (example \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm}), as the [[homotopy quotient]] by the [[infinitesimal gauge symmetries]] of the [[homotopy intersection]] with the [[shell]], this in general still does not yield a [[covariant phase space]] of [[on-shell]] [[field histories]] (prop. \ref{CovariantPhaseSpace}), since [[Cauchy surfaces]] for the [[equations of motion]] may still not exist (def. \ref{CauchySurface}).

However, with the [[homological resolution]] constituted by the [[BV-BRST complex]] in hand, we now have the freedom to adjust the [[field (physics)|field]]-content of the theory without changing its would-be [[reduced phase space]], namely without changing its [[BV-BRST cohomology]]. In particular we may adjoin further "[[auxiliary fields]]" in various degrees, as long as they contribute only a [[contractible chain complex|contractible cochain complex]] to the [[BV-BRST complex]]. If such a _[[quasi-isomorphism]]_ of [[BV-BRST complexes]] brings the [[Lagrangian field theory]] into a form such that the [[equations of motion]] of the combined [[field (physics)|fields]], [[ghost fields]] and potential further [[auxiliary fields]] are [[Green hyperbolic differential equations]] after all, and thus admit a [[covariant phase space]], then this is called a _[[gauge fixing]]_ (def. \ref{GaugeFixingLagrangianDensity} below), since it is the [[infinitesimal gauge symmetries]] which [[obstruction|obstruct]] the existence of [[Cauchy surfaces]] (by prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces} and remark \ref{GaugeParametrizedInfinitesimalGaugeTransformation}).

The archetypical example is the [[Gaussian-averaged Lorenz gauge]] [[gauge fixing|fixing]] of the [[electromagnetic field]] (example \ref{NLGaugeFixingOfElectromagnetism} below) which reveals that the gauge-invariant content of [[electromagnetic waves]] is only in their transversal [[wave polarization]] (prop. \ref{GaugeInvariantPolynomialOnShellObservablesOfFreeElectromagneticField} below).

The tool of [[gauge fixing]] via [[quasi-isomorphisms]] of [[BV-BRST complexes]] finally brings us in position to consider, in the following chapters, the [[quantization]] also of [[gauge theories]]: We use [[gauge fixing]] [[quasi-isomorphisms]]
to bring the [[BV-BRST complexes]] of the given [[Lagrangian field theories]] into a form that admits degreewise [[quantization]] of a [[graded manifold|graded]] [[covariant phase space]] of [[fields (physics)|fields]], [[ghost fields]] and possibly further [[auxiliary fields]], compatible with the gauge-fixed [[BV-BRST differential]]:

$\,$

$$
  \array{
     \underline{\mathbf{\text{pre-quantum geometry}}}
     &&
     \underline{\mathbf{\text{higher pre-quantum geometry}}}
     \\
     \,
     \\
     \left\{
        \array{
           \text{Lagrangian field theory with}
           \\
           \text{infinitesimal gauge transformations}
        }
     \right\}
     &\overset{ \text{homotopy quotient by} \atop \text{gauge transformations}  }{\longrightarrow}&
     \left\{
        \array{
           \text{dg-Lagrangian field theory with}
           \\
           \text{quotiented by gauge transformations}
           \\
           \text{embodied by BRST complex }
        }
     \right\}
     \\
     && \Big\downarrow{}^{\mathrlap{ \text{pass to} \atop \text{derived critical locus} }}
     \\
     &&
     \left\{
        \array{
           \text{dg-reduced phase space}
           \\
           \text{ embodied by BV-BRST complex }
        }
     \right\}
     \\
     && {}^{\mathllap{\simeq}}\Big\downarrow{}^{\mathrlap{\text{fix gauge} }}
     \\
     \left\{
       \array{
         \text{ decategorified }
         \\
         \text{ covariant }
         \\
         \text{ reduced phase space }
       }
     \right\}
     &\underset{\text{pass to cohomology}}{\longleftarrow}&
     \left\{
        \array{
           \text{ dg-covariant}
           \\
           \text{reduced phase space  }
        }
     \right\}
     \\
     && \Big\downarrow{}^{\mathrlap{
       \array{
           \text{ quantize }
           \\
           \text{degreewise}
       }
     }}
     \\
     \left\{
       \array{
         \text{gauge invariant}
         \\
         \text{quantum observables}
       }
     \right\}
     &\underset{\text{pass to cohomology}}{\longleftarrow}&
     \left\{
       \array{
         \text{quantum}
         \\
        \text{BV-BRST complex}
       }
     \right\}
  }
$$


Here:

| term  |   meaning   |
|-------|-------------|
| "phase space" | [[derived critical locus]] of [[Lagrangian density|Lagrangian]] equipped with [[Poisson bracket]] |
| "reduced" | [[gauge transformations]] have been [[homotopy quotient|homotopy-quotiented]] out |
| "covariant" | [[Cauchy surfaces]] exist degreewise |

$\,$

We now discuss these topics:

1. _[Quasi-isomorphisms between local BV-BRST complexes](#QuasiIsomorphismsBetweenBVBRSTComplexes)_

   1. [gauge fixing chain maps](#GaugeFixingChainMaps);

   1. [adjoining contractible complexes of auxiliary fields](#AdjoiningAuiliaryFields)

1. _[Example: gauge fixed electromagnetic field](#GaugeFixingExamples)_


$\,$

**[[quasi-isomorphisms]] between [[local BV-BRST complexes]]**
 {#QuasiIsomorphismsBetweenBVBRSTComplexes}

Recall (prop. \ref{CochainCohomologyOfBVBRSTComplexInDegreeZero}) that given a [[local BV-BRST complex]] (example  \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm}) with [[BV-BRST differential]] $s$, then the space of
[[local observables]] which are [[on-shell]] and [[gauge invariance|gauge invariant]] is the [[cochain cohomology]]
of $s$ in degree zero:

$$
  H^0(s \vert d)
  \;=\;
  \left\{
    \array{
      \text{gauge invariant on-shell}
      \\
      \text{local observables}
    }
  \right\}
$$

The key point of having [[resolution|resolved]] (in chapter _[Reduced phase space](#ReducedPhaseSpace)_) the naive [[quotient]] by [[infinitesimal gauge symmetries]] of the naive [[intersection]] with the [[shell]] by the [[L-infinity algebroid]] whose [[Chevalley-Eilenberg algebra]] is called the _[[local BV-BRST complex]]_, is that placing the [[reduced phase space]] into the [[(infinity,1)-category|context]]
of [[homotopy theory]]/[[homological algebra]] this way provides the freedom of changing the choice of [[field bundle]] and of
[[Lagrangian density]] without actually changing the [[Lagrangian field theory]] _up to [[equivalence]]_, namely without changing the
[[cochain cohomology]] of the [[BV-BRST complex]].


A [[homomorphism]] of [[differential graded-commutative superalgebras]] (such as [[BV-BRST complexes]]) which
induces an [[isomorphism]] in [[cochain cohomology]] is called a _[[quasi-isomorphism]]_. We now discuss two
classes of [[quasi-isomorphisms]] between [[BV-BRST complexes]]:

1. _[[gauge fixing]]_ (def. \ref{GaugeFixingLagrangianDensity} below)

1. _adjoining [[auxiliary fields]]_ (def. \ref{AuxiliaryFields} below).

$\,$

**[[gauge fixing]] [[chain maps]]**
  {#GaugeFixingChainMaps}

+-- {:.num_prop #ExponentialOfLocalAntibracket}
###### Proposition
**([[local antibracket|local anti-]][[Hamiltonian flow]] is [[automorphism]] of [[local antibracket]])**

Let

$$
  CE\left(  E/(\mathcal{G} \times_\Sigma T\Sigma)_{\delta_{EL} L \simeq 0} \right)
  \;=\;
  \left(
    \Omega^{0,0}_\Sigma\left(
      T^\ast_{\Sigma,inf}[-1]\left(E \times_\Sigma \mathcal{G}[1]\right) \times_\Sigma T \Sigma[1]
    \right)
    \;,\;
    d_{CE}
    =
    \underset{s}{
    \underbrace{
      \left\{
        -\mathbf{L} + \mathbf{L}_{BRST}
        \,,\,
        -
      \right\}
    }
    }
    \;+\;
    d
  \right)
$$

be a  [[local BV-BRST complex]] of a [[Lagrangian field theory]] $(E,\mathbf{L})$ (example \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm}).

Then for

$$
  \mathbf{L}_{gf}
  \;\in\;
  \Omega^{p+1,0}
  \left(
    T^\ast_{\Sigma,inf}\left(E \times_\Sigma \mathcal{G}\right) \times_\Sigma T \Sigma[1]
  \right)
$$

a [[Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) on the [[graded manifold|graded]] [[field bundle]]

$$
  \mathbf{L}_{gf} \;=\; L_{gf} \ dvol_\Sigma
$$

of degree

$$
  deg(L) = (-1, even)
$$

then the [[exponential]] of forming the [[local antibracket]] (def. \ref{LocalAntibracket}) with $\mathbf{L}_{gf}$

$$
  \array{
    \Omega^{p+1,0}_\Sigma\left( T^\ast_{\Sigma,inf}[-1]\left( E \times_\Sigma \mathcal{G}[1]\right) \right)
    &
    \overset{
      e^{\left\{ \mathbf{L}_{gf} \,,\, -\right\}}(-)
    }{\longrightarrow}
    &
    \Omega^{p+1,0}_\Sigma\left( T^\ast_{\Sigma,inf}[-1]\left( E \times_\Sigma \mathcal{G}[1]\right) \right)
    \\
    \mathbf{K}
      &\mapsto&
    \left\{ \mathbf{L}_{gf} , \mathbf{K} \right\}
    +
    \tfrac{1}{2}
    \left\{ \mathbf{L}_{gf} \,,\, \left\{ \mathbf{L}_{gf} \,,\, \mathbf{K} \right\} \right\}
    +
    \tfrac{1}{6}
    \left\{ \mathbf{L}_{gf} \,,\,\left\{ \mathbf{L}_{gf} \,,\, \left\{ \mathbf{L}_{gf} \,,\,\mathbf{K} \right\} \right\} \right\}
    +
    \cdots
  }
$$

is an [[endomorphism]] of the [[local antibracket]] (def. \ref{LocalAntibracket}) in that

$$
  e^{
    \left\{ \mathbf{\psi} \,,\, - \right\}
  }
  \left(
    \left\{ \mathbf{A} \,,\, \mathbf{B} \right\}
  \right)
  \;=\;
  \left\{
    e^{
      \left\{ \mathbf{\psi} \,,\, - \right\}
    }
    \left(\mathbf{A}\right)
    \,,\,
    e^{
      \left\{ \psi \,,\, - \right\}
    }
    \left(\mathbf{B}\right)
  \right\}
$$

and in fact an [[automorphism]], with [[inverse morphism]] given by

$$
  \left(e^{\left\{ \psi \,,\, -\right\}}(-)\right)^{-1}
  \;=\;
  e^{\left\{ -\psi \,,\, -\right\}}(-)
  \,.
$$

We may think of this as the _[[Hamiltonian flow]]_ of $\mathbf{L}_{gf}$ under the [[local antibracket]].

In particular when applied to the [[BV-Lagrangian density]]

$$
  s_{gf}
  \;\coloneqq\;
  \left\{
    e^{\left\{ \mathbf{L}_{gf},-\right\}}\left(- \mathbf{L} +  \mathbf{L}_{BRST}\right)
    \,,\,
    -
  \right\}
$$

this yields another [[differential]]

$$
  \left( s_{gf}\right)^2
  \;=\;
  0
$$

and hence another [[differential graded-commutative superalgebra]] (def. \ref{differentialgradedcommutativeSuperalgebra})

$$
  CE\left(  E/(\mathcal{G} \times_\Sigma T\Sigma)^{gf}_{\delta_{EL} L \simeq 0} \right)
  \;=\;
  \left(
    \Omega^{0,0}_\Sigma\left(
      T^\ast_{\Sigma,inf}[-1]\left(E \times_\Sigma \mathcal{G}[1]\right) \times_\Sigma T \Sigma[1]
    \right)
    \;,\;
    d_{CE}
    =
    \underset{s_{gf}}{
    \underbrace{
      \left\{
        e^{\left\{ \mathbf{L}_{gf}, - \right\}}\left( - \mathbf{L} + \mathbf{L}_{BRST} \right)
        \,,\,
        -
      \right\}
    }
    }
    \;+\;
    d
  \right)
$$

Finally, $e^{\left\{\mathbf{L}_{gf},-\right\}}$ constitutes a [[chain map]]
from the [[local BV-BRST complex]] to this deformed version, in fact a
[[homomorphism]] of [[differential graded-commutative superalgebras]], in that

$$
  s_{gf} \circ e^{ \left\{ \mathbf{L}_{gf}\,,\, - \right\} }
  \;=\;
  e^{ \left\{ \mathbf{L}_{gf}\,,\, - \right\} } \circ s
  \,.
$$


=--

+-- {: .proof}
###### Proof

By prop. \ref{BasicPropertiesOfTheLocalAntibracket}
the [[local antibracket]] $\left\{ -,-\right\}$ is a graded [[derivation]] in its second argument, of degree one more than the degree of its first argument (eq:LocalAntibracketGradedDerivationInSecondArgument). Hence for the first argument of degree -1 this implies
that $e^{\{\mathbf{L}_{gf}, - \}}$ is an automorphism of the local antibracket. Moreover, it is clear from the definition that
$\left\{ \mathbf{L}_{gf},-\right\}$ is a [[derivation]] with respect to the pointwise product of smooth functions,
so that $e^{\{\mathbf{L}_{gf},-\}}$ is also a homomorpism of graded algebras.

Since $e^{\{\mathbf{L}_{gf}, -\}}$ is an automorphism of the local antibracket, and since $s$ and $s_{gf}$
are themselves given by applying the local antibracket in the second argument, this implies that
$e^{\{\mathbf{L}_{gf},-\}}$ respects the differentials:

$$
  \array{
    \mathbf{A}
      &\overset{e^{\{\mathbf{L}_{gf},-\}}}{\longrightarrow}&
    e^{\{\mathbf{L}_{gf},-\}}\left( \mathbf{A} \right)
    \\
    {}^{\mathllap{s}}\downarrow && \downarrow^{\mathrlap{s_{gf}}}
    \\
    \left\{ \left(-\mathbf{L} + \mathbf{L}_{BRST}\right)\,,\, \mathbf{A}\right\}
      &\underset{ e^{\{\mathbf{L}_{gf}\,,\,-\}} }{\longrightarrow}&
    \left\{ e^{\{\mathbf{L}_{gf},-\}}\left(-\mathbf{L} + \mathbf{L}_{BRST}\right)
      \,,\,
    e^{\{\mathbf{L}_{gf},-\}}(\mathbf{A})
    \right\}
  }
$$

=--


+-- {: .num_defn #GaugeFixingLagrangianDensity}
###### Definition
**([[gauge fixing Lagrangian density]])**

Let

$$
  CE\left(  E/(\mathcal{G} \times_\Sigma T\Sigma)_{\delta_{EL} L \simeq 0} \right)
  \;=\;
  \left(
    \Omega^{0,0}_\Sigma\left(
      T^\ast_{\Sigma,inf}[-1]\left(E \times_\Sigma \mathcal{G}[1]\right) \times_\Sigma T \Sigma[1]
    \right)
    \;,\;
    d_{CE}
    =
    \underset{s}{
    \underbrace{
      \left\{
        -\mathbf{L} + \mathbf{L}_{BRST}
        \,,\,
        -
      \right\}
    }
    }
    \;+\;
    d
  \right)
$$

be a  [[local BV-BRST complex]] of a [[Lagrangian field theory]] $(E,\mathbf{L})$ (example \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm}) and let

$$
  \mathbf{L}_{gf}
  \;\in\;
  \Omega^{p+1,0}
  \left(
    T^\ast_{\Sigma,inf}\left(E \times_\Sigma \mathcal{G}\right) \times_\Sigma T \Sigma[1]
  \right)
$$

be a [[Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) on the [[graded manifold|graded]] [[field bundle]] such that

$$
  deg(L_{gf}) = -1
  \,.
$$

If the [[quasi-isomorphism]] of [[BV-BRST complexes]] given by the [[local antibracket|local anti-]][[Hamiltonian flow]]
$\mathbf{L}_{gf}$ via prop. \ref{ExponentialOfLocalAntibracket}

$$
  e^{\left\{ \mathbf{L}_{gf},-\right\}}
  \;\colon\;
  CE\left(  E/(\mathcal{G} \times_\Sigma T\Sigma)^{gf}_{\delta_{EL} L \simeq 0} \right)
    \overset{\phantom{A}\simeq_{qi}\phantom{A}}{\longrightarrow}
  CE\left(  E/(\mathcal{G} \times_\Sigma T\Sigma)^{gf}_{\delta_{EL} L \simeq 0} \right)
$$

is such that for the transformed graded [[Lagrangian field theory]]

$$
  \label{GaugeFixedLagrangianDensity}
  -\underset{deg_{af} = 0}{\underbrace{\mathbf{L}' }} + \mathbf{L}'_{BRST}
  \;\coloneqq\;
  e^{\{\mathbf{L}_{gf},-\}}(-\mathbf{L} + \mathbf{L}_{BRST})
$$

(with [[Lagrangian density]] $\mathbf{L}'$ the part independent of [[antifields]])
the [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}) admit [[Cauchy surfaces]] (def. \ref{CauchySurface}), then we call $\mathbf{L}_{gf}$ a _[[gauge fixing Lagrangian density]]_
for the original Lagrangian field theory, and $\mathbf{L}'$ the corresponding _gauge fixed_ form of the original [[Lagrangian density]] $\mathbf{L}$.

=--


+-- {: .num_remark}
###### Remark
**(warning on terminology)**

What we call a _[[gauge fixing Lagrangian density]]_ $\mathbf{L}_{gf}$ in def. \ref{GaugeFixingLagrangianDensity} is traditionally called a _[[gauge fixing fermion]]_ and denoted by "$\psi$" ([Henneaux 90, section 8.3, 8.4](BRST+complex#Henneaux90)).

Here "fermion" is meant as a reference to the fact that the cohomological degree $deg(L_{gf}) = -1$, which is reminiscent of the odd [[supergeometry|super-degree]] of [[fermion]] fields such as the [[Dirac field]] (example \ref{DiracFieldBundle}); see at _[[signs in supergeometry]]_ the section _[The super odd sign rule](signs+in+supergeometry#SuperOddConvention)_. 

=--

+-- {: .num_example #GaugeFixingViaAntiLagrangianSubspaces}
###### Example
**([[gauge fixing]] via [[local antibracket|anti-]][[Lagrangian subspaces]])**



Let $\mathbf{L}_{gf}$ be a [[gauge fixing Lagrangian density]] as in def. \ref{GaugeFixingLagrangianDensity}
such that

1. its [[local antibracket]]-square vanishes

   $$
     \left\{ \mathbf{L}_{gf},\, \left\{ \mathbf{L}_{gf}, \, -\right\} \right\} = 0
   $$

   hence its [[local antibracket|anti-]][[Hamiltonian flow]] has at most a linear component in its argument $\mathbf{A}$:

   $$
     e^{\left\{ \mathbf{L}_{gf} \,,\, \mathbf{A}  \right\}}
     \;=\;
     \mathbf{A} + \left\{ \mathbf{L}_{gf} \,,\, \mathbf{A}  \right\}
   $$

1. it is independent of the [[antifields]]

   $$
     deg_{af}\left( L_{gf} \right) \;=\; 0
     \,.
   $$

Then with

* $(\phi^A)$ collectively denoting all the [[field (physics)|field]] coordinates

  (including the actual fields $\phi^a$, the [[ghost fields]] $c^\alpha$ as well as possibly further [[auxiliary fields]])

* $(\phi^\ddagger_A)$ collectively denoting all the [[antifield]] coordinates

  (includion the antifields $\phi^\ddagger_a$ of the actual fields, the antifields $c^\ddagger_\alpha$ of the [[ghost fields]] as well as those of possibly further [[auxiliary fields]] )

we have

$$
  \begin{aligned}
    (\phi')^A
    & \coloneqq
    e^{\left\{ \mathbf{L}_{gf}\,,\, - \right\}}(\phi^A)
    \\
    & = \phi^A
    \\
    \phantom{A}
    \\
    (\phi')^\ddagger_A
    & \coloneqq
    e^{\left\{ \mathbf{L}_{gf}\,,\, - \right\}}
    \left( \phi^\ddagger_A \right)
    \\
    &  =
    \phi^\ddagger_A - \frac{\overset{\leftarrow}{\delta}_{EL} \mathbf{L}_{gf}}{\delta \phi^a}
  \end{aligned}
$$

(and similarly for the higher jets); and the corresponding transformed [[Lagrangian density]] (eq:GaugeFixedLagrangianDensity)
may be written as

$$
  \begin{aligned}
    -\mathbf{L}' +  \mathbf{L}'_{BRST}
    & \coloneqq
    e^{\left\{ \mathbf{L}_{gf}\,,\, - \right\}}\left( -\mathbf{L} + \mathbf{L}_{BRST} \right)
    \\
    & =
    \left(
      -\mathbf{L}
      +
      \mathbf{L}_{BRST}
    \right)
    \left( \phi', (\phi')^\ddagger  \right)
  \end{aligned}
  \,,
$$

where the notation on the right denotes that $\phi'$ is [[substitution|substituted]] for $\phi$ and $\phi'_\ddagger$ for $\phi_\ddagger$.

This means that the defining condition that $\mathbf{L}'$ be the antifield-independent summand (eq:GaugeFixedLagrangianDensity), which we may write as

$$
  \mathbf{L}'
  \coloneqq
  \left(
    -\mathbf{L}
    +
    \mathbf{L}_{BRST}
  \right)
  \left( \phi'(\phi), \phi_\ddagger = 0  \right)
$$

translates into

$$
  \mathbf{L}'
  \coloneqq
  \left(
    -\mathbf{L}
    +
    \mathbf{L}_{BRST}
  \right)
  \left( \phi', (\phi')^\ddagger_A  = -\frac{\overset{\leftarrow}{\delta}_{EL} L_{gf}}{\delta \phi^A}  \right)
  \,.
$$

In this form BV-gauge fixing is considered traditionally
(e.g. [Hennaux 90, section 8.3, page 83, equation (76b) and item (iii)](gauge+fixing#Henneaux90)).

=--

$\,$

**adjoining [[contractible chain complexes|contractible cochain complexes]] of [[auxiliary fields]]**
  {#AdjoiningAuiliaryFields}

Typically a [[Lagrangian field theory]] $(E,\mathbf{L})$ for given choice of [[field bundle]], even after finding appropriate [[gauge parameter bundles]] $\mathcal{G}$, does not yet admit a [[gauge fixing Lagrangian density]] (def. \ref{GaugeFixingLagrangianDensity}).
But if the [[gauge parameter bundle]] has been
chosen suitably, then the remaining [[obstruction]] vanishes "up to [[homotopy]]" in that a [[gauge fixing Lagrangian density]]
does exist if only one adjoins sufficiently many [[auxiliary fields]] forming a [[contractible chain complex|contractible complex]], hence without changing the [[cochain cohomology]] of the [[BV-BRST complex]]:

+-- {: .num_defn #AuxiliaryFields}
###### Definition
**([[auxiliary fields]] and [[antighost fields]])**

Over [[Minkowski spacetime]] $\Sigma$, let

$$
  A \overset{aux}{\longrightarrow} \Sigma
$$

be any [[graded manifold|graded]] [[vector bundle]] (remark \ref{dgManifolds}), to be regarded as a [[field bundle]] (def. \ref{FieldsAndFieldBundles}) for _[[auxiliary fields]]_. If this is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) we denote its field [[coordinates]] by $(b^i)$. On the corresponding graded bundle with degrees shifted down by one

$$
  A[-1] \overset{aux[-1]}{\longrightarrow} \Sigma
$$

we write $(\overline{c}^i)$ for the induced field coordinates.

Accordingly, the shifted infinitesimal [[vertical cotangent bundle]] (def. \ref{InfinitesimalCotangentBundleOfFieldAndGaugeParameterBundle})
of the [[fiber product]] of these bundles

$$
  T^\ast_{\Sigma,inf}[-1]\left( A \times_\Sigma A^\ast[-1]  \right)
$$

has the following coordinates:

$$
  \array{
    \text{name:}
    &
    \array{
      \text{antifield of}
      \\
      \text{antighost field}
    }
    &
    \array{
      \text{antifield of}
      \\
      \text{auxiliary field}
    }
    &
    \text{antighost field}
    &
    \text{auxiliary field}
    \\
    \text{symbol:} & \overline{c}^\ddagger_i & b^\ddagger_i & \overline c^i & b^i
    \\
    deg = & -(deg(b^i)-1)-1 & -deg(b^i)-1 & deg(b^i)-1 & deg(b^i)
    \\
    & = -deg(b^i)
  }
$$

On this [[fiber bundle]] consider the [[Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})

$$
  \label{LagrangianDensityForAuxiliaryFields}
  \mathbf{L}_{aux}
  \;\in\;
  \Omega^{p+1,0}_\Sigma( T^\ast_{\Sigma,inf}[-1]\left( A \times_\Sigma A[-1] \right) )
$$

given in [[local coordinates]] by

$$
  \mathbf{L}_{aux}
    \;\coloneqq\;
   \overline{c}^\ddagger_i b^i \, dvol_\Sigma
   \,.
$$

This is such that the [[local antibracket]] (def. \ref{LocalAntibracket}) with this Lagrangian
acts on generators as follows:

$$
  \label{BVDifferentialOnauxiliaryFields}
  \array{
    && \left\{ \mathbf{L}_{aux},- \right\}
    \\
    \text{auxiliary field}
    &
    b^i &\mapsto& 0
    \\
    \text{antighost field}
    &
    \overline{c}^i &\mapsto& b^i
    \\
    \text{antifield of auxiliary field}
    &
    b^\ddagger_i &\mapsto& - \overline{c}^\ddagger_i
    \\
    \text{antifield of antighost field}
    &
    \overline{c}^\ddagger_i &\mapsto& 0
  }
$$

=--


+-- {: .num_remark}
###### Remark
**(warning on terminology)**

Beware that when adjoining [[antifields]] as in def. \ref{AuxiliaryFields} to a [[Lagrangian field theory]] which also has [[ghost fields]] $(c^\alpha)$ adjoined (example \ref{LocalOffShellBRSTComplex}) then there is _no_ relation, a priori, between

* the "antighost field" $\overline{c}^i$

and

* the "antifield of the ghost field" $c^\ddagger_\alpha$

In particular there is also the

* "antifield of the antighost field" $\overline{c}^\ddagger_i$

The terminology and notation is maybe unfortunate but entirely established.

=--

The following is immediate from def. \ref{AuxiliaryFields}, in fact this is the purpose of the definition:

+-- {: .num_prop #QuasiIsomorphismAdjoiningAuxiliaryFields}
###### Proposition
**(adjoining [[auxiliary fields]] is [[quasi-isomorphism]] of [[BV-BRST complexes]])**

Let

$$
  CE\left(  E/(\mathcal{G} \times_\Sigma T\Sigma)_{\delta_{EL} L \simeq 0} \right)
  \;=\;
  \left(
    \Omega^{0,0}_\Sigma\left(
      T^\ast_{\Sigma,inf}[-1]\left(E \times_\Sigma \mathcal{G}[1]\right) \times_\Sigma T \Sigma[1]
    \right)
    \;,\;
    d_{CE}
    =
    \underset{s}{
    \underbrace{
      \left\{
        -\mathbf{L} + \mathbf{L}_{BRST}
        \,,\,
        -
      \right\}
    }
    }
    \;+\;
    d
  \right)
$$

be a  [[local BV-BRST complex]] of a [[Lagrangian field theory]] $(E,\mathbf{L})$ (example \ref{LocalBVBRSTComplexIsDerivedCriticalLocusOfEulerLagrangeForm}).

Let moreover $A \overset{aux}{\longrightarrow} \Sigma$ be any [[auxiliary field bundle]] (def. \ref{AuxiliaryFields}).
Then on the [[fiber product]] of the original [[field bundle]] $E$ and the shifted [[gauge parameter bundle]] $\mathcal{G}[1]$ with the [[auxiliary field bundle]] $A$
the sum of the original [[BV-Lagrangian density]] $-\mathbf{L} + \mathbf{L}_{BRST}$ with the
auxiliary Lagrangian density $\mathbf{L}_{aux}$ (eq:LagrangianDensityForAuxiliaryFields)
induce a new [[differential graded-commutative superalgebra]]:

$$
  \begin{aligned}
  & CE\left( E/(\mathcal{G} \times_\Sigma (A \times_\Sigma A[-1]) \times_\Sigma T \Sigma)^{aux}_{\delta_{EL} L \simeq 0} \right)
  \\
  & \coloneqq\;
  \left(
    \Omega^{0,0}_\Sigma\left(
      T^\ast_{\Sigma,inf}[-1]
      \left(
         E \times_\Sigma \mathcal{G}[1] \times_\Sigma \left( A \times_\Sigma A[-1]\right) \right) \times_\Sigma T \Sigma[1]
    \right)
    \;,\;
    d_{CE}
    =
    \underset{s}{
    \underbrace{
      \left\{
        \left( - L + L_{BRST} + \mathbf{L}_{aux} \right) dvol_\Sigma
        \,,\,
        -
      \right\}
    }
    }
    \;+\;
    d
  \right)
  \end{aligned}
$$

with generators

$$
  \array{
    \text{fields} & \phi^a & E &  \phi^\ddagger_a & \text{antifields}
    \\
    \\
    \text{ghost fields} & c^\alpha & \mathcal{G}[1] & c^\ddagger_\alpha & \array{ \text{antifields of} \\ \text{ghost fields} }
    \\
    \\
    \text{ auxiliary fields } & b^i & A & b^\ddagger_i & \array{ \text{antifields of} \\ \text{auxiliary fields} }
    \\
    \\
    \text{ antighost fields } & \overline{c}^i & A[-1] & \overline{c}^{\ddagger}_i & \array{ \text{antifields of} \\ \text{antighost fields} }
  }
$$

Moreover, the [[differential graded-commutative superalgebra]] of [[auxiliary fields]] and their [[antighost fields]] is a [[contractible chain complex]]

$$
  \left(
    \Omega^{0,0}_\Sigma( A \times_{\Sigma} A[-1] )
    \,,\,
    d_{CE} = \left\{ \overline{c}^\ddagger_i b^i \, dvol_\Sigma \,,\, - \right\}
  \right)
    \overset{\simeq_{qi}}{\longrightarrow}
  0
$$

and thus the canonical inclusion map

$$
  CE\left( E/(\mathcal{G} \times_\Sigma \times_\Sigma T \Sigma)_{\delta_{EL} L \simeq 0} \right)
    \overset{\phantom{AA} \simeq_{qi} \phantom{aa}}{\hookrightarrow}
  CE\left( E/(\mathcal{G} \times_\Sigma (A \times_\Sigma A[-1]) \times_\Sigma T \Sigma)^{aux}_{\delta_{EL} L \simeq 0} \right)
$$

(of the original [[BV-BRST complex]] into its [[tensor product]] with that for the [[auxiliary fields]] and their [[antighost fields]])
is a [[quasi-isomorphism]].

=--

+-- {: .proof}
###### Proof

From (eq:BVDifferentialOnauxiliaryFields) we read off that

1. the map $s_{aux} \coloneqq \left\{ \mathbf{L}_{aux},- \right\}$ is a [[differential]] (squares to zero), and
   the auxiliary [[Lagrangian density]] satisfies its [[classical master equation]] (remark \ref{ClassicalMasterEquationLocal}) strictly

   $$
      \{\mathbf{L}_{aux}, \mathbf{L}_{aux}\} = 0
   $$

1. the [[cochain cohomology]] of this differential is trivial:

   $$
     H^\bullet( s_{aux} )\;=\;0
   $$

1. The [[local antibracket]] of the [[BV-Lagrangian density]] with the auxiliary Lagrangian density vanishes:

   $$
     \left\{
       - \mathbf{L} + \mathbf{L}_{BRST}
       \,,\,
       \mathbf{L}_{aux}
     \right\}
     \;=\;
     0
   $$

Together this implies that the sum $-\mathbf{L} + \mathbf{L}_{BRST} + \mathbf{L}_{aux}$ satisfies the [[classical master equation]] (remark \ref{ClassicalMasterEquationLocal})

$$
  \left\{
    \left(
    - \mathbf{L} + \mathbf{L}_{BRST} + \mathbf{L}_{aux}
    \right)
    \,,\,
    \left(
    - \mathbf{L} + \mathbf{L}_{BRST} + \mathbf{L}_{aux}
    \right)
  \right\}
  \;=\;
  0
$$

and hence that

$$
  s + s_{aux}
  \;\coloneqq\;
  \left\{
    - \mathbf{L} + \mathbf{L}_{BRST} + \mathbf{L}_{aux}
    \,,\,
    -
  \right\}
$$

is indeed a [[differential]]; such that its [[cochain cohomology]] is identified with that of $s = \left\{-\mathbf{L} + \mathbf{L}_{BRST},-\right\}$ under the canonical inclusion map.

=--

+-- {: .num_remark #FieldBundleBVBRST}
###### Remark
**([[gauge fixing|gauge fixed]] [[BV-BRST formalism|BV-BRST]] [[field bundle]])**

In conclusion, we have that, given

1. $(E,\mathbf{L})$ a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), with [[field bundle]] $E$ (def. \ref{FieldsAndFieldBundles});

1. $\mathcal{G}$ a choice of [[gauge parameters]] (def. \ref{GaugeParameters}), 

   hence 

   $\mathcal{G}[1]$ a choice of [[ghost fields]] (example \ref{LocalOffShellBRSTComplex});

1. $A$ a choice of [[auxiliary fields]] (def. \ref{AuxiliaryFields}), 

   hence 

   $A[-1]$ a choice of [[antighost fields]] (def. \ref{AuxiliaryFields})

1. $T^\ast_{\Sigma,inf}[-1](\cdots)$ the corresponding [[antifields]] (def. \ref{InfinitesimalCotangentBundleOfFieldAndGaugeParameterBundle})

1. a [[gauge fixing Lagrangian density]] $\mathbf{L}_{gf}$ (def. \ref{GaugeFixingLagrangianDensity}) 

then the result is a new [[Lagrangian field theory]]

$$
  \left( E_{\text{BV-BRST}}, \mathbf{L}' \right)
$$

now with [[graded manifold|graded]] [[field bundle]] (remark \ref{dgManifolds}) the [[fiber product]]

$$
  E_{\text{BV-BRST}}
  \;\coloneqq\;
  \underset{
    \array{ \text{anti-} \\ \text{fields} }
  }{
  \underbrace{
  T^\ast_{\Sigma,inf}
  }
  }
  \left(
    \underset{\text{fields}}{\underbrace{E}}
      \times_\Sigma 
    \underset{ \array{ \text{ghost} \\ \text{fields} }}{\underbrace{\mathcal{G}[1]}}
       \times_\Sigma
    \underset{\array{ \text{auxiliary} \\ \text{fields} }}{\underbrace{A}}
       \times_{\Sigma}
    \underset{ \array{ \text{antighost} \\ \text{fields} } }{\underbrace{A[-1]}}
  \right)
$$

and with [[Lagrangian density]] $\mathbf{L'}$ independent of the [[antifields]], but complemented by an auxiliary Lagrangian density $\mathbf{L}'_{BRST}$. 

The key point being that $\mathbf{L}'$ admits a [[covariant phase space]] (while $\mathbf{L}$ may not), while in [[BV-BRST cohomology]] both theories still have the same gauge-invariant on-shell observables.

=--

$\,$

**Gauge fixed electromagnetic field**
 {#GaugeFixingExamples}

As an example of the general theory of BV-BRST [[gauge fixing]] above we now discuss the gauge fixing of the [[electromagnetic field]].

+-- {: .num_example #NLGaugeFixingOfElectromagnetism}
###### Example
**([[Gaussian-averaged Lorenz gauge]] [[gauge fixing|fixing]] of [[vacuum]] [[electromagnetism]])**

Consider the [[local BV-BRST complex]] for the [[free field theory|free]] [[electromagnetic field]] on [[Minkowski spacetime]] from example \ref{LocalBVComplexOfVacuumElectromagnetismOnMinkowskiSpacetime}:

The [[field bundle]] is $E \coloneqq T^\ast \Sigma$ and the [[gauge parameter bundle]]  is $\mathcal{G} \coloneqq \Sigma \times \mathbb{R}$.
The 0-jet field coordinates are

$$
  \array{
    & c^\ddagger & (a^\ddagger)^\mu & a_\mu & c
    \\
    deg =
    &
    -2 & -1 & 0 & 1
  }
$$

the [[Lagrangian density]] is (eq:ElectromagnetismLagrangian)

$$
  \label{VacuumEMLagrangianDensityRecalledForNLFields}
  \mathbf{L}_{EM} \coloneqq \tfrac{1}{2} f_{\mu \nu} f^{\mu \nu}
$$

and the [[BV-BRST differential]] acts as:

$$
  \array{
    & &\array{ \text{BV-BRST} \\ \text{differential} }&
    \\
    \array{
       \text{ electromagnetic field }
       \\
       \text{ ("vector potential") }
    }
    & a_\mu &\mapsto& c_{,\mu} & \text{gauge transformation}
    \\
    \phantom{A}
    \\
      \text{ ghost field }
    & c &\mapsto& 0 & \text{abelian Lie algebra}
    \\
    \phantom{A}
    \\
    \array{
      \text{antifield of}
      \\
      \text{electromagnetic field}
    }
    & (a^\ddagger)^\mu &\mapsto&  f^{\nu \mu}_{,\nu}  & \text{equations of motion}
    \\
    \phantom{A}
    \\
    \array{
      \text{antifield of}
      \\
      \text{ghostfield}
    }
    & c^\ddagger &\mapsto& (a^\ddagger)^\mu_{,\mu} & \text{Noether identity}
    \\
    \phantom{A}
    \\
      \text{Nakanishi-Lautrup field}
    &
    b &\mapsto& 0 & \text{vanishing of auxiliary fields...}
    \\
    \phantom{A}
    \\
    \text{antighost field}
    &
    \overline{c} &\mapsto& b & \text{... in cohomology}
    \\
    \phantom{A}
    \\
    \array{
      \text{antifield of}
      \\
      \text{ Nakanishi-Lautrup field }
    }
    &
    b^\ddagger &\mapsto& -\overline{c}^\ddagger
    &
    \text{vanishing of antifields of auxiliary fields...}
    \\
    \phantom{A}
    \\
    \array{
      \text{antifield of}
      \\
      \text{antighost field}
    }
    &
    \overline{c}^\ddagger &\mapsto& 0
    &
    \text{... in cohomology}
  }
$$


Introduce a [[trivial vector bundle|trivial]] [[real line bundle]] for [[auxiliary fields]] $b$
in degree 0 and their [[antighost fields]] $\overline{c}$ (def. \ref{AuxiliaryFields}) in degree -1:

$$
  \array{
    &
    \Sigma \times \langle \overline{c}\rangle
      &\overset{ \overline{c} \mapsto b}{\longrightarrow}&
    \Sigma \times\langle b\rangle
    \\
    deg = & -1 && 0
  }
  \,.
$$

In the present context the [[auxiliary field]] $b$ is called the _[[abelian Lie algebra|abelian]] [[Nakanishi-Lautrup field]]_.

The corresponding [[BV-BRST complex]] with [[auxiliary fields]] adjoined,
which, by prop. \ref{QuasiIsomorphismAdjoiningAuxiliaryFields}, is [[quasi-isomorphism|quasi-isomorphic]] to the original one above,
has coordinate generators

$$
  \array{
    & c^\ddagger & (a^\ddagger)^\mu & a_\mu & c
    \\
    & & \overline{c} & b
    \\
    & & b^{\ddagger} & \overline{c}^\ddagger
    \\
    deg =
    &
    -2 & -1 & 0 & 1
  }
  \,.
$$

and [[BV-BRST differential]] given by the [[local antibracket]] (def. \ref{LocalAntibracket}) with $-\mathbf{L}_{EM} + \mathbf{L}_{BRST} + \mathbf{L}_{aux}$:

$$
  s
  \;=\;
  \left\{
    \left(
    - \underset{ = L_{EM}}{\underbrace{\tfrac{1}{2}f_{\mu \nu} f^{\mu \nu}}}
    +
    \underset{ = L_{BRST} }{\underbrace{ c_{,\mu} (a^\ddagger)^\mu }}
    +
    \underset{ = L_{aux} }{\underbrace{ b \overline{c}^{\ddagger} }}
    \right)
    dvol_\Sigma
    \,,\,
    (-)
  \right\}
$$

We say that the [[gauge fixing Lagrangian]] (def. \ref{GaugeFixingLagrangianDensity}) for [[Gaussian-averaged Lorenz gauge]]_ for the [[electromagnetic field]]

$$
  \mathbf{L}_{gf}
  \;\in\;
  \Omega^{p+1}_\Sigma\left(
    E \times_\Sigma \mathcal{G}[1] \times_\Sigma A \times_\Sigma A[-1]
  \right)
  \,.
$$

is given by ([Henneaux 90 (103a)](Nakanishi-Lautrup+field#Henneaux90))

$$
  \label{GaugeFixingLagrangianForGaussianAveragedLorentzGauge}
  \mathbf{L}_{gf}
  \;\coloneqq\;
  \underset{deg = -1}{
  \underbrace{
    \phantom{A}\overline{c}\phantom{A}
  }}
  \underset{deg = 0}{\underbrace{( b - a^{\mu}_{,\mu} )}} \, dvol_\Sigma
  \,.
$$

We check that this really is a [[gauge fixing Lagrangian density]] according to def. \ref{GaugeFixingLagrangianDensity}:

From (eq:VacuumEMLagrangianDensityRecalledForNLFields) and (eq:GaugeFixingLagrangianForGaussianAveragedLorentzGauge) we find the [[local antibracket|local antibrackets]] (def. \ref{LocalAntibracket}) with this [[gauge fixing Lagrangian density]] to be

$$
  \begin{aligned}
    \left\{\mathbf{L}_{gf}\,,\,\left( - \mathbf{L}_{EM} + \mathbf{L}_{BRST} +  \mathbf{L}_{aux} \right) \right\}
    & =
    \left\{
      \overline{c}\left( b - a^\mu_{,\mu}\right) \, dvol_\Sigma
      \,,\,
      \left(
        -\tfrac{1}{2}f_{\mu \nu}f^{\mu \nu}
        +
        c_{,\mu} (a^\ddagger)^\mu
        +
        b \overline{c}^\ddagger
      \right)
      dvol_\Sigma
    \right\}
    \\
    & =
    \left\{
      \overline{c}\left( b - a^\mu_{,\mu}\right) \, dvol_\Sigma
      \,,\,
      b \overline{c}^{\ddagger} \, dvol_\Sigma
    \right\}
    +
    \left\{
      \overline{c}\left( b - a^\mu_{,\mu}\right) \, dvol_\Sigma
      \,,\,
      c_{,\mu} (a^{\ddagger})^\mu \, dvol_\Sigma
    \right\}
    \\
    & =
    -
    \left(
       b ( b - a^{\mu}_{,\mu} ) + \overline{c}_{,\mu} c^{,\mu}
    \right)
    \, dvol_\Sigma
    \\
    \phantom{A}
    \\
   \{ \mathbf{L}_{gf}, \{ \mathbf{L}_{gf} , (-\mathbf{L} + \mathbf{L}_{BRST} + \mathbf{L}_{aux}  )\}\}
   & = 0
  \end{aligned}
$$

(So we are in the traditional situation of example \ref{GaugeFixingViaAntiLagrangianSubspaces}.)

Therefore the corresponding [[gauge fixing|gauge fixed]] [[Lagrangian density]]  (eq:GaugeFixedLagrangianDensity) is (see also [Henneaux 90 (103b)](Nakanishi-Lautrup+field#Henneaux90)):

$$
\label{GaussianAveragedLorentzianGaugeFixOfElectromagneticFieldOnMinkowskiSpacetime}
  \begin{aligned}
    -\mathbf{L}' + \mathbf{L}'_{BRST}
      & \coloneqq
     e^{\left\{ \mathbf{L}_{gf} ,-\right\}}\left( -\mathbf{L}_{EM} + \mathbf{L}_{BRST} + \mathbf{L}_{aux}  \right)
    \\
    & =
    -
    \underset{
      = \mathbf{L}'
    }{
    \underbrace{
    \left(
      \underset{ = L_{EM} }{
        \underbrace{
          \tfrac{1}{2} f_{\mu \nu} f^{\mu \nu}
        }
      }
      +
      \underset{ = -\left\{ L_{gf}, L_{BRST} + L_{aux} \right\} }{
        \underbrace{
          b ( b - a^{\mu}_{,\mu} )
          +
          \overline{c}_{,\mu} c^{,\mu}
        }
      }
    \right) dvol_\Sigma
    }
    }
    \;+\;
    \underset{ = \mathbf{L}'_{BRST} }{
      \underbrace{
        \left(
          \underset{ = L_{BRST} }{
            \underbrace{
              c_{,\mu} (a^\ddagger)^\mu
            }
          }
          +
          \underset{ = L_{aux} }{
            \underbrace{
              b \overline{c}^\ddagger
            }
          }
        \right)
        dvol_\Sigma
      }
    }
  \end{aligned}
  \,.
$$


The [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] (def.
 \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime})
induced by the gauge fixed Lagrangian density $\mathbf{L}'$ at antifield degree 0 are (using (eq:ElectromagneticFieldEulerLagrangeForm)):

$$
  \label{LorenzGaugeFixedEOMForVacuumElectromagnetism}
  \delta_{EL} \mathbf{L}' \;=\; 0
  \phantom{AAA}
  \Leftrightarrow
  \phantom{AAA}
  \left\{
  \begin{aligned}
    -\frac{d}{d x^\mu} f^{\mu \nu} & =  b^{,\nu}
    \\
    b & = \tfrac{1}{2} a^\mu_{,\mu}
    \\
    c_{,\mu}{}^{,\mu} & = 0
    \\
    \overline{c}_{,\mu}{}^{,\mu} & = 0
  \end{aligned}
  \right.
  \phantom{AAA}
  \Leftrightarrow
  \phantom{AAA}
  \left\{
  \begin{aligned}
    \Box a^\mu & = 0
    \\
    b & = \tfrac{1}{2} div a
    \\
    \Box c & = 0
    \\
    \Box \overline{c} & = 0
  \end{aligned}
  \right.
$$

(e.g. [Rejzner 16 (7.15) and (7.16)](Nakanishi-Lautrup+field#Rejzner16)).

(Here in the middle we show the equations as the appear directly from the [[Euler-Lagrange variational derivative]]
(prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}).
The [[differential operator]] $\Box = \eta^{\mu \nu} \frac{d}{d x^\mu} \frac{d}{d x^\nu} $ on the right is the [[wave operator]] (example \ref{EquationOfMotionOfFreeRealScalarField})
and $div$ denotes the [[divergence]].
The equivalence to the equations on the right follows from using in the first equation the derivative of the second equation
on the left, which is $b^{,\nu} = \tfrac{1}{2} a^{\mu,\nu}{}_{,\mu}$
and recalling the definition of the universal [[Faraday tensor]] (eq:FaradayTensorJet):
$\frac{d}{d x^\mu} f^{\mu \nu} = \tfrac{1}{2} \left( a^{\nu,\mu}{}_{,\mu} - a^{\mu,\nu}{}_{,\mu} \right)$.)


Now the [[differential equations]] for [[gauge fixing|gauge-fixed]] [[electromagnetism]] on the right in (eq:LorenzGaugeFixedEOMForVacuumElectromagnetism) are
nothing but the [[wave equations]] [[equations of motion|of motion]] of $(p+1) + 1 + 1$ [[free field theory|free]] [[mass|massless]] [[scalar fields]] (example \ref{EquationOfMotionOfFreeRealScalarField}).

As such, by example \ref{GreenHyperbolicKleinGordonEquation} they are a system of [[Green hyperbolic differential equations]] (def. \ref{GreenHyperbolicDifferentialOperator}),
hence admit [[Cauchy surfaces]] (def. \ref{CauchySurface}).

Therefore (eq:GaussianAveragedLorentzianGaugeFixOfElectromagneticFieldOnMinkowskiSpacetime) indeed is a [[gauge fixing]] of
the [[Lagrangian density]] of the [[electromagnetic field]] on [[Minkowski spacetime]] according to def. \ref{GaugeFixingLagrangianDensity}.

The gauge-fixed [[BRST operator]] induced from the gauge fixed Lagrangian density (eq:GaussianAveragedLorentzianGaugeFixOfElectromagneticFieldOnMinkowskiSpacetime) acts as

$$
  \label{GaussianAveragedLorentzGaugeFixedBRSTOperator}
  \array{
    & \array{ s'_{BRST} = \\ \left\{ \left( c_{,\mu} (a^\ddagger)^\mu + b \overline{c}^{\ddagger}\right) dvol_\Sigma, (-)  \right\}  }
    \\
    a_\mu &\mapsto& c_{,\mu}
    \\
    b &\mapsto& 0
    \\
    \overline{c} &\mapsto & b
  }
$$

=--

From this we immediately obtain the [[propagators]] for the gauge-fixed [[electromagnetic field]]:

+-- {: .num_prop #PhotonPropagatorInGaussianAveragedLorenzGauge}
###### Proposition
**([[photon propagator]] in [[Gaussian-averaged Lorenz gauge]])**

After [[gauge fixing|fixing]] [[Gaussian-averaged Lorenz gauge]] (example \ref{NLGaugeFixingOfElectromagnetism}) of the [[electromagnetic field]] on [[Minkowski spacetime]], the [[causal propagator]] (prop. \ref{GreenFunctionsAreContinuous}) of the combined [[electromagnetic field]] and [[Nakanishi-Lautrup field]] is of the form

$$
  \Delta^{EM, EL}
  \;=\;
  \left(
    \array{
      \Delta^{photon} & \ast
      \\
      \ast & \ast
    }
  \right)
$$

with

$$
  \Delta^{photon}_{\mu \nu}(x,y)
  \;=\;
  \eta_{\mu \nu} \Delta(x,y)
  \,,
$$

where

1. $\eta_{\mu \nu}$ is the [[Minkowski metric]] [[tensor]] (def. \ref{MinkowskiSpacetime});

1. $\Delta(x,y)$ is the [[causal propagator]] of the [[free field theory]] [[mass|massless]] [[real scalar field]] (prop. \ref{ModeExpansionOfCausalPropagatorForKleinGordonOnMinkowski}).

Accordingly the [[Feynman propagator]] of the [[electromagnetic field]] in [[Gaussian-averaged Lorenz gauge]] is

$$
  (\Delta^{photon}_F)_{\mu \nu}(x,y)
  \;=\;
  \eta_{\mu \nu} \Delta_F(x,y)
  \,,
$$

where on the right $\Delta_F(x,y)$ is the [[Feynman propagator]] of the [[free field theory|free]] [[mass|massless]] [[real scalar field]] (def. \ref{FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime}).

This is also called the _[[photon propagator]]_.

Hence by prop. \ref{FeynmanPropagatorAsACauchyPrincipalvalue} the [[Fourier transform of distributions|distributional Fourier transform]] of the photon propagator is

$$
  \widehat{\Delta^{photon}_F}_{\mu \nu}(k)
  \;=\;
  \frac{1}{- k^\mu k_\mu + i 0^+}
  \,.
$$

=--

(this is a special case of [Khavkine 14 (99)](gauge+fixing#Khavkine14), see also [Rejzner 16, (7.20)](perturbative+algebraic+quantum+field+theory#Rejzner16))

+-- {: .proof}
###### Proof

The Gaussian-averaged Lorenz gauge-fixed equations of motion (eq:LorenzGaugeFixedEOMForVacuumElectromagnetism) of the electromagnetic field are just $(p+1)$ uncoupled [[mass|massless]] [[Klein-Gordon equations]], hence [[wave equations]] (example \ref{EquationOfMotionOfFreeRealScalarField}) for the $(p+1)$ real components of the [[electromagnetic field]] ("[[vector potential]]")

$$
  \Box A_\mu = 0\phantom{AAAA} \mu \in \{0,1,\cdots, p\}
  \,.
$$

This shows that the propoagator is proportional to that of the [[real scalar field]]. 

To see that the index structure is as claimed, recall that the [[domain]] and [[codomain]] of the [[advanced and retarded propagators]] in def. \ref{AdvancedAndRetardedGreenFunctions} is 

$$
  \array{
    \Gamma_\Sigma(T\Sigma) 
      &\overset{\left( (\mathrm{G}_{\pm})_{\mu \nu} \right)}{\longrightarrow}&
    \Gamma_\Sigma(T^\ast \Sigma)
  }
$$

corresponding to a [[differential operator]] for the [[equations of motion]] which by (eq:ElectromagneticFieldEulerLagrangeForm) and (eq:LorenzGaugeFixedEOMForVacuumElectromagnetism) is given by

$$
  \array{
    \Gamma_\Sigma(T^\ast \Sigma)
      &\overset{ \eta^{-1} \circ \Box }{\longrightarrow}&
    \Gamma_\Sigma(T \Sigma)
    \\
    A_\mu &\mapsto& \eta^{\mu \nu} \Box A_\nu
  }
$$

Then the defining equation (eq:AdvancedRetardedGreenFunctionIsRightInverseToDiffOperator) for the [[advanced and retarded Green functions]] is, in terms of their [[integral kernels]], the [[advanced and retarded propagators]] $\Delta_{\pm}$

$$
  \eta^{\mu' \mu} \Box \underset{y \in X}{\int} (\Delta_{\pm})_{\mu \nu}((-),y) A^{\nu}(y) \, dvol_\Sigma(x)
  =
  A^\nu(x)
  \,.
$$

This shows that

$$
  (\Delta_{\pm})_{\mu \nu}
  \;=\;
  \eta_{\mu\nu} \Delta_{\pm}
$$

with $\Delta_{\pm}$ the [[advanced and retarded propagator]] of the [[free field theory|free]] [[real scalar field]] on [[Minkowski spacetime]] (prop. \ref{AdvancedRetardedPropagatorsForKleinGordonOnMinkowskiSpacetime}), and hence


$$
  \begin{aligned}
    \Delta_{\mu \nu}
    &=
    (\Delta_+)_{\mu \nu}
    -
    (\Delta_-)_{\mu \nu}
    \\
    & =
    \eta_{\mu \nu} (\Delta_+ - \Delta_-)
    \\
    & =
    \eta_{\mu \nu} \Delta
  \end{aligned}
$$

=--

Next we compute the gauge-invariant on-shell polynomial observables of the electromagnetic field.  The result will involve the following concept:

+-- {: .num_defn #LinearObservablesOfElectromagenticFieldWavePolarization}
###### Definition
**([[wave polarization]] of linear [[observables]] of the [[electromagnetic field]])**

Consider the [[electromagnetic field]] on [[Minkowski spacetime]] $\Sigma$, with [[field bundle]] the [[cotangent bundle]]

The space of off-shell linear observables is spanned by the point evaluation observables

$$
  e^\mu \mathbf{A}_\mu(x)
  \;\in\;
  LinObs(T^\ast \Sigma)
$$

where

1. $e = (e^\mu) \in \mathbb{R}^{p,1}$ is some vector;

1. $x \in \mathbb{R}^{p,1}$ is some point in Minkowski spacetime

1. $\mathbf{A}_\mu(x) \;\colon\; A \mapsto A_\mu(x)$

   is the functional which sends a section $A \in \Gamma_\Sigma(E) = \Omega^1(\Sigma)$ to its $\mu$-component at $x$.

After [[Fourier transform of distributions]] this is

$$
  e^\mu \widehat{\mathbf{A}}_\mu(k)
  \;\in\;
  LinObs(T^\ast \Sigma)
$$

for $k = (k_\mu) \in (\mathbb{R}^{p,1})^\ast$ the _[[wave vector]]_

for $e = (e^\mu) \in \mathbb{R}^{p,1}$ the _[[wave polarization]]_

The linear [[on-shell]] observables are spanned by the same expressions, but subject to the condition that

$$
  {\vert k\vert}_\eta^2 = k^\mu k_\mu = 0
$$

hence

$$
  LinObs(T^\ast \Sigma,\mathbf{L}_{EM})
  \;=\;
  \left\langle
    e^\mu \widehat{\mathbf{A}}_\mu(k)
    \;\vert\;
    k^\mu k_\mu = 0
  \right\rangle
$$

We say that the space of _[[transversal polarization|transversally polarized]]_ linear on-shell observables
is the [[quotient vector space]]

$$
  \label{ElectromagneticFieldLinearObservablesTransversallyPolarized}
  LinObs(T^\ast \Sigma,\mathbf{L}_{EM})_{trans}
  \;\coloneqq\;
  \frac{
    \langle
      e^\mu \widehat{\mathbf{A}}_\mu(k)
      \;\vert\;
      k^\mu k_\mu = 0 \,\, \text{and} \,\, e^\mu k_\mu = 0
    \rangle
  }{
    \langle
      e^\mu \widehat{\mathbf{A}}_\mu(k)
      \;\vert\;
      k^\mu k_\mu = 0 \,\, \text{and} \,\, e_\mu \propto k_\mu
    \rangle
  }
$$

of those observables whose [[Fourier modes]] involve [[wave polarization]] vectors $e$ that vanish when contracted with the
[[wave vector]] $k$, modulo those whose [[wave polarization]] vector $e$ is proportional to the [[wave vector]].

For example if $k = (\kappa, 0, \cdots, \kappa)$, then the corresponding space of transversal polarization vectors may be identified
with $\left\{e \,\vert\, e =  (0,e_1, e_2, \cdots, e_{p-1}, 0) \right\}$.


=--

+-- {: .num_prop #GausianAveragedLorenzGaugeFixedLinearObservablesOfTheElectromagneticField}
###### Proposition
**([[BRST cohomology]] on linear [[on-shell]] [[observables]] of the [[Gaussian-averaged Lorenz gauge]] [[gauge fixing|fixed]] [[electromagnetic field]])**

After [[gauge fixing|fixing]] [[Gaussian-averaged Lorenz gauge]] (example \ref{NLGaugeFixingOfElectromagnetism}) of the [[electromagnetic field]] on [[Minkowski spacetime]], the global [[BRST cohomology]] (def. \ref{ComplexBVBRSTGlobal}) on the [[Gaussian-averaged Lorenz gauge]] [[gauge fixing|fixed]] (def. \ref{NLGaugeFixingOfElectromagnetism}) [[on-shell]] [[linear observables]] (def. \ref{LinearObservables}) at $deg_{gh} = 0$ (prop. \ref{DerivedCriticalLocusOfActionLiAlgebroidBicomplexStructure}) is [[isomorphism|isomorphic]] to the space of transversally polarized linear observables, def. \ref{LinearObservablesOfElectromagenticFieldWavePolarization}:

$$
  H^0( LinObs( T^\ast \Sigma \times_\Sigma  A \times_\Sigma A[-1] \times_\Sigma \mathcal{G}[1], \mathbf{L}' ),  s'_{BRST} )
  \;\simeq\;
  LinObs( T^\ast \Sigma, \mathbf{L}_{EM})_{trans}
  \,.
$$

=--

(e.g. [Dermisek 09 II-5, p. 325](wave+polarization#Dermisek09))

+-- {: .proof}
###### Proof


The gauge fixed BRST differential (eq:GaussianAveragedLorentzGaugeFixedBRSTOperator) acts on the [[Fourier modes]] of the linear observables (def. \ref{LinearObservables}) as follows

$$
  \array{
     & & s'_{BRST}
     \\
     \array{ \text{antighost} \\ \text{field} }
     &
     \widehat{\overline{\mathbf{C}}}(k)
     &\mapsto&
     \widehat{\mathbf{B}}(k)  & \array{ \text{Nakanishi-Lautrup} \\ \text{field} }
     \\
     \phantom{a}
     \\
     &&& \underset{\text{on-shell}}{=}
     \tfrac{i}{2} k^\mu \widehat{\mathbf{A}}_\mu(k)
     &
     \array{ \text{Lorenz gauge} \\ \text{condition} }
    \\
    \phantom{A}
    \\ 
    \array{ \text{electromagnetic} \\ \text{field} }
    &
    e^\mu \widehat{\mathbf{A}}_\mu(k)
      &\mapsto&
    i \left(e^\mu k_\mu\right) \widehat{\mathbf{C}}(k)
    &
    \array{
      \text{polarization contracted} 
      \\ 
      \text{with wave vector}
      \\
      \text{times ghost field}
    }
    \\
    \phantom{A}
    \\
    \array{ \text{Nakanishi-Lautrup} \\ \text{field} }
    & \widehat{\mathbf{B}}
    &\mapsto&
    0
  }
$$

This impies that the gauge fixed [[BRST cohomology]] on linear on-shell observables at $deg_{gh} = 0$ is the space of transversally polarized linear observables (def. \ref{LinearObservablesOfElectromagenticFieldWavePolarization}):


$$
  \label{LinearOnShellObservablesGaugeFixedBRSTCohomologyForEMField}
  \begin{aligned}
    H^0(LinObs(E,\mathbf{L}_{EM}), s'_{BRST})
    & =
    \left\langle
      \frac{
        \left\{
        e^\mu \widehat{\mathbf{A}}_{\mu}(k)
        \,\vert\, k^\mu k_\mu = 0 \,\,\text{and}\,\,0 = d_{BRST}\left( e^\mu \widehat{\mathbf{A}}_\mu(k)
 \right)  = i (e^\mu k_\mu) \widehat{\mathbf{C}}(k)
        \right\}
      }{
        \left\{
        e^\mu \widehat{\mathbf{A}}_\mu(k)
        \,\vert\, k^\mu k_\mu = 0 \,\,\text{and}\,\, e^\mu \widehat{\mathbf{A}}_\mu(k) \propto s'_{BRST}( \widehat{\overline{\mathbf{C}}}(k) ) = \tfrac{i}{2} k^\mu \widehat{ \mathbf{A} }_\mu(k)
        \right\}
      }
    \right\rangle
    \\
    & =
    \left\langle
    \frac{
      \left\{
        e^\mu \widehat{\mathbf{A}}_\mu(k) \,\vert \, k^\mu k_\mu = 0 \,\, \text{and} \,\, e^\mu k_\mu = 0
      \right\}
    }
    {
      \left\{
        e^\mu \widehat{\mathbf{A}}_\mu(k) \,\vert \, k^\mu k_\mu = 0 \,\, \text{and} \,\, e^\mu \propto k^\mu
      \right\}
    }
    \right\rangle
    \\
    & =
    LinObs(T^\ast \Sigma,\mathbf{L}_{EM})_{trans}
  \end{aligned}
$$

Here the first line is the definition of [[cochain cohomology]] (using that both $\widehat{\mathbf{B}}$ and $\widehat{\overline{\mathbf{C}}}$ are immediately seen to vanish in cohomology), the second line is spelling out the action of the BRST operator and using the on-shell relations (eq:LorenzGaugeFixedEOMForVacuumElectromagnetism) for $\widehat{\mathbf{B}}$ and the last line is by def. \ref{LinearObservablesOfElectromagenticFieldWavePolarization}.

=--

As a corollary we obtain:

+-- {: .num_prop #BRSTCohomologyOnPolynomialOnShellObservabledOfTheGaussianAveragedLorenzGaugeFixedElectromagneticField}
###### Proposition
**([[BRST cohomology]] on polynomial [[on-shell]] [[observables]] of the [[Gaussian-averaged Lorenz gauge]] [[gauge fixing|fixed]] [[electromagnetic field]])**

After [[gauge fixing|fixing]] [[Gaussian-averaged Lorenz gauge]] (example \ref{NLGaugeFixingOfElectromagnetism}) of the [[electromagnetic field]] on [[Minkowski spacetime]], the global [[BRST cohomology]] (def. \ref{ComplexBVBRSTGlobal}) on the [[Gaussian-averaged Lorenz gauge]] [[gauge fixing|fixed]] (def. \ref{NLGaugeFixingOfElectromagnetism}) polynomial on-shell observables (def. \ref{PolynomialObservables}) at $deg_{gh} = 0$ (prop. \ref{DerivedCriticalLocusOfActionLiAlgebroidBicomplexStructure}) is [[isomorphism|isomorphic]] to the distributional polynomial algebra on transversally polarized linear observables, def. \ref{LinearObservablesOfElectromagenticFieldWavePolarization}:

$$
  \label{EMBRSTCohomologyOnPolynomialOnShellObservables}
  H^0(PolyObs( T^\ast \Sigma \times_\Sigma \mathcal{G}[1] \times_\Sigma A \times_\Sigma A[-1] ,\mathbf{L}), s'_{BRST})
  \;\simeq\;
  Sym\left(
    LinObs(T^\ast \Sigma,\mathbf{L}_{EM})_{trans}
  \right)
$$

=--

+-- {: .proof}
###### Proof

Generally, if $(V^\bullet,d)$ is a cochain complex over a [[ground field]] of [[characteristic zero]]
(such as the [[real numbers]] in the present case) and $Sym(V^\bullet,d)$ the differential graded-[[symmetric algebra]] that it induces ([this example](symmetric+algebra#SymmetricAlgebraInCoChainComplexes)), then

$$
  H^\bullet(Sym(V,d)) = Sym(H^\bullet(V,d))
  \,.
$$

(by [this prop.](CochainCohomologyOfSymmetricAlgebraOnCochainComplex)).

=--

In conclusion we finally obtain:

+-- {: .num_prop #GaugeInvariantPolynomialOnShellObservablesOfFreeElectromagneticField}
###### Proposition
**(gauge-invariant polynomial [[on-shell]] [[observables]] of the [[free field theory]] [[electromagnetic field]])**

The [[BV-BRST cohomology]] on infinitesimal observables (def. \ref{LocalObservablesOnInfinitesimalNeighbourhood})
of the [[free field theory|free]] [[electromagnetic field]] on [[Minkowski spacetime]] (example \ref{LocalBVComplexOfVacuumElectromagnetismOnMinkowskiSpacetime}) at $deg_{gh} = 0$
is the distributional polynomial algebra in the transversally polarized linear on-shell observables, def. \ref{LinearObservablesOfElectromagenticFieldWavePolarization}, as in prop. \ref{BRSTCohomologyOnPolynomialOnShellObservabledOfTheGaussianAveragedLorenzGaugeFixedElectromagneticField}.

=--

+-- {: .proof}
###### Proof

By the classes of [[quasi-isomorphisms]] of prop. \ref{ExponentialOfLocalAntibracket} and prop. \ref{QuasiIsomorphismAdjoiningAuxiliaryFields} we may equivalently compute the cohomology if the [[BV-BRST complex]] with differential $s'$, obtained after [[Gaussian-averaged Lorenz gauge]] [[gauge fixing|fixing]] from example \ref{NLGaugeFixingOfElectromagnetism}. Since the [[equations of motion]] (eq:LorenzGaugeFixedEOMForVacuumElectromagnetism) are manifestly [[Green hyperbolic differential equations]] after this gauge fixing [[Cauchy surfaces]] for the [[equations of motion]] exist and hence prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces} together with prop. \ref{BVComplexIsHomologicalResolutionPreciselyIfNoNonTrivialImplicitGaugeSymmetres} implies that the gauge fixed BV-complex $s'_{BV}$ has its cohomology concentrated in degree zero on the [[on-shell]] observables. Therefore prop. \ref{CochainCohomologyOfBVBRSTComplexInDegreeZero} (i.e. the collapsing of the [[spectral sequence]] for the BV/BRST [[bicomplex]]) implies that the gauge fixed BV-BRST cohomology at ghost number
zero is given by the on-shell BRST-cohomology. This is characterized by prop. \ref{BRSTCohomologyOnPolynomialOnShellObservabledOfTheGaussianAveragedLorenzGaugeFixedElectromagneticField}.

=--



$\,$

This concludes our discussion of [[gauge fixing]]. With the [[covariant phase space]] for [[gauge theories]] obtained thereby,
we may finally pass to the [[quantization]] of field theory to [[quantum field theory]] proper, in the [next chapter](#Quantization).
