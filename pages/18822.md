
## Symmetries
 {#Symmetries}

We have introduced the concept of _[[Lagrangian field theories]]_ $(E,\mathbf{L})$ in terms of a [[field bundle]] $E$ equipped with a
[[Lagrangian density]] $\mathbf{L}$ on its [[jet bundle]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).
Generally, given any [[object]] equipped with some [[structure]], it is of paramount interest to determine
the [[symmetries]], hence the [[isomorphisms]]/[[equivalences]] of the object that preserve the given [[structure]]
(this is the "[[Erlanger program]]", [Klein 1872](Erlangen+program#Klein1872)).

The [[infinitesimal symmetries of the Lagrangian density]] (def. \ref{SymmetriesAndConservedCurrents} below)
send one [[field history]] to an [[infinitesimal|infinitesimally]] nearby one which is
"[[equivalence|equivalent]]" for all purposes of [[field theory]]. Among these are the _[[infinitesimal gauge symmetries]]_
which will be of concern [below](#GaugeSymmetries).
A central theorem of [[variational calculus]] says that [[infinitesimal symmetries of the Lagrangian]]
correspond to _[[conserved currents]]_, this is [[Noether theorem|Noether's theorem I]], prop. \ref{NoethersFirstTheorem} below.
These conserved currents constitute an [[Lie algebra extension|extension]] of the [[Lie algebra]]
of symmetries, called the _[[Dickey bracket]]_.

But in (eq:DerivativeOfLepageForm) we have seen that the [[Lagrangian density]]
of a [[Lagrangian field theory]] is just one component, in [[codimension]] 0, of an inhomogeneous
"[[Lepage form]]" which in [[codimension]] 1 is given by the [[presymplectic potential current]] $\Theta_{BFV}$ (eq:PresymplecticPotential).
(This will be conceptually elucidated, after we have introduced the [[local BV-complex]], in example \ref{DerivedPresymplecticCurrentOfRealScalarField} below.) This means that in [[codimension]] 1 we are to
consider infinitesimal [[on-shell]] symmetries of the [[Lepage form]] $\mathbf{L} + \Theta_{BFV}$. These are
known as _[[Hamiltonian vector fields]]_ (def. \ref{HamiltonianForms} below) and the analog of [[Noether's theorem|Noether's theorem I]]
now says that these correspond to _[[Hamiltonian differential forms]]_. The [[Lie algebra]] of these
infinitesimal symmetries is called the _[[Poisson bracket Lie n-algebra|local Poisson bracket]]_ (prop. \ref{LocalPoissonBracket} below).



**[[Noether theorem]] and [[Hamiltonian Noether theorem]]**

| $\,$ [[variational differential forms|variational form]] $\,$  |   $\,$ [[symmetry]] $\,$ | $\,$ [[Cartan's homotopy formula|homotopy formula]] $\,$ | $\,$ physical quantity $\,\,\,$ | $\,$ [[Lie n-algebra|local symmetry algebra]] $\,$ |
|----|----------|----------------------------|---------------------------------|------|
| [[Lagrangian density]] $\mathbf{L}$ <br/> (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) | $\mathcal{L}_v \mathbf{L} = d \tilde J$  | $ d(\underset{= J_v}{\underbrace{\tilde J - \iota_v \Theta_{BFV}}}) = \iota_v \, \delta_{EL}\mathbf{L}$ | [[conserved current]] $J_v$ <br/> (def. \ref{SymmetriesAndConservedCurrents}) | [[Dickey bracket]] |
| [[presymplectic current]] $\Omega_{BFV}$ <br/> (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime})  | $\mathcal{L}^{var}_v \Theta_{BFV} = \delta \tilde H$ | $\delta(\underset{= H_v}{\underbrace{\tilde H_v - \iota_v \Theta_{BFV}}}) = \iota_v \Omega_{BFV}$ | [[Hamiltonian differential form|Hamiltonian form]] $H_v$ <br/> (def. \ref{HamiltonianForms}) | [[Poisson bracket Lie n-algebra|local Poisson bracket]] <br/> (prop. \ref{LocalPoissonBracket}) |

$\,$

In _[Phase space](#PhaseSpace)_ below we [[transgression|transgress]] this [[Poisson bracket Lie n-algebra|local Poisson bracket]]
of [[infinitesimal symmetries]] of the [[presymplectic potential current]] to the "global" [[Poisson bracket]] on the _[[covariant phase space]]_ (def. \ref{PoissonBracketOnHamiltonianLocalObservables} below). This is the structure which then [further below](#Quantization) leads over to the
[[quantization]] ([[deformation quantization]]) of the [[prequantum field theory]] to a genuine [[perturbative quantum field theory]].
However, it will turn out that there may be an [[obstruction]] to this construction, namely the existence of
special infinitesimal symmetries of the Lagrangian densities, called _implicit [[gauge symmetries]]_ (discussed [further below](#GaugeSymmetries)).

$\,$

We now discuss these topics:

$\,$

* _[Infinitesimal symmetries of the Lagrangian density](#InfinitesimalSymmetriesOfTheLagrangianDensity)_

* _[Infinitesimal symmetries of the presymplectic potential current](#InfinitesimalSymmetriesOfThePresymplecticPotentialCurrent)_

$\,$

**[[infinitesimal symmetries]] of the [[Lagrangian density]]**
 {#InfinitesimalSymmetriesOfTheLagrangianDensity}

+-- {: .num_defn #Variation}
###### Definition
**(variation)**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] (def. \ref{FieldsAndFieldBundles}).

A _variation_ is a [[vertical vector field]] $v$ on the [[jet bundle]] $J^\infty_\Sigma(E)$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) hence a vector field which
vanishes when evaluated in the [[horizontal differential forms]].

In the special case that the [[field bundle]] is [[trivial vector bundle]] over [[Minkowski spacetime]] as in example \ref{TrivialVectorBundleAsAFieldBundle},
a variation is of the form

$$
  v = v^a \partial_{\phi^a} + v^a_{,\mu} \partial_{\phi^a_{,\mu}} + v^a_{\mu_1 \mu_2} \partial_{\phi^a_{\mu_1 \mu_2}} + \cdots
$$

=--

The concept of variation in def. \ref{Variation} is very general, in that it allows to vary the
field coordinates independently from the corresponding jets. This generality is necessary for
discussion of symmetries of [[presymplectic currents]] in def. \ref{HamiltonianForms} below.
But for discussion of symmetries of [[Lagrangian densities]] we are interested in
explicitly varying just the [[field (physics)|field]] coordinates (def. \ref{EvolutionaryVectorField} below)
and inducing from this the corresponding variations of the field derivatives (prop. \ref{EvolutionaryVectorFieldProlongation}) below.

In order to motivate the following definition \ref{EvolutionaryVectorField}
of _[[evolutionary vector fields]]_ we follow remark \ref{ReplacingBundleMorphismsByDifferentialOperators}
saying that concepts in [[variational calculus]] are obtained from their analogous concepts
in plain [[differential calculus]] by replacing plain [[bundle morphisms]] by morphism out of
the [[jet bundle]]:

Given a [[fiber bundle]] $E \overset{fb}{\to} \Sigma$, then a _[[vertical vector field]]_ on $E$ is
a [[section]] of its [[vertical tangent bundle]] $T_\Sigma E$ (def. \ref{VerticalTangentBundle}), hence is a [[bundle morphism]]
of this form

$$
  \array{
    E && \overset{\text{vertical vector field}}{\longrightarrow} && T_\Sigma E
    \\
    & {}_{\mathllap{id}}\searrow && \swarrow
    \\
    && E
  }
$$

The variational version replaces the vector bundle on the left with its jet bundle:


+-- {: .num_defn #EvolutionaryVectorField}
###### Definition
**([[evolutionary vector fields]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] (def. \ref{FieldsAndFieldBundles}). Then an _[[evolutionary vector field]]_ $v$ on $E$ is  "variational vertical vector field" on $E$, hence a smooth [[bundle]] [[homomorphism]]
out of the [[jet bundle]] (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime})



$$
  \array{
    J^\infty_\Sigma E
    && \overset{v}{\longrightarrow} &&
    T_\Sigma E
    \\
    & {}_{\mathllap{jb_{\infty,0}}}\searrow && \swarrow_{\mathllap{}}
    \\
    && E
  }
$$

to the [[vertical tangent bundle]] $T_\Sigma E \overset{}{\to} \Sigma$ (def. \ref{VerticalTangentBundle}) of $E \overset{fb}{\to} \Sigma$.

In the special case that the [[field bundle]] is a [[trivial vector bundle]] over [[Minkowski spacetime]] as in example \ref{TrivialVectorBundleAsAFieldBundle}, this means that an evolutionary vector field is
a [[tangent vector field]] (example \ref{TangentVectorFields}) on $J^\infty_\Sigma(E)$ of the special form

$$
  \begin{aligned}
    v
     & =
    v^a \partial_{\phi^a}
    \\
    & =
    v^a\left(
      (x^\mu), (\phi^a), (\phi^a_{,\mu}), \cdots
    \right) \partial_{\phi^a}
  \end{aligned}
  \,,
$$

where the [[coefficients]] $v^a \in C^\infty(J^\infty_\Sigma(E))$ are general [[smooth functions]]
on the [[jet bundle]] (while the cmponents are [[tangent vectors]] along the field coordinates $(\phi^a)$,
but not along the spacetime coordinates $(x^\mu)$ and not along the jet coordinates $\phi^a_{,\mu_1 \cdots \mu_k}$).

We write

$$
  \Gamma_E^{ev}\left( T_\Sigma E \right)
  \;\in\;
  \Omega^{0,0}_\Sigma(E) Mod
$$

for the space of evolutionary vector fields,
regarded as a [[module]] over the $\mathbb{R}$-[[associative algebra|algebra]]

$$
  \Omega^{0,0}_\Sigma(E)
  \;=\;
  C^\infty\left( J^\infty_\Sigma(E) \right)
$$

of [[smooth functions]] on the [[jet bundle]].


=--

An [[evolutionary vector field]] (def. \ref{EvolutionaryVectorField}) describes
an infinitesimal change of field values _depending_ on, possibly, the point in spacetime and the values of the field
and all its derivatives (locally to finite order, by prop. \ref{JetBundleIsLocallyProManifold}).

This induces a corresponding infinitesimal change of the derivatives of the fields, called the _prolongation_
of the evolutionary vector field:


+-- {: .num_prop #EvolutionaryVectorFieldProlongation}
###### Proposition
**(prolongation of [[evolutionary vector field]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[fiber bundle]].

Given an [[evolutionary vector field]] $v$ on $E$ (def. \ref{EvolutionaryVectorField})
there is a unique [[tangent vector field]] $\hat v$ (example \ref{TangentVectorFields}) on the [[jet bundle]] $J^\infty_\Sigma(E)$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) such that

1. $\hat v$ agrees on field coordinates (as opposed to jet coordinates) with $v$:

   $$
     (jb_{\infty,0})_\ast(\hat v) = v
     \,,
   $$

   which means in the special case that $E \overset{fb}{\to} \Sigma$ is a [[trivial vector bundle]] over [[Minkowski spacetime]]
   (example \ref{TrivialVectorBundleAsAFieldBundle})
   that $\hat v$ is of the form

   $$
     \label{GenericComponentsForProlongationOfEvolutionaryVectorField}
     \hat v
     \;=\;
     \underset{
       = v
     }{
     \underbrace{
     v^a \partial_{\phi^a}
     }}
     \,+\,
     \hat v^a_{\mu} \partial_{\phi^a_{,\mu}}
     +
     \hat v^a_{\mu_1 \mu_2} \partial_{\phi^a_{,\mu_1 \mu_2}}
     +
     \cdots
   $$

1. contraction with $\hat v$ (def. \ref{ContractionOfFormsWithVectorFields}) anti-commutes with the [[total derivative|total spacetime derivative]] (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}):

   $$
     \label{ProlongedEvolutionaryVectorFieldContractionAnticommutedWithHorizontalDerivative}
     \iota_{\hat v} \circ d + d \circ \iota_{\hat v} = 0
     \,.
   $$

In particular [[Cartan's homotopy formula]] (prop. \ref{CartanHomotopyFormula})
for the [[Lie derivative]] $\mathcal{L}_{\hat v}$ holds with respect to the [[variational derivative]] $\delta$:

$$
 \label{HomotopyFormulaForLieDerivativeAlongProlongationOfEvolutionaryVectorField}
  \mathcal{L}_{\hat v} = \delta \circ \iota_{\hat v} + \iota_{\hat v} \circ \delta
$$

Explicitly, in the special case that the [[field bundle]] is a [[trivial vector bundle]] over [[Minkowski spacetime]] (example \ref{TrivialVectorBundleAsAFieldBundle}) $\hat v$ is given by

$$
  \label{ProlongationOfEvolutionaryVectorFieldExplicit}
  \hat v = \underoverset{n = 0}{\infty}{\sum} \frac{d^n v^a}{ d x^{\mu_1} \cdots d x^{\mu_n} } \partial_{\phi^a_{\mu_1 \cdots \mu_n}}
  \,.
$$


=--

+-- {: .proof}
###### Proof

It is sufficient to prove the coordinate version of the statement.
We prove this by [[induction]] over the maximal jet order $k$. Notice that the coefficient of $\partial_{\phi^a_{\mu_1 \cdots \mu_k}}$
in $\hat v$ is given by the contraction $\iota_{\hat v} \delta \phi^a_{\mu_1 \cdots \mu_k}$ (def. \ref{ContractionOfFormsWithVectorFields}).

Similarly (at "$k = -1$") the component of $\partial_{\mu_1}$ is given by $\iota_{\hat v} d x^{\mu}$. But by the second condition
above this vanishes:

$$
  \begin{aligned}
    \iota_{\hat v} d x^\mu
    & =
    d \iota_{\hat v} x^\mu
    \\
    & =
    0
  \end{aligned}
$$

Moreover, the coefficient of $\partial_{\phi^a}$ in $\hat v$ is fixed by the first condition above to be

$$
  \iota_{\hat v} \delta \phi^a
  =
  v^a
  \,.
$$

This shows the statement for $k = 0$. Now assume that the statement is true up to some $k \in \mathbb{N}$.
Observe that the coefficients of all $\partial_{\phi^a_{\mu_1 \cdots \mu_{k+1}}}$ are fixed by the
contractions with $\delta \phi^a_{\mu_1 \cdots \mu_{k} \mu_{k+1}} \wedge d x^{\mu_{k+1}}$. For this we find again from the second
condition and using $\delta \circ d + d \circ \delta = 0$ as well as the induction assumption that

$$
  \begin{aligned}
    \iota_{\hat v} \delta \phi^a_{\mu_1 \cdots \mu_{k+1}} \wedge d x^{\mu_{k+1}}
    & =
    \iota_{\hat v}  \delta d \phi^a_{\mu_1 \cdots \mu_k}
    \\
    & =
    d \iota_{\hat v} \delta \phi^a_{\mu_1 \cdots \mu_k}
    \\
    &
    = d \frac{d^k v^a}{d x^{\mu_1} \cdots d x^{\mu_k}}
    \\
    & =
    \frac{d^{k+1}v^a }{d x^{\mu_1} \cdots d x^{\mu_{k+1}}} d x^{\mu_{k+1}}
    \,.
  \end{aligned}
$$

This shows that $\hat v$ satisfying the two conditions given exists uniquely.

Finally formula (eq:HomotopyFormulaForLieDerivativeAlongProlongationOfEvolutionaryVectorField) for the [[Lie derivative]] follows from the second of the two conditions with [[Cartan's homotopy formula]]
$\mathcal{L}_{\hat v} = \mathbf{d} \circ \iota_{\hat v} + \iota_{\hat v} \circ \mathbf{d}$ (prop. \ref{CartanHomotopyFormula})
together with $\mathbf{d} = \delta + d$ (eq:VariationalDerivative).

=--


+-- {: .num_prop #EvolutionaryVectorFieldLieAlgebra}
###### Proposition
**([[evolutionary vector fields]] form a [[Lie algebra]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[fiber bundle]]. For any two [[evolutionary vector fields]]
$v_1$, $v_2$ on $E$ (def. \ref{EvolutionaryVectorField}) the [[Lie bracket]] of [[tangent vector fields]]
of their prolongations $\hat v_1$, $\hat v_2$ (def. \ref{EvolutionaryVectorFieldProlongation})
is itself the prolongation $\widehat{[v_1, v_2]}$ of a unique evolutionary vector field $[v_1,v_2]$.

This defines the structure of a [[Lie algebra]] on evolutionary vector fields.

=--

+-- {: .proof}
###### Proof

It is clear that $[\hat v_1, \hat v_2]$ is still [[vertical vector field|vertical]], therefore, by
prop. \ref{EvolutionaryVectorFieldProlongation}, it is sufficient to show that contraction $\iota_{[v_1, v_2]}$ with this
vector field (def. \ref{ContractionOfFormsWithVectorFields}) anti-commutes with the [[horizontal derivative]] $d$,
hence that $[d, \iota_{[\hat v_1, \hat v_2]}] = 0$.

Now $[d, \iota_{[\hat v_1, \hat v_2]}]$ is an
operator that sends vertical 1-forms to horizontal 1-forms and vanishes on
horizontal 1-forms. Therefore it is sufficient to see that this operator
in fact also vanishes on all vertical 1-forms. But for this it is
sufficient that it commutes with the vertical derivative.
This we check by [[Cartan calculus]], using $[d,\delta] = 0$ and $[d, \iota_{\hat v_i}]$, by assumption:

$$
  \begin{aligned}
    {[ \delta, [ d,\iota_{[\hat v_1, \hat v_2]}] ]}
    & =
    - [d, [\delta, \iota_{[\hat v_1, \hat v_2]}]]
    \\
    & =
    - [d,  \mathcal{L}_{[\hat v_1, \hat v_2]}]
    \\
    & =
    -[d, [\mathcal{L}_{\hat v_1}, \iota_{\hat v_2}]  ]
    \\
    & =
    - [d, [ [\delta, \iota_{\hat v_1}], \iota_{\hat v_2}  ]]
    \\
    & =
    0
    \,.
  \end{aligned}
$$



=--

Now given an evolutionary vector field, we want to consider the [[flow]] that it
induces on the [[space of field histories]]:

+-- {: .num_defn #FlowOfFieldHistoriesAlongEvolutionaryVectorField}
###### Definition
**([[flow]] of [[field histories]] along [[evolutionary vector field]])**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] (def. \ref{FieldsAndFieldBundles})
and let $v$ be an [[evolutionary vector field]] (def. \ref{EvolutionaryVectorField})
such that the ordinary [[flow]] of its prolongation $\hat v$ (prop. \ref{EvolutionaryVectorFieldProlongation})

$$
  \exp(t \hat v)
  \;\colon\; J^\infty_\Sigma(E) \longrightarrow J^\infty_\Sigma(E)
$$

exists on the [[jet bundle]] (e.g. if the order of derivatives of field coordinates that it depends
on is bounded).


For $\Phi_{(-)} \colon U_1 \to  \Gamma_\Sigma(E)$ a collection of  [[field histories]]
(hence a plot of the [[space of field histories]] (def. \ref{SupergeometricSpaceOfFieldHistories}) ) the _[[flow]]_ of $v$
through $\Phi_{(-)}$ is the [[smooth function]]

$$
  U_1 \times \mathbb{R}^1
   \overset{\exp(v)(\Phi_{(-)})}{\longrightarrow}
  \Gamma_\Sigma(E)
$$

whose unique factorization $\widehat{\exp(v)}(\Phi_{(-)})$ through the space of jets of field histories
(i.e. the [[image]] $im(j^\infty_\Sigma)$ of [[jet prolongation]], def. \ref{JetProlongation})

$$
  \array{
    && im(j^\infty_\Sigma) &\hookrightarrow& \Gamma_\Sigma(J^\infty_\Sigma(E))
    \\
    & {}^{\mathllap{\widehat{\exp(v)}(\Phi_{(-)})}} \nearrow& \downarrow^{\mathrlap{\simeq}}
    \\
    U_1 \times \mathbb{R}^1
      &\underset{ \exp(v)(\Phi) }{\longrightarrow}&
    \Gamma_{\Sigma}(E)_{}
  }
$$

takes a plot $t_{(-)} \;\colon\; U_2 \to \mathbb{R}^1$ of the [[real line]]
(regarded as a [[super formal smooth set|super smooth set]] via example \ref{SuperSmoothSetSuperCartesianSpaces}), to the plot

$$
  \label{LocalDataForFlowOfImplicitInfinitesimalGaugeSymmetry}
  (\exp(t(-) \hat v) \circ j^\infty_\Sigma(\Phi_{(-)})
    \;\colon\:
  U_1 \times U_2   \longrightarrow \Gamma_\Sigma\left( J^\infty_\Sigma(E) \right)
$$

of the [[smooth space|smooth]] [[space of sections]] of the [[jet bundle]].

(That $\exp(t(-) \hat v)$ indeed flows jet prolongations $j^\infty_\Sigma(\Phi(-))$ again to jet prolongations
is due to its defining relation to the [[evolutionary vector field]] $v$ from prop. \ref{EvolutionaryVectorFieldProlongation}.)

=--



+-- {: .num_defn #SymmetriesAndConservedCurrents}
###### Definition
**([[infinitesimal symmetries of the Lagrangian]] and [[conserved currents]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

Then

1. an _[[infinitesimal symmetry of the Lagrangian]]_ is an [[evolutionary vector field]] $v$ (def. \ref{EvolutionaryVectorField})
   such that the [[Lie derivative]] of the [[Lagrangian density]] along its
   prolongation $\hat v$ (prop. \ref{EvolutionaryVectorFieldProlongation}) is a [[total spacetime derivative]]:

   $$
     \mathcal{L}_{\hat v} \mathbf{L} \;=\; d \tilde J_{\hat v}
   $$


1. an _[[on-shell]] [[conserved current]]_ is a horizontal $p$-form $J \in \Omega^{p,0}_\Sigma(E)$ (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime})
   whose [[total derivative|total spacetime derivative]] vanishes on the [[prolonged shell]] (eq:ShellInJetBundle)

   $$
     d J\vert_{\mathcal{E}^\infty} \;=\; 0
     \,.
   $$

=--




+-- {: .num_prop #NoethersFirstTheorem}
###### Proposition
**([[Noether's theorem]] I)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

If $v$ is an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents})
with $\mathcal{L}_{\hat v} \mathbf{L} = d \tilde J_{\hat v}$, then

$$
  \label{NoetherCurrent}
  J_{\hat v} \coloneqq \tilde J_{\hat v} - \iota_{\hat v} \Theta_{BFV}
$$

is an [[on-shell]] [[conserved current]] (def. \ref{SymmetriesAndConservedCurrents}), for $\Theta_{BFV}$
a presymplectic potential (eq:PresymplecticPotential) from def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}.

=--

([[Noether's theorem|Noether's theorem II]] is prop. \ref{NoetherIdentities} below.)

+-- {: .proof}
###### Proof

By [[Cartan's homotopy formula]] for the [[Lie derivative]] (prop. \ref{CartanHomotopyFormula})
and the decomposition of the variational derivative $\delta \mathbf{L}$ (eq:dLDecomposition)
and the fact that contraction $\iota_{\hat v}$ with the prolongtion of an evolutionary vector field vanishes on horizontal differential forms
(eq:GenericComponentsForProlongationOfEvolutionaryVectorField) and anti-commutes with the horizontal differential (eq:ProlongedEvolutionaryVectorFieldContractionAnticommutedWithHorizontalDerivative), by def. \ref{EvolutionaryVectorField},
we may re-express the defining equation for the symmetry as follows:

$$
  \begin{aligned}
    d \tilde J_{\hat v}
    & =
    \mathcal{L}_{\hat v} \mathbf{L}
    \\
    & =
    \iota_{\hat v} \underset{= \delta_{EL}\mathbf{L} - d \Theta_{BFV}}{\underbrace{\mathbf{d} \mathbf{L}}}
    +
    \mathbf{d} \underset{= 0}{\underbrace{\iota_v \mathbf{L}}}
    \\
    & =
    \iota_{\hat v} \delta_{EL} \mathbf{L}
    + d \iota_{\hat v} \Theta_{BFV}
  \end{aligned}
$$

which is equivalent to

$$
  d(\underset{= J_{\hat v}}{\underbrace{\tilde J_{\hat v} - \iota_{\hat v} \Theta_{BFV}}}) = \iota_{\hat v} \delta_{EL}\mathbf{L}
$$

Since, by definition of the [[shell]] $\mathcal{E}$, the differential form on the right
vanishes on $\mathcal{E}$ this yields the claim.

=--


+-- {: .num_example #ScalarFieldEnergyMomentum}
###### Example
**([[energy-momentum]] of the [[scalar field]])**

Consider the [[Lagrangian field theory]] of the [[free field|free]] [[scalar field]] from def. \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}:

$$
  \mathbf{L}
  \;=\;
  \tfrac{1}{2}
  \left(
    \eta^{\mu \nu}\phi_{,\mu} \phi_{,\nu}
    -
    m^2 \phi^2
  \right)
  dvol_\Sigma
  \,.
$$

For $\nu \in \{0, 1, \cdots, p\}$ consider the vector field on the jet bundle given by

$$
  v_\nu
  \;\coloneqq\;
  \phi_{,\nu} \partial_{\phi}
  +
  \phi_{,\mu \nu} \partial_{\phi_{,\mu}}
  +
  \cdots
  \,.
$$

This describes infinitesimal translations of the fields in the direction of $\partial_\nu$.

And this is an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents}), since

$$
  \iota_{v_\nu} \mathbf{d}\mathbf{L}
  =
  d L \wedge \iota_{\partial_\nu} dvol_\Sigma
  \,.
$$

With the formula (eq:PresymplecticPotentialOfFreeScalarField) for the presymplectic potential

$$
  \Theta_{BFV}
    =
  \eta^{\mu \nu} \phi_{,\mu} \delta \phi \iota_{\partial_{\nu}} dvol_\Sigma
$$

it hence follows from [[Noether's theorem]] (prop. \ref{NoethersFirstTheorem}) that the corresponding
[[conserved current]] (def. \ref{SymmetriesAndConservedCurrents}) is

$$
  \begin{aligned}
    T_\nu
     & =
     L \, \iota_{\partial_\nu} dvol_\Sigma
     -
     \iota_{v_\nu}\Theta_{BFV}
     \\
     &
     =
     L \, \iota_{\partial_\nu} dvol_\Sigma
     -
     \eta^{\rho \mu} \phi_{,\rho} \phi_{,\nu}
     \,
     \iota_{\partial_\mu} dvol_\Sigma
     \\
     &  =
     (
     \underset{=: T^\mu_\nu}{
     \underbrace{
       \delta^\mu_\nu  L
       -
       \eta^{\rho \mu} \phi_{,\rho} \phi_{,\nu}
     }
     }
     )
     \,
     \iota_{\partial_\mu} dvol_\Sigma
   \end{aligned}
   \,.
$$

This [[conserved current]] is called the _[[energy-momentum tensor]]_.


=--


+-- {: .num_example #DiracCurrent}
###### Example
**([[Dirac current]])**

Consider the [[Lagrangian field theory]] of the [[free field theory|free]] [[Dirac field]] on [[Minkowski spacetime]] in spacetime dimension $p + 1 = 3+1$ (example \ref{LagrangianDensityForDiracField})

$$
  \mathbf{L} = i \overline{\psi} \gamma^\mu \psi_{,\mu} \, dvol_\Sigma
  \,.
$$

Then the prolongation (prop. \ref{EvolutionaryVectorFieldProlongation}) of the [[evolutionary vector field]] (def. \ref{EvolutionaryVectorField})

$$
  v \;\coloneqq\; i \psi_\alpha \partial_{\psi_\alpha}
$$

is an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents}). The [[conserved current]] that corresponds to this under [[Noether's theorem|Noether's theorem I]] (prop. \ref{NoethersFirstTheorem}) is

$$
  \overline{\psi} \gamma^\mu \psi \, \iota_{\partial_\mu} dvol_\Sigma
  \;\in\;
  \Omega^{p,0}_{\Sigma(E)}
  \,.
$$

This is called the _[[Dirac current]]_.

In fact, due to the [[supergeometry|supergeometric]] nature of the [[Dirac field]], the [[Dirac current]] is conserved even [[off-shell]], as discussed in remark \ref{LagrangianDensityOfDiracFieldSupergeometricNature}.

=--


+-- {: .proof}
###### Proof

By equation (eq:ProlongationOfEvolutionaryVectorFieldExplicit) the prolongation of $v$ is

$$
  \hat v
    =
  i \psi_\alpha \partial_{\psi_\alpha}
    +
  i \psi_{\alpha,\mu} \partial_{\psi_{\alpha,\mu}}
    +
   \cdots
  \,.
$$

Therefore

$$
  \begin{aligned}
    \mathcal{L}_{\hat v} \left(
      i \overline{\psi} \gamma^\mu \psi_{,\mu}
    \right)
    dvol_\Sigma
    & =
    \underset{
      = i \cdot (-i) \overline{\psi} \gamma^\mu \psi_{,\mu}
    }{
    \underbrace{
      i \overline{i \psi} \gamma^\mu \psi_{,\mu}
    }
    }
    dvol_\Sigma
    +
    \underset{
      i \cdot i \overline{\psi} \gamma^\mu \psi_{,\mu}
    }{
    \underbrace{
      i \overline{\psi} \gamma^\mu (i \psi_{,\mu})
    }
    }
    dvol_\Sigma
    \\ & =
    0
  \end{aligned}
$$

=--


$\,$




Since an [[infinitesimal symmetry of a Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents}) by definition changes the Lagrangian only up to a [[total spacetime derivative]], and since the [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] by construction depend on the [[Lagrangian density]] only up to a [[total spacetime derivative]] (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}), it is plausible that and [[infinitesimal symmetry of the Lagrangian]] preserves the [[equations of motion]] (eq:EulerLagrangeEquationGeneral), hence the [[shell]] (eq:ProlongedShellInJetBundle). That this is indeed the case is the statement of prop. \ref{InfinitesimalSymmetriesOfLagrangianAreAlsoSymmetriesOfTheEquationsOfMotion} below.

To make the proof transparent, we now first introduce the concept of the _[[evolutionary derivative]]_ (def. \ref{FieldDependentDifferentialOperatorDerivative}) below and then observe that in terms of these the [[Euler-Lagrange derivative]] is in fact a [[derivation]] (prop. \ref{EulerLagrangeDerivativeIsDerivationViaAdjointFrechetDerivatives}).

+-- {: .num_defn #FieldDependentSections}
###### Definition
**([[field (physics)|field]]-dependent [[sections]])**

For

$$
  E \overset{fb}{\longrightarrow} \Sigma
$$

a [[fiber bundle]] (def. \ref{FiberBundle}), regarded as a [[field bundle]] (def. \ref{FieldsAndFieldBundles}), and for

$$
  E' \overset{fb'}{\longrightarrow} \Sigma
$$

any other [[fiber bundle]] over the same base space ([[spacetime]]), we write

$$
  \Gamma_{J^\infty_\Sigma(E)}(E')
  \;\coloneqq\;
  \Gamma_{J^\infty_\Sigma(E)}( jb^\ast E' )
  \;=\;
  Hom_\Sigma(J^\infty_\Sigma(E), E')
  \;\simeq\;
  DiffOp(E,E')
$$

for the [[space of sections]] of the [[pullback of bundles]] of $E'$ to the [[jet bundle]] $J^\infty_\Sigma(E) \overset{jb}{\longrightarrow} \Sigma$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) along $jb$.

$$
  \Gamma_{J^\infty_\Sigma(E)}(E')
  \;=\;
  \left\{
    \array{
       && E'
       \\
       & {}^{\mathllap{}}\nearrow & \downarrow \mathrlap{fb'}
       \\
       J^\infty_\Sigma(E)
       &\underset{jb}{\longrightarrow}&
       \Sigma
    }
    \phantom{A}\,\,
  \right\}
  \,.
$$

(Equivalently this is the space of [[differential operators]] from sections of $E$ to sections of $E'$, according to prop. \ref{DifferentialOperator}. )

=--


In ([Olver 93, section 5.1, p. 288](evolutionary+derivative#Olver93)) the field dependent sections of def. \ref{FieldDependentSections}, considered in [[local coordinates]], are referred to as [[tuples]] of _differential functions_.

+-- {: .num_example #EvolutionaryVectorFieldsAsFieldDependentSections}
###### Example
**([[source forms]] and [[evolutionary vector fields]] are field-dependent sections)**

For $E \overset{fb}{\to} \Sigma$ a [[field bundle]], write $T_\Sigma E$ for its [[vertical tangent bundle]] (example \ref{VerticalTangentBundle}) and $T_\Sigma^\ast E$ for its [[dual vector bundle]] (def. \ref{DualVectorBundle}), the [[vertical cotangent bundle]].

Then the field-dependent sections of these bundles according to def. \ref{FieldDependentSections} are identified as follows:

* the space $\Gamma_{J^\infty_\Sigma(E)}(T_\Sigma E)$ contains the space of [[evolutionary vector fields]] $v$ (def. \ref{EvolutionaryVectorField}) as those bundle morphism which respect not just the projection to $\Sigma$ but also its factorization through $E$:

  $$
    \left(
      \array{
        && T_\Sigma E
        \\
        & {}^{\mathllap{v}}\nearrow & \downarrow^{\mathrlap{tb_\Sigma}}
        \\
        J^\infty_\Sigma(E) &\underset{jb_{\infty,0}}{\longrightarrow}& E & \underset{fb}{\longrightarrow}& \Sigma
      }
    \right)
    \;\in\;
    \Gamma_{J^\infty_\Sigma(E)}(T_\Sigma E)
  $$

* $\Gamma_{J^\infty_\Sigma(E)}( T^\ast_\Sigma E) \otimes \wedge^{p+1}_\Sigma(T^\ast \Sigma)$ contains the space of [[source forms]] $E$ (prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) as those bundle morphisms which respect not just the projection to $\Sigma$ but also its factorization through $E$:

  $$
    \left(
      \array{
        && T^\ast_\Sigma E
        \\
        & {}^{E}\nearrow & \downarrow^{\mathrlap{ctb_\Sigma}}
        \\
        J^\infty_\Sigma(E) &\underset{jb_{\infty,0}}{\longrightarrow}& E & \underset{fb}{\longrightarrow}& \Sigma
      }
    \right)
    \;\in\;
    \Gamma_{J^\infty_\Sigma(E)}(T^\ast_\Sigma E)
  $$


This makes manifest the duality pairing between [[source forms]] and [[evolutionary vector fields]]

$$
  \array{
    \Gamma_{J^\infty_\Sigma(E)}(T_\Sigma E)
    \otimes
    \Gamma_{J^\infty_\Sigma(E)}(T^\ast_\Sigma E)
    &\longrightarrow&
    C^\infty(J^\infty_\Sigma(E))
  }
$$

which in local coordinates is given by

$$
  (v^a \partial_{\phi^a} \,,\, \omega_a \delta \phi^a)
  \mapsto
  v^a \omega_a
$$

for $v^a, \omega_a \in C^\infty(J^\infty_\Sigma(E))$ [[smooth functions]] on the [[jet bundle]] (as in prop. \ref{JetBundleIsLocallyProManifold}).

=--

+-- {: .num_defn #FieldDependentDifferentialOperatorDerivative}
###### Definition
**([[evolutionary derivative of field-dependent section]])**

Let

$$
  E \overset{fb}{\to} \Sigma
$$

be a [[fiber bundle]] regarded as a [[field bundle]] (def. \ref{FieldsAndFieldBundles}) and let

$$
  V \overset{vb}{\to} \Sigma
$$

be a [[vector bundle]] (def. \ref{VectorBundle}). Then for

$$
  P \in \Gamma_{J^\infty_\Sigma(E)}(V)
$$

a field-dependent section of $E$ according to def. \ref{FieldDependentSections}, its _evolutionary derivative_ is the morphism

$$
  \array{
    \Gamma_{J^\infty_\Sigma(E)}(T_\Sigma E)
      & \overset{  \mathrm{D}P }{\longrightarrow} &
    \Gamma_{J^\infty_\Sigma(E)}(V)
    \\
    v &\mapsto& \hat v(P)
  }
$$

which, under the identification of example \ref{EvolutionaryVectorFieldsAsFieldDependentSections}, sense an [[evolutionary vector field]] $v$ to the [[derivative]] of $P$ (example \ref{TangentVectorFields}) along the prolongation [[tangent vector field]] $\hat v $ of $v$ (prop. \ref{EvolutionaryVectorFieldProlongation}).


In the case that $E$ and $V$ are [[trivial vector bundles]] over [[Minkowski spacetime]] with coordinates $((x^\mu), (\phi^a))$ and $((x^\mu),  (\rho^b))$, respectively (example \ref{TrivialVectorBundleAsAFieldBundle}), then by (eq:ProlongationOfEvolutionaryVectorFieldExplicit) this is given by

$$
  ((\mathrm{D}P)(v))^b
   \;=\;
  \left(
     v^a \frac{\partial P^b}{\partial \phi^a}
     +
     \frac{d v^a}{d x^\mu}
     \frac{\partial P^b}{\partial \phi^a_{,\mu}}
     +
      \frac{d^2 v^a}{d x^\mu d x^\nu}
      \frac{\partial  P^b}{\partial \phi^a_{,\mu \nu}}
      +
     \cdots
  \right)
$$

This makes manifest that $\mathrm{D}P$ may equivalently be regarded as a $J^\infty_\Sigma(E)$-dependent [[differential operator]] (def. \ref{DifferentialOperator}) from the [[vertical tangent bundle]] $T_\Sigma E$ (def. \ref{VerticalTangentBundle}) to $V$, namely a [[bundle homomorphism]] over $\Sigma$ of the form

$$
  \mathrm{D}_P
  \;\colon\;
  J^\infty_\Sigma(E) \times_\Sigma J^\infty_\Sigma T_\Sigma E
  \longrightarrow
  V
$$

in that

$$
  \label{FrechetDerivativeAsDifferentialOperatorEquality}
  \mathrm{D}_P(-,v)
  =
  \mathrm{D}P(v)
  =
  \hat v (P)
  \,.
$$

=--


([Olver 93, def. 5.24](evolutionary+derivative#Olver93))


+-- {: .num_example #DifferentialOperatorDerivativeOfLagrangianFunction}
###### Example
**([[evolutionary derivative]] of [[Lagrangian function]])**

Over [[Minkowski spacetime]] $\Sigma$ (def. \ref{MinkowskiSpacetime}), let $\mathbf{L} = L dvol \in \Omega^{p,0}_\Sigma(E)$ be a [[Lagrangian density]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}), with coefficient function regarded as a field-dependent section (def. \ref{FieldDependentSections}) of the [[trivial bundle|trivial]] [[real line bundle]]:

$$
  L \;\in \; \Gamma_{J^\infty_\Sigma}(E)(\Sigma \times \mathbb{R})
  \,,
$$

Then the [[formally adjoint differential operator]] (def. \ref{FormallyAdjointDifferentialOperators})

$$
  (\mathrm{D}_L)^\ast
    \;\colon\;
  J^\infty_\Sigma(E)\times_\Sigma (\Sigma \times \mathbb{R})^\ast
  \longrightarrow
  T_\Sigma^\ast E
$$


of its [[evolutionary derivative]], def. \ref{FieldDependentDifferentialOperatorDerivative}, regarded as a $J^\infty_\Sigma(E)$-dependent differential operator $\mathrm{D}_P$ from $T_\Sigma$ to $V$ and applied to the constant section

$$
  1 \in \Gamma_\Sigma(\Sigma \times \mathbb{R}^\ast)
$$

is the [[Euler-Lagrange derivative]] (eq:EulerLagrangeEquationGeneral)

$$
  \delta_{EL}\mathbf{L}
  \;=\;
  \left(\mathrm{D}_{L}\right)^\ast(1)
  \;\in\;
  \Gamma_{J^\infty_\Sigma(E)}(T_\Sigma^\ast)
   \simeq
   \Omega^{p+1,1}_\Sigma(E)_{source}
$$

via the identification from example \ref{EvolutionaryVectorFieldsAsFieldDependentSections}.

=--

+-- {: .num_prop #EulerLagrangeDerivativeIsDerivationViaAdjointFrechetDerivatives}
###### Proposition
**([[Euler-Lagrange derivative]] is [[derivation]] via [[evolutionary derivatives]])**

Let $V \overset{vb}{\to} \Sigma$ be a [[vector bundle]] (def. \ref{VectorBundle}) and write $V^\ast \overset{}{\to} \Sigma$ for its [[dual vector bundle]] (def. \ref{DualVectorBundle}).

For field-dependent sections (def. \ref{FieldDependentSections})

$$
  \alpha \in \Gamma_{J^\infty_\Sigma(E)}(V)
$$

and

$$
  \beta^\ast \in \Gamma_{J^\infty_\Sigma(E)}(V^\ast)
$$

we have that the [[Euler-Lagrange derivative]] (eq:EulerLagrangeEquationGeneral) of their canonical pairing to a [[smooth function]] on the [[jet bundle]] (as in prop. \ref{JetBundleIsLocallyProManifold}) is the sum of the derivative of either one via the [[formally adjoint differential operator]] (def. \ref{FormallyAdjointDifferentialOperators}) of the [[evolutionary derivative]] (def. \ref{FieldDependentDifferentialOperatorDerivative}) of the other:

$$
  \delta_{EL}( \alpha \cdot \beta^\ast )
  \;=\;
  (\mathrm{D}_\alpha)^\ast(\beta^\ast)
  +
  (\mathrm{D}_{\beta^\ast})^\ast(\alpha)
$$

=--


+-- {: .proof}
###### Proof

It is sufficient to check this in [[local coordinates]]. By the [[product law]] for [[differentiation]] we have

$$
  \begin{aligned}
    \frac{
      \delta_{EL} \left(\alpha \cdot \beta^\ast \right)
    }
    {
      \delta \phi^a
    }
    & =
    \frac{\partial \left(\alpha \cdot \beta^\ast \right)}{\partial \phi^a}
    -
    \frac{d}{d x^\mu}
    \left(
       \frac{\partial \left( \alpha \cdot \beta^\ast \right)}{\partial \phi^a_{,\mu}}
    \right)
    +
    \frac{d}{d x^\mu d x^\nu}
    \left(
       \frac{\partial \left( \alpha \cdot \beta^\ast \right) }{\partial \phi^a_{,\mu \nu}}
    \right)
    -
    \cdots
    \\
    & =
    \phantom{+}
    \frac{\partial \alpha }{\partial \phi^a}
    \cdot \beta^\ast
    -
    \frac{d}{d x^\mu}
    \left(
       \frac{\partial \alpha }{\partial \phi^a_{,\mu}}
       \cdot
       \beta^\ast
    \right)
    +
    \frac{d}{d x^\mu d x^\nu}
    \left(
       \frac{\partial \alpha  }{\partial \phi^a_{,\mu \nu}}
       \cdot
       \beta^\ast
    \right)
    -
    \cdots
    \\
    & \phantom{=}
    +
    \frac{\partial \beta^\ast }{\partial \phi^a}
    \cdot \alpha
    -
    \frac{d}{d x^\mu}
    \left(
       \frac{\partial \beta^\ast }{\partial \phi^a_{,\mu}}
       \cdot
       \alpha
    \right)
    +
    \frac{d}{d x^\mu d x^\nu}
    \left(
       \frac{\partial \beta^\ast  }{\partial \phi^a_{,\mu \nu}}
       \cdot
       \alpha
    \right)
    -
    \cdots
    \\
    & =
    (\mathrm{D}_\alpha)^\ast(\beta^\ast)
    +
    (\mathrm{D}_{\beta^\ast})^\ast(\alpha)
  \end{aligned}
$$

=--


+-- {: .num_prop #EvolutionaryDerivativeOfEulerLagrangeFormIsFormallySelfAdjoint}
###### Proposition
**([[evolutionary derivative]] of [[Euler-Lagrange forms]] is [[formally self-adjoint differential operator|formally self-adjoint]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) over [[Minkowski spacetime]] (def. \ref{MinkowskiSpacetime}) and regard the [[Euler-Lagrange derivative]]

$$
  \delta_{EL}\mathbf{L}
  \;=\;
  \delta_{EL}L \wedge dvol_\Sigma
$$

(from prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) as a field-dependent section of the [[vertical cotangent bundle]]

$$
  \delta_{EL}L
  \;\in\;
  \Gamma_{J^\infty_\Sigma(E)}(T^\ast_\Sigma E)
$$

as in example \ref{EvolutionaryVectorFieldsAsFieldDependentSections}. Then the corresponding [[evolutionary derivative]] field-dependent [[differential operator]] $D_{\delta_{EL}L}$ (def. \ref{FieldDependentDifferentialOperatorDerivative})  is [[formally self-adjoint differential operator|formally self-adjoint]] (def. \ref{FormallyAdjointDifferentialOperators}):

$$
  (D_{\delta_{EL}L})^\ast
  \;=\;
  D_{\delta_{EL}L}
$$

=--

([Olver 93, theorem 5.92](evolutionary+derivative#Olver93)) The following proof is due to [[Igor Khavkine]].

+-- {: .proof}
###### Proof

By definition of the [[Euler-Lagrange form]] (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}) we have

$$
  \frac{\delta_{EL} L }{\delta \phi^a}
  \delta \phi^a
  \,
  \wedge
  dvol_\Sigma
  \;=\;
  \delta L \,\wedge dvol_\Sigma \;+\; d(...)
  \,.
$$

Applying the [[variational derivative]] $\delta$ (def. \ref{VariationalBicomplexOnSecondOrderJetBundleOverTrivialVectorBundleOverMinkowskiSpacetime}) to both sides of this equation yields

$$
  \left(\delta \frac{\delta_{EL} L }{\delta \phi^a}\right)
  \wedge
  \delta \phi^a
  \,
  \wedge
  dvol_\Sigma
  \;=\;
  \underset{= 0}{\underbrace{\delta \delta L}} \wedge dvol_\Sigma
  \;+\;
  d(...)
  \,.
$$

It follows that for $v,w$ any two [[evolutionary vector fields]] the contraction (def. \ref{ContractionOfFormsWithVectorFields}) of their prolongations $\hat v$ and $\hat w$ (def. \ref{EvolutionaryVectorFieldProlongation}) into the [[variational differential form|differential 2-form]] on the left is

$$
  \left(
    \delta \frac{\delta_{EL} L }{\delta \phi^a}
    \wedge
    \delta \phi^a
  \right)(v,w)
  =
    w^a
    (\mathrm{D}_{\delta_{EL}})_a(v)
    -
    v^b(\mathrm{D}_{\delta_{EL}})_b(w)
  \,,
$$

by inspection of the definition of the [[evolutionary derivative]] (def. \ref{FieldDependentDifferentialOperatorDerivative}).
Moreover, their contraction into the differential form on the right is

$$
  \iota_{\hat v}
  \iota_{\hat w}
  d(...)
  \;=\;
  d(...)
$$

by the fact (prop. \ref{EvolutionaryVectorFieldProlongation}) that contraction with prolongations of evolutionary vector fields antio-commutes with the [[total spacetime derivative]] (eq:ProlongedEvolutionaryVectorFieldContractionAnticommutedWithHorizontalDerivative).

Hence the last two equations combined give

$$
  w^a
  (\mathrm{D}_{\delta_{EL}})_a(v)
  -
  v^b(\mathrm{D}_{\delta_{EL}})_b(w)
  \;=\;
  d(...)
  \,.
$$


This is the defining condition for $\mathrm{D}_{\delta_{EL}}$ to be [[formally self-adjoint differential operator]] (def. \ref{FormallyAdjointDifferentialOperators}).

=--


$\,$

Now we may finally prove that an [[infinitesimal symmetry of the Lagrangian]] is also an infinitesimal symmetry of the [[Euler-Lagrange equations|Euler-Lagrange]] [[equations of motion]]:

+-- {: .num_prop #InfinitesimalSymmetriesOfLagrangianAreAlsoSymmetriesOfTheEquationsOfMotion}
###### Proposition
**([[infinitesimal symmetries of the Lagrangian]] are also [[infinitesimal symmetries]] of the [[equations of motion]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]]. If an [[evolutionary vector field]] $v$ is an [[infinitesimal symmetry of the Lagrangian]] then the [[flow]] along its prolongation $\hat v$ preserves the [[prolonged shell]] $\mathcal{E}^\infty \hookrightarrow J^\infty_\Sigma(E)$ (eq:ProlongedShellInJetBundle) in that the [[Lie derivative]] of the [[Euler-Lagrange form]] $\delta_{EL}\mathbf{L}$ along $\hat v$ vanishes on $\mathcal{E}^\infty$:

$$
  \mathcal{L}_{\hat v}\mathbf{L} = d(...)
  \phantom{AAA}
  \Rightarrow
  \phantom{AAA}
  \mathcal{L}_{\hat v} \, \delta_{EL}\mathbf{L}\vert_{\mathcal{E}^\infty} = 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

Notice that for any vector field $\hat v$ the [[Lie derivative]] (prop. \ref{CartanHomotopyFormula})$\mathcal{L}_{\hat v}$ of the [[Euler-Lagrange form]] $\delta_{EL}\mathbf{L} = \frac{\delta_{EL}L}{\delta \phi^a} \delta \phi^a \wedge dvol_\Sigma$ differs from that of its component functions $\frac{\delta_{EL}L}{\delta \phi^a} dvol_\Sigma$ by a term proportional to these component functions, which by definition vanishes on-shell:

$$
  \mathcal{L}_{\hat v} \left( \frac{\delta_{EL} L}{\delta \phi^a} \delta \phi^a \wedge dvol_\Sigma \right)
  \;=\;
  \underset{
    = \hat v\left( \frac{\delta_{EL}L}{\delta \phi^a} \right)
  }{
  \underbrace{
  \left(
    \mathcal{L}_{\hat v}
     \frac{\delta_{EL}L}{\delta \phi^a}
  \right)
  }
  }
  \delta \phi^a
  \wedge
  dvol_\Sigma
  +
  \underset{
    = 0 \, \text{on} \, \mathcal{E}^\infty
  }{
  \underbrace{
    \frac{\delta_{EL}L}{\delta \phi^a}
  }
  }
    \left(
    \mathcal{L}_{\hat v} \delta \phi^a
    \right)
    \wedge dvol_\Sigma
$$

 But the Lie derivative of the component functions is just their plain derivative. Therefore it is sufficient to show that

$$
  \hat v
  \left(
    \frac{\delta_{EL} L}{\delta \phi^a}
  \right)
  \vert_{\mathcal{E}^\infty}
  \;=\;
  0
  \,.
$$

Now by [[Noether's theorem|Noether's theorem I]] (prop. \ref{NoethersFirstTheorem}) the condition $\mathcal{L}_{\hat v} = d \tilde J_{\hat v}$ for an [[infinitesimal symmetry of the Lagrangian]] implies that  the contraction (def. \ref{ContractionOfFormsWithVectorFields}) of the [[Euler-Lagrange form]] with the corresponding [[evolutionary vector field]] is a [[total spacetime derivative]]:

$$
  \iota_{\hat v} \, \delta_{EL}\mathbf{L}
  \;=\;
  d J_{\hat v}
  \,.
$$

Since the [[Euler-Lagrange derivative]] vanishes on [[total spacetime derivative]] (example \ref{TrivialLagrangianDensities}) also its application on the contraction on the left vanishes. But via example \ref{EvolutionaryVectorFieldsAsFieldDependentSections} that contraction is a pairing of field-dependent sections as in prop. \ref{EulerLagrangeDerivativeIsDerivationViaAdjointFrechetDerivatives}. Hence we use this proposition to compute:

$$
  \begin{aligned}
    0
    & =
    \frac{\delta_{EL} \left( v \cdot \delta_{EL} L\right) }{ \delta \phi^a }
    \\
    & =
    (\mathrm{D}_{v})^\ast( \delta_{EL}L )
    +
    (\mathrm{D}_{\delta_{EL}L})^\ast(v)
    \\
    & =
    (\mathrm{D}_{v})^\ast( \delta_{EL}L )
    +
    (\mathrm{D}_{\delta_{EL}L})(v)
    \\
    & =
    (\mathrm{D}_{v})^\ast( \delta_{EL}L )
    +
    \hat v(\delta_{EL}L)
    \,.
  \end{aligned}
$$

Here the first step is by prop. \ref{EulerLagrangeDerivativeIsDerivationViaAdjointFrechetDerivatives}, the second step is by prop. \ref{EvolutionaryDerivativeOfEulerLagrangeFormIsFormallySelfAdjoint} and the third step is
(eq:FrechetDerivativeAsDifferentialOperatorEquality).

Hence

$$
  \begin{aligned}
    \hat v(\delta_{EL}L) \vert_{\mathcal{E}^\infty}
    & =
    -
    (\mathrm{D}_{v})^\ast( \delta_{EL}L ) \vert_{\mathcal{E}^\infty}
    \\
    & =
    0
  \end{aligned}
  \,,
$$

where in the last line we used that on the [[prolonged shell]] $\delta_{EL}L$ and all its horizontal derivatives vanish, by definition.


=--


As a corollary we obtain:


+-- {: .num_prop #FlowAlongInfinitesimalSymmetryOfLagrangianPreservesOnShellSpaceOfFieldHistories}
###### Proposition
**([[flow]] along [[infinitesimal symmetry of the Lagrangian]] preserves [[on-shell]] [[space of field histories]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

For $v$ an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents})
the [[flow]] on the [[space of field histories]] (example \ref{DiffeologicalSpaceOfFieldHistories}) that it induces by def. \ref{FlowOfFieldHistoriesAlongEvolutionaryVectorField}
preserves the space of [[on-shell]] field histories (from prop. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}):

$$
  \array{
    \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
      &\hookrightarrow&
    \Gamma_\Sigma(E)
    \\
    {\mathllap{\exp(\hat v)\vert_{\delta_{EL}\mathbf{L} = 0}  }}
    \uparrow
      &&
    \uparrow {\mathrlap{\exp(\hat v)}}
    \\
    \Gamma_\Sigma(E)_{\delta_{EL}\mathbf{L} = 0}
      &\hookrightarrow&
    \Gamma_\Sigma(E)
  }
$$

=--


+-- {: .proof}
###### Proof


By def. \ref{EulerLagrangeEquationsOnTrivialVectorFieldBundleOverMinkowskiSpacetime} a field history
$\Phi \in \Gamma_\Sigma(E)$ is [[on-shell]] precisely if its [[jet prolongation]] $j^\infty_\Sigma(E)$ (def. \ref{JetProlongation})
factors through the [[shell]] $\mathcal{E} \hookrightarrow J^\infty_\Sigma(E)$ (eq:ShellInJetBundle).
Hence by def. \ref{FlowOfFieldHistoriesAlongEvolutionaryVectorField} the statement is equivalently that
the ordinary flow (prop. \ref{CartanHomotopyFormula}) of $\hat v$ (def. \ref{EvolutionaryVectorFieldProlongation})
on the [[jet bundle]] $J^\infty_\Sigma(E)$ preserves the [[shell]]. This in turn means that it preserves the
vanishing locus of the [[Euler-Lagrange form]] $\delta_{EL} \mathbf{L}$, which is the case by prop. \ref{InfinitesimalSymmetriesOfLagrangianAreAlsoSymmetriesOfTheEquationsOfMotion}.

=--





$\,$

**[[infinitesimal symmetries]] of the [[presymplectic potential current]]**
 {#InfinitesimalSymmetriesOfThePresymplecticPotentialCurrent}

Evidently [[Noether's theorem|Noether's theorem I]] in [[variational calculus]] (prop. \ref{NoethersFirstTheorem})
is the special case for horizontal $p+1$-forms of a more general phenomenon relating
symmetries of variational forms to forms that are closed up to a contraction. The same phenomenon applied instead
to the [[presymplectic current]] yields the following:


+-- {: .num_defn #LieDerivativeVariational}
###### Definition
**(variational Lie derivative)**

Let $E \overset{fb}{\to} \Sigma$ be a [[field bundle]] (def. \ref{FieldsAndFieldBundles})
with [[jet bundle]] $J^\infty_\Sigma(E)$ (def. \ref{JetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

For $v$ a vertical [[tangent vector field]] on the [[jet bundle]] (a variation def. \ref{Variation})
write

$$
  \label{LieDerivativeVariational}
  \mathcal{L}^{var}_{v}
    \;\coloneqq\;
  \delta \circ \iota_v + \iota_v \circ \delta
$$

for the _variational Lie derivative_ along $v$, analogous to [[Cartan's homotopy formula]] (prop. \ref{CartanHomotopyFormula})
but defined in terms of the variational derivative $\delta$ (eq:VariationalDerivative) as opposed to the full [[de Rham differential]].

Then for $v_1$ and $v_2$ two vertical vector fields, write

$$
  [v_1, v_2]^{var} \;\in \; \Gamma( T_{vert} J^\infty_\Sigma(E) )
$$

for the vector field whose contraction operator (def. \ref{ContractionOfFormsWithVectorFields}) is given by

$$
  \begin{aligned}
    \iota_{[v_1,v_2]^{var}}
     & =
    \left[
      \mathcal{L}^{var}_{v_1}, \iota_{v_2}
    \right]
    \\
    & \coloneqq
    \mathcal{L}^{var}_{v_1} \circ \iota_{v_2}
    -
    \iota_{v_2} \circ \mathcal{L}^{var}_{v_1}
  \end{aligned}
  \,,
$$

=--


+-- {: .num_defn #HamiltonianForms}
###### Definition
**([[Hamiltonian vector fields|infinitesimal symmetry of the presymplectic potential]] and [[Hamiltonian differential forms]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}) with [[presymplectic potential current]] $\Theta_{BFV}$ (eq:PresymplecticPotential). Write $\mathcal{E} \hookrightarrow J^\infty_\Sigma(E)$ for the [[shell]] (eq:ShellInJetBundle).

Then:

1. An [[on-shell]] variation $v$ (def. \ref{Variation}) is an _[[infinitesimal symmetry]] of the [[presymplectic current]]_
   or _[[Hamiltonian vector field]]_ if [[on-shell]] (def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime})
   its variational Lie derivative along $v$ (def. \ref{LieDerivativeVariational}) is a [[variational derivative]]:

   $$
     (\delta \circ \iota_v + \iota_v \circ \delta)  \Theta_{BFV}  = \delta \tilde H_v
     \phantom{AAA}
     \text{on}\, \mathcal{E}
   $$

   for some variational form $\tilde H_v$.

1. A _[[Hamiltonian differential form]]_ $H$ (or _local Hamiltonian current_) is a variational form on the shell such that there
   exists a variation $v$ with

   $$
     \delta H = \iota_v \Omega_{BFV}
     \phantom{AA}
     \,
     \text{on}\, \mathcal{E}
     \,.
   $$

We write

$$
  \Omega^{p,0}_{\Sigma, Ham}(E)
  \;\coloneqq\;
  \left\{
    (H,v)
    \;\vert\;
    v \, \text{is a variation and}\,
    \iota_v \Omega_{BFV} = \delta H
  \right\}
$$

for the space of pairs consisting of a Hamiltonian differential forms [[on-shell]] and a corresponding variation.

=--


+-- {: .num_prop #HamiltonianDifferentialForms}
###### Proposition
**([[Hamiltonian Noether's theorem]])**

A variation $v$ is an infinitesimal symmetry of the presymplectic potential (def. \ref{HamiltonianForms})
with $\mathcal{L}^{var}_v ( \Theta_{BFV} ) = \delta \tilde H_v$ precisely if

$$
  H_v \coloneqq \tilde H_v - \iota_v \Theta_{BFV}
$$

is a [[Hamiltonian differential form]] for $v$.

=--


+-- {: .proof}
###### Proof

From the definition (eq:LieDerivativeVariational) of $\mathcal{L}^{var}_v$ we have

$$
  \begin{aligned}
    & \mathcal{L}^{var}_v \Theta_{BFV}
    =
    \delta \tilde H_v
    \\
    \Leftrightarrow\;\;
    &
    \delta \iota_v \Theta_{BFV} + \iota_v \underset{= \Omega_{BFV}}{\underbrace{\delta \Theta_{BFV}}} = \delta \tilde H_v
    \\
    \Leftrightarrow\;\;
    &
    \delta \left(
      \tilde H_v - \iota_v \Theta_{BFV}
    \right)
    =
    \iota_v \Omega_{BFV}
    \,,
  \end{aligned}
$$

where we used the definition (eq:PresymplecticCurrent) of $\Omega_{BFV}$ .

=--



$\,$





Since therefore both the [[conserved currents]] from [[Noether's theorem]] as well as
the [[Hamiltonian differential forms]] are generators of infinitesimal [[symmetries]] of certain variational forms
(namely of the [[Lagrangian density]] and of the [[presymplectic current]], respectively) they
form a [[Lie algebra]]. For the conserved currents this is sometimes known as the _[[Dickey bracket]] Lie algebra_.
For the Hamiltonian forms it is the _[[Poisson bracket Lie n-algebra|Poisson bracket Lie p+1-algebra]]_. Since here for simplicity
we are considering just vertical variations, we have just a plain [[Lie algebra]].
The [[transgression of variational differential forms|transgression]] of this Lie algebra of Hamiltonian forms
on the jet bundle to [[Cauchy surfaces]] yields a [[presymplectic structure]] on [[phase space]], this we discuss
[below](#PhaseSpace).


+-- {: .num_prop #LocalPoissonBracket}
###### Proposition
**([[Poisson bracket Lie n-algebra|local Poisson bracket]])**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

On the space $\Omega^{p,0}_{\Sigma,Ham}(E)$ pairs $(H,v)$ of [[Hamiltonian differential forms]] $H$ with compatible variation $v$ (def. \ref{HamiltonianForms}) the following operation constitutes a [[Lie bracket]]:

$$
  \label{LocalPoissonLieBracket}
  \left\{(H_1, v_1),\, (H_2, v_2)\right\}
  \;\coloneqq\;
  (\iota_{v_1} \iota_{v_2} \Omega_{BFV},\, [v_1,v_2]^{var})
  \,,
$$

where $[v_1, v_2]^{var}$ is the variational Lie bracket from def. \ref{LieDerivativeVariational}.

We call this the _local Poisson Lie bracket_.

=--


+-- {: .proof}
###### Proof

First we need to check that the bracket is well defined in itself. It
is clear that it is linear and skew-symmetric, but what needs proof is that
it does indeed land in $\Omega^{p,0}_{\Sigma,Ham}(E)$, hence that the following
equation holds:

$$
  \delta \iota_{v_2} \iota_{v_1} \Omega_{BFV}
  \;=\;
  \iota_{[v_1, v_2]^{var}} \Omega_{BFV}
  \,.
$$



With def. \ref{LieDerivativeVariational} for $\mathcal{L}^{var}$ and $[-,-]^{var}$ we compute this as follows:

$$
  \begin{aligned}
    \delta \iota_{v_1} \iota_{v_2} \Omega_{BFV}
    & =
    \tfrac{1}{2} \delta \iota_{v_1} \iota_{v_2} \Omega_{BFV}
    -
    \tfrac{1}{2} (v_1 \leftrightarrow v_2)
    \\
    & =
    \tfrac{1}{2}
    \left(
      \mathcal{L}^{var}_{v_1} \iota_{v_2} \Omega_{BFV}
      -
      \iota_{v_1} \delta \iota_{v_2} \Omega_{BFV}
    \right)
    -
    \tfrac{1}{2} (v_1 \leftrightarrow v_2)
    \\
    & =
    \tfrac{1}{2}
    \left(
      \mathcal{L}^{var}_{v_1} \iota_{v_2} \Omega_{BFV}
      -
      \iota_{v_1} \mathcal{L}^{var}_{v_2} \Omega_{BFV}
      +
      \iota_{v_1} \iota_{v_2} \underset{= 0}{\underbrace{\delta \Omega_{BFV}}}
    \right)
    -
    \tfrac{1}{2} (v_1 \leftrightarrow v_2)
    \\
    & =
    [\mathcal{L}^{var}_{v_2}, \iota_{v_1}] \Omega_{BFV}
    \\
    & =
    \iota_{[v_1, v_2]^{var}} \Omega_{BFV}
    \,.
  \end{aligned}
$$

This shows that the bracket is well defined.

It remains to see that the bracket satifies the [[Jacobi identity]]:

$$
\left\{ (H_1, v_1), \left\{ (H_2, v_2), (H_3,v_3) \right\} \right\}
  \;+\; (cyclic)
   \;=\;
  0
$$

hence that

$$
  \left(  \iota_{v_1} \iota_{[v_2,v_3]^{var}}  \Omega_{BFV} ,\,   [v_1, [v_2, v_2]^{var}]^{var} \right)
  \;+\; (cyclic)
  \;=\; 0
  \,.
$$

Here $ [v_1, [v_2, v_3]^{var}]^{var} + (cyclic) = 0 $ holds because by def. \ref{LieDerivativeVariational} $[v_1,-]^{var}$
acts as a derivation,
and hence what remains to be shown is that

$$
  \iota_{v_1} \iota_{\left([v_2, v_3]^{var}\right)}   \Omega_{BFV} + (cyclic) = 0
$$

We check this by repeated uses of def. \ref{LieDerivativeVariational}, using in addition
that

1. $\delta \iota_{v_i} \Omega_{BFV} = 0$

   (since $\iota_{v_i} \Omega_{BFV} = \delta H_i$ by $v_i$ being Hamiltonian)

1. $\mathcal{L}^{var}_{v_i} \Omega_{BFV} = 0$

   (since in addition $\delta \Omega_{BFV} = 0$)

1. $\iota_{v_1} \iota_{v_2} \iota_{v_3} \Omega_{BFV} = 0$

   (since $\Omega_{BFV} \in \Omega^{p,2}_\Sigma(E)$ is of vertical degree 2, and since all variations $v_i$ are vertical by assumption).

So we compute as follows (a special case of [FRS 13b, lemma 3.1.1](Poisson+bracket+Lie+n-algebra#FRS13b)):

$$
  \begin{aligned}
    0
    & =
    \delta \iota_{v_1} \iota_{v_2} \iota_{v_3} \Omega_{BFV}
    \\
    & =
    \mathcal{L}^{var}_{v_1} \iota_{v_2} \iota_{v_3} \Omega_{BFV}
    -
    \iota_{v_1} \delta \iota_{v_2} \iota_{v_3} \Omega_{BFV}
    \\
    & =
    \iota_{[v_1, v_2]^{var}} \iota_{v_3} \Omega_{BFV}
    +
    \iota_{v_2} \mathcal{L}^{var}_{v_1} \iota_{v_3} \Omega_{BFV}
    -
    \iota_{v_1} \mathcal{L}^{var}_{v_2} \iota_{v_3} \Omega_{BFV}
    +
    \iota_{v_1} \iota_{v_2} \delta \iota_{v_3} \Omega_{BFV}
    \\
    & =
    \iota_{[v_1, v_2]^{var}} \iota_{v_3} \Omega_{BFV}
    +
    \iota_{v_2} \iota_{[v_1,v_3]^{var}} \Omega_{BFV}
    -
    \iota_{v_1} \iota_{[v_2, v_3]^{var}} \Omega_{BFV}
    \\
    & =
    -
    \iota_{v_1} \iota_{[v_2, v_3]^{var}} \Omega_{BFV}
    -
    \iota_{v_2} \iota_{[v_3, v_1]^{var}} \Omega_{BFV}
    -
    \iota_{v_3} \iota_{[v_1, v_2]^{var}} \Omega_{BFV}
    \,.
  \end{aligned}
$$

=--

$\,$

The [[Poisson bracket Lie n-algebra|local Poisson bracket]] [[Lie algebra]] $(\Omega^{p,0}_{\Sigma,Ham}(E), [-,-]^{var})$ from prop.
\ref{LocalPoissonBracket} is but the lowest stage of
a [[higher Lie theory|higher Lie theoretic]] structure called the _[[Poisson bracket Lie n-algebra|Poisson bracket Lie p-algebra]]_.
Here we will not go deeper into this [[schreiber:Higher Structures|higher structure]] (see at _[[schreiber:Higher Prequantum Geometry]]_
for more), but below we will need the following simple shadow of it:

+-- {: .num_lemma #HorizontallyExactFormsDropOutOfLocalLieBracket}
###### Lemma

The horizontally exact Hamiltonian forms constitute a [[Lie ideal]] for the
local Poisson Lie bracket (eq:LocalPoissonLieBracket).

=--

+-- {: .proof}
###### Proof

Let $E$ be a horizontally exact Hamiltonian form, hence

$$
  E = d K
$$

for some $K$. Write $e$ for a [[Hamiltonian vector field]] for $E$.

Then for $(H,v)$ any other pair consisting of a Hamiltonian form and a corresponding
Hamiltonian vector field, we have

$$
  \begin{aligned}
    \iota_v \, \iota_e \, \Omega_{BFV}
    & =
    \phantom{-}\iota_v \, \delta E
    \\
    & =
    \phantom{-}\iota_v \, \delta \, d \, K
    \\
    & =
    - \iota_v \, d \, \delta K
    \\
    & =
    \phantom{-}d \, \iota_v \, \delta \, K
    \,.
  \end{aligned}
$$

Here we used that the horizontal derivative anti-commutes with the
vertical one by construction of the [[variational bicomplex]], and
 that $\iota_e$ anti-commutes with the horizontal derivative $d$ since the variation $e$ (def. \ref{Variation}) is
by definition vertical.

=--



+-- {: .num_example #LocalPoissonBracketForRealScalarField}
###### Example
**([[Poisson bracket Lie n-algebra|local Poisson bracket]] for [[real scalar field]])**

Consider the [[Lagrangian field theory]] for the [[free field|free]] [[real scalar field]] from example \ref{LagrangianForFreeScalarFieldOnMinkowskiSpacetime}.

By example \ref{FreeScalarFieldEOM} its [[presymplectic current]] is

$$
  \Omega_{BFV}
   =
  \eta^{\mu \nu} \delta \phi_{,\mu} \wedge \delta \phi \wedge \iota_{\partial_\mu} dvol_\Sigma
  \,
$$

The corresponding [[Poisson bracket Lie n-algebra|local Poisson bracket algebra]] (prop. \ref{LocalPoissonBracket}) has in degree 0
[[Hamiltonian forms]] (def. \ref{HamiltonianDifferentialForms}) such as

$$
  Q \;\coloneqq\; \phi \,\iota_{\partial_0} dvol_\Sigma \in \Omega^{p,0}(E)
$$

and

$$
  P \;\coloneqq\; \eta^{\mu \nu} \phi_{,\mu} \, \iota_{\partial_\nu} dvol_{\Sigma} \in \Omega^{p,0}(E)
  \,.
$$

The corresponding [[Hamiltonian vector fields]] are

$$
 v_Q = -\partial_{\phi_{,0}}
$$

and

$$
  v_P = - \partial_{\phi}
  \,.
$$

Hence the corresponding [[Poisson bracket Lie n-algebra|local Poisson bracket]] is

$$
  \{P,Q\} = \iota_{v_P} \iota_{v_Q} \omega = \iota_{\partial_0} dvol_\Sigma
  \,.
$$

More generally for $b_1, b_2 \in C^\infty_{cp}(\Sigma)$ two [[bump functions]] then

$$
  \{ b_1 P, b_2 Q \} = b_1 b_2 \iota_{\partial_0} dvol_\Sigma
  \,.
$$

=--




+-- {: .num_example #LocalPoissonBracketForDiracField}
###### Example
**([[Poisson bracket Lie n-algebra|local Poisson bracket]] for [[free field theory|free]] [[Dirac field]])**

Consider the [[Lagrangian field theory]] of the [[free field theory|free]] [[Dirac field]] on [[Minkowski spacetime]] (example \ref{LagrangianDensityForDiracField}), whose [[presymplectic current]] is, according to example \ref{PresymplecticCurrentDiracField}, given by

$$
  \label{RecallPresymplecticCurrentOfDiracField}
  \Omega_{BFV}
  \;=\;
  (\overline{\delta \psi}) \, \gamma^\mu \, (\delta \psi) \, \iota_{\partial_\mu} dvol_\Sigma
  \,.
$$

Consider this specifically in [[spacetime]] [[dimension]] $p + 1 = 4$ in which case the components $\psi_\alpha$ are [[complex number]]-valued (by prop./def. \ref{SpacetimeAsMatrices}), so that the [[tuple]] $(\psi_\alpha)$ amounts to 8 real-valued coordinate functions. By changing complex coordinates, we may equivalently consider $(\psi_\alpha)$ as four coordinate functions, and $(\overline{\psi}^\alpha)$ as another four independent coordinate functions.

Using this coordinate transformation, it is immediate to find the following [[pairs]] of [[Hamiltonian vector fields]] and their [[Hamiltonian differential forms]] from def. \ref{HamiltonianForms} applied to (eq:RecallPresymplecticCurrentOfDiracField)

| [[Hamiltonian vector field]] | [[Hamiltonian differential form]] |
|------------------------------|-----------------------------------|
|  $\phantom{AA} \partial_{\psi_\alpha}$      | $\phantom{AA}\left(\overline{\delta \psi}\gamma^\mu\right)^\alpha\, \iota_{\partial_\mu} dvol_\Sigma$ |
| $\phantom{AA} \partial_{\overline{\psi}_\alpha}$ | $\phantom{AA}\left( \gamma^\mu \psi  \right)_\alpha \, \iota_{\partial_\mu} dvol_\Sigma$ |

and to obtain the following non-trivial [[Poisson bracket Lie n-algebra|local Poisson brackets]] (prop. \ref{LocalPoissonBracket}) (the other possible brackets vanish):

$$
  \left\{
     \left( \gamma^\mu \psi  \right)_\alpha \, \iota_{\partial_\mu} dvol_\Sigma
     \,,\,
     \left(\overline{\psi}\gamma^\mu\right)^\beta\, \iota_{\partial_\mu} dvol_\Sigma
  \right\}
  \;=\;
  \left(\gamma^\mu\right)_\alpha{}^{\beta} \, \iota_{\partial_\mu} dvol_\Sigma
  \,.
$$

Notice the signs: Due to the odd-grading of the field coordinate function $\psi$,
its variational derivative $\delta \psi$ has bi-degree $(1,odd)$ and the
contraction operation $\iota_{\psi}$ has bi-degree $(-1,odd)$, so that commuting it
past $\overline{\psi}$ picks up _two_ minus signs, a "cohomological" sign due to the differential form
degrees, and a "supergeometric" one (def. \ref{DifferentialFormOnSuperCartesianSpaces}):

$$
  \iota_{\partial_\psi} \overline{\delta \psi} \cdots
  =
  (-1) (-1) \overline{\delta \psi} \,\iota_{\partial_\psi} \cdots
  \,.
$$

For the same reason, the [[Poisson bracket Lie n-algebra|local Poisson bracket]]
is a _[[super Lie algebra]]_ with _symmetric_ super Lie bracket:


$$
  \left\{
     \left( \gamma^\mu \psi  \right)_\alpha \, \iota_{\partial_\mu} dvol_\Sigma
     \,,\,
     \left(\overline{\psi}\gamma^\mu\right)^\beta\, \iota_{\partial_\mu} dvol_\Sigma
  \right\}
  \;=\;
  +
  \left\{
     \left(\overline{\psi}\gamma^\mu\right)^\beta\, \iota_{\partial_\mu} dvol_\Sigma
     \,,\,
     \left( \gamma^\mu \psi  \right)_\alpha \, \iota_{\partial_\mu} dvol_\Sigma
  \right\}
  \,.
$$

=--


$\,$

This concludes our discussion of general [[infinitesimal symmetries of a Lagrangian]]. We pick this up again in the discussion of
_[Gauge symmetries](#GaugeSymmetries)_ below. First, in the [next chapter](#Observables) we discuss
the concept of [[observables]] in [[field theory]].
