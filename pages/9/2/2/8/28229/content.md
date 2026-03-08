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

A _string spectrum_ is the [[Thom spectrum]] of the [[universal vector bundle]] over a [[string group]]. Their limit over the infinite string group is of particular interest since its [[generalized homology theory]] describes [[string bordisms]].

## Definition

Let $String(n)\coloneqq O(n)\langle 4\rangle=O(n)\langle 5\rangle=O(n)\langle 6\rangle=O(n)\langle 7\rangle$ be the $3$-connected cover in the [[Whitehead tower]] of the [[orthogonal group]] $O(n)$. Through the canonical projection $p\colon String(n)\twoheadrightarrow O(n)$, there is a [[pullback]]:
$$
\gamma_String^n
\coloneqq p^*\gamma_\mathbb{R}^n
\twoheadrightarrow BString(n).
$$
Its [[Thom spectrum]] is the _string spectrum_:
$$
MString(n)
\coloneqq\mathbf{Th}\left(\gamma_String^n\right)
=\Sigma^{\infty-n}Th\left(\gamma_String^n\right).
$$
The desuspension assures the invariance under the [[Whitney sum]] with trivial bundles, so $MString(n)=\mathbf{Th}\left(\gamma_String^n\oplus\underline{\mathbb{R}^m}\right)$. It also assures that the canonical inclusion $i\colon String(n)\rightarrow String(n+1)$, which pulls back to a canonical [[vector bundle]] homomorphism $\gamma_String^n\oplus\underline{\mathbb{R}}=i^*\gamma_String^{n+1}\rightarrow\gamma_String^{n+1}$, induces a spectrum homomorphism:
$$
\begin{aligned}
MString(n)
&=\Sigma^{\infty-n}Th\left(\gamma_String^n\right)
\cong\Sigma^{\infty-(n+1)}Th\left(\gamma_String^n\oplus\underline{\mathbb{R}}\right) \\
&\rightarrow\Sigma^{\infty-(n+1)}Th\left(\gamma_String^{n+1}\right)
=MString(n+1).
\end{aligned}
$$
Its [[limit]] is denoted:
$$
MString
\coloneqq\lim_{n\rightarrow\infty}MString(n).
$$

## Properties

According to [[Thom's theorem]], there is an isomorphism to [[string bordism groups]]:
$$
\Omega_n^String
\cong\pi_n MString
=\lim_{k\rightarrow\infty}\pi_k MString_{n+k}.
$$

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

[[!redirects String spectrum]]
[[!redirects String spectrum]]
[[!redirects String spectra]]
[[!redirects String spectra]]
[[!redirects String Thom spectrum]]
[[!redirects String Thom spectrum]]
[[!redirects String Thom spectra]]
[[!redirects String Thom spectra]]