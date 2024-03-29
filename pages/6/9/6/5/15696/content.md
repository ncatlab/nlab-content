
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Theta functions
+--{: .hide}
[[!include theta functions - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In the context of [[regularization (physics)|regularization in physics]], _zeta function regularization_ is a method/prescription for extracing finite values for [[traces]] of powers of [[Laplace operators]]/[[Dirac operators]] by 

1. considering $s$-powers for all values of $s$ in the [[complex plane]] where the naive trace does make sense and then 

1. using [[analytic continuation]] to obtain the desired [[special values of L-functions|special value]] at $s = 1$ -- as for [[zeta functions]].


### Analytic regularization of propagators

One speaks of _analytic regularization_ ([Speer 71](#Speer71)) or _zeta function regularization_ (e.g. [M 99](#M99), [BCEMZ 03, section 2](#BCEMZ03)) if a [[Feynman propagator]]/[[Green's function]] for a [[boson|bosonic]] [[field (physics)|field]], which is naively given by the expression
"$Tr\left(\frac{1}{H}\right)$" (for $H$ the given [[wave operator]]/[[Laplace operator]]) is made well defined by interpreting it as the [[principal value]] of the [[special values of L-functions|special value]] at $s= 1$ 

$$
  Tr_{reg}
  \left(\frac{1}{H}\right)
  \coloneqq
  pv\, \zeta_H(1)
$$

of the [[zeta function of an elliptic differential operator|zeta function]] which is given by the expression


$$
  \zeta_H(s) 
    \coloneqq 
  Tr\left(
    \frac{1}{H}
  \right)^s
$$ 

for all values of $s \in \mathbb{C}$ for which the right hand side exists, and is defined by [[analytic continuation]] elsewhere.


Analogously the zeta function regularization of the [[Dirac propagator]] for a [[fermion]] [[field (physics)|field]] with [[Dirac operator]] $D$ is defined by

$$
  Tr_{reg}
  \left(\frac{D}{D^2} \right)
  \coloneqq
  pv\, \eta_D(1)
$$

where $\eta$ is the [[eta function]] of $D$.

### Functional determinants

Notice that the first [[derivative]] $\zeta^\prime_H$ of this [[zeta function of an elliptic differential operator|zeta function]] is, where the original series converges, given by

$$
  \zeta_H^\prime(s)
  =
  \sum_{n = 1}^\infty \frac{- \ln \lambda_n}{ (\lambda_n)^s}
  \,.
$$


Therefore the _[[functional determinant]]_ of $H$ ([Ray-Singer 71](#RaySinger71)) is the exponential of the zeta function of $H$ at 0:

$$
  Det_{reg} H
  \coloneqq
  \exp(- \zeta_H^\prime(0))
  \,.
$$

(see also [BCEMZ 03, section 2.3](#BCEMZ03))

Via the [[analytic continuation]] involved in defining $\zeta_H(0)$ in the first place, this may be thought of as a _[[regularization (physics)|regularization]]_ of the ill-defined  naive definition "$\prod_n \lambda_n$" of the [[determinant]] of $H$. As such functional determinants often appear in [[quantum field theory]] as what is called _[[zeta function regularization]]_.

### Higher amplitudes

Accordingly, more general [[scattering amplitudes]] are controled by [[multiple zeta functions]] (...).

## Examples

### Of Laplace operator on complex torus and Dedekind eta function

For $\mathbb{C}/(\mathbb{Z}\oplus \tau \mathbb{Z})$
a [[complex torus]] (complex [[elliptic curve]]) equipped with its
standard flat [[Riemannian metric]], then the [[zeta function of an elliptic differential operator|zeta function]] of the corresponding [[Laplace operator]] $\Delta$ is

$$
  \zeta_{\Delta} = (2\pi)^{-2 s} E(s)
   \coloneqq
   (2\pi)^{-2 s} \underset{(k,l)\in \mathbb{Z}\times\mathbb{Z}-(0,0)}{\sum}
  \frac{1}{{\vert k +\tau l\vert}^{2s}}
  \,.
$$

The corresponding [[functional determinant]] is

$$
  \exp(
    E^\prime_{\Delta}(0)
  )
  = (Im \tau)^2 {\vert \eta(\tau)\vert}^4
  \,,
$$

where $\eta$ is the [[Dedekind eta function]]. 

(recalled e.g. in [Todorov 03, page 3](#Todorov03))


### Zeta regularization for divergent integrals ###

the zeta regularizatio method can be extended to include also a regularization for the divergent integrals $ \int_{a}^{\infty}x^{m}dx $ which appears in QFT, this is made by means of the identity

$$\begin{array}{l}
\int_{a}^{\infty }x^{m-s} dx =\frac{m-s}{2} \int_{a}^{\infty }x^{m-1-s} dx +\zeta (s-m)-\sum_{i=1}^{a}i^{m-s}  +a^{m-s}  \\
-\sum_{r=1}^{\infty }\frac{B_{2r} \Gamma (m-s+1)}{(2r)!\Gamma (m-2r+2-s)}  (m-2r+1-s)\int_{a}^{\infty }x^{m-2r-s} dx \end{array}  $$

for the case of $ m=-1$ although the harmonic series has a pole we can regularize by the 2 possibilities

$ \sum_{n=0}^{\infty} \frac{1}{n+a} = -\Psi (a) $ or $ \sum_{n=0}^{\infty} \frac{1}{n+a} = -\Psi (a)+log(a) $ in particular   
$ \sum_{n=1}^{\infty} \frac{1}{n} = \gamma $  Euler-Mascheroni constant, and $ \Psi(a)= -\frac{\Gamma '(a)}{\Gamma (a)} $

So within this reuglarization there wouldn't be any UV ultraviolet divergence
### Analytic torsion

The functional determinant of a [[Laplace operator]] of a [[Riemannian manifold]] acting on [[differential n-forms]] is up to a sign in the exponent a factor in what is called the _[[analytic torsion]]_ of the manifold.



## Related concepts


[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

## References

Original articles include

* {#Speer71} [[Eugene Speer]], _On the structure of Analytic Renormalization_, Comm. Math. Phys. 23, 23-36 (1971) ([Euclid](http://projecteuclid.org/euclid.cmp/1103857549))

* {#RaySinger71} D. Ray, [[Isadore Singer]], _R-torsion and the Laplacian on Riemannian manifolds_, Advances in Math. 7: 145&#8211;210, (1971) doi:10.1016/0001-8708(71)90045-4, MR 0295381


Modern accounts and reviews include

* {#Freed87} [[Daniel Freed]], page 8 of _On determinant line bundles_, Math. aspects of [[string theory]], ed. S. T. Yau, World Sci. Publ. 1987,  (revised [pdf](http://www.math.utexas.edu/~dafr/Index/determinants.pdf), [dg-ga/9505002](http://arxiv.org/abs/dg-ga/9505002))


* {#Elizalde95} [[Emilio Elizalde]], _Ten Physical Applications of Spectral Zeta Functions_ (1995)

* {#M99}  [[Valter Moretti]], _Local z-function techniques vs point-splitting procedures: a few rigorous results_
Commun. Math. Phys. 201, 327 (1999).

* {#BCEMZ03} A. Bytsenko, G. Cognola, [[Emilio Elizalde]], [[Valter Moretti]], S. Zerbini, section 2 of _Analytic Aspects of Quantum Fields_, World Scientific Publishing, 2003, ISBN 981-238-364-6

* {#Robles09} [[Nicolas Robles]], _Zeta function regularization_, 2009 ([[RoblesZetaRegularization.pdf:file]])



See also 

* {#Todorov03} [[Andrey Todorov]], _The analogue of the Dedekind eta function for CY threefolds_, 2003 [pdf](http://www.ma.huji.ac.il/conf/crelle.pdf)

[[!redirects zeta function regularizations]]

[[!redirects functional determinant]]
[[!redirects functional determinants]]

[[!redirects zeta-function regularization]]
[[!redirects zeta-function regularizations]]

