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

A _ninebrane spectrum_ is the [[Thom spectrum]] of the [[universal vector bundle]] over a [[ninebrane group]]. Their limit over the infinite ninebrane group is of particular interest since its [[generalized homology theory]] describes ninebrane bordisms.

## Definition

Let $Ninebrane(n)\coloneqq O(n)\langle 12\rangle$ be the $11$-connected cover in the [[Whitehead tower]] of the [[orthogonal group]] $O(n)$. (Following the notations $2-Orient(n)=BO(n) \langle 9\rangle$ and $2-Spin(n) =BO(n) \langle 10\rangle$, one could also write $2-String(n)=Ninebrane(n)$ to indicte its correspondence with the [[string group]] under [[Bott periodicity]].)  Through the canonical projection $p\colon Ninebrane(n)\twoheadrightarrow O(n)$, there is a [[pullback]]:
$$
\gamma_{Ninebrane}^n
\coloneqq p^*\gamma_\mathbb{R}^n
\twoheadrightarrow BNinebrane(n).
$$
Its [[Thom spectrum]] is the _Ninebrane spectrum_:
$$
MNinebrane(n)
\coloneqq\mathbf{Th}\left(\gamma_{Ninebrane}^n\right)
=\Sigma^{\infty-n}Th\left(\gamma_{Ninebrane}^n\right).
$$
The desuspension assures the invariance under the [[Whitney sum]] with trivial bundles, so $MNinebrane(n)=\mathbf{Th}\left(\gamma_{Ninebrane}^n\oplus\underline{\mathbb{R}^m}\right)$. It also assures that the canonical inclusion $i\colon Ninebrane(n)\rightarrow Ninebrane(n+1)$, which pulls back to a canonical [[vector bundle]] homomorphism $\gamma_{Ninebrane}^n\oplus\underline{\mathbb{R}}=i^*\gamma_{Ninebrane}^{n+1}\rightarrow\gamma_{Ninebrane}^{n+1}$, induces a spectrum homomorphism:
$$
\begin{aligned}
MNinebrane(n)
&=\Sigma^{\infty-n}Th\left(\gamma_{Ninebrane}^n\right)
\cong\Sigma^{\infty-(n+1)}Th\left(\gamma_{Ninebrane}^n\oplus\underline{\mathbb{R}}\right) \\
&\rightarrow\Sigma^{\infty-(n+1)}Th\left(\gamma_{Ninebrane}^{n+1}\right)
=MNinebrane(n+1).
\end{aligned}
$$
Its [[limit]] is denoted:
$$
MNinebrane
\coloneqq\lim_{n\rightarrow\infty}MNinebrane(n).
$$

## Connections

From the canonical projections $O(n)\langle 16\rangle\twoheadrightarrow Ninebrane(n)\twoheadrightarrow Fivebrane(n)$ and $O\langle 16\rangle\twoheadrightarrow Ninebrane\twoheadrightarrow Fivebrane$ , there are canonical spectrum morphisms:
$$
MO(n)\langle 16\rangle\rightarrow MNinebrane(n)\rightarrow MFivebrane(n);
$$
$$
MO\langle 16\rangle\rightarrow MNinebrane\rightarrow MFivebrane.
$$

## Properties

According to [[Thom's theorem]], there is an isomorphism:
$$
\Omega_n^{Ninebrane}
\cong\pi_n MNinebrane
=\lim_{k\rightarrow\infty}\pi_k MNinebrane_{n+k}.
$$

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

[[!redirects Ninebrane spectrum]]
[[!redirects Ninebrane spectrum]]
[[!redirects Ninebrane spectra]]
[[!redirects Ninebrane spectra]]
[[!redirects Ninebrane Thom spectrum]]
[[!redirects Ninebrane Thom spectrum]]
[[!redirects Ninebrane Thom spectra]]
[[!redirects Ninebrane Thom spectra]]