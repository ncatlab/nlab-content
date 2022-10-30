

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Algbraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
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

What is called the _Feynman propagator_ over a [[globally hyperbolic spacetime]] is one of the [[Green functions]] for the [[Klein-Gordon operator]] $\Box + m^2$ (hence a [[fundamental solution]] to the [[wave equation]] when the [[mass]] $m$ vanishes). 

As discussed in detail at _[S-matrix -- Feynman diagrams and renormalization](S-matrix#ExistenceAndRenormalization)_, 
the Feynman propagator encodes [[time-ordered products]] of [[quantum observables]] in [[free field]] [[perturbative quantum field theory]] (in the same way as the [[Hadamard propagator]] encodes [[normal ordered products]] of quantum fields). This implies that the [[scattering amplitude]] associated with a [[Feynman diagram]] in the [[Feynman perturbation series]] expansion of the [[S-matrix]] is, away from the locus of coinciding interaction points, a [[product of distributions|product]] of Feynman propagators, one for each [[edge]] in the [[Feynman diagram]] (the [[extension of distributions]] of this [[product of distributions]] to coinciding points is _[[renormalization]]_). 

This is why Feynman propagators are ubiquituous in [[perturbative quantum field theory]]: they are the building blocks of perturbative [[scattering amplitudes]].

## Definition

By the discussion at _[S-matrix -- Feynman diagrams and renormalization](S-matrix#ExistenceAndRenormalization)_, the Feynman propagator $\omega_F$ is properly defined to be the [[linear combination]] of the chosen [[Hadamard propagator]] (encoding the [[vacuum state]]) and the [[advanced causal propagator]]:

+-- {: .num_defn #FeynmanPropatorAsSumOfHadamardPropagatorWithAdvancedPropagator}
###### Definition
**(Feynman propagator on [[globally hyperbolic spacetimes]])

Given a [[time orientation|time-oriented]] [[globally hyperbolic spacetime]] $\Sigma$ there exists a unique [[advanced causal propagator]] $\Delta_A \in \mathcal{D}'(\Sigma \times \Sigma)$ and a [[Hadamard propagator]] $\omega \in \mathcal{D}'(\Sigma \times \Sigma)$, unique up to addition of a regular distributio (a smooth function). Given a choice of $\omega$ (the [[vacuum state]]) then the corresponding _Feynman propagator_ is the sum

$$
  \omega_F \coloneqq \omega + i \Delta_A
  \,.
$$

=--

(for [[Minkowski spacetime]] this is e.g. [Scharf 95 (2.3.41)](#Scharf95), for general [[globally hyperbolic spacetimes]] this is [Radzikowski 96, p. 5](#Radzikowski96))

On [[Minkowski spacetime]] this may be expressed as a sum of [[products of distributions]] of a [[Heaviside distribution]] in the time coordinate with the Hadamard distribution and its opposite, and this is often taken as the definition of the Feynman propagator. But the above formula applies to general [[globally hyperbolic spacetimes]].
 
[[!include propagators - table]]

### On Minkowski spacetime

+-- {: .num_prop #ContourIntegralRepresentationOfStandardFeynmanPropagatorOnMinkowskiSpacetime}
###### Proposition
**([[contour integral]] presentation of standard Feynman propagator on [[Minkowski spacetime]])**

For $p \in \mathbb{N}$, on [[Minkowski spacetime]] of [[dimension]] $p+1$ the Feynman propagator $\omega_F$ according to prop. \ref{FeynmanPropatorAsSumOfHadamardPropagatorWithAdvancedPropagator}, with respect to the standard [[vacuum state|vacuum]] [[Hadamard state]] ([this def.](Hadamard+distribution#StandardHadamardDistributionOnMinkowskiSpacetime)) is

$$
  \label{ContourIntegralForStandardFeynmanPropagatorOnMinkowskiSpacetime}
  \begin{aligned}
    \omega_F(x,y)
    & \coloneqq
      -(2\pi)^{-(p+1)}
      \int
       \frac{e^{-i k_\mu (x-y)^\mu}}{ k_\mu k^\mu + m^2 + i0}
    d^{p+1} k
    \\ & \coloneqq
      -(2\pi)^{-(p+1)}
      \underset{\epsilon \to 0^+}{\lim}
      \int
      \int
       \frac{
         e^{-i k_\mu (x-y)^\mu}
       }{
         ( E(\vec k) + (k_0 - i \epsilon) )
         ( E(\vec k) - (k_0 + i \epsilon) ) 
       }
      d k_0
      d^{p} k
  \end{aligned}
 \,.
$$

(compare to [this computation](advanced+and+retarded+causal+propagators#eq:ContourIntegrationForCausalPropagator) at _[[advanced and retarded propagators]]_ to see the point of the notation "$+ i 0$" in the first line, and its definition by the second line).

<img src="https://ncatlab.org/nlab/files/ContourForFeynmanPropagator.png" height="300">

> graphics grabbed from ([Kocic 16](#Kocic16))

=--

(e.g. [Scharf 95 (2.3.44)](#Scharf95))


+-- {: .proof}
###### Proof

We may compute the [[line integral]] in the second line of (eq:ContourIntegralForStandardFeynmanPropagatorOnMinkowskiSpacetime) by completing to a [[contour integral]] in the [[complex plane]]. For $(x^0 - y^0) \gt 0$ we have that $e^{-i k_0 (x^0 - y^0)}$ decays as the [[imaginary part]] of $k_0$ goes to $-\infty$, and hence in this case we need to close the contour in the [[lower half plane]]. Conversely, for $(x^0 - y^0) \lt 0$ we need to close the conour in the [[upper half plane]]. By the [[Cauchy integral formula]], in the first case we pick up the [[residue]] at the [[pole]] at $E(\vec k) - i \epsilon$ with a minus sign (because the contour in this case runs clockwise), while in the second case we pick up the residue at $-E(\vec k) + i \epsilon$ (without an extra minus sign, because in this case it runs counter-clockwise). Hence we get

$$
  \label{FeynmanPropagatorAsContourIntegral}
  \begin{aligned}
    \omega_F(x,y)
    & = 
      \left\{
        \array{
      (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)} e^{- i E(\vec k) (x^0 - y^0) - \vec k \cdot (\vec x - \vec y)} d^{p} \vec k
          & \vert & (x^0 - y^0) \gt 0
          \\
      (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)} e^{+ i E(\vec k) (x^0 - y^0) - \vec k \cdot (\vec x - \vec y)} d^{p} \vec k
          & \vert & (x^0 - y^0) \lt  0
        }
      \right. 
    \\
    & = 
    \left\{
      \array{
        \omega(x,y) & \vert & (x^0 - y^0) \gt 0
        \\
        \omega(y,x) & \vert & (x^0 - y^0) \lt 0
      }
    \right.
  \end{aligned} 
$$ 

(as befits the expectation value of the [[time-ordered product]] $T(\phi(x) \phi(y))$).

On the other hand, by [this equation](advanced+and+retarded+causal+propagators#eq:AdvancedPropagatorAsSumOfResidues) for from the discussion at _[[advanced propagator]]_ and [this equation](Hadamard+distribution#eq:2PointFunctionFreeScalarFieldOnMinkowski) from the discussion at _[[Hadamard propagator]]_ we have

$$
  \begin{aligned}
    i \Delta_A(x,y)
    & = 
    \left\{
      \array{
        -
        (2\pi)^{-p} 
        \int
        \left(
          \frac{
            e^{-i E(\vec k) (x^0 - y^0) e^{-i \vec k \cdot (\vec x - \vec y)}}
          }
          {
            2 E(\vec k)
          }
          -
          \frac{
            e^{ + i E(\vec k)(x^0 - y^0)} e^{-i \vec k \cdot (\vec x - \vec y)}
          }{
            2 E(\vec k)
          }
        \right)
        & \vert & (x^0 - y^0) \lt 0
        \\
        0 & \vert & (x^0 - y^0) \gt 0
      }
    \right.
    \\
    \omega(x,y)
    & = 
    (2\pi)^{-p} \int \tfrac{1}{2 E(\vec k)} e^{- i E(\vec k) (x-y)^0 - \vec k \cdot (\vec x - \vec y)} d^{p} \vec k
  \end{aligned}
  \,.
$$

Adding up the two lines and comparing with (eq:FeynmanPropagatorAsContourIntegral) shows that with $\omega_F$ as defined by (eq:ContourIntegralForStandardFeynmanPropagatorOnMinkowskiSpacetime) indeed satisfies the defining equation 

$$
  \omega_F = \omega + i \Delta_A
$$

from def. \ref{FeynmanPropatorAsSumOfHadamardPropagatorWithAdvancedPropagator}.

 

=--


### As a zeta function

> needs harmonization

From another perspective, the loop contributions of [[Feynman diagrams]] are typically would-be [[traces]] over inverse powers $H^{-n}$ of the relativistic particle [[Hamiltonian]].

For instance for the free [[scalar particle]] of [[mass]] $m$ in 4d [[Minkowski spacetime]] the 1-loop [[vacuum amplitude]] is the regularized trace over the Feynman propagator

$$
  \propto \int d^4 \mathbf{p} \; \frac{1}{\mathbf{p}^2 - m^2}
$$

where the integral would naively be over all of $\mathbb{R}^4$, which is of course not well defined. The integrand here is typically called the _Feynman  propagator_ or _propagator_ for short (e.g. [Grozin 05, section 2.1](#Grozin05) [Kleinert 11, 8.1](#Kleinert11)). See at _[Feynman diagram -- For finitely many degrees of freedoms](Feynman+diagram#ForFinitelyManyDegreesOfFreedom)_ for how this comes about.

Several methods are considered for _[[regularization (physics)|regularizing]]_, hence making sense of it as a finite expression. One of these is [[zeta function regularization]] (also "analytic regularization/renormalization" [Speer 71](#Speer71)). Here one notices that the [[zeta function of an elliptic differential operator|zeta function]] of the [[wave operator]]/[[Laplace operator]] $H = \mathbf{p}^2 + m^2$ is well-defined for $\Re(s) \gt 1$ by the naive [[trace]]

$$
  \hat \zeta_H(s)\coloneqq Tr_{reg}( H^{-s} )
$$

and defined from there by [[analytic continuation]] on allmost all of the [[complex plane]]. The [[special values of L-functions|special value]] at $s = 1$ (or its [[principal value]]) is the regularized Feynman propagator. See ([BCEMZ 03, section 2.4.2](#BCEMZ03)).  For the example of the above basic Feynman propagator see e.g. [Grozin 05, section 2.1](#Grozin05)

Representing the (completed) [[zeta function]] here are the [[Mellin transform]] of some [[theta function]] -- which in the present case is the [[partition function]] $t\mapsto Tr_{reg} \exp(-t H)$ of the [[worldline formalism]] of the given theory, is what in the physics literature is known as the [[Schwinger parameter]]-formulation

$$
  Tr_{reg} H^{-s} = \int_0^\infty t^{s-1} Tr\, \exp(-t H)\,d t
  \,.
$$


[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]


## Related concepts

* [[causal propagator]]

* [[Hadamard distribution]]

## References

Textbook accounts for quantum fields on [[Minkowski spacetime]] includes

* {#Scharf95} [[Günter Scharf]],  section 2.3 of _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Springer 1995

* {#Scharf01} [[Günter Scharf]], section 1 of  _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001


An concise overview of the [[Green functions]] of the [[Klein-Gordon operator]], hence of the Feynman propagator, [[advanced propagator]], [[retarded propagator]], [[causal propagator]] etc. is given in

* {#Kocic16} [[Mikica Kocic]], _Invariant Commutation and Propagation Functions Invariant Commutation and Propagation Functions_, 2016 ([[KGPropagatorsOnMinkowskiTable.pdf:file]])


Discussion on general [[globally hyperbolic spacetimes]] is in

* {#Radzikowski96} [[Marek Radzikowski]], _Micro-local approach to the Hadamard condition in quantum field theory on curved space-time_, Commun. Math. Phys. 179 (1996), 529&#8211;553 ([Euclid](http://projecteuclid.org/euclid.cmp/1104287114))

where the issue with the underlying [[Hadamard propagators]] was settled, and reviewed for instance in

* {#BCEMZ03} A. Bytsenko, G. Cognola, [[Emilio Elizalde]], [[Valter Moretti]], S. Zerbini, section 2 of _Analytic Aspects of Quantum Fields_, World Scientific Publishing, 2003, ISBN 981-238-364-6



Lecture notes (mostly for the case over Minkowski spacetime) include

* {#Grozin05} Andrey Grozin, _Lectures on QED and QCD_ ([arXiv:hep-ph/0508242](http://arxiv.org/abs/hep-ph/0508242))

* {#GFP} _Green functions and propagators_ ([[GreenFunctionsAndPropagators.pdf:file]])


* _Green functions for the Klein-Gordon operator_ ([pdf](http://sgovindarajan.wdfiles.com/local--files/serc2009/greenfunction.pdf))

* {#Kleinert11} [[Hagen Kleinert]], V. Schulte-Frohlinde, _Critical properties of $\phi^4$-Theories_ 2001 ([pdf](http://users.physik.fu-berlin.de/~kleinert/b8/psfiles/08.pdf))

An overview of the [[Green functions]] of the [[Klein-Gordon operator]], hence of the [[Feynman propagator]], [[advanced propagator]], [[retarded propagator]], [[causal propagator]] etc. is given in

* {#Kocic16} [[Mikica Kocic]], _Invariant Commutation and Propagation Functions Invariant Commutation and Propagation Functions_, 2016 ([[KGPropagatorsOnMinkowskiTable.pdf:file]])


The zeta function regularization method originates around

* {#Speer71} [[Eugene Speer]], _On the structure of Analytic Renormalization_, Comm. math. Phys. 23, 23-36 (1971) ([Euclid](http://projecteuclid.org/euclid.cmp/1103857549))

and a comprehensive discussion is in ([BCEMZ 03, section 2](#BCEMZ03)).

Discussion of zeta functions of Dirac operators in 2d includes

* Michael McGuigan, _Riemann Hypothesis and Short Distance Fermionic Green's Functions_ ([arXiv:math-ph/0504035](http://arxiv.org/abs/math-ph/0504035))

Lecture notes concerning 1-loop vacuum amplitudes for the [[string]] include

* _The IIA/B superstring one-loop vacuum amplitude_ ([pdf](http://www.thphys.uni-heidelberg.de/~palti/Stringcourse/problemset11.pdf))

[[!redirects Feynman propagators]]

