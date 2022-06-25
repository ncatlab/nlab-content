

> This entry is about polarization of [[phase spaces]] (or of any [[symplectic manifold]]) into canonical "position" coordinates and [[canonical momenta]]. Different concepts of a similar name include the _[[polarization identity]]_ (such as in an [[inner product space]] or a [[Jordan algebra]]) or _[[wave polarization]]_ (such as polarized [[light]]). On the other hand, the concept of _[[polarized algebraic variety]]_ is closely related.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Geometric quantization
+-- {: .hide}
[[!include geometric quantization - contents]]
=--
#### Symplectic geometry
+-- {: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}



## Idea

For a [[symplectic manifold]] $(X, \omega)$ regarded as the [[phase space]] of a [[physical system]], a choice of _polarization_ is, locally, a choice of decomposition of the [[coordinates]] on $X$ into "[[canonical coordinates]]" and "[[canonical momenta]]".

The archtypical example is that where $X = T^* \Sigma$ is the [[cotangent bundle]] of a [[manifold]] $\Sigma$. In this case the canonical [[canonical coordinates]] are those parameterizing $\Sigma$ itself, while the canonical [[canonical momenta]] are coordinates on each [[fiber]] of the cotangent bundle.

But for general symplectic manifolds there is no such canonical choice of coordinates and momenta. Moreover, in general there is not even a global notion of canonical momenta. Instead, a choice of (real) polarization is a [[foliation]] of phase space by [[Lagrangian submanifolds]] and then

* the "[[canonical coordinates]]" are coordinates on the corresponding [[leaf space]] (parameterizing the leaves);

* the "[[canonical momenta]]" are coordinates along each [[leaf]]. If there is no _typical leaf_ then this is not a globally defined notion, only the polarization itself is.

Locally this is a choice of [[coordinate patch]] $\phi : \mathbb{R}^{2n} \to X$ such that the [[symplectic form]] takes the form

$$
  \phi^* \omega = \sum_{i = 1}^n \mathbf{d} q^i \wedge \mathbf{d}p_i
$$

where the $\{q^i : \mathbb{R}^{2n} \simeq \mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}\}$ are the canonical coordinates on the first $\mathbb{R}^n$-factor of the [[Cartesian space]] $\mathbb{R}^{2n}$, and where $\{p_o : \mathbb{R}^{2n} \simeq \mathbb{R}^n \times \mathbb{R}^n \to \mathbb{R}\}$ are canonical coordinates  on the second $\mathbb{R}^n$-factor.

## Definition

The traditional notion of polarization applies to a [[symplectic manifold]].

* [Of a symplectic manifold](OfASymplecticManifold)

Symplectic manifold are the lowest step in a tower of notions in [[higher symplectic geometry]] which proceeds with [[n-plectic geometry]] for all $n$ and manifolds refined to [[smooth infinity-groupoids]]. The next simplest cases in this tower are [[symplectic Lie n-algebroids]], which for $n=1$ are [[Poisson Lie algebroids]] and for $n = 2$ are [[Courant Lie 2-algebroids]]:

* [Of a Poisson Lie algebroid](#OfAPoissonLieAlgebroid)

* [Of a Courant Lie 2-algebroid](#OfACourantLie2Algebroid)

* [Of a symplectic Lie n-algebroid](#OfASymplecticLienAlgebroid)

### Of a symplectic manifold
 {#OfASymplecticManifold}

Let $(X, \omega)$ be a [[symplectic manifold]]. 

+-- {: .num_defn #ByLagrangianFoliation}
###### Definition

A **real polarization** of $(X, \omega)$ is a [[foliation]] by [[Lagrangian submanifolds]]. 

=--

For instance ([Weinstein, p. 9](#Weinstein)).

More generally

+-- {: .num_defn }
###### Definition

A **polarization** of $(X,\omega)$ is a choice of involutive [[Lagrangian subspace|Lagrangian subbundle]] $\mathcal{P} \hookrightarrow T_{\mathbb{C}} X$ of of the [[complexification|complexified]] [[tangent bundle]] of $X$.

=--

For instance ([Bates-Weinstein, def. 7.4](#BatesWeinstein))

### Of a Poisson Lie algebroid
 {#OfAPoissonLieAlgebroid}

A [[Poisson Lie algebroid]] $\mathfrak{P}$ is a [[symplectic Lie n-algebroid]] for $n = 1$. Regarding its [[Chevalley-Eilenberg algebra]] as the algebra of functions on a [[dg-manifold]], that dg-manifold carries a graded [[symplectic form]] $\omega$. One can then say

+-- {: .num_defn #ForPoissonLieAlgebroidyByLagrangianFoliation}
###### Definition

A dg-[[Lagrangian submanifold]] of $(\mathfrak{P}, \omega)$ is also called a **$\Lambda$-structure**. ([&#352;evera, section 4](#Severa)).

Hence we might say **real polarization** of $(\mathfrak{P}, \omega)$ is a foliation by dg-Lagrangian submanifolds.

=--

+-- {: .num_prop}
###### Proposition

For $(X, \pi)$ the [[Poisson manifold]] underlying a [[Poisson Lie algebroid]] $(\mathfrak{P}, \omega)$, a dg-Lagrangian submanifold of $(\mathfrak{P}, \omega)$ corresponds to a [[coisotropic submanifold]] of $(X, \pi)$.

=--

([&#352;evera, section 4](#Severa))

+-- {: .num_remark}
###### Remark

The dg-Lagrangian submanifolds also correspond to [[branes]] in the [[Poisson sigma-model]] (see there) on $(\mathfrak{P}, \omega)$. 

=--



### Of a Courant Lie 2-algebroid
 {#OfACourantLie2Algebroid}

A [[Courant Lie algebroid]] $\mathfrak{C}$ is a [[symplectic Lie n-algebroid]] for $n = 2$. Regarding its [[Chevalley-Eilenberg algebra]] as the algebra of functions on a [[dg-manifold]], that dg-manifold carries a graded [[symplectic form]] $\omega$. One can then say

+-- {: .num_defn #ForPoissonLieAlgebroidyByLagrangianFoliation}
###### Definition

A dg-[[Lagrangian submanifold]] of $(\mathfrak{C}, \omega)$ is also called a **$\Lambda$-structure**. ([&#352;evera, section 4](#Severa)).

Hence we might say **real polarization** of $(\mathfrak{C}, \omega)$ is a foliation by dg-Lagrangian submanifolds.

=--

+-- {: .num_prop}
###### Proposition

The dg-Lagrangian submanifolds of a Courant Lie 2-algebroid $(\mathfrak{C}, \omega)$ correspond to [[Dirac structures]] on $(\mathfrak{C}, \omega)$.

=--

([&#352;evera, section 4](#Severa))

### Of a symplectic Lie $n$-algebroid
 {#OfASymplecticLienAlgebroid}

??

### Of an $n$-plectic smooth $\infty$-groupoid

A simple notion of a real polarization for [[2-plectic manifolds]] is 
considered within the context of higher geometric quantization in
[Rogers, Chap. 7](#Rogers).

## Examples

### Real polarizations

(...)

### K&#228;hler polarizations
 {#K&#228;hlerPolarization}

If the  [[symplectic manifold]] $(X,\omega)$ lifts to the structure of a [[Kähler manifold]] $(X, J, g)$, hence with [[Riemannian metric]] $g(-,-) = \omega(-,I(-))$, then the holomorphic/antiholomorphic decomposition induced by the [[complex manifold]] structure is a polarization of $(X,\omega)$. Polarizations of this form are therefore called **[[Kähler polarizations]]**.

### Convex polarizations

* [[p-convex polarization]]

## Related concepts

### Quantum states and wave functions

Upon ([[geometric quantization|geometric]]) [[quantization]] of the physical system described by the [[symplectic manifold]] $(X, \omega)$ a [[quantum state]] is supposed to be a function on $X$ -- or rather a [[section]] of a [[prequantum line bundle]] which is a "wave-function that only depends on the canonical coordinates", not on the canonical momenta. In terms of polarizations this is formalized by saying that a [[space of states (in geometric quantization)|quantum state]] is a section which is [[covariant derivative|covariant constant]] along the [[leaves]] of the polarization (along the "momentum direction"). 

### Bohr-Sommerfeld leaves

After a choice of [[prequantum line bundle]] $\nabla$ lifting $\omega$, a **[[Bohr-Sommerfeld leaf]]** of a (real) polarization is a [[leaf]] on which the prequantum line bundle is not just flat, but also trivializable as a [[circle bundle]] with connection.

### Liouville integrability

If a polarization on an $2n$-dimensional symplectic manifold is generated from $n$ [[Hamiltonian vector fields]] whose [[Hamiltonians]] commute with each other under the [[Poisson bracket]] (and one of them is regarded as that generating time evolution of a mechanical system) then one speaks of a [[Liouville integrable system]].

### Refinement to higher geometric quantization

[[!include infinity-CS theory for binary non-degenerate invariant polynomial - table]]


### Refinement to higher quantization by push-forward

[[!include orientations in higher quantization - table]]

### Other

* [[canonical transformation]]

* [[polarized algebraic variety]]

## References

Lecture notes include 

* [[Alan Weinstein]], _Lectures on Symplectic manifolds_ Lecture 2 _Lagrangian splittings, real and complex polarizations, K&#228;hler manifolds_, CBMS Regional Conference Series in Mathematics, AMS (1977)
 {#Weinstein}

* Sean Bates, [[Alan Weinstein]], _Lectures on the geometry of quantization_, [pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf)
 {#BatesWeinstein}


* Kristin Shaw, _An introduction to polarizations_ ([pdf](http://www.math.toronto.edu/karshon/grad/2006-07/polarizations.pdf))

and section 4 and 5 of 

* [[Matthias Blau]], _Symplectic Geometry and Geometric Quantization_ ([[BlauGeometricQuantization.pdf:file]])
 {#Blau}

or section 5 of 

* A. Echeverria-Enriquez, M.C. Munoz-Lecanda, N. Roman-Roy, C. Victoria-Monge, _Mathematical Foundations of Geometric Quantization_ Extracta Math. 13 (1998) 135-238 ([arXiv:math-ph/9904008](http://arxiv.org/abs/math-ph/9904008))


or

* Yuichi Nohara, _Independence of Polarization
in Geometric Quantization_ ([pdf](http://geoquant2007.mi.ras.ru/nohara.pdf))

Lagrangian submanifolds of [[L-infinity algebroids]] are considered in

* {#Severa} [[Pavol Ševera]], _Some title containing the words "homotopy" and "symplectic", e.g. this one_ ([arXiv:0105080](http://arxiv.org/abs/math/0105080))
 
In the case that the polarization integrates to the [[action]] of a [[Lie group]] $G$ one may think of passing to polarized sections as equivlent to passing to $G$-[[gauge equivalence|gauge equivalence classes]]. This point of view is highlighted in

* [[Gabriel Catren]], _On the Relation Between Gauge and Phase Symmetries_, Foundations of Physics 44 (12):1317-1335 (2014) ([web](http://philpapers.org/rec/CATOTR))

A candidate for polarizations for higher geometric quantization in $n$-plectic geometry is discussed in Chapter 7 of

* {#Rogers} [[Chris Rogers]], _Higher symplectic geometry_ PhD thesis ([arXiv:1106.4068](http://arxiv.org/abs/1106.4068)). 


[[!redirects polarizations]]

[[!redirects canonical coordinate]]
[[!redirects canonical coordinates]]

[[!redirects real polarization]]
[[!redirects real polarizations]]

[[!redirects complex polarization]]
[[!redirects complex polarizations]]

[[!redirects canonical position]]
[[!redirects canonical positions]]
