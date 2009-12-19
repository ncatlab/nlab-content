<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc} 

##Idea

The **Atiyah Lie algebroid** associated to a $G$-[[principal bundle]] $P$ over $X$ is a [[Lie algebroid]] structure on the [[vector bundle]] $T P/ G$.

The [[Lie groupoid]] that the Atiyah Lie algebroid [[Lie integration|integrates to]] is the [[Atiyah Lie groupoid]]. See there for more background and discussion.

## Definition

Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and let $P \to X$ be a $G$-[[principal bundle]]:

the **Atiyah Lie algebroid sequence** of $P$ is a sequence of [[Lie algebroid]]s

$$
  ad(P) \to at(P) \to T X
  \,,
$$

where 

* $ad(P) = P \times_G \mathfrak{g}$ is the [[adjoint bundle]] of Lie algebras, associated via the [[adjoint action]] of $G$ on its Lie algebra;

* $at(P) := (T P)/G$ is the **Atiyah Lie algebroid**

* $T X$ is the [[tangent Lie algebroid]] of $X$.

The bracket on the sections of $at(P)$ is that inherited from the tangent Lie algebroid of $P$.

## Relation to connections

A splitting $\nabla_{flat} : T X \to at(P)$ of the Atiyah Lie algebroid sequence in the category of [[Lie algebroid]]s is precisely a flat [[connection on a bundle|connection on]] $P$.

To get non-flat connections in the literature one often sees discussed splittings of the Atiyah Lie algebroid sequence in the category just of [[vector bundle]]s. In that case one finds the curvature of the connection precisely as the obstruction to having a splitting even in Lie algebroids.

One can describe non-flat connections without leaving the context of Lie algebroids by passing to higher Lie algebroids, namely $L_\infty$-[[L-infinity-algebroid|algebroids]], in terms of an [[horizontal categorification]] of [[nonabelian Lie algebra cohomology]]:

...


## References

A discussion with an emphasis on the relation to [[connection on a bundle|connections]] and [[Lie 2-algebra]]s is on the first pages of

* Danny Stevenson, Lie 2-algebras and the geometry of gerbes, Unni Namboodiri Lectures 2006 [slides](http://math.ucr.edu/home/baez/namboodiri/stevenson_maclane.pdf)


