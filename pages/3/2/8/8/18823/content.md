
## Observables
 {#Observables}


Given a [[Lagrangian field theory]] (def. \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}), then a general _[[observable]] quantity_ or just _[[observable]]_ for short (def. \ref{Observable} below),  is a [[smooth function]]

$$
  A \;\colon\; \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0} \longrightarrow \mathbb{C}
$$

on the [[on-shell]] [[space of field histories]] (example \ref{DiffeologicalSpaceOfFieldHistories}, example \ref{SupergeometricSpaceOfFieldHistories})
hence a [[smooth function|smooth]] "[[functional]]" of field histories. We think
of this as assigning to each physically realizable field history $\Phi$ the value $A(\Phi)$ of the given quantity as exhibited by
that field history. For instance concepts like "average [[field strength]] in the compact spacetime region $\mathcal{O}$" should be
observables. In particular the _field [[amplitude]] at spacetime point $x$_ should be an observable, the "[[field observable]]" denoted $\mathbf{\Phi}^a(x)$.

Beware that in much of the literature on [[field theory]], these point-evaluation [[field observables]] $\mathbf{\Phi}^a(x)$
(example below \ref{PointEvaluationObservables}) are eventually referred to as "fields" themselves, blurring the distinction between

1. [[types]] of fields/[[field bundles]] $E$,

1. [[field histories]]/[[sections]] $\Phi$,

1. [[functions]] on the [[space of field histories]] $\mathbf{\Phi}^a(x)$.

In particular, the process of _[[quantization]]_ (discussed in _[Quantization](#Quantization)_ below)
affects the third of these concepts only, in that it [[deformation theory|deforms]] the [[associative algebra|algebra]] [[structure]]
on observables to a [[non-commutative algebra|non-commutative]] [[algebra of quantum observables]].
For this reason the [[field observables]] $\mathbf{\Phi}^a(x)$ are often referred to as _quantum fields_.
But to understand the conceptual nature of [[quantum field theory]] it is important that the
$\mathbf{\Phi}^a(x)$ are really the _[[observables]]_ or _[[quantum observables]]_ on the [[space of field histories]].

**[[field (physics)|fields]]**

| aspect | [[term]] | [[type]] |  description | def. |
|--|------------|-|---------|----|
| [[field bundle|field component]] | $\phi^a$, $\phi^a_{,\mu}$ |  $J^\infty_\Sigma(E) \to \mathbb{R}$ |[[coordinate function]] on [[jet bundle]] of [[field bundle]] | def. \ref{FieldsAndFieldBundles}, def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime} |
| [[field history]] | $\Phi$, $\frac{\partial \Phi}{\partial x^\mu}$ | $\Sigma \to J^\infty_\Sigma(E)$  | [[jet prolongation]] of [[section]] of [[field bundle]] | def. \ref{FieldsAndFieldBundles}, def. \ref{JetProlongation}  |
| [[field observable]] | $\mathbf{\Phi}^a(x)$, $\partial_{\mu} \mathbf{\Phi}^a(x),   $ | $\Gamma_{\Sigma}(E) \to \mathbb{R}$  | [[derivative of a distribution|derivatives]] of [[delta-distribution|delta]]-[[functional]] on [[space of sections]] | def. \ref{Observable}, example \ref{PointEvaluationObservables} |
| averaging of [[field observable]] | $\alpha^\ast \mapsto \underset{\Sigma}{\int} \alpha^\ast_a(x) \mathbf{\Phi}^a(x) \, dvol_\Sigma(x)$ | $\Gamma_{\Sigma,cp}(E^\ast) \to Obs(E_{scp},\mathbf{L})$ |  [[operator-valued distribution|observable-valued distribution]]  | def. \ref{RegularLinearFieldObservables} |
| [[algebra of quantum observables]] | $\left( Obs(E,\mathbf{L})_{\mu c},\, \star\right)$  | $\mathbb{C}Alg$  | [[non-commutative algebra]] [[structure]] on [[field observables]] | def. \ref{WickAlgebraOfFreeQuantumField}, def. \ref{GeneratingFunctionsForCorrelationFunctions} |

$\,$

There are various further conditions on [[observables]] which we will eventually consider, forming subspaces of
_[[gauge invariant]] observables_ (def. \ref{GaugeInvariantFunctionsIntermsOfLieAlgebroids}),
_[[local observables]]_ (def. \ref{LocalObservables} below), _Hamiltonian local observables_ (def. \ref{HamiltonianLocalObservables} below) and _[[microcausal functional|microcausal observables]]_ (def. \ref{MicrocausalFunctionals}). While in the end it is
only these special kinds of observables that matter, it is useful to first consider the unconstrained concept
and then consecutively characterize smaller subspaces of well-behaved observables.
In fact it is useful to consider yet more generally the observables on the full [[space of field histories]]
(not just the [[on-shell]] subspace), called the _off-shell observables_.


In the case that the [[field bundle]] is a [[vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}),
the [[off-shell]] [[space of field histories]]
is canonically a [[vector space]] and hence it makes sense to consider _[[linear map|linear]]_ off-shell observables, i.e.
those observables $A$ with $A(c \Phi) = c A(\Phi)$ and $A(\Phi_1 + \Phi_2) = A(\Phi_1) + A(\Phi_2)$.
It turns out that these are precisely the _[[compactly supported distributions]]_ in the sense of [[Laurent Schwartz]]
(prop. \ref{LinearObservablesAreTheCompactlySupportedDistributions} below).
This fact makes powerful tools from [[functional analysis]] and [[microlocal analysis]] available for the analysis of [[field theory]]
(discussed [below](#MicrolocalAnalysisAndUltravioletDivergence)).

More generally there are the [[multilinear map|multilinear]] off-shell observables, and these are analogously given by
_[[distributions of several variables]]_ (def. \ref{PolynomialObservables} below). In fully [[perturbative quantum field theory]]
one considers only the [[infinitesimal neighbourhood]] (example \ref{InfinitesimalNeighbourhood}) of a single [[on-shell]] [[field history]]
and in this case all [[observables]] are in fact given by such multilinear observables (def. \ref{LocalObservablesOnInfinitesimalNeighbourhood} below).

For a [[free field theory]] (def. \ref{FreeFieldTheory}) whose [[Euler-Lagrange equations|Euler-Lagrange]] [[equations of motion]] are given by a [[linear differential operator]] which behaves well in that it is  "[[Green hyperbolic differential operator|Green hyperbolic]]" (def. \ref{GreenHyperbolicDifferentialOperator} below) it follows that the actual [[on-shell]] [[linear observables]] are equivalently those off-shell observables which are
_spatially [[compactly supported distribution|compactly supported]] [[distributional solution of a PDE|distributional solutions]]_ to the [[formally adjoint differential operator|formally adjoint]]
[[equation of motion]] (prop. \ref{DistributionsOnSolutionSpaceAreTheGeneralizedPDESolutions} below);
and this equivalence is exhibited by [[composition]] with the _[[causal Green function]]_
(def. \ref{AdvancedAndRetardedGreenFunctions} below):

This is theorem \ref{LinearObservablesForGreeFreeFieldTheoryAreDistributionalSolutionsToTheEquationsOfMotion} below,
which is pivotal for passing from [[classical field theory]] to [[quantum field theory]]:

$$
  \left\{
    \,\,
    \array{
      \text{polynomial}
      \\
      \text{on-shell}
      \\
      \text{observables}
    }
    \,\,
  \right\}
    \underoverset{\simeq}{\text{restriction}}{\longleftarrow}
  \left\{
    \array{
      \text{polynomial}
      \\
      \text{off-shell}
      \\
      \text{observables}
      \\
      \text{modulo equations of motion}
    }
  \right\}
    \underoverset{\simeq}{\text{causal propagator}}{\longleftarrow}
  \left\{
    \array{
      \text{spatially compactly supported}
      \\
      \text{distributions in several variables}
      \\
      \text{which are distributional solutions}
      \\
      \text{to the adjoint equations of motion}
    }
  \right\}
$$

This fact makes, in addition, the distributional analysis of [[linear differential equations]]
available for the analysis of [[free field theory]], notably the theory of _[[propagators]]_, such as _[[Feynman propagators]]_ (def. \ref{FeynmanPropagatorForKleinGordonEquationOnMinkowskiSpacetime} below), which we turn to
in _[Propagators](#Propagators)_ below.

The [[functional analysis]] and [[microlocal analysis]] ([below](#MicrolocalAnalysisAndUltravioletDivergence)) of linear [[observables]] re-expressed in [[distribution|distribution theory]]
via theorem \ref{LinearObservablesForGreeFreeFieldTheoryAreDistributionalSolutionsToTheEquationsOfMotion} solves the
issues that the original formulation of [[perturbative quantum field theory]] by [[Schwinger-Tomonaga-Feynman-Dyson]] in the 1940s
was notorious for suffering from ([Feynman 85](Schwinger-Tomonaga-Feynman-Dyson#Feynman85SuchABunchOfWords)): The [[normal ordered product]] of
quantum observables in a [[Wick algebra]] of observables follows from [[Hörmander's criterion]] for the [[product of distributions]]
to be well-defined (this we discuss in _[Free quantum fields](#FreeQuantumFields)_ below) and the
_[[renormalization]]_ freedom in the construction of the [[S-matrix]] is governed by the mechanism of
_[[extensions of distributions]]_ (this we discuss in _[Renormalization](#Renormalization)_ below).


Among the polynomial on-shell observables characterized this way, the focus is furthermore on the _[[local observables]]_:

In _[[local field theory]]_ the idea is that both the [[equations of motion]] as well as the observations
are fully determined by their restriction to [[infinitesimal neighbourhoods]] of spacetime points ([[events]]).
For the equations of motion this means that they are [[partial differential equations]] as we have seen
[above](#EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime). For the observables
it should mean that they must be averages over regions of spacetime of functions of the value of the field histories and their derivatives
_at any point_ of spacetime.
Now a "smooth function of the value of the field histories and their derivatives at any point"
is precisely a smooth function on the [[jet bundle]] of the [[field bundle]] (example \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
pulled back via [[jet prolongation]] (def. \ref{JetProlongation}).
If this is to be averaged over spacetime it needs to be the coefficient of a horizontal $p+1$-form (prop. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}).

In mathematical terminology these desiderata say that the [[local observables]] in a local field theory should be precisely the
"[[transgression of variational differential forms|transgressions]]" (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces} below) of horizontal variational $p+1$-forms
(with compact spacetime support, def. \ref{SpacetimeSupport} below) to the [[space of field histories]] (example \ref{DiffeologicalSpaceOfFieldHistories}). This is
def. \ref{LocalObservables} below.

A key example of a [[local observable]] in [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) is the _[[action functional]]_ (example \ref{ActionFunctional} below). This is the [[transgression of variational differential forms|transgression]]
of the [[Lagrangian density]] itself, or rather of its product with an "[[adiabatic switching]] function" that
localizes its [[support]] in a compact spacetime region. In typical cases the physical quantity whose observation is
represented by the action functional is the difference of the [[kinetic energy|kinetic]] energy-momentum minus the [[potential energy]]
of a field history averaged over the given region of spacetime.

The [[equations of motion]] of a [[Lagrangian field theory]] say that those field histories
are physically realized which are [[critical points]] of this [[action functional]] observable. This is
the _[[principle of extremal action]]_ (prop. \ref{PrincipleOfExtremalAction} below).

In summary we find the following system of types of observables:

[[!include perturbative observables -- table]]

In the chapter _[Free quantum fields](#FreeQuantumFields)_ we will see that the space of all [[polynomial observables]]
is too large to admit [[quantization]], while the space of [[regular polynomial observables|regular]] [[local observables]]
is too small to contain the usual [[interaction]] terms for [[perturbative quantum field theory]] (example \ref{RegularPolynomialLocalObservablesAreNecessarilyLinear}) below. The space of [[microcausal polynomial observables]] 
(def. \ref{MicrocausalObservable} below) is in between these two extremes, and evades both of these obstacles.

$\,$

Given the concept of [[observables]], it remains to formalize what it means for the [[physical system]] to be in some definite _[[state]]_
so that the [[observable]] quantities take some definite value, reflecting the properties of that state.

Whatever formalization for _[[states]]_ of a [[field theory]] one considers, at the very least
the [[space of states]] $States$ should come with a pairing [[linear map]]

$$
  \array{
    Obs \otimes States & \longrightarrow&  \mathcal{C}
    \\
    \left( A , \langle - \rangle \right) &\mapsto& \langle A \rangle
  }
$$

which reads in an [[observable]] quantity $A$ and a state, to be denoted $\langle - \rangle$,
and produces the [[complex number]] $\langle A \rangle$
which is the "value of the observable quantity $A$ in the case that the physical system is in the state $\langle -\rangle$".

One might imagine that
it is fundamentally possible to pinpoint the exact [[field history]] that the
[[physical system]] is found in. From this perspective, fixing a [[state]] should simply mean to
pick such a [[field history]], namely an element $\Phi \in \Gamma_{\Sigma}(E)_{\delta_{EL}\mathbf{L} = 0}$
in the [[on-shell]] [[space of field histories]].
If we write $\langle -\rangle_{\Phi}$ for this state, its pairing map with the [[observables]] would simply be
[[evaluation]] of the observable, being a function on the field history space, on that particular element in this space:

$$
  \langle A \rangle_{\Phi} \coloneqq A(\Phi)
  \,.
$$

However, in the practice of [[experiment]] a field history can never be known precisely, without remaining uncertainty.
Moreover, [[quantum physics]] (to which we finally come [below](#Quantization)), suggests that this is
true not just in practice, but even in principle. Therefore we should allow [[states]] to be a kind of [[probability distributions]]
on the [[space of field histories]], and regard the pairing $\langle A \rangle$ of a state $\langle - \rangle$ with an observable
$A$ as a kind of _[[expectation value]]_ of the function $A$ averaged with respect to this probability distribution.
Specifically, if the observable quantity $A$ is (a smooth approximation to) a [[characteristic function]]
of a [[subset]] $S \subset \Gamma_{\Sigma}(E)_{\delta_{EL}\mathbf{L} = 0}$ of the [[space of field histories]], then its value in a given state should be the [[probability]] to find the [[physical system]] in that subset of field histories.

But, moreover, the [[superposition principle]] of [[quantum physics]] says that the actually observable observables
are only those of the form $A^\ast A$ (for $A^\ast$ the image under the star-operation on the [[star algebra]]
of observables.

This finally leads to the definition of _[[states]]_ in def. \ref{States} below.



$\,$

We now discuss these topics:

$\,$

* _[General observables](#GeneralObservables)_

* _[Polynomial off-shell observables and Distributions](#LinearOffShellObservablesAreDistributions)_

* _[Polynomial on-shell observables and Distributional solutions to PDEs](#PolynomialOnShellObservablesAreDistributionalSolutionsToTheEquationsOfMotion)_

* _[Local observables and Transgression](#LocalObservablesByTransgression)_

* _[Infinitesimal observables](#InfinitesimalObservables)_

* _[States](#StatesArePositiveLinearFunctionals)_

$\,$

**General observables**
{#GeneralObservables}

+-- {: .num_defn #Observable}
###### Definition
**([[observables]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
with $\Gamma_\Sigma(E)_{\delta_{EL} \mathbf{L} = 0}$ its [[on-shell]] [[space of field histories]] (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}).

Then the _space of [[observables]]_ is the [[super formal smooth set]] (def. \ref{SuperFormalSmoothSet})
which is the [[mapping space]]

$$
  Obs(E,\mathbf{L})
  \;\coloneqq\;
  \left[
    \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
    \,,\,
    \mathbb{C}
  \right]
$$

from the [[on-shell]] [[space of field histories]] to the [[complex numbers]].

Similarly there is the space of _off-shell observables_

$$
  Obs(E)
  \;\coloneqq\;
  \left[
    \Gamma_\Sigma(E)
    \,,\,
    \mathbb{C}
  \right]
  \,.
$$

Every off-shell observables induces an on-shell observable by [[restriction]], this yields a smooth function

$$
  \label{OffShellObservablesRestrictToOnShellObservables}
  Obs(E)
    \overset{(-)_{\delta_{EL}\mathbf{L} = 0}}{\longrightarrow}
  Obs(E,\mathbf{L})
$$

similarly we may consider the observables on the sup-spaces of field histories with restricted causal support
according to def. \ref{CompactlySourceCausalSupport}. We write

$$
  Obs(E_{scp})
  \;\coloneqq\;
  \left[ \Gamma_{\Sigma,scp}(E), \mathbb{C}  \right]
$$

and

$$
  \label{SpaceOfObservablesOnFieldHistoriesOfSpatiallyCompactSupport}
  Obs(E_{scp}, \mathbf{L})
  \;\coloneqq\;
  \left[ \Gamma_{\Sigma,scp}(E)_{\delta_{EL} \mathbf{L} = 0}, \mathbb{C}  \right]
$$

for the spaces of (off-shell) observables on [[field histories]] with spatially compact support (def. \ref{CompactlySourceCausalSupport}).

$\,$

**Observables on bosonic fields**

In the case that $E$ is a purely [[bosonic]] [[field bundle]] in [[smooth manifolds]] so that $\Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}$
is a [[diffeological space]] (def. \ref{DiffeologicalSpaceOfFieldHistories}, def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime})
this means that a single [[observable]] $A \in Obs_{E,\mathbf{L}}$ is equivalently a [[smooth function]] (def. \ref{DiffeologicalSpace})

$$
  A
    \;\colon\;
  \Gamma_\Sigma(E)_{\delta_{EL} \mathbf{L} = 0}
    \longrightarrow
  \mathbb{C}
  \,.
$$

Explicitly, by def. \ref{SmoothSet} (and similarly by def. \ref{SuperFormalSmoothSet}) this means that
$A$ is for each [[Cartesian space]] $U$ (generally: [[super Cartesian space]], def. \ref{SuperCartesianSpace})
a [[natural transformation|natural]] function of plots

$$
  A_U
  \;\colon\;
  \left\{
    \array{
      U \times \Sigma && \overset{\Phi_{(-)}}{\longrightarrow} && E
      \\
      & {}_{\mathllap{pr_2}}\searrow &&  \swarrow_{\mathrlap{fb}}
      \\
      && \Sigma
    }
  \right\}_{\delta_{EL}\mathbf{L} = 0}
    \;\overset{}{\longrightarrow}\;
  \left\{
    U \to \mathbb{C}
  \right\}
  \,.
$$

**Observables on fermionic fields**

In the case that $E$ has purely [[fermionic]] [[fibers]] (def. \ref{FermionicBosonicFields}), such as for the [[Dirac field]] (example \ref{DiracFieldBundle})
with
$E = \Sigma\times S_{odd}$  then the only point in $Obs_{E,\mathbf{L}}$ is the zero-observable,
instead an observable is now a morphism

$$
  (\theta \mapsto \theta A)
    \;\colon\;
  \mathbb{R}^{0\vert 1}
    \longrightarrow
  Obs_{E,\mathbf{L}}
$$

and its component $A$ is a bosonic observable as above.

=--

The most basic kind of observables are the following:

+-- {: .num_example #PointEvaluationObservables}
###### Example
**(point evaluation observables -- [[field observables]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] (def. \ref{FieldsAndFieldBundles}) over some [[spacetime]] $\Sigma$
happens to be a [[trivial vector bundle]] in even degree (i.e. bosonic) with [[field fiber]] [[coordinates]] $(\phi^a)$ (example \ref{TrivialVectorBundleAsAFieldBundle}).
With respect to these coordinates a [[field history]], hence a [[section]] of the [[field bundle]]

$$
  \Phi \;\in \; \Gamma_\Sigma(E)
$$

has components $(\Phi^a)$ which are [[smooth functions]] on [[spacetime]].

Then for every index $a$ and every point $x \in \Sigma$ in [[spacetime]] (every [[event]]) there is an [[observable]] (def. \ref{Observable})
denoted $\mathbf{\Phi}^a(x)$ which is given by

$$
  \mathbf{\Phi}^a(x)
  \;\colon\;
  \Phi_{(-)}
    \mapsto
  \Phi_{(-)}^a(x)
  \,,
$$

hence which on a test space $U$ (a [[Cartesian space]] or more generally [[super Cartesian space]], def. \ref{SuperCartesianSpace}) sends a $U$-parameterized collection of fields

$$
  \Phi_{(-)} \colon U \to \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
$$

to their $U$-parameterized collection of values at $x$ of their $a$-th component.

Notice how the various aspects of the concept of "field" are involved here, all closely related
but crucially different:

$$
  \array{
    \mathbf{\Phi}^a(x)
    &\colon&
    \Phi
    &\overset{\phantom{AA}}{\mapsto}&
    \Phi^a(x)
    &=&
    \phi^a & \circ \Phi(x)
    \\
    \array{
      \text{field}
      \\
      \text{observable}
    }
    &&
    \array{
      \text{field}
      \\
      \text{history}
    }
    &&
    \array{
      \text{field}
      \\
      \text{value}
    }
    &&
    \array{
      \text{field}
      \\
      \text{component}
    }
  }
$$


=--






$\,$


**Polynomial off-shell Observables and Distributions**
{#LinearOffShellObservablesAreDistributions}

We consider here _[[linear observables]]_ (def. \ref{LinearObservables} below) and more generally
_quadratic observables_ (def. \ref{QuadraticObservables}) and generally _[[polynomial observables]]_ (def. \ref{PolynomialObservables} below) for [[free field theories]] and discuss how these are equivalently given by
[[integration]] against [[generalized functions]] called _[[distributions]]_ (prop. \ref{LinearObservablesAreTheCompactlySupportedDistributions} and prop. \ref{DistributionsAreGeneralizedFunctions} below).

This is the basis for the discussion of [[quantum observables]] for [[free field theories]] [further below](#FreeQuantumFields).

$\,$

+-- {: .num_defn #LinearObservables}
###### Definition
**([[linear map|linear]] [[off-shell]] [[observables]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ (def. \ref{FieldsAndFieldBundles}) is a [[super vector bundle|super]] [[vector bundle]]
(as in example \ref{TrivialVectorBundleAsAFieldBundle} and as opposed to more general non-linear [[fiber bundles]]).

This means that the
[[off-shell]] [[space of field histories]] $\Gamma_\Sigma(E)$ (example \ref{SupergeometricSpaceOfFieldHistories})
inherits the structure of a [[super vector space|super]] [[vector space]] by spacetime-pointwise (i.e. [[event]]-wise) scaling and addition of
[[field histories]].

Then an [[off-shell]] [[observable]] (def. \ref{Observable})

$$
  A \;\colon\; \Gamma_\Sigma(E) \longrightarrow \mathbb{C}
$$

is a _[[linear observable]]_ if it is a [[linear function]] with respect to this vector space structure, hence if

$$
  A\left( c \Phi_{(-)}) = c A(\Phi_{(-)} \right)
  \phantom{AAAA}
  \text{and}
  \phantom{AAAA}
  A\left(\Phi_{(-)} + \Phi'_{(-)} \right)
  =
  A\left( \Phi_{(-)}) + A(\Phi'_{(-)} \right)
$$

for all plots of [[field histories]] $\Phi_{(-)}, \Phi'_{(-)}$.

If moreover $(E,\mathbf{L})$ is a [[free field theory]] (def. \ref{FreeFieldTheory}) then the [[on-shell]] [[space of field histories]] inherits this linear structure and we may similarly speak of linear on-shell observables.

We write

$$
  LinObs(E,\mathbf{L}) \hookrightarrow Obs(E,\mathbf{L})
$$

for the subspace of [[linear observables]] inside all [[observables]] (def. \ref{Observable}) and similarly

$$
  LinObs(E) \hookrightarrow Obs(E)
$$

for the linear off-shell observables inside all off-shell observables, and similarly
for the subspaces of [[linear observables]] on [[field histories]] of spatially compact supprt (eq:SpaceOfObservablesOnFieldHistoriesOfSpatiallyCompactSupport):

$$
  \label{LinearObservablesOnSpatiallyCompactlySupportedOnShellFieldHistories}
  LinObs(E_{scp}, \mathbf{L})
    \hookrightarrow
  Obs(E_{scp}, \mathbf{L})
$$

and

$$
  LinObs(E_{scp})
    \hookrightarrow
  Obs(E_{scp})
  \,.
$$

=--


+-- {: .num_example #LinearPointEvaluationObservables}
###### Example
**(point evaluation observables are linear)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}),
whose [[field bundle]] $E$ (def. \ref{FieldsAndFieldBundles}) is the [[trivial vector bundle]]
with field [[coordinates]] $(\phi^a)$ (example \ref{TrivialVectorBundleAsAFieldBundle}).

Then for each field component index $a$ and point $x \in \Sigma$ of [[spacetime]] (each [[event]])
the point evaluation observable (example \ref{PointEvaluationObservables})

$$
  \array{
    \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
      &\overset{\mathbf{\Phi}^a(x)}{\longrightarrow}&
    \mathbb{C}
    \\
    \phi &\mapsto& \phi^a(x)
  }
$$

is a [[linear observable]] according to def. \ref{LinearObservables}. The [[distribution]]
that it corresponds to under prop. \ref{LinearObservablesAreTheCompactlySupportedDistributions}
is the _[[Dirac delta-distribution]]_ at the point $x$ combined with the [[Kronecker delta]] on the index $a$:
In the [[generalized function]]-notation of remark \ref{LinearObservablesAsGeneralizedFunctions} this reads:

$$
  \Phi^a(x) \;\colon\; \Phi \mapsto \int_\Sigma \Phi^b(y) \delta_b^a \delta(x,y) \, dvol_\Sigma(y)
  \,.
$$

=--


+-- {: .num_prop #LinearObservablesAreTheCompactlySupportedDistributions}
###### Proposition
**([[linear map|linear]] [[off-shell]] [[observables]] of [[scalar field]] are the [[compactly supported distributions]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}),
whose [[field bundle]] $E$ (def. \ref{FieldsAndFieldBundles}) is the [[trivial vector bundle|trivial]] [[real line bundle]]
(as for the [[real scalar field]], example \ref{RealScalarFieldBundle}).
This means that the [[off-shell]] [[space of field histories]] $\Gamma_\Sigma(E) \simeq C^\infty(\Sigma)$ (eq:SpaceOfFieldHistoriesOfRealScalarField) is the
[[real vector space]] of [[smooth functions]] on [[Minkowski spacetime]] and that every [[linear observable]] $A$ (def. \ref{LinearObservables})
gives a [[linear function]]

$$
  A_\ast \;\colon\; C^\infty(\Sigma)_{\delta_{EL}\mathbf{L} = 0} \longrightarrow \mathbb{C}
  \,.
$$

This [[linear function]] $A_\ast$ is in fact
a _[[compactly supported distribution]]_, in the sense of [[functional analysis]], in that it satisfies
the following [[Fréchet vector space]] [[continuous function|continuity condition]]:

* **[[Fréchet space|Fréchet]] [[continuous linear functional]]**

  A [[linear function]] $A_\ast \;\colon\; C^\infty(\mathbb{R}^{p,1}) \to \mathbb{R}$ is called _[[continuous function|continuous]]_ if
  there exists

  1. a [[compact subset]] $K \subset \mathbb{R}^{p,1}$ of [[Minkowski spacetime]];

  1. a [[natural number]] $k \in \mathbb{N}$;

  1. a [[positive number|positive]] [[real number]] $C \in \mathbb{R}_+$

  such that for all [[on-shell]] [[field histories]]

  $$
    \Phi \in C^\infty(\Sigma)_{\delta_{EL}\mathbf{L} = 0}
  $$

  the following [[inequality]] of [[absolute values]] ${\vert -\vert}$ of [[partial derivatives]] holds

  $$
    {\vert A_\ast(\Phi)\vert}
    \;\leq\;
    C \underset{{\vert \alpha \vert} \leq k}{\sum} \, \underset{x \in K}{sup} {\vert \partial^\alpha \Phi(x)\vert}
    \,,
  $$

  where the sum is over all multi-indices $\alpha \in \mathbb{N}^{p+1}$ (eq:PartialDerivativeWithManyIndices)
  whose total degree ${\vert \alpha\vert} \coloneqq \alpha_0 + \cdots + \alpha_{p}$ is bounded by $k$,
  and where

  $$
    \partial^\alpha \Phi
    \;\coloneqq\;
    \frac{\partial^{{\vert \alpha\vert}} \Phi }{ \partial^{\alpha_0} x^0 \partial^{\alpha_1} x^1 \cdots \partial^{\alpha^p} x^p  }
  $$

  denotes the corresponding [[partial derivative]] (eq:PartialDerivativeWithManyIndices).

This identification constitutes a [[linear isomorphism]]

$$
  \array{
    LinObs(\Sigma \times \mathbb{R}) &\overset{\simeq}{\longrightarrow}& \mathcal{E}'(\Sigma)
    \\
    \array{
      \text{linear off-shell}
      \\
      \text{observables}
      \\
      \text{of the scalar field}
    }
    &&
    \array{
      \text{compactly supported}
      \\
      \text{distributions}
      \\
      \text{on spacetime}
    }
  }
  \,,
$$

saying that all [[compactly supported distributions]] arise from linear off-shell observables of the [[scalar field]] this way, and uniquely so.

=--

For **proof** see at _[[distributions are the smooth linear functionals]]_, [this prop.](distributions+are+the+smooth+linear+functionals#CompactlySupportedDistributionsAreTheSmoothLinearFunctionals)

The identification from prop. \ref{LinearObservablesAreTheCompactlySupportedDistributions} of linear off-shell observables
with [[compactly  supported distributions]] makes available powerful tools from [[functional analysis]]. The key fact is the
following:


+-- {: .num_prop #DistributionsAreGeneralizedFunctions}
###### Proposition
**([[distributions]] are [[generalized functions]])**

For $n \in \mathbb{N}$, every [[compactly supported function|compactly supported]] [[smooth function]]
$b \in C^\infty_{cp}(\mathbb{R}^n)$ on the [[Cartesian space]] $\mathbb{R}^n$ induces a [[distribution]] (prop. \ref{LinearObservablesAreTheCompactlySupportedDistributions}), hence a [[continuous linear functional]],
by [[integration]] against $b$ times the [[volume form]].

$$
  \array{
    C^\infty(\mathbb{R}^n) &\longrightarrow& \mathbb{R}
    \\
    f &\mapsto& \int_{\mathbb{R}^n} f(x) b(x) \, dvol(x)
  }
$$


The distributions arising this way are called the _[[non-singular distributions]]_.

This construction is clearly a [[linear function|linear]] [[monomorphism|inclusion]]

$$
  C^\infty_{cp}(\mathbb{R}^n) \overset{\phantom{AAA}}{\hookrightarrow} \mathcal{E}'(\mathbb{R}^n)
$$

and in fact this is a [[dense subspace]] inclusion for the space of compactly supported distributions
$\mathcal{E}'(\mathbb{R}^n)$ equipped with the [[dual space]] topology ([this def.](dual+vector+space#LinearDualOfATopologicalVectorSpace)) to the [[Fréchet space]] structure on $C^\infty(\mathbb{R}^n)$ from prop. \ref{LinearObservablesAreTheCompactlySupportedDistributions}.

Hence every [[compactly supported distribution]] $u$ is the [[limit of a sequence|limit]] of a [[sequence]]  $\{b_n\}_{n \in \mathbb{N}}$
of [[compactly supported function|compactly supported]] [[smooth functions]]  in that for every [[smooth function]] $f \in C^\infty(\mathbb{R}^n)$ we have that the value $u(f) \in \mathbb{R}$  is the [[limit of a sequence|limit]] of [[integrals]]
against $b_n dvol$:

$$
  u(f)
    \;=\;
  \underset{n \to \infty}{\lim}\, \int_{\mathbb{R}^n} f(x) b_n(x) dvol(x)
  \,.
$$

=--

(e. g. [H&#246;rmander 90, theorem 4.1.5](non-singular+distributionFourier+transform#Hoermander90Fourier+transform#Hoermander90))

Proposition \ref{DistributionsAreGeneralizedFunctions} with prop. \ref{LinearObservablesAreTheCompactlySupportedDistributions} implies that with due care we may think of _all_ linear off-shell observables as arising from [[integration]] of [[field histories]]
against some "[[generalized function|generalized smooth functions]]" (namely a [[limit of a sequence|limit]] of actual smooth functions):

+-- {: .num_remark #LinearObservablesAsGeneralizedFunctions}
###### Remark
**([[linear map|linear]] [[off-shell]] [[observables]] of [[real scalar field]] as [[integration]] against [[generalized functions]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}),
whose [[field bundle]] $E$ (def. \ref{FieldsAndFieldBundles}) is a [[trivial vector bundle]] with field
coordinates $(\phi^a)$.

Prop. \ref{LinearObservablesAreTheCompactlySupportedDistributions} implies immediately that in this
situation linear off-shell observables $A$ (def. \ref{LinearObservables}) correspond to [[tuples]] $(A_a)$
of [[compactly supported distributions]] via

$$
  A(\Phi) = \underset{a}{\sum} A_a(\Phi^a)
  \,.
$$

With prop. \ref{DistributionsAreGeneralizedFunctions} it follows furthermore that
there is a [[sequence]] of [[tuples]] of [[smooth functions]] $\{(\alpha_n)_{a}\}_{n \in \mathbb{N}}$ such that $A_a$
is the [[limit of a sequence|limit]] of the [[integrations]] against these:

$$
  A(\Phi)
  \;=\;
  \underset{n \to \infty}{\lim}
  \,
  \int_\Sigma \Phi^a(x) (\alpha_n)_a(x) \, dvol(x)
  \,,
$$

where now the [[sum]] over the index $a$ is again left notationally implicit.

For handling distributions/linear off-shell observables it is therefore useful to adopt, with due care,
shorthand notation as if the [[limit of a sequence|limits]] of the [[sequences]] of [[smooth functions]] $(\alpha_n)_a$ actually existed,
as "[[generalized functions]]" $\alpha_a$, and to set

$$
  \int_\Sigma \Phi^a(x) \alpha_a(x) \, dvol(x)
  \;\coloneqq\;
  A(\Phi)
  \,,
$$

This suggests that basic operations on functions, such as their pointwise product,
should be [[extension|extended]] to [[distributions]], e.g. to a _[[product of distributions]]_.
This turns out to exist, as long as the high-frequency modes in the [[Fourier transform of distributions|Fourier transform of]]
the distributions being multiplied cancel out -- the mathematical reflection of "[[UV-divergences]]" in [[quantum field theory]].
This we turn to in _[Free quantum fields](#FreeQuantumFields)_ below.

=--

These considerations generalize from the [[field bundle]] of the [[real scalar field]] to general [[field bundles]] (def. \ref{FieldsAndFieldBundles})
as long as they are [[smooth vector bundles]] (def. \ref{VectorBundle}):

+-- {: .num_defn #TVSStructureOnSpacesOfSmoothSections}
###### Definition
**([[Fréchet space|Fréchet]] [[topological vector space]] on [[spaces of smooth sections]] of a [[smooth vector bundle]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] (def. \ref{FieldsAndFieldBundles}) which is a [[smooth vector bundle]] (def. \ref{VectorBundle}) over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime});
hence, up to [[isomorphism]], a [[trivial vector bundle]] as in example \ref{TrivialVectorBundleAsAFieldBundle}.

On its [[real vector space]] $\Gamma_\Sigma(E)$ [[space of sections|of smooth sections]] consider the [[seminorms]] indexed by a [[compact subset]] $K \subset \Sigma$ and a [[natural number]] $k \in \mathbb{N}$  and given by

$$
  \array{
    \Gamma_\Sigma(E) &\overset{p_K^k}{\longrightarrow}&
    [0,\infty)
    \\
    \Phi &\mapsto&  \underset{ {\vert \alpha\vert} \leq k}{max} \left( \underset{x \in K}{sup} {\vert \partial^\alpha \Phi(x)\vert}\right) \,,
  }
$$

where on the right we have the [[absolute values]] of the [[partial derivatives]] of $\Phi$ index by $\alpha$ (eq:PartialDerivativeWithManyIndices) with respect to any choice of [[norm]] on the [[fibers]].

This makes $\Gamma_\Sigma(E)$ a [[Fréchet space|Fréchet]] [[topological vector space]].

For $K \subset \Sigma$ any [[closed subset]] then the sub-space of sections

$$
  \Gamma_{\Sigma,K}(E) \hookrightarrow \Gamma_\Sigma(E)
$$

of sections whose [[support]] is inside $K$ becomes a [[Fréchet space|Fréchet]] [[topological vector spaces]] with the induced [[subspace topology]], which makes these be [[closed subspaces]].

Finally, the [[vector spaces]] of smooth sections with prescribed causal support (def. \ref{CompactlySourceCausalSupport})
are [[inductive limits]] of vector spaces $\Gamma_{\Sigma,K}(E)$ as above, and hence they inherit
[[topological vector space]] [[structure]] by forming the corresponding [[inductive limit]] in the [[category]]
of [[topological vector spaces]]. For instance

$$
  \Gamma_{\Sigma,cp}(E)
  \;\coloneqq\;
  \underset{\underset{ {K \subset \Sigma} \atop {K\, \text{compact}} }{\longrightarrow}}{\lim}
  \Gamma_{\Sigma,K}(E)
$$

etc.

=--

([B&#228;r 14, 2.1](space+of+sections#Baer14))



+-- {: .num_defn #DistributionalSections}
###### Definition
**([[distribution|distributional]] [[sections]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[smooth vector bundle]] (def. \ref{VectorBundle}) over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}).

The [[vector space|vector]] [[spaces of smooth sections]] with restricted support from def. \ref{CompactlySourceCausalSupport} structures of [[topological vector spaces]] via def. \ref{TVSStructureOnSpacesOfSmoothSections}. We denote the [[dual topological vector spaces]] by

$$
  \Gamma'_{\Sigma}( E ^*)
    \;\coloneqq\;
  (\Gamma_{\Sigma,cp}(E))^*
  \,.
$$

This is called the space of _distributional sections_ of the [[dual vector bundle]] ${E}^*$.

The _[[support of a distribution|support of a distributional section]]_ $supp(u)$ is the set of points in $\Sigma$ such that
for every neighbourhood of that point $u$ does not vanish on all sections with support in that neighbourhood.

Imposing the same restrictions to the [[supports of distributions|supports of distributional sections]] as in def. \ref{CompactlySourceCausalSupport}, we have the following subspaces of distributional sections:

$$
  \Gamma'_{\Sigma,cp}(E^\ast) ,
  \Gamma'_{\Sigma,\pm cp}(E^\ast) ,
  \Gamma'_{\Sigma,scp}(E^\ast) ,
  \Gamma'_{\Sigma,fcp}(E^\ast) ,
  \Gamma'_{\Sigma,pcp}(E^\ast) ,
  \Gamma'_{\Sigma,tcp}(E^\ast)
  \;\subset\;
  \Gamma'_{\Sigma}(E^\ast) .
$$

=--

([Sanders 13](Green+hyperbolic+differential+operator#Sanders12), [B&#228;r 14](Green+hyperbolic+differential+operator#Baer14))

As before in prop. \ref{DistributionsAreGeneralizedFunctions} the actual [[smooth sections]] yield
examples of distributional sections, and all distributional sections arise as [[limit of a sequence|limits]]
of integrations against smooth sections:

+-- {: .num_prop #NonSingularDistributionalSections}
###### Proposition
**([[non-singular distribution|non-singular distributional sections]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[smooth vector bundle]] over [[Minkowski spacetime]] and let
$s \in \{cp, \pm cp, scp, tcp\}$ be any of the [[support]] conditions from def. \ref{CompactlySourceCausalSupport}.

Then the operation of regarding a [[compact support|compactly supported]] [[smooth section]] of the [[dual vector bundle]]
as a [[functional]] on sections with this support property is a [[dense subspace]] inclusion into the
[[topological vector space]] of distributional sections from def. \ref{DistributionalSections}:

$$
  \array{
    \Gamma_{\Sigma,cp}(E^\ast)
      &\overset{\phantom{A}u_{(-)}\phantom{A} }{\hookrightarrow}&
    \Gamma'_{\Sigma,s}(E)
    \\
    b &\mapsto& \left( \Phi \mapsto \underset{\Sigma}{\int} b(x) \cdot \Phi(x) \, dvol_\Sigma(x) \right)
  }
$$

=--

([B&#228;r 14, lemma 2.15](Green+hyperbolic+differential+equation#Baer14}))




+-- {: .num_prop #DistributionsWithCausalSupports}
###### Proposition
**(distribution dualities with causally restricted supports)**

Let $E \overset{fb}{\to} \Sigma$ be a  [[smooth vector bundle]] (def. \ref{VectorBundle}) over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}).

Then there are the following [[isomorphisms]] of [[topological vector spaces]] between a) [[dual spaces]] of [[spaces of sections]]
with restricted causal support (def. \ref{CompactlySourceCausalSupport}) and equipped with the topology from def. \ref{TVSStructureOnSpacesOfSmoothSections} and b) spaces of distributional sections with restricted supports, according to def. \ref{DistributionalSections}:


$$
\begin{aligned}
  \Gamma_{\Sigma,cp}(E)^* &\simeq \Gamma'_{\Sigma}(E^\ast) ,
  \\
  \Gamma_{\Sigma,+cp}(E)^* &\simeq \Gamma'_{\Sigma,fcp}(E^\ast) ,
  \\
  \Gamma_{\Sigma,-cp}(E)^* &\simeq \Gamma'_{\Sigma,pcp}(E^\ast) ,
  \\
  \Gamma_{\Sigma,scp}(E)^* &\simeq \Gamma'_{\Sigma,tcp}(E^\ast) ,
  \\
  \Gamma_{\Sigma,fcp}(E)^* &\simeq \Gamma'_{\Sigma,+cp}(E^\ast) ,
  \\
  \Gamma_{\Sigma,pcp}(E)^* &\simeq \Gamma'_{\Sigma,-cp}(E^\ast) ,
  \\
  \Gamma_{\Sigma,tcp}(E)^* &\simeq \Gamma'_{\Sigma,scp}(E^\ast) ,
  \\
  \Gamma_{\Sigma}(E)^* &\simeq \Gamma'_{\Sigma,cp}(E^\ast) .
\end{aligned}
$$

=--

([Sanders 13, thm. 4.3](Green+hyperbolic+differential+operator#Sanders12), [B&#228;r 14, lem. 2.14](Green+hyperbolic+differential+operator#Baer14))



The concept of [[linear observables]] naturally generalizes to that of [[multilinear map|multilinear observables]]:

+-- {: .num_defn #QuadraticObservables}
###### Definition
**([[quadratic form|quadratic]] [[off-shell]] [[observables]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
over a [[spacetime]] $\Sigma$
whose [[field bundle]] $E$ (def. \ref{FieldsAndFieldBundles}) is a [[super vector bundle|super]] [[vector bundle]].

The _[[external tensor product|external]] [[tensor product of vector bundles]]_ of the [[field bundle]]
$E \overset{fb}{\to} \Sigma$ with itself, denoted

$$
  E \boxtimes E \overset{}{\to} \Sigma \times \Sigma
$$

is the [[vector bundle]] over the [[Cartesian product]] $\Sigma \times \Sigma$, of [[spacetime]] with itself,
whose [[fiber]] over a pair of points $(x_1,x_2)$ is the [[tensor product]] $E_{x_1} \otimes E_{x_2}$ of the corresponding field fibers.

Given a [[field history]], hence a [[section]]  $\phi \in \Gamma_\Sigma(E)$ of the [[field bundle]], there is then
the induced section $\phi \boxtimes \phi \in \Gamma_{\Sigma \times \Sigma}(E \boxtimes E)$.

We say that an [[off-shell]] [[observable]]

$$
  A \;\colon\; \Gamma_\Sigma(E) \longrightarrow \mathbb{C}
$$

is _[[quadratic form|quadratic]]_ if it comes from a "graded-symmetric [[bilinear map|bilinear]] observable", namely a smooth function on the [[space of sections]]
of the [[external tensor product|external]] [[tensor product of vector bundles|tensor product of]] the [[field bundle]]
with itself

$$
  B
   \;\colon\;
  \Gamma_{\Sigma \times \Sigma}(E \boxtimes E)_{\delta_{EL}\mathbf{L} = 0}
    \longrightarrow
  \mathbb{C}
  \,,
$$

as

$$
  A(\Phi) = B(\Phi,\Phi)
  \,.
$$

More explicitly: By prop. \ref{LinearObservablesAreTheCompactlySupportedDistributions} the quadratic observable $A$
is given by a [[compactly supported distribution]] [[distribution of two variables|of two variables]]
which in the notation of remark \ref{LinearObservablesAsGeneralizedFunctions} comes from a graded-symmetric [[matrix]] of
[[generalized functions]]
$\beta_{a_1 a_2} \in \mathcal{E}'(\Sigma \times \Sigma, E \boxtimes E)$ as

$$
  A(\Phi)
    \;=\;
  \int_{\Sigma \times \Sigma} \Phi^{a_1}(x_1) \beta_{a_1 a_2}(x_1,x_2) \Phi^{a_2}(x_2)\, dvol_\Sigma(x_1) dvol_\Sigma(x_2)
  \,.
$$

This notation makes manifest how the concept of  quadratic observables is a generalization of that of [[quadratic forms]] coming from  [[bilinear forms]].

=--


+-- {: .num_defn #PolynomialObservables}
###### Definition
**([[off-shell]] [[polynomial observables]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
over a [[spacetime]] $\Sigma$
whose [[field bundle]] $E$ (def. \ref{FieldsAndFieldBundles}) is a [[super vector bundle|super]] [[vector bundle]].

An [[off-shell]] [[observable]] (def. \ref{Observable})

$$
  A \;\colon\; \Gamma_\Sigma(E) \longrightarrow \mathbb{C}
$$

is a _[[polynomial observable]]_ if it is the [[sum]] of a constant, and a [[linear observable]] (def. \ref{LinearObservables}),
and a quadratic observable (def. \ref{QuadraticObservables}) and so on:

$$
  \label{ExpansionOfPolynomialObservables}
  \begin{aligned}
    A(\Phi)
     & = \phantom{+}
    \alpha^{(0)}
    \\
    &
    \phantom{=}
      +
    \int_{\Sigma} \Phi^a(x) \alpha^{(1)}_a(x) \, dvol_\Sigma(x)
    \\
    &
    \phantom{=}
     +
    \int_{\Sigma^2} \Phi^{a_1}(x_1) \Phi^{a_2}(x_2) \alpha^{(2)}_{a_1 a_2}(x_1, x_2) \, dvol_\Sigma(x_1) dvol_\Sigma(x_2)
    \\
    &
    \phantom{=}
     +
    \int_{\Sigma^3} \Phi^{a_1}(x_1) \Phi^{a_2}(x_2) \Phi^{a_3}(x_3)
    \alpha^{(3)}_{a_1 a_2 a_3}(x_1,x_2,x_3) \, dvol_\Sigma(x_1) dvol_\Sigma(x_2) dvol_\Sigma(x^3)
    \\
    &
    \phantom{=}
     +
    \cdots
  \,.
  \end{aligned}
$$

If all the [[coefficient]] [[distributions]] $\alpha^{(k)}$ are [[non-singular distributions]], then we say that $A$ is a _[[regular polynomial observable]]_.

We write

$$
  PolyObs(E)_{reg} \hookrightarrow PolyObs(E) \hookrightarrow Obs(E)
$$

for the subspace of (regular) polynomial off-shell observables.



=--

$\,$

Next we discuss the restriction of these off-shell polynomial observables to the [[shell]] to yield [[on-shell]]  polynomial observables, characterized by theorem \ref{LinearObservablesForGreeFreeFieldTheoryAreDistributionalSolutionsToTheEquationsOfMotion} below.

$\,$



**Polynomial on-shell Observables and Distributional solutions to PDEs**
{#PolynomialOnShellObservablesAreDistributionalSolutionsToTheEquationsOfMotion}

The evident [[on-shell]] version of def. \ref{PolynomialObservables} is this:

+-- {: .num_defn #PolynomialObservablesOnShell}
###### Definition
**([[on-shell]] [[polynomial observables]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] (def. \ref{FreeFieldTheory}) with [[on-shell]] [[space of field histories]]  $\Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0} \hookrightarrow \Gamma_\Sigma(E)$. Then an [[on-shell]] [[observable]] (def. \ref{Observable})

$$
  A \;\colon\; \Gamma_\Sigma(E) \longrightarrow \mathbb{C}
$$

is an _[[on-shell]] [[polynomial observable]]_ if it is the [[restriction]] of an [[off-shell]] [[polynomial observable]] $A_{off}$ according to def. \ref{PolynomialObservables}:

$$
  \array{
    \Gamma_{\Sigma}(E)_{\delta_{EL}\mathbf{L} = 0} &\overset{\phantom{A}A\phantom{A}}{\longrightarrow}&
    \\
    \downarrow & \nearrow_{\mathrlap{A_{off}}}
    \\
    \Gamma_\Sigma(E)
  }
  \,.
$$

Similarly $A$ is an [[on-shell]] [[linear observable]] or [[on-shell]] [[regular polynomial observable]] etc. if it is the [[restriction]] of a [[linear observable]] or [[regular polynomial observable]], respectively, according to def. \ref{PolynomialObservables}. We write

$$
  PolyObs(E,\mathbf{L}) \hookrightarrow Obs(E,\mathbf{L})
$$

for the subspace of polynomial on-shell observables inside all on-shell observables, and similarly


$$
  LinObs(E,\mathbf{L}) \hookrightarrow Obs(E,\mathbf{L})
$$

and

$$
  PolyObs(E,\mathbf{L})_{reg} \hookrightarrow Obs(E,\mathbf{L})
$$

etc.

$$

=--

While by def. \ref{PolynomialObservablesOnShell} every [[off-shell]] [[observable]] induces an [[on-shell]] [[observable]]
simply by [[restriction]] (eq:OffShellObservablesRestrictToOnShellObservables),
different off-shell observables may restrict to the _same_ on-shell observale.
It is therefore useful to find a condition on off-shell observables
that makes them equivalent to on-shell observables under restriction.
We now discuss such precise characterizations of the off-shell polynomial observables
for the case of sufficiently well behaved [[free field theory|free field]] [[equations of motion]]
-- namely [[Green hyperbolic differential equations]], def. \ref{GreenHyperbolicDifferentialOperator} below.
The main result is theorem \ref{LinearObservablesForGreeFreeFieldTheoryAreDistributionalSolutionsToTheEquationsOfMotion} below.

While in general the [[equations of motion]] are not [[Green hyperbolic differential equations|Green hyperbolic]] --
namely not in the presence of implicit [[infinitesimal gauge symmetries]] discussed in _[Gauge symmetries](#GaugeSymmetries)_ below --
it turns out that up to a suitable notion of [[equivalence]] they are equivalent to those that are; this we discuss in the chapter _[Gauge fixing](#GaugeFixing)_ below.

$\,$


+-- {: .num_defn #DistributionalDerivatives}
###### Definition
**([[derivatives of distributions]] and [[distributional solutions of PDEs]])**

Given a [[pair]] of [[formally adjoint differential operators]] $P, P^\ast \colon \Gamma_\Sigma(E) \to \Gamma_\Sigma(E^\ast)$
(def. \ref{FormallyAdjointDifferentialOperators})
then the _[[derivative of distributions|distributional derivative]]_
of a [[distribution|distributional section]] $u \in \Gamma'_\Sigma(E)$ (def. \ref{DistributionalSections})
by $P$ is the distributional section $P u \in \Gamma'_\Sigma(E^\ast)$

$$
  P u
     \;\coloneqq\;
  u(P^\ast(-)) \;\colon\; \Gamma_{\Sigma,cp}(E^\ast)
  \,.
$$

If

$$
  P u = 0 \;\in\; \Gamma'_\Sigma(E^\ast)
$$

then we say that $u$ is a [[distributional solution]] (or [[generalized solution]]) of the homogeneous [[differential equation]]
defined by $P$.

=--

+-- {: .num_example #DistributionalPDESolutionsFromOrdinaryPDESolutions}
###### Example
**(ordinary [[PDE]] solutions are [[generalized solutions of a PDE|generalized solutions]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[smooth vector bundle]] over [[Minkowski spacetime]]
and let $P, P^\ast \colon \Gamma_\Sigma(E) \to \Gamma_\Sigma(E^\ast)$ be a [[pair]] of [[formally adjoint differential operators]].

Then for every [[non-singular distribution|non-singular distributional section]] $u_{\Phi} \in \Gamma'_{\Sigma}(E^\ast)$
coming from an actual smooth section $\Phi \in \Gamma_\Sigma(E)$ via prop. \ref{NonSingularDistributionalSections}
the [[derivative of distributions]] (def. \ref{DistributionalDerivatives}) is the distributional section
induced from the ordinary derivative of smooth functions:

$$
  P u_\Phi \;=\; u_{P \Phi}
  \,.
$$

In particular $u_\Phi$ is a [[generalized solution of a PDE|distributional solution]] to the [[PDE]] precisely
if $\Phi$ is an ordinary solution:

$$
  P u_\Phi \;=\; 0
  \phantom{AAA}
  \Leftrightarrow
  \phantom{AAA}
  P \Phi = 0
  \,.
$$


=--


+-- {: .proof}
###### Proof

For all $b \in \Gamma_{\Sigma,cp}(E)$ we have

$$
  \begin{aligned}
    (P u_\Phi)(b)
    & =
    u_\Phi(P^\ast b)
    \\
    & =
    \int u \cdot P^\ast b \, dvol
    \\
    & =
    \int (P u) \cdot b \, dvol
    \\
    & =
    u_{P \Phi}(b)
  \end{aligned}
$$

where all steps are by the definitions except the third, which is by the definition of
[[formally adjoint differential operator]] (def. \ref{FormallyAdjointDifferentialOperators}),
using that by the [[compact support]] of $b$ and the [[Stokes theorem]] (prop. \ref{StokesTheorem})
the term $K(\Phi,b)$ in def. \ref{FormallyAdjointDifferentialOperators} does not contribute to the [[integral]].

=--




+-- {: .num_defn #AdvancedAndRetardedGreenFunctions}
###### Definition
**([[advanced and retarded Green functions]] and [[causal Green function]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] (def. \ref{FieldsAndFieldBundles}) which is a [[vector bundle]] (def. \ref{VectorBundle}) over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}).
Let $P \;\colon\;\Gamma_\Sigma(E) \to \Gamma_\Sigma(E^\ast)$ be a [[differential operator]] (def. \ref{DifferentialOperator}) on its [[space of smooth sections]].

Then a [[linear map]]

$$
  \mathrm{G}_{P,\pm}
    \;\colon\;
  \Gamma_{\Sigma, cp}(E^\ast)
    \longrightarrow
  \Gamma_{\Sigma, \pm cp}(E)
$$


from [[spaces of smooth sections]] of [[compact support]] to spaces of sections of causally sourced future/past support (def. \ref{CompactlySourceCausalSupport}) is called an _[[advanced or retarded Green function]]_ for $P$, respectively, if

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

1. the [[support]] of $G_{P,\pm}(\Phi)$ is in the [[closed future cone]] or [[closed past cone]] of the support of $\Phi$, respectively.

If the advanced/retarded Green functions $G_{P\pm}$ exists, then the difference

$$
  \label{CausalGreenFunction}
  \mathrm{G}_P \coloneqq \mathrm{G}_{P,+} - \mathrm{G}_{P,-}
$$

is called the _[[causal Green function]]_.

=--

(e.g. [B&#228;r 14, def. 3.2, cor. 3.10](Green+hyperbolic+differential+equation#Baer14}))


+-- {: .num_defn #GreenHyperbolicDifferentialOperator}
###### Definition
**([[Green hyperbolic differential equation]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] (def. \ref{FieldsAndFieldBundles}) which is a [[vector bundle]] (def. \ref{VectorBundle}) over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}).

A [[differential operator]] (def. \ref{NormallyHyperbolicDifferentialOperator})

$$
  P
    \;\colon\;
  \Gamma_\Sigma(E)
    \longrightarrow
  \Gamma_{\Sigma}(E^\ast)
$$

is called a _[[Green hyperbolic differential operator]]_ if $P$ as well as its [[formal adjoint differential operator]] $P^\ast$ (def. \ref{FormallyAdjointDifferentialOperators}) admit [[advanced and retarded Green functions]] (def. \ref{AdvancedAndRetardedGreenFunctions}).

=--

([B&#228;r 14, def. 3.2](Green+hyperbolic+partial+differential+equation##Baer14}), [Khavkine 14, def. 2.2](Green+hyperbolic+partial+differential+equation#Khavkine14))


The two archtypical examples of [[Green hyperbolic differential equations]] are the [[Klein-Gordon equation]]
and the [[Dirac equation]] on [[Minkowski spacetime]]. For the moment we just cite the existence of the
[[advanced and retarded Green functions]] for these, we will work these out in detail below in _[Propagators](#Propagators)_.

+-- {: .num_example #GreenHyperbolicKleinGordonEquation}
###### Example
**([[Klein-Gordon equation]] is a [[Green hyperbolic differential equation]])**

The [[Klein-Gordon equation]], hence the [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]]
of the [[free field theory|free]] [[scalar field]] (example \ref{EquationOfMotionOfFreeRealScalarField})
is a [[Green hyperbolic differential equation]] (def. \ref{GreenHyperbolicDifferentialOperator})
and [[formal adjoint differential operator|formally self-adjoint]] (example \ref{FormallySelfAdjointKleinGordonOperator}).

=--

(e. g. [B&#228;r-Ginoux-Pfaeffle 07](Klein-Gordon+equation#BaerGinouxPfaeffle07), [B&#228;r 14, example 3.3](#Baer14))

+-- {: .num_example #GreenHyperbolicDiracOperator}
###### Example
**([[Dirac operator]] is [[Green hyperbolic differential operator|Green hyperbolic]])**

The [[Dirac equation]], hence the [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]]
of the [[mass|massive]] [[free field theory|free]] [[Dirac field]]  (example \ref{EquationOfMotionOfDiracFieldIsDiracEquation}) is a [[Green hyperbolic differential equation]] (def. \ref{GreenHyperbolicDifferentialOperator})
and [[formally adjoint differential operator|formally anti self-adjoint]] (example \ref{DiracOperatorOnDiracSpinorsIsFormallySelfAdjointDifferentialOperator}).

=--

([B&#228;r 14, corollary 3.15, example 3.16](#Baer14))


+-- {: .num_example #CausalGreenFunctionOfFormallyAdjointDifferentialOperatorAreFormallyAdjoint}
###### Example
**([[causal Green functions]] of [[formally adjoint differential operator|formally adjoint]] [[Green hyperbolic differential operators]] are [[formally adjoint differential operator|formally adjoint]])**

Let

$$
  P, P^\ast \;\colon\;\Gamma_\Sigma(E) \overset{}{\longrightarrow} \Gamma_\Sigma(E^\ast)
$$

be a pair of [[Green hyperbolic differential operators]] (def. \ref{GreenHyperbolicDifferentialOperator}) which are [[formally adjoint differential operator|formally adjoint]] (def. \ref{FormallyAdjointDifferentialOperators}).  Then also their [[causal Green functions]] $\mathrm{G}_P$ and $G_{P^\ast}$ (def. \ref{AdvancedAndRetardedGreenFunctions}) are [[formally adjoint differential operators]], up to a sign:

$$
  \left(
    \mathrm{G}_P
  \right)^\ast
  \;=\;
  - \mathrm{G}_{P^\ast}
  \,.
$$

=--

([Khavkine 14, (24), (25)](Green+hyperbolic+partial+differential+equation#Khavkine14))

We did not require that the [[advanced and retarded Green functions]] of a [[Green hyperbolic differential operator]] are unique;
in fact this is automatic:

+-- {: .num_prop #AdvancedAndRetardedGreenFunctionsForGreenHyperbolicOperatorAreUnique}
###### Proposition
**([[advanced and retarded Green functions]] of [[Green hyperbolic differential operator]] are unique)**

The [[advanced and retarded Green functions]] (def. \ref{AdvancedAndRetardedGreenFunctions}) of a [[Green hyperbolic differential operator]] (def. \ref{GreenHyperbolicDifferentialOperator}) are unique.

=--

([B&#228;r 14, cor. 3.12](Green+hyperbolic+differential+operator#Baer14})


Moreover we did not require that the [[advanced and retarded Green functions]] of a [[Green hyperbolic differential operator]]
come from [[integral kernels]] ("[[propagators]]"). This, too, is automatic:

+-- {: .num_prop #GreenFunctionsAreContinuous}
###### Proposition
**([[causal Green functions]] of [[Green hyperbolic differential operators]] are [[continuous linear maps]])**

Given a [[Green hyperbolic differential operator]] $P$ (def. \ref{GreenHyperbolicDifferentialOperator}), the advanced, retarded and causal Green functions of $P$ (def. \ref{AdvancedAndRetardedGreenFunctions}) are [[continuous linear maps]] with respect to the [[topological vector space]] structure from def. \ref{TVSStructureOnSpacesOfSmoothSections} and also have a unique continuous [[extension]] to the spaces of sections with larger support (def. \ref{CompactlySourceCausalSupport}) as follows:

$$
\begin{aligned}
  \mathrm{G}_{P,+}
    &\;\colon\;
  \Gamma_{\Sigma, pcp}(E^\ast)
    \longrightarrow
  \Gamma_{\Sigma, pcp}(E) ,
  \\
  \mathrm{G}_{P,-}
    &\;\colon\;
  \Gamma_{\Sigma, fcp}(E^\ast)
    \longrightarrow
  \Gamma_{\Sigma, fcp}(E) ,
  \\
  \mathrm{G}_{P}
    &\;\colon\;
  \Gamma_{\Sigma, tcp}(E^\ast)
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
  supp \mathrm{G}_{P,\pm}({\alpha}^*) \subseteq J^\pm(supp {\alpha}^*)
  \,.
$$

By the _[[Schwartz kernel theorem]]_ the continuity of $\mathrm{G}_{\pm}, \mathrm{G}$
implies that there are [[integral kernels]]

$$
  \Delta_{\pm}  \;\in\; \Gamma'_{\Sigma \times \Sigma}( E \boxtimes_\Sigma E )
$$

such that, in the notation of [[generalized functions]],

$$
  (G_{\pm} \alpha^\ast)(x)
   \;=\;
  \underset{\Sigma}{\int}
    \Delta_\pm(x,y) \cdot \alpha^\ast(y) \, dvol_\Sigma(y)
  \,.
$$

These [[integral kernels]] are called the _[[advanced and retarded propagators]]_. Similarly the combination

$$
  \label{CausalPropagator}
  \Delta \;\coloneqq\; \Delta_+ - \Delta_-
$$

is called the _[[causal propagator]]_.

=--

([B&#228;r 14, thm. 3.8, cor. 3.11](Green+hyperbolic+differential+operator#Baer14))




We now come to the main theorem on [[polynomial observables]]:

+-- {: .num_lemma #ExactSequenceOfGreenHyperbolicSystem}
###### Lemma
**([[exact sequence]] of [[Green hyperbolic differential operator]])**

Let $\Gamma_\Sigma(E) \overset{P}{\longrightarrow} \Gamma_\Sigma(E^\ast)$ be a [[Green hyperbolic differential operator]] (def. \ref{GreenHyperbolicDifferentialOperator}) with [[causal Green function]] $\mathrm{G}$ (def. \ref{GreenHyperbolicDifferentialOperator}). Then the sequences

$$
  \label{GreenOperatorExactSequenceFirst}
  \array{
  0
    &\to&
  \Gamma_{\Sigma,cp}(E)
   &\overset{P}{\longrightarrow}&
  \Gamma_{\Sigma,cp}(E^\ast)
    &\overset{\mathrm{G}_P}{\longrightarrow}&
  \Gamma_{\Sigma,scp}(E)
    &\overset{P}{\longrightarrow}&
  \Gamma_{\Sigma,scp}(E^\ast)
     &\to&
  0
  \\
  \\
  0
    &\to&
  \Gamma_{\Sigma,tcp}(E)
   &\overset{P}{\longrightarrow}&
  \Gamma_{\Sigma,tcp}(E^\ast)
    &\overset{\mathrm{G}_P}{\longrightarrow}&
  \Gamma_{\Sigma}(E)
    &\overset{P}{\longrightarrow}&
  \Gamma_{\Sigma}(E^\ast)
     &\to&
  0
  }
$$

of these operators restricted to functions with causally restricted supports as indicated (def. \ref{CompactlySourceCausalSupport})
are [[exact sequence]]s of [[topological vector spaces]] and continuous [[linear map]]s between them.

Under passing to [[dual spaces]] and using the isomorphisms of spaces of distributional sections (def. \ref{DistributionalSections}) from prop. \ref{DistributionsWithCausalSupports} this yields the following dual [[exact sequence]] of [[topological vector spaces]] and continuous [[linear maps]] between them:

$$
  \label{GreenHyperbolicOperatorDualExactSequence}
  \array{
  0
    &\to&
  \Gamma'_{\Sigma,tcp}(E)
   &\overset{P^*}{\longrightarrow}&
  \Gamma'_{\Sigma,tcp}(E^\ast)
    &\overset{-\mathrm{G}_{P^*}}{\longrightarrow}&
  \Gamma'_{\Sigma}(E)
    &\overset{P^*}{\longrightarrow}&
  \Gamma'_{\Sigma}(E^\ast)
    &\to&
  0
  \\
  \\
  0
    &\to&
  \Gamma'_{\Sigma,cp}(E)
   &\overset{P^*}{\longrightarrow}&
  \Gamma'_{\Sigma,cp}(E^\ast)
    &\overset{-\mathrm{G}_{P^*}}{\longrightarrow}&
  \Gamma'_{\Sigma,scp}(E)
    &\overset{P^*}{\longrightarrow}&
  \Gamma'_{\Sigma,scp}(E^\ast)
     &\to&
  0
  }
$$

=--

This is due to [[Igor Khavkine]], based on ([Khavkine 14, prop. 2.1](Green+hyperbolic+partial+differential+equation#Khavkine14));
for **proof** see at _[[Green hyperbolic differential operator]]_  [this lemma](Green+hyperbolic+partial+differential+equation#ExactSequenceOfGreenHyperbolicSystem).


+-- {: .num_cor #OnShellSpaceOfFieldHistoriesForFreeFieldTheoryGreenHyperbolic}
###### Corollary
**([[on-shell]] [[space of field histories]] for [[Green hyperbolic differential operator|Green hyperbolic]] [[free field theories]])**

Let $(E,\mathbf{L})$ be a [[free field theory]] [[Lagrangian field theory]] (def. \ref{LagrangianDensityForDiracField})
whose [[Euler-Lagrange equation|Euler-Lagrange]] [[equation of motion]] $P \Phi = 0$ is [[Green hyperbolic differential operator|Green hyperbolic]] (def. \ref{GreenHyperbolicDifferentialOperator}).

Then the [[on-shell]] [[space of field histories]] (or of [[field histories]] with spatially compact support, def. \ref{CompactlySourceCausalSupport}) is, as a [[vector space]], [[linear isomorphism|linearly isomorphic]]
to the [[quotient space]] of [[compact support|compactly supported]] sections (or of temporally compactly supported sections, def. \ref{CompactlySourceCausalSupport}) by the [[image]] of the [[differential operator]] $P$, and this isomorphism
is given by the [[causal Green function]] $\mathrm{G}_P$ (eq:CausalGreenFunction)

$$
  \label{SolutionSpaceIsomorphicToQuotientByImP}
  \array{
    \Gamma_{\Sigma,tcp}(E^\ast)/im(P)
      &\underoverset{\simeq}{\phantom{A}\mathrm{G}_P \phantom{A}}{\longrightarrow}&
    ker(P) \;=\; \Gamma_{\Sigma}(E)_{\delta_{EL}\mathbf{L} = 0}
    \\
    \Gamma_{\Sigma,cp}(E^\ast)/im(P)
      &\underoverset{\simeq}{\phantom{A}\mathrm{G}_P\phantom{A}}{\longrightarrow}&
    ker_{scp}(P) \;=\; \Gamma_{\Sigma,scp}(E)_{\delta_{EL}\mathbf{L} = 0}
    \,.
  }
$$

=--


+-- {: .proof}
###### Proof

This is a direct consequence of the [[exact sequence|exactness]] of the sequence (eq:GreenOperatorExactSequenceFirst)
in lemma \ref{ExactSequenceOfGreenHyperbolicSystem}.

We spell this out for the statement for $\Gamma_{\Sigma,scp}(E)_{\delta_{EL} \mathbf{L} = 0}$,
which follows from the first line in (eq:GreenOperatorExactSequenceFirst), the first statement
similarly follows from the second line of (eq:GreenOperatorExactSequenceFirst):

First the [[on-shell]] [[space of field histories]] is the [[kernel]] of $P$, by definition
of [[free field theory]] (def. \ref{LagrangianDensityForDiracField})

$$
  \Gamma_{\Sigma,scp}(E)_{\delta_{EL} \mathbf{L} = 0}
  \;=\;
  ker_{scp}(P)
  \,.
$$

Second, exactness of the sequence (eq:GreenOperatorExactSequenceFirst) at $\Gamma_{\Sigma,scp}(E)$ means that the
[[kernel]] $ker_{scp}(P)$ of $P$ equals the [[image]] $im(\mathrm{G}_{P})$. But by exactness of the sequence
at $\Gamma_{\Sigma,cp}(E^\ast)$ it follows that $\mathrm{G}_P$ becomes [[injective]] on the [[quotient space]]
$\Gamma_{\Sigma,cp}(E)^\ast/im(P)$. Therefore on this quotient space it becomes an isomorphism onto its [[image]].

=--

+-- {: .num_remark #LinearOnShellObservablesAreTheGeneralizedPDESolutionsNaiveVersion}
###### Remark

Under passing to [[dual vector spaces]], the linear isomorphism in corollary \ref{OnShellSpaceOfFieldHistoriesForFreeFieldTheoryGreenHyperbolic}
in turn yields [[linear isomorphisms]] of the form

$$
  \label{DualSolutionSpaceIsomorphicToQuotientByImP}
  \array{
    \left(\Gamma_{\Sigma,cp}(E^\ast)/im(P)\right)^\ast
      &\underoverset{\simeq}{(-)\circ \mathrm{G}_P}{\longleftarrow}&
    \left(ker_{scp}(P)\right)^\ast
    \\
    \left(\Gamma_\Sigma(E^\ast)/im(P)\right)^\ast
      &\underoverset{\simeq}{(-)\circ \mathrm{G}_P }{\longleftarrow}&
    \left(ker(P)\right)^\ast
  }
  \,.
$$

Except possibly for the issue of [[continuous map|continuity]] this says that
the linear on-shell [[observables]] (def. \ref{LinearObservables}) of a [[Green hyperbolic differential equation|Green hyperbolic]] [[free field theory]] are equivalently those linear off-shell observables which
are [[generalized solution of a PDE|generalized solutions]] of the [[formally adjoint differential operator|formally dual]]
[[equation of motion]] according to def. \ref{DistributionalDerivatives}.

That this remains true also for [[topological vector space]] [[structure]] follows with the dual exact sequence
(eq:GreenHyperbolicOperatorDualExactSequence). This is the statement of prop. \ref{DistributionsOnSolutionSpaceAreTheGeneralizedPDESolutions} below.

=--


+-- {: .num_prop #DistributionsOnSolutionSpaceAreTheGeneralizedPDESolutions}
###### Proposition
**([[distributions|distributional sections]] on a [[Green hyperbolic differential equation|Green hyperbolic]] solution space are the [[generalized PDE solutions]])**

Let $P, P \ast \;\colon\; \Gamma_\Sigma(E) \overset{}{\longrightarrow} \Gamma_\Sigma(E^\ast)$ be a pair of  [[Green hyperbolic differential operators]] (def. \ref{GreenHyperbolicDifferentialOperator}) which are [[formally adjoint differential operator|formally adjoint]] (def. \ref{FormallyAdjointDifferentialOperators}).

Then

1. the canonical pairing (from prop. \ref{DistributionsWithCausalSupports})

   $$
     \array{
       \Gamma'_{\Sigma,cp}(E^\ast) &\otimes& \Gamma_\Sigma(E)
         &\overset{}{\longrightarrow}&
       \mathbb{C}
       \\
       \alpha^\ast &,& \Phi &\mapsto& \int \alpha^\ast_a(x) \Phi^a(x)\, dvol_\Sigma(x)
     }
   $$

   induces a [[continuous linear map|continuous]] [[linear isomorphism]]

   $$
     \label{LinearDualOfSolutionSpaceIsLinearDualOfFullSpaceModuloImageOfDifferentialOperator}
     (ker(P))^\ast
     \;\simeq\;
     \Gamma'_{\Sigma,cp}(E^\ast)/im_{cp}(P^\ast)
   $$


1. a [[continuous linear functional]] on the solution space

   $$
     u_{sol} \in \left(ker(P)\right)^\ast
   $$

   is equivalently a [[distribution|distributional section]] (def. \ref{DistributionalSections})
   whose [[support of a distribution|support]] is spacelike
   compact (def. \ref{CompactlySourceCausalSupport}, prop. \ref{DistributionsWithCausalSupports})

   $$
     u \in \Gamma'_{\Sigma,scp}(E)
   $$

   and which is a [[distributional solution of a PDE|distributional solution]] (def. \ref{DistributionalDerivatives})
   to the differential equation

   $$
     P^\ast u = 0
     \,.
   $$

   Similarly, a [[continuous linear functional]] on the subspace of solutions that have spatially compact support (def. \ref{CompactlySourceCausalSupport})

   $$
     u_{sol} \in \left(ker(P)_{scp}\right)^\ast
   $$

   is equivalently a [[distribution|distributional section]] (def. \ref{DistributionalSections})
   without constraint on its [[support of a distribution|distributional support]]

   $$
     u \in \Gamma'_{\Sigma}(E)
   $$

   and which is a [[distributional solution of a PDE|distributional solution]] (def. \ref{DistributionalDerivatives})
   to the differential equation

   $$
     P^\ast u = 0
     \,.
   $$

   Moreover, these [[linear isomorphisms]] are both given by composition with
   the [[causal Green function]] $\mathrm{G}$ (def. \ref{AdvancedAndRetardedGreenFunctions}):

   $$
     \array{
       \left(ker(P)\right)^\ast
          &\underoverset{\simeq}{(-)\circ \mathrm{G}}{\longrightarrow}&
        \left\{
          u \in  \Gamma'_{\Sigma,scp}(E)
          \,\vert\,
          P^\ast u = 0
        \right\}
       \\
       \left(ker_{scp}(P)\right)^\ast
          &\underoverset{\simeq}{(-)\circ \mathrm{G}}{\longrightarrow}&
        \left\{
          u \in  \Gamma'_{\Sigma}(E)
          \,\vert\,
          P^\ast u = 0
        \right\}
     }
     \,.
   $$

=--

This follows from the [[exact sequence]] in lemma \ref{ExactSequenceOfGreenHyperbolicSystem}.
For details of the **proof** see at _[[Green hyperbolic differential operator]]_ [this prop.](Green+hyperbolic+partial+differential+equation#DistributionsOnSolutionSpaceAreTheGeneralizedPDESolutions),
due to [[Igor Khavkine]].

In conclusion we have found the following:


+-- {: .num_theorem #LinearObservablesForGreeFreeFieldTheoryAreDistributionalSolutionsToTheEquationsOfMotion}
###### Theorem
**(linear [[observables]] of [[Green hyperbolic differential operator|Green]] [[free field theory]] are the [[distributional solution of a PDE|distributional solutions]] to the [[formally adjoint differential operator|formally adjoint]] [[equations of motion]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory|Lagrangian]] [[free field theory]] (def. \ref{FreeFieldTheory})
which is a [[free field theory]] (def. \ref{FreeFieldTheory})
whose [[Euler-Lagrange equation|Euler-Lagrange]] [[differential equation|differential]] [[equation of motion]] $P \Phi = 0$ (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}) is [[Green hyperbolic differential equation|Green hyperbolic]] (def. \ref{GreenHyperbolicDifferentialOperator}), such as the [[Klein-Gordon equation]] (example \ref{GreenHyperbolicKleinGordonEquation})
or the [[Dirac equation]] (example \ref{GreenHyperbolicDiracOperator}). Then:

1. The linear off-shell observables (def. \ref{LinearObservables}) are equivalently the
   [[compactly supported distribution|compactly supported distributional sections]]  (def. \ref{DistributionalSections}) of the [[field  bundle]]:

   $$
     LinObs(E)
      \;\simeq\;
     \Gamma'_{\Sigma,cp}(E)
   $$

1. The linear on-shell [[observables]] (def. \ref{LinearObservables}) are equivalently the linear off-shell observables
   modulo the image of the [[differential operator]] $P$:

   $$
     \label{LinearOnShellObservablesAreLinearOffShellobservableModuloTheEquationsOfMotion}
     LinObs(E,\mathbf{L})
     \simeq
     LinObs(E)/im(P)
     \,.
   $$

   More generally the on-shell [[polynomial observables]] are identified with the off-shell polynomial observables (def. \ref{PolynomialObservables}) modulo the image of $P$:

   $$
     \label{PolynomialOnShellObservablesArePolynomialOffShellobservableModuloTheEquationsOfMotion}
     PolyObObs(E,\mathbf{L})
     \simeq
     PolyObs(E)/im(P)
     \,.
   $$



1. The linear on-shell [[observables]] (def. \ref{LinearObservables}) are also equivalently
   those spacelike compactly supported [[distribution|compactly distributional sections]]  (def. \ref{DistributionalSections})
   which are [[distributional solution of a PDE|distributional solutions]] of the [[formally adjoint differential operator|formally adjoint]] [[equations of motion]] (def. \ref{FormallyAdjointDifferentialOperators}), and this isomorphism is exhibited by precomposition with the [[causal propagator]] $\mathrm{G}$:

   $$
     LinObs(E,\mathbf{L})
      \;\underoverset{\simeq}{\phantom{A}(-)\circ\mathrm{G}_P \phantom{A}}{\longrightarrow}\;
     \left\{
       A \in \Gamma'_{\Sigma,scp}(E)
       \;\vert\;
       P^\ast A = 0
     \right\}
   $$

   Similarly the linear on-shell observables on spacelike compactly supported on-shell field histories (eq:SpaceOfObservablesOnFieldHistoriesOfSpatiallyCompactSupport) are equivalently the [[distributional solution of a PDE|distributional solutions]] without constraint on their [[support of a distribution|support]]:

   $$
     LinObs(E_{scp},\mathbf{L})
      \;\underoverset{\simeq}{\phantom{A}(-) \circ \mathrm{G}_P \phantom{A}}{\longrightarrow}\;
     \left\{
       A \in \Gamma'_{\Sigma}(E)
       \;\vert\;
       P^\ast A = 0
     \right\}
   $$

=--


+-- {: .proof}
###### Proof

The first statement follows with prop. \ref{LinearObservablesAreTheCompactlySupportedDistributions}
applied componentwise. The same proof applies verbatim to the subspace of solutions,
showing that $LinObs(E,\mathbf{L}) \simeq \left( ker(P)\right)^\ast$, with the [[dual topological vector space]] on the right.
With this the second and third statement follows by prop. \ref{DistributionsOnSolutionSpaceAreTheGeneralizedPDESolutions}.

=--

We will be interested in those [[linear observables]] which under the identification from theorem \ref{LinearObservablesForGreeFreeFieldTheoryAreDistributionalSolutionsToTheEquationsOfMotion} correspond to the [[non-singular distributions]] (because on these the [[Poisson-Peierls bracket]] of the theory is defined, theorem \ref{PPeierlsBracket} below):

+-- {: .num_defn #RegularLinearFieldObservables}
###### Definition
**(linear [[regular observables]] and [[operator-valued distribution|observable-valued distributions]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] (def. \ref{FreeFieldTheory}) whose [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] (prop. \ref{EulerLagrangeFormIsSectionOfLocalCotangentBundleOfJetBundleGaugeActionLieAlgebroid}) is [[Green hyperbolic differential equation|Green hyperbolic]] (def. \ref{GreenHyperbolicDifferentialOperator}).

Define the _[[regular linear observable|regular]]_ [[linear observables]] among the linear on-shell observables (def. \ref{LinearObservables}) to be the [[non-singular distributions]] on the [[on-shell]] [[space of field histories]], hence the [[image]]

$$
  LinObs(E_{scp},\mathbf{L})_{reg}
    \hookrightarrow
  LinObs(E_{scp},\mathbf{L})
$$

of the map

$$
  \label{RegularLinearObservables}
  \array{
    \mathbf{\Phi}
      &\colon&
    \Gamma_{\Sigma,cp}(E^\ast)
      &\longrightarrow&
    LinObs(E_{scp},\mathbf{L})
      &\hookrightarrow&
    Obs(E_{scp},\mathbf{L})
    \\
    && \alpha^\ast
    &\mapsto&
    \left(
      \Phi
        \mapsto
      \underset{\Sigma}{\int} \alpha^\ast_a(x) \Phi^a(x)
       \, dvol_\Sigma(x)
    \right)
  }
$$

By theorem \ref{LinearObservablesForGreeFreeFieldTheoryAreDistributionalSolutionsToTheEquationsOfMotion} we have the identification (eq:LinearDualOfSolutionSpaceIsLinearDualOfFullSpaceModuloImageOfDifferentialOperator) (eq:LinearOnShellObservablesAreLinearOffShellobservableModuloTheEquationsOfMotion)

$$
  \label{RegularLinearObservablesAreCompactlySupportedSectionsModuloImageOfP}
  LinObs(E_{scp},\mathbf{L})_{reg}
   \;\simeq\;
  \Gamma_{\Sigma,scp}(E^\ast)/im(P)
  \,.
$$

The point-evaluation [[field observables]] $\mathbf{\Phi}^a(x)$ (example \ref{PointEvaluationObservables}) are [[linear observables]] (example \ref{LinearPointEvaluationObservables}) but far from being regular (eq:RegularLinearObservables)
(except in [[spacetime]] [[dimension]] $p +1 = 0+1$). But the regular observables are precisely the
averages ("smearings") of these point evaluation observables against compactly supported weights.

Viewed this way, the defining inclusion of the [[regular observable|regular]] [[linear observables]] (eq:RegularLinearObservables) is itself
an _[[operator-valued distribution|observable valued distribution]]_

$$
  \label{AverageOfFieldObservableIsRegularLinearObservables}
  \array{
    \mathbf{\Phi} &\colon& \Gamma_{\Sigma,cp}(E^\ast) &\hookrightarrow& LinObs(E,\mathbf{L})
    \\
    && \alpha^\ast &\mapsto& \underset{\Sigma}{\int} \alpha^\ast_a(x) \mathbf{\Phi}^a(x)\, dvol_\Sigma(x)
  }
$$

which to a "smearing function" $\alpha^\ast$ assigns the observable which is the [[field observable]] smeared by (i.e. averaged against)
that smearing function.

Below in _[Free quantum fields](#FreeQuantumFields)_ we discuss how the [[polynomial Poisson algebra]] of regular polynomial observables of a [[free field theory]] may be [[deformation quantization|deformed]] to a [[non-commutative algebra|non-commutative]] [[algebra of quantum observables]]. Often this may be [[representation|represented]] by [[linear operators]] acting on some [[Hilbert space]].
In this case then $\mathbf{\Phi}$ above becomes a [[continuous linear functional]] from $\Gamma_{\Sigma,cp}(E)$ to a space of
linear operators on some Hilbert space. As such it is then called an _[[operator-valued distribution]]_.

=--


$\,$


**Local observables**
 {#LocalObservablesByTransgression}

We now discuss the sub-class of those [[observables]] which are "[[local field theory|local]]".

+-- {: .num_defn #SpacetimeSupport}
###### Definition
**(spacetime support)**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] over a [[spacetime]] $\Sigma$ (def. \ref{FieldsAndFieldBundles}),
with induced [[jet bundle]] $J^\infty_\Sigma(E)$

For every [[subset]] $S \subset \Sigma$ let

$$
  \array{
    J^\infty_\Sigma(E)\vert_S
      &\overset{\iota_S}{\hookrightarrow}&
    J^\infty_\Sigma(E)
    \\
    \downarrow &(pb)& \downarrow
    \\
    S &\hookrightarrow& \Sigma
  }
$$

be the corresponding restriction of the [[jet bundle]] of $E$.

The _spacetime support  _ $supp_\Sigma(A)$ of a [[differential form]] $A \in \Omega^\bullet(J^\infty_\Sigma(E))$
on the [[jet bundle]] of $E$ is the [[topological closure]] of the maximal subset $S \subset \Sigma$
such that the restriction of $A$ to the jet bundle restrited to this subset vanishes:

$$
  supp_\Sigma(A) \coloneqq Cl( \{ x \in \Sigma |  \iota_{\{x\}^\ast A = 0} \} )
$$

We write

$$
  \Omega^{r,s}_{\Sigma,cp}(E)
  \coloneqq
  \left\{
    A \in \Omega^{r,s}_\Sigma(E)
    \;\vert\;
    supp_\Sigma(A) \, \text{is compact}
  \right\}
    \;\hookrightarrow\;
  \Omega^{r,s}_\Sigma(E)
$$

for the subspace of differential forms on the jet bundle whose spacetime support is a [[compact subspace]].

=--

+-- {: .num_defn #TransgressionOfVariationalDifferentialFormsToConfigrationSpaces}
###### Definition
**([[transgression of variational differential forms]] to [[space of field histories]])**


Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] over a [[spacetime]] $\Sigma$ (def. \ref{FieldsAndFieldBundles}).
and let
$$
  \Sigma_r \hookrightarrow \Sigma
$$

be a [[submanifold]] of [[spacetime]] of dimension $r \in \mathbb{N}$. Recall the [[space of field histories]]
restricted to its [[infinitesimal neighbourhood]], denoted $\Gamma_{\Sigma_r}(E)$ (def. \ref{FieldsAndFieldBundles}).


Then the operation of _[[transgression of variational differential forms]]_ to $\Sigma_r$ is the [[linear map]]

$$
  \tau_{\Sigma_r}
   \;\colon\;
  \Omega^{\bullet,\bullet}_{\Sigma,cp}(E)
    \overset{  }{\longrightarrow}
  \Omega^\bullet\left(
    \Gamma_{\Sigma_r}(E)
   \right)
$$

that sends a variational differential form $A \in \Omega^{\bullet,\bullet}_{\Sigma,cp}(E)$
to the differential form $\tau_{\Sigma_r} \in \Omega^\bullet(\Gamma_{\Sigma_r}(E))$
(def. \ref{DifferentialFormsOnDiffeologicalSpaces}, example \ref{ModuliOfSDifferentialForms})
which to a smooth family on field histories

$$
  \Phi_{(-)}(-) \;\colon\; U \times N_\Sigma \Sigma_r \longrightarrow E
$$

assigns the differential form given by first forming the [[pullback of differential forms]] along the family of [[jet prolongation]] $j^\infty_\Sigma(\Phi_{(-)})$ followed by the [[integration of differential forms]] over $\Sigma_r$:

$$
  (\tau_{\Sigma}A)_\Phi
    \;\coloneqq\;
  \int_{\Sigma_r}  (j^\infty_\Sigma(\Phi_{(-)}))^\ast A
  \;\in\;
  \Omega^\bullet(U)
  \,.
$$


=--


+-- {: .num_remark #TransgressionToDimensionrSupportedOnHorizontalrForms}
###### Remark
**([[transgression of variational differential forms|transgression]] to dimension $r$ picks out horizontal $r$-forms)**

In def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces}
we regard [[integration of differential forms]] over $\Sigma_r$ as an operation defined on differential forms of all degrees, which vanishes except on forms of degree $r$, and hence transgression of variational differential forms
to $\Sigma_r$ vanishes except on the subspace

$$
  \Omega^{r,\bullet}_\Sigma(E)
  \;\subset\;
  \Omega^{\bullet,\bullet}_\Sigma(E)
$$

of forms of horizontal degree $r$.

=--

+-- {: .num_example #ActionFunctional}
###### Example
**([[adiabatic switching|adiabatically switched]] [[action functional]])**

Given a [[field bundle]] $E \overset{fb}{\longrightarrow} \Sigma$,
consider a [[local Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})

$$
  \mathbf{L} \in \Omega^{p+1,0}_\Sigma(E)
  \,.
$$

For any [[bump function]] $b \in C^\infty_{cp}(\Sigma)$, the [[transgression of variational differential forms|transgression]] of $b \mathbf{L}$
(def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces}) is called the _[[action functional]]_

$$
  \mathcal{S}_b \mathbf{L}
    \coloneqq
  \tau_{\Sigma}
  \left(
    b \mathbf{L}
  \right)
  \;\colon\;
  \Gamma_\Sigma(E)
    \longrightarrow
  \mathbb{R}
$$

induced by $\mathbf{L}$, "[[adiabatic switching|adiabatically switched]]" by $b$.

Specifically if the field bundle is a [[trivial vector bundle]] as in example \ref{TrivialVectorBundleAsAFieldBundle},
such that the Lagrangian density may be written in the form

$$
  \mathbf{L}
    \;=\;
  L
  \left(
    (x^\mu), (\phi^a), (\phi^a_{,\mu}),
    \cdots
  \right)
  \,
  b dvol_\Sigma
   \;\in\;
  \Omega^{p+1,0}_{\Sigma,cp}( E )
  \,.
$$

then its action functional takes a field history $\Phi$ to the value

$$
  \mathcal{S}_{b \mathbf{L}}(\Phi)
  \:\colon\;
  \int_\Sigma
    L
    \left(
      x,
      \left( \Phi^a(x) \right),
      \left(\frac{\partial \Phi^a}{\partial x^\mu}(x)\right),
      \cdots
    \right)
    \,
  b(x)
  dvol_\Sigma(x)
$$

=--


+-- {: .num_prop #TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative}
###### Proposition
**([[transgression of variational differential forms|transgression]] compatible with [[variational derivative]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] over a [[spacetime]] $\Sigma$ (def. \ref{FieldsAndFieldBundles})
and let $\Sigma_r \hookrightarrow \Sigma$ be a [[submanifold]] possibly [[manifold with boundary|with boundary]]
$\partial \Sigma_r \hookrightarrow \Sigma_r$. Write

$$
  \Gamma_{\Sigma_r}(E) \overset{(-)\vert_{\partial \Sigma_r}}{\longrightarrow} \Gamma_{\partial \Sigma_r}(E)
$$

for the boundary restriction map.

Then the operation of [[transgression of variational differential forms]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})

$$
  \tau_{\Sigma} \;\colon\; \Omega^{\bullet,\bullet}_{\Sigma,cp}(E) \longrightarrow \Omega^\bullet\left(\Gamma_{\Sigma_r}(E)\right)
$$

is compatible with the [[variational derivative]] $\delta$ and with the [[total derivative|total spacetime derivative]] $d$
in the following way:

1. On variational forms that are in the image of the total spacetime derivative
   a transgressive variant of the [[Stokes' theorem]] (prop. \ref{StokesTheorem}) holds:

   $$
     \tau_{\Sigma_r}(d \alpha) \;=\; ((-)\vert_{\partial \Sigma})^\ast \tau_{\partial \Sigma_r}( \alpha)
   $$

1. Transgression intertwines, up to a sign, the [[variational derivative]] $\delta$ on variational differential forms with the
   plain de Rham differential on the space of field histories:

   $$
     \tau_{\Sigma}\left(
       \delta \alpha
     \right)
     \;=\;
     (-1)^{p+1}\, d \,\tau_{\Sigma}(\alpha)
     \,.
   $$

=--


+-- {: .proof}
###### Proof

Regarding the first statement, consider a horizontally exact variational form

$$
  d \alpha \in \Omega^{r,s}_{\Sigma,cp}(E)
  \,.
$$

By prop. \ref{PullbackAlongJetProlongationIntertwinesHorizontalDerivative} the pullback of this form
along the jet prolongation of fields is exact in the $\Sigma$-direction:

$$
  (j^\infty_\Sigma\Phi_{(-)})^\ast(d \alpha )
  \;=\;
  d_\Sigma (j^\infty_\Sigma\Phi_{(-)})^\ast \alpha
  \,,
$$

(where we write $d = d_U + d_\Sigma$ for the de Rham differential on $U \times \Sigma$).
Hence by the ordinary [[Stokes' theorem]] (prop. \ref{StokesTheorem}) restricted to any $\Phi_{(-)} \colon U \to \Gamma_{\Sigma_r}(E)$
with restriction $(-)\vert_{\partial \Sigma_r} \circ \Phi_{(-)} \colon U \to \Gamma_{\Sigma_r}(E)$
the relation

$$
  \begin{aligned}
    (\Phi_{(-)})^\ast \tau_{\Sigma_r}(d \alpha)
    & =
    \int_{\Sigma_r}
      d_{\Sigma_r} (j^\infty_\Sigma\Phi_{(-)})^\ast\alpha
    \\
    & = \int_{\partial \Sigma_r} (j^\infty_\Sigma\Phi_{(-)})^\ast\alpha
    \\
    & = \int_{\partial \Sigma_r} (j^\infty_\Sigma ( (-)\vert_\Sigma \circ \Phi_{(-)}) )^\ast\alpha
    \\
    & =
    ( (-)\vert_\Sigma \circ \Phi_{(-)} )^\ast \tau_{\partial \Sigma_r}(\alpha)
    \\
    & =
    (\Phi_{(-)})^\ast ((-)\vert_{\Sigma_r})^\ast \tau_{\partial \Sigma_r}(\alpha)
    \,.
  \end{aligned}
  \,.
$$


Regarding the second statement: by the [[Leibniz rule]] for de Rham differential
([[product law]] of [[differentiation]]) it is sufficient to check the claim on variational
derivatives of local coordinate functions

$$
  \delta \phi^a_{\mu_1 \cdots \mu_k} b
  \in
  \Omega^{0,1}_\Sigma(E)
  \,.
$$

The [[pullback of differential forms]] (prop. \ref{PullbackOfDifferentialForms})
along the [[jet prolongation]] $j^\infty_\Sigma(\Phi_{(-)}) \colon U \times \Sigma \to J^\infty_\Sigma(E)$ has two contributions:
one from the variation along $\Sigma$, the other from variation along $U$:


1. By prop. \ref{PullbackAlongJetProlongationIntertwinesHorizontalDerivative},
for _fixed_ $u \in U$ the pullback of $\delta \phi^a_{\mu_1 \cdots \mu_k}$ along the jet prolongation vanishes.

1. For  fixed $x \in \Sigma$, the pullback of the full de Rham differential $\mathbf{d} \phi^a_{\mu_1\cdots \mu_k}$ is

   $$
     \begin{aligned}
       (\Phi_{(-)}(x))^\ast( \mathbf{d} \phi^a_{\mu_1\cdots \mu_k} )
       & =
       d_U (\Phi_{(-)}(x))^\ast(\phi^a_{\mu_1\cdots \mu_k})
       \\
       & =
       d_U \frac{ \partial^k \Phi_{(-)}(x)}{\partial x^{\mu^1} \cdots \partial x^{\mu_k}}
     \end{aligned}
   $$

   (since the full de Rham differentials always commute with pullback of differential forms by prop. \ref{PullbackOfDifferentialForms}),
   while the pullback of the horizontal derivative
$d \phi^a_{\mu_1\cdots \mu_k} = \phi^a_{\mu_1 \cdots \mu_{k} \mu_{k+1}} \mathbf{d}x^{\mu_{k+1}}$
vanishes at fixed $x \in \Sigma$.

This implies over the given smooth family $\Phi_{(-)}$ that

$$
  \begin{aligned}
    \tau_\Sigma\left(
      \delta \phi^a_{,\mu_1 \cdots \mu_k} b
    \right)\vert_{\Phi_{(-)}}
    & =
    \tau_\Sigma\left(
       \mathbf{d} ( \phi^a_{,\mu_1 \cdots \mu_k} b)
    \right)
    \vert_{\Phi_{(-)}}
      -
    \underset{ = 0 }{
    \underbrace{
    \tau_\Sigma
    \left(
      d (\phi^a_{,\mu_1 \cdots \mu_k} b)
    \right)\vert_{\Phi_{(-)}}
    }}
    \\
    & =
    \int_\Sigma d_U (\Phi_{(-)})^\ast ( \phi^a_{\mu_1\cdots \mu_k} b )
    \\
    & = (-1)^{p+1} d_U \int_\Sigma  (\Phi_{(-)})^\ast ( \phi^a_{\mu_1\cdots \mu_k} b )
    \\
    & = (-1)^{p+1} d_U \tau_{\Sigma}( \Phi_{(-)} )^\ast ( \phi^a_{\mu_1 \cdots \mu_k} )
    \,.
  \end{aligned}
$$

and since this holds covariantly for all smooth families $\Phi_{(-)}$, this implies the claim.

=--



+-- {: .num_example #VariationOfTheActionFunctional}
###### Example
**([[variational derivative|variation]] of the [[action functional]])**

Given a [[Lagrangian field theory]] $(E,\mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
then the derivative of its [[adiabatic switching|adiabatically switched]] [[action functional]]
(def. \ref{ActionFunctional}) equals the [[transgression of variational differential forms|transgression]]
of the [[Euler-Lagrange variational derivative]] $\delta_{EL} \mathbf{L}$ (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}):

$$
  d \mathcal{S}_{b \mathbf{L}}
  \;=\;
  \tau_\Sigma( b \delta_{EL}\mathbf{L} )
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the second statement of prop. \ref{TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative} we have

$$
  \begin{aligned}
    d \mathcal{S}_{b \mathbf{L}}
    & =
    \tau_\Sigma( \delta ( b \mathbf{L} )  )
  \end{aligned}
  \,,
$$

Moreover, by prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime} this is

$$
  \begin{aligned}
    \cdots
    & =
    \tau_\Sigma( \delta_{EL} b \mathbf{L} + d \Theta_{BFV,b} )
    \\
    & =
    \tau_\Sigma( \delta_{EL} b \mathbf{L} ) + \underset{= 0}{\underbrace{\tau_\Sigma( d \Theta_{BFV,b} )}}
  \end{aligned}
  \,,
$$

where the second term vanishes by the first statement of prop. \ref{TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative}.

=--


+-- {: .num_prop #PrincipleOfExtremalAction}
###### Proposition
**([[principle of extremal action]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

The [[de Rham differential]] $d \mathcal{S}_{b\mathbf{L}}$ of the [[action functional]] (example \ref{VariationOfTheActionFunctional})
vanishes at a field history

$$
  \Phi \in \Gamma_\Sigma(E)
$$

for all [[adiabatic switchings]] $b \in C^\infty_{cp}(\Sigma)$ constant on some
subset $\mathcal{O} \subset \Sigma$ (def. \ref{CutoffFunctions}) on those smooth collections of field histories

$$
  \Phi_{(-)} \;\colon\; U \longrightarrow \Gamma_\Sigma(E)
$$

around $\Phi$ which, as functions on $U$, are constant outside $\mathcal{O}$ (example \ref{DiffeologicalSpaceOfFieldHistories}, example \ref{SupergeometricSpaceOfFieldHistories})
precisely if $\Phi$ solves the [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]]
(def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}):

$$
  \left(
  \underset{ { {\mathcal{O} \subset \Sigma} \atop { b\vert_{\mathcal{O}} = const } } \atop { \Phi_{(-)}\vert_{\Sigma \setminus \mathcal{O}} = const }  }{\forall}
  \left(
     (\Phi_{(-)})^\ast d \mathcal{S}_{b \mathbf{L}}(\Phi) = 0
  \right)
  \right)
  \;\Leftrightarrow\;
  \left(
    j^\infty_\Sigma(\Phi)^\ast \left( \frac{\delta_{EL} L}{\delta \phi^a} \right) = 0
  \right)
  \,.
$$

=--


+-- {: .proof}
###### Proof

By prop. \ref{TransgressionOfVariationaldifferentialFormsCompatibleWithVariationalDerivative} we have

$$
  (\Phi_{(-)})^\ast d \mathcal{S}_{b \mathbf{L}}
  \;=\;
   \int_\Sigma
   j^\infty_\Sigma(\Phi_{(-)})^\ast (  \delta_{EL}  b \mathbf{L} )
   \,.
$$

By the assumption on $\Phi_{(-)}$ it follows that after pullback to $U$ the switching function $b$ is constant, so that
it commutes with the differentials:

$$
  (\Phi_{(-)})^\ast
  d \mathcal{S}_{b \mathbf{L}}
  \;=\;
   \int_\Sigma
   b
   j^\infty_\Sigma(\Phi_{(-)})^\ast (  \delta_{EL}   \mathbf{L} )
   \,.
$$

This vanishes at $\Phi$ for all $\Phi_{(-)}$ precisely if all components of $j^\infty_\Sigma(\Phi_{(-)})^\ast (  \delta_{EL}   \mathbf{L} )$
vanish, which is the statement of the Euler-Lagrange equations of motion.

=--


+-- {: .num_defn #LocalObservables}
###### Definition
**([[local observables]])**

Given a [[Lagrangian field theory]] $(E,\mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) with  [[on-shell]] [[space of histories]] $\Gamma_\Sigma(E)_{\delta_{EL} \mathbf{L} = 0}$ (eq:OnShellFieldHistories)
then the space

$$
  \label{GlobalObservables}
  Obs_\Sigma(E)
  \;\coloneqq\;
  C^\infty( \Gamma_\Sigma(E) )
$$

of _[[observables]]_ is simply the space of [[complex numbers|complex]]-valued [[smooth functions]]

$$
  A \;\colon\;  \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0} \longrightarrow \mathbb{C}
$$

on the [[on-shell]] [[space of field histories]] (eq:OnShellFieldHistories).
This is a [[star-algebra]] under pointwise [[complex conjugation]].

(That we consider functions with values in [[complex numbers]] instead of [[real numbers]] is a
reflection of the [[superposition principle]] in [[quantum physics]], more about this below.)

On the other hand the _[[local observables]]_ are the [[horizontal differential form|horizontal p+1-forms]]

1. of compact spacetime support (def. \ref{SpacetimeSupport})

1. modulo [[total spacetime derivatives]]

1. restricted to the [[shell]] $\mathcal{E}^\infty$ (eq:ProlongedShellInJetBundle):

$$
  LocObs_\Sigma(E) \;\coloneqq\; \left(\Omega^{p+1,0}_{\Sigma,cp}(E)/(im(d))\right)\vert_{\mathcal{E}^\infty}
$$

which we may identify with the subspace of all observables (eq:GlobalObservables)
on those that arise as the [[image]] under
[[transgression of variational differential forms]] $\tau_\Sigma$ (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces})
of local observables to [[functionals]] on the [[on-shell]] [[space of field histories]] (eq:OnShellFieldHistories):

$$
  LocObs_\Sigma(E)
    \overset{\tau_\Sigma}{\hookrightarrow}
  \in
  C^\infty\left( \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0} \right)
  \,.
$$

This is a sub-vector space inside all observables which is in general not closed under the product of functions. We write

$$
  \mathcal{F}
    \;\coloneqq\;
  \langle LocObs_\Sigma \rangle_{C^\infty\left(\Gamma_\Sigma(E)\right)_{\delta_{EL}\mathbf{L} = 0}}
$$

for the smallest subalgebra of observables, under the pointwise product, that contains all the local observables. This is called the algebra of _multilocal observables_.

=--


+-- {: .num_example }
###### Example
**([[local observables]] of the [[real scalar field]])**

Consider the [[field bundle]] of the [[real scalar field]] (example \ref{RealScalarFieldBundle}).

A typical example of [[local observables]] (def. \ref{LocalObservables}) in this case is
the "field amplitude averaged over a given spacetime region"
determined by a [[bump function]] $b \in C^\infty_{cp}(\Sigma)$. On an on-shell field history $\Phi$ this observable
takes as value the integral

$$
  \tau_\Sigma(b \phi)(\Phi) \;=\;  \int_\Sigma \Phi(x) b(x) dvol_\Sigma(x)
  \,.
$$

=--


+-- {: .num_example }
###### Example
**([[local observables]] of the [[electromagnetic field]])**

Consider the [[field bundle]] for [[free field theory|free]] [[electromagnetism]] on [[Minkowski spacetime]] $\Sigma$.

Then for $b \in C^\infty(\Sigma)$ a [[bump function]] on [[spacetime]], the [[transgression of variational differential forms|transgression]]
of the universal [[Faraday tensor]] (def. \ref{JetFaraday}) against $b$ times the [[volume form]] is a [[local observable]]
(def. \ref{LocalObservables}), namely the _[[field strength]]_ (eq:TensorFaraday) of the [[electromagnetic field]]
averaged over spacetime.

=--

For the construction of the [[algebra of quantum observables]] it will be important to notice that the
[[intersection]] between [[local observables]] and [[regular polynomial observables]] is very small:

+-- {: .num_example #RegularPolynomialLocalObservablesAreNecessarilyLinear}
###### Example
**([[local observable|local]] [[regular polynomial observables]] are [[linear observables]])**

An [[observable]] (def. \ref{Observable}) which is

1. a [[regular polynomial observable]] (def. \ref{PolynomialObservables});

1. a [[local observable]] (def. \ref{LocalObservables})

is necessarily

* a [[linear observable]] (def. \ref{LinearObservables}).

This is because non-linear local expressions are polynomials in the sense of def. \ref{PolynomialObservables}
with [[delta distribution]]-[[coefficients]], for instance for the [[real scalar field]] the $\Phi^2$ [[interaction]]
term is

$$
  \int (\Phi(x))^2 \, dvol_\Sigma(x)
  \;=\;
  \int \int \Phi(x) \Phi(y) \underset{ = \alpha^{(2)}(x,y) }{\underbrace{\delta(x-y)}} \, dvol_\Sigma(y)
$$

and so its [[coefficient]] $\alpha^{(2)}$ is manifestly not a [[non-singular distribution]].

=--



$\,$







**Infinitesimal observables**
 {#InfinitesimalObservables}

The definition of [[observables]] in def. \ref{Observable} and specifically of [[local observables]] in def. \ref{LocalObservables} uses explicit restriction to the [[shell]],
hence, by the [[principle of extremal action]] (prop. \ref{PrincipleOfExtremalAction}) to the "[[critical locus]]" of the [[action functional]]. Such [[critical loci]] are often hard to
handle explicitly. It helps to consider a "[[homological resolution]]" that is given, in good circumstances, by the corresponding
"[[derived critical locus]]". These we consider in detail below in _[Reduced phase space](#ReducedPhaseSpace)_.
In order to have good control over these resolutions, we here consider the first _[[perturbative quantum field theory|perturbative]]_
aspect of [[field theory]], namely we consider the restriction of [[local observables]] to just an
[[infinitesimal neighbourhood]] of a background [[on-shell]] field history:


+-- {: .num_defn #LocalObservablesOnInfinitesimalNeighbourhood}
###### Definition
**([[local observables]] around [[infinitesimal neighbourhood]] of background [[on-shell]] field history)**


Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) and whose [[Lagrangian density]] $\mathbf{L}$ is spacetime-independent (example \ref{ShellForSpacetimeIndependentLagrangians}).
Let $\Sigma \times \{\varphi\} \hookrightarrow \mathcal{E}$ be a constant section of the shell (eq:ConstantSectionOfTrivialShellBundle)
as in example \ref{ShellForSpacetimeIndependentLagrangians}.

Then we write

$$
  LocObs_\Sigma(E,\varphi)
$$

for the restriction of the [[local observables]] (def. \ref{LocalObservables}) to the fiberwise
[[infinitesimal neighbourhood]] (example \ref{InfinitesimalNeighbourhood}) of $\Sigma \times \{\varphi\}$.

Explicitly, this means the following:

First of all, by prop. \ref{JetBundleIsLocallyProManifold} the dependence of the Lagrangian density $\mathbf{L}$
on the order of field derivatives is bounded by some $k \in \mathbb{N}$ on some [[neighbourhood]] of $\varphi$ and hence,
by the spacetime independence of $\mathbf{L}$, on some neighbourhood of $\Sigma \times \{\varphi\}$.

Therefore we may restrict without loss to the order-$k$ jets. By slight abuse of notation we still write

$$
  \mathcal{E} \hookrightarrow J^k_\Sigma(E)
$$

for the corresponding shell. It follows then that the restriction of the ring $\Omega^{0,0}_{\Sigma,cp}(E)$ of smooth functions
on the jet bundle to the [[infinitesimal neighbourhood]] (example \ref{InfinitesimalNeighbourhood})
is equivalently the [[formal power series ring]] over $C^\infty_{cp}(\Sigma)$
in the variables

$$
  ((\phi^a- \varphi^a),
   (\phi^a_{,\mu}- \varphi^a_{,\mu}),
   \cdots,
   (\phi^a_{,\mu_1 \cdots \mu_k} - \varphi^a_{,\mu_1 \cdots \mu_k})
  )
$$

We denote this by

$$
  \label{FunctionsOnInfNbh}
  \Omega^{0,0}_{\Sigma,cp}(E,\varphi)
    \;\coloneqq\;
  C^\infty_{cp}(\Sigma)\left[ \left[ (\phi^a - \varphi^a ), (\phi^a_{,\mu} -\varphi^a_{,\mu}), \cdots, (\phi^a_{,\mu_1 \cdots \mu_k}- \varphi^a_{,\mu_1 \cdots \mu_k}) \right] \right]
  \,.
$$

A key consequence is that the further restriction of this ring to the [[shell]] $\mathcal{E}^\infty$ (eq:ProlongedShellInJetBundle)
is now simply the further [[quotient ring]] by the ideal generated by the [[total spacetime derivatives]]
of the components $\frac{\partial_{EL}L}{\delta \phi^a}$ of
the [[Euler-Lagrange form]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}).

$$
  \label{ObservablesOnInfinitesimalNeighbourhoodOfZeroInShellInFieldFiber}
  \begin{aligned}
    \Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}}
      & \coloneqq
    \Omega^{0,0}_{\Sigma,cp}(E,\varphi)
      /
    \left(
      \frac{d^k}{ d x^{\mu_1} \cdots d x^{\mu_l}} \frac{\delta_{EL} L}{\delta \phi^a}
    \right)_{ { a \in \{1, \cdots, s\} }  \atop { { l \in \{1, \cdots, k\} } \atop { \mu_r \in \{0, \cdots, p\} }   } }
    \\
    & =
  C^\infty_{cp}(\Sigma)\left[ \left[ (\phi^a - \varphi^a ), (\phi^a_{,\mu} -\varphi^a_{,\mu}), \cdots, (\phi^a_{,\mu_1 \cdots \mu_k}- \varphi^a_{,\mu_1 \cdots \mu_k}) \right] \right]
   /
  \left(
    \frac{d^k}{ d x^{\mu_1} \cdots d x^{\mu_l}} \frac{\delta_{EL} L}{\delta \phi^a}
  \right)_{ { a \in \{1, \cdots, s\} }  \atop { { l \in \{1, \cdots, k\} } \atop { \mu_r \in \{0, \cdots, p\} }   } }
  \end{aligned}
  \,.
$$

Finally the [[local observables]] restricted to the infinitesimal neighbourhood is the module

$$
  \label{LocalObservablesRestrictedToInfinitesimalNeighbourhood}
  LocObs_\Sigma(E,\varphi)
    \;\simeq\;
  \left(
     \Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}} \langle dvol_\Sigma \rangle
  \right)/(im(d))
  \,.
$$


=--

The space of local observables in def. \ref{LocalObservablesOnInfinitesimalNeighbourhood} is the
[[quotient]] of a [[formal power series algebra]] by the components of the [[Euler-Lagrange form]]
and by the [[image]] of the horizontal spacetime [[de Rham differential]]. It is convenient
to also conceive of the components of the [[Euler-Lagrange form]] as the [[image]] of a [[differential]],
for then the algebra of local observables obtaines a [[cochain cohomology|cohomological]] interpretation,
which will lend itself to computation. This differential, whose image is the components of the
[[Euler-Lagrange form]], is called the _[[BV-differential]]. We introduce this
now first (def. \ref{BVComplexOfOrdinaryLagrangianDensity} below) in a direct ad-hoc way.
Further [below](#ReducedPhaseSpace) we discuss the conceptual nature of this differential
as part of the construction of the [[reduced phase space]] as a [[derived critical locus]] (example \ref{DerivedProlongedShellInAbsenceOfExplicitGaugeSymmetries} below).


+-- {: .num_defn #BVComplexOfOrdinaryLagrangianDensity}
###### Definition
**([[local BV-complex]] of ordinary [[Lagrangian density]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
whose [[field bundle]] $E$ is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) and whose [[Lagrangian density]] $\mathbf{L}$ is spacetime-independent (example \ref{LocalObservablesOnInfinitesimalNeighbourhood}).
Let $\Sigma \times \{\varphi\} \hookrightarrow \mathcal{E}^\infty$ be a constant section of the shell (eq:ConstantSectionOfTrivialShellBundle).

In correspondence with def. \ref{LocalObservablesOnInfinitesimalNeighbourhood}, write

$$
  \Gamma_{\Sigma,cp}(T_\Sigma J^\infty_\Sigma E,\varphi)
  \simeq
  \Gamma_{\Sigma,cp}(J^\infty_\Sigma T_\Sigma E,\varphi)
  \;\in\;
  \Omega^{0,0}_{\Sigma,cp}(E) Mod
$$

for the restriction of [[vertical vector fields]] on the [[jet bundle]] to the fiberwise [[infinitesimal neighbourhood]]
(example \ref{InfinitesimalNeighbourhood}) of $\Sigma \times {\varphi}$.

Now we regard this as a _[[graded module]]_ over $\Omega^{0,0}_{\Sigma,cp}(E,\varphi)$ (eq:FunctionsOnInfNbh) concentrated in degree $-1$:

$$
  \Gamma_{\Sigma,cp}(J^\infty_\Sigma T_\Sigma E,\varphi)[-1]
  \;\in\;
  \Omega^{0,0}_{\Sigma,cp}(E) Mod^{\mathbb{Z}}
  \,.
$$

This is called the module of _[[antifields]]_ corresponding the given [[type]] of [[field (physics)|fields]] encoded by $E$.

If the [[field bundle]] is a [[trivial vector bundle]] (example \ref{TrivialVectorBundleAsAFieldBundle}) with field coordinates
$(\phi^a)$, then we write

$$
  \label{AntifieldCoordinates}
  \phi^{\ddagger}_{a,\mu_1 \cdots \mu_l}
  \;\coloneqq\;
  \left(
     \partial_{(\phi^a_{\mu_1 \cdots \mu_l})}
  \right)[-1]
  \;\in\;
  \Gamma_{\Sigma,cp}(T_\Sigma J^\infty_\Sigma E,\varphi)[-1]
$$

for the vector field generator that takes derivatives along $\partial_{\phi^a_{,\mu_1 \cdots \mu_k}}$, but regarded now in degree -1.

Evaluation of vector fields in the
[[total spacetime derivatives]] $\frac{d^l}{d x^{\mu_1} \cdots d x^{\mu_l}} \delta\mathbf{L} \in \Omega^{p,0}_\Sigma(E) \wedge \delta \Omega^{0,0}_\Sigma(E)$ of the [[variational derivative]]  (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) yields a [[linear map]]
over $\Omega^{\bullet,\bullet}_{\Sigma,cp}(E,\varphi)$ (eq:ObservablesOnInfinitesimalNeighbourhoodOfZeroInShellInFieldFiber)

$$
  \iota_{(-)}\delta_{EL} \mathbf{L}
   \;\colon\;
  \Gamma_{\Sigma,cp}( J^\infty_\Sigma T_\Sigma E,\varphi)[-1]
    \longrightarrow
  \Omega^{p+1,0}_{\Sigma,cp}(E,\varphi)
  \,.
$$

If we use the [[volume form]] $dvol_\Sigma$ on [[spacetime]] $\Sigma$ to induce an identification

$$
  \Omega^{p+1,0}_\Sigma(E) \;\simeq\; C^\infty(J^\infty_\Sigma(E))\langle dvol_\sigma\rangle
$$

with respect to which the [[Lagrangian density]] decomposes as

$$
  \mathbf{L} = L dvol_\Sigma
$$

then this is a $\Omega^{0,0}_\sigma(E,\varphi)$-[[linear map]] of the form

$$
  \iota_{(-)}{\delta L_{EL}}
    \;\colon\;
  \Gamma_{\Sigma,cp}^{ev}(T_\Sigma E,\varphi)[-1]
    \longrightarrow
  \Omega^{0,0}_{\Sigma,cp}(E,\varphi)
  \,.
$$

In the special case that the [[field bundle]] $E \overset{fb}{\to} \Sigma$ is a [[trivial vector bundle]]
(example \ref{TrivialVectorBundleAsAFieldBundle}) with [[field (physics)|field]] coordinates $(\phi^a)$
so that the [[Euler-Lagrange form]] has the coordinate expansion

$$
  \delta_{EL} \mathbf{L}
  \;=\;
  \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a} \delta \phi^a
$$

then this map is given on the [[antifield]] basis elements (eq:AntifieldCoordinates) by

$$
  \iota_{(-)} {\delta L_{EL}}
  \;\colon\;
  \phi^{\ddagger}_{a,\mu_1 \cdots \mu_l}
    \;\mapsto\;
  \frac{d^l}{d x^{\mu_1} \cdots d x^{\mu_l}} \frac{\delta_{EL} L}{\delta \phi^a}
  \,.
$$

Consider then the [[symmetric algebra|graded symmetric algebra]]

$$
  C^\infty( J^\infty_\Sigma((T_\Sigma E)[-1] \times_\Sigma E, \varphi) )
  \;\coloneqq\;
  Sym_{\Omega^{0,0}_{\Sigma,cp}(E,\varphi)}\left(
    \Gamma_{\Sigma,cp}(J^\infty_\Sigma T_\Sigma E,\varphi)[-1]
  \right)
$$

which is generated over $\Omega^{0,0}_{\Sigma,cp}(E,\varphi)$ from the module of vector fields in degree -1.

If we think of a single vector field as a fiber-wise [[linear function]] on the [[cotangent bundle]],
and of a [[multivector field]] similarly as a [[multilinear function]] on the cotangent bundle, then we may
think of this as the algebra of functions on the [[infinitesimal neighbourhood]] (example \ref{InfinitesimalNeighbourhood}) of $\varphi$
inside the [[graded manifold]] $(T_\Sigma E)[-1] \times_\Sigma E$.


Let now

$$
  \label{BVDifferentialForOrdinaryLagrangian}
  s_{BV}
  \;\colon\;
  C^\infty( J^\infty_\Sigma((T_\Sigma E)[-1] \times_\Sigma E, \varphi) )
    \;\longrightarrow\;
  C^\infty( J^\infty_\Sigma((T_\Sigma E)[-1] \times_\Sigma E, \varphi) )
$$

be the unique extension of the linear map $\iota_{(-)}{\delta_{EL} L}$ to an $\mathbb{R}$-linear [[derivation]] of degree +1 on this algebra.


The resulting [[differential graded-commutative algebra]] over $\mathbb{R}$

$$
  \Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}_{BV}}
    \;\coloneqq\;
  \left(
  C^\infty( J^\infty_\Sigma((T_\Sigma E)[-1] \times_\Sigma E, \varphi) )
    \,,\,
    s_{BV}
  \right)
$$

is called the _[[local BRST cohomology|local]] [[BV-complex]]_
of the Lagrangian field theory at the background solution $\varphi$.
This is the CE-algebra of the infintiesimal neighbourhood of $\Sigma \times \{\varphi\}$
in the derived prolonged shell (def. \ref{DerivedProlongedShell}).
In this case, in the absence of any explicit infinitesimal gauge symmetries,
this is an example of a _[[Koszul complex]]_.

There are canonical homomorphisms of [[dgc-algebras]], one from the
algebra of functions $\Omega^{0,0}_{\Sigma,cp}(E,\varphi)$ on the [[infinitesimal neighbourhood]]
of the background solution $\varphi$ to the local BV-complex
and from there to the
local observables on the  neighbourhood of the background solution $\varphi$ (eq:ObservablesOnInfinitesimalNeighbourhoodOfZeroInShellInFieldFiber), all considered
with compact spacetime support:

$$
    \Omega^{0,0}_{\Sigma,cp}(E,\varphi)
      \longrightarrow
    \Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}_{BV}}
      \longrightarrow
    \Omega^{0,0}_{\Sigma,cp}(E,\varphi)\vert_{\mathcal{E}}
$$

such that the composite is the canonical [[quotient]] [[coprojection]].

Similarly we obtain a factorization for the entire [[variational bicomplex]]:

$$
  \label{ComparisonMorphismFromOrdinaryBVComplexToLocalObservables}
    \Omega^{\bullet,\bullet}_\Sigma(E,\varphi)
      \longrightarrow
    \Omega^{\bullet,\bullet}_\Sigma(E,\varphi)\vert_{\mathcal{E}_{BV}}
      \longrightarrow
    \Omega^{\bullet,\bullet}_\Sigma(E,\varphi)\vert_{\mathcal{E}}
    \,,
$$

where $\Omega^{\bullet,\bullet}_\Sigma(E,\varphi)\vert_{\mathcal{E}_{BV}}$
is now triply graded, with three anti-commuting differentials $d$ $\delta$ and $s_{BV}$.

By construction this is now such that the local observables (def. \ref{LocalObservables})
are the [[cochain cohomology]] of this complex in horizontal form degree p+1, vertical degree 0
and BV-degree 0:

$$
  LocObs_\Sigma(E) \simeq \Omega^{p+1,0}_{\Sigma,cp}(E)/(im(s_{BV} + d))
  \,.
$$

=--




$\,$

**States**
 {#StatesArePositiveLinearFunctionals}


+-- {: .num_defn #StarAlgebra}
###### Definition
**([[star algebra]])**

A _[[star ring]]_ is a [[ring]] $R$ equipped with

* a [[linear map]]

  $(-)^\ast \;\colon\; R \longrightarrow R$

such that

* ([[involution]]) $((-)^\ast)^\ast = id$;

* ([[antihomomorphism]])

  1. $(a b)^\ast = b^\ast a^\ast$ for all $a,b \in R$

  1. $1^\ast = 1$.

A [[homomorphism]] of star-rings

$$
  f \;\colon\; (R_1, (-)^\ast) \longrightarrow (R_2, (-)^\dagger)
$$

is a [[homomorphism]] of the underlying [[rings]]

$$
  f \;\colon\; R_1 \longrightarrow R_2
$$

which respects the star-[[involutions]] in that

$$
  f \circ (-)^\ast \;=\; (-)^\dagger \circ f
  \,.
$$

A _[[star algebra]]_ $\mathcal{A}$ over a [[commutative ring|commutative]] star-ring $R$ in an [[associative algebra]] $\mathcal{A}$ over $R$ such that the inclusion

$$
  R \hookrightarrow \mathcal{A}
$$

is a star-homomorphism.

=--

+-- {: .num_examples #StarAlgebraOfObservables}
###### Examples
**([[complex number]]-valued [[observables]] are [[star-algebra]] under pointwise product and pointwise [[complex conjugation]])**

The [[complex numbers]] $\mathbb{C}$ carry the [[structure]] of a [[star-ring]] (def. \ref{StarAlgebra}) with star-operation given by [[complex conjugation]].

Given any space $X$, then the [[algebra of functions]] on $X$ with values in the [[complex numbers]] carries the [[structure]] of a [[star-algebra]] over the star-ring $\mathbb{C}$ (def. \ref{StarAlgebra}) with star-operation given by pointwise [[complex conjugation]] in the [[complex numbers]].

In particular for $(E,\mathbf{L})$ a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) then its [[on-shell]] [[observables]] $Obs(E,\mathbf{L})$ (def. \ref{Observable}) carry the structure of a [[star-algebra]] this way.


=--

+-- {: .num_defn #StateOnAStarAlgebra}
###### Definition
**([[state on a star-algebra]])**

Given a [[star algebra]] $(\mathcal{A}, (-)^\ast)$ (def. \ref{StarAlgebra})
over the star-ring of [[complex numbers]] (def. \ref{StarAlgebraOfObservables}) a _[[state on a star-algebra|state]]_ is a [[function]] to the [[complex numbers]]

$$
  \langle -\rangle
  \;\colon\;
  Obs_\Sigma \longrightarrow \mathbb{C}
$$

such that

1. (linearity) this is a complex-[[linear map]]:

   $$
     \left\langle
       c_1 A_1 + c_2 A_2
     \right\rangle
     \;=\;
     c_1 \langle A_1 \rangle + c_2 \langle A_2 \rangle
   $$

1. (positivity) for all $A \in Obs$ we have that

   $$
     \langle A^\ast A \rangle \geq 0 \;\in\; \mathbb{R}
   $$

   where on the left $A^\ast$ is the [[star-algebra|star-operation]] from

1. (normalization)

   $$
     \langle 1 \rangle \;=\; 1
     \,.
   $$

=--

(e.g. [Bordemann-Waldmann 96](state+on+a+star-algebra#BordemannWaldmann96), [Fredenhagen-Rejzner 12, def. 2.4](state+on+a+star-algebra#FredenhagenRejzner12), [Khavkine-Moretti 15, def. 6](state+on+a+star-algebra#KhavkineMoretti15))

+-- {: .num_remark #ProbabilityTheoreticInterpretationOfStateOnAStarAlgebra}
###### Remark
**([[probability theory|probability theoretic]] interpretation of [[state on a star-algebra]])**

A [[star algebra]] $\mathcal{A}$ (def. \ref{StarAlgebra}) equipped with a [[state on a star-algebra|state]] $\mathcal{A} \overset{\langle -\rangle}{\longrightarrow} \mathbb{C}$ (def. \ref{States}) is also called a _[[quantum probability space]]_, at least when $\mathcal{A}$ is in fact a [[von Neumann algebra]].

For this interpretation we think of each element $A \in \mathcal{A}$ as an [[observable]] as in example \ref{StarAlgebraOfObservables} and of the state as assigning _[[expectation values]]_.

=--




+-- {: .num_remark #StatesFormAConvexSet}
###### Remark
**([[state on a star-algebra|states]] form a [[convex set]])**

For $\mathcal{A}$ a unital [[star-algebra]] (def. \ref{StarAlgebra}), the [[set]] of [[state on a star-algebra|states]] on $\mathcal{A}$ according to def. \ref{StateOnAStarAlgebra} is naturally a [[convex set]]: For $\langle (-)\rangle_1, \langle - \rangle_2 \colon \mathcal{A} \to \mathbb{C}$ two [[state on a star-algebra|states]] then for every $p \in [0,1] \subset \mathbb{R}$ also the [[linear combination]]

$$
  \array{
    \mathcal{A}
     &\overset{p \langle (-)\rangle_1 + (1-p) \langle (-)\rangle_2}{\longrightarrow}&
    \mathbb{C}
    \\
    A &\mapsto& p \langle A \rangle_1 + (1-p) \langle A \rangle_2
  }
$$


is a [[state on a star-algebra|state]].

=--

+-- {: .num_defn #PureStateOnAStarAlgebra}
###### Definition
**([[pure state]])**

A [[state on a star-algebra|state]] $\rho \colon \mathcal{A} \to \mathbb{C}$ on a unital [[star-algebra]] (def. \ref{StateOnAStarAlgebra}) is called a _[[pure state]]_ if it is extremal in the [[convex set]] of all states (remark \ref{StatesFormAConvexSet}) in that an identification

$$
  \langle (- )\rangle = p \langle (-)\rangle_1 + (1-p) \langle (-)\rangle_2
$$

for $p \in (0,1)$ implies that $\langle (-) \rangle_1 = \langle (-)\rangle_2$ (hence $= \langle (-)\rangle$).

=--


+-- {: .num_prop #ClassicalProbabilityMeasureAsStateOnMeasurableFunctions}
###### Proposition
**(classical [[probability measure]] as state on [[measurable functions]])**

For $\Omega$ classical [[probability space]], hence a [[measure space]] which normalized total measure $\int_\Omega d\mu = 1$, let $\mathcal{A} \cloneqq L^1(\Omega)$ be the algebra of Lebesgue [[measurable functions]] with values in the [[complex numbers]], regarded as a [[star algebra]] (def. \ref{StarAlgebra}) by pointwise [[complex conjugation]] as in example \ref{StarAlgebraOfObservables}. Then forming the [[expectation value]] with respect to $\mu$ defines a [[state on a star-algebra|state]] (def. \ref{StateOnAStarAlgebra}):

$$
  \array{
    L^1(\Omega)
      &\overset{\langle (-)\rangle_\mu}{\longrightarrow}&
    \mathbb{C}
    \\
    A &\mapsto& \int_\Omega A d\mu
  }
$$


=--

+-- {: .num_example #ElementsOfHilbertSpaceAsPureStates}
###### Example
**(elements of a [[Hilbert space]] as [[pure states]] on [[bounded operators]])**

Let $\mathcal{H}$ be a [[complex numbers|complex]] [[separable Hilbert space|separable]] [[Hilbert space]] with [[inner product]] $\langle -,-\rangle$ and let $\mathcal{A} \coloneqq \mathcal{B}(\mathcal{H})$ be the algebra of [[bounded operators]], regarded as a [[star algebra]] (def. \ref{StarAlgebra}) under forming [[adjoint operators]]. Then for every element $\psi \in \mathcal{H}$ of unit [[norm]] $\langle \psi,\psi\rangle = 1$ there is the [[state on a star-algebra|state]] (def. \ref{StateOnAStarAlgebra}) given by

$$
  \array{
    \mathcal{B}(\mathcal{H})
      &\overset{\langle (-)\rangle_\psi}{\longrightarrow}&
     \mathbb{C}
     \\
     A &\mapsto& \langle \psi \vert\, A \, \vert \psi \rangle &\coloneqq& \langle \psi, A \psi \rangle
  }
$$

These are [[pure states]] (def. \ref{PureStateOnAStarAlgebra}).

More general states in this case are given by [[density matrices]].

=--

+-- {: .num_theorem #GNSConstruction}
###### Theorem
**([[GNS construction]])**

Given

1. a [[star-algebra]], $\mathcal{A}$ (def. \ref{StarAlgebra});

1. a [[state on a star-algebra|state]], $\langle (-)\rangle \;\colon\; \mathcal{A} \to \mathbb{C}$ (def. \ref{StateOnAStarAlgebra})

there exists

1. a [[star-representation]]

   $$
     \pi
     \;\colon\;
     \mathcal{A}
      \longrightarrow
      End(\mathcal{H})
   $$

   of $\mathcal{A}$ on some [[Hilbert space]] $\mathcal{H}$

1. a [[cyclic vector]] $\psi \in \mathcal{H}$

such that $\langle (-)\rangle$ is the state corresponding to $\psi$ via example \ref{ElementsOfHilbertSpaceAsPureStates}, in that

$$
  \begin{aligned}
    \langle A \rangle
      & = \langle \psi \vert\, A \, \vert \psi \rangle
      \\
      & \coloneqq
      \langle \psi , \pi(A) \psi \rangle
  \end{aligned}
$$

for all $A \in \mathcal{A}$.

=--

([Khavkine-Moretti 15, theorem 1](GNS+construction#KhavkineMoretti15))



+-- {: .num_defn #ClassicalState}
###### Definition
**(classical state)**

Given a [[Lagrangian field theory]] $(E,\mathbf{L})$ (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) then a _classical state_ is a [[state on a star-algebra|state on the star algebra]] (def. \ref{StateOnAStarAlgebra}) of [[on-shell]] [[observables]] (example \ref{StarAlgebraOfObservables}):

$$
  \langle -\rangle
  \;\colon\;
  Obs(E,\mathbf{L})
   \longrightarrow
  \mathbb{C}
  \,.
$$


=--



Below we consider _[[quantum states]]_. These are defined just as in def. \ref{ClassicalState}, only that now the algebra of observables is equipped with another product, which changes the meaning of the product expression $A^\ast A$ and hence the positivity condition in def. \ref{StateOnAStarAlgebra}.


$\,$

This concludes our discussion of [[observables]]. In the [next chapter](#PhaseSpace) we consider the
construction of the [[covariant phase space]] and of the [[Poisson-Peierls bracket]] on [[observables]].
