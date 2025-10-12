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

The orthogonal [[Thom spectrum]] $MO$ is obtained from the real universal line bundles, which arise as [[limits]] from the real [[tautological bundles]]. Taking their orthogonal complement (which are transverse) with respect to the canonical [[scalar product]] then produces different [[Thom spaces]] and different [[suspension spectra]] $MTO(k)$.

## Definition

Let $\gamma_\mathbb{R}^{k,n}\twoheadrightarrow Gr_k(\mathbb{R}^{n+k})$ be a real tautological vector bundle of rank $k$ and ${\gamma_\mathbb{R}^{k,n}}^\perp\twoheadrightarrow Gr_k(\mathbb{R}^{n+k})$ be its orthogonal complement of rank $n$ with respect to the standard scalar product, then:
$$
MTO(k,n)
\coloneqq\mathbf{Th}\left({\gamma_\mathbb{R}^{k,n}}^\perp\right)
=\Sigma^{\infty-n}Th\left({\gamma_\mathbb{R}^{k,n}}^\perp\right)
$$

([Gollinger 2016, Def. 1.2.1.](#Gollinger16))

There is a canonical vector bundle homomorphism ${\gamma_\mathbb{R}^{k,n}}^\perp\oplus\underline{\mathbb{R}}\rightarrow{\gamma_\mathbb{R}^{k,n+1}}^\perp$ (obtained as the [[pullback]] along the canonical inclusion $Gr_k(\mathbb{R}^{n+k})\hookrightarrow Gr_k(\mathbb{R}^{n+k+1}), V\mapsto V\times\{0\}$) and applying the [[Thom space]] yields a continuous map $\Sigma Th\left({\gamma_\mathbb{R}^{k,n}}^\perp\right)\rightarrow Th\left({\gamma_\mathbb{R}^{k,n+1}}^\perp\right)$ and further induces a spectrum homomorphism $MTO(k,n)\rightarrow MTO(k,n+1)$. Its limit is denoted:
$$
MTO(k)
\coloneqq\lim_{n\rightarrow\infty}MTO(k,n).
$$

## Galatius-Madsen-Tillmann-Weiss theorem

\begin{theorem}
**([[Galatius-Madsen-Tillmann-Weiss theorem]])**
The loop space of the [[classifying space]] of the [[cobordism category]] $Cob_k$ is weakly homotopy equivalent to the [[infinite loop space]] of $MTO(k)$, hence:
$$
\Omega|N Cob_k|
\simeq\Omega^\infty MTO(k).
$$
(Alternatively it is written as $|N Cob_k|\simeq\Omega^{\infty-1}MTO(k)$.)
\end{theorem}

([Galatius, Madsen, Tillmann & Weiss 2009, Main Theorem](#GMWT09))

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

## References

* {#GMWT09} [[Søren Galatius]], [[Ib Madsen]], [[Ulrike Tillmann]], and [[Michael Weiss]], _The homotopy type of the cobordism category_, Acta Math. **202** 2 (2009) 195--239 &lbrack;[arXiv:math/0605249](http://arxiv.org/abs/math/0605249)&rbrack;
* {#Gollinger16} William Gollinger, _Madsen-Tillmann-Weiss spectra and a signature problem for manifolds_ (2016), [pdf](https://ncatlab.org/nlab/files/GollingerMTWSpectra.pdf)

[[!redirects MTO(k)]]
[[!redirects MTO(n)]]