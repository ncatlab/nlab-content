
#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

A [[Poisson manifold]] may be thought of as a [[Poisson Lie algebroid]], a [[Lie algebroid]] with extra structure: called an [[n-symplectic manifold]] for $n = 1$.

By [[Lie integration]] this Lie algebroid should integrate to a [[Lie groupoid]] with extra structure. Symplectic groupoids are supposed to be these objects that integrate [[n-symplectic manifold]] aka [[Poisson manifold]]s in this sense.

The [[category algebra|groupoid algebra]] of these symplectic groupoids are [[C-star algebra]]s that may be regarded as the [[quantization]] of the original [[Poisson manifold]]. This is described in the references below.

#Definition#

A **symplectic Lie groupoid** is a [[Lie groupoid]] $C$ whose space of [[object]]s is a [[Poisson manifold]] and whose space of [[morphism]]s carries a [[symplectic manifold|symplectic structure]] whose symplectic form $\omega \in \Omega^2_{closed}(Mor(C))$ is _multiplicative_ in that it is closed regarded as an element in the [[simplicial deRham complex]] of the [[nerve]] of $C$:

$$
  0 = d \omega + \delta \omega =
  \delta \omega = pr_1^* \omega - compose^* \omega 
  + pr_2^* \omega
$$

# Properties #


Every [[Lie groupoid]] [[Lie integration|integrating]] a [[Poisson Lie algebroid]] is naturally a symplectic Lie groupoid. Picking always the unique source-simply connected integrating [[Lie groupoid]] produces a [[functor]]

$$
  \Sigma : PoissonManifolds \to SymplecticGroupoids
  \,.
$$

When the [[Poisson manifold]] we start with happens to be a [[symplectic manifold]], then its symplectic Lie groupoid is always the [[fundamental groupoid]] of $X$:

$$
  ((X,\pi) symplectic)
  \;\;\Rightarrow\;\;
  (\Sigma(X,\pi) = \Pi(X))
  \,.
$$

When $X$ is [[fundamental group|simply connected]] such that $\Pi(X)$ is the [[codiscrete category|codiscrete groupoid]] $Pair(X)$ we have that the symplectic form on $Mor(\Pi(X)) = X \times X$ is $\omega \otimes (-\omega)$, for $\omega$ the [[symplectic manifold|symplectic form]] on $X$.

# in geometric quantization of Poisson manifolds #

In the _groupoid approach to quantization_

* Eli Hawkins, _A groupoid approach to quantization_ ([arXiv](http://arxiv.org/abs/math.SG/0612363))

symplectic groupoids are the right tool for thinking about [[geometric quantization]] not of [[symplectic manifold]]s but of just [[Poisson manifold]]s.

A _**symplectic groupoid** in this context is something like a [[groupoid]] [[internalization|internal to]] the [[category]] of [[symplectic manifold]]s

> but beware, there is some fine print, see the references below


The following blog discussion should eventually be copied here:

* [[Urs Schreiber]], 

  * [A Groupoid approach to quantization](http://golem.ph.utexas.edu/category/2008/06/a_groupoid_approach_to_quantiz.html)

  * [Landsman on Quantization of Poisson Algebras Associated to Lie Algebroids](http://golem.ph.utexas.edu/category/2008/06/landsmanon_quantization_of_poi.html)

  * [Eli Hawkins on Geometric Quantization I](http://golem.ph.utexas.edu/category/2008/06/eli_hawkins_on_geometric_quant.html)

  * [Eli Hawkins on Geometric Quantization II](http://golem.ph.utexas.edu/category/2008/06/eli_hawkins_on_geometric_quant_1.html)

#References#

* Eli Hawkins, _A groupoid approach to quantization_ ([arXiv](http://arxiv.org/abs/math.SG/0612363))
