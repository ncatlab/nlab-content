
#Contents#
* table of contents
{:toc}

## Definition

Throughout, let 

1. $\Sigma$ be a [[smooth manifold]] of [[dimension]] $p+1$, thought of as [[spacetime]];

1. $E \overset{fb}{\longrightarrow} \Sigma$ a [[fiber bundle]] thought of as a _[[field bundle]]_

1. $\mathbf{L} \in \Omega^{p+1,0}_\Sigma(E)$ a [[Lagrangian density]].


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

1. an _[[infinitesimal symmetry of the Lagrangian]]_ is a variation $v$ (def. \ref{Variation})
   which arises as the prolongation $\hat v$ (prop. \ref{EvolutionaryVectorFieldProlongation})
   of  an [[evolutionary vector field]] $v$ (def. \ref{EvolutionaryVectorField}) such that the [[Lie derivative]] $\mathcal{L}_v$ of the Lagrangian density along $\hat v$ is a [[total derivative|total spacetime derivative]]

   $$
     \mathcal{L}_v \mathbf{L} = d \tilde J_v
   $$


1. an _[[on-shell]] [[conserved current]]_ is a horizontal $p$-form $J \in \Omega^{p,0}_\Sigma(E)$
   whose [[total derivative|total spacetime derivative]] vanishes on the prolonged [[shell]] (eq:ShellInJetBundle)

   $$
     d J\vert_{\mathcal{E}^\infty} = 0
     \,.
   $$

=--




+-- {: .num_prop #NoethersFirstTheorem}
###### Proposition
**([[Noether's theorem]] I)**

Let $(E,\mathbf{L})$ be a [[Lagrangian field theory]] (def. \ref{LocalLagrangianDensityOnSecondOrderJetBundleOfTrivialVectorBundleOverMinkowskiSpacetime}).

If $v$ is an [[infinitesimal symmetry of the Lagrangian]] (def. \ref{SymmetriesAndConservedCurrents})
with $\mathcal{L}_v \mathbf{L} = d \tilde J_v$, then

$$
  J_v \coloneqq \tilde J_v - \iota_v \Theta_{BFV}
$$

is an [[on-shell]] [[conserved current]] (def. \ref{SymmetriesAndConservedCurrents}), for $\Theta_{BFV}$
a presymplectic potential (eq:PresymplecticPotential) from def. \ref{EulerLagrangeOperatorForTivialVectorBundleOverMinkowskiSpacetime}.

=--

+-- {: .proof}
###### Proof

By [[Cartan's homotopy formula]] for the [[Lie derivative]] (prop. \ref{CartanHomotopyFormula})
and the decomposition of the variational derivative $\delta \mathbf{L}$ (eq:dLDecomposition)
and the fact that contraction $\iota_{\hat v}$ with the prolongtion of an evolutionary vector field vanishes on horizontal differential forms
(eq:GenericComponentsForProlongationOfEvolutionaryVectorField) and anti-commutes with the horizontal differential (eq:ProlongedEvolutionaryVectorFieldContractionAnticommutedWithHorizontalDerivative), by def. \ref{EvolutionaryVectorField},
we may re-express the defining equation for the symmetry as follows:

$$
  \begin{aligned}
    d \tilde J_v
    & =
    \mathcal{L}_v \mathbf{L}
    \\
    & =
    \iota_v \underset{= \delta_{EL}\mathbf{L} - d \Theta_{BFV}}{\underbrace{\mathbf{d} \mathbf{L}}}
    +
    \mathbf{d} \underset{= 0}{\underbrace{\iota_v \mathbf{L}}}
    \\
    & =
    \iota_v \delta_{EL} \mathbf{L}
    + d \iota_v \Theta_{BFV}
  \end{aligned}
$$

which is equivalent to

$$
  d(\underset{= J_v}{\underbrace{\tilde J_v - \iota_v \Theta_{BFV}}}) = \iota_v \delta_{EL}\mathbf{L}
$$

Since, by definition of the [[shell]] $\mathcal{E}$, the form $\frac{\delta_{EL} \mathbf{L}}{\delta v}$ vanishes on $\mathcal{E}$
this yields the claim.

=--


+-- {: .num_prop #FlowAlongImplicitInfinitesimalGaugeSymmetryPreservesOnShellSpaceofFieldHistories}
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
vanishing locus of the [[Euler-Lagrange form]] $\delta_{EL} \mathbf{L}$.

For this it is sufficient to show that the [[derivative]] of the components of the [[Euler-Lagrange form]] along $\hat v$ vanish on the [[prolonged shell]]

$$
  \hat v \left( \frac{\delta_{EL} L}{\delta \phi^a} \right)
  \;=\;
  0
  \phantom{AA}
  on \mathcal{E}^\infty \hookrightarrow J^\infty_\Sigma(E)
  \,.
$$

This is the statement of [Olver 95, theorem 5.53](#Olver95).

=--


## References

* {#Olver95} [[Peter Olver]], _Applications of Lie groups to differential equations_, Springer; _Equivalence, invariants, and symmetry_, Cambridge Univ. Press 1995.



[[!redirects symmetries of a Lagrangian density]]


[[!redirects symmetry of the Lagrangian density]]
[[!redirects symmetries of the Lagrangian density]]

[[!redirects symmetry of a Lagrangian]]
[[!redirects symmetries of a Lagrangian]]

[[!redirects symmetry of the Lagrangian]]
[[!redirects symmetries of the Lagrangian]]



[[!redirects infinitesimal symmetry of a Lagrangian density]]
[[!redirects infinitesimal symmetries of a Lagrangian density]]


[[!redirects infinitesimal symmetry of the Lagrangian density]]
[[!redirects infinitesimal symmetries of the Lagrangian density]]

[[!redirects infinitesimal symmetry of a Lagrangian]]
[[!redirects infinitesimal symmetries of a Lagrangian]]

[[!redirects infinitesimal symmetry of the Lagrangian]]
[[!redirects infinitesimal symmetries of the Lagrangian]]

[[!redirects infinitesimal symmetries of Lagrangians]]
