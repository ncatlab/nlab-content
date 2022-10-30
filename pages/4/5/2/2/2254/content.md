
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
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

### Relation to complex oriented cohomology theories

* [[complex oriented cohomology theory]]

## Examples

* [[formal multiplicative group]]

* [[Artin-Mazur formal group]]


## Related concepts

* [[height of a formal group law]]

* [[Lie algebra]], [[Lie group]]

* [[formal groupoid]]

Formal geometry is closely related also to the [[rigid analytic geometry]].


(nlab remark: we should explain connections to the Witt rings, Cartier/Dieudonn&#233; modules).


[[!include infinitesimal and local - table]]


## References

* [[Alexander Grothendieck]] et al. [[SGA]] III, vol. 1, Expose VIIB (P. Gabriel) ETUDE INFINITESIMALE DES SCHEMAS EN GROUPES (part B) 474-560 
 {#Grothendieck}

* [[Benoit Fresse]], _Lie theory of formal groups over an operad_, J. Alg. __202__, 455--511, 1998, [doi](http://dx.doi.org/10.1006/jabr.1997.7280) 
 {#Fresse}

* Shigkaki T&#244;g&#244;, _Note of formal Lie groups_ , American Journal of Mathematics, Vol. 81, No. 3, Jul., 1959 ([JSTOR](http://www.jstor.org/stable/2372919))

* Michiel Hazewinkel, Formal Groups and Applications, [projecteuclid](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183548600)

* Michel [[Demazure, lectures on p-divisible groups]]
 
* [[Daniel Quillen]], on the formal group laws of unoriented and complex cobordism theory, 1969, [projecteuclid](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183530915)

* [[Jacob Lurie]], _Chromatic Homotopy Theory_, Lecture series ([lecture notes](http://www.math.harvard.edu/~lurie/252x.html))
 {#Lurie10}



[[!redirects formal groups]]

[[!redirects formal group scheme]]
[[!redirects formal group schemes]]

[[!redirects formal group law]]
[[!redirects formal group laws]]


