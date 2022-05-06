

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[microlocal analysis]] the _propagation of singularities theorem_ ([Duistermaat-H&#246;rmander 72, section 6.1](#DuistermaatHoermander72)) characterizes the [[wave front set]] of a [[distributional solution to a partial differential equation]] in terms of the [[principal symbol]] of the corresponding [[differential operator]]: It says that the singularity wave fronts of the solution propagate along the [[Hamiltonian flow]] of the [[principal symbol]] of the differential operator (its [[bicharacteristic flow]]).

Hence this theorem makes fully manifest how the concept of [[wave front set]] enhances that of [[singular support]] by adding [[direction of a vector|directional]] information about the singularities.

One implication is the proof of existence of solutions to suitable (possibly inhomogeneous) differential equations ([Duistermaat-H&#246;rmander 72, section 6.3](#DuistermaatHoermander72)). 

For example the proof of existence the [[Feynman propagator]] on a [[Lorentzian manifold]] is obtained this way ([Duistermaat-H&#246;rmander 72, theorem 6.5.3 and beginning of section 6.6](#DuistermaatHoermander72), [Radzikowski 96, section 4](#Radzikowski96)).


## Definitions
 {#Definitions}



+-- {: .num_defn #ProperlySupportedPseudoDifferentialOperator}
###### Definition
**([[properly supported peudo-differential operator]])

A [[pseudo-differential operator]] $Q$ on a [[manifold]] $X$ is called _[[properly supported pseudo-differential operator|properly supported]]_ if for each [[compact subset]] $K \subset X$ there exists a compact subset $K' \subset X$ such that for $u$ a [[distribution]] with [[support of a distribution|support]] in $K$ it follows that the [[derivative of distributions]] $Q u$ has support in $K'$ and such that $u\vert_{K'} = 0$ implies $(Q u)\vert_{K} = 0$.

=--

([H&#246;rmander 85 (18.1.21)](#Hoermander85) recalled e.g. in [Radzikowski 96. p. 8,9](#Radzikowski96))

+-- {: .num_example}
###### Example
**([[differential operators]] are properly supported [[pseudo-differential operators]])**

Every ordinary [[differential operator]], regarded as a [[pseudo-differential operator]], is properly supported (def. \ref{ProperlySupportedPseudoDifferentialOperator}), since differential operators do not increase [[support]].

=--


+-- {: .num_defn #SymbolOrder}
###### Definition
**([[symbol order]])**

A [[smooth function]] $q$ on a [[cotangent bundle]] (e.g. [[symbol of a differential operator]]) is of _order $m$_ (and type $1,0$, denoted $q \in S^m = S^m_{1,0}$), for $m \in \mathbb{N}$, if on each [[coordinate chart]] $((x^i), (k_i))$ we have that for every [[compact subset]] $K$ of the base space and all multi-indices $\alpha$ and $\beta$, there is a  [[real number]] $C_{\alpha, \beta,K } \in \mathbb{R}$ such that the [[absolute value]] of the [[partial derivatives]] of $q$ is bounded by


$$
  \left\vert
    \frac{\partial^\alpha}{\partial k_\alpha}
    \frac{\partial^\beta}{\partial x^\beta}
    q(x,k)
  \right\vert  
  \;\leq\;
  C_{\alpha,\beta,K}\left( 1+ {\vert k\vert}\right)^{m - {\vert \alpha\vert}}
$$

for all $x \in K$ and all cotangent vectors $k$ to $x$.

A [[Fourier integral]] operator $Q$ is of _[[symbol class]]_ $L^m = L^m_{1,0}$ if it is of the form

   $$
     Q f (x)
     \;=\;
     \int \int e^{i k \cdot (x - y)} q(x,y,k) f(y) \, d y d k
   $$

with symbol $q$ of order $m$, in the above sense.

=--

([H&#246;rmander 71, def. 1.1.1 and first sentence of section 2.1 with (1.4.1)](#Hoermander71))


+-- {: .num_example}
###### Example

The [[wave operator]]/[[Klein-Gordon operator]] on [[Minkowski spacetime]] is of class $L^2$, according to def. \ref{SymbolOrder}.

=--

## Statement


+-- {: .num_prop #PropagationOfSingularitiesTheorem}
###### Proposition
**(propagation of singularities theorem)**

Let $Q$ be a [[pseudo-differential operator]] on some [[smooth manifold]] $X$ which is [[properly supported pseudo-differential operator|properly supported]] (def. \ref{ProperlySupportedPseudoDifferentialOperator}) and of [[symbol class]] $L^m$ (def. \ref{SymbolOrder}) with real [[principal symbol]] $q$ that is [[homogeneous function|homogeneous]] of degree $m$.

For $u \in \mathcal{D}'(X)$ a [[distribution]] with $Q u = f$, then the [[complement]] of the [[wave front set]] of $u$ by that of $f$ is contained in the set of covectors on which the [[principal symbol]] $q$ vanishes:

$$
  WF(u) \setminus WF(f) \;\subset\; q^{-1}(0)
  \,.
$$

Moreover, $WF(u) \setminus WF(f)$ is invariant under the [[bicharacteristic flow]] induced by the [[Hamiltonian vector field]] of $q$ with respect to the canonical [[symplectic manifold]] structure on the [[cotangent bundle]] ([here](cotangent+bundle#SymplecticStructure)).

=--

([Duistermaat-H&#246;rmander 72, theorem 6.1.1](#DuistermaatHoermander72), recalled e.g. as [Radzikowski 96, theorem 4.6](#Radzikowski96) 

## Examples

+-- {: .num_example #PropagationOfSingularitiesForKleinGordonOperator}
###### Example

For $(X,e)$ a [[globally hyperbolic spacetime]] and $P$ a [[hyperbolic differential operator]] such as the [[wave operator]]/[[Klein-Gordon operator]], then the wave front set of any solution $f$ to $P f = 0$ is a union of [[cotangent vectors]] along [[lightlike]] [[geodesics]] .

=--

+-- {: .proof}
###### Proof

This follows by prop. \ref{PropagationOfSingularitiesTheorem} by the fact that the [[bicharacteristic strips]] of the [[wave operator]]/[[Klein-Gordon operator]] are [[cotangent vectors]] of [[lightlike]] [[geodesics]], by [this example](bicharacteristic+flow#BicharachteristicFlowOfKleinGordonOperator).

=--

## References

The theorem is due to

* {#DuistermaatHoermander72} [[Johann Duistermaat]], [[Lars Hörmander]], _Fourier integral operators II_, Acta Mathematica 128, 183-269, 1972 ([Euclid](https://projecteuclid.org/euclid.acta/1485889724))

discussed in

* {#Hoermander85} [[Lars Hörmander]], _The analysis of partial differential operators III_, Springer 1985


Review in the context of the [[free field|free]] [[scalar field]] on [[globally hyperbolic spacetimes]] (with $Q$ the [[wave operator]]/[[Klein-Gordon operator]]) is in

* {#Radzikowski96} [[Marek Radzikowski]], _Micro-local approach to the Hadamard condition in quantum field theory on curved space-time_, Commun. Math. Phys. 179 (1996), 529&#8211;553 ([Euclid](http://projecteuclid.org/euclid.cmp/1104287114))

which otherwise discusses the corresponding [[Hadamard distributions]].

See also

* {#Hoermander71} [[Lars Hörmander]], _Fourier  integral  operators I._ Acta  Mathematica  127, 79-183 (1971) ([Euclid](https://projecteuclid.org/euclid.acta/1485889699))

[[!redirects propagation of singularities]]
