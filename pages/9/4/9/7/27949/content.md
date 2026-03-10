+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Higher Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _fivebrane spectrum_ is the [[Thom spectrum]] of the [[universal vector bundle]] over a [[fivebrane group]]. Their limit over the infinite fivebrane group is of particular interest since its [[generalized homology theory]] describes [[fivebrane bordisms]].

## Definition

Let $Fivebrane(n)\coloneqq O(n)\langle 8\rangle$ be the $7$-connected cover in the [[Whitehead tower]] of the [[orthogonal group]] $O(n)$. Through the canonical projection $p\colon Fivebrane(n)\twoheadrightarrow O(n)$, there is a [[pullback]]:
$$
\gamma_{Fivebrane}^n
\coloneqq p^*\gamma_\mathbb{R}^n
\twoheadrightarrow BFivebrane(n).
$$
Its [[Thom spectrum]] is the _Fivebrane spectrum_:
$$
MFivebrane(n)
\coloneqq\mathbf{Th}\left(\gamma_{Fivebrane}^n\right)
=\Sigma^{\infty-n}Th\left(\gamma_{Fivebrane}^n\right).
$$
The desuspension assures the invariance under the [[Whitney sum]] with trivial bundles, so $MFivebrane(n)=\mathbf{Th}\left(\gamma_{Fivebrane}^n\oplus\underline{\mathbb{R}^m}\right)$. It also assures that the canonical inclusion $i\colon Fivebrane(n)\rightarrow Fivebrane(n+1)$, which pulls back to a canonical [[vector bundle]] homomorphism $\gamma_{Fivebrane}^n\oplus\underline{\mathbb{R}}=i^*\gamma_{Fivebrane}^{n+1}\rightarrow\gamma_{Fivebrane}^{n+1}$, induces a spectrum homomorphism:
$$
\begin{aligned}
MFivebrane(n)
&=\Sigma^{\infty-n}Th\left(\gamma_{Fivebrane}^n\right)
\cong\Sigma^{\infty-(n+1)}Th\left(\gamma_{Fivebrane}^n\oplus\underline{\mathbb{R}}\right) \\
&\rightarrow\Sigma^{\infty-(n+1)}Th\left(\gamma_{Fivebrane}^{n+1}\right)
=MFivebrane(n+1).
\end{aligned}
$$
Its [[limit]] is denoted:
$$
MFivebrane
\coloneqq\lim_{n\rightarrow\infty}MFivebrane(n).
$$

## Connections

From the canonical projections $Ninebrane(n)\twoheadrightarrow Fivebrane(n)\twoheadrightarrow String(n)$ and $Ninebrane\twoheadrightarrow Fivebrane\twoheadrightarrow String$, there are canonical spectrum morphisms:
$$
MNinebrane(n)\rightarrow MFivebrane(n)\rightarrow MString(n);
$$
$$
MNinebrane\rightarrow MFivebrane\rightarrow MString.
$$

## Fivebrane bordism homology theory

According to [[Thom's theorem]], there is an isomorphism to [[fivebrane bordism groups]]:
$$
\Omega_n^{Fivebrane}
\cong\pi_n MFivebrane
=\lim_{k\rightarrow\infty}\pi_k MFivebrane_{n+k}.
$$
More general, [[MFivebrane]] defines a [[generalized homology theory]] (formally also denoted $\widetilde{MFivebrane}_*$) given by:
$$
\Omega_n^Fivebrane(X)
\coloneqq\pi_n^stab(X_+\wedge MFivebrane)
\coloneqq\lim_{k\rightarrow\infty}\pi_{n+k}(X_+\wedge MFivebrane_k)
$$
for all [[topological spaces]] $X$ with the [[disjoint union]] $X_+\coloneqq X+\{*\}$. Since $\{*\}_+\cong S^0$ is the neutral element of the [[wedge product]], one has $\Omega_n^Fivebrane=\Omega_n^Fivebrane(*)$. Geometrically, $\Omega_n^Fivebrane(X)$ can also be described by $n$-dimensional [[fivebrane manifolds]] representing cycles and $n+1$-dimensional [[fivebrane bordisms]] representing homologous cycles, which are mapped [[continuous]] into $X$. For a detailed explanation see [[fivebrane bordism]].

A $n$-dimensional [[fivebrane manifold]] $X$ has a *fivebrane [[fundamental class]]* $[X]\in\Omega_n^Fivebrane(X)$. Let $i\colon X\hookrightarrow\mathbb{R}^{n+k}\hookrightarrow S^{n+k}$ be an [[embedding]] (which always exists due to the [[Whitney embedding theorem]]), then its [[Pontrjagin-Thom collapse map]] is:
$$
S^{n+k}\rightarrow X_+\wedge Th(N_i X)
$$
with the [[normal bundle]] $N_i X\coloneqq TS^{n+k}/i^*TX$. Since the [[fivebrane structure]] of $X$ transfers over to its [[stable normal bundle]] ($N_i X$ for $k\rightarrow\infty$), postcomposition yields the map:
$$
S^{n+k}\rightarrow X_+\wedge MFivebrane_k
$$
representing the fivebrane [[fundamental class]] $[X]\in\Omega_n^Fivebrane(X)$. Geometrically, it's represented by the [[identity]] $id\colon X\rightarrow X$.

## Fivebrane cobordism cohomology theory

[[MFivebrane]] also defines a [[generalized cohomology theory]] given by:
$$
\widetilde{MFivebrane}^n(X)
\coloneqq\lim_{k\rightarrow\infty}[\Sigma^k X,MFivebrane_{n+k}]
$$
for all [[topological spaces]] $X$. It can also be described geometrically with [[fivebrane structures]].

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

[[!redirects Fivebrane spectrum]]
[[!redirects Fivebrane spectrum]]
[[!redirects Fivebrane spectra]]
[[!redirects Fivebrane spectra]]
[[!redirects Fivebrane Thom spectrum]]
[[!redirects Fivebrane Thom spectrum]]
[[!redirects Fivebrane Thom spectra]]
[[!redirects Fivebrane Thom spectra]]