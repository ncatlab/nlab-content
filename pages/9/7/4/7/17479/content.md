

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The universal [[Thom spectrum]] for [[spin structure]] is denoted $M Spin$.

## Spin bordism homology theory

According to [[Thom's theorem]], there is an isomorphism to [[spin bordism groups]]:
$$
\Omega_n^Spin
\cong\pi_n MSpin
=\lim_{k\rightarrow\infty}\pi_k MSpin_{n+k}.
$$
More general, [[MSpin]] defines a [[generalized homology theory]] (formally also denoted $\widetilde{MSpin}_*$) given by:
$$
\Omega_n^Spin(X)
\coloneqq\pi_n^stab(X_+\wedge MSpin)
\coloneqq\lim_{k\rightarrow\infty}\pi_{n+k}(X_+\wedge MSpin_k)
$$
for all [[topological spaces]] $X$ with the [[disjoint union]] $X_+\coloneqq X+\{*\}$. Since $\{*\}_+\cong S^0$ is the neutral element of the [[wedge product]], one has $\Omega_n^Spin=\Omega_n^Spin(*)$. Geometrically, $\Omega_n^Spin(X)$ can also be described by $n$-dimensional [[spin manifolds]] representing cycles and $n+1$-dimensional [[spin bordisms]] representing homologous cycles, which are mapped [[continuous]] into $X$. For a detailed explanation see [[spin bordism]].

A $n$-dimensional [[spin manifold]] $X$ has a *spin [[fundamental class]]* $[X]\in\Omega_n^Spin(X)$. Let $i\colon X\hookrightarrow\mathbb{R}^{n+k}\hookrightarrow S^{n+k}$ be an [[embedding]] (which always exists due to the [[Whitney embedding theorem]]), then its [[Pontrjagin-Thom collapse map]] is:
$$
S^{n+k}\rightarrow X_+\wedge Th(N_i X)
$$
with the [[normal bundle]] $N_i X\coloneqq TS^{n+k}/i^*TX$. Since the [[spin structure]] of $X$ transfers over to its [[stable normal bundle]] ($N_i X$ for $k\rightarrow\infty$), postcomposition yields the map:
$$
S^{n+k}\rightarrow X_+\wedge MSpin_k,
$$
which represents the spin [[fundamental class]] $[X]\in\Omega_n^Spin(X)$. Geometrically, it's represented by the [[identity]] $id\colon X\rightarrow X$.

## Spin cobordism cohomology theory

[[MSpin]] also defines a [[generalized cohomology theory]] given by:
$$
\widetilde{MSpin}^n(X)
\coloneqq\lim_{k\rightarrow\infty}[\Sigma^k X,MSpin_{n+k}]
$$
for all [[topological spaces]] $X$. It can also be described geometrically with [[spin structures]].

## Related concepts

* [[Atiyah-Bott-Shapiro orientation]]


\linebreak

[[!include flavours of cobordism cohomology theories -- table]]
