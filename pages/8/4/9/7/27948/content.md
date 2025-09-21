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

## Properties

According to [[Thom's theorem]], there is an isomorphism:
$$
\Omega_n^{Spin^\mathrm{h}}
\cong\pi_n MSpin^\mathrm{h}
=\lim_{k\rightarrow\infty}\pi_k MSpin^\mathrm{h}_{n+k}.
$$

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