
#Contents#
* table of contents
{:toc}

## Idea

For a suitable [[linear operator]] (say on [[section]] of a [[line bundle]] over a [[Riemann surface]]), its _zeta function_ is the [[sum]] of the $-s$-powers of all its [[eigenvalues]], as a function of $s$. This is analogous to the _[[Riemann zeta function]]_ and the [[Dedekind zeta function]] (or would be if there were something like a [[Laplace operator]] on [[Spec(Z)]]).

## Definition

### The zeta function

Given an [[elliptic differential operator]] with positive lower bound $c$,  write $H$ for its [[self-adjoint extension]] and write 

$$
  0 \lt \lambda_1 \leq \lambda_2 \leq \cdots
$$

for its [[eigenvalues]].

Then the _zeta function_ of $H$ is

$$
  \begin{aligned}
    \zeta_H(s) 
    & \coloneqq 
    tr( H^{-s} )
    \\
    & \coloneqq
    \underoverset{n = 1}{\infty}{\sum} \frac{1}{(\lambda_n)^s}
  \end{aligned}
  \,.
$$

where the [[series]] converges and then extended by [[analytic continuation]] 
(e.g. ([Duistermaat-Guillemin 75 (2.13)](#DuistermaatGuillemin75))).

### Functional determinant and zeta-function regularization

Notice that the first [[derivative]] $\zeta^\prime_H$ of this zeta function is, where the original series converges, given by

$$
  \zeta_H^\prime(s)
  =
  \sum_{n = 1}^\infty \frac{- \ln \lambda_n}{ (\lambda_n)^s}
  \,.
$$



Therefore one says ([Ray-Singer 71](#RaySinger71)) that the _functional determinant_ of $D$ is the exponential of the zeta function of $D$ at 0:

$$
  det H
  \coloneqq
  \exp(- \zeta_H^\prime(0))
  \,.
$$

Via the [[analytic continuation]] involved in defining $\eta_H(0)$ in the first place, this may be thought of as a _regularization_ of the ill-defined  naive definition "prod_n \lambda^n" of the [[determinant]] of $H$. As such functional determinants often appear in [[quantum field theory]] as what is called _zeta function regularization_.

If $H = D^2$ has a square root $D$ (a [[Dirac operator]]-type square root as in [[supersymmetric quantum mechanics]]) then under some conditions on the growth of the eigenvalies, then the functional determinant may also be expressed in terms of the [[eta function]] of $D$ as

$$
  det H 
  =
  det (D^2) 
   = 
  \exp( \frac{\partial}{\partial s}\frac{\partial}{\partial c} \eta_{D}(0))
  \,.
$$

See at _[eta invariant -- Relation to zeta function](eta+invariant#RelationToTheZetaFunction)_ for more on this.

## Examples

### Analytic torsion

The functional determinant of a [[Laplace operator]] of a [[Riemannian manifold]] acting on [[differential n-forms]] is up to a sign in the exponent a factor in what is called the _[[analytic torsion]]_ of the manifold.

## Related concepts

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

## References

### General

* Wikipedia, _[Functional determinant -- Zeta function version](http://en.wikipedia.org/wiki/Functional_determinant#Zeta_function_version)_

* Wikipedia, _[Zeta function regularization](http://en.wikipedia.org/wiki/Zeta_function_regularization)_


* {#DuistermaatGuillemin75} [[Hans Duistermaat]], [[Victor Guillemin]], _The Spectrum of Positive Elliptic Operators and Periodic Bicharacteristics_,Inventiones mathematicae (1975) Volume: 29, page 39-80 ([EuDML](https://eudml.org/doc/142329))

 (see also at _[[Duistermaat-Guillemin trace formula]]_)


* {#Richardson} [[Ken Richardson]], section 3 of _Introduction to the Eta invariant_ ([pdf](http://faculty.tcu.edu/richardson/Seminars/etaInvariant.pdf))

### Functional determinant

* {#RaySinger71} D. Ray,  B.; [[Isadore Singer]], _R-torsion and the Laplacian on Riemannian manifolds_, Advances in Math. 7: 145&#8211;210, (1971) doi:10.1016/0001-8708(71)90045-4, MR 0295381



[[!redirects functional determinant]]
[[!redirects functional determinants]]