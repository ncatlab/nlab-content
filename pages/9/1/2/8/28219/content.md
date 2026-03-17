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

A *spinᶜ bordism* is a [[B-bordism]] for the [[tangential structure]] ([[(B,f)-structure]]) being the [[spinᶜ structure]]. Its [[bordism homology theory]] and [[cobordism cohomology theory]] are described by the [[Thom spectrum]] [[MSpinᶜ]].

Its definition is fully analogous to that of [[spin bordism]]. Similarily, there are *spinᶜ bordism groups* and the *spinᶜ bordism ring*:
$$
\Omega_n^{Spin^\mathrm{c}}
\coloneqq\pi_n MSpin^\mathrm{c}
=\lim_{k\rightarrow\infty}\pi_{n+k} MSpin^\mathrm{c}_k;
$$
$$
\Omega^{Spin^\mathrm{c}}
\coloneqq\bigoplus_{n\in\mathbb{N}}\Omega_n^{Spin^\mathrm{c}}.
$$

## Definition

Let $M$ and $N$ be $n$-dimensional [[spinᶜ manifolds]] with respective [[spinᶜ structures]] $\tau_M\colon M\rightarrow BSpin^c(n)$ and $\tau_N\colon N\rightarrow BSpin^c(n)$. A $n+1$-dimensional [[spinᶜ manifold]] $W$ with [[spinᶜ structure]] $\tau_W\colon W\rightarrow BSpin^c(n+1)$ together with inclusions $i\colon M\hookrightarrow\partial W$ and $j\colon N\hookrightarrow\partial W$ so that:
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
with the canonical inclusion $k\colon Spin^c(n)\rightarrow Spin^c(n+1)$ is a *spinᶜ bordism* between $M$ and $N$. It is fully denoted by $(W,M,N,i,j)$, but usually $W$ is sufficient from context.

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

## References

* {#BuchananMcKean26} [[Jonathan Buchanan]], [[Stephen McKean]]: _KSp-characteristic classes determine Spin cobordism_, Algebr. Geom. Topol. **26** (2026) 485-551 &lbrack;[arXiv:2312.08209](http://arxiv.org/abs/2312.08209), [doi:10.2140/agt.2026.26.485](https://doi.org/10.2140/agt.2026.26.485)&rbrack;

[[!redirects Spinᶜ bordism]]
[[!redirects spinᶜ cobordism]] 
[[!redirects Spinᶜ cobordism]]

[[!redirects spinᶜ bordism group]] 
[[!redirects Spinᶜ bordism group]]
[[!redirects spinᶜ bordism groups]] 
[[!redirects Spinᶜ bordism groups]]
[[!redirects spinᶜ bordism ring]] 
[[!redirects Spinᶜ bordism ring]]

[[!redirects spinᶜ bordism homology]] 
[[!redirects Spinᶜ bordism homology]]
[[!redirects spinᶜ bordism homology theory]] 
[[!redirects Spinᶜ bordism homology theory]]

[[!redirects spinᶜ cobordism cohomology]] 
[[!redirects Spinᶜ cobordism cohomology]]
[[!redirects spinᶜ cobordism cohomology theory]] 
[[!redirects Spinᶜ cobordism cohomology theory]]

[[!redirects spinc bordism]]
[[!redirects Spinc bordism]]
[[!redirects spinc cobordism]] 
[[!redirects Spinc cobordism]]

[[!redirects spinc bordism group]] 
[[!redirects Spinc bordism group]]
[[!redirects spinc bordism groups]] 
[[!redirects Spinc bordism groups]]
[[!redirects spinc bordism ring]] 
[[!redirects Spinc bordism ring]]

[[!redirects spinc bordism homology]] 
[[!redirects Spinc bordism homology]]
[[!redirects spinc bordism homology theory]] 
[[!redirects Spinc bordism homology theory]]

[[!redirects spinc cobordism cohomology]] 
[[!redirects Spinc cobordism cohomology]]
[[!redirects spinc cobordism cohomology theory]] 
[[!redirects Spinc cobordism cohomology theory]]