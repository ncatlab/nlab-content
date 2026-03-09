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

A _spinʰ spectrum_ is the [[Thom spectrum]] of the [[universal vector bundle]] over a [[spinʰ group]]. Their limit over the infinite spinʰ group is of particular interest since its [[generalized homology theory]] describes spinʰ bordisms.

## Definition

Let $Spin^\mathrm{h}(n)\coloneqq (Spin(n)\times Sp(1))/\mathbb{Z}_2$ be the [[spinʰ group]]. Through the canonical projection $p\colon Spin^\mathrm{h}(n)\twoheadrightarrow O(n)$, there is a [[pullback]]:
$$
\gamma_{Spin^\mathrm{h}}^n
\coloneqq p^*\gamma_\mathbb{R}^n
\twoheadrightarrow BSpin^\mathrm{h}(n).
$$
Its [[Thom spectrum]] is the _Spinʰ spectrum_:
$$
MSpin^\mathrm{h}(n)
\coloneqq\mathbf{Th}\left(\gamma_{Spin^\mathrm{h}}^n\right)
=\Sigma^{\infty-n}Th\left(\gamma_{Spin^\mathrm{h}}^n\right).
$$
The desuspension assures the invariance under the [[Whitney sum]] with trivial bundles, so $MSpin^\mathrm{h}(n)=\mathbf{Th}\left(\gamma_{Spin^\mathrm{h}}^n\oplus\underline{\mathbb{R}^m}\right)$. It also assures that the canonical inclusion $i\colon Spin^\mathrm{h}(n)\rightarrow Spin^\mathrm{h}(n+1)$, which pulls back to a canonical [[vector bundle]] homomorphism $\gamma_{Spin^\mathrm{h}}^n\oplus\underline{\mathbb{R}}=i^*\gamma_{Spin^\mathrm{h}}^{n+1}\rightarrow\gamma_{Spin^\mathrm{h}}^{n+1}$, induces a spectrum homomorphism:
$$
MSpin^\mathrm{h}(n)
=\Sigma^{\infty-n}Th\left(\gamma_{Spin^\mathrm{h}}^n\right)
\cong\Sigma^{\infty-(n+1)}Th\left(\gamma_{Spin^\mathrm{h}}^n\oplus\underline{\mathbb{R}}\right)
\rightarrow\Sigma^{\infty-(n+1)}Th\left(\gamma_{Spin^\mathrm{h}}^{n+1}\right)
=MSpin^\mathrm{h}(n+1).
$$
Its [[limit]] is denoted:
$$
MSpin^\mathrm{h}
\coloneqq\lim_{n\rightarrow\infty}MSpin^\mathrm{h}(n).
$$

## Connections

From the canonical projections $Spin(n)\hookrightarrow Spin^\mathrm{c}(n)\hookrightarrow Spin^\mathrm{h}(n)$ and $Spin\hookrightarrow Spin^\mathrm{c}
\hookrightarrow Spin^\mathrm{h}$, there are canonical spectrum morphisms:
$$
MSpin(n)\rightarrow MSpin^\mathrm{c}(n)\rightarrow MSpin^\mathrm{h}(n);
$$
$$
MSpin\rightarrow MSpin^\mathrm{c}\rightarrow MSpin^\mathrm{h}.
$$

## Examples

Due to the isomophisms $Spin^\mathrm{h}(1)\cong Sp(1)\cong SU(2)$ and $Spin^\mathrm{h}(2)\cong U(2)$ there are isomorphisms:
$$
MSpin^\mathrm{h}(1)
\cong MSp(1)
\cong MSU(2);
$$
$$
MSpin^\mathrm{h}(2)
\cong MU(2).
$$

## Spinʰ bordism homology theory

According to [[Thom's theorem]], there is an isomorphism to [[spinʰ bordism groups]]:
$$
\Omega_n^{Spin^\mathrm{h}}
\cong\pi_n MSpin^\mathrm{h}
=\lim_{k\rightarrow\infty}\pi_k MSpin^\mathrm{h}_{n+k}.
$$
More general, [[MSpinʰ]] defines a [[generalized homology theory]] (formally also denoted $\widetilde{MSpin^\mathrm{h}}_*$) given by:
$$
\Omega_n^{Spin^\mathrm{h}}(X)
\coloneqq\pi_n^stab(X_+\wedge MSpin^\mathrm{h})
\coloneqq\lim_{k\rightarrow\infty}\pi_{n+k}(X_+\wedge MSpin^\mathrm{h}_k)
$$
for all [[topological spaces]] $X$ with the [[disjoint union]] $X_+\coloneqq X+\{*\}$. Since $\{*\}_+\cong S^0$ is the neutral element of the [[wedge product]], one has $\Omega_n^{Spin^\mathrm{h}}=\Omega_n^{Spin^\mathrm{h}}(*)$. Geometrically, $\Omega_n^{Spin^\mathrm{h}}(X)$ can also be described by $n$-dimensional [[spinʰ manifolds]] representing cycles and $n+1$-dimensional [[spinʰ bordisms]] representing homologous cycles, which are mapped [[continuous]] into $X$. For a detailed explanation see [[spinʰ bordism]].

## Spinʰ cobordism cohomology theory

[[MSpinʰ]] also defines a [[generalized cohomology theory]] given by:
$$
\widetilde{MSpin^\mathrm{h}}^n(X)
\coloneqq\lim_{k\rightarrow\infty}[\Sigma^k X,MSpin^\mathrm{h}_{n+k}]
$$
for all [[topological spaces]] $X$. It can also be described geometrically with [[spinʰ structures]].

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

[[!redirects MSpin^h]]
[[!redirects Spinʰ spectrum]]
[[!redirects Spin^h spectrum]]
[[!redirects Spinʰ spectra]]
[[!redirects Spin^h spectra]]
[[!redirects Spinʰ Thom spectrum]]
[[!redirects Spin^h Thom spectrum]]
[[!redirects Spinʰ Thom spectra]]
[[!redirects Spin^h Thom spectra]]