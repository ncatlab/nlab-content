
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
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


In [[perturbative quantum field theory]] [[AQFT on curved spacetimes|on curved spacetimes]], _Hadamard states_ are certain [[quantum states]] of [[free fields]] (whose [[2-point function]] is the corresponding _Hadamard distribution_ on [[spacetime]]) that play the role that the _[[vacuum state]]_ plays on [[Minkowski spacetime]].

Here a _[[vacuum state]]_ is supposed to be a [[quantum state]] that expresses the absence of any [[particle]] excitations of the fields.
On [[Minkowski spacetime]] the _vacuum state_ for a [[free field theory]] is the standard Hadamard state (def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime} below). On general [[globally hyperbolic spacetimes]] there are always Hadamard states ([Radzikowski 96](#Radzikowski96), see def. \ref{HadamardDistribution} below),  and they do play the role of the vacuum state in  the construction of [[AQFT on curved spacetimes]], see at _[[locally covariant perturbative AQFT]]_. Notably the choice of such a Hadamard state fixes the _[[Feynman propagator]]_, hence the [[time-ordered product]] of [[quantum observables]] and thus the [[perturbative quantum field theory|perturbative]] [[S-matrix]] away from coinciding interaction points (the [[extension of distributions|extension of these distributions]] to coinciding interaction points is the process of [[renormalization]]).

However, since on a general [[globally hyperbolic spacetime]] there is no globally well-defined concept of [[particles]], there is in general no concept of vacuum state. But under good conditions (such as existence of suitable [[timelike]] [[Killing vectors]]) one may identify Hadamard states which deserve to be thought of as vacuum states ([Brum-Fredenhagen 13](#BrumFredenhagen13)).

Hadamard states are mathematically characterized as follows:

Given a [[globally hyperbolic spacetime]], the [[causal propagator]] defines a [[symplectic form]] on the [[covariant phase space]] of the [[free field|free]] [[scalar field]]. However its [[wave front set]] is too large for the would-be induced [[Moyal star product]] to exist on but a very small subalgebra of smooth functionals, due to the failure of the relevant [[products of distributions]] to exist. However the Moyal star product makes sense more generally for [[almost Kähler structures]] with a symmetric contribution added to the skew-symmetric symplectic form. 

A _Hadamard distribution_ is such a modification of the causal propagator by a symmetric component such that the resulting [[wave front set]] is just one causal half of that of the [[causal propagator]]. This allows to define the corresponding [[Moyal star product]] on the larger algebra of [[microcausal functionals]] which is large enough to contain the [[adiabatic switching|adiabatically switched]] point [[interaction]] terms $g \phi(x)^n$ (as in [[phi^4 theory]] etc.). The resulting [[algebra of observables]] is the _[[Wick algebra]]_ of the free scalar field.

The Hadamard distribution may also be thought of as the [[2-point function]] of a [[quasi-free quantum state]]. These states are therefore called _Hadamard states_.

[[!include propagators - table]]


## Definition

### On Minkowski spacetime
 {#OnMinkowskiSpacetime}


+-- {: .num_defn #StandardHadamardDistributionOnMinkowskiSpacetime}
###### Definition
**(standard Hadamard distribution on [[Minkowski spacetime]])**

For $p \in \mathbb{N}$, the standard [[vacuum state|vacuum]] Hadamard distribution on [[Minkowski spacetime]] of [[dimension]] $(p+1)$ is (see the computation of [this prop.](scalar+field#IntegralKernelForPoissonBracketOfFreeScalarFieldOnMinkowskiSpacetime) at _[[scalar field]]_)

$$
  \label{2PointFunctionFreeScalarFieldOnMinkowski}
  \begin{aligned}
    \omega(x,y)
     & \coloneqq
    (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)} e^{- i E(\vec k) (x-y)^0 - \vec k \cdot (\vec x - \vec y)} d^{p} \vec k
    \\
    & =
    (2\pi)^{-p} \int \delta( k_\mu k^\mu + m^2 ) \Theta( k_0 ) e^{ - i k_\mu (x-y)^\mu } d^{p+1} k
    \,,
  \end{aligned}
$$

(where the first line follows from the second by the [[change of integration variables]] via $k_0 = \sqrt{h}$).

=--

+-- {: .num_prop #ContourIntegralForStandardHadamardPropagatorOnMinkowskiSpacetime}
###### Proposition
**([[contour integral]] representation of standard Hadamard propagator on [[Minkowski spacetime]])

The standard Hadamard distribution on Minkowski spacetime from 
def. \ref{StandardHadamardDistributionOnMinkowskiSpacetime} is 
equivalently given by the [[contour integral]]

$$
  \label{StandardHadamardPropagatorOnMinkowskiSpacetimeInTermsOfContourIntegral}
  \omega(x,y)
  \;=\;
    -i(2\pi)^{-(p+1)}
    \int
    \oint_{C_+(\vec k)}
     \frac{e^{-i k_\mu (x-y)^\mu}}{ k_\mu k^\mu + m^2 }
    d k_0
    d^{p} k
  \,,
$$

where the [[Jordan curve]] $C_+(\vec k) \subset \mathbb{C}$ runs counter-clockwise, enclosing the point $+ E(\vec k) \in \mathbb{R} \subset \mathbb{C}$, but not enclosing the point $- E(\vec k) \in \mathbb{R} \subset \mathbb{C}$. (Compare the analogous expression for the [[causal propagator]] in [this equation](causal+propagator#eq:CausalPropagatorOnMinkowskiSpacetimeInTermsOfContourIntegral).)


<img src="https://ncatlab.org/nlab/files/ContourForHadamardPropagator.png" height="200">

> graphics grabbed from [Kocic 16](#Kocic16)

=--

+-- {: .proof}
###### Proof

[[Cauchy's integral formula]] says that the given contour integral picks up the [[residue]] of the [[pole]] of the [[integrand]] at $+ E(\vec k) \in \mathbb{R} \subset \mathbb{C}$: 


$$
  \begin{aligned}
    -i(2\pi)^{-(p+1)}
    \int
    \oint_{C_+(\vec k)}
     \frac{e^{-i k_\mu (x-y)^\mu}}{ k_\mu k^\mu + m^2 }
    d k_0
    d^{p} k
    & =
    -i(2\pi)^{-(p+1)}
    \int
    \oint_{C_+(\vec k)}
      \frac{
        e^{-i k_0 x^0} e^{- i \vec k \cdot (\vec x - \vec y)}
      }{
        - k_0^2 + E(\vec k)^2 
      } 
    d k_0
    d^p \vec k 
    \\
    & =   
    -i(2\pi)^{-(p+1)}
    \int
    \oint_{C_+(\vec k)}
      \frac{
        e^{-i k_0 (x-y)^0} e^{- i \vec k \cdot (\vec x - \vec y)}
      }{
        ( E_\epsilon(\vec k) + k_0 )
        ( E_\epsilon(\vec k) - k_0 )
      } 
    d k_0
    d^p \vec k
    \\
    & = 
    (2\pi)^{-p}
     \int
       \frac{1}{2 E(\vec k)}
       e^{-i E(\vec k) (x-y)^2 e^{-i \vec k \cdot (\vec x - \vec y)}}
    d^p \vec k
    \\
    & = \omega(x,y)
    \,.
  \end{aligned}
$$

=--


### On general globally hyperbolic spacetimes


Recall the following general facts about the [[wave equation]]/[[Klein-Gordon equation]]

+-- {: .num_prop #PropertiesOfTheCausalPropagator}
###### Proposition
**(the causal propagator)**

Let $(X,g)$ be a [[time orientation|time-oriented]] [[globally hyperbolic spacetime]] and let $m \in \mathbb{R}_{\geq 0}$ (the "[[mass]]"). Then the [[Klein-Gordon equation]]

$$
  (\Box_g - m^2) \phi = 0
$$

(a [[partial differential equation]] on [[smooth functions]] $f \in C^\infty(X,\mathbb{R})$ ) has unique advanced and retarded [[Green functions]] $E^{R/A}$, namely [[continuous linear functionals]]

$$
  E^{A/R} 
   \;\colon\;
  C^\infty_c(X)
   \longrightarrow
  C^\infty(X)
$$

(from [[bump functions]] to general [[smooth functions]]) which are [[fundamental solutions]] in that 

$$
  (\Box_g - m^2) \circ E^{A/R} = \delta
  \phantom{AAAA}
  E^{A/R} \circ (\Box_g - m^2) = \delta
$$

and which have advanced/retarded [[support of a distribution]] when viewed (via the [[Schwartz kernel theorem]]) as [[distributions]] on the [[Cartesian product]] manifold $X \times X$

$$
  supp( E^{A/R}) \subset \{ (x_1, x_2) \in X \times X  \;\vert\; x_1 \in J^{\mp} (x_2) \}
 \,.
$$

In fact these two fundamental solutions are related by switching their arguments 

$$
  E^{A/R}(x_1, x_2) = E^{R/A}(x_2, x_1)
  \,.
$$

Finally their [[wave front set]] is 

$$
  WF(E^{A/R})
  \;=\;
  \left\{
   ((x_1, x_2), (k_1, -k_2))
   \;\vert\;
   x_1 \in J^{\mp}(x_2)
   \;\text{and}\;
   \left(
     (x_1, k_1) \sim (x_2, k_2)
   \right)
   \;\text{or}\;
   \left(
     (x_1 = x_2)
     \,\text{and}\,
     k_1 = -k_2
   \right)
  \right\}
  \,.
$$

Here the [[relation]] $(x_1, k_1) \sim (x_2, k_2)$ means that there exists a [[lightlike]] [[geodesic]] from $x_1$ to $x_2$ with cotangent vector $k_1$ at $x_1$ and $k_2$ at $x_2$.

It follows that the [[wave front set]] of their difference (the [[causal propagator]])

$$
  E \;\coloneqq\; E^A - E^R
$$

is 

$$
  WF(E)
  \;=\;
  \left\{
    ((x_1 x_2), (k_1, -k_2))
    \;\vert\;
    (x_1, k_1) \sim (x_2, k_2)
  \right\}
  \,.
$$


=--

+-- {: .num_defn #HadamardDistribution}
###### Definition
**(Hadamard distribution)

Let $(X,g)$ be a [[time orientation|time oriented]] [[globally hyperbolic spacetime]].

A _Hadamard 2-point function_ or _Hadamard distribution_ for the [[free field|free]] [[scalar field]] on $(X,g)$ is a [[distribution of two variables]] 

$$
  \omega \in \mathcal{D}'(X \times X)
$$

on the [[Cartesian product]] manifold such that


1. the anti-symmetric part of $\omega$ is the [[causal propagator]] $E$ (from prop. \ref{PropertiesOfTheCausalPropagator})

   $$
     \omega(x_1, x_2) - \omega(x_2, x_1)
     \;=\;
     i E(x_1, x_2)
   $$

1. (wave front set spectral condition ([Radzikowski 96, def. 6.1](#Radzikowski96)))

   the [[wave front set]] is one causal half that of the causal propagator:

   $$
     WF(\omega)
     \;=\;
     \left\{
       ((x_1, x_2), (k_1, -k_2))
       \;\vert\;
       (x_1, k_1) \simeq (x_2, k_2)
       \;\;\text{and}\;\;
       k_1 \in V_{x_1}^+
     \right\}
   $$



1. (Klein-Gordon bi-solution) $(\Box_g - m^2) \omega(-,x) = 0$ and $(\Box_g - m^2)\omega(x,-) = 0$, for all $x \in X$;


1. (positive semi-definiteness) For any complex-valued [[bump function]] $b$ we have that 

   $$
     \int_{X \times X} b^\ast(x) \omega(x,y) b(y) \, dvol(x) dvol(y)
     \;\coloneqq\;
     \langle \omega, b^\ast \otimes b \rangle 
     \;\geq\; 0 
   $$

=--

+-- {: .num_remark}
###### Remark

Before ([Radzikowski 96](#Radzikowski96)), Hadamard distributions were characterized by their singularity structure (see ... below). In ([Kay-Wald 91](#KayWald91)) the spectrum condition in def. \ref{HadamardDistribution} was formulated, and ([Radzikowski 96](#Radzikowski96)) proved that this is equivalent to the original definition via singularity structure.

=--


## Properties

### Existence

+-- {: .num_prop #ExistenceOfHadamardDistributions}
###### Proposition
**(existence of Hadamard distributions)

Let $(X,g)$ be a [[globally hyperbolic spacetime]]. Then a [[Hadamard distribution]] $\omega$ according to def. \ref{HadamardDistribution} does exist.

It is given, up to addition by a smooth function, as the difference between the [[advanced propagator]] and the [[Feynman propagator]]
 
=--

([Radzikowski 96, above theorem 6.3 with theorem 5.1](#Radzikowski96))

In fact there exist infinitely many Hadamard distributions on any globally hyperbolic spacetime ([Junker-Schrohe 02](#JunkerSchrohe02), [Fulling-Narcowich-Wald 81](#FullingNarcowichWald81)).

## Examples

### In Minkowski spacetime

In [[Minkowski spacetime]] $\mathbb{R}^{d-1,1}$ the Hadamard distribution is given by

$$
  \omega(x,y)
  \;=\;
  \tfrac{1}{(2\pi)^{d-1}}
  \int_{\mathbb{R}^d}
  e^{i p (x-y)}
  \theta(p^0) \delta(p^2 + m^2 ) d^d p
$$

(e.g. [KM 14, equation (38) and section 3.4](#KM14))

## Related concepts

* [[causal propagator]]

* [[Feynman propagator]]


## References

Textbook discussion of the Hadamard distribution for [[free fields]] in [[Minkowski spacetime]] is in

* {#Scharf95} [[Günter Scharf]],  section 2.3 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Springer 1995

* [[Günter Scharf]], section 1 of  _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

(there the Hadamard distribution is denoted "$-i D^+_m(x-y)$").

An concise overview of the standard Hadamard propagator in Minkowski spacetime and its relation to the other pertinent propagors is given in

* {#Kocic16} [[Mikica Kocic]], _Invariant Commutation and Propagation Functions Invariant Commutation and Propagation Functions_, 2016 ([[KGPropagatorsOnMinkowskiTable.pdf:file]])


On general [[globally hyperbolic spacetimes]] Hadamard spectrum condition was first rigorously defined in 

* {#KayWald91} B. S. Kay, [[Robert Wald]], _Theorems on the uniqueness and thermal properties of stationary, nonsingular, quasifree states on spacetimes  with a bifurcate  Killing  horizon_, Phys.  Rep. 207(2), 49-136 (1991)

and shown to be equivalent to the definition in terms of singular structure in 

* {#Radzikowski96} [[Marek Radzikowski]], _Micro-local approach to the Hadamard condition in quantum field theory on curved space-time_, Commun. Math. Phys. 179 (1996), 529&#8211;553 ([Euclid](http://projecteuclid.org/euclid.cmp/1104287114))


Hadamard states with [[smooth function|smooth]] dependence on the [[mass]] square (needed for [[dimensional regularization]] methods in [[causal perturbation theory]]/[[perturbative AQFT]]) are constructed in

* {#Keller10} [[Kai Keller]], chapter III of _Dimensional Regularization in Position Space and a Forest Formula for Regularized Epstein-Glaser Renormalization_, PhD thesis ([arXxiv:1006.2148](https://arxiv.org/abs/1006.2148))

Discussion of [[vacuum state]]-like Hadamard states is in

* {#BrumFredenhagen13} Marcos Brum, [[Klaus Fredenhagen]], _"Vacuum-like" Hadamard states for quantum fields on curved spacetimes_ ([arXiv:1307.0482](https://arxiv.org/abs/1307.0482))


Review and further developments are in

* {#Hollands07} [[Stefan Hollands]], appendix D of _Renormalized Quantum Yang-Mills Fields in Curved Spacetime_, Rev. Math. Phys. 20:1033-1172, 2008 ([arXiv:0705.3340](https://arxiv.org/abs/0705.3340))

*  {#KM14} [[Igor Khavkine]], [[Valter Moretti]], _Algebraic QFT in Curved Spacetime and quasifree Hadamard states: an introduction_, Chapter 5 in [[Romeo Brunetti]] et al. (eds.) _Advances in Algebraic Quantum Field Theory_, Springer, 2015 ([arXiv:1412.5945](https://arxiv.org/abs/1412.5945))

Discussion for [[electromagnetism]] is in

* [[Claudio Dappiaggi]], D. Siemssen, _Hadamard states for the vector potential on asymptotically flat spacetimes_, Rev. Math. Phys. 25, 1 (2013)


See also

* {#JunkerSchrohe02} W. Junker and E. Schrohe: _Adiabatic vacuum states on general spacetime manifolds: Definition, construction, and physical properties_, Annales Poincare Phys. Theor. 3, 1113
(2002)

* S. A. Fulling, M. Sweeny, [[Robert Wald]], _Singularity Structure Of The Two Point Function In Quantum Field Theory In Curved Space-Time_, Commun. Math.
Phys. 63, 257 (1978).

* {#FullingNarcowichWald81} S. A. Fulling, F. J. Narcowich, [[Robert Wald]], _Singularity Structure Of The Two Point Function In Quantum Field Theory In Curved Space-Time_, Annals Phys. 136, 243 (1981), 


* Marcos Brum, [[Klaus Fredenhagen]], _"Vacuum-like" Hadamard states for quantum fields on curved spacetimes_, Classical and Quantum Gravity, Volume 31, Number 2 ([arXiv:1307.0482](https://arxiv.org/abs/1307.0482))

[[!redirects Hadamard distributions]]

[[!redirects quasi-free Hadamard state]]
[[!redirects quasi-free Hadamard states]]

[[!redirects Hadamard state]]
[[!redirects Hadamard states]]

[[!redirects Hadamard propagator]]
[[!redirects Hadamard propagators]]


[[!redirects Hadamard 2-point function]]
[[!redirects Hadamard 2-point functions]]



