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

A *ninebrane bordism* is a [[B-bordism]] for the [[tangential structure]] ([[(B,f)-structure]]) being the [[ninebrane structure]]. Its [[bordism homology theory]] and [[cobordism cohomology theory]] are described by the [[Thom spectrum]] [[MNinebrane]].

## Definition

Let $M$ and $N$ be $n$-dimensional [[ninebrane manifolds]] with respective [[ninebrane structures]] $\tau_M\colon M\rightarrow BNinebrane(n)$ and $\tau_N\colon N\rightarrow BNinebrane(n)$. A $n+1$-dimensional [[ninebrane manifold]] $W$ with [[ninebrane structure]] $\tau_W\colon W\rightarrow BNinebrane(n+1)$ together with inclusions $i\colon M\hookrightarrow\partial W$ and $j\colon N\hookrightarrow\partial W$ so that:
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
with the canonical inclusion $k\colon Ninebrane(n)\rightarrow Ninebrane(n+1)$ is a *ninebrane bordism* between $M$ and $N$. It is fully denoted by $(W,M,N,i,j)$, but usually $W$ is sufficient from context.

## Ninebrane bordism groups

Under the [[equivalence relation]] of fivebrane bordism, all $n$-dimensional closed [[fivebrane manifolds]] form the *fivebrane bordism group* $\Omega_n^\mathrm{Fivebrane}$, which as the [[disjoint union]] as composition, the empty manifold as neutral element and the inversion of [[orientation]] as inversion. According to [[Thom's theorem]], ninebrane bordism groups are exactly the [[stable homotopy groups]] of the [[Thom spectrum]] [[MNinebrane]]:
$$
\Omega_n^Ninebrane
\cong\pi_n MNinebrane
=\lim_{k\rightarrow\infty}\pi_{n+k}MNinebrane_k.
$$

Since $BFivebrane=BO\langle 16\rangle$ is $15$-connected, the first fifteen fivebrane bordism groups ($0\leq n\leq 14$) coincide with the [[framed bordism groups]]:

* $\Omega_0^Ninebrane\cong\Omega_0^fr\cong\mathbb{Z}$
* $\Omega_1^Ninebrane\cong\Omega_1^fr\cong\mathbb{Z}_2$
* $\Omega_2^Ninebrane\cong\Omega_2^fr\cong\mathbb{Z}_2$
* $\Omega_3^Ninebrane\cong\Omega_3^fr\cong\mathbb{Z}_24$
* $\Omega_4^Ninebrane\cong\Omega_4^fr\cong 1$
* $\Omega_5^Ninebrane\cong\Omega_5^fr\cong 1$
* $\Omega_6^Ninebrane\cong\Omega_6^fr\cong\mathbb{Z}_2$
* $\Omega_7^Ninebrane\cong\Omega_7^fr\cong\mathbb{Z}_240$

## Ninebrane bordism ring

All fivebrane bordism groups in a [[direct sum]] form the *ninebrane bordism ring*:
$$
\Omega^\mathrm{Ninebrane}
\coloneqq\bigoplus_{n\in\mathbb{N}}\Omega_n^\mathrm{Ninebrane},
$$
which has the cartesian product as additional composition and the singleton as an additional neutral element.

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

[[!redirects Ninebrane bordism]]
[[!redirects ninebrane bordisms]] 
[[!redirects Ninebrane bordisms]]

[[!redirects ninebrane cobordism]] 
[[!redirects Ninebrane cobordism]]
[[!redirects ninebrane cobordisms]] 
[[!redirects Ninebrane cobordisms]]

[[!redirects ninebrane bordism group]] 
[[!redirects Ninebrane bordism group]]
[[!redirects ninebrane bordism groups]] 
[[!redirects Ninebrane bordism groups]]
[[!redirects ninebrane bordism ring]] 
[[!redirects Ninebrane bordism ring]]

[[!redirects ninebrane bordism homology]] 
[[!redirects Ninebrane bordism homology]]
[[!redirects ninebrane bordism homology theory]] 
[[!redirects Ninebrane bordism homology theory]]

[[!redirects ninebrane cobordism cohomology]] 
[[!redirects Ninebrane cobordism cohomology]]
[[!redirects ninebrane cobordism cohomology theory]] 
[[!redirects Ninebrane cobordism cohomology theory]]