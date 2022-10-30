
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

The _Klein-Gordon equation_ is the [[partial differential equation]] which is the [[equation of motion]] of a [[free field|free]] [[scalar field|scalar]] [[field (physics)|field]] of possibly non-vanishing [[mass]] $m$ on some (possibly [[curved spacetime|curved]]) [[spacetime]] ([[Lorentzian manifold]]): it is the relativistic [[wave equation]] with inhomogenety the mass $m^2$.

The structure of the Klein-Gordon equation appears also in the [[equations of motion]] of richer [[field (physics)|fields]] than just [[scalar fields]], where now the underlying [[field bundle]] may more generally be some [[vector bundle]]. Therefore the [[fundamental solutions]] of the Klein-Gordon equation, called the _[[propagators]]_ (see [below](#FundamentalSolutions)) pervades all of relativistic [[perturbative quantum field theory]].

 
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

### Bicharacteristic flow and propagation of singularities

The [[bicharacteristic strips]] of the Klein-Gordon operator are [[cotangent vectors]] along [[lightlike]] [[geodesics]] ([this example](bicharacteristic+flow#BicharachteristicFlowOfKleinGordonOperator)).


### Fundamental solutions
 {#FundamentalSolutions}

On a [[globally hyperbolic spacetime]] $M$ the Klein-Gordon equation has unique advanced and retarded [[Green functions]], $\Delta_R \in \mathcal{D}'(M\times M)$ and $\Delta_A \in \mathcal{D}'(M\times M)$ respectively.

The retarded and advanced Green functions are uniquely distinguished by their [[support of a distribution|support]] properties. Namely, $(x,y) \in \operatorname{supp} \Delta_R$ only if $x$ is in the [[causal future]] of $y$, while $(x,y) \in \operatorname{supp} \Delta_A$ only if $x$ is in the [[causal past]] of $y$.

Their difference $\Delta_S = \Delta_R - \Delta_A$ is a bisolution known as the [[causal propagator]], which is the [[Peierls bracket]] which gives the [[Poisson bracket]] on the [[covariant phase space]] of the [[free field|free]] [[scalar field]].  This in turn defines the [[Wick algebra]] of the free scalar field, which yields the [[quantization]] of the free scalar field to a [[quantum field theory]].


Other important Green functions or bisolutions include any (anti-)[[Feynman propagator]] ($\Delta_{\bar{F}}$) $\Delta_F$ and [[Hadamard propagator]]. Unfortunately, it is not possible to identify them by a simple support condition. On Minkowski space, they are identified by the support of their Fourier transform. On curved spacetimes, there are two possibilities. One specifies the asymptotic expansion $\Delta(x,y)$ in a geodesically convex neighborhood of the diagonal $x=y$ to be of a special _Hadamard form_. The other specifies constraints on the [[wavefront set]] $WF(\Delta)$. The possibilities were proven to be equivalent in [Radzikowski 96](#Radzikowski96), which made essential use of the relevant notions of microlocal analysis and of _distinguished parametrices_ introduced in [DuistermaatH&#246;rmander 72](#DuistermaatHoermander72).

According to [Radzikowski 96](#Radzikowski96), the constraints on the wavefront sets of important Green functions and bisolutions can be diagrammatically illustrated as follows below. Note that the primed [[wavefront set]] of a distribution on $M\times M$ is defined as $WF'(\Delta) = \{ (x,y;p,-q) \in T^*(M\times M) \mid (x,y;p,q) \in WF(\Delta) \}$. The diagrams illustrate tuples $(x,y; p,q) \in T^*(M\times M)$, where the vertex of a cone corresponds to $y$ and the cone illustrates all points $x$ linked to $y$ by null geodesics; the arrows illustrate the allowed directions of $p$, with $p$ and $q$ linked by parallel transport and both tangent to null geodesic linking $x$ and $y$.


[[!include propagators - table]]

These propagators govern the construction of the [[Wick algebra]] of [[quantum observables]] of the [[free field|free]] [[scalar field]] on the given [[globally hyperbolic spacetime]], as well as the further [[deformation quantization]] to [[interaction|interacting]] [[perturbative quantum field theory]] [[quantum field theory on curved spacetimes|on curved spacetimes]] via [[causal perturbation theory]]. See at _[[locally covariant perturbative quantum field theory]]_ for more on this.


## References

The Klein-Gordon equation is named after [[Oskar Klein]] and [[Walter Gordon]]. 

The [[Hadamard propagator]] for the Klein-Gordon equation was found in

* {#Radzikowski96} [[Marek Radzikowski]], _Micro-local approach to the Hadamard condition in quantum field theory on curved space-time_, Commun. Math. Phys. 179 (1996), 529&#8211;553 ([Euclid](http://projecteuclid.org/euclid.cmp/1104287114))

The original reference on the relevant notions of microlocal analysis and distinguished parametrices of the Klein-Gordon equation is

* {#DuistermaatHoermander72} [[Johann Duistermaat]], [[Lars Hörmander]], _Fourier integral operators. II_, Acta Mathematica 128 (1972), 183-269 ([doi](http://dx.doi.org/10.1007/bf02392165))

Textbook accounts include

* {#BaerGinouxPfaeffle07} [[Christian Bär]], [[Nicolas Ginoux]], [[Frank Pfäffle]], _Wave Equations on Lorentzian Manifolds and Quantization_, ESI Lectures in Mathematics and Physics, European Mathematical Society Publishing House, ISBN 978-3-03719-037-1, March 2007, Softcover ([arXiv:0806.1036](https://arxiv.org/abs/0806.1036))


* {#Ginoux08} [[Nicolas Ginoux]], _Linear wave equations_,  Ch. 3 in [[Christian Bär]], [[Klaus Fredenhagen]], _Quantum Field Theory on Curved Spacetimes: Concepts and Methods_, Lecture Notes in Physics, Vol. 786, Springer, 2009 



[[!redirects Klein-Gordon equations]]

[[!redirects Klein-Gordon operator]]
[[!redirects Klein-Gordon operators]]

