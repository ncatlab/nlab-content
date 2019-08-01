

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Topological Yang-Mills theory is a [[gauge theory]] [[topological quantum field theory]] .

## Definition

For $X$ a 4-[[dimensional]] [[smooth manifold]], $\mathfrak{g}$ a [[Lie algebra]] with [[Lie group]] $G$ and $\langle-,-\rangle \in W(\mathfrak{g})$ a binary [[invariant polynomial]] on $\mathfrak{g}$, **topological Yang-Mills theory** is the [[quantum field theory]] defined by the [[action functional]]

$$
  S : G Bund_\nabla(X) \to \mathbb{R}
$$

on the [[groupoid]] of $G$-[[principal bundle]]s with [[connection on a bundle]] that sends a connecton $\nabla$ to the integral of the [[curvature]] 4-form $\langle F_\nabla \wedge F_\nabla \rangle$ of the corresponding [[Chern-Simons circle 3-bundle]]:

$$
  S : \nabla \mapsto \int_X \langle F_A \wedge F_A\rangle
  \,.
$$

## Relation to other models

The ordinary kinetic term of [[Yang-Mills theory]] differs from this by the fact that the [[Hodge star operator]] appears $\langle F_\nabla \wedge \star F_\nabla \rangle$. In full Yang-Mills theory both terms appear.

The topological Yang-Mills action also appears in the [[generalized Chern-Simons theory]] given by a [[Chern-Simons element]] in a [[Lie 2-algebra]], where it is coupled to [[BF-theory]]. See [[Chern-Simons element]] for details.

## Related concepts

* [[theta angle]]

* [[topologically twisted D=4 super Yang-Mills theory]]

## References

The term originates with

* L. Baulieu, [[Isadore Singer]], _Topological Yang-Mills symmetry_, Nuclear Physics B - Proceedings Supplements Volume 5, Issue 2, December 1988, Pages 12-19 (<a href="https://doi.org/10.1016/0920-5632(88)90366-0">doi:10.1016/0920-5632(88)90366-0</a>)

following 

* {#Witten88} [[Edward Witten]], _Topological quantum field theory_, Comm. Math. Phys. Volume 117, Number 3 (1988), 353-386. ([euclid:1104161738](http://projecteuclid.org/euclid.cmp/1104161738))


Review emphasizing the relation to [[Chern-Simons theory]] is

* P van Baal, _An introduction to topological Yang-Mills theory_, Acta Phys.Polon. B21 (1990) 73 ([spire:280417](http://inspirehep.net/record/280417), [pdf](http://www.actaphys.uj.edu.pl/fulltext?series=Reg&vol=21&page=73))

The relation to [[Chern-Simons theory]] on the boundary in an ambient [[string theory|string theoretic]] context is indicated in section 2 (starting around p. 21) of

* {#Witten} [[Edward Witten]], _Fivebranes and Knots_ ([arXiv:1101.3216](http://arxiv.org/abs/1101.3216))
 

On the [[Gribov ambiguity]] in topological Yang-Mills theory:

* D. Dudal, C. P. Felix, O. C. Junqueira, D. S. Montes, A. D. Pereira, G. Sadovski, R. F. Sobreiro, A. A. Tomaz, _Gribov problem in topological Yang-Mills theories_ ([arXiv:1907.05460](https://arxiv.org/abs/1907.05460))

See also

* O. C. Junqueira, A. D. Pereira, G. Sadovski, R. F. Sobreiro, A. A. Tomaz, _Absence of radiative corrections in 4-dimensional topological Yang-Mills theories_, Phys. Rev. D 98, 021701 (2018) ([arXiv:1805.01850](https://arxiv.org/abs/1805.01850))


[[!redirects topological Yang-Mills theories]]
