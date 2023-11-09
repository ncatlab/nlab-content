
\begin{remark}\label{HermitianFormsViaHermitianMetrics}
**(Hermitian forms via Hermitian metrics)**
\linebreak
The decomposition of a Hermitian form into its [[real part]] and [[imaginary part]] is traditionally written with the symbols
$$
  \langle-\vert-\rangle
  \;=\;
  g(-,-)
  +
  \mathrm{i} \omega(-,-)
$$
or similar, where
$$
  g(-,-)
  \;\coloneqq\;
  \Re \langle-\vert-\rangle
  \,,
$$
$$
  \omega(-,-)
  \;\coloneqq\;
  \Im \langle-\vert-\rangle
  \,.
$$
are real [[bilinear forms]] on the [[underlying]] [[real vector space]].

In fact, the real part fully determines the imaginary part and hence the Hermitian form:
$$
  \begin{array}{l}
    \omega(-,-)
    & =
    \Im \langle-\vert-\rangle
    \\
    & = 
    \Re \big(-\mathrm{i} \langle-\vert-\rangle\big)
    \\
    & =
    \Re \langle \mathrm{i} - \vert - \rangle
    \\
    & =
    \Re \langle J(-) \vert - \rangle
    \\
    & =
    g\big(J(-), -\big)
    \,,
  \end{array}
$$
where in the last line we introduced the [[complex structure]] $J$ on the [[underlying]] real vector space which promotes it back to the original complex vector space.

Notice that the complex structure $J$ is an [[orthogonal map]] with respect to the inner product $g$, equivalently $g$ is a [[Hermitian metric]] with respect to $J$, in that

$$
  \begin{array}{l}
    g\big(J(-), J(-)\big)
    \\
    \;=\;
    \Re 
    \big\langle 
      \mathrm{i}(-) 
    \big\vert 
      \mathrm{i}(-) 
    \big\rangle
    \\
    \;=\;
    \Re 
    \big(
      -\mathrm{i} \cdot \mathrm{i}
      \langle - \vert - \rangle
    \big)
    \\
    \;=\;
    \Re 
      \langle - \vert - \rangle
    \\
    \;=\;
    g(-,-)
    \,.
  \end{array}
$$ 

Conversely, for a real vector space equipped with a [[complex structure]] $J$ and a [[Hermitian metric]] $g$, in that $g\big(J(-), J(-)\big) \,=\, g(-,-,)$, the formula
$$
  \langle-\vert-\rangle
  \;=\;
  g(-,-)
  +
  \mathrm{i} 
  g\big(J(-), -\big)
$$
defines a Hermitian form on the corresponding complex vector space:

The linearity in the second argument is clear. The [[anti-linear map|antilinearity]] in the first argument follows by:
$$
  \begin{array}{l}
    g(\mathrm{i}-,-)
    +
    \mathrm{i} 
    g\big(J(\mathrm{i}-), -\big)
    \\
    \;=\;
    g\big(J(-),-\big)
    +
    \mathrm{i} 
    g\big(J\circ J (-), - \big)
    \\
    \;=\;
    g\big(J(-),-\big)
    -
    \mathrm{i} 
    g\big(-, - \big)
    \\
    \;=\;
    -\mathrm{i}
    \Big(
      g(-,-)
      +
      \mathrm{i} g\big( J(-), - \big)
    \Big)
    \,.
  \end{array}
$$
and Hermiticity follows by:
$$
  \begin{array}{l}
    g(w,v) 
      + 
    \mathrm{i}
    g\big( J(w), v \big)
    \\
    \;=\;
    g(w,v) 
      + 
    \mathrm{i}
    g\big( J \circ J(w), J(v) \big)
    \\
    \;=\;
    g(w,v) 
      - 
    \mathrm{i}
    g\big( w, J(v) \big)
    \\
    \;=\;
    g(v,w) 
      - 
    \mathrm{i}
    g\big( J(v),  w\big)
    \,.
  \end{array}
$$
\end{remark}

\begin{proposition}
Let $\mathscr{V}$ be a [[real vector space]] equipped with a [[complex structure]] 
$$
  J \,\colon\, \mathscr{V} \to \mathscr{V}
$$
and a [[Hermitian metric]] 
$$
  g 
    \,\colon\, 
  \mathscr{V} \otimes \mathscr{V}
  \longrightarrow 
  \mathbb{R}
  \,.
$$
Then the corresponding Hermitian form (via Rem. \ref{HermitianFormsViaHermitianMetrics}) is the [[underlying]] map of the image of this structure under the equivalence of real vector space with Real vector bundles over the point:
$$
  \array{
    \mathbb{R}Vect
    &\overset{\; \sim \;}{\longrightarrow}&
    RealVectBund_{\ast}
    \\
    (g,J) 
      &\mapsto& 
    \big(
      \langle-\vert-\rangle
      ,
      \mathrm{I}
    \big)
  }
$$ 
\end{proposition}
\begin{proof}
  If we write $\mathscr{V}_J$ for the complex vector space determined by $\mathscr{V}$ and $J$, then the equivalence sends
$$
  (\mathscr{V}, J)
  \;\mapsto\;
  \mathscr{V}_J \oplus \mathscr{V}_{-J}
  \,,
$$
where the right hand side is a Real vector space via the antilinear involution which on underlying real spaces is the swapping of the two summands. On this, the complex structure is
$$
  I 
  \;=\;
  diag(\mathrm{i}, -\mathrm{i})
  \,.
$$
Therefore the Hermiticity of $g$ on the left becomes on the right the condition that the $\mathbb{Z}/2 \curvearrowright \mathbb{C}$-bilinear pairing
$$
  \big(
    \mathscr{V}_J \oplus \mathscr{V}_{-J}
  \big)
  \otimes
  \big(
    \mathscr{V}_J \oplus \mathscr{V}_{-J}
  \big)
  \longrightarrow
  \mathbb{C}
$$
is non-trivial only on the mixed terms
$$
  \mathscr{V}_J \otimes \mathscr{V}_{-J}
  \;\;\oplus\;\;
  \mathscr{V}_{-J} \otimes \mathscr{V}_{J}
  \longrightarrow
  \mathbb{C}
  \,,
$$
where $\mathbb{Z}/2$-equivariance says that this is determined already by its value on one of the two summands, where it must be a Hermitian form.

This implies now that on the $\mathbb{Z}/2$-fixed locus
$$
  \mathscr{V}
  \otimes
  \mathscr{V}
  \;\simeq\;
  \Big(
  \big(
    \mathscr{V}_J \oplus \mathscr{V}_{-J}
  \big)
  \otimes
  \big(
    \mathscr{V}_J \oplus \mathscr{V}_{-J}
  \big)
  \Big)^{\mathbb{Z}/2}
$$
it coincides with $g(-,-)$. 

From this, the claim follows by Rem. \ref{HermitianFormsViaHermitianMetrics}.
\end{proof}

***

Let $X$ be a [[compact Hausdorff space]]. By a [[vector bundle]] (over $X$) we mean a [[topological vector bundle|topological]] [[complex vector bundle]].

Let $X$ be equipped with an [[involution]] $\sigma \,\colon\, X \to X$ (a [[homeomorphism]] such that $\sigma \circ \sigma = Id_X$ is the [[identity function]]).

\begin{definition}
\label{SigmaQuadraticFormOnComplexVectorBundle}
A *$\sigma$-[[quadratic form]]* on a topological complex vector bundle $\mathscr{V}$ over $X$ is:

* a morphism of complex topological bundles from the [[tensor product of vector bundles|tensor product]] of $\mathscr{V}$ with the [[pullback bundle|pullback]] of itself along $\sigma$ to the [[trivial bundle|trivial]] [[complex line bundle]]:

  $$
    g
    \,\colon\,
    \mathscr{V}
    \otimes
    \sigma^\ast \mathscr{V}
    \longrightarrow
    \underline{\mathbb{C}}
  $$

> (notice that [[fiber]]-wise this is a [[bilinear map]], *not* a [[sesquilinear map]])

such that:

1. $g$ is non-degenerate, in that its [[adjunct]] is an [[isomorphism]]

   $$
      \begin{array}{ccl}
       \mathscr{V} 
       &
       \overset{ \sim }{\longrightarrow}
       &
       \big(\sigma^\ast \mathscr{V}\big)^\ast
       \\
       v 
         &\mapsto& 
      \big(v' \mapsto g(v, v')
      \big)
     \end{array}
   $$

1. $g$ is $\sigma$-symmetric, in that

   $$
    \left.
     \begin{array}{l}
     v_1 
       \,\in\, 
     \mathscr{V}_x \,=\, (\sigma^\ast \mathscr{V})_{\sigma(x)}
     \\
     v_2 
       \,\in\, 
     (\sigma^\ast \mathscr{V})_{x} \,=\, \mathscr{V}_{\sigma(x)}
     \end{array}
     \right\}
     \;\;\;\;\;\;
     \vdash
     \;\;\;\;\;\;
     g_x(v_1, v_2)
     \;=\;
     g_{\sigma(x)}(v_2, v_1)
   $$

A [[homomorphism]] of such vector bundles with $\sigma$-quadratic form is a morphism of the underling topological complex vector bundles $f \,\colon\, \mathscr{V} \to \mathscr{V}$ over $X$, which is an [[isometry]] in that $g'\big(f(-),f(-)\big) = g(-,-)$.
\end{definition}

Write 
$$
  QVect_{\mathbb{C}}(X,\sigma)
$$ 
for the resulting [[category]].

The [[direct sum of vector bundles|direct sum of]] [[underlying]] vector bundles with $\sigma$-quadratic form (Def. \ref{SigmaQuadraticFormOnComplexVectorBundle}) inherits a $\sigma$-quadratic form in the evident summand-wise way. This operation makes the set of [[isomorphism classes]] into a [[commutative monoid]]:
\[
  \label{MonoidOfSigmaQuadraticComplexVectorBundles}
  \big(
    QVect_{\mathbb{C}}(X,\sigma)_{/\sim}, 
    \oplus
  \big)
  \;\;\;
    \in
  \;\;\;
  CMnd.
\]

\begin{definition}\label{TopologicalHermitianKTheoryDueToCrabb}
  The [[group completion]] of the monoid (eq:MonoidOfSigmaQuadraticComplexVectorBundles) is the $\mathbb{Z}/2$-equivariant Hermtian K-theory of $(X, \sigma)$:
$$
  KH(X, \sigma)
  \;\;
  \coloneqq
  \;\;
  G
  \big(
    QVect_{\mathbb{C}}(X,\sigma)_{/\sim}, 
    \oplus
  \big)
  \,.
$$
\end{definition}

\begin{example}
**([[hyperbolic functor]])**
For $\mathscr{V}$ an ordinary complex topological vector bundle over $X$, the [[direct sum of vector bundles|direct sum]] with the [[dual vector bundle|dual]] of its [[pullback bundle|pullback]] along $\sigma$
$$
  \mathscr{V}
  \,\mapsto\,
  \mathscr{V}
  \otimes
  (\sigma^\ast\mathscr{V})^\ast
$$
is canonically self-$\sigma$-dual
$$
  \array{
    \sigma^\ast
    \Big(
      \mathscr{V}
      \otimes
      (\sigma^\ast\mathscr{V})^\ast
    \Big)^\ast
    &\simeq&
      \mathscr{V}
      \otimes
      (\sigma^\ast\mathscr{V})^\ast
  }
$$
and carries a canonical $\sigma$-quadratic form (Def. \ref{SigmaQuadraticFormOnComplexVectorBundle}), given componentwise by the [[evaluation map]] $ev \,\colon\,\mathscr{V} \otimes \mathscr{V}^\ast \to \underline{\mathbb{C}}$.

This construction extends to an [[additive functor]] from the [[core groupoid]] of [[VectBund|$Vect_{\mathbb{C}}(X)$]] to $QVect_{\mathbb{C}}(X,\sigma)$, called the *[[hyperbolic functor]]*, and hence define a [[group homomorphism]] from the ordinary [[topological K-theory]]-group of $X$ to its topological Hermtian K-theory (eq:TopologicalHermitianKTheoryDueToCrabb):
$$
  K(X) \to KH(X,\sigma)
  \,.
$$
\end{example}

\begin{proposition}
  There is an isomorphism
$$
  KH(X,\sigma)
  \,\simeq\,
  KR(X,\sigma)
$$
between the $\mathbb{Z}/2$-equivariant topological Hermitian K-theory of Def. \ref{TopologicalHermitianKTheoryDueToCrabb} and the [[KR-theory]] of the [[real space]] $(X,\sigma)$.
\end{proposition}
\begin{proof}
To define a comparison map
$$
  KH(X,\sigma)
  \longrightarrow
  KR(X,\sigma)
$$  
given any representative $(\mathscr{V}, g)$, we may *choose* (see [here](inner+product+on+vector+bundles#ExistenceOfInnerProductOfTopologicalVectorBundlesOverParacompactHausdorffSpaces)) a [[Hermitian form|Hermitian]] [[inner product of vector bundles]]
$$
  \langle \cdot \vert \cdot \rangle
  \;\colon\;
  \mathscr{V} \otimes \mathscr{V}
  \to 
  \underline{\mathbb{C}}
  \,.
$$

Now since both $g(-,-)$ and $\langle-\vert-\rangle$ are non-degenerate, with adjunct [[bijections]]
$$
  \tilde g 
    \,\colon\,
  \mathscr{V}
  \to 
  (\sigma^\ast\mathscr{V})^\ast
  \,,
  \;\;\;\;\;\;
  \tilde h 
    \,\colon\,
  \mathscr{V}
  \to 
  \mathscr{V}^\ast
  \,,
$$
we obtain an [[anti-linear map|anti-linear]] isomorphism
$$
  \tau
  \,\coloneqq\,
  \sigma^\ast(\tilde h)^{-1}
  \circ
  \tilde g
  \;\colon\;
  \mathscr{V} \to \sigma^\ast\mathscr{V}
$$
such that
$$
  g(-,-)
  \;=\;
  \langle
    \tau(-)
    ,
    -
  \rangle
  \,.
$$

Similarly
$$
  \langle
    v_1
    ,
    \tau(v_2)
  \rangle
  \;=\;
  \langle
    \tau(v_2)
    ,
    v_1
  \rangle^\ast
  \;=\;
  g(v_2, v_1)^\ast
  \;=\;
  g(v_1, v_2)^\ast
  \;=\;
  \langle \tau(v_1) \vert v_2 \rangle^\ast
$$
This means that
$$
  \tau_{\sigma(x)} \circ \tau_x
  \,\colon\,
  \mathscr{V}_x \to \mathscr{V}_x
$$
is a self-adjoint operator with respect to $\langle -, - \rangle$.

(...)

\end{proof}


$\lhd$
<!--% https://q.uiver.app/#q=WzAsOSxbMCwwLCJhIl0sWzEsMCwiYSJdLFsyLDAsImEiXSxbMCwxLCJhIl0sWzIsMSwiYSJdLFszLDEsImEiXSxbNCwxLCJhIl0sWzMsMF0sWzQsMF0sWzMsNCwidCIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6ImJhcnJlZCJ9fX1dLFswLDEsInQiLDAseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJiYXJyZWQifX19XSxbMSwyLCJ0IiwwLHsic3R5bGUiOnsiYm9keSI6eyJuYW1lIjoiYmFycmVkIn19fV0sWzAsMywiIiwxLHsibGV2ZWwiOjIsInN0eWxlIjp7ImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMiw0LCIiLDEseyJsZXZlbCI6Miwic3R5bGUiOnsiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs3LDgsIiIsMix7InN0eWxlIjp7ImJvZHkiOnsibmFtZSI6Im5vbmUifSwiaGVhZCI6eyJuYW1lIjoibm9uZSJ9fX1dLFs1LDYsInQiLDIseyJzdHlsZSI6eyJib2R5Ijp7Im5hbWUiOiJiYXJyZWQifX19XSxbMSw5LCJcXG11IiwyLHsic2hvcnRlbiI6eyJ0YXJnZXQiOjIwfX1dLFsxNCw1LCIiLDIseyJzaG9ydGVuIjp7InNvdXJjZSI6MjB9LCJzdHlsZSI6eyJoZWFkIjp7Im5hbWUiOiJub25lIn19fV0sWzE0LDYsIiIsMCx7InNob3J0ZW4iOnsic291cmNlIjoyMH0sInN0eWxlIjp7ImhlYWQiOnsibmFtZSI6Im5vbmUifX19XSxbMTQsMTUsIlxcZXRhIiwyLHsibGFiZWxfcG9zaXRpb24iOjYwLCJzaG9ydGVuIjp7InNvdXJjZSI6NDAsInRhcmdldCI6MjB9fV1d-->
\begin{tikzcd}[row sep=scriptsize]
	a & a & a & {} & {} \\
	a && a & a & a
	\arrow[""{name=0, anchor=center, inner sep=0}, "t"', "\shortmid"{marking}, from=2-1, to=2-3]
	\arrow["t", "\shortmid"{marking}, from=1-1, to=1-2]
	\arrow["t", "\shortmid"{marking}, from=1-2, to=1-3]
	\arrow[Rightarrow, no head, from=1-1, to=2-1]
	\arrow[Rightarrow, no head, from=1-3, to=2-3]
	\arrow[""{name=1, anchor=center, inner sep=0}, draw=none, from=1-4, to=1-5]
	\arrow[""{name=2, anchor=center, inner sep=0}, "t"', "\shortmid"{marking}, from=2-4, to=2-5]
	\arrow["\mu"', shorten >=3pt, Rightarrow, from=1-2, to=0]
	\arrow[shorten <=4pt, Rightarrow, no head, from=1, to=2-4]
	\arrow[shorten <=4pt, Rightarrow, no head, from=1, to=2-5]
	\arrow["\eta"'{pos=0.6}, shorten <=9pt, shorten >=4pt, Rightarrow, from=1, to=2]
\end{tikzcd}

[[Kobal-HermitianKTheory.pdf:file]]

## Commuting diagrams

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &
    {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{\epsilon \otimes id}}
    \\
    && A
  }
$$

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &   {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{id \otimes \epsilon}}
    \\
    && A
  }
$$

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &
    {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{\epsilon \otimes id}}
    \\
    && A
  }
  \,.
$$

$$
  \array{
    A &\overset{\Delta}{\longrightarrow}& A \otimes A
    \\
    &   {}_{\mathllap{id}}\searrow
    & \downarrow^{\mathrlap{id \otimes \epsilon}}
    \\
    && A
  }
  \,.
$$

Diagram test


\begin{center}
\begin{tikzcd}[column sep=small]
	V && U \\
	& X
	\arrow[hook, from=1-1, to=1-3]
	\arrow[from=1-1, to=2-2]
	\arrow[from=1-3, to=2-2]
\end{tikzcd}
\end{center}

## Definition

Given a [[topological space]] $X$, the **category of open subsets** $Op(X)$ of $X$ is the [[category]] whose

* [[object | objects]] are the [[open subset | open subsets]] $U \hookrightarrow X$ of $X$;

* [[morphism | morphisms]] are the inclusions 

## Properties

* The category $Op(X)$ is a [[poset]], in fact a [[frame]] (dually a [[locale]]): it is the [[frame of opens]] of $X$.

* The category $Op(X)$ is naturally equipped with the
structure of a [[site]], where a collection $\{U_i \to U\}_i$ of morphisms is a cover precisely if their [[union]] in $X$ equals $U$:
$$ \bigcup_i U_i = U .$$

  The [[category of sheaves]] on $Op(X)$ equipped with this site structure is typically referred to as the _[[category of sheaves on a topological space|category of sheaves on the topological space]]_ and denoted

  $$
    Sh(X) \;\coloneqq\; Sh(Op(X))
    \,.
  $$

* The category $Op(X)$ is also a [[suplattice]].


## Related concepts

* [[spatial locale]]

* [[spatial topos]]




