
+-- {: .num_cor #OnShellSpaceOfFieldHistoriesForFreeFieldTheoryGreenHyperbolic}
###### Corollary
**([[on-shell]] [[space of field histories]] for [[Green hyperbolic differential operrator|Green hyperbolic]] [[free field theories]])**

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
  }
  \,.
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
[[kernel]] $ker_{scp}(P)$ of $P$ equals the [[image]] $im(\mathrm{G}_{P})$. But by exactmness of the sequence
at $\Gamma_{\Sigma,cp}(E^\ast)$ it follows that $\mathrm{G}_P$ becomes [[injective]] on the [[quotient space]]
$\Gamma_{\Sigma,cp}(E)^\ast/im(P)$. Therefore on this quotient space it becomes an isomorphism onto its [[image]].

=--

+-- {: .num_reamrk #LinearOnShellObservablesAreTheGeneralizedPDESolutionsNaiveVersion}
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
the linear on-shell [[observables]] (def. \ref{LinearObservables}) are equivalently those linear off-shell observables which
are [[generalized solution of a PDE|generalized solutions]] of the [[formally adjoint differential operator|formally dual]]
[[equation of motion]] according to def. \ref{DistributionalDerivatives}.

That this remains true also for [[topological vector space]] [[structure]] follows with the dual exact sequence
(eq:GreenHyperbolicOperatorDualExactSequence). This is the statement of prop. \ref{DistributionsOnSolutionSpaceAreTheGeneralizedPDESolutions} below.

=--
