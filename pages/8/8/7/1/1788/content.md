


$\,$

$\,$

$\,$

$\,$

$\,$


**[[local BRST complex|local]] [[off-shell]] [[BRST complex]]**
 {#BRSTComplex}

With the general concept of [[Lie algebra action]] (def. \ref{InfinitesimalActionByLieAlgebra}) and the corresponding [[action Lie algebroids]] (def. \ref{ActionLieAlgebroid}) and more general [[Lie ∞-algebroids]] in hand (def. \ref{LInfinityAlgebroid}})
we now apply this to the [[action]] of [[infinitesimal gauge symmetries]] (def. \ref{GaugeParameters}) on field histories of a [[Lagrangian field theory]], but we consider this _[[local field theory|locally]]_, namel on the [[jet bundle]]. The [[Chevalley-Eilenberg algebra]] of the resulting [[action Lie algebroid]] (def. \ref{ActionLieAlgebroid}) is known as the _[[local BRST complex|local]] [[BRST complex]]_, example \ref{LocalOffShellBRSTComplex} below.

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
**(local [[BRST complex]] and [[ghost fields]] for closed [[gauge parameters]])**

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

([Barnich-Brandt-Henneaux 94](local+BRST+cohomology#BarnichBrandtHenneaux94)).


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

+-- {: .num_example}
###### Example

For $\mathfrak{g}$ a [[semisimple Lie algebra]], consider the [[Lagrangian field theory]] of [[Yang-Mills theory]] on [[Minkowski spacetime]] from example \ref{YangMillsLagrangian}, with [[Lagrangian density]]

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

To see this, observe that the candidate BRST differential needs to be of the form (eq:OnMinkowskiInfinitesimalGaugeSymmetryForYangMills) plus the dual of the Lie bracket $[-,-]_{\mathcal{G}}^\ast$

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

We may equivalently make an Ansatz for $([-,-]_{\mathcal{G}})^\ast$ and if the resulting differential $s_{BRST}$ squares to zero, this defines the required closure bracket $[-,-]_\mathcal{G}$. 

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

Here first we expanded out, then in the second-but-last line we used the [[Jacobi identity]] and in the last line we just readjusted indices, for convenience of comparison with the next term. That next term is
 
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
$$

and thus is evidently cancels the first term.

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

This concludes our discussion of [[gauge symmetries]] as such. In the [next chapter](#ReducedPhaseSpace) we discuss
the [[homotopy quotient]] of the [[covariant phase space]] by the [[gauge symmetries]], called the _[[reduced phase space]]_.

