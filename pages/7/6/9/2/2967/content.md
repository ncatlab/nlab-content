
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A _standard Courant Lie algebroid_ of a [[manifold]] $X$ is a type of [[Courant algebroid]] constructed from the [[tangent bundle]] and cotangent bundle of a manifold. This is the principle algebraic structure studied in [[generalized complex geometry]].

## Definition

Recall from the discussion at [[Courant algebroid]] that there are the following two equivalent definition of Courant algebroids: 

* as a vector bundle equipped with a bracket and a bilinear form on its space of sections, satisfying various identities;

* as a [[L-infinity algebroid|Lie 2-algebroid]] equivalently encoded in its [[Chevalley-Eilenberg algebra]], equivalently the function algebra on a certain type of [[NQ-supermanifold]].

### As a vector bundle with extra structure 

In the first perspective a _standard Courant algebroid_ of a [[manifold]] $X$ is one of the form $E = T X\oplus T^* X$, the fiberwise direct sum of the [[tangent bundle]] and the cotangent bundle; with 

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

### As a Lie 2-algebroid

As an [[NQ-supermanifold]] a standard Courant algeebroid is is $\Pi T^* \Pi T X$, the shifted cotangent bundle of the [[shifted tangent bundle]],

where the differential (homological vector field) is on each local coordinate patch $\mathbb{R}^n \simeq U \subset X$ with coordinates 

* $\{x^i\}$ in degree 0

* $\{d x^i\}$ and $\{\theta_i\}$ in degree 1 

* and $\{p_i\}$ in degree 2 

given by

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

A useful place to start reading about the standard Courant algebroid with an emphasis on its Lie-2-algebroid nature (in [[NQ-supermanifold]]-language) is section 5 of

* [[Dmitry Roytenberg]], _On the structure of graded symplectic supermanifolds and Courant algebroids_ ([arXiv](http://arxiv.org/abs/math/0203110))

