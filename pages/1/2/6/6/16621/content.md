
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
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

Where the [[Chern character]] of a map to $\mathbf{B}U$ (for $U$ the [[stable unitary group]]) is a sum of [[characteristic classes]] corresponding to [[invariant polynomials]], the _odd Chern character_ $ch(g)$ of a map to $g \colon X \to U$ is a sum of the corresponding [[WZW term]] [[curvatures]]

$$
  ch(g) \coloneqq \underoverset{k= 0}{\infty}{\sum} (-1)^k \frac{k!}{(2k+1)!} tr[(g^{-1} d g)^{2k+1}]
  \,,
$$

where $g^{-1}d g \coloneqq g^\ast \theta$ is the [[pullback of differential forms]] along $g$ of the [[Maurer-Cartan form]] on $U$.

The odd Chern character appears in the index theory for [[Toeplitz operators]] and the [[eta invariant]] for even-dimensional manifolds ([Dai-Zhang 12](#DaiZhang12)).

## Related concepts

* [[K-theory]], [[K-homology]], [[index theory]]

## References

* [[Paul Baum]], R. G. Douglas, K-homology and index theory, in Proc. Sympos. Pure
and Appl. Math., Vol. 38, pp. 117-173, Amer. Math. Soc. Providence, 1982.

* [[Ezra Getzler]], _The odd Chern character in cyclic homology and spectral
flow_, Topology, 32(3):489&#8211;507, 1993.

Discussion of the relation to [[index theory]] of [[Toeplitz operators]] and [[eta invariants]] is in 

* {#DaiZhang12} [[Xianzhe Dai]], [[Weiping Zhang]], _Eta invariant and holonomy, the even dimensional case_ ([arXiv:1205.0562](http://arxiv.org/abs/1205.0562))

Discussion of odd [[differential K-theory]] via the odd Chern character is in 

* [[Thomas Tradler]], [[Scott Wilson]], [[Mahmoud Zeinalian]], _An Elementary Differential Extension of Odd K-theory_, J. of K-theory, K-theory and its Applications to Algebra, Geometry, Analysis
and Topology, ([arXiv:1211.4477](http://arxiv.org/abs/1211.4477))

* [[Scott Wilson]], _A loop group extension of the odd Chern character_ ([arXiv:1311.6393](http://arxiv.org/abs/1311.6393))

[[!redirects odd Chern characters]]