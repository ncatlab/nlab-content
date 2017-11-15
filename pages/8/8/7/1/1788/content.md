Let $\Gamma_\Sigma(E) \overset{P}{\longrightarrow} \Gamma_\Sigma(E^\ast)$ be a [[Green hyperbolic differential operator]] (def. \ref{GreenHyperbolicDifferentialOperator}) with [[causal Green function]] $\mathrm{G}$ (def. \ref{GreenHyperbolicDifferentialOperator}). Then the sequences

$$
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

Under passing to [[dual spaces]] and using the isomorphisms of spaces of distributional sections (def. \ref{DistributionalSections}) from prop. \ref{DistributionsWithCausalSupports} this yields the following dual [[exact sequence]] of [[topological vector spaces]] and continuous [[linear map]] between them:

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
