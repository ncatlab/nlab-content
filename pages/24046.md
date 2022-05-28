
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


\tableofcontents


## Idea

An alternative to [[complete topological vector spaces]] in the framework of [[condensed mathematics]].

Roughly, completeness is expressed as ability to integrate with respect to [[Radon measures]].

This doesn't quite work as stated, and to make this rigorous
one has to bring [[L^p-spaces]] for $0\lt p\le 1$ (i.e., the non-convex case)
into the picture.

## Definition

A [[condensed abelian group]] $V$ is __$p$-liquid__ ($0\lt p\le 1$)
if for every [[compact Hausdorff topological space]] $S$
and every morphism of [[condensed sets]] $f\colon S\to V$
there is a unique morphism of [[condensed abelian groups]]
$M_{\lt p}(S)\to V$ that extends $f$ along the inclusion $S\to M_{\lt p}(S)$.

Here for a [[compact Hausdorff topological space]] $S$
and for any $p$ such that $0\lt p\le 1$ we have
$$M_{\lt p}(S)=\bigcup_{q\lt p}M_q(S),$$
where
$$M_p(S)=\bigcup_{C\gt 0}M(S)_{\ell^p\le C},$$
where
$$M(S)_{\ell^p\le C}=\lim_i M(S_i)_{\ell^p\le C},$$
where $S_i$ are finite sets such that
$$S = \lim_i S_i$$
and
$$M(F)_{\ell^p\le C}$$
for a [[finite set]] $F$ denotes the subset of $\mathbf{R}^F$
consisting of [[sequence]] with [[p-norm|$\ell^p$-norm]] at most $C$.


## Related concepts

* [[solid module]]


## References

See at *[[condensed mathematics]]*.

[[!redirects liquid vector spaces]]
