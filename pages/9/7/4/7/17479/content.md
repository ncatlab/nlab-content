

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
