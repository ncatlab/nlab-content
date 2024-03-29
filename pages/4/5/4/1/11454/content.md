
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For $S$ a [[scheme]], a _cubic curve_ over $S$ is a scheme $p \colon X \to S$ over $S$ equipped with a [[section]] $e \colon S \to X$ and such that [[Zariski topology|Zariski locally]] on $S$, $X$ is given by a solution in [[projective space]] $\mathbb{P}_S^2$ of an [[equation]] of the form

$$
  y^2 + a_1 x y = x^3 + a_2 x^2 + a_4 x + a_6
$$

(the _Weierstrass equation_) such that $e \colon S \to X$ is the line at infinity.

Equivalently this says that $p$ is a [[proper morphism|proper]] [[flat morphism]] with a section contained in the [[smooth locus]] whose [[fibers]] are geometrically integral curves of [[arithmetic genus]] one.

A [[non-singular algebraic variety|non-singular]] solution to this equation is an [[elliptic curve]] (see there for more).
Write $\mathcal{M}_{cub}$ for the [[moduli stack]] of such [[cubic curves]]. Then the [[moduli stack of elliptic curves]] is the non-vanishing locus of the [[discriminant]]  $\Delta \in H^0(\mathcal{M}_{cub}, \omega^{12})$

(e.g. [Mathew, section 3](#Mathew))

[[!include moduli stack of curves -- table]]

## Properties

### Covers

There is an eight-fold cover of $\mathcal{M}_{cub}$ [[localization of a ring|localized]] at $2$ ([Mathew 13, section 4.2](#Mathew13)) which is analogous to the canonical 2-fold cover of the moduli stack of formal tori (which gives the $\mathbb{Z}_2$-action on [[KU]] whose [[homotopy fixed points]] are [[KO]]).

## References

Reviews for the case that 2 and 3 are invertible include

* [[Balázs Szendrői]], _Cubic curves: a short survey_  ([pdf](http://people.maths.ox.ac.uk/szendroi/cubic.pdf))

and specifically over the complex numbers:

* {#Hain08} [[Richard Hain]], section 5 of _Lectures on Moduli Spaces of Elliptic Curves_ ([arXiv:0812.1803](http://arxiv.org/abs/0812.1803))


Discussion of the general case in the context of the construction of [[tmf]] is in

* {#Mathew13} [[Akhil Mathew]], _The homology of $tmf$_ ([arXiv:1305.6100](http://arxiv.org/abs/1305.6100))

reviewed in

* {#Mathew} [[Akhil Mathew]], section 3 of: _The homotopy groups of $TMF$_ ([pdf](http://math.mit.edu/~sglasman/tmfhomotopy.pdf))


[[!redirects cubic curves]]

[[!redirects moduli stack of cubic curves]]


[[!redirects Weierstrass equation]]