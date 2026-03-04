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

Under the [[equivalence relation]] of fivebrane bordism, all $n$-dimensional closed [[fivebrane manifolds]] form the *fivebrane bordism group* $\Omega_n^\mathrm{Fivebrane}$, which as the [[disjoint union]] as composition, the empty manifold as neutral element and the inversion of [[orientation]] as inversion.

## Ninebrane bordism ring

All fivebrane bordism groups in a [[direct sum]] form the *ninebrane bordism ring*:
$$
\Omega^\mathrm{Ninebrane}
\coloneqq\bigoplus_{n\in\mathbb{N}}\Omega_n^\mathrm{Ninebrane},
$$
which has the cartesian product as additional composition and the singleton as an additional neutral element.

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

[[!redirects ninebrane cobordism]] 
[[!redirects Ninebrane cobordism]]

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