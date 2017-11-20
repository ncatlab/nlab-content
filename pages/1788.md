

+-- {: .num_defn #RegularLinearFieldObservables}
###### Definition
**(regular linear field observables and [[operator-valued distribution|observable-valued distributions]])**

Let $(E,\mathbf{L})$ be a [[free field theory|free]] [[Lagrangian field theory]] (def. \ref{FreeFieldTheory}) whose [[Euler-Lagrange equation|Euler-Lagrange]] [[equations of motion]] (prop. \ref{EulerLagrangeFormIsSectionOfLocalCotangentBundleOfJetBundleGaugeActionLieAlgebroid}) is [[Green hyperbolic differential equation|Green hyperbolic]] (def. \ref{GreenHyperbolicDifferentialOperator}).

Define the _regular_ linear field observables among the linear on-shell observables (def. \ref{LinearObservables}) to be the [[non-singular distributions]] on the [[on-shell]] [[space of field histories]], hence the [[image]] 

$$
  LinObs(E_{scp},\mathbf{L})
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
      \underset{\Sigma}{\int} \alpha^\ast_a(x) \cdot \Phi^a(x)
       \, dvol_\Sigma(x)
    \right)
  }
$$

By lemma \ref{ExactSequenceOfGreenHyperbolicSystem} every $\Phi \in \Gamma_{\Sigma,scp}(E)$ is in the image of $\mathrm{G}$ and by example \ref{CausalGreenFunctionOfFormallyAdjointDifferentialOperatorAreFormallyAdjoint} this implies that the [[kernel]] of this map is the [[image]] of $P \;\colon\; \Gamma_{\Sigma,cp}(E) \to \Gamma_{\Sigma,cp}(E^\ast)$:

$$
  LinObs(E_{scp},\mathbf{L})^{reg}
   \;\simeq\;
  \Gamma_{\Sigma,scp}(E^\ast)/im(P)
  \,.
$$

The point-evaluation field observables $\mathbf{\Psi}^a(x)$ (example \ref{PointEvaluationObservables}) are linear observables (example \ref{LinearPointEvaluationObservables}) but far from being regular (eq:RegularLinearObservables) 
(except in [[spacetime]] [[dimension]] $p +1 = 0+1$). But the regular observables are precisely the 
averages ("smearings") of these point evaluation observables against compactly supported weights.

Viewed this way, the defining inclusion of the regular linear observables (eq:RegularLinearObservables) is itself 
an _[[operator-valued distribution|observable valued distribution]]_

$$
  \label{AverageOfFieldObservableIsRegularLinearObservables}
  \array{
    \mathbf{\Phi} &\colon& \Gamma_{\Sigma,cp}(E^\ast) &\hookrightarrow& LinObs(E,\mathbf{L})
    \\
    && \alpha^\ast &\mapsto& \underset{\Sigma}{\int} \alpha^\ast_a(x) \mathbf{\Phi}^a(x)\, dvol_\Sigma(x)
  }
$$

which to a "smearing function" $\alpha^\ast$ assigns the observable which is the field observable smeared by (i.e. averaged against)
that smearing function.

Below in _[Free quantum fields](#FreeQuantumFields)_ we discuss how the [[polynomial Poisson algebra]] of regular polynomial observables of a [[free field theory]] may be [[deformation quantization|deformed]] to a [[non-commutative algebra|non-commutative]] [[algebra of quantum observables]]. Often this may be [[representation|represented]] by [[linear operators]] acting on some [[Hilbert space]].
In this case then $\mathbf{\Phi}$ above becomes a [[continuous linear functional]] from $\Gamma_{\Sigma,cp}(E)$ to a space of
linear operators on some Hilbert space. As such it is then called an _[[operator-valued distribution]]_.

=--

+-- {: .num_remark #ObservableValuedDistributions}
###### Remark
**(regular linear field observables are [[operator-valued distribution|observable-valued distributions]])**




While the point-evaluation field observables $\mathbf{\Phi}^a(x)$ are not themselves regular observables, 
the [[Peierls-Poisson bracket]] (eq:CausalPropagatorPPeierlsBracket) is clearly induced from the
following distributional bracket between them

$$
  \left\{
    \mathbf{\Phi}^a(x)
    ,
    \mathbf{\Phi}^b(y)
  \right\}
  \;=\;
  \Delta^{a b}(x,y)
$$

with the [[causal propagator]] (eq:CausalPropagator) on the right, in that then with the identification (eq:AverageOfFieldObservableIsRegularLinearObservables) the [[Peierls-Poisson bracket]] on 
regular linear observables arises as follows:

$$
  \begin{aligned}
    \left\{
      \underset{\Sigma}{\int} \alpha^\ast_a(x) \mathbf{\Phi}^a(x) \, dvol_\Sigma(x)
      \,,\,
      \underset{\Sigma}{\int} \beta^\ast_b(y) \mathbf{\Phi}^b(y) \, dvol_\Sigma(y)
    \right\}
    & =
    \underset{\Sigma}{\int} \underset{\Sigma}{\int}
      \alpha^\ast_a(x) 
      \underset{= \Delta^{a b}(x,y)}{
      \underbrace{
      \left\{
        \mathbf{\Phi}^a(x),
        \mathbf{\Phi}^b(y)
      \right\}
      }
      }
      \beta^\ast_b(y)
      \, dvol_\Sigma(x)\, dvol_\Sigma(y)
    \\
    & =
    \underset{\Sigma}{\int} \underset{\Sigma}{\int}
      \alpha^\ast_a(x)
      \Delta^{a b}(x,y)
      \beta^\ast_b(y)
      \, dvol_\Sigma(x)\, dvol_\Sigma(y)
  \end{aligned}
$$

=--
