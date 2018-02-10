
$$
  \begin{aligned}
  \mathbf{L}
    & =
    \tfrac{1}{2}
    k_{\alpha \beta} 
    f^\alpha_{\mu \nu} 
    \tfrac{1}{2}
    \left(
      a^\alpha_{\nu,\mu}
      -
      a^\alpha_{\mu,\nu}
      +
      g \gamma^{\alpha}{}_{\beta' \gamma'}
      a^{\beta'}_{\mu} a^{\gamma'}_{\nu}
    \right)
    \tfrac{1}{2}
    \left(
      a^{\beta\nu,\mu}
      -
      a^{\beta \mu,\nu}
      +
      g \gamma^{\beta}{}_{\beta'' \gamma''}
      a^{\beta''}_{\mu} a^{\gamma''}_{\nu}
    \right)
    \,dvol_\Sigma
    \\
    & =
    \underset{
      \mathbf{L}_{\mathrm{free}}
    }{
    \underbrace{
    \tfrac{1}{2}
    k_{\alpha \beta} 
    f^\alpha_{\mu \nu} 
    \tfrac{1}{2}
    \left(
      a^\alpha_{\nu,\mu}
      -
      a^\alpha_{\mu,\nu}
    \right)
    \tfrac{1}{2}
    \left(
      a^{\beta\nu,\mu}
      -
      a^{\beta \mu,\nu}
    \right)
    \,dvol_\Sigma
    }
    }
    \\
    & \phantom{=}
    +
    \underset{
      \mathbf{L}_{int}
    }{
    \underbrace{
    g 
    \, 
    k_{\alpha \beta} 
    f^\alpha_{\mu \nu} 
    \tfrac{1}{2}
    \left(
      a^\alpha_{\nu,\mu}
      -
      a^\alpha_{\mu,\nu}
    \right)
    \tfrac{1}{2}
    \left(
      \gamma^{\beta}{}_{\beta'' \gamma''}
      a^{\beta''}_{\mu} a^{\gamma''}_{\nu}
    \right)
    \,dvol_\Sigma
    \;
    +
    \;
    g^2
    \,
    \tfrac{1}{2}
    k_{\alpha \beta} 
    f^\alpha_{\mu \nu} 
    \tfrac{1}{2}
    \left(
      \gamma^{\alpha}{}_{\beta' \gamma'}
      a^{\beta'}_{\mu} a^{\gamma'}_{\nu}
    \right)
    \tfrac{1}{2}
    \left(
      \gamma^{\beta}{}_{\beta'' \gamma''}
      a^{\beta''}_{\mu} a^{\gamma''}_{\nu}
    \right)
    \,dvol_\Sigma
    }
    }
    \\
  \end{aligned}
  \,,
$$



$$
  \begin{aligned}
  \mathbf{L}
    & =
    \tfrac{1}{2 g^2}
    k_{\alpha \beta} 
    f^\alpha_{\mu \nu} 
    \tfrac{1}{2}
    \left(
      \tilde a^\alpha_{\nu,\mu}
      -
      \tilde a^\alpha_{\mu,\nu}
      +
      \gamma^{\alpha}{}_{\beta' \gamma'}
      \tilde a^{\beta'}_{\mu} \tilde a^{\gamma'}_{\nu}
    \right)
    \tfrac{1}{2}
    \left(
      \tilde a^{\beta\nu,\mu}
      -
      \tilde a^{\beta \mu,\nu}
      +
      \gamma^{\beta}{}_{\beta'' \gamma''}
      \tilde a^{\beta''}_{\mu} \tilde a^{\gamma''}_{\nu}
    \right)
    \,dvol_\Sigma
  \end{aligned}
  \,,
$$



$$
  \frac{\delta}{\delta \phi}
  \Gamma(\phi)
  _{\vert \phi = \langle \mathbf{\Phi}_{int}\rangle}
  = 
  0
$$

$$
  \langle \mathbf{\Phi}_{int}\rangle
  =
  \frac{\delta}{\delta J} W(J)
$$

[[GravityVertexCorrectionsForQED.png:file]]

In conclusion this shows that a consistent choice of [[counterterms]] $\mathcal{Z}_\Lambda$ exists to produce
_some_ S-matrix $\mathcal{S} = \underset{\Lambda \to \infty }{\lim} (\mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda)$.
It just remains to see that for _every_ other S-matrix $\widetilde{\mathcal{S}}$ there exist counterterms
$\widetilde{\mathcal{Z}}_\lambda$ such 
that $\widetilde{\mathcal{S}} = \underset{\Lambda \to \infty }{\lim} (\mathcal{S}_\Lambda \circ \widetilde{\mathcal{Z}}_\Lambda)$.

But by the [[main theorem of perturbative renormalization]] (theorem \ref{PerturbativeRenormalizationMainTheorem}) 
we know that there exists a [[vertex redefinition]] $\mathcal{Z}$ such that 

$$
  \begin{aligned}
    \widetilde{\mathcal{S}} 
    & = \mathcal{S} \circ \mathcal{Z}
    \\
    & =
    \underset{\Lambda \to \infty}{\lim} 
    \left(
      \mathcal{S}_\Lambda \circ \mathcal{Z}_\Lambda
    \right)
    \circ
    \mathcal{Z}
    \\
    & = 
    \underset{\Lambda \to \infty}{\lim}
    (
      \mathcal{S}_\Lambda 
        \circ 
      (
        \underset{
          \widetilde{\mathcal{Z}}_\Lambda
        }{
        \underbrace{
        \mathcal{Z}_\Lambda
          \circ
        \mathcal{Z}
        }
        }
      )
    )
  \end{aligned}  
$$

and hence counterterms for any $\widetilde{\mathcal{S}}$ are given by the composite $\widetilde{\mathcal{Z}}_\Lambda \coloneqq \mathcal{Z}_\Lambda \circ \mathcal{Z}$.
