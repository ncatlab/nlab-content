+-- {: .proof}
###### Proof

Let $\{p_{\rho_k}\}_{k \in \mathbb{N}}$ be a sequence of projection maps as in [this equation](renormalization#) defining an [[Epstein-Glaser renormalization|Epstein-Glaser ("re"-)normalization]] (prop. \ref{RenormalizationIsInductivelyExtensionToDiagonal}) of [[time-ordered products]] $\{T_k\}_{k \in \mathbb{N}}$ as [[extensions of distributions]] of the $T_k$, regarded as distribution via remark \ref{TimeOrderedProductOfFixedInteraction}, by the choice $q_k^\alpha = 0$ in (eq:ExtensionOfDitstributionsPointFixedAndChoice).

By the proof of prop. \ref{SpaceOfPointExtensions} the extension of the time ordered products after the $p_\rho$-projections is unique, so that the actual S-matrix may be written as

$$
  \mathcal{S}(O)
  \;=\;
  \underset{\Lambda \to \infty}{\lim}
  \underset{k}{\sum}
  \frac{1}{k!} \frac{1}{(i \hbar)!}  
  \left\langle 
    T_{k,\Lambda} \,,\, p_{\rho_k} ( \underset{k \, \text{factors}}{\underbrace{O \otimes \cdots \otimes O} })
  \right\rangle
$$

where

$$
  \left\langle 
    T_{k,\Lambda}
    \,,\,
    O_1 \otimes \cdots \otimes O_k
  \right\rangle
  \;=\;
  O_1
    \star_{F,\Lambda}
    \cdots
    \star_{F,\Lambda}
  O_k
$$

is the effective time-ordered product at cutoff scale $\Lambda$ as in def. \ref{SMatrixEffective}, 
written as an evaluation of distributions on test functions.

With this it is now sufficient to find $\mathcal{Z}_\Lambda$ such that

$$
  \left\langle
    T_{k+1,\Lambda} \circ \mathcal{Z}_{\leq k+1, \Lambda}
    \,,\,
  \right\rangle
  \;=\;
  \left\langle
    T_{k+1, \Lambda} 
    \,,\, 
    p\left( - \right)
  \right\rangle
  \,,
$$

where on the left we mean the $(k+1)$-ary coefficient of $\mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda$, in the same way as in the proof of the [[main theorem of perturbative renormalization]] (prop. \ref{AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition}).

Further proceeding as in that proof, by [[induction]] over the arity of the time-ordered products, this implies that $Z_{n+1,\Lambda}$ is fixed to be

$$
  Z_{n+1,\Lambda}
  \;=\;
  \left\langle 
    T_{n+1,\Lambda} 
    \,,\,
    p(-)
  \right\rangle
  -
  \left\langle
    T_{n+1, \Lambda} \circ \mathcal{Z}_{\leq n}
    \,,\,
    -
  \right\rangle
  +
  K_\Lambda
  \,,
$$

where we have the freedom to choose $K_\Lambda$ such that

1. $\underset{\Lambda \to \infty}{\lim} K_\Lambda = 0$;

1. $Z_{n+1,\Lambda}$ is local.

Consider

$$
  K_\Lambda
  \;\coloneqq\;
  \left\langle
    T_{n+1,\Lambda} \circ \mathcal{Z}_{\leq n} 
    \,,\,
    p(-)
  \right\rangle
  -
  \left\langle
    T_{n+1,\Lambda} 
    \,,\,
    p(-)
  \right\rangle
$$

In fact $K_\Lambda = 0$ identically, since $p$ projects away from the diagonal, but a [[vertex redefinition]] $\mathcal{Z}_{\leq n}$ only acts non-trivially on the diagonal, by definition.

This way we get 

$$
  \begin{aligned}
    Z_{n+1,\Lambda}
    & =
    \left\langle
      T_{n+1,\Lambda} \circ \mathcal{Z}_{\leq n} 
      \,,\,
      p(-)
    \right\rangle
    -
    \left\langle
      T_{n+1, \Lambda} \circ \mathcal{Z}_{\leq n}
      \,,\,
      (-)
    \right\rangle
    \\
    & =
    \left\langle
      T_{n+1,\Lambda} \circ \mathcal{Z}_{\leq n} 
      \,,\,
      ( p - id)( -)
    \right\rangle
  \end{aligned}
$$

By by definition $p - id$ is the identity on test functions (adiabatic switchings) that vanish at the diagonal. This means that $Z_{n+1,\Lambda}$ is indeed local.

This shows that a consistent choice of $\mathcal{S}_\Lambda$ exists. To see that every [[S-matrix scheme]] arises this way from choice of $\mathcal{Z}_\Lambda$ it is now sufficient, by the above proof, to see that every S-matrix scheme  comes from vanishing renormalization constants $q^\alpha_k$ in (eq:ExtensionOfDitstributionsPointFixedAndChoice) for _some_ sequence of projections $\{p_{\rho_k}\}_{k \in \mathbb{N}}$ (in the notation of the proof of prop. \ref{SpaceOfPointExtensions}). This is pretty clear...

=--
