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

The special orthogonal [[Thom spectrum]] $MSO$ is obtained from the [[orientable]] real universal line bundles, which arise as [[limits]] from the [[orientable]] real [[tautological bundles]]. Taking their orthogonal complement (which are transverse) with respect to the canonical [[scalar product]] then produces different [[Thom spaces]] and different [[suspension spectra]] $MTSO(k)$.

## Definition

Let $\widetilde\gamma_\mathbb{R}^{k,n}\twoheadrightarrow\widetilde {Gr}_k(\mathbb{R}^{n+k})$ be a oriented real tautological vector bundle of rank $k$ and ${\widetilde\gamma_\mathbb{R}^{k,n}}^\perp\twoheadrightarrow\widetilde{Gr}_k(\mathbb{R}^{n+k})$ be its orthogonal complement of rank $n$ with respect to the standard scalar product, then:
$$
MTSO(k,n)
\coloneqq\mathbf{Th}\left({\widetilde\gamma_\mathbb{R}^{k,n}}^\perp\right)
=\Sigma^{\infty-n}Th\left({\widetilde\gamma_\mathbb{R}^{k,n}}^\perp\right)
$$
There is a canonical vector bundle homomorphism ${\widetilde\gamma_\mathbb{R}^{k,n}}^\perp\oplus\underline{\mathbb{R}}\rightarrow{\widetilde \gamma_\mathbb{R}^{k,n+1}}^\perp$ (obtained as the [[pullback]] along the canonical inclusion $\widetilde{Gr}_k(\mathbb{R}^{n+k})\hookrightarrow\widetilde{Gr}_k(\mathbb{R}^{n+k+1}), V\mapsto V\times\{0\}$) and applying the [[Thom space]] yields a continuous map $\Sigma Th\left({\widetilde\gamma_\mathbb{R}^{k,n}}^\perp\right)\rightarrow Th\left({\widetilde\gamma_\mathbb{R}^{k,n+1}}^\perp\right)$ and further induces a spectrum homomorphism $MTSO(k,n)\rightarrow MTSO(k,n+1)$. Its limit is denoted:
$$
MTSO(k)
\coloneqq\lim_{n\rightarrow\infty}MTSO(k,n).
$$

## Galatius-Madsen-Tillmann-Weiss theorem

\begin{theorem}
**([[Galatius-Madsen-Tillmann-Weiss theorem]])**
The loop space of the [[classifying space]] of the oriented [[cobordism category]] $Cob_k^+$ is weakly homotopy equivalent to the [[infinite loop space]] of $MTSO(k)$, hence:
$$
\Omega|N Cob_k^+|
\simeq\Omega^\infty MTSO(k).
$$
(Alternatively it is written as $|N Cob_k^+|\simeq\Omega^{\infty-1}MTSO(k)$.)
\end{theorem}

([Galatius, Madsen, Tillmann & Weiss 2009, Main Theorem](#GMWT09))

## Homotopy groups

| | $\pi_{-4}$ | $\pi_{-3}$ | $\pi_{-2}$ | $\pi_{-1}$ | $\pi_0$ | $\pi_1$ | $\pi_2$ | $\pi_3$ | $\pi_4$ |
| -- | -- | -- | -- | -- | -- | -- | -- | -- | -- |
| MTSO(2) | $1$ | $1$ | $\mathbb{Z}$ | $1$ | $\mathbb{Z}$ | $1$ | $\mathbb{Z}$ | $\mathbb{Z}/24\mathbb{Z}$  | $\mathbb{Z}$ | 
| MTSO(3) | $1$ | $\mathbb{Z}$ | $1$ | $1$ | $1$ | $\mathbb{Z}$ | ? | ? | ? |

([Gollinger 2016, Thrm. 3.0.8.](#Gollinger16))

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

## References

* {#GMWT09} [[Søren Galatius]], [[Ib Madsen]], [[Ulrike Tillmann]], and [[Michael Weiss]], _The homotopy type of the cobordism category_, Acta Math. **202** 2 (2009) 195--239 &lbrack;[arXiv:math/0605249](http://arxiv.org/abs/math/0605249)&rbrack;
* {#Gollinger16} William Gollinger, _Madsen-Tillmann-Weiss spectra and a signature problem for manifolds_ (2016), [pdf](https://ncatlab.org/nlab/files/GollingerMTWSpectra.pdf)

[[!redirects MTSO(k)]]
[[!redirects MTSO(n)]]