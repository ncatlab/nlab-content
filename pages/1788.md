

## Gauge symmetries
 {#GaugeSymmetries}

The existence of the [[covariant phase space]] (prop. \ref{CovariantPhaseSpace}) of a [[Lagrangian field theory]]
requires the existence of [[Cauchy surfaces]] (def. \ref{CauchySurface}) for its [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] This the case of [[free field theory]] (def. \ref{FreeFieldTheory}) this means that the [[equations of motion]] are [[Green hyperbolic differential equation|Green hyperbolic]] (def. \ref{GreenHyperbolicDifferentialOperator}).

We have seen that this is the case for instance for the [[scalar field]] (example \ref{GreenHyperbolicKleinGordonEquation})
and the [[Dirac field]] (example \ref{GreenHyperbolicDiracOperator}), but it is not the case generally,
for instance it fails for the [[electromagnetic field]] (example \ref{ElectromagnetismEl}), the [[Yang-Mills field]] (example \ref{YangMillsLagrangian}) and the [[B-field]] (example \ref{BFieldLagrangianDensity}).
An [[obstruction]] to the existence of the [[covariant phase space]] turns out to be (prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces} below)
the presence of [[infinitesimal symmetries of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents})
that have compact spacetime support (def. \ref{SpacetimeSupport}).


An class of examples of such are those
[[infinitesimal symmetries of the Lagrangian]] which occur
linearly _parameterized_  by arbitrary [[sections]] (and their [[derivatives]]) of some [[vector bundle]] on [[spacetime]].
Because then for every choice of section of [[compact support]] the corresponding symmetry will have compact spacetime support.
These parameterized [[infinitesimal symmetries of the Lagrangian]] are called _[[infinitesimal gauge symmetries]]_,
and their parameters we call the _[[gauge parameters]]_ (def. \ref{GaugeParameters} below).


Typically all compactly supported [[infinitesimal symmetries of the Lagrangian]] arise from parameterized symmetries this way; this is notably the case for the [[Lagrangian density]] of the [[electromagnetic field]] (example \ref{InfinitesimalGaugeSymmetryElectromagnetism}) and more generally of the [[Yang-Mills field]].

Therefore the presence of [[infinitesimal symmetries of the Lagrangian]] with compact spacetime support is a defect of the theory
which however implies its own solution, by indicating which [[relations]] ought to be promoted
to "[[gauge equivalences|gauge]]" [[equivalences]]. 

This obstruction is neatly
captured by the [[cochain cohomology]] of the _[[local BV-complex]]_ (def. \ref{BVComplexOfOrdinaryLagrangianDensity}) of the Lagrangian field theory (prop. \ref{BVComplexIsHomologicalResolutionPreciselyIfNoNonTrivialImplicitGaugeSymmetres} below).
This may be understood as the [[algebra of functions]] on an extension of the [[jet bundle]] from a
(locally pro-finite dimensional, prop. \ref{InfinitesimalActionByLieAlgebra}) [[smooth manifold]] to
a [[differential graded manifold]].
This appearance of [[homotopy theory]] in the guise of [[homological algebra]] in Lagrangian field theory
paves the way to understanding the cause of the obstruction: It disappears when the
[[field bundle]] (or more generally its [[jet bundle]]) is promoted to its _infinitesimal [[homotopy quotient]]_
by the [[action]] of these compactly supported symmetries (the "[[action Lie algebroid]]", def. \ref{ActionLieAlgebroid} below).

Passing to this [[homotopy quotient]]
means to hard-wire into the geometry of the  types of [[field (physics)|field]] their _[[equivalence]]_ under these symmetries: in physics this is called _[[gauge equivalence]]_.  The result is called the "[[reduced phase space]]", which we turn to further [below](#ReducedPhaseSpace).




$\,$

We now discuss these topics

* [Infinitesimal gauge symmetries](#InfinitesimalGauge)

* [Lie algebra action and Lie algebroids](#LieAlgebraActionAndLieAlgebroids)

* [BRST complex](#BRSTComplex)


$\,$

As an immediate corollary of prop. \ref{FlowAlongInfinitesimalSymmetryOfLagrangianPreservesOnShellSpaceOfFieldHistories} we have the following important observation:

+-- {: .num_prop #NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces}
###### Proposition
**(spacetime-compactly supported and [[on-shell]] non-trivial [[infinitesimal symmetries of the Lagrangian]] [[obstruction|obstruc]] the [[covariant phase space]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] over a [[Lorentzian manifold|Lorentzian]] [[spacetime]].

If there exists a single [[infinitesimal symmetry of the Lagrangian]] $v$ (def. \ref{SymmetriesAndConservedCurrents}) such that

1. it has compact spacetime support (def. \ref{SpacetimeSupport})

1. it does not vanish [[on-shell]] (eq:ProlongedShellInJetBundle) (so not a trivial one, example \ref{TrivialImplicialInfinitesimalGaugeTransformations})

then there does not exist any [[Cauchy surface]] (def. \ref{CauchySurface}) for the [[Euler-Lagrange equations|Euler-Lagrange]] [[equations of motion]] (def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}) outside the spacetime support of $v$.

=--

+-- {: .proof}
###### Proof

By prop. \ref{FlowAlongInfinitesimalSymmetryOfLagrangianPreservesOnShellSpaceOfFieldHistories}
the flow along $\hat v$ preserves the [[on-shell]] [[space of field histories]]. Now by the assumption that $\hat v$ does not vanish [[on-shell]] implies that this flow is non-trivial, hence that it does continuously change the [[field histories]] over some points of spacetime, while the assumption that it has compact spacetime support means that these changes are confined to a [[compact subset]] of [[spacetime]].

This means that there is a continuum of solutions to the [[equations of motion]] whose restriction to the [[infinitesimal neighbourhood]] of any [[codimension]]-1 suface $\Sigma_p \hookrightarrow \Sigma$ outside of this compact support coincides. Therefore this restriction map is not an [[isomorphism]] and $\Sigma_p$ not a [[Cauchy surface]] for the [[equations of motion]].

=--

Notice that there always exist spacetime-compactly supported infinitesimal symmetries that however do vanish [[on-shell]]:

+-- {: .num_example #TrivialImplicialInfinitesimalGaugeTransformations}
###### Example
**(trivial implicit [[infinitesimal gauge symmetries]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}), so that the [[Lagrangian density]]
is canonically of the form

$$
  \mathbf{L} = L \, dvol_\Sigma
$$

with [[Lagrangian function]] $L \in \Omega^{0,0}_\Sigma(E) = C^\infty(J^\infty_\Sigma(E))$ a [[smooth function]] of the [[jet bundle]] (characterized by prop. \ref{JetBundleIsLocallyProManifold}).

Then every [[evolutionary vector field]] (def. \ref{EvolutionaryVectorField}) whose [[coefficients]]
which is proportional to the [[Euler-Lagrange derivative]] (eq:EulerLagrangeEquationGeneral) of the [[Lagrangian function]] $L$

$$
  v
  \;
    \coloneqq
  \;
  \frac{\delta_{EL} L }{\delta \phi^a} \kappa^{[a b]} \, \partial_{\phi^a}
  \;\in\;
  \Gamma_E^{ev}( T_\Sigma E )
$$

by smooth coefficient functions $\kappa^{a b}$

$$
  \kappa^{[a b]} \;\in\; \Omega^{0,0}_\Sigma(E)
$$

such that

1. each $\kappa^{a b}$ has compact spacetime support (def. \ref{SpacetimeSupport})

1. $\kappa$ is skew-symmetric in its indices: $\kappa^{[a b]} = - \kappa^{[b a]}$

is an implicit infinitesimal gauge symmetry (def. \ref{ImplicitInfinitesimalGaugeSymmetry}).

This is so for a "trivial reason" namely due to that that skew symmetry:

$$
  \begin{aligned}
    \mathcal{L}_{\hat v} \mathbf{L}
    & =
    \iota_{\hat v} \delta \mathbf{L}
    \\
    &=
    \iota_{\hat v} ( \delta_{EL}\mathbf{L} - d \Theta_{BFV} )
    \\
    & =
    \iota_\epsilon \frac{\delta_{EL}L}{\delta \phi^a} \delta \phi^a + d \iota_{\hat v}\Theta_{BFV}
    \\
    & =
    \underset{= 0}{
    \underbrace{
     \left( \frac{\delta_{EL} L }{\delta \phi^a} \right)
     \left( \frac{\delta_{EL} L }{\delta \phi^b} \right)
     \kappa^{[a b]}
    }
    }
    \,
    dvol_\Sigma
    \;+\; d \iota_{\hat v} \Theta_{BFV}
    \\
    & =
    d \iota_{\hat v} \Theta_{BFV}
  \end{aligned}
$$

Here the first steps are just recalling those in the proof of [[Noether's theorem|Noether's theorem I]]
(prop. \ref{NoethersFirstTheorem}) while the last step follows with the skew-symmetry of $\kappa$.

Notice that this means that

1. the [[Noether current]] (eq:NoetherCurrent) vanishes: $J_{\hat v} = 0$;

1. the infinitesimal symmetry vanishes [[on-shell]] (eq:InclusionOfOnShellSpaceOfFieldHistories): $\hat v \vert_{\mathcal{E}} = 0$.

Therefore these implicit infinitesimal gauge symmetries
are called the _trivial infinitesimal gauge transformations_.

=--

(e.g. [Henneaux 90, section 2.5](BRST+complex#Henneaux90))

$\,$


**[[infinitesimal gauge symmetries]]**
 {#InfinitesimalGauge}

Prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces} says that  the problem is to identify the presence of spacetime-compactly supported infinitesimal symmetries that are on-shell non-trivial.

One way they may be identified is if [[infinitesimal symmetries]] appear in _linearly [[dependent type|parameterized collections]]_, where the parameter itself is an _arbitrary_ [[spacetime]]-dependent [[section]] of some [[fiber bundle]] (hence is itself like a [[field history]]), because then choosing the parameter to have [[compact support]] yields an [[infinitesimal gauge symmetry]]. In this case we speak of a _[[gauge parameter]]_ (def. \ref{GaugeParameters} below). It turns out that in most examples of [[Lagrangian field theories]] of interest, the [[infinitesimal gauge symmetries]] all come from [[gauge parameters]] this way, and often "[[gauge symmetry]]" is undertood by default to refer to this case. Therefore we now consider this case in detail.


+-- {: .num_defn #GaugeParameters}
###### Definition
**([[infinitesimal gauge symmetries]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Then a collection of _[[infinitesimal gauge symmetries]]_ of $(E,\mathbf{L})$ is

1. a [[vector bundle]] $\mathcal{G} \overset{gb}{\longrightarrow} \Sigma$ over [[spacetime]] $\Sigma$ of [[positive number|positive]] [[rank of a vector bundle|rank]], to be called a _[[gauge parameter]] bundle_;

1. a [[bundle morphism]] (def. \ref{BundlesAndFibers}) $R$ from the
   [[jet bundle]] of the  [[fiber product]] $\mathcal{G} \times_\Sigma E$ with the [[field bundle]] (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) to the [[vertical tangent bundle]] of $E$ (def. \ref{VerticalTangentBundle}):

   $$
     \array{
       J^\infty_\Sigma( \mathcal{G} \times_\Sigma E )
         && \overset{R}{\longrightarrow} &&
       T_\Sigma E
         & \overset{i}{\hookrightarrow} &
       T_\Sigma (\mathcal{G} \times_\Sigma E)
       \\
       & \searrow && \swarrow
       \\
       && E
     }
   $$

such that

1. $R$ is [[linear map|linear]] in the first argument (in the [[gauge parameter]]);

1. $i \circ R$ is an [[evolutionary vector field]] on $\mathcal{G} \times_\Sigma E$ (def. \ref{EvolutionaryVectorField});

1. $R$ is an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents}) in the second argument.

We may express this equivalently in components
in the case that the [[field bundle]] $E$ is a [[trivial vector bundle]] with [[field (physics)|field]] [[fiber]] coordinates
$(\phi^a)$ (example \ref{TrivialVectorBundleAsAFieldBundle})
and also $\mathcal{G}$ happens to be a [[trivial vector bundle]]

$$
  \mathcal{G} = \Sigma \times \mathfrak{g}
$$

where $\mathfrak{g}$ is a [[vector space]] with [[coordinate functions]] $\{c^\alpha\}$.

Then $R$ may be expanded in the form

$$
  \label{CoordinateExpressionForGaugeParameterized}
  R
  \;=\;
  \left(
    c^\alpha R^a_\alpha
    +
    c^\alpha_{,\mu} R^{a \mu}_\alpha
    +
    c^\alpha_{,\mu_1 \mu_2} R^{a \mu_1 \mu_2}_\alpha
    +
    \cdots
  \right)
  \partial_{\phi^a}
  \,,
$$

where the components

$$
  R^{a \mu_1 \cdots \mu_k}_\alpha
  =
  R^{a \mu_1 \cdots \mu_k}_\alpha\left( (\phi^b), (\phi^b_{,\mu}), \cdots \right)
  \;\in\; \Omega^{0,0}_\Sigma(E) = C^\infty(J^\infty_\Sigma(E))
$$

are [[smooth functions]] on the jet bundle of $E$,
locally of finite order (prop. \ref{JetBundleIsLocallyProManifold}), and such that the [[Lie derivative]]
of the [[Lagrangian density]] along $R(e)$ is a [[total spacetime derivative]], which by [[Noether's theorem|Noether's theorem I]] (prop. \ref{NoethersFirstTheorem}) mean in components that

$$
  \left(
    c^\alpha R^a_\alpha
    +
    c^\alpha_{,\mu} R^{a \mu}_\alpha
    +
    c^\alpha_{,\mu_1 \mu_2} R^{a \mu_1 \mu_2}_\alpha
    +
    \cdots
  \right)
  \frac{\delta_{EL} \mathbf{L}}{\delta \phi^a}
  \;=\;
  \frac{d}{d x^\mu} J^\mu_{R(e)}
  \,.
$$

=--

The point is that [[infinitesimal gauge symmetries]] in particular yield spacetime-compactly supported infinitesimal gauge symmetries:

+-- {: .num_remark #GaugeParametrizedInfinitesimalGaugeTransformation}
###### Remark
**([[infinitesimal gauge symmetries]] yield spacetime-compactly supported [[infinitesimal symmetries of the Lagrangian]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) and $\mathcal{G} \overset{gb}{\to} \Sigma$ a bundle of [[gauge parameters]] for it (def. \ref{GaugeParameters}) with gauge parametrization

$$
  J^\infty_\Sigma(\mathcal{G} \times_\Sigma E)
  \overset{R}{\longrightarrow}
  T_\Sigma E
  \,.
$$

Then for _every_ smooth [[section]] $\epsilon \in \Gamma_\Sigma(\mathcal{G})$ of the [[gauge parameter]] bundle (def. \ref{Sections})
there is an induced [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents}) given by the [[composition]] of $R$ with the [[jet prolongation]] of $\epsilon$ (def. \ref{JetProlongation})

$$
  R(\epsilon)
  \;\colon\;
  J^\infty_\Sigma(E)
    =
  \Sigma_ \times_\Sigma J^\infty_\Sigma(E)
    \overset{(j^\infty_\Sigma(eps),id)}{\longrightarrow}
  J^\infty_\Sigma(\mathcal{G} \times_\Sigma E)
    \overset{R}{\longrightarrow}
  T_\Sigma E
  \,.
$$

In the components (eq:CoordinateExpressionForGaugeParameterized) this means that

$$
  R(\epsilon)
  \;=\;
  \left(
    \epsilon^\alpha R^a_\alpha
    +
    \frac{\partial^2 \epsilon^\alpha}{\partial x^\mu} R^{a \mu}_\alpha
    +
    \frac{\partial \epsilon^\alpha}{\partial x^\mu \partial x^\nu} R^{a \mu_1 \mu_2}_\alpha
    +
    \cdots
  \right)
  \,,
$$

where now $\frac{\partial^k \epsilon^\alpha}{\partial x^{\mu_1} \cdots \partial x^{\mu_k}}((x^\mu))$  are the actual [[spacetime]] [[partial derivatives]] of the [[gauge parameter]] [[section]].

In particular, since $\mathcal{G} \overset{gb}{\to} \Sigma$ is assumed to be a [[vector bundle]], there always exists [[gauge parameter]] [[sections]] $\epsilon$ that have [[compact support]] ([[bump functions]]). For such compactly supported $\epsilon$ the infinitesimal symmetry $R(\epsilon)$ is
spacetime-compactly supported as in prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces}.

=--

The following is a way to identify [[infinitesimal gauge symmetries]]:

+-- {: .num_prop #NoetherIdentities}
###### Proposition
**([[Noether's theorem|Noether's theorem II]] -- [[Noether identities]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) and let $\mathal{G} \overset{gb}{\to} \Sigma$ be a [[vector bundle]].

The a [[bundle morphism]] of the form

$$
  J^\infty_\Sigma(\mathcal{G} \times_\Sigma E) \overset{R}{\longrightarrow} T_\Sigma E
$$

a collection of [[infinitesimal gauge symmetries]] (def. \ref{GaugeParameters}) with local components (eq:CoordinateExpressionForGaugeParameterized)

$$
  R
  \;=\;
  \left(
    c^\alpha R^a_\alpha
    +
    c^\alpha_{,\mu} R^{a \mu}_\alpha
    +
    c^\alpha_{,\mu_1 \mu_2} R^{a \mu_1 \mu_2}_\alpha
    +
    \cdots
  \right)
  \partial_{\phi^a}
$$

precisely if the [[Euler-Lagrange form]] $\delta_{EL}\mathbf{L}$ (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime})
satisfies the following condition:

$$
  \left(
    R^{a}_\alpha \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a}
    -
    R^{a \mu}_\alpha \frac{d}{d x^\mu} \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a}
    +
    R^{a \mu_1 \mu_2}_\alpha \frac{d^2}{d x^{\mu_1} d x^{\mu_2}} \frac{\delta_{EL}\mathbf{L}}{\delta \phi^a}
    -
    \cdots
  \right)
  \;=\;
  0
  \,.
$$

These relations are called the _[[Noether identities]]_ of the [[Euler-Lagrange equations|Euler-Lagrange]] [[equations of motion]] (def \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime}).

=--

+-- {: .proof}
###### Proof

By [[Noether's theorem|Noether's theorem I]],
$R$ is an [[infinitesimal symmetry of the Lagrangian]] precisely if the contraction (def. \ref{ContractionOfFormsWithVectorFields})
of $R$ with the [[Euler-Lagrange form]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime})
is horizontally exact:

$$
  \iota_{R} \delta_{EL}\mathbf{L} = d J_{\hat R}
  \,.
$$

From (eq:CoordinateExpressionForGaugeParameterized) this means that

$$
  \begin{aligned}
    d J_{\hat R}
    & =
    \iota_{R} \delta_{EL} \mathbf{L}
    \\
    & =
    \underset{k \in \mathbb{N}}{\sum}
      c^\alpha_{\mu_1 \cdots \mu_k} R^{a \mu_1 \cdots \mu_k}_\alpha
      \frac{\delta_{EL} \mathbf{L}}{\delta \phi^a}
    \\
    & =
    \underset{A}{
    \underbrace{
    c^\alpha
    \underset{k \in \mathbb{N}}{\sum}
      (-1)^k  R^{a \mu_1 \cdots \mu_k}_\alpha
      \frac{d^k}{d x^{\mu_1} \cdots d x^{\mu_k}}
      \frac{\delta_{EL} \mathbf{L}}{\delta \phi^a}
    }
    }
    +
    d (...)
    \,,
  \end{aligned}
$$

where in the last step we used jet-level [[integration by parts]] to move the [[total spacetime derivatives]] off of $c^\alpha$, thereby picking up some horizontally exact correction term, as show.

This means that the term $A$ over the brace is horizontally exact:

$$
  \label{NoetherIdentityTermIsHorizontallyExact}
  c^\alpha
   \underset{k \in \mathbb{N}}{\sum}
     (-1)^k  R^{a \mu_1 \cdots \mu_k}_\alpha
      \frac{d^k}{d x^{\mu_1} \cdots d x^{\mu_k}}
      \frac{\delta_{EL} \mathbf{L}}{\delta \phi^a}
   \;=\;
   d(...)
$$

But now the term on the left is independent of the jet coordinates $\epsilon^\alpha_{,\mu_1 \cdots \mu_k}$
of positive order $k \geq 1$, while the horizontal derivative increases the dependency on the jet order by one.
Therefore the term on the left is horizontally exact precisely if it vanishes, which is the case precisely if the coefficients of $c^\alpha$ vanish, which is the statement of the Noether identities.

Alternatively we may reach this conclusion from (eq:NoetherIdentityTermIsHorizontallyExact) by applying to both sides of (eq:NoetherIdentityTermIsHorizontallyExact) the [[Euler-Lagrange derivative]] (eq:EulerLagrangeEquationGeneral) _with respect to $c^\alpha$_. On the left this yields again the coefficients of $c^\alpha$,
while by the argument from example \ref{TrivialLagrangianDensities} it makes the right hand side vanish.

=--





$\,$




+-- {: .num_example #InfinitesimalGaugeSymmetryElectromagnetism}
###### Example
**([[infinitesimal gauge symmetry]] of [[electromagnetic field]])**

Consider the [[Lagrangian field theory]]  $(E,\mathbf{L})$ of [[free field|free]] [[electromagnetism]]
on [[Minkowski spacetime]] $\Sigma$ from example \ref{ElectromagnetismLagrangianDensity}. With field coordinates denoted $((x^\mu), (a_\mu))$ the [[Lagrangian density]] is

$$
  \mathbf{L}
  \;=\;
  \tfrac{1}{2} f_{\mu \nu} f^{\mu \nu}
  \, dvol_\Sigma
  \,,
$$

where $f_{\mu \nu} \coloneqq a_{\nu,\mu}$ is the universal [[Faraday tensor]] from example \ref{JetFaraday}.

Let $\mathcal{G} \coloneqq \Sigma \times \mathbb{R}$ be the [[trivial line bundle]], regarded as a
[[gauge parameter]] bundle (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) with coordinate functions $((x^\mu), c)$.

Then a [[gauge parameter|gauge parametrized]] [[evolutionary vector field]] (eq:CoordinateExpressionForGaugeParameterized) is given by

$$
  R
  \;=\;
  c_{,\mu} \partial_{a_\mu} 
$$

with prolongation (prop. \ref{EvolutionaryVectorFieldProlongation})

$$
  \label{EMProlongedSymmetryVectorField}
  \widehat R
  \;=\;
  c_{,\mu} \partial_{a_\mu} 
    +  
  c_{,\mu \nu} \partial_{a_{\mu,\nu}}
    + 
  \cdots
  \,.
$$

This is because already the universal [[Faraday tensor]] is [[invariant]] under this flow:

$$
  \begin{aligned}
    \mathcal{L}_R f_{\mu \nu}
    &=
    \tfrac{1}{2}
    c_{,\mu' \nu'} \partial_{a_{\mu',\nu'}}
    \left(
      a_{\nu, \mu} - a_{\mu,\nu}
    \right)
    \\
    & =
    \tfrac{1}{2}
    \left(
      c_{,\nu\mu} - c_{,\mu \nu}
    \right)
    \\
    & = 0
    \,,
  \end{aligned}
$$

because [[partial derivatives]] commute with each other: $c_{,\mu \nu} = c_{,\nu \mu}$ (eq:JetCoodinatesSymmetry).

Equivalently, the [[Euler-Lagrange form]]

$$
  \delta_{EL}\mathbf{L}
  \;=\;
  \frac{d}{d x^\mu }f^{\mu \nu} \delta a_\nu \, dvol_\Sigma
$$

of the theory (example \ref{ElectromagnetismEl}),
corresponding to the [[vacuum]] [[Maxwell equations]] (example \ref{MaxwellVacuumEquation}),
satisfies the following [[Noether identity]] (prop. \ref{NoetherIdentities}):

$$
  \frac{d}{d x^\mu} \frac{d}{d x^\nu} f^{\mu \nu} = 0
  \,,
$$

again due to the fact that partial derivatives commute with each other.

This is the archetypical _[[infinitesimal gauge symmetry]]_ that gives [[gauge theory]] its name.

=--

More generally:

+-- {: .num_example #InfinitesimalGaugeSymmetryOfYangMillsTheory}
###### Example
**([[infinitesimal gauge symmetry]] of [[Yang-Mills theory]])**

For $\mathfrak{g}$ a [[semisimple Lie algebra]], 
consider the [[Lagrangian field theory]] of [[Yang-Mills theory]] on [[Minkowski spacetime]] from example \ref{YangMillsLagrangian}, with [[Lagrangian density]]

$$
  \mathbf{L}
  \;=\;
  \tfrac{1}{2} f^\alpha_{\mu \nu} f_\alpha^{\mu \nu}
$$

given by the universal [[field strength]]

$$
  f^\alpha_{\mu \nu}
  \;\coloneqq\;
  \tfrac{1}{2}
  \left(
    a^\alpha_{[\nu,\mu]}
    +
    \tfrac{1}{2} \gamma^\alpha_{\beta \gamma} a^\beta_{[\mu} a^\gamma_{\nu]}
  \right)
  \,.
$$

Let $\mathcal{G} \coloneqq \Sigma \times \mathfrak{g}$ be the [[trivial vector bundle]] with [[fiber]] $\mathfrak{g}$, regarded as a
[[gauge parameter]] bundle (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) with coordinate functions $((x^\mu), c^\alpha)$.

Then a [[gauge parameter|gauge parametrized]] [[evolutionary vector field]] (eq:CoordinateExpressionForGaugeParameterized) is given by

$$
  R
  \;=\;
  \left(
    c^\alpha_{,\mu} 
    -
    \gamma^\alpha_{\beta \gamma} c^\beta a^\gamma_\mu 
  \right)
  \partial_{a^\alpha_\mu} 
$$

with prolongation (prop. \ref{EvolutionaryVectorFieldProlongation})

$$
  \widehat{R}
  \;=\;
  \left(
    c^\alpha_{,\mu} 
    -
    \gamma^\alpha_{\beta \gamma} c^\beta a^\gamma_\mu 
  \right)
  \partial_{a^\alpha_\mu} 
  \;+\;
  \left(
    c^\alpha_{,\mu \nu} 
    -
    \gamma^\alpha_{\beta \gamma} 
    \left(
      c^\beta_{,\nu} a^\gamma_\mu 
      + 
      c^\beta a^\gamma_{\mu,\nu}
    \right)
  \right)
  \partial_{a^\alpha_{\mu,\nu}} 
  \;+\;
  \cdots
  \,.
$$

We compute the [[derivative]] of the [[Lagrangian function]] along this vector field:

$$
  \begin{aligned}
    \widehat{R}
    \tfrac{1}{2} f^\alpha_{\mu \nu} f_\alpha^{\mu \nu}
    & =
    \left(
      R f^\alpha_{\mu \nu}
    \right)
    f_\alpha^{\mu \nu}
    \\
    & =
    \left(
      R 
      \left(
        a_{\nu,\mu}
        +
        \tfrac{1}{2}\gamma^\alpha_{\beta \gamma} a^\beta_{\mu} a^\gamma_{\nu}
      \right)
    \right)
    f_\alpha^{\mu \nu}
    \\
    & =
    \left(
      c^\alpha_{,\nu \mu}
      -
      \gamma^\alpha_{\beta \gamma} 
      \left(
        c^\beta_{,\mu} a^\gamma_\nu
        + 
        c^\beta a^\gamma_{\nu,\mu}
      \right)
      +
      \gamma^\alpha_{\beta \gamma}
      \left(  
        c^\beta_{,\mu} 
        -
        \gamma^\beta_{\beta' \gamma'} 
        c^{\beta'} a^{\gamma'}_\mu   
      \right)
      a^\gamma_{\nu}
    \right)
    f_\alpha^{\mu \nu}
    \\
    & =
    - \gamma^{\alpha}_{\beta \gamma} c^\beta
    \underset{
      = 2 f^\gamma_{\mu \nu}
    }{
    \underbrace{
      \left(
        a^\gamma_{\nu,\mu}
        +
        \gamma^\gamma_{\beta' \gamma'} 
        a^{\beta'}_\mu a^{\gamma'}_\nu
      \right)
    }
    }
    f_\alpha{}^{\mu \nu}
    \\
    &=
    2
    \gamma_{\alpha \beta \gamma}
    c^\alpha f^\beta_{\mu \nu} f^{\gamma \mu \nu}
    \\
    & = 0
    \,.
  \end{aligned}  
$$

Here in the third step we used that $c^\alpha_{,\nu \mu} = + c^\alpha_{,\mu \nu}$ (eq:JetCoodinatesSymmetry), so that its contraction with the skew-symmetric $f_\alpha^{\mu\nu}$ vanishes, and in the last step we used that for a [[semisimple Lie algebra]] $\gamma_{\alpha \beta \gamma} \coloneqq k_{\alpha \alpha'} \gamma^{\alpha'}{}_{\beta \gamma}$ is totally skew symmetric.

So the [[Lagrangian density]] of [[Yang-Mills theory]] is strictly invariant under these [[infinitesimal gauge symmetries]].

=--


$\,$


**[[Lie algebra action]] and [[Lie algebroids]]**
 {#LieAlgebraActionAndLieAlgebroids}



Making the _implicit_ [[infinitesimal gauge symmetries]] _explicit_ means
to make explicit how they _[[action|act]]_ on the fields. To this end consider
the general concept of an [[action]] of a [[Lie algebra]] by [[infinitesimal]] [[diffeomorphisms]]:


+-- {: .num_defn #InfinitesimalActionByLieAlgebra}
###### Definition
**([[action]] of [[Lie algebra]] by [[infinitesimal]] [[diffeomorphism]])**

Let $X$ be a [[smooth manifold]] or more generally a [[locally pro-manifold]] (prop. \ref{JetBundleIsLocallyProManifold}), and let $\mathfrak{g}$ be a [[Lie algebra]].

An _[[action]]_ of $\mathfrak{g}$ on $X$ by
[[infinitesimal]] [[diffeomorphisms]], is a [[homomorphism]]
of Lie algebras

$$
  \rho \;\colon \mathfrak{g} \longrightarrow ( Vect(X), [-,-] )
$$

to the smooth [[vector fields]] on $X$.

Equivalently -- to bring out the relation to
the [[gauge parameter|gauge parameterized]] implicit [[infinitesimal gauge transformations]] in def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation} -- this is a $\mathfrak{g}$-parameterized [[section]]

$$
  \array{
     \mathfrak{g} \times X && \overset{\rho}{\longrightarrow} && T X
     \\
     & {\mathllap{pr_2}}\searrow && \swarrow_{\mathrlap{p}}
     \\
     && X
  }
$$

of the [[tangent bundle]], such that for all pairs of points $e_1, e_2$ in $\mathfrak{g}$
we have

$$
  \left[\rho(e_1,-), \rho(e_2,-)\right] = \rho([e_1,e_2],-)
$$

(with the [[Lie bracket]] of [[vector fields]] on the left).

=--



+-- {: .num_defn #GaugeParametrizedInfinitesimalGaugeTransformationIrreducibleClosed}
###### Definition
**(irreducible closed [[gauge parameters]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}). Then a collection

$$
  J^\infty_\Sigma(\mathcal{G} \times_\Sigma E) \overset{R}{\to} T_\Sigma E
$$

of [[infinitesimal gauge symmetries]] (def. \ref{GaugeParameters}) is called _irreducibly closed_ if it is closed under the [[Lie bracket]] of [[evolutionary vector fields]] (prop. \ref{EvolutionaryVectorFieldLieAlgebra}) in that there is a unique morphism

$$
  [-,-]
  \;\colon\;
  J^\infty_\Sigma(\mathcal{G}) \times_\Sigma J^\infty_\Sigma(\mathcal{G})
  \longrightarrow
  J^\infty_\Sigma(\mathcal{G})
$$

such that

$$
  \left[ R(-) , R(-)\right]
  \;=\;
  R([-,-])
  \;\colon\;
  J^\infty_\Sigma(\mathcal{G})
  \times_\Sigma J^\infty_\Sigma(\mathcal{G})
  \times_\Sigma J^\infty_\Sigma(E)
  \longrightarrow
  T_\Sigma(E)
  \,,
$$

where on the left we have the Lie bracket of eolutionary vector fields from prop. \ref{EvolutionaryVectorFieldLieAlgebra}.


=--


+-- {: .num_example #ActionOfGaugeParameterizedInfinitesimalGaugeSymmetriesOnJetBundle}
###### Example
**([[action]] of irreducible closed [[gauge parameter|gauge parameterized]] implicit [[infinitesimal gauge symmetries]] on [[field (physics)|fields]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), and let
$\mathcal{G}   \overset{gb}{\to} \Sigma$ be a bundle of irreducible closed [[gauge parameters]]
for the theory (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) with
bundle morphism

$$
  \array{
    J^\infty_\Sigma( \mathcal{G} \times_\Sigma E )
    && \overset{R}{\longrightarrow} &&
    T_\Sigma E
    \\
    & \searrow && \swarrow
    \\
    && E
  }
$$

exhibiting the corresponding parameterized implicit [[infinitesimal gauge symmetries]].

By passing from these [[evolutionary vector fields]] $R(e)$ (def. \ref{EvolutionaryVectorField})
to their prolongations $\widehat{R(e)}$,  being actual vector fields on the jet bundle (prop. \ref{EvolutionaryVectorFieldProlongation}),
we obtain a bundle morphism of the form

$$
  \array{
    J^\infty_\Sigma(\mathcal{G}) \times_\Sigma J^\infty_\Sigma E
     && \overset{\widehat{R(e)}}{\longrightarrow} &&
    T_\Sigma J^\infty_\Sigma(E)
    \\
    & \searrow && \swarrow
    \\
    && J^\infty_\Sigma(E)
  }
  \,.
$$

In the case that $\mathcal{G} = \mathfrak{g} \times \Sigma$ is a [[trivial vector bundle]], with [[fiber]] $\mathfrak{g}$, then so is its [[jet bundle]]

$$
  J^\infty_\Sigma(\mathfrak{g} \times \Sigma) = \mathfrak{g}^\infty \times \Sigma
  \,,
$$

and so in this case the above becomes of the form

$$
  \array{
    \mathfrak{g}^\infty \times J^\infty_\Sigma E
     && \overset{\widehat{R(e)}}{\longrightarrow} &&
    T_\Sigma J^\infty_\Sigma(E)
    \\
    & \searrow && \swarrow
    \\
    && J^\infty_\Sigma(E)
  }
  \,.
$$

By def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation} and def. \ref{InfinitesimalActionByLieAlgebra}
this now exhibits an [[action]]

$$
  \widehat{\rho}
  \;\colon\;
  \mathfrak{g}^\infty \longrightarrow \Gamma_{J^\infty_\Sigma(E)}\left( T(J^\infty_\Sigma(E)) \right)
$$

of a [[Lie algebra]] $\mathfrak{g}^\infty$ on the [[jet bundle]]
of the [[field bundle]] by [[infinitesimal]] [[diffeomorphisms]].

=--

We have seen that the presence of non-trivial _implicit_ [[infinitesimal gauge transformations]]
(def. \ref{ImplicitInfinitesimalGaugeSymmetry}) in a [[Lagrangian field theory]] [[obstruction|obstructs]] the existence of the [[covariant phase space]] of the theory (prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces}). But these
implicit infinitesimal gauge symmetries become _explicit_ by hard-wiring into the very [[geometry]] of the types of [[field (physics)|fields]] their _[[equivalence]]_ under these symmetries: In physics this is called _[[gauge equivalence]]_.

Mathematically this means to pass to the infinitesimal [[homotopy quotient]] of the [[action]] of the gauge symmetries on the [[shell]],
represented by the [[action Lie algebroid]] (def. \ref{ActionLieAlgebroid} below).
This is called the _local [[reduced phase space]]_ of the theory.
Such "[[schreiber:Higher Structures|higher structures]]" exist in the
unification of [[differential geometry]] with [[homotopy theory]] called _[[higher differential geometry]]_.
The ("[[Chevalley-Eilenberg algebra|Chevalley-Eilenberg]]"-)[[algebra of functions]] on this "field bundle with infinitesimal gauge symmetries made explicit" is called the _[[BRST complex]]_.
In this [[cochain complex]] the formerly _implicit_ [[infinitesimal gauge symmetries]] appear _explicitly_ in the guise of [[field (physics)|field]] variables of positive (i.e. "higher") degree in a [[differential graded-commutative algebra]]. These are called _[[ghost fields]]_.


$\,$


+-- {: .num_defn #LInfinityAlgebroid}
###### Definition
**([[Lie ∞-algebroid]])**

Let $X$ be an [[infinitesimally thickened point]] and write $C^\infty(X)$ for its [[algebra of functions]].
Then  a _connected [[Lie ∞-algebroid]]_ $\mathfrak{a}$ over $X$ of [[finite type]] is a

1. a sequence $(\mathfrak{a}_k)_{ k = 1 }^\infty$ of [[free modules]] of [[finite number|finite]] [[rank]] over $C^\infty(X)$, hence a
   [[graded module]] $\mathfrak{a}_\bullet$ in degrees $k \in \mathbb{N}$; $k \geq 1$

1. a [[differential]] $d_{CE}$ that makes the [[graded-commutative algebra]] $Sym_{C^\infty(X)}(\mathfrak{a}^\ast_\bullet)$
   into a cochain [[differential graded-commutative algebra]] (hence with $d_{CE}$ of degree +1) over $\mathbb{R}$
   (not necessarily over $C^\infty(X)$), to be called the _[[Chevalley-Eilenberg algebra]]_ of $\mathfrak{a}$:

   $$
     \label{CEAlgebra}
     CE(\mathfrak{a})
      \;\coloneqq\;
     \left(
       Sym_{C^\infty(X)}(\mathfrak{a}^\ast_\bullet)
       \,,\,
       d_{CE}
     \right)
     \,.
   $$

If we allow $\mathfrak{a}_\bullet$ to also have terms in non-positive degree, then we speak of a _[[derived Lie algebroid]]_.
If $\mathfrak{a}_\bullet$ is _only_ concentrated in negative degrees, we also speak of a _[[derived manifold]]_.

With $C^\infty(X)$ canonically itself regarded as a [[dgc-algebra]], there is a canonical
dg-algebra homomorphism

$$
  CE(\mathfrak{a}) \longrightarrow C^\infty(X)
$$

which is the identity on $C^\infty(X)$ and zero on $\mathfrak{a}^\ast_{\neq 0}$.

=--


+-- {: .num_remark #dgManifolds}
###### Remark
**([[Lie algebroids]] as [[differential graded manifolds]])**

Definition \ref{LInfinityAlgebroid} of _[[derived Lie algebroids]]_ is an encoding in [[higher algebra]]
([[homological algebra]], in this case) of a situation that is usefully thought of in terms of
[[higher differential geometry]].

To see this, recall the magic algebraic properties of ordinary [[differential geometry]] (prop. \ref{AlgebraicFactsOfDifferentialGeometry})

1. [[embedding of smooth manifolds into formal duals of R-algebras]];

1. [[smooth Serre-Swan theorem|embedding of smooth vector bundles into formal duals of modules]]

Together these imply that we may think of the [[graded algebra]] underlying a [[Chevalley-Eilenberg algebra]]
as being the [[algebra of functions]] on a [[graded manifold]]

$$
  \cdots \times \mathfrak{a}_2 \times \mathfrak{a}_1 \times X \times \mathfrak{a}_{-1} \times \cdots
$$

which is [[infinitesimal]] in non-vanishing degree.

The "higher" in [[higher differential geometry]] refers to the degrees higher than zero. See at
_[[schreiber:Higher Structures]]_ for exposition.
Specifically if $\mathfrak{a}_\bullet$ has components in negative degrees,
these are also called _[[derived manifolds]]_.

=--

+-- {: .num_example #BasicExamplesOfLieAlgebroids}
###### Example
**(basic examples of [[Lie algebroids]])**

Two basic examples of [[Lie algebroids]] are:

1. For $X$ any [[smooth manifold]], then setting $\mathfrak{a}_{\neq 0 } \coloneqq 0$ and $d_{CE} \coloneqq 0$
   makes it a Lie algebroid. We will just still just write $X$ for the manifold trivially regarded
   as a Lie alebroid this way.

1. For $\mathfrak{g}$ a [[finite number|finite]] [[dimension|dimensional]] [[Lie algebra]]
   we obtain a Lie algebroid denoted $\ast/\mathfrak{g}$ or $B \mathfrak{g}$ by taking the base manifold
   to be the point, taking $\mathfrak{a}$ to be concentrated in degree 1 on $\mathfrak{g}$, and
   taking the differential to be given by the linear dual of the [[Lie bracket]]

   $$
     d_{CE} \;\colon\; \mathfrak{g}^\ast \overset{[-,-]^\ast}{\longrightarrow} \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast
     \,.
   $$

   If $(t_\alpha)$ is a [[linear basis]] for $\mathfrak{g}$ and $(t^\alpha)$ a corresponding dual basis for $\mathfrak{g}^\ast$,
   then this is given by

   $$
     d_{CE} t^\alpha -\tfrac{1}{2} C^\alpha_{\beta \gamma} t^\beta \wedge t^\gamma
     \,,
   $$

   where on the right we have the structure constants of the [[Lie bracket]] in this basis:

   $$
     [t^\beta, t^\gamma] = t_\alpha C^\alpha{}_{\beta \gamma}
     \,.
   $$

   The resulting [[dgc-algebra]]

   $$
     \left(
       \wedge^\bullet \mathfrak{g}^\ast, d_{CE} = [-,-]^\ast
     \right)
   $$

   is the standard [[Chevalley-Eilenberg algebra]] from basic [[Lie theory]], whence the name of the general concept.


=--

The two basic examples \ref{BasicExamplesOfLieAlgebroids} are unified by the concept of _[[action Lie algebroid]]_
(def. \ref{ActionLieAlgebroid} below),
which is the one of central relevance for the discussion of [[gauge theory]]: the local [[BRST complex]] (def. \ref{LocalOffShellBRSTComplex} below).





+-- {: .num_defn #ActionLieAlgebroid}
###### Definition
**([[action Lie algebroid]])**

Given an [[infinitesimal]] [[action]] of a [[Lie algebra]] $\mathfrak{g}$
on a manifold $X$ (def. \ref{InfinitesimalActionByLieAlgebra}) the _[[action Lie algebroid]]_ $X/\mathfrak{g}$
is the [[Lie algebroid]] (def. \ref{LInfinityAlgebroid}) whose underlying space is $X$;
whose $C^\infty(X)$-module is concentrated in degree 1 on the [[free module]] $C^\infty(X) \otimes_{\mathbb{R}} \mathfrak{g}$
and whose [[Chevalley-Eilenberg algebra|CE-differential]] is given

* on functions $f \in C^\infty(X)$ by the Lie algebra action

  $$
    d_{CE} f \coloneqq \rho(-)(f) \in C^\infty(X) \otimes \mathfrak{g}^\ast
  $$

* on dual Lie algebra elements $\omega \in \mathfrak{g}^\ast$ by the [[linear dual]] of the [[Lie bracket]]

  $$
    d_{CE} \omega \coloneqq \omega([-,-]) \;\in \; \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast
    \,.
  $$

In terms of [[coordinates]] this means the following. Assume that $X = \mathbb{R}^n$ is a [[Cartesian space]]
with coordinates $(\phi^a)$ and let $\{t_\alpha\}$ be a [[linear basis]] for $\mathfrak{g}$
with dual basis $(c^\alpha)$ for $\mathfrak{g}^\ast$. Then the
Lie action has components

$$
  \begin{aligned}
    d_{CE} \phi^a & = \rho^{a}_{\alpha} c^\alpha
    \\
    d_{CE} c^\alpha & = -\tfrac{1}{2} \gamma^\alpha{}_{\beta \gamma} \, c^\beta \wedge c^\gamma
  \end{aligned}
$$

where on the right we have the structure constants of the Lie algebra in this basis:

$$
  [t_\beta, t_\gamma] = \gamma^\alpha{}_{\beta \gamma} t_\alpha
  \,.
$$

That the differential $d_{CE}$ thus defined indeed squares to 0 is

* in degree 0 the action property: $\rho([t, t']) = [\rho(t), \rho(t')]$

* in degree 1 the [[Jacobi identity]].

=--


+-- {: .num_example #HorizontalTangentLieAlgebroid}
###### Example
**(horizontal [[tangent Lie algebroid]])**

Let $\Sigma$ be a [[smooth manifold]] or more generally a [[locally pro-manifold]] (prop. \ref{JetBundleIsLocallyProManifold}).
Then we write $\Sigma/T\Sigma$ for the [[Lie algebroid]] over $X$ and whose [[Chevalley-Eilenberg algebra]] is generated
over $C^\infty(X)$ in degree 1
from the [[module]]

$$
  \mathfrak{a}_1^\ast \coloneqq (\Gamma(T \Sigma))^\ast \simeq\Gamma(T^\ast \Sigma) = \Omega^1(\Sigma)
$$

of [[differential 1-forms]] and whose [[Chevalley-Eilenberg differential]] is the [[de Rham differential]],
so that the [[Chevalley-Eilenberg algebra]] is the [[de Rham dg-algebra]]

$$
  CE( \Sigma/T\Sigma ) \coloneqq (\Omega^\bullet(\Sigma), d_{dR})
  \,.
$$

This is called the _[[tangent Lie algebroid]]_ of $\Sigma$.
As a [[graded manifold]] (via remark \ref{dgManifolds}) this is called the "[[shifted tangent bundle]]" $T[1] \Sigma$ of $X$.

More generally, let $E \overset{fb}{\to} \Sigma$ be a [[fiber bundle]] over $\Sigma$. Then there is a [[Lie algebroid]]
$J^\infty_\Sigma(E)/T\Sigma$ over the [[jet bundle]] of $E$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
defined by its [[Chevalley-Eilenberg algebra]] being the [[horizontal derivative|horizontal]] part of the
[[variational bicomplex]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}):

$$
  CE\left(
    J^\infty_\Sigma(E)/T\Sigma
  \right)
  \;\coloneqq\;
  \left(\Omega^{\bullet,0}_\Sigma(E), d\right)
  \,.
$$

The underlying [[graded manifold]] of $J^\infty_\Sigma(E)/T\Sigma$ is the [[fiber product]]
$J^\infty_\Sigma(E)\times_\Sigma T[1]\Sigma$ of the [[jet bundle]] of $E$ with the [[shifted tangent bundle]]
of $\Sigma$.

There is then a canonical homomorphism of Lie algebroids (def. \ref{HomomorphismBetweenLieAlgebroids})

$$
  \array{
    J^\infty_\Sigma(E)/T\Sigma
    \\
    \downarrow
    \\
    \Sigma/T\Sigma
  }
$$

=--

$\,$

**[[local BRST complex|local]] [[off-shell]] [[BRST complex]]**
 {#BRSTComplex}


+-- {: .num_example #LocalOffShellBRSTComplex}
###### Example
**(local [[BRST complex]] and [[ghost fields]] for irreducible closed [[gauge parameters]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), and let
$\mathcal{G} \overset{gb}{\longrightarrow} \Sigma$ be a bundle of irreducible closed  [[gauge parameters]]
for the theory (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) with
bundle morphism

$$
  \array{
    J^\infty_\Sigma( \mathcal{G} \times_\Sigma E )
    && \overset{R}{\longrightarrow} &&
    T_\Sigma E
    \\
    & \searrow && \swarrow
    \\
    && E
  }
  \,.
$$

Assuming that the gauge parameter bundle is [[trivial vector bundle|trivial]], $\mathcal{G} = \mathfrak{g} \times \Sigma$,
then by example \ref{ActionOfGaugeParameterizedInfinitesimalGaugeSymmetriesOnJetBundle} this
induces an [[action]] $\hat R$
of a Lie algebra $\mathfrak{g}^\infty$ on $J^\infty_\Sigma E$ by [[infinitesimal]] [[diffeomorphisms]].

The corresponding [[action Lie algebroid]] $J^\infty_\Sigma(E)/\mathfrak{g}^\infty$
(def. \ref{ActionLieAlgebroid}) has as underlying [[graded manifold]] (remark \ref{dgManifolds})

$$
  \mathfrak{g}^\infty[1] \times J^\infty_\Sigma(E)
  \;\simeq\;
  J^\infty_\Sigma( \mathcal{G}[1] \times_\Sigma E  )
$$

the [[jet bundle]] of the _[[graded manifold|graded]] [[field bundle]]_

$$
  E_{BRST} \coloneqq \mathcal{G}[1]  \times E
$$

which regards the [[gauge parameters]] as [[field (physics)|fields]] in degree 1.
As such these are called _[[ghost fields]]_:

$$
  \left\{
    \text{ghost field histories}
  \right\}
   \;\coloneqq\;
  \Gamma_\Sigma( \mathcal{G}[1] )
  \,.
$$

Therefore we write suggestively

$$
  E/\mathcal{G}
  \;\coloneqq\;
  J^\infty_\Sigma(E)/\mathfrak{g}^\infty
$$

for the [[action Lie algebroid]] of the [[gauge parameter|gauge parameterized]] implicit [[infinitesimal gauge symmetries]]
on the [[jet bundle]] of the [[field bundle]].

The Chevalley-Eilenberg [[differential]] of the [[BRST complex]] is traditionally denoted

$$
  s_{BRST} \coloneqq d_{CE}
  \,.
$$

To express this in [[coordinates]], assume that the [[field bundle]] $E$ as well as the [[gauge parameter]]
bundle are [[trivial vector bundles]] (example \ref{TrivialVectorBundleAsAFieldBundle})
with $(\phi^a)$ the [[field (physics)|field]] coordinates on the [[fiber]] of $E$
with induced jet coordinates $((x^\mu), (\phi^a), (\phi^a_{\mu}), \cdots)$ and
$(c^\alpha)$ are [[ghost field]] coordinates on the fiber of $\mathcal{G}[1]$ with induced
jet coordinates $((x^\mu), (c^\alpha), (c^\alpha_\mu), \cdots)$.

Then in terms of the
corresponding coordinate expression for the gauge symmetries $R$ (eq:CoordinateExpressionForGaugeParameterized)
the [[BRST differential]] is given on the [[field (physics)|fields]] by

$$
  s_{BRST} \, \phi^a
  \;=\;
  \underset{k \in \mathbb{N}}{\sum}
    R^{a \mu_1 \cdots \mu_k}_{\alpha} c^\alpha_{\mu_1 \cdots \mu_k}
$$

and on the [[ghost fields]] by

$$
  s_{BRST} \, c^\alpha = \tfrac{1}{2}\gamma^\alpha{}_{\beta \gamma} c^\beta c^\gamma
  \,,
$$

and it extends from there, via prop. \ref{EvolutionaryVectorFieldProlongation},
to jets of fields and ghost fields by (anti-)commutativity with the [[total derivative|total spacetime derivative]].

Moreover, since the action of the [[infinitesimal gauge symmetries]] is by definition via
prolongations (prop. \ref{EvolutionaryVectorFieldProlongation}) of [[evolutionary vector fields]] (def. \ref{EvolutionaryVectorField}) and hence compatible with the [[total derivative|total spacetime derivative]] (eq:ProlongedEvolutionaryVectorFieldContractionAnticommutedWithHorizontalDerivative) this construction
descends to the horizontal tangent Lie algebroid $J^\infty_\Sigma(E)/T\Sigma$ (example \ref{HorizontalTangentLieAlgebroid})
to yield

$$
  E/(\mathcal{G}\times_\Sigma T \Sigma)
  \;\coloneqq\;
  \left(J^\infty_\Sigma(E)/T\Sigma\right)/\mathfrak{g}^\infty
$$

The [[Chevalley-Eilenberg differential]] on $E/(\mathcal{G}\times_\Sigma T \Sigma)$ is

$$
  d - s_{BRST}
$$

The [[Chevalley-Eilenberg algebra]] of functions on this [[differential graded manifold]] (eq:CEAlgebra)
is called the off-shell _[[local BRST complex]]_ ([Barnich-Brandt-Henneaux 94](local+BRST+cohomology#BarnichBrandtHenneaux94)).

We may pass from the [[local BRST complex]] on the [[jet bundle]] to the "global" BRST
complex by [[transgression of variational differential forms]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces}):

Write $Obs_\Sigma(E \times\Sigma \mathcal{G}[1])$ for the induced graded [[algebra of observables]] (def. \ref{LocalObservables}).
For $A \in \Omega^{p+1,\bullet}_\Sigma(E \times_\Sigma \mathcal{G}[1])$ with corresponding [[local observable]]
$\tau_\Sigma(A) \in LocObs_\Sigma(E \times_\Sigma \mathcal{G}[1])$ its BRST differential is defined by

$$
  s_{BRST} \tau_{\Sigma}(A) \;\coloneqq\; \tau_{\Sigma}(s_{BRST} A)
$$

and extended from there to $Obs_\Sigma(E \times_\Sigma \mathcal{G}[1])$ as a graded derivation.

=--

+-- {: .num_prop #LocalBRSTComplexForFreeElectromagneticFieldOnMinkowskiSpacetim}
###### Example
**([[local BRST complex]] for [[free field|free]] [[electromagnetic field]] on [[Minkowski spacetime]])**

Consider the [[Lagrangian field theory]] of [[free field|free]] [[electromagnetism]] on [[Minkowski spacetime]] (example \ref{ElectromagnetismLagrangianDensity}) with its [[gauge parameter]] bundle as in
example \ref{InfinitesimalGaugeSymmetryElectromagnetism}.

By (eq:EMProlongedSymmetryVectorField) the action of the [[BRST differential]] is the derivation

$$
  s_{BRST}
   \;=\;
  c_{,\mu} \frac{\partial}{\partial a_\mu}
  +
  c_{, \mu \nu} \frac{\partial}{\partial a_{\mu, \nu}}
  +
  \cdots
  \,.
$$

In particular the [[Lagrangian density]] is BRST-closed

$$
  \begin{aligned}
    s_{BRST} \mathbf{L}
    & =
    s_{BRST} f_{\mu \nu} f^{\mu \nu} dvol_\Sigma
    \\
    & =
    c_{,\mu \nu} f^{\mu \nu} dvol_\Sigma
    \\
    & =
    0
  \end{aligned}
$$

as is the [[Euler-Lagrange form]] (due to the symmetry $c_{,\mu \nu} = c_{,\nu \mu}$ and in contrast to the
skew-symmetry $f_{\mu \nu} = - f_{\nu \mu}$).


=--



$\,$

This concludes our discussion of [[gauge symmetries]] as such. In the [next chapter](#ReducedPhaseSpace) we discuss
the [[homotopy quotient]] of the [[covariant phase space]] by the [[gauge symmetries]], called the _[[reduced phase space]]_.

