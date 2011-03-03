
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _covariant phase space_ of a system in [[physics]] is the [[space]] of all of its solutions to its [[classical mechanics|classical equations of motion]], the space of _classical trajectories_ of the system. 

For a system described by [[Lagrangian]] mechanics this comes canonically equipped with a [[presymplectic structure]]. A proper _phase space_ or _reduced phase space_ is a subspace or [[quotient space]] of the covariant phase space on which the presymplectic structure refines to a [[symplectic manifold|symplectic structure]] or [[Poisson manifold|Poisson strucure]]. 

Typically these phase spaces are (locally) naturally parameterized by the suitable boundary conditions which uniquely determine the corresponding history of the physical system. Much of the literature on phase spaces deals with parameterizing these boundary conditions. 

For instance for a [[relativistic particle|particle]] propagating on a [[Riemannian manifold]] $X$ with the usual [[action functional]], a trajectory is uniquely fixed by the position $x \in X$ and the momentum $p \in T^*_x X$ of the particle at a given time. Correspondingly the space of all solutions and hence the (covariant) phase space of the system may be identified with the [[cotangent bundle]] $T^* X$ of $X$.  
 
However, even reduced phase spaces are not all cotangent bundles, typically not, for instance, if they are obtained by [[symplectic reduction]]. This way a finite-dimensional phase space can sometimes describe continuous systems (e.g. in hydrodynamics) whch have infinitely many degrees of freedom; that phase space is however not a cotangent bundle of something in general. 


## Definition

(...)

## Examples

### In dg-geometry

Let the ambient context be that of [[dg-geometry]]. Let $C$ be an ordinary [[smooth manifold]], assumed finite dimensional for the moment, and $\exp(i S) : C \to \mathbb{R}/\mathbb{Z}$ an ordinary [[smooth function]] such that its 0-locus is an sub-manifold.

Then a presentation for the homotopy fiber of $\exp(i S)$ is given by the formal dual of the [[dg-algebra]]

$$
 (\wedge^{-\bullet}_{C^\infty(X)}\Gamma(T X), \iota_{(-)} d \exp(i S))
 \left[
  \cdots \to \wedge_{C^\infty(X)}^2\Gamma(T X) \stackrel{{\iota_{(-)}d \exp(i S)}}{\to} \Gamma(T X) \stackrel{\iota_{(-)}d \exp(i S)}{\to} C^\infty(X) 
  \right]
$$

concentrated in non-positive degree, which in degree $k$ has the $k$th exterior powers of the [[tangent vector]]s of $X$ and whose differential is given by contracting a tangent vector with the 1-form $d \exp(i S)$.  

This is a [[Koszul resolution]]-type resolution of the 0-locus of $\exp(i S)$. More generally, the homotopy fiber is given by a [[Koszul-Tate resolution]]-type complex. This is known as the _antifield complex_ in the [[BV-BRST formalism|BV-BRST formulation]] of derived phase spaces.

## References

An early description of the [[presymplectic structure]] on covariant phase space is in

* G. J. Zuckerman, _Action Principles and Global Geometry_ , in Mathematical Aspects of String Theory, S. T. Yau (Ed.), World Scienti&#166;c, Singapore, 1987, pp. 259&#8364;284.

and 

* [[Edward Witten]], _Interacting field theory of open superstrings_ , Nucl. Phys. B276, 291

and further developed in

* C. Crnkovi&#263;, _Symplectic Geometry of the Covariant Phase Space_ , Class. Quant. Grav. 5 (1988) 1557&#128;1575.

A discussion of its application to non-abelian [[gauge theory]] ([[Yang-Mills theory]]) and of [[gravity]] is in 

* C. Crnkovi&#263;, [[Edward Witten]], _Covariant Description of Canonical Formalism in Geometrical Theories_, in Three Hundred Years of Gravitation, S. W. Hawking and W. Israel (Eds.), Cambridge
University Press, Cambridge, 1987, pp. 676&#8364;684. ([pdf](http://www.phys.lsu.edu/classes/spring2006/phys7777/crnkovicwitten.pdf))

Reviews of covariant phase space theory:

* L. Vitagliano, _Secondary calculus and the covariant phase space_, [pdf](http://diffiety.ac.ru/preprint/2008/02-08.pdf)

* M. J. Gotay, J. Isenberg, R. Montgomery, J. E. Marsden, _Momentum Maps and Classical Fields, Part I: Covariant Field Theory_ [pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.6.6137&rep=rep1&type=pdf)

A discussion in the context of the [[variational bicomplex]] with further pointers to the use in [[physics]] is in 

* E. Reyes, _On Covariant Phase Space and the Variational Bicomplex_ , Int. J. Theor. Phys. 43, no 5 (2004) 1267&#8364;1286

A systematic discussion leading up to the derived covariant phase space by [[BRST-BV formalism]] is in section 8.3 of

* [[Frédéric Paugam]], _Towards the mathematics of quantum field theory_ ([pdf](http://www.math.jussieu.fr/~fpaugam/documents/enseignement/master-mathematical-physics-impa-v01-2011.pdf))
{#Paugam}


Standard textbooks on [[classical mechanics]] include

* [[Vladimir Arnold]], _Mathematical methods of classical mechanics_

* H. Goldstein, _Classical mechanics_

* L. D. Landau, E. M. Lifshitz, _Mechanics_, (vol. I of [[Landau-Lifschitz]] Course on theoretical physics)

* R. Abraham, J. E. Marsden, _Foundations of mechanics_

* J. E. Marsden, T. Ratiu, _Introduction to mechanics and symmetry_

* wikipedia: [phase space](http://en.wikipedia.org/wiki/Phase_space)

[[!redirects covariant phase space]]

[[!redirects phase spaces]]
[[!redirects covariant phase spaces]]
