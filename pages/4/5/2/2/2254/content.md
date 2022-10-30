
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _formal group_ is a [[group object]] [[internalization|internal to]] [[infinitesimal space]]s. More general than [[Lie algebra]]s, which are group objects in _first order infinitesimal_ spaces, formal groups may be of arbitrary infinitesimal order. They sit between [[Lie algebra]]s and finite [[Lie group]]s or [[algebraic group]]s.

Since [[infinitesimal space]]s are typically modeled as [[Isbell duality|formal duals]] to [[algebra]]s, formal groups are typically conceived as group objects in formal duals to [[power series]] algebras.

### Formal group laws

One of the oldest formalisms is the formalism of 
**formal group laws** (early study by Bochner and Lazard), which are a version of representing a group operation in terms of coefficients of the formal power series rings. A __formal group law of dimension__ $n$ is given by a set of $n$ power series $F_i$ of $2n$ variables $x_1,\ldots,x_n,y_1,\ldots,y_n$ such that (in notation $x=(x_1,\ldots,x_n)$, $y=(y_1,\ldots,y_n)$, $F(x,y) = (F_1(x,y),\ldots,F_n(x,y))$) 

$$
F(x,F(y,z))=F(F(x,y),z)
$$

$$
F_i(x,y) = x_i+y_i+\,\,higher\,\,order\,\,terms
$$

Formal group laws of dimension $1$ proved to be important in [[algebraic topology]], especially in the study of [[cobordism]], starting with the works of Novikov, Buchstaber and Quillen; among the generalized cohomology theories the complex cobordism is characterized by the so-called universal group law; moreover the usage is recently paralleled in the theory of [[algebraic cobordism]] of Morel and Levine in [[algebraic geometry]].  Formal groups are also useful in local class field theory; they can be used to explicitly construct the local Artin map according to Lubin and Tate.



### Formal group schemes

Much more general are **formal group schemes** from ([Grothendieck](#Grothendieck))


__Formal group schemes__ are simply the [[group object]]s in a category of [[formal schemes]]; however usually only the case of the formal spectra of complete $k$-algebras is considered; this category is equivalent to the category of complete cocommutative $k$-[[Hopf algebras]]. 

### Formal groups over an operad

For a generalization over [[operads]] see ([Fresse](#Fresse)).



## Properties

### In characteristic 0

+-- {: .num_prop}
###### Proposition

The quotient [[moduli stack]] $\mathcal{M}_{FG} \times Spec \mathbb{Q}$ of formal group over the [[rational numbers]] is isomorphic to $\mathbf{B}\mathbb{G}_m$, the [[delooping]] of the [[multiplicative group]] (over $Spec \mathbb{Q}$). This means that in [[characteristic]] 0 every formal group is determined, up to unique [[isomorphism]], by its [[Lie algebra]].

=--

For instance ([Lurie 10, lecture 12, corollary 3](#Lurie10)).

### Universal formal group

* [[Lazard ring]], [[Quillen's theorem on MU]]

### Relation to complex oriented cohomology theories

* [[complex oriented cohomology theory]]

## Examples

* [[formal multiplicative group]]

* [[Artin-Mazur formal group]] of an [[algebraic variety]],

  * [[formal Picard group]],

  * [[formal Brauer group]]

* [[Lubin-Tate formal group]]

* [[Honda formal group]]

## Related concepts

* [[height of a formal group law]]

* [[p-typical formal group law]]

* [[Morava stabilizer group]]

* [[Landweber exact functor theorem]]

* [[chromatic homotopy theory]]

* [[Lie algebra]], [[Lie group]]

* [[formal groupoid]]


Formal geometry is closely related also to the [[rigid analytic geometry]].


(nlab remark: we should explain connections to the Witt rings, Cartier/Dieudonn&#233; modules).


[[!include infinitesimal and local - table]]


## References

### General

* {#Grothendieck} [[Alexander Grothendieck]] et al. [[SGA]] III, vol. 1, Expose VIIB (P. Gabriel) ETUDE INFINITESIMALE DES SCHEMAS EN GROUPES (part B) 474-560 
 

* {#Fresse} [[Benoit Fresse]], _Lie theory of formal groups over an operad_, J. Alg. __202__, 455--511, 1998, [doi](http://dx.doi.org/10.1006/jabr.1997.7280) 
 

* Shigkaki T&#244;g&#244;, _Note of formal Lie groups_ , American Journal of Mathematics, Vol. 81, No. 3, Jul., 1959 ([JSTOR](http://www.jstor.org/stable/2372919))

* Michiel Hazewinkel, Formal Groups and Applications, [projecteuclid](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183548600)

* Michel [[Demazure, lectures on p-divisible groups]]
 
* [[Jean Dieudonné]], _Introduction to the theory of formal groups_, Marcel Dekker, New York 1973.

* {#Lurie10} [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html)) Lecture 11 _Formal groups_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture11.pdf))

[[Quillen's theorem on MU]] is due to

* {#Quillen69} [[Daniel Quillen]], on the formal group laws of unoriented and complex cobordism theory, 1969, [projecteuclid](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183530915)


### 1-Dimensional formal groups 

A basic introduction is in

* Carl Erickson, _One-dimensional formal groups_ ([pdf](http://people.brandeis.edu/~cwe/pdfs/formal_groups.pdf))

See also

* [[Takeshi Torii]], _One dimensional formal group laws of height $N$ and $N-1$_, PhD thesis 2001 ([pdf](http://mathnt.mat.jhu.edu/mathnew/Thesis/Torii.thesis.pdf))

* [[Takeshi Torii]], _On Degeneration of One-Dimensional Formal Group Laws and Applications to Stable Homotopy Theory_,  American Journal of Mathematics Vol. 125, No. 5 (Oct., 2003), pp. 1037-1077 ([JSTOR](http://www.jstor.org/stable/25099207))

* [[Stefan Schwede]], _Formal groups and stable homotopy of commutative rings_, Geom. Topol. 8 (2004) 335-412 ([arXiv:math/0402372](http://arxiv.org/abs/math/0402372))

The [[moduli stack]] of formal groups and its incarnation as a [[Hopf algebroid]]:

* [[Niko Naumann]], _The stack of formal groups in stable homotopy theory_, Advances in Mathematics Volume 215, Issue 2, 10 November 2007, Pages 569&#8211;600 doi:[10.1016/j.aim.2007.04.007](http://dx.doi.org/10.1016/j.aim.2007.04.007), arXiv:[math.AT/0503308](http://front.math.ucdavis.edu/math.AT/0503308)

[[!redirects formal groups]]

[[!redirects formal group scheme]]
[[!redirects formal group schemes]]

[[!redirects formal group law]]
[[!redirects formal group laws]]