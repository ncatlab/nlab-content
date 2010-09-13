
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents
{:toc}


## Idea

A **Courant algebroid** is a Lie-algebraic structure encoding a [[n-symplectic manifold|2-symplectic manifold]].

Various different incarnations of this data are considered in the literature. Following Roytenberg's analysis (see below) we may identify a Courant algebroid as a [[Lie infinity-algebroid|Lie 2-algebroid]] that generalizes the notion of [[Poisson Lie algebroid]] to one degree higher:

on its defining [[Chevalley-Eilenberg algebra]] $CE(\Theta)$ exists a graded Poisson bracket $\{-,-\}$ of degree $-2$ and in it a degree 3 element $\Theta$ -- the higher analog of the [[Poisson Lie algebroid|Poisson bivector]] $\pi$ -- such that the differential on $CE(\theta)$ is

$$
  d_{CE(\theta)} = \{\Theta, - \}
  \,.
$$

In the literature, this Lie 2-algebroid perspective on Courant algebroids is not usually considered. Instead, by the [[red herring principle]] what is usually called a Courant algebroid is neither an [[algebroid]] nor in fact in general a [[Lie algebroid]], but is thought of as a generalization of a [[Lie bialgebroid]]: every [[Lie bialgebroid]] induces a Courant algebroid.

The concept of Courant algebroids was originally introduced by Irene Dorfman and Ted Courant to study [[geometric quantization]] in the presence of constraints. Later it was studied by Liu, [[Alan Weinstein]] and Xu in the study of [[double Lie algebroid]]s.

In these parts of the literature Courant algebroids are considered in the form of [[Lie algebroid]]s with relaxed axioms on the bracket. Even of this type there are two different definitions:

* in one there is a skew-symmetric bracket which fails to satisfy a Jacobi identity by a coherent term -- this is the Courant bracket definition proper;

* in the other there is a bracket which satisfies a Jacobi identity but is skew-symmetric only up to a correction term -- this is the Dorfman version.

So there are several different ways to present the structure encoded in a Courant algebroid. The picture that seems to be emerging is that the _true_ meaning of the notoin of Courant algebroids is given by the notion of [[n-symplectic manifold|2-symplectic manifold]]s.

Moreover, the way [[Lie algebroid]]s may be expressed in terms of [[Lie-Rinehart algebra]]s, Courant algebroids yield [[Courant-Dorfman algebra]]s.


***

(... need to say more about the way the Courant Lie algebroid is obtained from a Lie bialgebroid by derived brackets ...)

***

## Standard Courant algebroid and $U(1)$-gerbes

The [[standard Courant algebroid]] of a [[manifold]] $X$ is the one which 

* as a [[vector bundle]] with extra structure is $E = T X\oplus T^* X$, the fiberwise direct sum of the [[tangent bundle]] and the cotangent bundle; with 

  * bilinear form 

    $$
      \langle X + \xi , Y +\eta \rangle = \eta(X) + \xi(Y)
    $$

  for $X,Y \in \Gamma(T X)$ and $\xi, \eta \in \Gamma(T^* X)$

  * brackets

    $$
      [X + \xi, Y + \eta] = [X,Y] + \mathcal{L}_X \eta 
      - \mathcal{L}_Y \xi + \frac{1}{2} d (\eta(X) - \xi(Y))
    $$

    where $\mathcal{L}_X \eta = \{d,\iota_X\} \eta$ denotes the [[Lie derivative]] of the 1-form $\eta$ by the vector field $X$.

* as an [[NQ-supermanifold]] is $\Pi T^* \Pi T X$, the shifted cotangent bundle of the [[shifted tangent bundle]],

  where the differential (homological vector field) is on each local coordinate patch $\mathbb{R}^n \simeq U \subset X$ with coordinates $\{x^i\}$ in degree 0, $\{d x^i\}$ and $\{\theta_i\}$ in degree 1 and $\{p_i\}$ in degree 2 given by

  $$
    \begin{aligned}
      d_C &= d_{dR} + p_i \frac{\partial}{\partial \theta_i}
      \\
      &= dx^i \frac{\partial}{\partial x^i }
       + p_i \frac{\partial}{\partial \theta_i}
    \end{aligned}
    \,.
  $$

Such a standard Courant algebroid may be understood as the higher analog of the  [[Atiyah Lie algebroid]] of a line bundle (...explain...).


## References

A useful place to start reading about Courant algebroids with an emphasis on its Lie-2-algebroid nature (in [[NQ-supermanifold]]-language) is

* [[Dmitry Roytenberg]], _On the structure of graded symplectic supermanifolds and Courant algebroids_ ([arXiv:math/0203110](http://arxiv.org/abs/math/0203110))

This proceeds from the perspective of [[n-symplectic manifold]]s and derives the fact that a 2-symplectic manifold encodes and is encoded by a Courant algebroid.
The last section is about the [[standard Courant algebroid]].

Another useful summary of the theory of Courant algebroids is in [section 3](http://arxiv.org/PS_cache/math/pdf/0401/0401221v1.pdf#page=19) of

* [[Marco Gualtieri]], _Generalized complex geometry_ ([arXiv:math/0401221](http://arxiv.org/abs/math/0401221))


The identification of the [[L-infinity-algebra|Lie 3-algebra]] incarnation of the same date was given by

* [[Dmitry Roytenberg]], [[Alan Weinstein]], _Courant algebroids and strongly homotopy Lie algebras_ ([arXiv:math/9802118](http://arxiv.org/abs/math/9802118))

Equation (9) and theorem 4.3 there gives the [[L-infinity-algebra|Lie 3-algebra]] corresponding to a Courant algebroid (the way the [[tangent Lie algebroid]] gives the [[Lie algebra]] of vector fields). In this perspective the Courant algebroid with base space a point is the [[string Lie 2-algebra]].

This is reviewed and further developed in

* [[Dmitry Roytenberg]], _Courant algebroids, derived brackets and even symplectic supermanifolds_ ([math.DG/9910078](http://arxiv.org/abs/math.DG/9910078))

A discussion of Courant algebroids with an eye towards the relation of the [[standard Courant algebroid]] to [[bundle gerbe]]s is 

* [[Paul Bressler]], [[Alexander Chervov]], _Courant algebroids_ ([hep-th/0212195](http://arxiv.org/abs/hep-th/0212195))

The relation between the two different Lie-alebroid-like  definition of Courant algebroids, one with skew, the other with non-skew brackets inspired on the level of [[L-infinity algebra|Lie 2-algebra]]s the treatment

* [[Dmitry Roytenberg]], _On weak Lie 2-algebras_ ([arXiv/0712.3461](http://arxiv.org/abs/0712.3461))

Chris Rogers paper discusses 2-plectic manifolds, manifolds with nondegenerate closed 3 forms and shows that they are related to a special class of Courant algebroids, those that are exact.

* [[Chris Rogers]] _Courant algebroids from categorified symplectic geometry_, <a href="http://front.math.ucdavis.edu/1001.0040">arXiv:1001.0040v1 [math-ph]</a>

[[!redirects Courant Lie algebroid]]