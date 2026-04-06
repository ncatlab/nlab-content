+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

*Uhlenbeck's compactness theorem* is a theorem about [[sequences]] of (weak [[Yang-Mills field|Yang-Mills]]) [[connections]] with uniformly bounded [[curvature]] having weakly or uniformly [[convergence|convergent]] subsequences up to [[gauge]]. 

This is an important theorem used in the [[compactification]] of the anti self-dual [[Yang-Mills moduli space]] (ASDYM moduli space), which is central to the construction of [[Donaldson invariants]] on [[4-manifolds]] or [[monopole Floer homology]] on [[3-manifolds]]. 

[[Uhlenbeck's singularity theorem]] was also first published in the same journal, *Communications in Mathematical Physics*. In 2019, [[Karen Uhlenbeck]], after whom the theorem is named, became the first woman to be awarded the Abel Prize, in part for her contributions to [[partial differential equations]] and [[gauge theory]].

## Uhlenbeck's weak compactness theorem

Let $X$ be a $n$-[[dimension|dimensional]] [[compact]] [[Riemannian manifold]] and $P\twoheadrightarrow X$ be a [[principal bundle|principal $G$-bundle]] with a [[compact]] [[Lie group]] $G$. Let $1\lt p\lt\infty$ with $p\gt n/2$ and let $(A_m)_{m\in\mathbb{N}}\in\mathcal{A}^{1,p}(P)\coloneqq W^{1,p}(X,Ad(P))\subset L^p(X,Ad(P))$ be a [[sequence]] of [[Sobolev space|Sobolev]] [[principal connections]] with uniform bound for $\|F_{A_m}\|_p$, the [[norm]] of their [[curvatures]]. Then there exists a sequence $u_m\in\mathcal{G}^{2,p}(P)$ of [[gauge transformations]], so that $u_m^*A_m$ [[weak convergence|converges weakly]]. In other words, any $L^p$-[[bounded]] subset of $\mathcal{A}^{1,p}(P)/\mathcal{G}^{2,p}(P)$ is [[weakly compact]].

([Uhlenbeck 82, Theorem 1.5 (3.6)](#Uhlenbeck82compactness) [Wehrheim 03, Theorem A](#Wehrheim03))

## Uhlenbeck's strong compactness theorem

Let $X$ be a $n$-[[dimension|dimensional]] [[compact]] [[Riemannian manifold]] and $P\twoheadrightarrow X$ be a [[principal bundle|principal $G$-bundle]] with a [[compact]] [[Lie group]] $G$. Let $1\lt p\lt\infty$ with $p\gt n/2$ and $p\gt 4/3$ if $n=2$. Let $(A_m)_{m\in\mathbb{N}}\in\mathcal{A}^{1,p}(P)
\coloneqq W^{1,p}(X,Ad(P))\subset L^p(X,Ad(P))$ be a sequence of weak [[Yang-Mills connections]], hence so that:
$$
\int_X\langle F_{A_m},d_{A_m}\beta\rangle d vol_g
=0
$$
for all $m\in\mathbb{N}$ and $\beta\in\mathcal{A}^{1,p}(P)$, with uniform bound for $\|F_{A_m}\|_p$. Then there exists a [[subsequence]], also denoted $(A_m)_{m\in\mathbb{N}}$, and a sequence $u_m\in\mathcal{G}^{2,p}(P)$ of [[gauge transformations]], so that $u_m^*A_m$ [[uniform convergence|converges uniformly]] to a smooth connection $A\in\mathcal{A}(P)$. (Uhlenbeck's strong compactness theorem is not stated explicitly in Uhlenbeck's 1982 paper, but follows from the results within.)

([Wehrheim 03, Theorem E](#Wehrheim03))

## Related concepts

[[!include Yang-Mills theory -- table]]

## References

* {#Uhlenbeck82compactness} [[Karen Uhlenbeck]], _Connections with $L^p$ bounds on curvature_, Communications in Mathematical Physics *83* (1982) 31–42 &lbrack;[doi:10.1007/BF01947069](https://doi.org/10.1007%2FBF01947069)&rbrack;

* {#Waldron18} [[Alex Waldron]], _Uhlenbeck compactness for Yang-Mills flow in higher dimensions_ (2018) &lbrack;[arXiv:1812.10863](https://arxiv.org/abs/1812.10863)&rbrack;

* {#Wehrheim03} [[Katrin Wehrheim]], _Uhlenbeck compactness_, EMS Series of Lectures in Mathematics. Vol. 1 (2003) &lbrack;[doi:10.4171/004](https://ems.press/books/elm/1) [ISBN 978-3-03719-004-3](https://ems.press/books/elm/1)&rbrack;

See also:

* Wikipedia, _[Uhlenbeck's compactness theorem](https://en.wikipedia.org/wiki/Uhlenbeck%27s_compactness_theorem)_

[[!redirects Uhlenbeck compactness theorem]]