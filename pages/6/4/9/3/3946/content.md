
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

In [[microlocal analysis]], the _wave front set_ ([H&#246;rmander 70](#Hoermander70)) of a [[generalized function]] such as a [[distribution]] or a [[hyperfunction]] is a characterization of the singularity structure of the generalized function, hence of how it deviates from being an ordinary smooth function.

The wave front set is the sub-bundle of the [[cotangent bundle]] that consists of all those [[direction of a vector|directions]] (non-zero [[covectors]]) such that the local [[Fourier transform]] of the distribution is not rapidly decaying in this [[direction of a vector|direction]] ([H&#246;rmander 90, section 8.1](#Hoermander90)).  Such covectors are stable under multiplication by positive scalars, so the wave front set can also be considered as a [[sub-bundle]] of the [[unit sphere bundle]] of the [[cotangent bundle]].

The [[projection]] of the wave front set down to the base space is the [[singular support of a distribution|singular support]] of the distribution. The additional information in the "wave front" [[covectors]] over this singular support may be understood as providing the directions of _propagation of these singularities_. This is made precise by the _[[propagation of singularities theorem]]_

A notorious issue with [[distributions]] is that, when thought of as generalized functions, generally neither their [[composition of distributions]] nor their pointwise [[product of distributions]] is defined. However, closer inspection shows that the [[obstruction]] to these operations being defined for any given pair of distributions is exactly characterized by the wave front set:

For instance the [[product of distributions]] is well defined precisely if the sum of their wave front sets does not intersect the zero-section ([H&#246;rmander 90, theorem 8.2.10](#Hoermander90)).



## Definition

### Motivation

The definition of wavefront sets is motivated by a version of a [[Paley-Wiener theorem]] that characterizes smooth compactly supported functions ($\mathbb{R}^n \to \mathbb{R}$) by a growth condition on their [[Fourier transform]] $\mathcal{F}$:

+-- {: .num_theorem}
###### Theorem
**([[Paley-Wiener-Schwartz theorem]])**


The vector space $C_0^{\infty}(\mathbb{R}^n)$ of [[smooth function|smooth]] [[compact support|compactly supported]] functions ([[bump functions]]) is (algebraically and topologically) [[isomorphism|isomorphic]], via the [[Fourier transform]], to the space of [[entire functions]] $F$ which satisfy the following estimate: there is a positive constant $B$ such that for every [[integer]] $m \gt 0$ there is a constant $C_m$ such that:
$$ 
      F(z) \le C_m (1 + |z|)^{-m} \exp{ (B \; |\operatorname{Im}(z)|)}
$$ 

=--

### Smoothness

We call a smooth compactly supported function that is identically $1$ in a neighbourhood of a point $x_0$ a **cutoff** function at $x_0$.
Let $U \subset \mathbb{R}^n$ be open, we identify the [[cotangent bundle]] of $U$ with $U \times \mathbb{R}^n$. A subset of $U \times \mathbb{R}^n$ is said to be **conic** if it is stable under the transformation
$$
    (x, \zeta) \mapsto (x, \rho \zeta) \quad \text{with} \; \rho \gt 0
$$
Note that a [[conical set|conic]] subset is uniquely determined by its intersection with the [[unit sphere]] bundle $U\times S^{n-1}$.

+-- {: .num_defn}
###### Definition

Let $f$ be a distribution and $(x_0, \zeta_0)$ with $\zeta_0 \neq 0$ be a point of the cotangent bundle of $U$. $f$ is **smooth** in $(x_0, \zeta_0)$ if there is a cutoff function $\chi$ in $x_0$ and an open cone $\Gamma_0$ in $\mathbb{R}^n$ containing $\zeta_0$ such that for every $m \gt 0$ there is a nonnegative constant $C_m$ such that for all $\zeta \in \Gamma_0$:
$$
\| \mathcal{F}(\chi f) (\zeta)   \| \le C_m (1 + \| \zeta \|)^{-m}
$$ 
where $\mathcal{F}(\chi f)$ is the [[Fourier transform]] (of the variable $\zeta$) of the function $\chi f$ (of the variable $x$).

=--


+-- {: .num_defn}
###### Definition

A distribution $f$ is smooth in a [[conical set|conic]] subset $\Gamma$ of the cotangent bundle of $U$ if $f$ is smooth in a neighbourhood of every point in $\Gamma$.

=--


### Wavefront set

Let $U \subseteq \mathbb{R}^n$ be an open subset, $T^* U$ its cotangent bundle and $f$ be a distribution on $U$. The complement of the union of all [[conical set|conic]] subsets of $T^* U$ where $f$ is smooth is the **wavefront set $WF(f)$**.  Since the wavefront set is therefore itself [[conical set|conic]], it is equivalently determined by a subset of the unit sphere bundle of $T^* U$.

([H&#246;rmander 70 (2.4.1)](#Hoermander70), [H&#246;rmander 90, section 8.1](#Hoermander90))

This definition turns out to make invariant sense ([H&#246;rmander 90, p. 256](#Hoermander90)).



## Examples


+-- {: .num_example #WaveFrontOfDeltaDistribution}
###### Example
**(wave front set of [[delta distribution]])**

For $n \in \mathbb{N}$, consider the [[delta distribution]]

$$
  \delta(0) \in \mathcal{D}'(\mathbb{R}^n)
$$

on $n$-dimensional [[Cartesian space]], given by [[evaluation]] at the origin. Its wave front set is

$$
  WF(\delta(0))
  = 
  \left\{
    (0,k)
    \;\vert\;
    k \in \mathbb{R}^n \setminus \{0\}
  \right\}
  \subset
  \mathbb{R}^n \times \mathbb{R}^n
  \simeq
  T^\ast \mathbb{R}^n 
  \,.
$$

=--

+-- {: .proof}
###### Proof

First of all the [[singular support of a distribution|singular support]] of $\delta(0)$ is clearly $singsupp(\delta(0)) = \{0\}$, hence the wave front set vanishes over $\mathbb{R}^n \setminus \{0\}$. 

At the origin, any bump function $b$ supported around the origin with $b(0) = 1$ satisfies $b \cdot \delta(0) = \delta(0)$ and hence the wave front set over the origin is the set of covectors along which the [[Fourier transform of distributions|Fourier transform]] $\hat \delta(0)$ does not suitably decay. But this Fourier transform is in fact a [[constant function]] and hence does not decay in any direction.

=--

+-- {: .num_example #WaveFrontSetOfHeavisideDistribution}
###### Example
**(wave front set of [[Heaviside distribution]])**

Let $H \in \mathcal{D}'(\mathbb{R}^1)$ be the [[Heaviside distribution]] given by

$$
  \langle H, b\rangle \coloneqq \int_0^\infty b(x)\, d x
  \,.
$$

Its wave front set is

$$
  WF(H) = \{(0,k) \vert k \neq 0\}
  \,.
$$

=--


+-- {: .num_example}
###### Example

For $(X,e)$ a [[globally hyperbolic spacetime]] and $P$ a [[hyperbolic differential operator]] such as the [[wave operator]]/[[Klein-Gordon operator]], then the [[propagation of singularities theorem]] says that the wave front set of any solution $f$ to $P f = 0$ is a union of [[lightlike]] [[geodesics]] and their [[cotangent vectors]].

Specifically for the [[Klein-Gordon operator]] such ditributional solutions include the [[causal propagator]] and the [[Feynman propagator]].

=--



+-- {: .num_example #WaveFrontOfTensorProductDistribution}
###### Example
**(wave front set of [[tensor product distribution]])**

Let $u \in \mathcal{D}'(X)$ and $v \in \mathcal{D}'(Y)$ be two distributions. then the wave front set of their [[tensor product distribution]] $u \otimes v \in \mathcal{D}'(X \times Y)$ satisfies

$$
  WF(u \otimes v)
  \;\subset\;
  \left(
     WF(u) \times WF(v)
  \right)
    \cup
  \left(
    \left( supp(u) \times \{0\} \right)
    \times WF(v)
  \right)
    \cup
   \left(
     WF(u)
     \times
     \left(
       supp(v) \times \{0\}
     \right)
   \right)
  \,,
$$

where $supp(-)$ denotes the [[support of a distribution]].

=--

([H&#246;rmander 90, theorem 8.2.9](#Hoermander90))



## Properties


+-- {: .num_prop #EmptyWaveFrontSetCorrespondsToOrdinaryFunction}
###### Proposition
**(empty wave front set corresponds to ordinary functions)**

The wave front set of a [[compactly supported distribution]] is empty precisely if the distribution comes from an ordinary [[smooth function]] (hence a [[bump function]]). 

=--

e.g. ([H&#246;rmander 90, below (8.1.1)](#Hoermander90))


+-- {: .num_prop #DerivativeOfDistributionRetainsOrShrinksWaveFrontSet}
###### Proposition
**([[derivative of distributions]] retains or shrinks wave front set)**

Taking [[derivatives of distributions]] retains or shrinks the wave front set:

For $u \in \mathcal{D}'(\mathbb{R}^n)$ a distribution and $\alpha \in \mathbb{N}^n$ a multi-index with $D^\alpha$ denoting the corresponding [[partial derivative]], then 

$$
  WF(D^\alpha u) \subset WF(u)
  \,.
$$ 

=--

([H&#246;rmander 90, (8.1.10), p. 256](#Hoermander90))

## Related concepts

* [[ultraviolet divergence]]


## References

### General

The concept of wave front set is due to

* {#Hoermander70} [[Lars Hörmander]], _Linear differential operators_, Actes Congr. Int. Math. Nice 1970, 1, 121-133 ([pdf](http://www.mathunion.org/ICM/ICM1970.1/Main/icm1970.1.0121.0134.ocr.pdf))

A textbook account for distributions on open subsets of [[Euclidean space]] is in

* {#Hoermander90} [[Lars Hörmander]], section 8.1 of _The analysis of linear partial differential operators_, vol. I, Springer 1983, 1990

and for distributions more generally on smooth manifolds is in 

* {#Hoermander94} [[Lars Hörmander]], _The analysis of linear partial differential operators_, vol. III, Springer 1994

A history of the concept of wave front sets with extensive pointers to the 
literature is given in [H&#246;rmander 90, p. 322-324](#Hoermander90).

See also

* Wikipedia: [wavefront set] (http://en.wikipedia.org/wiki/Wavefront_set)

### In quantum field theory

The application of [[microlocal analysis]] via wave front sets to the discussion of [[n-point functions]] in [[quantum field theory]] and especially [[quantum field theory on curved spacetimes]] originates with the results of

* {#DuistermaatHoermander72} [[Johann Duistermaat]], [[Lars Hörmander]], sections 6.5, 6.6 of _Fourier integral operators II_, Acta Mathematica 128, 183-269, 1972 ([Euclid](https://projecteuclid.org/euclid.acta/1485889724))

which were first picked up in

* C. Moreno, _Spaces of positive and negative  frequency  solutions of  field equations in curved  space- times. I.  The Klein-Gordon  equation in stationary  space-times, II. The massive  vector field equations in static  space-times_, J. Math.  Phys. 18, 2153-61 (1977), J. Math.  Phys. 19, 92-99 (1978)

*  [[Jonathan Dimock]], _Scalar  quantum field  in  an external  gravitational  background_,  J. Math.  Phys. 20, 2549-2555 (1979)

and brought into context with the [[Hadamard distributions]] needed for the [[construction]] of [[Wick algebras]] in 

* {#Radzikowski96} [[Marek Radzikowski]], _Micro-local approach to the Hadamard condition in quantum field theory on curved space-time_, Commun. Math. Phys. 179 (1996), 529&#8211;553 ([Euclid](http://projecteuclid.org/euclid.cmp/1104287114))

A textbook account amplifying this usage (on [[Minkowski spacetime]]) in the mathematically rigorous construction of [[perturbative quantum field theory]] via [[causal perturbation theory]] is in 

* {#Scharf95} [[Günter Scharf]], _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

* {#Scharf01} [[Günter Scharf]], _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

For more see the references at _[[locally covariant perturbative quantum field theory]]_.

[[!redirects wavefront sets]]

[[!redirects wave front set]]
[[!redirects wave front sets]]

[[!redirects wave-front set]]
[[!redirects wave-front sets]]
