
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Theta functions
+--{: .hide}
[[!include theta functions - contents]]
=--
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
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

A [[modular form]].

The [[Jacobi theta function]] for special values of its arguments...

## Definition

$$
  \eta(\tau) = q^{1/24} \prod_{n=1}^\infty (1-q^n)
$$

for $q \coloneqq e^{2\pi i \tau}$.

## Properties

### As functional determinant of Laplace operator on elliptic curve

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

This kind of expression appears as the [[partition function]] of the [[bosonic string]] (e.g. section 6.4.2 in these lectures: [pdf](http://www.damtp.cam.ac.uk/user/tong/string/six.pdf))

## References

* Wikipedia, _[Dedekind eta function](http://en.wikipedia.org/wiki/Dedekind_eta_function)_

* {#Atiyah87} [[Michael Atiyah]], _The logarithm of the Dedekind $\eta$-function_, Math. Ann. 278, 335-380 (1987) ([pdf](http://www.maths.ed.ac.uk/~aar/papers/atiyahlg.pdf))

See also

* {#Todorov03} [[Andrey Todorov]], _The analogue of the Dedekind eta function for CY threefolds_, 2003 [pdf](http://www.ma.huji.ac.il/conf/crelle.pdf)

[[!redirects Dedekind eta functions]]

[[!redirects Dedekind eta-function]]