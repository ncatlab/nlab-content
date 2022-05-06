
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

For $V$ a [[vector space]] or more generally a $k$-[[module]], then a _quadratic form_ on $V$ is a [[function]]

$$
  q\colon V \to k
$$

which is [[homogeneous function|homogeneous]] of degree 2 in that for all $v \in V$, $t \in k$

$$
  q(t v) = t^2 q(v)
$$

and such that the _[[polarization identity|polarization]]_ of $q$

$$
  (v,w) \mapsto q(v+w) - q(v) - q(w) 
$$

is a [[bilinear form]].

Written entirely in terms of $q$, the axioms for a quadratic form are:

* $q(t v) = t^2 q(v)$,
* $q(t v + w) + t q(v) + t q(w) = t q(v + w) + t^2 q(v) + q(w)$,
* $q(u + v + w) + q(u) + q(v) + q(w) = q(u + v) + q(u + w) + q(v + w)$.

(Besides the homogeneity, these come from two requirements of a bilinear form to preserve scalar multiplication and addition, respectively.)  So we may alternatively define a __quadratic form__ to be a map $q\colon V \to k$ satisfying these three axioms.

A more general __quadratic map__ (or _homogeneous_ quadratic map to be specific) between vector spaces $V$ and $W$ is a map $q\colon V \to W$ that satisfies the above three conditions.  (Then an _affine_ quadratic map is the sum of a homogeneous quadratic map, a [[linear map]], and a constant, just as an [[affine linear map]] is the sum of a linear map and a constant.)

From the converse point of view, $q$ is a [[quadratic refinement]] of the bilinear form $(-,-)$.  (This always exists uniquely if $2 \in k$ is invertible, but in general the question involves the [[characteristic elements of a bilinear form|characteristic elements]] of $(-u,-)$.  See there for more.)

Quadratic forms with values in the [[real numbers]] $k = \mathbb{R}$ are called _positive definite_ or _negative definite_ if $q(v) \gt 0$ or $q(v) \lt 0$, respectively, for all $v \neq 0$.  See [[definiteness]] for more options.


## Related concepts

* [[linear function]]

* [[polarization identity]]

* [[bilinear form]]

* [[sesquilinear form]]

* [[symplectic form]], [[Kähler form]], [[Hermitian form]]

* [[completing the square]]

* [[quadratic refinement]]

* [[signature of a metric]]

* [[polynomial observable]]


## References
 {#References}

The theory of quadratic forms emerged as a part of (elementary)
[[number theory]], dealing with quadratic [[diophantine equations]], initially
over the rational integers

The terminology "form" possibly originated with 

* [[Leonhard Euler]],  _Novae demonstrations circa divisors numerorum formae $x x + n y y$..._, Acad. Petrop. recitata, Nov 20, 1775, published poshumously

(which is cited as such in [Gauss 1798, paragraph 151](#Gauss1798)).


First classification results for forms over the [[integers]] were due to 

* {#Gauss1798} [[Carl Gauss]], section V of _[[Disquisitiones Arithmeticae]]_, 1798

(which speaks of _formas secundi gradus_)

* [[Hermann Minkowski]], _Grundlagen f&#252;r eine Theorie der quadratischen Formen mit ganzzahligen Koeffizienten, M&#233;moires pr&#233;sent&#233;s par divers savants a l'Acad&#180;emie des Sciences de l'institut national de France_, Tome XXIX, No. 2. 1884.

* [[Hermann Minkowski]], _Untersuchungen &#252;ber quadratische Formen. Bestimmung der Anzahl verschiedener Formen, die ein gegebenes Genus enth&#228;lt_, K&#246;nigsberg 1885; Acta Mathematica 7 (1885), 201&#8211;258

See also

* Rudolf Scharlau, _Martin Kneser's work on quadratic forms and algebraic groups_, 2007 ([pdf](http://inst-mat.utalca.cl/qfc2007/Talks/scharlau.pdf))

Course notes include for instance

* _On the relation between quadratic and bilinear forms_ ([pdf](http://www.maths.manchester.ac.uk/~khudian/Etudes/Algebra/quadrform2.pdf))

* _Bilinear and quadratic forms_ ([pdf](http://buzzard.ups.edu/courses/2007spring/projects/ott-paper-revised.pdf))

* section 10 in _Analytic theory of modular forms_ ([pdf](http://www.math.harvard.edu/~jbland/ma259x_notes.pdf))

Quadratic refinements of [[intersection pairing]] in [[cohomology]] is a powerful tool in [[algebraic topology]] and [[differential topology]]. See

* [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_

See also 

* Wikipedia, _[Quadratic form](https://en.wikipedia.org/wiki/Quadratic_form)_

* Wikipedia, _[Definite quadratic form](https://en.wikipedia.org/wiki/Definite_quadratic_form)_


[[!redirects quadratic form]]
[[!redirects quadratic forms]]

[[!redirects quadratic map]]
[[!redirects quadratic maps]]

[[!redirects quadratic function]]
[[!redirects quadratic functions]]

[[!redirects signature of a quadratic form]]
[[!redirects signatures of a quadratic form]]
[[!redirects signatures of quadratic forms]]

[[!redirects positive definite quadratic form]]
[[!redirects positive definite quadratic forms]]

[[!redirects negative definite quadratic form]]
[[!redirects negative definite quadratic forms]]

[[!redirects positive quadratic form]]
[[!redirects positive quadratic forms]]

[[!redirects negative quadratic form]]
[[!redirects negative quadratic forms]]
