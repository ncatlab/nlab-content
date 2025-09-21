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

A _fivebrane spectrum_ is the [[Thom spectrum]] of the [[universal vector bundle]] over a [[fivebrane group]]. Their limit over the infinite fivebrane group is of particular interest since its [[generalized homology theory]] describes fivebrane bordisms.

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
MNinebrane(n)\twoheadrightarrow MFivebrane(n)\twoheadrightarrow MString(n);
$$
$$
MNinebrane\twoheadrightarrow MFivebrane\twoheadrightarrow MString.
$$

## Properties

According to [[Thom's theorem]], there is an isomorphism:
$$
\Omega_n^{Fivebrane}
\cong\pi_n Fivebrane
=\lim_{k\rightarrow\infty}\pi_k Fivebrane_{n+k}.
$$

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