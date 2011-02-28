
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

The _covariant phase space_ of a system in [[physics]] is the [[space]] of all of its [[classical mechanics|classical solutions]]. For any system described by [[Lagrangian]] mechanics this comes canonically equipped with a [[presymplectic structure]]. A proper _phase space_ or _reduced phase space_ is a subspace or [[quotient space]] of the covariant phase space on which the presymplectic structure refines to a [[symplectic manifold|symplectic structure]] or [[Poisson manifold|Poisson strucure]]. 

Typically these phase spaces are naturally parameterized by the suitable boundary conditions which uniquely determine the corresponding history of the physical system.

For instance for a [[relativistic particle|particle]] propagating on a [[Riemannian manifold]] $X$ with the usual [[action functional]], a trajectory is uniquely fixed by the position $x \in X$ and the momentum $p \in T^*_x X$ of the particle at a given time. Correspondingly the space of all solutions and hence the phase space of the system may be identified with the [[cotangent bundle]] $T^* X$ of $X$.  
 
Generally the system is defined by [[configuration space]] $X$, then the phase space of the system is given by the [[cotangent bundle]] $T^* X$. However some models are obtained by [[symplectic reduction]]. This way a finite-dimensional phase space can sometimes describe continuous systems (e.g. in hydrodynamics) whch have infinitely many degrees of freedom; that phase space is however not a cotangent bundle of something in general. 


## Definition

Let $\mathbf{H}$ be the ambient [[cohesive (∞,1)-topos]] with a [[natural numbers object]] and equipped with a [[line object]] $\mathbb{A}^1$.

For $C \in \mathbf{H}$ an object thought of as the _(field) configuration space_ or _space of histories_ of a physical system.  An [[action functional]] is a morphism

$$
  \exp(i S(-)) : C \to \mathbb{A}^1/\mathbb{Z}
  \,.
$$

The [[Euler-Lagrange equation]] of the system is the corresponding <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#CurvatureCharacteristics">differential characteristic class</a> 

$$
  d \exp(i S) : C \stackrel{\exp(i S(-))}{\to} \mathbb{A}^1/\mathbb{Z}
   \stackrel{}{\to} \mathbf{\flat}_{dR} \mathbf{B}\mathbb{A}^1
  \,.
$$

The **covarian phase space** $P$ of the system -- the solution space of the Euler-Lagrange equations -- is the [[homotopy fiber]] of the  over $0 \in \mathbf{\flat}_{dR} \mathbb{A}^1 $, the [[(∞,1)-pullback]]

$$
  \array{
     P &\to& *
     \\
     \downarrow && \downarrow^{\mathrlap{0}}
     \\
     C &\stackrel{d \exp(i S(-))}{\to}& \mathbf{\flat}_{dR} \mathbf{B}\mathbb{A}^1
  }
  \,.
$$

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

The [[presymplectic structure]] on covariant phase space was first described in

* G. J. Zuckerman, _Action Principles and Global Geometry_ , in Mathematical Aspects of String Theory, S. T. Yau (Ed.), World Scienti&#166;c, Singapore, 1987, pp. 259&#8364;284.

and 

* [[Edward Witten]], _Interacting field theory of open superstrings_ , Nucl. Phys. B276, 291

and further developed in

* C. Crnkovi&#263;, _Symplectic Geometry of the Covariant Phase Space_ , Class. Quant. Grav. 5 (1988) 1557&#128;1575.

A discussion of its application to non-abelian [[gauge theory]] ([[Yang-Mills theory]]) and of [[gravity]] is in 

* C. Crnkovi&#263;, [[Edward Witten]], _Covariant Description of Canonical Formalism in Geometrical Theories_, in Three Hundred Years of Gravitation, S. W. Hawking and W. Israel (Eds.), Cambridge
University Press, Cambridge, 1987, pp. 676&#8364;684. ([pdf](http://www.phys.lsu.edu/classes/spring2006/phys7777/crnkovicwitten.pdf))

A review of covariant phase space theory is in 

* L. Vitagliano, _Secondary calculus and the covariant phase space_ ([pdf](http://diffiety.ac.ru/preprint/2008/02-08.pdf))


Standard textbooks on [[classical mechanics]] include

* [[Vladimir Arnold]], _Mathematical methods of classical mechanics_

* H. Goldstein, _Classical mechanics_

* L. D. Landau, E. M. Lifshitz, _Mechanics_, (vol. I of Course on theoretical physics)

* R. Abraham, J. E. Marsden, _Foundations of mechanics_

* J. E. Marsden, T. Ratiu, _Introduction to mechanics and symmetry_

* wikipedia: [phase space](http://en.wikipedia.org/wiki/Phase_space)

[[!redirects covariant phase space]]