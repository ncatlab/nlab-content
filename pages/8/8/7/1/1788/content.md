
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
  Q Vect_{\mathbb{C}}(X,\sigma)
$$ 
for the resulting [[category]].

The [[direct sum of vector bundles|direct sum of]] [[underlying]] vector bundles with $\sigma$-quadratic form (Def. \ref{SigmaQuadraticFormOnComplexVectorBundle}) inherits a $\sigma$-quadratic form in the evident summand-wise way. This operation makes the set of [[isomorphism classes]] into a [[commutative monoid]]:
\[
  \label{MonoidOfSigmaQuadraticComplexVectorBundles}
  \big(
    Q Vect_{\mathbb{C}}(X,\sigma)_{/\sim}, 
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
    Q Vect_{\mathbb{C}}(X,\sigma)_{/\sim}, 
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

This construction extends to an [[additive functor]] from the [[core groupoid]] of [[VectBund|$Vect_{\mathbb{C}}(X)$]] to $Q Vect_{\mathbb{C}}(X,\sigma)$, called the *[[hyperbolic functor]]*, and hence define a [[group homomorphism]] from the ordinary [[topological K-theory]]-group of $X$ to its topological Hermtian K-theory (eq:TopologicalHermitianKTheoryDueToCrabb):
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
Now since 
$$
  \tau_{\sigma(x)} \circ \tau_x
  \,\colon\,
  \mathscr{V}_x \to \mathscr{V}_x
$$

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
