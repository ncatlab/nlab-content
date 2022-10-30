
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

The _Klein-Gordon equation_ is the [[equation of motion]] of a [[free field|free]] [[scalar field|scalar]] [[field (physics)|field]].
 
## Definition

Given a [[spacetime]] $(X,g)$ (a [[pseudo-Riemannian manifold]]) and a [[real number]] $m \in \mathbb{R}_{\geq 0}$, then the _Klein-Gordon equation_ is the [[differential equation]] on [[smooth functions]] $\phi \colon X \to \mathbb{R}$ given by

$$
  (\Box_g - m^2 ) \phi = 0
  \,,
$$

where $\Box_g$ denotes the _[[wave operator]]_ on $(X,g)$ (the analog of the [[Laplace operator]] in [[Lorentzian geometry]]).

This is the [[equation of motion]] of the [[free field|free]] [[scalar field]] on $X$, of [[mass]] $m$ and subject to a [[background field]] of [[gravity]] as encoded in the metric $g$.

Sometimes the Klein-Gordon equation is thought of as a [[general relativity|relativistic]] refinement of the [[Schrödinger equation]] (as one passes from the non-relativistic to the [[relativistic particle]]). But this requires some care. A priori the Klein-Gordon equation takes as arguments a [[field (physics)|field]] on [[spacetime]], whereas the Schr&#246;dinger equation takes as argument a [[wave function]] on [[phase space]].

## Properties

### Fundamental solution

On a [[globally hyperbolic spacetime]] the Klein-Gordon equation has unique advanceed and retarded [[Green functions]].  

Their difference is the [[Peierls bracket]] which gives the [[Poisson bracket]] on the [[covariant phase space]] of the [[free field|free]] [[scalar field]].  This in turn defines the [[Wick algebra]] of the free scalar field, which yields the [[quantization]] of the free scalar field to a [[quantum field theory]].

## References

Named after [[Oskar Klein]] and [[Walter Gordon]]. 

* {#BaerGinouxPfaeffle07} [[Christian Bär]], [[Nicolas Ginoux]], [[Frank Pfäffle]], _Wave Equations on Lorentzian Manifolds and Quantization_, ESI Lectures in Mathematics and Physics, European Mathematical Society Publishing House, ISBN 978-3-03719-037-1, March 2007, Softcover ([arXiv:0806.1036](https://arxiv.org/abs/0806.1036))


* {#Ginoux08} [[Nicolas Ginoux]], _Linear wave equations_,  Ch. 3 in [[Christian Bär]], [[Klaus Fredenhagen]], _Quantum Field Theory on Curved Spacetimes: Concepts and Methods_, Lecture Notes in Physics, Vol. 786, Springer, 2009 



[[!redirects Klein-Gordon equations]]

[[!redirects Klein-Gordon operator]]
[[!redirects Klein-Gordon operators]]

