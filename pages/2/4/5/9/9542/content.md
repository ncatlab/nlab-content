[[!redirects Moyal quantization]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
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

The _Moyal product_ is a [[formal deformation quantization]] of a linear [[Poisson manifold]], hence of a [[vector space]] $V$ equipped with a [[Poisson bivector]] $\pi \in V \wedge V$, regarded as a constant (translation invariant) [[tensor field|bivector field]].

Moyal quantization serves as an intermediate step in quantization of more general situations:

Given a [[symplectic manifold]], then Moyal quantization applies in each [[fiber]] of the [[tangent bundle]]. The resulting [[fiber bundle]] of Moyal algebras admits a [[flat connection]] (non-uniquely) compatible with the algebra structure. The [[covariantly constant sections]] of this Moyal-algebra bundle constitute a [[formal deformation quantization]] of the symplectic manifold, see at _[[Fedosov's deformation quantization]]_.

With a little care, the Moyal construction applies also to infinite-dimensional Poisson vector spaces such as appear in [[local field theory]].  Here the Moyal quantization yields [[formal deformation quantization]] of [[free field theories]] to [[perturbative quantum field theories]], the result are the _[[Wick algebras]]_ of free field theory ([Dito 90](#Dito90), [D&#252;tsch-Fredenhagen 01](#DutschFredenhagen01)). Combining this this with [[Fedosov's deformation quantization]] as above yields [[interaction|interacting]] [[perturbative quantum field theories]] as constructed via [[causal perturbation theory]] ([Collini 16](#Collini16)), see at _[[locally covariant perturbative quantum field theory]]_ for more on this.


## Definition

The Moyal [[star product]] on [[smooth functions]] $C^\infty(V)$ is given on $f,g \in C^\infty(V)$ by

$$
  f \star g \coloneqq prod \circ \exp(\hbar \pi)(f , g)
  \,,
$$

where in the exponent we regard $\pi$ as an [[endomorphism]] on the [[tensor product]] $C^\infty(V) \otimes C^\infty(V)$ by [[differentiation]] in each argument, where the [[exponential]] denotes the corresponding [[formal power series]] of iterated applications of this endomorphism, and where $prod \colon C^\infty(V) \otimes C^\infty(V) \to C^\infty(V)$ is the usual pointwise product of functions.

This means that given a choice of [[basis]] $\{x^i\}_i$ of $V$ such that $\pi$ has components $\{\pi^{i j}\}_{i j}$ in this basis, the resulting [[formal power series]] in the formal parameter $\hbar$ ("[[Planck's constant]]") starts out as

$$
  (f \star g) =
  f \cdot g
  + 
  \hbar 
  \sum_{i,j} \pi^{i j} \frac{\partial f}{\partial x^i}\cdot \frac{\partial g}{\partial x^j}
  + 
  \frac{1}{2}
  \hbar^2
  \sum_{i,j,k, l} \pi^{k l} \pi^{i j} \frac{\partial^2 f}{\partial x^k\partial x^i}\cdot \frac{\partial^2 g}{\partial x^l \partial x^j}
   + 
  \cdots
$$

## Properties

### Integral representation


+-- {: .num_prop #IntegralRepresentationOfStarProduct}
###### Proposition
**([[integral]] representation of [[star product]])**

If the functions $f,g$ admit [[Fourier analysis]] (are [[functions with rapidly decreasing partial derivatives]]), then  their [[star product]] is equivalently given by the following [[integral]] expression:

$$
  \begin{aligned}
  \left(f \star_\omega g\right)(x)
   &= 
  \frac{(det(\omega)^{2n})}{(2 \pi \hbar)^{2n} }
  \int
    e^{ - \tfrac{1}{i \hbar} \omega((x - \tilde y),(x-y))}
    f(y)
    g(\tilde y)
   \,
   d^{2 n} y
   \,
   d^{2 n} \tilde y
  \end{aligned}
$$

=--

([Baker 58](#Baker58), see at _[[star product]]_ [this prop](star+product#IntegralRepresentationOfStarProduct)).


### Via geometric quantization
 {#ViaGeometricQuantization}

The Moyal quantization of a Poisson vector space $(V,\pi)$ arises equivalently as the canonical [[geometric quantization of symplectic groupoids]] of the [[symplectic groupoid]] which is the [[Lie integration]] of the corresponding [[Poisson Lie algebroid]] ([Weinstein 91, p. 446](#Weinstein91), [Garcia-Bondia & Varilly 94, section V](#GBV), [Hawkins 06](#EH)).

See at _[[star product]]_ [this prop.](star+product#PolarizedSymplecticGroupoidConvolutionProductOfSymplecticVectorSpaceIsMoyalStarProduct) for the **proof**; and see at _[geometric quantization of symplectic groupoids -- Examples -- Moyal quantization](geometric+quantization+of+symplectic+groupoids#MoyalQuantizationofPoissonVectorSpace)_ for more. 



## References
 {#References}

The Moyal product was introduced independently in 

* [[Hilbrand Groenewold]], _On the Principles of elementary quantum mechanics_, Physica,12 (1946) pp. 405-460.

* [[José Moyal]], _Quantum mechanics as a statistical theory_. Mathematical Proceedings of the Cambridge Philosophical Society 45: 99 (1949)

The integral expression (prop. \ref{IntegralRepresentationOfStarProduct}) is apparently due to 

* {#Baker58} George A. Baker, _Formulation of Quantum Mechanics Based on the Quasi-Probability Distribution Induced on Phase Space_, Jr. Phys. Rev. 109, 2198 – Published 15 March 1958 ([doi:10.1103/PhysRev.109.2198](https://doi.org/10.1103/PhysRev.109.2198))

General accounts include

* D. B. Fairlie, _Moyal Brackets, Star Products and the Generalised Wigner Function_ ([arXiv:hep-th/9806198](https://arxiv.org/abs/hep-th/9806198))

* Maciej Blaszak, Ziemowit Domanski, _Maciej Blaszak, Ziemowit Domanski_ ([arXiv:1009.0150](https://arxiv.org/abs/1009.0150))


The understanding of the Moyal product as the [[polarization|polarized]] [[groupoid convolution algebra]] of the corresponding [[symplectic groupoid]], hence as an example of [[geometric quantization of symplectic groupoids]] had been suggested without proof in

* {#Weinstein91} [[Alan Weinstein]], p. 446 in P. Donato et al. (eds.) _Symplectic Geometry and Mathematical Physics,  (Birkh&#228;user, Basel, 1991);

and was proven in detail in

* {#GBV} [[José Gracia-Bondia]], [[Joseph Varilly]], _From geometric quantization to Moyal quantization_, J. Math. Phys. 36 (1995) 2691-2701 ([arXiv:hep-th/9406170](http://arxiv.org/abs/hep-th/9406170))

In a broader context this was reconsidered in

* {#EH} [[Eli Hawkins]], example 6.2 of _A groupoid approach to quantization_,  J. Symplectic Geom. Volume 6, Number 1 (2008), 61-125. ([arXiv:math.SG/0612363](http://arxiv.org/abs/math.SG/0612363))

The observation that Moyal deformation quantization applied to the [[Peierls-Poisson  bracket]] yields the [[Wick algebra]] quantization of [[free field theories]] is due to 

* {#Dito90} J. Dito, _Star-product approach to quantum field theory: The free scalar field_. Letters in Mathematical Physics, 20(2):125&#8211;134, 1990 ([spire](https://inspirehep.net/record/303898/))

and was amplified in the broader context of [[perturbative AQFT]] in

* {#DutschFredenhagen01} [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic field theory, and deformation quantization_, in [[Roberto Longo]] (ed.), _Mathematical Physics in Mathematics and Physics, Quantum and Operator Algebraic Aspects_, volume 30 of Fields Institute Communications, pages 151&#8211;160. American Mathematical Society, 2001
  
That moreover the corresponding [[Fedosov deformation quantization]] based on this free field theory star product yields the [[causal perturbation theory]] quantization of interacting field theories is due to 

* {#Collini16} [[Giovanni Collini]], _Fedosov Quantization and Perturbative Quantum Field Theory_ ([arXiv:1603.09626](https://arxiv.org/abs/1603.09626))



[[!redirects Moyal product]]
[[!redirects Moyal products]]

[[!redirects Moyal star-product]]
[[!redirects Moyal star-products]]

[[!redirects Moyal star product]]
[[!redirects Moyal star products]]

[[!redirects Moyal *-product]]
[[!redirects Moyal *-products]]

[[!redirects Moyal star]]

[[!redirects Moyal deformation quantization]]
