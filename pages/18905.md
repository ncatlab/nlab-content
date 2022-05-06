

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### General

In [[field theory]] one speaks of _Euclidean field theory_ if the underlying [[spaces]] on which the [[field (physics)|fields]] are defined are [[Riemannian manifolds]], as opposed to [[Lorentzian  manifold|Lorentzian]] [[spacetimes]] used in [[relativistic field theory]], hence locally are _[[Euclidean spaces]]_ instead of [[Minkowski spacetimes]], whence the name "Euclidean field theory." 

Concretely this means that in Euclidean field theoy the [[local field theory|locality]] condition on the [[net of observables|net of]] [[quantum observables]] requires observables $A, B$to [[commutator|commute]] as soon as their [[supports]] are [[disjoint subset|disjoint]] at all

$$
  supp(A) \cap supp(B) = \emptyset
  \;\;\Rightarrow\;\;
  [A,B] = 0
  \,.
$$ 

This is in contrast to the analogous condition in [[relativistic field theory]] whose _[[causal locality]]_ requires this implication only if the two [[supports]] are in addition [[spacelike]]-separated.

This Euclidean locality property applies in particular in [[statistical mechanics]], where the "[[field (physics)|fields]]" of the field theory are not thought of as encoding the [[spacetime]]-behaviour of [[fundamental particles]] as governed by [[quantum physics]], but instead the spatial [[expectation values]] (at any given time) of equilibrium [[thermodynamics|thermodynamic]]-processes governed by [[classical physics]].
An archetypical example of a Eculidean field theory in this thermodynamic sense is the [[Ising model]]. 

Despite this superficially stark contrast between Euclidean and relativistic field theory, the two turn out to be tightly related to each other in a subtle way that involves and generalizes the concept of [[analytic continuation]] from [[complex analysis]], here this is called _[[Wick rotation]]_.






### Thermal quantum field theory via periodic Euclidean time
 {#ThermalQuantumFieldTheoryViaPeriodicEuclideanTime}

The equal-time [[n-point functions]] in [[relativistic field theory]] on [[Minkowski spacetime]] $\mathbb{R}^{d,1}$ in a [[vacuum state]] reflecting equilibrium at [[finite number|finite]] [[temperature]] $T$ may be argued ([Bloch 58](#Bloch58)) to be computed equivalently by Euclidean field theory on the [[Cartesian product]] $\mathbb{R}^d \times S^1$ of [[Euclidean space]] $\mathbb{R}^d$ with a [[circle]] $S^1$ of [[length|circumference]] $\beta \coloneqq 1/T$:

$$
  \underset{
    {\text{on Minkowski spacetime}\, \mathbb{R}^{d,1}}
    \atop
    {\text{at finite temperature}\, T}
  }{
  \underbrace{
    \left\langle  :\mathbf{\Phi}(x_1,t) \mathbf{\Phi}(x_2,t) \cdots \mathbf{\Phi}(x_n,t) : \right\rangle_{\mathbb{R}^{d,1}, T}
  }}
  \;=\;
  \underset{
    {\text{on Euclidean space}\, \mathbb{R}^{d} \times S^1}
    \atop
    {\text{with circle of circumference}\, \beta \coloneqq 1/T}   
  }{
  \underbrace{
  \left\langle  :\mathbf{\Phi}(x_1) \mathbf{\Phi}(x_2) \cdots \mathbf{\Phi}(x_n) : \right\rangle_{\mathbb{R}^{d} \times S^1_{\beta}}
  }}
$$

(see e.g. [Moore 03, section 1.1](#Moore03) for the quick informal [[path integral]]-idea and see [Fulling-Ruijsenaars 87, section 2, (2.50)](#FullingRuijsenaars87) for a careful discussion).

This perspective is known as _[[thermal quantum field theory]]_ or similar, the use of a "periodic Euclidean time coordinate" is also known as _[[Matsubara formalism]]_ (e.g. [Landsman-vanWert 87, section 2.3.1](#LandsmanVanWert87)) and specifically the condition that the periodicity has to be $\beta \coloneqq 1/T$ is known as the _[[KMS conditions]]_ (For _Kubo-Martin-Schwinger_, due to [Kubo 57](#Kubo57), [Martin-Schwinger 59](#MartinSchwinger59) with its final form due to [Haag-Hugenholtz-Winnink 67](#HaagHugenholtzWinnink67), see [Fulling-Ruijsenaars 87, section 3.1](#FullingRuijsenaars87)).

(e.g. [Thoma 00, section 2.2](#Thoma00), [Peeters-Zamaklar 09, section 1.3](#PeetersZamaklar09))

<center>
<img src="https://ncatlab.org/nlab/files/EuclideanTime.jpg" width="580">
</center>

> graphics grabbed form [Frolov-Zelnikov 11](#FrolovZelnikov11)

## Examples

* [[Ising model]]

## Related concepts

* [[2d CFT]]

* [[relativistic field theory]]

* [[lattice gauge theory]]


## References

### General

* {#PeetersZamaklar09} [[Kasper Peeters]], [[Marija Zamaklar]], _Euclidean Field Theory_, Lecture notes 2009-2011 ([web](http://maths.dur.ac.uk/users/kasper.peeters/eft.html), [pdf](http://maths.dur.ac.uk/users/kasper.peeters/pdf/eft.pdf))

### Thermal quantum field theory:

A good introduction is in [Fulling-Ruijsenaars 87, section 2](#FullingRuijsenaars87).

The idea goes back to 

* {#Bloch58} Claude Bloch, _Sur la détermination de l'état fondamental d'un système de particules_,  Nucl. Phys. 7 (1958) 451

The KMS condition is due to

* {#Kubo57} R. Kubo _Statistical-Mechanical Theory of Irreversible Processes  I. General Theory and Simple Applications to Magnetic and Conduction Problems_, Journal of the Physical Society of Japan 12, 570-586 1957

* {#MartinSchwinger59} Paul C. Martin, [[Julian Schwinger]], _Theory of Many-Particle Systems.  I_, Physical Review 115, 1342-1373 (1959)

* {#HaagHugenholtzWinnink67} [[Rudolf Haag]], N. M. Hugenholtz, M. Winnink, _On the equilibrium states in quantum statistical mechanics_, Comm. Math. Phys. Volume 5, Number 3 (1967), 215-236 ([euclid:1103840050](https://projecteuclid.org/euclid.cmp/1103840050))

Review includes 

* [Fulling-Ruijsenaars 87, sections 2 and 3](#FullingRuijsenaars87)

* {#LandsmanVanWert87} [[Klaas Landsman]], Ch.G.van Weert, _Real- and imaginary-time field theory at finite temperature and density_, Physics Reports Volume 145, Issues 3–4, January 1987, Pages 141-249 (<a href="https://doi.org/10.1016/0370-1573(87)90121-9">doi:10.1016/0370-1573(87)90121-9</a>)

* [[Jean Zinn-Justin]], _Quantum Field Theory at Finite Temperature: An Introduction_ ([arXiv:hep-ph/0005272](https://arxiv.org/abs/hep-ph/0005272))

* {#Thoma00} Markus H. Thoma, _New Developments and Applications of Thermal Field Theory_ ([arXiv:hep-ph/0010164](https://arxiv.org/abs/hep-ph/0010164))

* Yuhao Yang, _An Introduction to Thermal Field Theory_, 2011 ([pdf](https://www.imperial.ac.uk/media/imperial-college/research-centres-and-groups/theoretical-physics/msc/dissertations/2011/Yuhao-Yang-Dissertation.pdf))

* Yi-Cheng Huang, _Field Theory in the Imaginary-time Formulation_ ([arXiv:1311.1990v4](https://arxiv.org/abs/1311.1990v4))

* [[Roberto Longo]], _Kubo-Martin-Schwinger, Non-Equilibrium Thermal states, and Conformal Field Theory_, 2016 ([pdf](https://www.mat.uniroma2.it/~longo/Slides_files/Harvard16.pdf))

Further discussion:

* Christian D. Jäkel, _The Reeh–Schlieder property for thermal field theories_, Journal of Mathematical Physics 41, 1745 2000 ([doi:10.1063/1.533208](https://doi.org/10.1063/1.533208))

* {#JaehelRobl11} Christian D. Jäkel, Florian Robl, _The relativistic KMS condition for the thermal $n$-point functions of the $P(\phi)_2$ model_ ([arXiv:1103.3609](https://arxiv.org/abs/1103.3609))



With an eye towards [[lattice gauge theory]]:

* {#Moore03} Guy Moore, _Informal lectures on lattice gauge theory_, 2003 ([pdf](https://theorie.ikp.physik.tu-darmstadt.de/qcd/moore/latt_lectures.pdf))

With an eye towards [[black hole thermodynamics]]:

* {#FullingRuijsenaars87} S.A. Fulling, S.N.M. Ruijsenaars, _Temperature, periodicity and horizons_, Physics Reports Volume 152, Issue 3, August 1987, Pages 135-176 ([pdf](https://www1.maths.leeds.ac.uk/~siru/papers/p26.pdf), <a href="https://doi.org/10.1016/0370-1573(87)90136-0">doi:10.1016/0370-1573(87)90136-0</a>)

* {#FrolovZelnikov11} [[Valeri Frolov]], Andrei Zelnikov, section F4.4 of _Introduction to black hole physics_, Oxford 2011

See also

* Wikipedia, _[Thermal quantum field theory](https://en.wikipedia.org/wiki/Thermal_quantum_field_theory)_

* Wikipedia, _[Matsubara frequency](https://en.wikipedia.org/wiki/Matsubara_frequency)_

* Wolfram Math World, _[KMS condition](http://mathworld.wolfram.com/KMSCondition.html)_

[[!redirects Euclidean field theories]]

[[!redirects thermal quantum field theory]]
[[!redirects thermal quantum field theories]]

[[!redirects thermal field theory]]
[[!redirects thermal field theories]]


[[!redirects Matsubara formalism]]
[[!redirects Matsubara formalisms]]

[[!redirects Matsubara frequency]]
[[!redirects Matsubara frequencies]]



[[!redirects KMS condition]]
[[!redirects KMS conditions]]
