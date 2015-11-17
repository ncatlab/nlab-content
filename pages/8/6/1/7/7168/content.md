
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

such that for all $v \in V$, $t \in k$

$$
  q(t v) = t^2 q(v)
$$

and the _[[polarization identity|polarization]]_ of $q$

$$
  (v,w) \mapsto q(v+w) - q(v) - q(w) 
$$

is a [[bilinear form]]. 


## Quadratic refinement

Let 

$$
  \langle -,-\rangle
  \colon
  V \otimes V \to k
$$ 

be a [[bilinear form]]. A [[function]] 

$$
  q \colon V \to k

$$ 

is called a **[[quadratic refinement]]** of $\langle -,-\rangle$ if

$$
  \langle v,w\rangle 
    = 
  q(v + w) - q(v) - q(w) + q(0)
$$

for all $v,w \in V$.


If such $q$ is indeed a [[quadratic form]] in that $q(t v) = t^2 q(v)$ then $q(0) = 0$ and

$$
  \langle v , v \rangle = 2 q(v)
  \,.
$$

This means that a quadratic refinement by a [[quadratic form]] always exists when $2 \in k$ is invertible. Otherwise its existence is a non-trivial condition. One way to express quadratic refinements is by [[characteristic elements of a bilinear form]]. See there for more.



## Related concepts

* [[polarization identity]]

* [[Hermitian form]]

* [[completing the square]]

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

* [[Herrmann Minkowski]], _Grundlagen f&#252;r eine Theorie der quadratischen Formen mit ganzzahligen Koeffizienten, M&#233;moires pr&#233;sent&#233;s par divers savants a l'Acad&#180;emie des Sciences de l'institut national de France_, Tome
XXIX, No. 2. 1884.

* [[Herrmann Minkowski]], _Untersuchungen &#252;ber quadratische Formen. Bestimmung der
Anzahl verschiedener Formen, die ein gegebenes Genus enth&#228;lt_, K&#246;nigsberg 1885; Acta Mathematica 7 (1885), 201&#8211;258

See also

* Rudolf Scharlau, _Martin Kneser's work on quadratic forms and algebraic groups_, 2007 ([pdf](http://inst-mat.utalca.cl/qfc2007/Talks/scharlau.pdf))

Course notes include for instance

* _On the relation between quadratic and bilinear forms_ ([pdf](http://www.maths.manchester.ac.uk/~khudian/Etudes/Algebra/quadrform2.pdf))

* _Bilinear and quadratic forms_ ([pdf](http://buzzard.ups.edu/courses/2007spring/projects/ott-paper-revised.pdf))

* section 10 in _Analytic theory of modular forms_ ([pdf](http://www.math.harvard.edu/~jbland/ma259x_notes.pdf))

Quadratic refinements of [[intersection pairing]] in [[cohomology]] is a powerful tool in [[algebraic topology]] and [[differential topology]]. See

* [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_


[[!redirects quadratic form]]
[[!redirects quadratic forms]]


[[!redirects signature of a quadratic form]]

