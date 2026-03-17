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
* table of contents
{:toc}

## Idea

A *2-spin bordism* is a [[B-bordism]] for the [[tangential structure]] ([[(B,f)-structure]]) being the [[2-spin structure]]. Its [[bordism homology theory]] and [[cobordism cohomology theory]] are described by the [[Thom spectrum]] [[M2-Spin]]. Its definition is fully analogous to that of similar bordisms like [[spin bordism]]. Similarily, there are *2-spin bordism groups* and the *2-spin bordism ring*:
$$
\Omega_n^{2\text{-}Spin}
\coloneqq\pi_n M2\text{-}Spin
=\lim_{k\rightarrow\infty}\pi_{n+k} M2\text{-}Spin_k;
$$
$$
\Omega^{2\text{-}Spin}
\coloneqq\bigoplus_{n\in\mathbb{N}}\Omega_n^{2\text{-}Spin}.
$$

## Properties

\begin{proposition}
Every $n$-dimensional [[2-spin manifold]] is 2-spin bordant to a $\min\left\{11,\left\lceil\frac{n}{2}-1\right\rceil\right\}$-[[n-connected space|connected]] [[2-spin manifold]], equivalently meaning that every 2-spin bordism homology class in $\Omega_n^{2\text{-}Spin}$ can be represented by such a [[2-spin manifold]]. (For $n\geq 23$, the result stabilizes at a [[n-connected space|11-connected]] [[2-spin manifold]].)
\end{proposition}

([Botvinnik & Labbi 14, Lem. 3.2 (1)](#BotvinnikLabbi14))

\begin{proposition}
For $n$-dimensional $\min\left\{11,\left\lceil\frac{n}{2}-1\right\rceil\right\}$-[[n-connected space|connected]] [[2-spin manifolds]] $M$ and $N$, a 2-spin bordism $W\colon M\rightsquigarrow N$ exists with $M\hookrightarrow W$ also $\min\left\{11,\left\lceil\frac{n}{2}-1\right\rceil\right\}$-[[n-connected space|connected]].
\end{proposition}

([Botvinnik & Labbi 14, Lem. 3.2 (2)](#BotvinnikLabbi14))

\begin{proposition}
If a $n$-dimensional $k$-[[n-connected space|connected]] [[compact]] [[2-spin manifold]] $M$ with $k\leq 10$ and $n\geq 2k+3$ is 2-spin bordant to another [[compact]] [[2-spin manifold]] $N$, then $M$ can be obtained from $N$ by [[surgery]] of [[codimension]] at least $k+2$.
\end{proposition}

([Botvinnik & Labbi 14, Prop. 3.4](#BotvinnikLabbi14))

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

## References

* {#Sati14} [[Hisham Sati]], _Ninebrane structures_ ([arXiv:1405.7686](http://arxiv.org/abs/1405.7686))

* {#BotvinnikLabbi14} [[Boris Botvinnik]], [[Mohammed Labbi]], _Highly connected manifolds of positive $p$-curvature_, Transactions of the AMS, Trans. Amer. Math. Soc. 366 (2014), 3405-3424 &lbrack;[arXiv:1201.1849](http://arxiv.org/abs/1201.1849), [doi:10.1090/S0002-9947-2014-05939-4](https://doi.org/10.1090/S0002-9947-2014-05939-4)&rbrack;

[[!redirects 2-Spin bordism]]
[[!redirects 2-spin cobordism]] 
[[!redirects 2-Spin cobordism]]

[[!redirects 2-spin bordisms]]
[[!redirects 2-Spin bordisms]]
[[!redirects 2-spin cobordisms]] 
[[!redirects 2-Spin cobordisms]]

[[!redirects 2-spin bordism group]] 
[[!redirects 2-Spin bordism group]]
[[!redirects 2-spin bordism groups]] 
[[!redirects 2-Spin bordism groups]]
[[!redirects 2-spin bordism ring]] 
[[!redirects 2-Spin bordism ring]]

[[!redirects 2-spin bordism homology]] 
[[!redirects 2-Spin bordism homology]]
[[!redirects 2-spin bordism homology theory]] 
[[!redirects 2-Spin bordism homology theory]]

[[!redirects 2-spin cobordism cohomology]] 
[[!redirects 2-Spin cobordism cohomology]]
[[!redirects 2-spin cobordism cohomology theory]] 
[[!redirects 2-Spin cobordism cohomology theory]]