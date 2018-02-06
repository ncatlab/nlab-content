+-- {: .proof}
###### Proof

Let $\{p_{\rho_{n+1}}\}_{k \in \mathbb{N}}$ be a sequence of projection maps as in (eq:ForExtensionOfDistributionsProjectionMaps) defining an [[Epstein-Glaser renormalization|Epstein-Glaser ("re"-)normalization]] (prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal}) of [[time-ordered products]] $\{T_k\}_{k \in \mathbb{N}}$ as [[extensions of distributions]] of the $T_k$, regarded as distributions via remark \ref{TimeOrderedProductOfFixedInteraction}, by the choice $q_k^\alpha = 0$ in (eq:ExtensionOfDitstributionsPointFixedAndChoice).

We will construct that $\mathcal{Z}_\Lambda$ in terms of these projections $p_\rho$.

First consider some convenient shorthand:

For $n \in \mathbb{N}$, write $\mathcal{Z}_{\leq n} \coloneqq \underset{1 \in \{1, \cdots, n\}}{\sum} \frac{1}{n!} Z_n$.
Moreover, for $k \in \mathbb{N}$ write $(T_\Lambda \circ \mathcal{Z}_{\leq n})_k$ for the $k$-ary coefficient in the
expansion of the composite $\mathcal{S}_\Lambda \circ \mathcal{Z}_{\leq n}$,
as in equation (eq:MainTheoremPerturbativeRenormalizationInductionStep) in the proof of the [[main theorem of perturbative renormalization]] (prop. \ref{AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition}).

In this notation we need to find $\mathcal{Z}_\Lambda$ such that for each $n \in \mathbb{N}$ we have

$$
  \label{CountertermsInductionAssumption}
  \underset{\Lambda \to \infty}{\lim}
  \left(
    T_\Lambda \circ \mathcal{Z}_{\leq n, \Lambda}
  \right)_n
  \;=\;
  T_n
  \,.
$$

We proceed by [[induction]] over $n \in \mathbb{N}$.

Since by definition $T_0 = const_1$, $T_1 = id$ and  $Z_0 = const_0$, $Z_1 = id$ the statement is trivially true for 
$n = 0$ and $n = 1$.

So assume now that for $n \in \mathbb{N}$ that $\{Z_{k}\}_{k \leq n}$ has
been found such that (eq:CountertermsInductionAssumption) holds.

Observe that with the chosen renormalizing projection $p_{\rho_{n+1}}$ the time-ordered product $T_{n+1}$ may be expressed as follows:

$$
  \label{RenormalizedSMatrixAsLimitOfEffectiveSMatricesEvaluatedOnProjection}
  \begin{aligned}
  T_{n+1}(O, \cdots, O)
  & =
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      T_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F}
    \left(
      {\, \atop \,}
      T_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_k}(O \otimes \cdots \otimes O)
  \right\rangle
  \\
  & = 
  \left\langle
  \underset{\Lambda \to \infty}{\lim}
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      T_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      T_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_k}(O \otimes \cdots \otimes O)
  \right\rangle
  \end{aligned}
  \,.
$$

Here in the first step we inserted the decomposition (eq:TimeOrderedProductsAwayFromDiagonalByInduction) 
of $T_{n+1}$ in terms of the $\{T_k\}_{k \leq n}$
away from the diagonal, as in the proof of prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal},
which is admissible because the image of $p_{\rho_{n+1}}$ vanishes on the diagonal. In the second step
we replaced the star-product of the Feynman propagator $\Delta_F$ with the limit over the star-products
of the regularized propagators $\Delta_{F,\Lambda}$, which converges by the nature of the [[Hörmander topology]].

Hence it is sufficient to find $Z_{n+1,\Lambda}$ and $K_{n+1,\Lambda}$ such that we have

$$
  \label{CountertermsAndCorrectionTerm}
  \begin{aligned}
  \left\langle
    \left(
      T_{\Lambda} \circ \mathcal{Z}_{\Lambda}
    \right)_{n+1}
    \,,\,
    (-, \cdots, -)
  \right\rangle
  & =
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      T_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      T_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_{k}}\left( -, \cdots, - \right)
  \right\rangle
  \\
  & \phantom{=}
  +
  K_{k,\Lambda}(-, \cdots, -)
  \end{aligned}
$$

subject to these two conditions:

1. $\mathcal{Z}_\Lambda$ is [[local observable|local]];

1. $\underset{\Lambda \to \infty}{\lim} K_{\Lambda,k} = 0$.


Now by expanding out the left hand side of (eq:CountertermsAndCorrectionTerm) as

$$
  (T_\Lambda \circ \mathcal{Z}_\Lambda)_{n+1}
  \;=\;
  Z_{n+1,\Lambda}
    \;+\;
  (T_\Lambda \circ Z_{\leq n, \Lambda})_{n+1}
$$

(which uses the condition $T_1 = id$) we find the unique solution of (eq:CountertermsAndCorrectionTerm) for $Z_{n+1,\Lambda}$, in terms of the $\{Z_{\leq n,\Lambda}\}$
and $K_{n+1,\Lambda}$ (the latter still to be chosen) to be:

$$
  \label{CountertermOrderByOrderInTermsOfCorrectionTerm}
  \begin{aligned}
  \left\langle
    Z_{n+1,\Lambda}
    ,
    (-,\cdots, -)
  \right\rangle
  & =
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      T_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      T_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_{n+1}}(-, \cdots, -)
  \right\rangle
  \\
  & \phantom{=}
  -
  \left\langle
    \left(
      T_{\Lambda} \circ \mathcal{Z}_{\leq n,\Lambda}
    \right)_{n+1}
    \,,\,
    (-, \cdots, -)
  \right\rangle
  \\
  & \phantom{=}
  +
  \left\langle
    K_{n+1, \Lambda},
    (-, \cdots, -)
  \right\rangle
  \end{aligned}
  \,.
$$

We claim that the following choice works:

$$
  \label{LocalityCorrection}
  \begin{aligned}
  K_{n+1, \Lambda}(-, \cdots, -)
  & \coloneqq
  \left\langle
    \left(
      T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda}
    \right)_{n+1}
    \,,\,
    p_{\rho_{n+1}}(-, \cdots, -)
  \right\rangle
  \\
  & \phantom{=}
  -
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      T_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      T_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_{n+1}}(-, \cdots, -)
  \right\rangle
  \end{aligned}
  \,.
$$

To prove this, we need to show that 1) the resulting $Z_{n+1,\Lambda}$ is local and 2) the limit of $K_{n+1,\Lambda}$ vanishes as $\Lambda \to \infty$.

First regarding the locality of $Z_{n+1,\Lambda}$: By inserting (eq:LocalityCorrection) into (eq:CountertermOrderByOrderInTermsOfCorrectionTerm)
we obtain

$$
  \begin{aligned}
    \left\langle
      Z_{n+1,\Lambda}
      \,,\,
      (-,\cdots,-)
    \right\rangle
    & =
    \left\langle
      \left(
        T_{\Lambda} \circ \mathcal{Z}_{\leq n}
      \right)_{n+1}
      \,,\,
      p(-, \cdots, -)
    \right\rangle
    -
    \left\langle
      \left(
        T_{\Lambda} \circ \mathcal{Z}_{\leq n}
      \right)_{n+1}
      \,,\,
      (-, \cdots, -)
    \right\rangle
    \\
    & =
    \left\langle
      \left(
        T_{\Lambda} \circ \mathcal{Z}_{\leq n}
      \right)_{n+1}
      \,,\,
      ( p_{\rho_{n+1}} - id)(-, \cdots, -)
    \right\rangle
  \end{aligned}
$$

By definition $p_{\rho_{n+1}} - id$ is the identity on test functions (adiabatic switchings) that vanish at the diagonal. This means that $Z_{n+1,\Lambda}$ is [[support of a distribution|supported]] on the diagonal, and is hence local.

Second we need to show that $\underset{\Lambda \to \infty}{\lim} K_{n+1,\Lambda} = 0$:

By applying the analogous causal decomposition (eq:TimeOrderedProductsAwayFromDiagonalByInduction)
to the regularized products, we find

$$
  \label{InductionStepForCounterterms}
  \begin{aligned}
  &
  \left\langle
    (T_\Lambda \circ \mathcal{Z}_{\leq n, \Lambda})_{n+1}
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \\
  & =
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \,.
  \end{aligned}
$$

Using this we compute as follows:

$$
  \label{CorrectionTermForCountertermsVanishesAsCutoffIsRemoved}
  \begin{aligned}
  &
  \left\langle
    \underset{\Lambda \to \infty}{\lim}
    (T_\Lambda \circ \mathcal{Z}_{\leq n, \Lambda})_{n+1}
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \\
  & =
  \left\langle
    \underset{\Lambda \to \infty}{\lim}
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { \mathbf{I}, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \!\!\chi_i(\mathbf{X})\,
    \left(
      {\, \atop \,}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{{\vert \mathbf{I}\vert}} (\mathbf{I})
      {\, \atop \,}
    \right)
      \star_{F,\Lambda}
    \left(
      {\, \atop \,}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
      {\, \atop \,}
    \right)
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \\
  & =
  \left\langle
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { I, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \chi_i(\mathbf{X})\,
    \underset{
      T_{{\vert \mathbf{I}\vert}}(\mathbf{I})
    }{
    \underbrace{
    \left(
      \underset{\Lambda \to \infty}{\lim}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{{\vert \mathbf{I}\vert}} (\mathbf{I})
    \right)
    }}
      \star_{F,\Lambda}
    \underset{
      T_{{\vert \overline{\mathbf{I}}\vert}}(\overline{\mathbf{I}})
    }{
    \underbrace{
    \left(
      \underset{\Lambda \to \infty}{\lim}
      (T_{\Lambda} \circ \mathcal{Z}_{\leq n, \Lambda})_{ {\vert \overline{\mathbf{I}} \vert} } ( \overline{\mathbf{I}} )
    \right)
    }}
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \\
  & =
  \left\langle
    \underset{\Lambda \to \infty}{\lim}
    \underset{  {\mathbf{I} \in \{1, \cdots, n+1\} } \atop { I, \overline{\mathbf{I}} \neq \emptyset }  }{\sum}
    \chi_i(\mathbf{X})\,
    T_{ { \vert \mathbf{I} \vert } }( \mathbf{I} )
      \star_{F,\Lambda}
    T_{ {\vert  \overline{\mathbf{I}} \vert} }( \overline{\mathbf{I}} )
    \,,\,
    p_{\rho_{n+1}}(-,\cdots,-)
  \right\rangle
  \end{aligned}
  \,.
$$

Here in the first step we inserted (eq:InductionStepForCounterterms); in the second step we used that in the [[Hörmander topology]] the [[product of distributions]] preserves limits in each variable and under the braces we used the induction assumption (eq:CountertermsInductionAssumption)
and the definition of [[UV cutoff]] (def. \ref{CutoffsUVForPerturbativeQFT}); in the third step we used that by the causal nature of $\chi_i$ (eq:PartitionCausalOfUnityForComplementOfDiagonal) the two factors of the [[star product]] are in [[causal order]]
so that we may equivalently use the [[Wick algebra]]-product $\star_H$ (by [this prop.](Wick+algebra#CausalOrderingTimeOrderedProductOnRegular)); in the fourth step we applied (eq:TimeOrderedProductsAwayFromDiagonalByInduction); and finally we
rewrote as in (eq:RenormalizedSMatrixAsLimitOfEffectiveSMatricesEvaluatedOnProjection), for emphasis.

Inserting this for the left summand in (eq:LocalityCorrection) makes manifest that $\underset{\Lambda \to \infty}{\lim} K_{n+1, \Lambda} = 0$.

In conclusion this shows that a consistent choice of [[counterterms]] $\mathcal{Z}_\Lambda$ exists. To see that every [[S-matrix scheme]] arises this way from a choice of $\mathcal{Z}_\Lambda$ it is now sufficient, by the above proof, to see that every S-matrix scheme  comes from vanishing renormalization constants $q^\alpha_k$ in (eq:ExtensionOfDitstributionsPointFixedAndChoice) for _some_ sequence of projections $\{p_{\rho_k}\}_{k \in \mathbb{N}}$ (in the notation of the proof of prop. \ref{SpaceOfPointExtensions}). This is pretty clear...

=--
