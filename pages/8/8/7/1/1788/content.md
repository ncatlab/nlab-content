> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

\linebreak



***


### Dimensional reduction of 5d Maxwell-Chern-Simons to 3D Chern-Simons

For $Y^{1,4}$ a [[Lorentzian manifold]], [[dimension of a manifold|$\mathrm{dim}\big(Y^{1,4}\big) = 5$]], with associated [[Hodge star operator]]
$$
  \star_{{}_Y} 
  \;\colon\;
  \Omega^\bullet_{dR}\big(
    Y^{1,4}
  \big)
  \longrightarrow
  \Omega^{5-\bullet}_{dR}\big(
    Y^{1,4}
  \big)
  \,,
$$

the [[equations of motion]] of [[5D Chern-Simons theory|5D Chern-Simons]]-[[Maxwell theory]] are
\[
  \label{EoMof5dMCSforDimReduction}
  \begin{aligned}
    \mathrm{d}\, F_2 & = 0 
    \mathrlap{\,,}
    \\
    \mathrm{d}\, \star_{{}_Y} F_2 
     & =
     \tfrac{1}{2} 
     F_2 \wedge F_2
    \mathrlap{\,.}
  \end{aligned}
\]

Consider the [[dimensional reduction]] of this situation to 3D, specifically: The case that $Y^{1,4}$ is a [[product manifold]] (with product [[Riemannian metric|metric]])
\[
  \label{DimRedSpacetime}
  Y^{1,4}
  =
  X^{1,2} \times L^1 \times V^1
  \,,
\]
of

* a [[Lorentzian manifold]] $X^{1,2}$, $dim\big(X^{1,2}\big) = 3$,

* 1-dimensional [[Riemannian manifolds]] $L^1$ and $V^1$

  which in suitable [[coordinates]] $l$ and $v$ have metrics
  $
    \begin{aligned}
      g_L & = \ell_l^2 \mathrm{d}l \otimes \mathrm{d}l
      \\
      g_V & = \ell_v^2 \mathrm{d}v \otimes \mathrm{d}v
    \end{aligned}
  $ 
  for [[positive number|positive]] [[real numbers]] $l,v \in \mathbb{R}_+$, respectively.

and that the [[flux density]] is constant along the fibers, in that

\[
  \label{DimRedDecompositionOfFluxDensity}
  \begin{aligned}
    F_2 
    = & 
    F_2^{(X X)} 
    \\
    & +
    F_1^{(X l)}
    \wedge
    \mathrm{d} l  
    \\
    & + 
    F_1^{(X v)}
    \wedge
    \mathrm{d} v  
    \\
    & +
    F^{(l v)}_0
    \mathrm{d}l
    \wedge
    \mathrm{d}v
  \end{aligned}
  \;\;\;\;\;
  \text{for}
  \;\;\;\;\;
  \left\{
  \begin{aligned}
    F_2^{(X X)}
    & 
    \in
    \Omega^2_{dR}\big(X^{1,2}\big)
    \xhookrightarrow{ p_X^\ast }
    \Omega^2_{dR}\big(Y^{1,4}\big)
    \\
    F_1^{(X l)}, 
    F_1^{(X v)}
    & 
    \in
    \Omega^1_{dR}\big(X^{1,2}\big)
    \xhookrightarrow{ p_X^\ast }
    \Omega^1_{dR}\big(Y^{1,4}\big)
    \\
    F_0^{(l v)}, 
    & 
    \in
    \Omega^0_{dR}\big(X^{1,2}\big)
    \xhookrightarrow{ p_X^\ast }
    \Omega^0_{dR}\big(Y^{1,4}\big)
  \end{aligned}
  \right.
\]
and such that 
\[
  \label{DimRedFluxCompactification}
  \underset{x \in X}{\forall} 
  \;
  F_0^{(l v)}(x) \neq 0
\]
(whence we have a *[[flux compactification]]*).

\begin{proposition}
  In this situation and in the [[limit of a sequence|limit]]
  $\ell_v \to 0$, the equations of motion (eq:EoMof5dMCSforDimReduction) are equivalent to the following system of equation:
$$
  \begin{aligned}
    &
    F_2^{(X X)}
    =
    - 
    \tfrac{1}{F_0^{(l v)}}
    F_1^{(X l)} \wedge F_1^{(X v)}
    \\
    &
    \mathrm{d}_X F_1^{(X v)} = 0,
    \;
    \mathrm{d}_X \star_X F_1^{(X v)} = 0,
    \\
    &
    \mathrm{d}_X F_1^{(X l)} = 0
    \mathrlap{\,.}
  \end{aligned}
$$
In particular, when either of the $F_1^{(X -)}$ vanishes, then $F_2^{(X X)}$ satisfies the equations of motion of 3D [[abelian Chern-Simons theory]], in the limit $\ell_v \to 0$.
\end{proposition}
\begin{proof}
Due to the product spacetime structure (eq:DimRedSpacetime), the Hodge dual of $F_2$ (eq:DimRedDecompositionOfFluxDensity) with respect to $Y^{1,4}$ is expressed in terms of the Hodge star operator $\star_{X}$ associated with $X^{1,2}$ as follows:
$$
  \begin{aligned}
  \star F_2
  =
  &
  \ell_l \ell_v
  \big(
    \star_X F_2^{(X X)} 
  \big)
  \wedge
  \mathrm{d}l
  \wedge
  \mathrm{d}v
  \\
  & +
  \tfrac{\ell_v}{\ell_l}
  \big(
    \star_X F_1^{(X l)}
  \big)
  \wedge
  \mathrm{d} v
  \\
  & -
  \tfrac{\ell_l}{\ell_v}
  \big(
    \star_X F_1^{(X v)}
  \big)
  \wedge
  \mathrm{d} l
  \\
  & + 
  \tfrac{1}{\ell_l \ell_v}
  \star_X F_0^{(l v)}
  \,,
  \end{aligned}
$$
whence the second equation of motion (eq:EoMof5dMCSforDimReduction) is seen to be equivalent to
\[
  \label{SecondEoMInKKComponents}
  \begin{aligned}
    \ell_l \ell_v
    \mathrm{d}_X
    \big(
      \star_X F_2^{(X X)} 
    \big)
    & =
    F_2^{(X X)} \wedge F_0^{(l v)}
    +
    F_1^{(X l)} \wedge F_1^{(X v)}
    \\
    \tfrac{\ell_v}{\ell_l}
    \mathrm{d}_X
    \big(
      \star_X F_1^{(X l)}
    \big)
    & =
    F_2^{(X X)} \wedge F_1^{(X v)}
    \\
    \tfrac{\ell_l}{\ell_v}
    \mathrm{d}_X
    \big(
      \star_X F_1^{(X v)}
    \big)
    & =
    - F_2^{(X X)} \wedge F_1^{(X l)}
    \\
    \tfrac{1}{\ell_l \ell_v}
    \underset{ = 0 }{
      \underbrace{
        \mathrm{d}_X
        \big(
          \star_X F_0^{(l v)}
        \big)
    }}
    & =
    \tfrac{1}{2}
    \underset{ =0 }{
    \underbrace{
      F_2^{(X X)} \wedge F_2^{(X X)}
    }}
    \mathrlap{\,,}
  \end{aligned}
\]
where the terms over the brace vanish by degree reasons.

In the limit $\ell_v \to 0$ the first equation in (eq:SecondEoMInKKComponents) goes to
$$
  \begin{aligned}
    F_2^{(X X)} 
    \to
    -
    \tfrac{1}{F_0^{(l v)}}
    F_1^{(X l)} \wedge F_1^{(X v)}
  \end{aligned}
$$
and thus implies the vanishing of the right hand sides of the second and third in (eq:SecondEoMInKKComponents), whence the only remaining condition expressed by (eq:SecondEoMInKKComponents) is
$$
  \mathrm{d}_X \big( \star_X F_1^{(X v)} \big)
  \to 0
  \,.
$$
Finally, the first equation of motion (eq:EoMof5dMCSforDimReduction) says that the component forms (eq:DimRedDecompositionOfFluxDensity) are closed. The closure of the 0-form component $F_0^{(l v)}$ means that it is locally constant, and the closure of $F_1^{(X -)}$ implies that of their wedge product $F_2^{(X X)}$. This completes the proof of the claim.
\end{proof}

