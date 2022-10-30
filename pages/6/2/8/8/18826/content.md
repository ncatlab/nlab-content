

## Gauge symmetries
 {#GaugeSymmetries}

An [[infinitesimal gauge symmetry]] of a [[Lagrangian field theory]] (def. \ref{GaugeParameters} below) is a [[infinitesimal symmetry of the Lagrangian]] which may be freely parameterized, hence "gauged", by a _[[gauge parameter]]_. A [[Lagrangian field theory]]
exhibiting these is also called a _[[gauge theory]]_.

By choosing the [[gauge parameter]] to have [[compact support]] [[infinitesimal gauge symmetries]] in particular yield
[[infinitesimal symmetries of the Lagrangian]] with compact spacetime support.
One finds (prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces} below)
that the the existence of [[on-shell]] non-trivial symmetries of this form is an [[obstruction]] to  
the existence of the [[covariant phase space]] of the theory (prop. \ref{CovariantPhaseSpace}).


$\,$

**[[gauge symmetries]]**

| name |  meaning | def. |
|------|----------|------|
| [[infinitesimal symmetry of the Lagrangian]] |  [[evolutionary vector field]] which leaves [[invariant]] the [[Lagrangian density]] up to a [[total spacetime derivative]] | def. \ref{SymmetriesAndConservedCurrents} |
| spacetime-compactly supported [[infinitesimal symmetry of the Lagrangian]] | [[obstruction|obstructs]] existence of the [[covariant phase space]] (if non-trivial [[on-shell]]) | prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces}  |
| [[infinitesimal gauge symmetry]] | [[gauge parameter|gauge parameterized]] collection of [[infinitesimal symmetries of the Lagrangian]]; <br/> for [[compact support|compactly supported]] [[gauge parameter]] this yields spacetime-compactly supported infinitesimal symmetries |  def. \ref{GaugeParameters} |
| [[rigid infinitesimal symmetry of the Lagrangian]] | infinitesimal symmetry modulo gauge symmetry |  def. \ref{RigidInfinitesimalSymmetriesOfTheLagrangian} |
| generating set of [[gauge parameters]] | reflects all the [[Noether identities]] | remark \ref{GeneratingSetOfGaugeTransformations} |
| closed [[gauge parameters]] | [[Lie bracket]] of [[infinitesimal gauge symmetries]] closes on [[gauge parameters]] | def. \ref{GaugeParametersClosed} |

$\,$


But we  may hard-wire these [[gauge equivalences]] into the very [[geometry]] of the [[types]] of [[field (physics)|fields]]
by forming the _[[homotopy quotient]]_ of the _[[action]]_ of the [[infinitesimal gauge symmetries]] on the [[jet bundle]].
This [[homotopy quotient]] is modeled by the  _[[action Lie algebroid]]_ (def. \ref{ActionLieAlgebroid} below).
Its [[algebra of functions]] is the _[[local BRST complex]]_ of the theory (def. \ref{LocalOffShellBRSTComplex}) below.

In this construction the [[gauge parameters]] appear as [[auxiliary fields]] whose [[field bundle]]
is a _[[graded manifold|graded]]_ version of the [[gauge parameter]]-bundle. As such they are called
_[[ghost fields]]_. The ghost fields may have [[infinitesimal gauge symmetries]] themselves
which leads to [[ghost-of-ghost fields]], etc. (example \ref{LocalBRSTComplexBFieldMinkowskiSpacetime}) below.

It is these [[auxiliary fields|auxiliary]] [[ghost fields]] and [[ghost-of-ghost fields]] which will serve to remove the [[obstruction]] to the existence of the [[covariant phase space]] for [[gauge theories]], this we arrive at in _[Gauge fixing](#GaugeFixing)_, further below.


**[[gauge parameters]] and [[ghost fields]]**

| symbol | meaning |  def.  |
|--------|---------|--------|
| $\mathcal{G} \overset{gb}{\to} \Sigma$ | [[gauge parameter]] bundle | def. \ref{GaugeParameters} |
| $c^\alpha \in C^\infty(\mathcal{G})$ | [[coordinate function]] on [[gauge parameter]] bundle |   |
| $\epsilon \in \Gamma_\Sigma(\mathcal{G})$ | [[gauge parameter]] |  |
| $\mathcal{G}[1]$ | [[gauge parameter]] [[bundle]] regarded as [[graded manifold]] in degree 1 |  expl. \ref{LocalOffShellBRSTComplex}  |
| $C \in \Gamma_\Sigma(\mathcal{G}[1])$ | [[ghost field|gost]] [[field history]] |  |
| $\underset{deg = 1}{\underbrace{c^\alpha}} \in C^\infty(\mathcal{G}[1])$ | [[ghost field]] component function |  |
| $\underset{deg = 1}{\underbrace{c^\alpha_{,\mu_1 \cdots \mu_k}}} \in C^\infty(J^\infty_\Sigma(\mathcal{G}[1]))$ | [[ghost field]] [[jet]] component function |  |
| $\phantom{A}$ |   |  |
| $\overset{(2)}{\mathcal{G}} \overset{gb}{\to} \Sigma$ | [[gauge-of-gauge transformation|gauge-of-gauge parameter]] bundle | expl. \ref{LocalBRSTComplexBFieldMinkowskiSpacetime} |
| $\overset{(2)}{c}^\alpha \in C^\infty(\overset{(2)}{\mathcal{G}})$ | [[coordinate function]] on [[gauge-of-gauge transformation|gauge-of-gauge parameter]] bundle |  |
| $\overset{(2)}{\epsilon} \in \Gamma_\Sigma(\mathcal{G})$ | gauge-of-gauge parameter |  |
| $\overset{(2)}{\mathcal{G}}[2]$ | [[gauge-of-gauge transformation|gauge-of-gauge parameter]] [[bundle]] regarded as [[graded manifold]] in degree 1 |  |
| $\overset{(2)}{C} \in \Gamma_\Sigma(\mathcal{G}[1])$ | [[ghost-of-ghost field|gost-of-ghost]] [[field history]] |  |
| $\underset{deg = 2}{\underbrace{\overset{(2)}{c}{}^\alpha}} \in C^\infty(\overset{(2)}{\mathcal{G}}[2])$ | [[ghost-of-ghost field]] component function |  |
| $\underset{deg = 2}{\underbrace{{\overset{(2)}{c}}{}^\alpha_{,\mu_1 \cdots \mu_k}}} \in C^\infty(J^\infty_\Sigma(\overset{(2)}{\mathcal{G}}[2]))$ | [[ghost-of-ghost field]] [[jet]] component function |  |


The mathematical theory capturing these phenomena is the [[higher Lie theory]] of [[Lie-∞ algebroids]] (def. \ref{LInfinityAlgebroid} below).




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
**(trivial compactly-supported [[infinitesimal symmetries of the Lagrangian]])**

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

(e.g. [Henneaux 90 (3)](BRST+complex#Henneaux90))


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

+-- {: .num_remark #GeneratingSetOfGaugeTransformations}
###### Remark
**(generating set of [[gauge transformations]])**

Given a [[Lagrangian field theory]], then a choice of [[gauge parameter]] bundle $\mathcal{G} \overset{gb}{\to} \Sigma$ with gauge parameterized [[infinitesimal gauge symmetries]] $J^\infty_\Sigma(\mathcal{G} \times_\Sigma E) \overset{R}{\longrightarrow} T_\Sigma E$ (def. \ref{GaugeParameters}) is indeed a _choice_ and not uniquely fixed.

For example given any such bundle one may form the [[direct sum of vector bundles]] $\mathcal{G} \oplus_\Sigma \mathcal{G}'$ with any other [[smooth vector bundle]] $\mathcal{G}'$ over $\Sigma$, extend $R$ by zero to $\mathbb{G}'$, and thereby obtain another [[gauge parameter|gauge parameterized]] of [[infinitesimal gauge symmetries]]

$$
  J^\infty_\Sigma((\mathcal{G}' \oplus_\Sigma \mathcal{G}) \times_\Sigma E) \overset{(0,R)}{\longrightarrow} T_\Sigma E
  \,.
$$

Conversely, given any [[subbundle]] $\mathcal{G}' \hookrightarrow \mathcal{G}$, then the [[restriction]] of $R$ to $\mathcal{G}'$ is still a [[gauge parameter|gauge parameterized]] collection of [[infinitesimal gauge symmetries]].

We will see that for the purpose of removing the [[obstruction]] to the existence of the [[covariant phase space]], the gauge parameters have to capture all [[Noether identities]] (prop. \ref{NoetherIdentities}). In this case one says that the gauge parameter bundle $\mathcal{G} \overset{gb}{\to} \Sigma$ is a _generating set_.

=--

(e.g.  [Henneaux 90, section (2.8)](BRST+complex#Henneaux90))

$\,$

It is then useful to introduce the following terminology:

+-- {: .num_defn #RigidInfinitesimalSymmetriesOfTheLagrangian}
###### Definition
**([[rigid infinitesimal symmetries of the Lagrangian]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})
and let $J^\infty_\Sigma(\mathcal{G} \times_\Sigma E) \overset{R}{\longrightarrow} T_\Sigma E$
be [[infinitesimal gauge symmetries]] (def.  \ref{GaugeParameters}) whose [[gauge parameters]]
form a generating set (remark \ref{GeneratingSetOfGaugeTransformations}).

Then the [[vector space]] of _[[rigid infinitesimal symmetries of the Lagrangian]]_ is the [[quotient space]]
of the [[infinitesimal symmetries of the Lagrangian]] by the [[image]] of the [[infinitesimal gauge symmetries]]:

$$
  \left\{ \text{rigid infinitesimal symmetries} \right\}
    \;=\;
  \left\{
    \text{infinitesimal symmetries}
  \right\} \,/\,
  \left\{ \text{infinitesimal gauge symmetries}  \right\}
  \,.
$$

=--


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
    \widehat {R} f_{\mu \nu}
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

given by the universal [[field strength]] (eq:YangMillsJetFieldStrengthMinkowski)

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
  \label{OnMinkowskiInfinitesimalGaugeSymmetryForYangMills}
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

+-- {: .num_example #InfinitesimalGaugeSymmetryOfTheBField}
###### Example
**([[infinitesimal gauge symmetry]] of the [[B-field]])**

Consider the [[Lagrangian field theory]] of the [[B-field]] on [[Minkowski spacetime]] from example \ref{BFieldLagrangianDensity}, with [[field bundle]] the [[differential 2-form]]-bundle $E = \wedge^2_\Sigma T^\ast \Sigma$ with coordinates $((x^\mu), (b_{\mu \nu}))$ subject to $b_{\mu \nu} = - b_{\nu \mu}$; and with [[Lagrangian density]]

$$
  \mathbf{L}
    \;=\;
  \tfrac{1}{2}
  h_{\mu_1 \mu_2 \mu_3} h^{\mu_1 \mu_2 \mu_3} \, dvol_\Sigma
$$

for

$$
 h_{\mu_1 \mu_2 \mu_3} = b_{[\mu_1 \mu_2, \mu_3]}
$$

the universal [[B-field|B-]][[field strength]] (example \ref{BFieldJetFaraday}).


Let $\mathcal{G} \coloneqq T^\ast \Sigma$ be the [[cotangent bundle]] (def. \ref{Differential1FormsOnCartesianSpaces}), regarded as a [[gauge parameter]] bundle (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) with coordinate functions $((x^\mu), (c_\mu))$ as in example \ref{Electromagnetism}.

Then a [[gauge parameter|gauge parametrized]] [[evolutionary vector field]] (eq:CoordinateExpressionForGaugeParameterized) is given by

$$
  R
  \;=\;
  c_{\mu,\nu} \partial_{b_{\mu \nu}}
$$

with prolongation (prop. \ref{EvolutionaryVectorFieldProlongation})

$$
  \label{InfinitesimalGaugeSymmetryForBFieldOnMinkowskiSpacetime}
  \widehat R
  \;=\;
  c_{\mu,\nu} \partial_{b_{\mu \nu}}
  +
  c_{\mu,\nu \rho} \partial_{b_{\mu \nu, \rho}}
  +
  \cdots
$$


In fact this leaves the [[Lagrangian function]] [[invariant]], in direct higher analogy to example \ref{InfinitesimalGaugeSymmetryElectromagnetism}:

$$
  \begin{aligned}
    \widehat{R} \tfrac{1}{2} h_{\mu_1 \mu_2 \mu_3} h^{\mu_1 \mu_2 \mu_3}
    & =
    \left(
      \widehat{R} b_{\mu_1 \mu_2, \mu_3}
    \right)
    h^{\mu_1 \mu_2 \mu_3}
    \\
    & =
    c_{\mu_1, \mu_2 \mu_3}
    h^{\mu_1 \mu_2 \mu_3}
    \\
    & = 0
  \end{aligned}
$$

due to the symmetry of [[partial derivatives]] (eq:JetCoodinatesSymmetry).

$$
  h_{,\mu}\partial_{c_{\mu}}
  +
  h_{,\mu \nu}\partial_{c_{\mu,\nu}}
$$

$$
  R_\alpha^{a, \mu}
  =
 c_{\mu,\nu}
 R^{\mu, \nu}_{\mu' \nu'}
 \partial_{b_{\mu' \nu'}}
 \,.
$$

While so far all this is in direct analogy to the case of the [[electromagnetic field]] (example \ref{InfinitesimalGaugeSymmetryElectromagnetism}), just with [[field histories]] being [[differential 1-forms]]
now replaced by [[differential 2-forms]], a key difference is that now the [[gauge parameter|gauge parameterization]] $R$
itself has [[infinitesimal gauge symmetries]]:

Let

$$
  \label{SecondOrderGaugeParameterBundleForBFieldOnMinkowskiSpacetime}
  \array{
    \overset{(2)}{\mathcal{G}} &\coloneqq& \Sigma \times \mathbb{R}
    \\
    {}^{\overset{(2)}{gb}}\downarrow  && \downarrow^{\mathrlap{pr_1}}
    \\
    \Sigma &=&
  }
$$

be the [[trivial vector bundle|trivial]] [[real line bundle]]
with coordinates $((x^\mu), \overset{(2)}{c})$, to be regarded as second order [[infinitesimal gauge-of-gauge symmetry]], then

$$
  \overset{(2)}{R}
  \;\coloneqq\;
  \overset{(2)}{c}_{,\mu} \partial_{c_\mu}
$$

with prolongation

$$
  \label{SecondOderGaugeSymmetryOfBFieldOnMinkowski}
  \widehat{\overset{(2)}{R}}
  \;\coloneqq\;
  \overset{(2)}{c}_{,\mu} \partial_{c_\mu}
  +
  \overset{(2)}{c}_{,\mu \nu} \partial_{c_{\mu,\nu}}
  +
  \cdots
$$

has the property that

$$
  \label{NoetherIdentitySecondOrderForBFieldOnMinkowskiSpacetime}
  \begin{aligned}
    \widehat{\overset{(2)}{R}} (R)
    &=
    \overset{(2)}{c}_{,\mu \nu} \frac{\partial}{\partial c_{\mu,\nu}}
    \left(
      c_{\mu',\nu'} \partial_{b_{\mu' \nu'}}
    \right)
    \\
    & = \overset{(2)}{c}_{,\mu \nu} \partial_{b_{\mu \nu}}
    \\
    & 0
    \,.
  \end{aligned}
$$

We further discuss these _[[higher gauge transformations]]_ below.

=--


$\,$


**[[Lie algebra actions]] and [[Lie algebroids]]**
 {#LieAlgebraActionAndLieAlgebroids}

We have seen above [[infinitesimal gauge symmetries]] _implied_ by a [[Lagrangian field theory]],
exhibited by [[infinitesimal symmetries of the Lagrangian]]. In order to remove the [[obstructions]] that these
[[infinitesimal gauge symmetries]] cause for the existence of the [[covariant phase space]] (via prop. \ref{NonTrivialImplicitInfinitesimalGaugeSymmetriesPbstructExistenceOfCauchySurfaces} and remark \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) we will need (discussed below in _[Gauge fixing](#GaugeFixing)_) to make these
symmetries manifest by hard-wiring them into the geometry of the [[type]] of [[field (physics)|fields]].
Mathematically this means that we need
to take the _[[homotopy quotient]]_ of the [[jet bundle]] of the [[field bundle]] by the [[action]] of the
[[infinitesimal gauge symmetries]], which is modeled by their _[[action Lie algebroid]]_.

Here we introduce the required _[[higher Lie theory]]_ of [[Lie ∞-algebroids]] (def. \ref{LInfinityAlgebroid} below).
Further [below](#BRSTComplex) we specify this to actions by [[infinitesimal gauge symmetries]] to obtain the
_[[local BRST complex|local]] [[BRST complex]]_ of a [[Lagrangian field theory]] (def. \ref{LocalOffShellBRSTComplex}) below.


$\,$

The following discussion introduces and uses the tremendously useful fact that ([[higher Lie theory|higher]]) [[Lie theory]] may usefully
be dually expressed in terms of [[differential graded-commutative algebra]] (def. \ref{differentialgradedcommutativeSuperalgebra} below), namely in terms of "[[Chevalley-Eilenberg algebras]]".
In the [[physics]] literature, besides the [[BRST-BV formalism]], this fact underlies the [[D'Auria-Fré formulation of supergravity]] ("[[FDAs]]", see the convoluted [history of the concept](L-infinity-algebra#History)).
Mathematically the deep underlying phenomenon  is called the "[[Koszul duality]] between the [[Lie operad]]
and the [[commutative algebra operad]]", but this need not concern us here. The phenomenon is readily seen in direct
application:


Before we proceed, we make explicit a [[structure]] wich we already encountered in example \ref{DifferentialFormOnSuperCartesianSpaces}.

+-- {: .num_defn #differentialgradedcommutativeSuperalgebra}
###### Definition
**([[differential graded-commutative superalgebra]])**

A _[[differential graded-commutative superalgebra]]_ is

1. a [[cochain complex]] $A_\bullet$ of [[super vector spaces]], hence for each $n \in \mathbb{Z}$

   1 a [[super vector space]] $A_n = (A_n)_{even} \oplus (A_n)_{odd}$;

   1. a super-degree preserving [[linear map]]

      $$
        d \;\colon\; A_{n} \longrightarrow A_{n+1}
      $$

   such that

   $$
     d \circ d = 0
   $$

1, an [[associative algebra]]-[[structure]] on $A \coloneqq \underset{n \in \mathbb{Z}}{\oplus} A_n$

such that for all $a_1, a_2 \in A$ with homogenous bidegree $a_i \in (A_{n_a})_{\sigma_a}$ we have
the [[signs in supergeometry|super sign rule]]

1. $a b = (-1)^{n_a n_b} (-1)^{\sigma_a \sigma_b} \, b a$

1. $d(a b) = (d a) b + (-1)^{n_1} a (d b)$.

A [[homomorphism]] between two [[differential graded-commutative superalgebras]] is a [[linear map]] between the underlying [[super vector spaces]] which preserves both degrees, and respects the product as well as the [[differential]] $d$.

We write $dgcSAlg$ for the [[category]] of [[differential graded-commutative superalgebra]].

=--

For the [[signs in supergeometry|super sigsn rule]] appearing here see also e.g. [Castellani-D'Auria-Fr&#233; 91 (II.2.106) and (II.2.109)](signs+in+supergeometry#CastellaniDAuriaFre91), [Deligne-Freed 99, section 6](signs+in+supergeometry#DeligneFreed99).

+-- {: .num_example #deRhamAlgebraOfSuperDifferentialFormsIsDifferentialGradedCommutativeSuperalgebra}
###### Example
**([[de Rham algebra]] of [[super differential forms]] is [[differential graded-commutative superalgebra]])**

For $X$ a [[super Cartesian space]], def. \ref{SuperCartesianSpace} (or more generally a [[supermanifold]], def. \ref{SuperSmoothManifolds}) the [[de Rham algebra]] of [[super differential forms]] from def. \ref{DifferentialFormOnSuperCartesianSpaces}

$$
  (\Omega^\bull(X), d)
$$

is a [[differential graded-commutative superalgebra]] (def. \ref{differentialgradedcommutativeSuperalgebra}) with
product the [[wedge product]] of differential forms and differential the [[de Rham differential]].

We will recognize the [[formal duality|dual]] incarnation of this in [[higher Lie theory]] below in example \ref{HorizontalTangentLieAlgebroid}.


=--


+-- {: .num_prop #LieAlgebraInTermsOfChevalleyEilenbergAlgebra}
###### Proposition
**([[Lie algebra]] in terms of [[Chevalley-Eilenberg algebra]])**

Let $\mathfrak{g}$ be a [[finite dimensional vector space|finite dimensional]] [[super vector space]]
equipped with a [[super Lie algebra|super]] [[Lie bracket]] $[-,-] \colon \mathfrak{g} \otimes \mathfrak{g} \to \mathfrak{g}$.
Write $\mathfrak{g}^\ast$ for the [[dual vector space]] and $[-,-]^\ast \;\colon\; \mathfrak{g}^\ast \to \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast$ for the [[linear dual]] map of the [[Lie bracket]]. Then on the [[Grassmann algebra]] $\wedge^\bullet \mathfrak{g}^\ast$
(which is $\mathbb{Z} \times \mathbb{Z}(2$ bigraded as in def. \ref{DifferentialFormOnSuperCartesianSpaces})
the graded [[derivation]] $d_{CE}$ of degree $(1,even)$, which on $\mathfrak{g}^\ast$ is given by $[-,-]^\ast$ constitutes a [[differential]]
in that $(d_{CE})^2 = 0$. The resulting [[differential graded-commutative algebra]] is called the [[Chevalley-Eilenberg algebra]]

$$
  CE(\mathfrak{g})
  \;\coloneqq\;
  \left(
    \wedge^\bullet \mathfrak{g}^\ast
    \,,
    d_{CE} = [-,-]^\ast
  \right)
  \,.
$$

In components:


If $\{c_\alpha\}$ is a [[linear basis]] of $\mathfrak{g}$, so that the [[Lie bracket]] is given by the structure constants $(\gamma^\alpha{}_{\beta \gamma})$ as

$$
  [c_\beta, c_\gamma] = \tfrac{1}{2} \gamma^\alpha{}_{\beta \gamma} c_\gamma
$$

and if $\{c^\alpha\}$ denotes the corresponding dual basis, then $\wedge^\bullet \mathfrak{g}^\ast$ is equivalently the [[differential graded-commutative superalgebra]] (def. \ref{differentialgradedcommutativeSuperalgebra}) generated from the $c^\alpha$ in bi-degree $(1,\sigma)$, where $\sigma \in \mathbb{Z}/2$ is the super-degree of $c_\alpha$ as in def. \ref{DifferentialFormOnSuperCartesianSpaces} subject to the relation

$$
  c^\alpha \wedge c^\beta = (-1) (-1)^{\sigma_\alpha \sigma_\beta} c^\beta \wedge c^\alpha
$$

and the differential is given by

$$
  d_{CE} c^\alpha = \gamma^\alpha{}_{\beta \gamma} c^\beta \wedge c^\gamma
  \,.
$$

Notice that by degree-reasons _every_ degree +1 [[derivation]] on $\wedge^\bullet \mathfrak{g}^\ast$ is of this form,

$$
  \left\{
  \array{
    \text{derivations}
    \\
    \text{of degree}\, (1,even)
    \\
    \text{on} \, \wedge^\bullet \mathfrak{g}^\ast
  }
  \right\}
  \;\;\simeq\;\,
  \left\{
    \array{
       \text{super-skew}
       \\
       \text{bilinear maps}
       \\
       \mathfrak{g} \otimes \mathfrak{g} \overset{[-,-]}{\longrightarrow} \mathfrak{g}
    }
  \right\}
$$

The condition that $(d_{CE})^2 = 0$ is equivalently the (super-)[[Jacobi identity]] on the bracket $[-,-]$, making
it an actual (super-)[[Lie bracket]]:

$$
  \label{JacobiIdentity}
  (d_{CE})^2 = 0
  \phantom{AAA}
    \Leftrightarrow
  \phantom{AAA}
  \gamma^\alpha{}_{\beta [\gamma} \gamma^{\beta}{}_{\beta' \gamma']}
  = 0
$$

(where the square brackets on the right denote super-skew-symmetrization).

Hence not only is $CE(\mathfrak{g})$ a [[differential graded-commutative superalgebra]] (def. \ref{differentialgradedcommutativeSuperalgebra}) whenever $\mathfrak{g}$ is a [[super Lie algebra]],
but conversely [[super Lie algebra]]-[[structure]] on a [[super vector space]] $\mathfrak{g}$ is the same as
a differential of degree $(1,even)$ on the [[Grassmann algebra]] $\wedge^\bullet \mathfrak{g}^\ast$.

We may state this equivalence in a more refined form: A [[homomorphism]] $\phi \;\colon\; \mathrak{g} \longrightarrow \mathfrak{h}$
between [[super vector space]] is, by degree-reasons, the same as a graded algebra homomorphism
$\phi^\ast \;\colon\; \wedge^\bullet \mathfrak{h}^\ast \longrightarrow \wedge^\bullet \mathfrak{g}^\ast$
and it is immediate to check that $\phi$ is a [[homomorphism]] of [[super Lie algebras]] precisely if
$\phi^\ast$ is a homomorpism of differential algebras:

$$
  d_{CE(\mathfrak{g})} \circ \phi^\ast
  =
  \phi^\ast \circ d_{CE(\mathfrak{h})}
  \phantom{AAA}
  \Leftrightarrow
  \phantom{AAA}
  \phi^{\alpha_1}{}_{\beta_1} \gamma^{\beta_1}_{\mathfrak{g}}{}_{\beta_2 \beta_3}
  =
  \gamma^{\alpha_1}_{\mathfrak{h}}{}_{\alpha_2 \alpha_3} \phi^{\alpha_2}{}_{\beta_2} \phi^{\alpha_3}{}_{\beta_3}
  \,.
$$

This is a [[natural bijection]] between homomrophism of [[super Lie algebras]] and of [[differential graded-commutative superalgebras]] (def. \ref{differentialgradedcommutativeSuperalgebra})

$$
  Hom_{SuperLieAlg}( \mathfrak{g}, \mathfrak{h}  )
  \;\simeq\;
  Hom_{dgcSAlg}\left( CE(\mathfrak{h}), CE(\mathfrak{g})  \right)
  \,.
$$

Stated more [[category theory|abstractly]] this means that forming [[Chevalley-Eilenberg algebras]] is a
[[fully faithful functor]]

$$
  CE
  \;\colon\;
  SuperLieAlg^{fin}
    \overset{\phantom{AAA}}{\hookrightarrow}
  dgcSAlg^{op}
  \,.
$$

=--

Notice that prop. \ref{LieAlgebraInTermsOfChevalleyEilenbergAlgebra} establishes a [[formal dual|dual]] algebraic incarnation of ([[super Lie algebras|super-]])[[Lie algebras]] which is of analogous form as the dual algebraic characterization of ([[super Cartesian space|super-]])[[Cartesian spaces]] from prop. \ref{AlgebraicFactsOfDifferentialGeometry} and def. \ref{SuperCartesianSpace}.
In fact both these concepts unify into the concept of an [[action Lie algebroid]]:


+-- {: .num_defn #InfinitesimalActionByLieAlgebra}
###### Definition
**([[action]] of [[Lie algebra]] by [[infinitesimal]] [[diffeomorphism]])**

Let $X$ be a [[supermanifold]] (def. \ref{SuperSmoothManifolds}), for instance a [[super Cartesian space]] (def. \ref{SuperCartesianSpace}), and let $\mathfrak{g}$ be a [[finite dimensional vector space|finite dimensional]] [[super Lie algebra]] as in prop. \ref{LieAlgebraInTermsOfChevalleyEilenbergAlgebra}.

An _[[action]]_ of $\mathfrak{g}$ on $X$ by
[[infinitesimal]] [[diffeomorphisms]], is a [[homomorphism]]
of [[super Lie algebras]]

$$
  \rho \;\colon \mathfrak{g} \longrightarrow ( Vect(X), [-,-] )
$$

to the [[tangent vector fields]] on $X$ (example \ref{TangentVectorFields})

Equivalently -- to bring out the relation to
the [[gauge parameter|gauge parameterized]] [[infinitesimal gauge transformations]] in def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation} -- this is a $\mathfrak{g}$-parameterized [[section]]

$$
  \array{
     \mathfrak{g} \times X && \overset{R}{\longrightarrow} && T X
     \\
     & {\mathllap{pr_2}}\searrow && \swarrow_{\mathrlap{p}}
     \\
     && X
  }
$$

of the [[tangent bundle]], such that for all pairs of points $e_1, e_2$ in $\mathfrak{g}$
we have

$$
  \left[R(e_1,-), R(e_2,-)\right] = R([e_1,e_2],-)
$$

(with the [[Lie bracket]] of [[tangent vector fields]] on the left).

In components:

If $\{c^\alpha\}$ is a linear basis of $\mathfrak{g}^\ast$
with corresponding structure constants $(\gamma^\alpha{}_{\beta \gamma})$ (as in prop. \ref{LieAlgebraInTermsOfChevalleyEilenbergAlgebra})
and if $\{\phi^a\}$ is a [[coordinate chart]] of $X$, then $R$ is given by

$$
  R \;=\; c^\alpha R_\alpha^a \frac{\partial}{\partial \phi^a}
  \,.
$$

=--

Now the construction of the [[Chevalley-Eilenberg algebra]] of a [[super Lie algebra]] (prop. \ref{LieAlgebraInTermsOfChevalleyEilenbergAlgebra})
extends to the case where this super Lie algebra [[action|acts]] on a [[supermanifold]] (def. \ref{InfinitesimalActionByLieAlgebra}):

+-- {: .num_defn #ActionLieAlgebroid}
###### Definition
**([[action Lie algebroid]])**

Given a [[Lie algebra action]]

$$
  \mathfrak{g} \times X
    \overset{R}{\longrightarrow}
  T X
$$

of a [[finite-dimensional vector space|finite-dimensional]] [[super Lie algebra]] $\mathfrak{g}$ on a [[supermanifold]] $X$ (def. \ref{InfinitesimalActionByLieAlgebra}) we obtain a [[differential graded-commutative superalgebra]] to be denoted $CE(X/\mathfrak{g})$

1. whose underlying graded-commutative superalgebra is the [[Grassmann algebra]] of the $C^\infty(X)$-[[free module]] on $\mathfrak{g}^\ast$ over $C^\infty(X)$

   $$
     \wedge^\bullet_{C^\infty(X)} (\mathfrak{g}^\ast \otimes C^\infty(X))
     \;=\;
     \underset{
       deg = 0
     }{
     \underbrace{
       C^\infty(X)
     }}
       \oplus
     \underset{
       deg = 1
     }{
     \underbrace{
     C^\infty(X) \otimes \mathfrak{g}^\ast
     }}
       \oplus
     \underset{
       def = 2
     }{
     \underbrace{
     C^\infty(X)
       \otimes
     \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast
     }}
       \oplus
     \cdots
   $$

1. whose [[differential]] $d_{CE}$ is given

   1. on functions $f \in C^\infty(X)$ by the [[linear dual]] of the Lie algebra action

     $$
       d_{CE} f \coloneqq \rho(-)(f) \in C^\infty(X) \otimes \mathfrak{g}^\ast
     $$

   1. on dual Lie algebra elements $\omega \in \mathfrak{g}^\ast$ by the [[linear dual]] of the [[Lie bracket]]

      $$
        d_{CE} \omega \coloneqq \omega([-,-]) \;\in \; \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast
        \,.
      $$

In components:

Assume that $X = \mathbb{R}^n$ is a [[super Cartesian space]]
with [[coordinate functions]] $(\phi^a)$ and let $\{c_\alpha\}$ be a [[linear basis]] for $\mathfrak{g}$
with dual basis $(c^\alpha)$ for $\mathfrak{g}^\ast$ and structure constants $(\gamma^\alpha){}_{\beta \gamma}$ as in prop. \ref{LieAlgebraInTermsOfChevalleyEilenbergAlgebra} and
with the Lie action given in components $(R_\alpha^a)$ as in def. \ref{InfinitesimalActionByLieAlgebra}.
Then the [[differential]] is given by

$$
  \begin{aligned}
    d_{CE(X/\mathfrak{g})} c^\alpha & = \tfrac{1}{2} \gamma^\alpha{}_{\beta \gamma} \, c^\beta \wedge c^\gamma
    \\
    d_{CE(X/\mathfrak{g})} \phi^a & = R^a_\alpha c^\alpha
  \end{aligned}
$$

That this squares to zero is equivalently

* in degree 0 the [[Lie algebra action|action property]]: $\rho([t, t']) = [\rho(t), \rho(t')]$

* in degree 1 the [[Jacobi identity]] (eq:JacobiIdentity).

$$
  (d_{CE(X/\mathfrak{g})})^2 = 0
  \phantom{AAA}
  \Leftrightarrow
  \phantom{AAA}
  \array{
    \phantom{and} \, \text{Jacobi identity}
    \\
    \text{and} \, \text{action property}
  }
$$

Hence as before in prop. \ref{LieAlgebraInTermsOfChevalleyEilenbergAlgebra} the [[Lie theory|Lie theoretic]] [[structure]] is faithfully captured dually by [[differential graded-commutative superalgebra]].

We call the [[formal duality|formal dual]] of this dgc-superalgebra the _[[action Lie algebroid]]_ $X/\mathfrak{g}$ of
$\mathfrak{g}$ acting on $X$.

=--

The concept emerging by this example we may consider generally:

+-- {: .num_defn #LInfinityAlgebroid}
###### Definition
**([[super L-∞ algebra|super]]-[[Lie ∞-algebroid]])**

Let $X$ be a [[supermanifold]] (def. \ref{SuperSmoothManifolds}) (for instance a [[super Cartesian space]], def. \ref{SuperCartesianSpace}) and write $C^\infty(X)$ for its [[algebra of functions]].
Then  a _connected [[super L-∞ algebra|super]] [[Lie ∞-algebroid]]_ $\mathfrak{a}$ over $X$ of [[finite type]] is a

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

With $C^\infty(X)$ canonically itself regarded as a [[differential graded-commutative superalgebra]], there is a canonical
dg-algebra homomorphism

$$
  CE(\mathfrak{a}) \longrightarrow C^\infty(X)
$$

which is the identity on $C^\infty(X)$ and zero on $\mathfrak{a}^\ast_{\neq 0}$.

=--

(We discuss [[homomorphism]] between [[Lie ∞-algebroid]] below in def. \ref{HomomorphismBetweenLieAlgebroids}.)


+-- {: .num_remark #dgManifolds}
###### Remark
**([[Lie algebroids]] as [[differential graded manifolds]])**

Definition \ref{LInfinityAlgebroid} of _[[derived Lie algebroids]]_ is an encoding in [[higher algebra]] ([[homological algebra]], in this case) of a situation that is usefully thought of in terms of
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

1. For $X$ any [[supermanifold]] (def. \ref{SuperSmoothManifolds}), for instance a [[super Cartesian space]] (def. \ref{SuperCartesianSpace}) then setting $\mathfrak{a}_{\neq 0 } \coloneqq 0$ and $d_{CE} \coloneqq 0$ makes it a Lie algebroid in the sense of def. \ref{LInfinityAlgebroid}.

1. For $\mathfrak{g}$ a [[finite-dimensional vector space|finite-dimensional]] [[super Lie algebra]], its [[Chevalley-Eilenberg algebra]] (prop. \ref{LieAlgebraInTermsOfChevalleyEilenbergAlgebra}) $CE(\mathfrak{g})$ exhibits $\mathfrak{g}$ as a [[Lie algebroid]] in the sense of def. \ref{LInfinityAlgebroid}. We write $B\mathfrak{g}$ or $\ast/\mathfrak{g}$ for $\mathfrak{g}$ regarded as a [[Lie algebroid]] this way.

1. For $X$ and $\mathfrak{g}$ as in the previous items, and for $R \colon \mathfrak{g} \times X \to T X$ a [[Lie algebra action]] (def. \ref{InfinitesimalActionByLieAlgebra}) of $\mathfrak{g}$ on $X$, then the dgs-superalegbra $CE(X/\mathfrak{g})$ from def. \ref{ActionLieAlgebroid} defines a [[Lie algebroid]] in the sense of def. \ref{LInfinityAlgebroid}, the _[[action Lie algebroid]]_.

   In the special case that $\mathfrak{g} = 0$ this reduces to the first example, while for $X = \ast$ this reduces to the second example.

=--



Here is another basic examples of [[Lie algebroids]] that will plays a role:

+-- {: .num_example #HorizontalTangentLieAlgebroid}
###### Example
**(horizontal [[tangent Lie algebroid]])**

Let $\Sigma$ be a [[smooth manifold]] or more generally a [[supermanifold]] or more generally a [[locally pro-manifold]] (prop. \ref{JetBundleIsLocallyProManifold}).
Then we write $\Sigma/T\Sigma$ for the [[Lie algebroid]] over $X$ and whose [[Chevalley-Eilenberg algebra]] is generated
over $C^\infty(X)$ in degree 1 from the [[module]]

$$
  \mathfrak{a}_1^\ast \coloneqq (\Gamma(T \Sigma))^\ast \simeq\Gamma(T^\ast \Sigma) = \Omega^1(\Sigma)
$$

of [[differential 1-forms]] and whose [[Chevalley-Eilenberg differential]] is the [[de Rham differential]],
so that the [[Chevalley-Eilenberg algebra]] is the [[de Rham dg-algebra]] of [[super differential forms]] (example \ref{deRhamAlgebraOfSuperDifferentialFormsIsDifferentialGradedCommutativeSuperalgebra})

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

With the general concept of [[Lie algebra action]] (def. \ref{InfinitesimalActionByLieAlgebra}) and the corresponding [[action Lie algebroids]] (def. \ref{ActionLieAlgebroid}) and more general [[Lie ∞-algebroids]] in hand (def. \ref{LInfinityAlgebroid}})
we now apply this to the [[action]] of [[infinitesimal gauge symmetries]] (def. \ref{GaugeParameters}) on field histories of a [[Lagrangian field theory]], but we consider this _[[local field theory|locally]]_, namely on the [[jet bundle]]. The [[Chevalley-Eilenberg algebra]] of the resulting [[action Lie algebroid]] (def. \ref{ActionLieAlgebroid}) is known as the _[[local BRST complex|local]] [[BRST complex]]_, example \ref{LocalOffShellBRSTComplex} below.

The [[Lie algebroid]]-perspective on [[BV-BRST formalism]] has been made explicit in ([Barnich 10](BRST+complex#Barnich10)).


+-- {: .num_defn #GaugeParametersClosed}
###### Definition
**(closed [[gauge parameters]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}). Then a [[gauge parameter]] bundle $\mathcal{G} \overset{gb}{\to} \Sigma$ parameterizing [[infinitesimal gauge symmetries]] (def. \ref{GaugeParameters})

$$
  J^\infty_\Sigma(\mathcal{G} \times_\Sigma E) \overset{R}{\longrightarrow} T_\Sigma E
$$

is called _closed_ if it is closed under the [[Lie bracket]] of [[evolutionary vector fields]] (prop. \ref{EvolutionaryVectorFieldLieAlgebra}) in that there exists a morphism (not necessarily uniquely)

$$
  \label{ClosedGaugeParametersBracket}
  [-,-]_{\mathcal{G}}
  \;\colon\;
  J^\infty_\Sigma( \mathcal{G} \times_\Sigma \mathcal{G} \times_\Sigma E )
  \longrightarrow
  J^\infty_\Sigma(\mathcal{G} \times_\Sigma E)
$$

such that

$$
  \left[ R(-) , R(-)\right]
  \;=\;
  R([-,-]_{\mathcal{G}})
  \,,
$$

where on the left we have the Lie bracket of [[evolutionary vector fields]] from prop. \ref{EvolutionaryVectorFieldLieAlgebra}.

Beware that $[-,-]_{\mathcal{G}}$ may be a function of the fields, namely of the [[jet bundle]] of the [[field bundle]] $E$. Hence for closed [[gauge parameters]] $[-,-]_{\mathcal{G}}$ in general defines a [[Lie algebroid]]-structure (def. \ref{LInfinityAlgebroid}).

Notice that the collection of all [[infinitesimal symmetries of the Lagrangian]] by necessity always forms a (very large) [[Lie algebra]]. The condition of closed [[gauge parameters]] is a condition on the _choice_ of parameterization of the [[infinitesimal gauge symmetries]], see remark \ref{GeneratingSetOfGaugeTransformations}.

=--

([Henneaux 90, section 2.9](BRST+complex#Henneaux90))


Recall the general concept of a [[Lie algebra action]] from def. \ref{InfinitesimalActionByLieAlgebra}.
The following realizes this for the action of closed [[infinitesimal gauge symmetries]] on the [[jet bundle]]
of a [[Lagrangian field theory]].


+-- {: .num_example #ActionOfGaugeParameterizedInfinitesimalGaugeSymmetriesOnJetBundle}
###### Example
**([[action]] of closed [[infinitesimal gauge symmetries]] on [[field (physics)|fields]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), and let
$\mathcal{G} \overset{gb}{\to} \Sigma$ be a bundle of [[gauge parameters]] (def. \ref{GaugeParameters}) paramaterizing [[infinitesimal gauge symmetries]]

$$
  J^\infty_\Sigma(\mathcal{G} \times_\Sigma E)
  \overset{R}{\longrightarrow}
  T_\Sigma E
$$

which are closed (def. \ref{GaugeParametersClosed}), via a bracket $[-,-]_{\mathcal{G}}$.

By passing from these [[evolutionary vector fields]] $R$ (def. \ref{EvolutionaryVectorField})
to their prolongations $\widehat{R}$, being actual vector fields on the jet bundle (prop. \ref{EvolutionaryVectorFieldProlongation}),
we obtain a bundle morphism of the form

$$
  \array{
    J^\infty_\Sigma(\mathcal{G}) \times_\Sigma J^\infty_\Sigma (E)
     && \overset{\widehat{R(e)}}{\longrightarrow} &&
    T_\Sigma J^\infty_\Sigma(E)
    \\
    & \searrow && \swarrow
    \\
    && J^\infty_\Sigma(E)
  }
$$

and via the assumed bracket $[-,-]_{\mathcal{G}}$ on [[gauge parameters]] this exhibits [[Lie algebroid]] structure on $J^\infty_\Sigma(\mathcal{G}) \times_\Sigma J^\infty_\Sigma(E) \overset{pr_2}{\to} J^\infty_\Sigma(E)$.



In the case that $\mathcal{G} = \mathfrak{g} \times \Sigma$ is a [[trivial vector bundle]], with [[fiber]] $\mathfrak{g}$, then so is its [[jet bundle]]

$$
  J^\infty_\Sigma(\mathfrak{g} \times \Sigma) = \mathfrak{g}^\infty \times \Sigma
  \,.
$$

If moreover the bracket (eq:ClosedGaugeParametersBracket) on the [[infinitesimal gauge symmetries]] is independent of the fields, then this induces a [[Lie algebra]] structure on $\mathfrak{g}^\infty$ and exhibits an [[Lie algebra action]]


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

of the [[gauge parameter|gauge parameterized]] [[infinitesimal gauge symmetries]] on the [[jet bundle]] of the [[field bundle]] by [[infinitesimal]] [[diffeomorphisms]].

=--

+-- {: .num_example #LocalOffShellBRSTComplex}
###### Example
**(local [[BRST complex]] and [[ghost fields]] for closed [[infinitesimal gauge symmetries]])**

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
is called the [[off-shell]] _[[local BRST complex]]_.

=--

([Barnich-Brandt-Henneaux 94](local+BRST+cohomology#BarnichBrandtHenneaux94), [Barnich 10 (35)](BRST+complex#Barnich10)).


+-- {: .num_defn}
###### Definition
**(global [[BRST complex]])**

We may pass from the [[off-shell]] [[local BRST complex]] (def. \ref{LocalOffShellBRSTComplex}) on the [[jet bundle]] to the "global" BRST
complex by [[transgression of variational differential forms]] (def. \ref{TransgressionOfVariationalDifferentialFormsToConfigrationSpaces}):

Write $Obs(E \times_\Sigma \mathcal{G}[1])$ for the induced graded [[off-shell]] [[algebra of observables]] (def. \ref{LocalObservables}).
For $A \in \Omega^{p+1,\bullet}_\Sigma(E \times_\Sigma \mathcal{G}[1])$ with corresponding [[local observable]]
$\tau_\Sigma(A) \in LocObs_\Sigma(E \times_\Sigma \mathcal{G}[1])$ its BRST differential is defined by

$$
  s_{BRST} \tau_{\Sigma}(A) \;\coloneqq\; \tau_{\Sigma}(s_{BRST} A)
$$

and extended from there to $Obs(E \times_\Sigma \mathcal{G}[1])$ as a graded derivation.

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

as is the [[Euler-Lagrange form]] (due to the symmetry $c_{,\mu \nu} = c_{,\nu \mu}$ (eq:JetCoodinatesSymmetry) and in contrast to the
skew-symmetry $f_{\mu \nu} = - f_{\nu \mu}$).

=--

+-- {: .num_example #YangMillsLocalBRSTComplex}
###### Example
**([[local BRST complex]] for the [[Yang-Mills field]] on [[Minkowski spacetime]])**

For $\mathfrak{g}$ a [[semisimple Lie algebra]], consider the [[Lagrangian field theory]] of [[Yang-Mills theory]] on [[Minkowski spacetime]] from example \ref{YangMillsLagrangian}, with [[Lagrangian density]]

$$
  \mathbf{L}
  \;=\;
  \tfrac{1}{2} f^\alpha_{\mu \nu} f_\alpha^{\mu \nu}
$$

given by the universal [[field strength]] (eq:YangMillsJetFieldStrengthMinkowski)

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
[[gauge parameter]] bundle (def. \ref{GaugeParametrizedInfinitesimalGaugeTransformation}) with coordinate functions $((x^\mu), c^\alpha)$ and consider the [[gauge parameter|gauge parametrized]] [[evolutionary vector field]] (eq:CoordinateExpressionForGaugeParameterized)

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

from example \ref{InfinitesimalGaugeSymmetryOfYangMillsTheory}.

We claim that these are _closed [[gauge parameters]]_ in the sense of def. \ref{GaugeParametersClosed}, hence that the [[local BRST complex]] in the form of example \ref{LocalOffShellBRSTComplex} exists.

To see this, observe that, by def. \ref{ActionLieAlgebroid} the candidate BRST differential needs to be of the form (eq:OnMinkowskiInfinitesimalGaugeSymmetryForYangMills) plus the [[linear dual]] of the [[Lie bracket]] $[-,-]_{\mathcal{G}}^\ast$

$$
  s_{BRST}
  \;=\;
   \left(
  \left(
    c^\alpha_{,\mu}
    -
    \gamma^\alpha_{\beta \gamma} c^\beta a^\gamma_\mu
  \right)
  \partial_{a^\alpha_\mu}
  \;+\;
  \text{prolongation}
  \right)
  +
  ([-,-]_{\mathcal{G}})^\ast
  \,.
$$

Moreover, by def. \ref{ActionLieAlgebroid} we may equivalently make an Ansatz for $([-,-]_{\mathcal{G}})^\ast$ and if the resulting differential $s_{BRST}$ squares to zero, as this dually defines the required closure bracket $[-,-]_\mathcal{G}$.

We claim that

$$
  \label{OffShellYangMillsOnMinkowskiBRSTOperator}
  s_{BRST}
  \;\coloneqq\;
  \widehat{
    \left(
      c^\alpha_{,\mu}
      -
      \gamma^\alpha_{\beta \gamma} c^\beta a^\gamma_\mu
    \right)
    \frac{\partial}{\partial a^\alpha_\mu}
   }
    +
   \widehat{
    \tfrac{1}{2}\gamma^\alpha{}_{\beta \gamma} \, c^\beta c^\gamma
    \frac{\partial}{\partial c^\alpha}
   }
  \,,
$$

where the hat denotes prolongation (prop. \ref{EvolutionaryVectorFieldProlongation}). This is the [[local BRST complex|local]] ([[jet bundle]]) [[BRST differential]] for [[Yang-Mills theory]] on [[Minkowski spacetime]].

=--


+-- {: .proof}
###### Proof

We need to show that (eq:OffShellYangMillsOnMinkowskiBRSTOperator) squares to zero. Consider the two terms that appear:

$$
  (s_{BRST})^2
  =
  \left[
    \widehat{
    \left(
     c^\alpha_{,\mu}
     -
     \gamma^\alpha_{\beta \gamma} c^\beta a^\gamma_\mu
    \right)
    \partial_{a^\alpha_\mu}
    }
    \;,\;
    \widehat{
    \left(
     c^{\alpha'}_{,\mu}
     -
     \gamma^{\alpha'}_{\beta \gamma} c^\beta a^\gamma_\mu
    \right)
    \partial_{a^{\alpha'}_\mu}
    }
  \right]
  \;+\;
  2
  \left[
    \widehat{
    \left(
     c^\alpha_{,\mu}
     -
     \gamma^\alpha_{\beta \gamma} c^\beta a^\gamma_\mu
    \right)
    \partial_{a^\alpha_\mu}
    }
    \;,\;
    \widehat{
    \tfrac{1}{2}\gamma^\alpha{}_{\beta \gamma}
    \,
    c^\beta c^\gamma \frac{\partial}{\partial c^\alpha}
    }
  \right]
  \,.
$$

The first term is

$$
  \begin{aligned}
  \left[
    \widehat{
    \left(
     c^\alpha_{,\mu}
     -
     \gamma^\alpha_{\beta \gamma} c^\beta a^\gamma_\mu
    \right)
    \partial_{a^\alpha_\mu}
    }
    \;,\;
    \widehat{
    \left(
     c^{\alpha'}_{,\mu}
     -
     \gamma^{\alpha'}_{\beta \gamma} c^\beta a^\gamma_\mu
    \right)
    \partial_{a^{\alpha'}_\mu}
    }
  \right]
  & =
    -
    2
    \gamma^{\alpha'}_{\beta \gamma}
    \widehat{
    c^\beta
    \left(
      c^\gamma_{,\mu}
      -
      \gamma^\gamma_{\beta' \gamma'} c^{\beta'} a^{\gamma'}_\mu
     \right)
    \frac{\partial}{\partial a^{\alpha'}_\mu}
    }
    \\
    & =
    -
    2
    \gamma^{\alpha'}_{\beta \gamma}
    \widehat{
    c^\beta
      c^\gamma_{,\mu}
    \frac{\partial}{\partial a^{\alpha'}_\mu}
     }
     +
     2
     \gamma^{\alpha'}_{\beta \gamma}
     \gamma^\gamma_{\beta' \gamma'}
     \widehat{
     c^\beta c^{\beta'} a^{\gamma'}_\mu
     \frac{\partial}{\partial a^{\alpha'}_\mu}
     }
     \\
    & =
    -
    2
    \gamma^{\alpha'}_{\beta \gamma}
    \widehat{
      c^\beta
      c^\gamma_{,\mu}
      \frac{\partial}{\partial a^{\alpha'}_\mu}
     }
     +
     \gamma^{\alpha'}_{\beta \gamma}
     \gamma^\gamma_{\beta' \gamma'}
     \widehat{
     \left(
       c^\beta c^{\beta'} a^{\gamma'}_\mu
       -
       c^{\beta'} c^{\beta} a^{\gamma'}_\mu
     \right)
     \frac{\partial}{\partial a^{\alpha'}_\mu}
     }
     \\
    & =
    -
    2
    \gamma^{\alpha'}_{\beta \gamma}
    \widehat{
      c^\beta
      c^\gamma_{,\mu}
      \frac{\partial}{\partial a^{\alpha'}_\mu}
     }
     +
     \gamma^{\alpha'}_{\beta \gamma}
     \gamma^\gamma_{\beta' \gamma'}
     \widehat{
     \left(
       -
       c^\beta c^{\gamma'} a^{\beta'}_\mu
       -
       c^{\beta'} c^{\beta} a^{\gamma'}_\mu
     \right)
     \frac{\partial}{\partial a^{\alpha'}_\mu}
     }
     \\
     & =
    -
    2
    \gamma^{\alpha'}_{\beta \gamma}
    \widehat{
      c^\beta
      c^\gamma_{,\mu}
     \frac{\partial}{\partial a^{\alpha'}_\mu}
     }
      +
     \gamma^{\alpha'}_{\beta \gamma}
     \gamma^\gamma_{\beta' \gamma'}
     \widehat{
       c^{\gamma'} c^{\beta'} a^{\beta}_\mu
      \frac{\partial}{\partial a^{\alpha'}_\mu}
     }
     \\
     & =
    -
    2
    \gamma^{\alpha'}_{\beta \gamma}
    \widehat{
      c^\beta
      c^\gamma_{,\mu}
      \frac{\partial}{\partial a^{\alpha'}_\mu}
     }
      +
     \gamma^{\alpha'}_{\gamma \beta}
     \gamma^\beta_{\beta' \gamma'}
     \widehat{
       c^{\beta'} c^{\gamma'} a^{\gamma}_\mu
      \frac{\partial}{\partial a^{\alpha'}_\mu}
     }
  \end{aligned}
$$

Here first we expanded out, then in the second-but-last line we used the [[Jacobi identity]] (eq:JacobiIdentity) and in the last line we just re-adjusted indices, just for convenience of comparison with the next term. That next term is

$$
  \left[
    \widehat{
    \left(
     c^\alpha_{,\mu}
     -
     \gamma^\alpha_{\beta \gamma} c^\beta a^\gamma_\mu
    \right)
    \partial_{a^\alpha_\mu}
    }
    \;,\;
    \gamma^\alpha{}_{\beta \gamma}
    \,
    \widehat{c^\beta c^\gamma \frac{\partial}{\partial c^\alpha}}
  \right]
  =
  2
  \gamma^\alpha_{\beta \gamma}
  \widehat{
    c^\beta_{,\mu} c^\gamma
    \frac{\partial}{\partial a^\alpha_\mu}
  }
  -
  \gamma^\alpha_{\beta \gamma}
  \gamma^\beta_{\beta' \gamma'}
  \widehat{
    c^{\beta'} c^{\gamma'}
    a^\gamma_\mu
    \frac{\partial}{\partial a^\alpha_\mu}
  }
  \,,
$$

where the first term on the right comes from the prolongation.

This shows that the two terms cancel.

=--



+-- {: .num_example #LocalBRSTComplexBFieldMinkowskiSpacetime}
###### Example
**([[local BRST complex]] for [[B-field]] on [[Minkowski spacetime]])**

Consider the [[Lagrangian field theory]] of the [[B-field]] on [[Minkowski spacetime]] from example \ref{BFieldLagrangianDensity}, with [[field bundle]] the [[differential 2-form]]-bundle $E = \wedge^2_\Sigma T^\ast \Sigma$ with coordinates $((x^\mu), (b_{\mu \nu}))$ subject to $b_{\mu \nu} = - b_{\nu \mu}$; and with [[Lagrangian density]].

By example \ref{InfinitesimalGaugeSymmetryOfTheBField} the [[local BRST complex]] (example \ref{example}) has BRST differential of the form

$$
  c_{\mu, \nu} \frac{\partial}{\partial b_{\mu \nu}}
  +
  c_{\mu,\nu_1 \nu_2} \frac{\partial}{\partial b_{\mu \nu_1, \nu_2}}
  +
  \cdots
  \,.
$$

In this case this enhanced to an [[L-infinity algebroid|Lie 2-algebroid]] by regarding the second-order [[gauge parameters]] (eq:SecondOrderGaugeParameterBundleForBFieldOnMinkowskiSpacetime) in degree 2 to form a [[graded manifold|graded]] [[field bundle]]

$$
  \underset{ \{\overset{(2)}{c}\} }{
  \underbrace{
    \overset{(2)}{\mathcal{G}}[2]
  }}
    \times_\Sigma
  \underset{\{c_\mu\}}{
  \underbrace{
    \mathcal{G}[1]
  }
  }
    \times_\Sigma
  \underset{
    (b_{\mu \nu})
  }{
  \underbrace{
    E
  }}
  \;=\;
  \mathbb{R}[2] \times T^\ast \Sigma [1] \times_\Sigma E
$$

by adding the [[ghost-of-ghost field]] $(\overset{(2)}{c})$ (eq:SecondOderGaugeSymmetryOfBFieldOnMinkowski) and taking the local BRST differential to be the sum of the first order [[infinitesimal gauge symmetries]] (eq:InfinitesimalGaugeSymmetryForBFieldOnMinkowskiSpacetime) and the second order [[infinitesimal gauge-of-gauge symmetry]] (eq:SecondOderGaugeSymmetryOfBFieldOnMinkowski)

$$
  s_{BRST}
  \;=\;
  \left(
  c_{\mu, \nu} \frac{\partial}{\partial b_{\mu \nu}}
  +
  c_{\mu,\nu_1 \nu_2} \frac{\partial}{\partial b_{\mu \nu_1, \nu_2}}
  +
  \cdots
  \right)
  +
  \left(
    \overset{(2)}{c}_{,\mu} \frac{\partial}{\partial c_\mu}
    +
    \overset{(2)}{c}_{,\mu \nu} \frac{\partial}{\partial c_{\mu,\nu}}
    +
    \cdots
  \right)
  \,.
$$

Notice that this indeed still squares to zero, due to the second-order [[Noether identity]] (eq:NoetherIdentitySecondOrderForBFieldOnMinkowskiSpacetime):

$$
  \begin{aligned}
    \left( s_{BSRT} \right)^2
    & =
    \left[
       \overset{(2)}{c}_{,\mu \nu} \frac{\partial}{\partial c_{\mu,\nu}},
         c_{\mu, \nu} \frac{\partial}{\partial b_{\mu \nu}}
    \right]
    \;+\;
    \left[
       \overset{(2)}{c}_{,\mu \nu_1 \nu_2} \frac{\partial}{\partial c_{\mu,\nu_1 \nu_2}},
         c_{\mu, \nu_1 \nu_2} \frac{\partial}{\partial b_{\mu \nu_1, \nu_2}}
    \right]
    \\
    & =
    \underset{ = 0 }{
    \underbrace{
      \overset{(2)}{c}_{,\mu \nu} \frac{\partial}{\partial b_{\mu \nu}}
    }}
    \;+\;
    \underset{ = 0 }{
    \underbrace{
    \overset{(2)}{c}_{,\mu \nu_1 \nu_2} \frac{\partial}{\partial b_{\mu \nu_1, \nu_2}}
    }}
    \;+\;
    \cdots
    \\
    & = 0
  \end{aligned}
$$

and thus it clearly cancels the first term.

=--


$\,$

This concludes our discussion of [[infinitesimal gauge symmetries]], their [[off-shell]] [[action]] on the [[jet bundle]] of the [[field bundle]] and the corresponding [[homotopy quaotient]] exhibited by the [[local BRST complex]]. In the [next chapter](#ReducedPhaseSpace) we discuss the [[homotopy intersection]] of this construction with the [[shell]]: the _[[reduced phase space]]_.
