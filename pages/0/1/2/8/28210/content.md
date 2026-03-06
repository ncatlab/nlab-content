+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* tabe of contents
{:toc}

## Idea

A *fivebrane bordism* is a [[B-bordism]] for the [[tangential structure]] ([[(B,f)-structure]]) being the [[fivebrane structure]]. Its [[bordism homology theory]] and [[cobordism cohomology theory]] are described by the [[Thom spectrum]] [[MFivebrane]].

## Definition

Let $M$ and $N$ be $n$-dimensional [[fivebrane manifolds]] with respective [[fivebrane structures]] $\tau_M\colon M\rightarrow BFivebrane(n)$ and $\tau_N\colon N\rightarrow BFivebrane(n)$. A $n+1$-dimensional [[fivebrane manifold]] $W$ with [[fivebrane structure]] $\tau_W\colon W\rightarrow BFivebrane(n+1)$ together with inclusions $i\colon M\hookrightarrow\partial W$ and $j\colon N\hookrightarrow\partial W$ so that:
$$
\partial W
=i(M)+j(N);
$$
$$
\mathcal{B}k\circ\tau_M
=\tau_W\circ i;
$$
$$
\mathcal{B}k\circ\tau_N
=\tau_W\circ j
$$
with the canonical inclusion $k\colon Fivebrane(n)\rightarrow Fivebrane(n+1)$ is a *fivebrane bordism* between $M$ and $N$. It is fully denoted by $(W,M,N,i,j)$, but usually $W$ is sufficient from context.

## Fivebrane bordism groups

Under the [[equivalence relation]] of fivebrane bordism, all $n$-dimensional closed [[fivebrane manifolds]] form the *fivebrane bordism group* $\Omega_n^\mathrm{Fivebrane}$, which has the [[disjoint union]] as composition, the empty manifold as neutral element and the inversion of [[orientation]] as inversion. According to [[Thom's theorem]], fivebrane bordism groups are exactly the [[stable homotopy groups]] of the [[Thom spectrum]] [[MFivebrane]]:
$$
\Omega_n^Fivebrane
\cong\pi_n MFivebrane
=\lim_{k\rightarrow\infty}\pi_{n+k}MFivebrane_k.
$$

Since $BFivebrane=BO\langle 9\rangle$ is $8$-connected, the first eight fivebrane bordism groups ($0\leq n\leq 7$) coincide with the [[framed bordism groups]]:

* $\Omega_0^Fivebrane\cong\Omega_0^fr\cong\mathbb{Z}$
* $\Omega_1^Fivebrane\cong\Omega_1^fr\cong\mathbb{Z}_2$
* $\Omega_2^Fivebrane\cong\Omega_2^fr\cong\mathbb{Z}_2$
* $\Omega_3^Fivebrane\cong\Omega_3^fr\cong\mathbb{Z}_24$
* $\Omega_4^Fivebrane\cong\Omega_4^fr\cong 1$
* $\Omega_5^Fivebrane\cong\Omega_5^fr\cong 1$
* $\Omega_6^Fivebrane\cong\Omega_6^fr\cong\mathbb{Z}_2$
* $\Omega_7^Fivebrane\cong\Omega_7^fr\cong\mathbb{Z}_240$

## Fivebrane bordism ring

All fivebrane bordism groups in a [[direct sum]] form the *fivebrane bordism ring*:
$$
\Omega^{Fivebrane}
\coloneqq\bigoplus_{n\in\mathbb{N}}\Omega_n^{Fivebrane},
$$
which has the cartesian product as additional composition and the singleton as an additional neutral element.

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

[[!redirects Fivebrane bordism]]
[[!redirects fivebrane bordisms]] 
[[!redirects Fivebrane bordisms]]

[[!redirects fivebrane cobordism]] 
[[!redirects Fivebrane cobordism]]
[[!redirects fivebrane cobordisms]] 
[[!redirects Fivebrane cobordisms]]

[[!redirects fivebrane bordism group]] 
[[!redirects Fivebrane bordism group]]
[[!redirects fivebrane bordism groups]] 
[[!redirects Fivebrane bordism groups]]
[[!redirects fivebrane bordism ring]] 
[[!redirects Fivebrane bordism ring]]

[[!redirects fivebrane bordism homology]] 
[[!redirects Fivebrane bordism homology]]
[[!redirects fivebrane bordism homology theory]] 
[[!redirects Fivebrane bordism homology theory]]

[[!redirects fivebrane cobordism cohomology]] 
[[!redirects Fivebrane cobordism cohomology]]
[[!redirects fivebrane cobordism cohomology theory]] 
[[!redirects Fivebrane cobordism cohomology theory]]