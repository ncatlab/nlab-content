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
    \\
    \mathrm{d}\, \star_{{}_X} F_2 
     & = F_2 \wedge F_2
  \end{aligned}
\]

Consider then the [[dimensional reduction]] of this situation to 3D, specifically: The case that $Y^{1,4}$ is a [[product manifold]] (with product [[Riemannian metric|metric]])
\[
  \label{DimRedSpacetime}
  Y^{1,4}
  =
  X^{1,2} \times L^1 \times V^1
  \,,
\]
of

* a [[Lorentzian manifold]] $X^{1,2}$, $dim\big(Y^{1,2}\big) = 3$,

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

and that the [[flux density]] has decomposition

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
  $\ell_v \to 0$, the equations of motion (eq:EoMof5dMCSforDimReduction) become equivalent to 
  $$
    \begin{aligned}
      F_2^{(X X)} & = 0
      \\
      F_1^{(X l)} F_1^{(X v)}  & = 0
      \,,
      \;\;\;
      \mathrm{d} F_1^{(X l)} = 0
      \,,
      \mathrm{d} F_1^{(X v)} = 0 
      \mathrlap{\,,}
    \end{aligned}
  $$
  hence are those of 3D [[abelian Chern-Simons theory]] for $F_2^{(X X)}$.
\end{proposition}

--- wrong ---

\begin{proof}
Due to the product spacetime structure (eq:DimRedSpacetime), the Hodge dual of $F_2$ (eq:DimRedDecompositionOfFluxDensity) with respect to $Y^{1,4}$ is expressed in terms of the Hodge star operator $\star_{X}$ associated with $X^{1,2}$ as follows:
$$
  \begin{aligned}
  \star F_2
  =
  &
  \ell_l \ell_v
  \big(
    \star_X F_2^{(s s)} 
  \big)
  \wedge
  \mathrm{d}l
  \wedge
  \mathrm{d}v
  \\
  & +
  \tfrac{\ell_v}{\ell_l}
  \big(
    \star_X F_1^{(s l)}
  \big)
  \wedge
  \mathrm{d} v
  \\
  & -
  \tfrac{\ell_l}{\ell_v}
  \big(
    \star_X F_1^{(s v)}
  \big)
  \wedge
  \mathrm{d} l
  \\
  & + 
  \tfrac{1}{\ell_l \ell_v}
  \star_X F_0^{(l v)}
  \end{aligned}
$$
Here the first two summands vanish as $\ell_v \to 0$, and the last summand vanishes under the 5D differential $\mathrm{d} = \mathrm{d}_X + \mathrm{d}_l + \mathrm{d}_v$ ($\mathrm{d}_X$ vanishes by degree reasons and $\mathrm{d}_l, \mathrm{d}_v$ by (eq:DimRedDecompositionOfFluxDensity)). Therefore, the whole left hand side of the second EoM (eq:EoMof5dMCSforDimReduction) vanishes in the limit, whence the EoM becomes:
$$
  \begin{aligned}
    0
    & =
    F_2^{(X X)} F_1^{(X l)}
    \\
    0
    & =
    F_2^{(X X)} F_1^{(X v)}
    \\
    0 & =
    F_2^{(X X)} F_0^{(l v)}
    +
    F_1^{(X l)} F_1^{(X v)}
    \mathrlap{\,.}
  \end{aligned}
$$

Here the first two equations are jointly equivalent to 
$$
  \underset{x \in X}{\forall}
  \bigg(
    F_2^{(X X)}(x) = 0
    \;\;
    or
    \;\;
    \Big(
      F_1^{(X l)}(x) = 0
      \;\;
      and
      \;\;
      F_1^{(X v)}(x) = 0
    \Big)
  \bigg)
  \,.
$$
Finally, this together with the third equation, subject to (eq:DimRedFluxCompactification), is equivalent to the claim.
\end{proof}

