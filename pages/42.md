
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

There are different ways to define a [[volume form|differential volume element]] on a [[smooth manifold]]. Some of these definitions can be carried over to [[supergeometry]], others cannot. The possibly most familiar way of talking about differential volume elements, in terms of top-degree [[differential form]]s, does _not_ carry over to [[supermanifold]]s.



### No top-degree forms in supergeometry 

In supergeometry the notion of _top-degree form_ does not in general make sense, since there are no top-degree wedge powers of "[[superdifferential form|odd 1-forms]]": if for instance $\theta_1$ and $\theta_2$ are odd functions on some [[super Cartesian space]] $\mathbb{R}^{p|q}$ and $d \theta_1$ and $d \theta_2$ are their [[differential 1-forms]], then the wedge product of these is symmetric in that

$$
  d\theta_1 \wedge d \theta_2 = + 
  d\theta_2 \wedge d \theta_1
  \,.
$$

Notice the plus sign on the right, which is the product of one minus sign for interchanging $\theta_1$ and $\theta_2$, and another minus sign for interchanging the two differentials. See at _[[signs in supergeometry]]_ for more on this.

Accordingly, the wedge product of the differential of an odd function $\theta$ with itself does not in general vanish:

$$
  (d \theta \wedge d\theta = 0)
  \Leftrightarrow
  (\theta = 0)
  \,.
$$

On the cartesian supermanifold $\mathbb{R}^{n|m}$ with canonical even coordinate functions $\{x^i\}_1^n$ and canonical odd coordinate functions $\{\theta^j\}_1^m$ the differential form which one would want to regard as the canonical [[volume form]] is

$$
  \omega :=
  d x^1 \wedge \cdots \wedge dx^n \wedge 
  d\theta^1 \wedge \cdots \wedge d\theta^m
  \,.
$$

Due to the above, this is not a _top_ form, since for instance

$$
  \omega \wedge d\theta^1 \neq 0
  \,.
$$

But this example also indicates the solution: apparently for integration it is not really essential that a form is a top power, what is rather essential is that it is, locally, the wedge product of a _basis_ of 1-forms. This perspective then does lead to a sensible definition of volume forms (and more generally "integrable forms") on supermanifolds, described below.

### Solution

Therefore the na&#239;ve identification of differential volume measures with top degree forms has to be refined. The idea is to characterize a volume form by other means, in particular as an equivalence class of choices of [[bases]] for the space of 1-forms, and then to define **integrable forms** to be pairs consisting of such a generalized volume form and a **multivector**: this pair is supposed to represent the differential form one would obtain could one contract the multivector with the volume form, as in ordinary differential geometry.

The definition of integration of integrable forms in supergeometry in terms of multivectorfields leads, in the case that the supermanifold in an [[NQ-supermanifold]] to the [[BV theory|BV formalism]].


## Related concepts

* [[integration]]

* [[Berezin integral]]

## References

An exposition of the standard lore is in

* [[Urs Schreiber]], [_Integration over supermanifolds_](http://www.math.uni-hamburg.de/home/schreiber/sin.pdf)

A general abstract discussion in terms of [[D-module]] theory is in 

* [[Frédéric Paugam]], _Homotopical Poisson Reduction of gauge theories_ ([pdf](http://people.math.jussieu.fr/~fpaugam/documents/homotopical-poisson-reduction-of-gauge-theories.pdf))


Geometric discussion of [[picture number]] appearing in the context of [[integration over supermanifolds]] (and originally seen in the [[quantization]] of the [[NSR superstring]], crucial in [[superstring field theory]]) is due to 

* {#Belopolsky97b} [[Alexander Belopolsky]], _Picture changing operators in supergeometry and superstring theory_ ([arXiv:hep-th/9706033](https://arxiv.org/abs/hep-th/9706033))

and further amplified in 

* {#Witten12} [[Edward Witten]], appendix D of _Notes On Super Riemann Surfaces And Their Moduli_ ([arXiv:1209.2459](http://arxiv.org/abs/1209.2459))

In this perspective picture number is an extra grading on [[differential forms on supermanifolds]] induced from a choice of _integral top-form_ needed to define [[integration over supermanifolds]]:

* {#CatenacciGrassiNoja18} [[Roberto Catenacci]], [[Pietro Grassi]], [[Simone Noja]], _Superstring Field Theory, Superforms and Supergeometry_, Journal of Geometry and Physics Volume 148, February 2020, 103559 ([arXiv:1807.09563](https://arxiv.org/abs/1807.09563))

  (with an eye towards [[superstring field theory]])

* [[C. A. Cremonini]], [[Pietro Grassi]], _Pictures from Super Chern-Simons Theory_ ([arXiv:1907.07152](https://arxiv.org/abs/1907.07152))

  (with an eye towards [[super Chern-Simons theory]])

* [[C. A. Cremonini]], [[Pietro Grassi]], S. Penati, _Supersymmetric Wilson Loops via Integral Forms_ ([arXiv:2003.01729](https://arxiv.org/abs/2003.01729))

  (for super-[[Wilson lines]])

Review: 

* [[Pietro Grassi]], *Integral Forms and Applications*, Sestri Levante 2015 ([pdf](https://agenda.infn.it/event/8823/attachments/55101/64989/Grassi-SL.pdf), [[GrassiIntegralForms2015.pdf:file]])

See also:

* Sergio L. Cacciatori, Simone Noja, Riccardo Re, _The Unifying Double Complex on Supermanifolds_ ([arXiv:2004.10906](https://arxiv.org/abs/2004.10906))


