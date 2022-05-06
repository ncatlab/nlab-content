
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Variational calculus
+-- {: .hide}
[[!include variational calculus - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $(X,g)$ a [[pseudo-Riemannian manifold]] and $\Box : C^\infty(X) \to C^\infty(X)$ its [[Laplace operator]], the **wave equation** on $X$ is the [[linear differential equation|linear]] [[differential equation]]

$$
  \Box_g f = 0
  \,.
$$

where $\Box_g$ denotes the _wave operator_ /[[Laplace operator]], a [[hyperbolic differential operator]].

For $m \in \mathbb{R}$ the inhomogenous equation

$$
  \Box_g f = m^2 f
$$

is called the _[[Klein-Gordon equation]]_.

## Properties

### Fundamental solution

On a [[globally hyperbolic spacetime]] the wave equation/Klein-Gordon equation has unique advanced and retarded [[Green functions]].  

Their difference is the [[Peierls bracket]] which gives the [[Poisson bracket]] on the [[covariant phase space]] of the [[free field|free]] [[scalar field]].  This in turn defines the [[Wick algebra]] of the free scalar field, which yields the [[quantization]] of the free scalar field to a [[quantum field theory]].


### Bicharacteristic flow and propagation of singularities

The [[bicharacteristic strips]] of the Klein-Gordon operator are [[cotangent vectors]] along [[lightlike]] [[geodesics]] ([this example](bicharacteristic+flow#BicharachteristicFlowOfKleinGordonOperator)).


## Related concepts

* [[wave]]

* [[plane wave]], 

  [[wave vector]], [[wavelength]], [[frequency]]

* [[scalar field]]

* [[Green's function]]

* [[Feynman propagator]]

* [[spectral geometry]], [[hearing the shape of a drum]]

* [[heat equation]]

* [[Klein-Gordon equation]]

* [[Schrödinger equation]]

* [[Dirac equation]]


## References

* F. Friedlander, _The Wave Equation on a Curved Space-Time_, Cambridge: Cambridge University Press, 1975

* {#BaerGinouxPfaeffle07} [[Christian Bär]], [[Nicolas Ginoux]], [[Frank Pfäffle]], _Wave Equations on Lorentzian Manifolds and Quantization_, ESI Lectures in Mathematics and Physics, European Mathematical Society Publishing House, ISBN 978-3-03719-037-1, March 2007, Softcover ([arXiv:0806.1036](https://arxiv.org/abs/0806.1036))

* {#Ginoux08} [[Nicolas Ginoux]], _Linear wave equations_,  Ch. 3 in [[Christian Bär]], [[Klaus Fredenhagen]], _Quantum Field Theory on Curved Spacetimes: Concepts and Methods_, Lecture Notes in Physics, Vol. 786, Springer, 2009 


* [[Sergiu Klainerman]], chapter 4, section 3 of _Lecture notes in analysis_, 2011 ([pdf](https://web.math.princeton.edu/~seri/homepage/courses/Analysis2011.pdf))


[[!redirects wave equations]]


[[!redirects wave operator]]
