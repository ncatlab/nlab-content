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

The [[cobordism theory]] for manifolds equipped with (stable) [[spinᶜ structure]].

## Properties

### Atiyah-Bott-Shapiro orientation

(...)

see at _[[Atiyah-Bott-Shapiro orientation]]_

(...)

### Relation to complex K-theory

$M Spin^c$ is related to [[KU]] in a variant of the [[Conner-Floyd isomorphism]], via the [[Atiyah-Bott-Shapiro orientation]] ([Hopkins-Hovey 92, Thm. 1](#HopkinsHovey92))

## Spinᶜ bordism homology theory

According to [[Thom's theorem]], there is an isomorphism to [[spinᶜ bordism groups]]:
$$
\Omega_n^{Spin^\mathrm{c}}
\cong\pi_n MSpin^\mathrm{c}
=\lim_{k\rightarrow\infty}\pi_k MSpin_{n+k}^\mathrm{c}.
$$
More general, [[MSpinᶜ]] defines a [[generalized homology theory]] (formally also denoted $\widetilde{MSpin^\mathrm{c}}_*$) given by:
$$
\Omega_n^{Spin^\mathrm{c}}(X)
\coloneqq\pi_n^stab(X_+\wedge MSpin^\mathrm{c})
\coloneqq\lim_{k\rightarrow\infty}\pi_{n+k}(X_+\wedge MSpin^\mathrm{c}_k)
$$
for all [[topological spaces]] $X$ with the [[disjoint union]] $X_+\coloneqq X+\{*\}$. Since $\{*\}_+\cong S^0$ is the neutral element of the [[wedge product]], one has $\Omega_n^{Spin^\mathrm{c}}=\Omega_n^{Spin^\mathrm{c}}(*)$. Geometrically, $\Omega_n^{Spin^\mathrm{c}}(X)$ can also be described by $n$-dimensional [[spinᶜ manifolds]] representing cycles and $n+1$-dimensional [[spinᶜ bordisms]] representing homologous cycles, which are mapped [[continuous]] into $X$. For a detailed explanation see [[spinᶜ bordism]].

A $n$-dimensional [[spinᶜ manifold]] $X$ has a *spinᶜ [[fundamental class]]* $[X]\in\Omega_n^{Spin^\mathrm{c}}(X)$. Let $i\colon X\hookrightarrow\mathbb{R}^{n+k}\hookrightarrow S^{n+k}$ be an [[embedding]] (which always exists due to the [[Whitney embedding theorem]]), then its [[Pontrjagin-Thom collapse map]] is:
$$
S^{n+k}\rightarrow X_+\wedge Th(N_i X)
$$
with the [[normal bundle]] $N_i X\coloneqq TS^{n+k}/i^*TX$. Since the [[spinᶜ structure]] of $X$ transfers over to its [[stable normal bundle]] ($N_i X$ for $k\rightarrow\infty$), postcomposition yields the map:
$$
S^{n+k}\rightarrow X_+\wedge MSpin^\mathrm{c}_k,
$$
which represents the spinᶜ [[fundamental class]] $[X]\in\Omega_n^{Spin^\mathrm{c}}(X)$. Geometrically, it's represented by the [[identity]] $id\colon X\rightarrow X$.

## Spinᶜ cobordism cohomology theory

[[MSpinᶜ]] also defines a [[generalized cohomology theory]] given by:
$$
\widetilde{MSpin^\mathrm{c}}^n(X)
\coloneqq\lim_{k\rightarrow\infty}[\Sigma^k X,MSpin^\mathrm{c}_{n+k}]
$$
for all [[topological spaces]] $X$. It can also be described geometrically.´with [[spinᶜ structures]].

## Related concepts


[[!include flavours of cobordism cohomology theories -- table]]


## References

* {#HopkinsHovey92} [[Michael Hopkins]], [[Mark Hovey]], _Spin cobordism determines real K-theory_, Mathematische Zeitschrift volume 210, pages 181–196 (1992) ([doi:10.1007/BF02571790](https://doi.org/10.1007/BF02571790), [[HopkinsHoveyCobordismK.pdf:file]])


[[!redirects MSpin^c]]


