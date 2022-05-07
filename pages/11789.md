
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

Let 

$$
  \langle -,-\rangle
  \colon
  V \otimes V \to k
$$ 

be a [[bilinear form]]. A ([[quadratic function|quadratic]]) [[function]] 

$$
  q \colon V \to k
$$ 

is called a __quadratic refinement__ of $\langle -,-\rangle$ if

$$
  \langle v,w\rangle = 
  q(v + w) - q(v) - q(w) + q(0)
$$

for all $v,w \in V$.


If such $q$ is indeed a [[quadratic form]] in that $q(t v) = t^2 q(v)$ then $q(0) = 0$ and

$$
  \langle v , v \rangle = 2 q(v)
  \,.
$$

This means that a quadratic refinement by a [[quadratic form]] always exists when $2 \in k$ is invertible. Otherwise its existence is a non-trivial condition. One way to express quadratic refinements is by [[characteristic elements of a bilinear form]]. See there for more.


## Related concepts

* [[cubical structure on a line bundle]]


## References

Quadratic refinements of [[intersection pairing]] in [[cohomology]] is a powerful tool in [[algebraic topology]] and [[differential topology]]. See:

* [[Mike Hopkins]], [[Isadore Singer]], *[[Quadratic Functions in Geometry, Topology, and M-Theory]]*, J. Diff. Geom. **70** (2005) 329-452 $[$[arXiv:math/0211216](https://arxiv.org/abs/math/0211216), [euclid.jdg/1143642908](https://projecteuclid.org/euclid.jdg/1143642908)$]$


[[!redirects quadratic refinement]]
[[!redirects quadratic refinements]]
