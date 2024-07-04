
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea 

The notion of _superconnection_ generalizes the notion of [[connection on a bundle]] from the [[internalization|context]] of [[differential geometry]] to that of [[supergeometry]].

An [[connection on a bundle|ordinary connection on a vectorbundle]] is given by a suitable [[functor]] $P_1(X) \to Vect$ on the [[path groupoid]] of some [[manifold]] $X$ -- its [[parallel transport]] functor. Here a path is a smooth map $I \to X$ from an [[interval]] $I_t = [0,t] \subset \mathbb{R}^1$ to $X$. A _superconnection_ is more generally given by a functor on _superpaths_ in $X$, where a superpath is a map on superintervals $I_{t,theta} \subset \mathbb{R}^{1|1}$.

## Definition

...


## Push-forward 

### Idea 

There is a natural notion of push-forward of superconnections along maps $\pi : Y \to X$ of [[manifold]]s whose [[fibers]] are [[compact space|compact]] [[spin structure|spin manifold]]s. Under this push-forward the different components of a superconnection mix. In particular, the push-forward of an ordinary connection in this sense is in general a superconnection. 

The push-forward of superconnections corresponds to (...details...) the push-forward in [[topological K-theory]] and [[differential K-theory]]. Bismut famously originally found a superconnection formula for the [[Chern character]] of a pushed [[K-theory]] class. See the references below.

### Details 

Let $E \to Y$ be a Hermitian $\mathbb{Z}_2$-graded [[vector bundle]] of finite rank with superconnection $\nabla = \nabla^E + \omega$ with ordinary connection part $\nabla^E$. 

The push-forward of $E$ along $\pi$ is the $\mathbb{Z}_2$-graed  vector bundle $\pi_* E \to X$ of infinite rank whose fiber over $x \in X$ is the space of [[section]]s of the [[tensor product]] of the spin bundle over $Y_x$ and $E_y$

$$
  (\pi_* E)_x = \Gamma(\mathbb{S}(Y/X)_x \otimes E_x)
  \,.
$$

The pushed connection $\pi_* \nabla$ on $\pi_* E$ is given by

$$
  \pi_* \nabla = D^\pi(\nabla^E) + \nabla^{\pi}_{spin}\otimes Id + Id \otimes \nabla^E
  + \frac{1}{4}c^\pi(T^\pi) + \pi_* \omega
 \,.
$$

### Example: push-forward of ordinary connection to point 

So in particular when $X = {*}$ is the [[point]] and $\nabla = \nabla^E$ is an ordinary connection, we find that the push-forward of an ordinary connection on a vector bundle $E$ on a Riemannian spin manifold $Y$ to the point is the [[Dirac operator]] $D(\nabla^E)$ acting on the space of [[section]]s of $E$ and regarded as the odd endomorphism-valued 0-form part of a superconnection on the point.

By Dumitrescu's formula for the parallel transport of a superconnection the parallel transport of this $\pi_*\nabla$ along the ordinary interval $I_{t,0}$ of length $t$ is the endomorphism

$$
  e^{-t D(\nabla^E)^2} : \Gamma(E) \to \Gamma(E)
  \,.
$$

This happens to be the (Euclidean) [[quantum mechanics]] time evolution operator for the [[sigma-model]] given by the spinning particle on $Y$ charged under the connection $\nabla$.

## Related concepts

* [[super parallel transport]]



## References 

The geometric interpretation of superconnections in terms of parallel transport along superpaths is due to

* [[Florin Dumitrescu]], _Superconnections and parallel transport_ ([arXiv](http://arxiv.org/abs/0711.2766))

The algebraic formulation of superconnections as differential operators on the algebra of differential forms with values in endomorphisms of a $\mathbb{Z}_2$-graded [[vector bundle]] is much older, due to

* [[Daniel Quillen]], _Superconnections and the Chern character_, Topology **24**  1 (1985) 89-95

There the notion of a superconnection was introduced as a means to encode the difference of the chern characters of two vector bundles, motivated from [[topological K-theory]].

This was extended to the parameterized ("families") version in

* [[Jean-Michel Bismut]], _The Atiyah-Singer index theorem for families of Dirac operators: Two heat equation proofs_

Bismut also showed that under the push-forward in [[topological K-theory]] superconnections naturally appear even if one starts with just an ordinary [[connection]].

This statement is generalized to a complete notion of push-forward of superconnections from vector bundles on a space $Y$ to vector bundles un a space $X$ along maps $\pi : Y \to X$ in

* [[Alexander Kahle]], _Superconnections and index theory_ ([arXiv](http://arxiv.org/abs/0810.0820), [talk notes](http://ncatlab.org/nlab/show/Oberwolfach+Workshop,+June+2009+--+Strings,+Fields,+Topology#kahle))

More on [[Chern-Weil theory]] of superconnections is in

* Sylvie Paycha, Simon Scott, _Chern-Weil forms associated with superconnections_ ([pdf](http://math.univ-bpclermont.fr/~paycha/articles/PaychaScottfinalproceedings.pdf))

[[!redirects superconnections]]

[[!redirects Bismut superconnection]]
[[!redirects Bismut superconnections]]



