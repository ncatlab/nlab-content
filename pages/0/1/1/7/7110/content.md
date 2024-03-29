
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

Smooth _branched $n$-manifolds_ are a generalization of [[smooth manifolds]] which may have ill-defined [[tangent spaces]] at certain "branch loci", where however they are required to have a well defined tangent $n$-plane. 

Branched $n$-manifolds arise for instance as [[quotients]] of [[foliations]]. 

## Definition

Let $X$ be a [[metrizable space]] with

: 1) a collection $\{U_i\}$ of [[closed subsets]] of $X$

: 2) for each $U_i$ a finite collection $\{D_{i j}\}$ of closed subsets of $U_i$

: 3). for each $i$ a map $\p_i:U_i\to D_i^n$ to a closed $n$-[[disk]] of class $C^k$ in $\mathbb{R}^n$

such that

: a) $\cup_i D_{i j}=U_i$ and $\cup_i U^\circ_i =X$

: b) $p_i |_{D_{i j}}$ is a [[homeomorphism]] onto its [[image]] which is a closed $C^k$ n-disk relative to $\partial D_i^n$.

: c) There is a "[[cocycle]]" of [[diffeomorphisms]] $\{\alpha_{i^' i}\}$ of class $C^k$ such that $p_{i^'}=\alpha_{i^',i}\circ p_i$ when defined. The domain of $\alpha_{i^' i}$ is $p_i(U_i\cap U_{i^'})$.

Then $X$ is called **branched n-manifold of class $C^k$**.


This appears as [Williams, def. 1.0 ns](#Williams).

If $X$ satisfies this set of axioms with b) replaced by 

$b_{ns})$ $p_i |_{D_{i j}}$ is a homeomorphisms onto $D_i^n$

$X$ is called **nonsingular branched $n$-manifold of class** $C^k$.

## Related concepts

* [[orbifold]]

## References

* Robert F. Williams, _Expanding attractors_, Publications math&#233;matique d l'IH&#201;S, tome 43 (1974) ([numdam](http://www.numdam.org/item?id=PMIHES_1974__43__169_0))
 {#Williams}

* [[Dusa McDuff]], _Groupoids, branched manifolds and multisections_, J. Symplectic Geom. Volume 4, Number 3 (2006), 259-315 ([project euclid](http://projecteuclid.org/euclid.jsg/1180135649))

Discussion relating to [[orbifolds]] is in 

* [[Dusa McDuff]], _Groupoids, branched manifolds and multisections_ ([arXiv:math/0509664](http://arxiv.org/abs/math/0509664))

[[!redirects branched manifolds]]