+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Theta functions
+--{: .hide}
[[!include theta functions - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

Given a [[Feynman propagator]] $\frac{1}{H}$, then the corresponding _vacuum energy_ $Z$ is the [[logarithm]] of the [[functional determinant]] $det_{reg}$ of $H$

$$
  Z \coloneqq -log\,det_{reg} H
  \,.
$$

## Properties

### In terms of special values of the zeta function
 {#InTermsOfSpecialValuesOfZetaFunctions}

The vacuum energy is equivalently the [[special values of L-functions|special value]] of the  [[zeta function of an elliptic differential operator|zeta function]] $\zeta_H$ of $H$ given by the [[derivative]] at 0:

$$
  Z = -\frac{1}{2}\zeta_H^\prime(0)
  \,.
$$

See at _[zeta function of an elliptic differential operator -- Functional determinant](zeta+function+of+an+elliptic+differential+operator#FunctionalDeterminant)_ for more.

### In terms of the path integral and relation to generating function

Traditionally the vacuum energy is expressed in terms of a hypothetical [[path integral]]. (As opposed to the [above](#InTermsOfSpecialValuesOfZetaFunctions) zeta-function formalization this is not rigorous, but it serves to give the idea of _why_ this is the vacuum energy and the the zeta-function expression may be taken to be the rigorous definition of the path integral heuristics.)

By [[analogy]] with finite-dimensional [[Gaussian integrals]] (see at _[Feynman diagram -- For finitely many degrees of freedom](Feynman+diagram#ForFinitelyManyDegreesOfFreedom)_) one expects that the [[Wick rotation|Wick rotated]] [[vacuum amplitude]] version of the [[path integral]] (no [[field (physics)|field]] insertions, no [[boundary field theory|boundary conditions]]) is

$$
  \underset{\phi \in \mathbf{Fields}}{\int} 
   \exp(- S_H(\phi))
  D\phi
  = 
  (det_reg H)^{-1/2}
  \,.
$$

Therefore 

$$
  log
    \underset{\phi \in \mathbf{Fields}}{\int} 
   \exp(- S_H(\phi))
  D\phi
  =
  -\frac{1}{2}log\, det_{reg} H 
$$

is the [[generating functional]] for [[n-point functions]]. (...)

e.g. ([Scrucca, section 1.6](#Scrucca), [Edelstein 13, page 2](#Edelstein13))


### As holomorphic potential for Determinant line bundle

Regard

$$
  h \coloneqq \frac{1}{2} det_{reg}H
$$

as a hermitian structure on a [[holomorphic line bundle]], hence, locally, as the [[absolute value]]-squared of the unit [[section]] $\phi_i$ of a [[holomorphic line bundle]] with respect to a local trivializing section (see at [[Chern connection]]).

$$
  h|_{U_i} = {\Vert \phi_i \Vert}^2
  \,.
$$

Then this line bundle is the [[determinant line bundle]] of $H$.
([Quillen 85](#Quillen85)), review includes ([Freed 87, p. 18](#Freed87), [Qiu 12, section 2.8.1](#Qiu12)).

The [[Chern connection]] is

$$
  A = \partial log(h) = \partial \frac{1}{2} det_{reg}H = \partial Z
$$

and the [[curvature]] [[differential 2-form]] is 

$$
  F = i \bar \partial\partial Z
  \,.
$$

> eh? Something wrong with the factors of $1/2$ here...

## References

For instance

* {#Scrucca} Claudio Scrucca, section 1.6 in _Advanced quantum field theory_ [pdf](http://itp.epfl.ch/webdav/site/itp/users/181759/public/aqft.pdf)

* {#Edelstein13} [[José Edelstein]], page 2 of _Lecture 8: 1-loop closed string vacuum amplitude_, 2013 ([pdf](http://www-fp.usc.es/~edels/Strings/Lect8Str.pdf))

* {#Quillen85} [[Daniel Quillen]], _Determinants of Cauchy-Riemann Operators over a Riemann Surface_, Functional Anal.
Appl. 19 (1985) 31.

* {#Freed87} [[Daniel Freed]], _On determinant line bundles_, Math. aspects of [[string theory]], ed. S. T. Yau, World Sci. Publ. 1987,  (revised [pdf](http://www.math.utexas.edu/~dafr/Index/determinants.pdf), [dg-ga/9505002](http://arxiv.org/abs/dg-ga/9505002))


* {#Qiu12} Jia Qiu, section 2.8 of _Lecture notes on topological field theory_ [arXiv:1201.5550](http://arxiv.org/abs/1201.5550)