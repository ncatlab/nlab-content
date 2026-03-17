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

A *2-oriented bordism* is a [[B-bordism]] for the [[tangential structure]] ([[(B,f)-structure]]) being the [[2-orientation]]. Its [[bordism homology theory]] and [[cobordism cohomology theory]] are described by the [[Thom spectrum]] [[M2-Orient]]. Its definition is fully analogous to that of similar bordisms like [[oriented bordism]]. Similarily, there are *2-oriented bordism groups* and the *2-oriented bordism ring*:
$$
\Omega_n^{2\text{-}Orient}
\coloneqq\pi_n M2\text{-}Orient
=\lim_{k\rightarrow\infty}\pi_{n+k} M2\text{-}Orient_k;
$$
$$
\Omega^{2\text{-}Orient}
\coloneqq\bigoplus_{n\in\mathbb{N}}\Omega_n^{2\text{-}Orient}.
$$

## Properties

\begin{proposition}
Every $n$-dimensional [[2-orient manifold]] is 2-orient bordant to a $\min\left\{9,\left\lceil\frac{n}{2}-1\right\rceil\right\}$-[[n-connected space|connected]] [[2-orient manifold]], equivalently meaning that every 2-orient bordism homology class in $\Omega_n^{2\text{-}Orient}$ can be represented by such a [[2-orient manifold]]. (For $n\geq 19$, the result stabilizes at a [[n-connected space|9-connected]] [[2-orient manifold]].)
\end{proposition}

([Botvinnik & Labbi 14, Lem. 3.2 (1)](#BotvinnikLabbi14))

\begin{proposition}
For $n$-dimensional $\min\left\{9,\left\lceil\frac{n}{2}-1\right\rceil\right\}$-[[n-connected space|connected]] [[2-orient manifolds]] $M$ and $N$, a 2-orient bordism $W\colon M\rightsquigarrow N$ exists with $M\hookrightarrow W$ also $\min\left\{9,\left\lceil\frac{n}{2}-1\right\rceil\right\}$-[[n-connected space|connected]].
\end{proposition}

([Botvinnik & Labbi 14, Lem. 3.2 (2)](#BotvinnikLabbi14))

\begin{proposition}
If a $n$-dimensional $k$-[[n-connected space|connected]] [[compact]] [[2-orient manifold]] $M$ with $k\leq 8$ and $n\geq 2k+3$ is 2-orient bordant to another [[compact]] [[2-orient manifold]] $N$, then $M$ can be obtained from $N$ by [[surgery]] of [[codimension]] at least $k+2$.
\end{proposition}

([Botvinnik & Labbi 14, Prop. 3.4](#BotvinnikLabbi14))

## Related concepts

[[!include flavours of cobordism cohomology theories -- table]]

## References

* {#Sati14} [[Hisham Sati]], _Ninebrane structures_ ([arXiv:1405.7686](http://arxiv.org/abs/1405.7686))

* {#BotvinnikLabbi14} [[Boris Botvinnik]], [[Mohammed Labbi]], _Highly connected manifolds of positive $p$-curvature_, Transactions of the AMS, Trans. Amer. Math. Soc. 366 (2014), 3405-3424 &lbrack;[arXiv:1201.1849](http://arxiv.org/abs/1201.1849), [doi:10.1090/S0002-9947-2014-05939-4](https://doi.org/10.1090/S0002-9947-2014-05939-4)&rbrack;
