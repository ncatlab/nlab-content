
claim

Let $\mathcal{S}$ be any [[S-matrix]] [[renormalization scheme]] and let $g S_{int} + j A \in LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g,j\rangle$ a polynomial [[local observable]], regarded as an [[adiabatic switching|adiabatically switched]] [[interaction]] [[action functional]].

Let moreover $\{\Delta_{F,\Lambda}\}_{\Lambda \in [0,\infty)}$ be a [[UV cutoff]]; with $\mathcal{S}_\Lambda$ the induced [[effective S-matrix schemes]] ([this def.](effective+quantum+field+theory#EffectiveSMatrixScheme)).


Then there exist [[vertex redefinitions]] $\{\mathcal{Z}_\Lambda\}_{\Lambda \in [0,\infty)}$ such that the [[limit of a sequence|limit]] of $\mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda$ exists and coincides $\mathcal{S}$:

$$
  \underset{\Lambda \to \infty}{\lim} 
  \mathcal{S}_{\Lambda} \circ \mathcal{Z}_\Lambda (g S_{int} + j A)
  \;=\;
  \mathcal{S}(g S_{int} + j A )
$$

+-- {: .proof}
###### Proof


Let $\{p_{\rho_k}\}_{k \in \mathbb{N}}$ be a sequence of projection maps as in [this equation](renormalization#eq:ForExtensionOfDistributionsTestFunctionDecomposition) defining an [[Epstein-Glaser renormalization|Epstein-Glaser ("re"-)normalization]] ([this prop.](renormalization#RenormalizationIsInductivelyExtensionToDiagonal)) of [[time-ordered products]] $\{T_k\}_{k \in \mathbb{N}}$ as [[extensions of distributions]] of the $T_k$ regarded as distribution via [this remark](renormalization#TimeOrderedProductOfFixedInteraction) by the choice $q_k^\alpha = 0$ in [this equation](renormalization#eq:ExtensionOfDitstributionsPointFixedAndChoice).

By the proof of [that prop.](renormalization#SpaceOfPointExtensions) the extension of the time ordered products after the $p_\rho$-projections is unique, so that the actual S-matrix may be written as

$$
  \mathcal{S}(O)
  \;=\;
  \underset{\Lambda \to \infty}{\lim}
  \underset{k}{\sum}
  \frac{1}{k!} \frac{1}{(i \hbar)!}
  {T_{k,\Lambda}} \circ p_{\rho_k} ( \underset{k \, \text{factors}}{\underbrace{O \otimes \cdots \otimes O} })
$$

where 

$$
  T_{k,\Lambda}(O_1, \cdots, O_k)
  \;=\;
  O_1 
    \star_{F,\Lambda}
    \cdots
    \star_{F,\Lambda}
  O_k
$$

is the effective time-ordered product at cutoff scale $\Lambda$ as in [this def.](renormalization#SMatrixEffective).

With this it is now sufficient to find $\mathcal{Z}_\Lambda$ such that

$$
  T_{k+1,\Lambda} \circ \mathcal{Z}_{\leq k+1, \Lambda}
  \;=\;
  T_{k+1, \Lambda} \circ p
  \,,
$$

where on the left we mean the $(k+1)$-ary coefficient of $\mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda$, in the same way as in the proof of the [[main theorem of perturbative renormalization]] ([this prop.](Stückelberg-Petermann+renormalization+group#AnyTwoSMatrixRenormalizationSchemesDifferByAUniqueVertexRedefinition)).

Further proceeding as in that proof, by [[induction]] over the arity of the time-ordered products, this implies that $Z_{n+1,\Lambda}$ is fixed to be

$$
  Z_{n+1,\Lambda}
  \;=\;
  T_{n+1,\Lambda} \circ p 
  -
  T_{n+1, \Lambda} \circ \mathcal{Z}_{\leq n}
  +
  K_\Lambda
$$

where we need to choose $K_\Lambda$ such that

1. $\underset{\Lambda \to \infty}{\lim} K_\Lambda = 0$;

1. $Z_{n+1,\Lambda}$ is local.

Consider

$$
  K_\Lambda
  \;\coloneqq\;
  T_{n+1,\Lambda} \circ \mathcal{Z}_{\leq n} \circ p
  -
  T_{n+1,\Lambda} \circ p
$$

In fact $K_\Lambda = 0$ independent of $\Lambda$, since $p$ projects away from the diagonal, but a vertex redefinition $\mathcal{Z}_{\leq n}$ only acts non-trivially on the diagonal, by definition.

Hence we may take

$$
  \begin{aligned}
    Z_{n+1,\Lambda}
    & =
    T_{n+1,\Lambda} \circ \mathcal{Z}_{\leq n} \circ p 
    -
    T_{n+1, \Lambda} \circ \mathcal{Z}_{\leq n}
    \\
    & =
    T_{n+1,\Lambda} \circ \mathcal{Z}_{\leq n} \circ ( p - id)
  \end{aligned}
$$

By by definition $p - id$ is the identity on test functions (adiabatic switchings) that vanish at the diagonal. This means that $Z_{n+1,\Lambda}$ is indeed local.

=--

