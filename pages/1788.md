
\begin{example}
  \label{CupSquareCohomologyOperation}
  [Cup-square cohomology operation]

Let $E$ be a [[multiplicative cohomology theory|multiplicative]] [[Whitehead-generalized cohomology theory]] [[Brown representability theorem|represented]] by a [[ring spectrum]]

$$
  \big(
    E, 1^E, m^E
  \big)
  \;\in\;
  CommutativeMonoids
  \Big(
    Ho\big( Spectra\big),
    \mathbb{S},
    \wedge
  \Big)
  \,.
$$

Then for all $n \in \mathbb{N}$ there is an unstable $E$-cohomology operation

\[
  \label{CupSquareAsUnstableCohomologyOperation}
  \big[
    \Omega^\infty \Sigma^n E
    \overset{
      (-)^{2_\cup}
    }{\longrightarrow}
    \Omega^\infty \Sigma^{k n} E
  \big]
  \;\;\in\;\;
  \widetilde E^{ 2 k }
  \big(
    \Omega^{\infty - n} E
  \big)
\]

defined -- via the [[Yoneda lemma]] on the [[opposite category|opposite]] of the [[classical homotopy category]] of [[pointed topological spaces]] -- by acting over any $X \,\in\, Ho\big(PointedTopologicalSpaces\big)$ as the [cup square on E-cohomology](cup+product#CupProductInWhiteheadGeneralizedCohomologyTheory) on cohomology in degree $n$:

\[
  \label{CupSquareInMultiplicativeCohomologyNaturalTransformation}
  X
  \;\;\mapsto\;\;
  \Big(
  [X, \Omega^\infty \Sigma^n E]
  \,=\,
  {\widetilde E}{}^n(X)
  \overset{
    \;\;
    \Delta_{{\widetilde E}{}^n(X)}
    \;\;
  }{\longrightarrow}
  {\widetilde E}{}^n(X)
  \times  
  {\widetilde E}{}^n(X)
  \overset{ \;\;  
    \cup^E 
  \;\; }{\longrightarrow}
  {\widetilde E}{}^n(X)
  \,=\,
  [X, \Omega^\infty \Sigma^{2n} E]
  \Big)
\]

Here the first [[function]] $\Delta_{{\widetilde E}{}^n(X)}$ is the [[diagonal morphism|diagonal]] on the _set_ underlying the degree=$n$ $E$-[[cohomology group]] of $X$, while the second function $\cup^E$ is the operation of forming the [[cup product]] of [[pairs]] of its elements.

Both of these operations are clearly [[natural transformations]] (for the first this is evident, for the second this comes down to the fact that the [smash-monoidal diagonals of suspension spectra](suspension+spectrum#SmashMonoidalDiagonals)) are natural, hence are [[monoidal category with diagonals|monoidal diagonals]]). Therefore the [[full subcategory|fully-faithfulness]] of the [[Yoneda embedding]] 

$$ 
  Ho
  \big(
    PointedTopologicalSpaces
  \big)^{op}
  \;\overset{ \;\; \;\; }{\hookrightarrow}\;
  Functors
  \Big(
    Ho
    \big(
      PointedTopologicalSpaces
    \big)^{op}
    ,
    Set
  \Big)
$$

implies that this natural transformation (eq:CupSquareInMultiplicativeCohomologyNaturalTransformation) between the [[representable functors]] $[-,\Omega^\infty \Sigma^n E]$ and $[-,\Omega^\infty \Sigma^{2n} E]$ is itself represented by a [[morphism]](eq:CupSquareAsUnstableCohomologyOperation) between the representing classifying spaces, hence by an unstable cohomology operation.

\end{example}



\begin{xymatrix}
  x = y
\end{xymatrix}

