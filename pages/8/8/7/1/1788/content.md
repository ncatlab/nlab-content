
Let $\{p_{\rho_k}\}_{k \in \mathbb{N}}$ be a sequence of projection maps as in [this equation](renormalization#eq:ForExtensionOfDistributionsTestFunctionDecomposition) defining an [[Epstein-Glaser renormalization|Epstein-Glaser ("re"-)normalization]] of [[time-ordered products]] $\{T_k\}_{k \in \mathbb{N}}$ by the choice $q_k^\alpha = 0$ in [this equation](renormalization#eq:ExtensionOfDitstributionsPointFixedAndChoice).

This means that we may write the corresponding [[S-matrix]] as

$$
  \mathcal{S}
    \;=\;
  \underset{\Lambda \to \infty}{\lim}
   \left(
     \underset{k \in \mathbb{N}}{\sum}
     \frac{1}{k!}
     \frac{1}{(i \hbar^k)}
     \left(
       \underset{
         k \, \text{arguments}
       }{
       \underbrace{
         (-) \star_{F,\Lambda} \cdots \star_{F,\Lambda} (-) 
       }
       }
     \right) \circ p_{\rho_k}
   \right)
$$

because, as in the proof of [this prop.](renormalization#SpaceOfPointExtensions), with the projection $p_{\rho_k}$ included, the [[extension of distributions]] to the diagonal is unique.

By definition we have $Z_{0,\Lambda} = 0$ and $Z_{1,\Lambda} = id$. So assume $\{Z_{k,\Lambda}\}_{k \leq n}$ has been found for some $n \in \mathbb{N}$.

We may solve the required equation equivalently for the corresponding [[effective actions]] $S_{eff} = S_{eff,0,\infty}$ (using the notation rom [this def.](renormalization#EffectiveActionRelative)), given by the [[Feynman perturbation series]] over [[connected graphs]] (by [this prop.](renormalization#EffectiveActionAsRelativeEffectiveAction)), since that uniquelydetermines the genuine S-matrices by exponentiation with respect to the pointwise product via

$$
  \mathcal{S}(O) = \exp_\cdot( S_{eff,0,\infty}(O) )
  \phantom{AAA}
  \mathcal{S}_\Lambda(O) = \exp_\cdot( S_{eff,0,\Lambda}(O) )
$$

Hence for any [[local observable]] 

$$
  O
    \;\in\;
  LocObs(E_{\text{BV-BRST}})[ [ \hbar, g, j] ]\langle g, j\rangle
$$

the equation to be solved is

$$
  S_{eff,0,\infty}(O)
  \;=\;
  \underset{\Lambda \to \infty }{\lim}
  \mathcal{S}_{eff,0,\Lambda}
  \left(
    \mathcal{Z}_\Lambda(O)
  \right)
$$

By induction assumption may then, as before, write also the renormalized effective as a limit over $\Lambda$, now with the vertex redefinitions $\mathcal{Z}_{\leq n}$ included, if we still keep the $p_{\rho}$-projections:

$$
  S_{eff,0,\infty}
    \;=\;
  \underset{\Lambda \to \infty}{\lim}
  \underset{\Gamma\in \mathcal{G}_{conn}}{\sum}
  \Gamma_\Lambda \circ p_{\rho}
  \left(
    \mathcal{Z}_{\leq n}(-)
    ,
    \cdots
    ,
    \mathcal{Z}_{\leq n}(-)
  \right)
  \.-
$$

Here $\Gamma_\Lambda$ denotes the [[Feynman amplitude]] computed with $\star_{F,\Lambda}$.

By inserting a sum of observables $\underset{1 \leq i \leq {n+1}}{\sum} \kappa_i O_i$ and then differentiating at $\kappa_1, \cdots, \kappa_{n+1} = 0$ we may solve for $Z_{n+1,\Lambda}$:

$$
  \begin{aligned}
    Z_{n+1, \Lambda}(O_1, \cdots, O_{n+1})
    & =
    \underset{
      \Gamma \in \mathcal{G}_{conn}
    }{\sum} 
    \left(
      \Gamma_{\Lambda} \circ p_{\rho_{n+1}} 
      \left(
        \mathcal{Z}_{\leq n,\Lambda}(O_1), 
        \cdots, 
        \mathcal{Z}_{\leq n, \Lambda}(O_{n+1})
      \right)
      -
      \Gamma_{\Lambda}
      \left(
           \mathcal{Z}_{\leq n,\Lambda}(O_1), 
           \cdots, 
           \mathcal{Z}_{\leq n, \Lambda }(O_{n+1})
      \right)
    \right) 
    \\
    & = 
    \underset{
      \Gamma \in \mathcal{G}_{conn}
    }{\sum} 
    \Gamma_\Lambda \circ ( p_{\rho} - id  )
    \left(
       \mathcal{Z}_{\leq n,\Lambda}(O_1), 
       \cdots, 
       \mathcal{Z}_{\leq n, \Lambda }(O_{n+1})
    \right)    
  \end{aligned}
$$

For this to be consistent, we need to show that $Z_{n+1,\Lambda}$ thus defined is local. This follows since the difference


$$
  p_{\rho_{n+1}} - id
$$

vanishes on test functions ([[adiabatic switching]]) which are supported away from the diagonal, becuase by the fact that $p_\rho$ projects onto the space of functions that vanish at the diagonal, together with their partial derivatives, to some order, it is the identity on these functions.

