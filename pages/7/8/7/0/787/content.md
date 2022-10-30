
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

A **Courant algebroid**  -- or better: **Courant Lie 2-algebroid** -- (named after [[Theodore Courant]]) is precisely a [[symplectic Lie n-algebroid|symplectic Lie 2-algebroid]] ([Roytenberg](#RoytenbergStructure)):

it is a [[L-infinity algebroid|Lie 2-algebroid]] $\mathfrak{P}$ whose [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{P})$ is equipped with the structure of a [[Poisson n-algebra|Poisson 3-algebra]] whose Poisson bracket

$$
  \{-,-\} : CE(\mathfrak{P})\otimes CE(\mathfrak{P})
  \to 
  CE(\mathfrak{P})
$$

of degree -2 in non-degenerate. 

Therefore the [[differential]] $d_{CE(\mathfrak{P})}$ on $CE(\mathfrak{P})$ has a [[Hamiltonian]] with respect to this bracket in that there is an element $\Theta \in CE(\mathfrak{P})$ such that

$$
  d_{CE(\mathfrak{P})} = \{\Theta, -\}
  \,.
$$

## History

The concept of Courant algebroids was originally introduced by [[Irene Dorfman]] and [[Ted Courant]] to study [[geometric quantization]] in the presence of constraints. Later it was considered by Liu, [[Alan Weinstein]] and [[Ping Xu]] in the study of [[double Lie algebroids]].

In these parts of the literature Courant algebroids are considered in the form of [[Lie algebroid]]s with relaxed axioms on the bracket. Even of this type there are two different definitions:

* in one there is a skew-symmetric bracket which fails to satisfy a Jacobi identity by a coherent term -- this is the Courant bracket definition proper;

* in the other there is a bracket which satisfies a Jacobi identity but is skew-symmetric only up to a correction term -- this is the Dorfman version.

So there are several different ways to present the structure encoded in a Courant algebroid. The picture that seems to be emerging is that the _true_ meaning of the notoin of Courant algebroids is given by the notion of [[n-symplectic manifold|2-symplectic manifold]]s.

Moreover, the way [[Lie algebroid]]s may be expressed in terms of [[Lie-Rinehart algebra]]s, Courant algebroids yield [[Courant-Dorfman algebra]]s.


***

(... need to say more about the way the Courant Lie algebroid is obtained from a Lie bialgebroid by derived brackets ...)

***

## Examples

### Lie algebras of compact type

A Courant Lie 2-algebroid over the point is precisely an ordinary [[Lie algebra]] $\mathfrak{g}$ that is equipped with a quadratic and non-degenerate [[invariant polynomial]].

### Standard Courant algebroid and $U(1)$-gerbes

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

* as a [[dg-manifold]] is $\Pi T^* \Pi T X$, the shifted cotangent bundle of the [[shifted tangent bundle]],

  where the [[differential]] is on each local [[coordinate patch]] $\mathbb{R}^n \simeq U \subset X$ with coordinates $\{x^i\}$ in degree 0, $\{d x^i\}$ and $\{\theta_i\}$ in degree 1 and $\{p_i\}$ in degree 2 given by

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

## Properties

### Generalized complex geometry

The study of Courant algebroids is to a large extent known as [[generalized complex geometry]], where the Courant algebroid appears as the [[generalized tangent bundle]].

### Chern-Simons element and Courant $\sigma$-model

As every [[symplectic Lie n-algebroid]] the defining [[invariant polynomial]] on a Courant Lie 2-algebroid transgresses to a cocycle in [[∞-Lie algebroid cohomology]] and this transgression is witnessed by a [[Chern-Simons element]]. The [[schreiber:∞-Chern-Simons theory]] induced by this element is the [[Courant sigma-model]].

### Lagrangian submanifolds and Dirac structures

The [[Lagrangian dg-submanifolds]] of a Courant Lie 2-algebroid corespond to its [[Dirac structures]]. 

## Related concepts

* [[symplectic Lie n-algebroid]]

  * [[symplectic manifold]]

  * [[Poisson Lie algebroid]]
 
  * **Courant algebroid**

* [[Dirac structure]]

* [[Courant sigma-model]]

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]


## References

The original references in order of appearance are

* [[Pavol Severa]], _Letters to A. Weinstein_ ([web](http://sophia.dtp.fmph.uniba.sk/~severa/letters/))

* [[Dmitry Roytenberg]], [[Alan Weinstein]], _Courant algebroids and strongly homotopy Lie algebras_, Lett. Math. Physics __46__(1):81-93, 1998.

* [[Dmitry Roytenberg]], _Courant algebroids, derived brackets and even symplectic supermanifolds_  PhD
thesis, University of California, Berkeley, 1999.
([math.DG/9910078](http://arxiv.org/abs/math.DG/9910078))

* [[Pavol Severa]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_, In Travaux
math&#233;matiques. Fasc. XVI, chapter Trav. Math., XVI, pp. 121-137. Univ. Luxembourg, 2005.

* [[Dmitry Roytenberg]], _On the structure of graded symplectic supermanifolds and Courant algebroids_, pp. 169--185. in Contemporary Mathematics __315__, _Quantization, Poisson brackets and beyond_ (Manchester, 2001), Theodore Voronov, editor, Amer. Math. Soc. 2002.
([arXiv:math/0203110](http://arxiv.org/abs/math/0203110))
{#RoytenbergStructure}

* [[Dmitry Roytenberg]], _Quasi-Lie bialgebroids and twisted Poisson manifolds_ , Letters in Mathematical
Physics, 61(2):123-137 (2002) ([arXiv:math/0112152](http://arxiv.org/abs/math/0112152))

Another useful summary of the theory of Courant algebroids is in [section 3](http://arxiv.org/PS_cache/math/pdf/0401/0401221v1.pdf#page=19) of

* [[Marco Gualtieri]], _Generalized complex geometry_ ([arXiv:math/0401221](http://arxiv.org/abs/math/0401221))

A discussion of Courant algebroids with an eye towards the relation of the [[standard Courant algebroid]] to [[bundle gerbes]] is 

* [[Paul Bressler]], Alexander Chervov, _Courant algebroids_ ([hep-th/0212195](http://arxiv.org/abs/hep-th/0212195))

See also 

* Wikipedia, _[Courant algebroid](http://en.wikipedia.org/wiki/Courant_algebroid)_


The relation between the two different Lie-alebroid-like  definition of Courant algebroids, one with skew, the other with non-skew brackets inspired on the level of [[L-infinity algebra|Lie 2-algebras]] the treatment

* [[Dmitry Roytenberg]], _On weak Lie 2-algebras_ ([arXiv/0712.3461](http://arxiv.org/abs/0712.3461))

Chris Rogers' paper discusses 2-plectic manifolds, manifolds with nondegenerate closed 3 forms and shows that they are related to a special class of Courant algebroids, those that are exact.

* [[Chris Rogers]], _Courant algebroids from categorified symplectic geometry_, ([arXiv:1001.0040](http://arxiv.org/abs/1001.0040))

* [[Chris Rogers]], _2-plectic geometry, Courant algebroids, and categorified prequantization_, ([arxiv:1009.2975](http://arxiv.org/abs/1009.2975))

The relation to [[schreiber:∞-Chern-Simons theory]] is discussed in 

* [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher Chern-Weil Derivation of AKSZ Sigma-Models]]_

[[!redirects Courant Lie algebroid]]
[[!redirects Courant Lie algebroids]]

[[!redirects Courant algebroids]]

[[!redirects Courant Lie 2-algebroid]]
[[!redirects Courant Lie 2-algebroids]]

[[!redirects Courant bracket]]
[[!redirects Courant brackets]]
