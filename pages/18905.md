
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### General

In [[field theory]] one speaks of _Euclidean field theory_ if the underlying [[spaces]] on which the [[field (physics)|fields]] are defined are [[Riemannian manifolds]], as opposed to [[Lorentzian  manifold|Lorentzian]] [[spacetimes]] used in [[relativistic field theory]], hence locally are _[[Euclidean spaces]]_ instead of [[Minkowski spacetimes]], whence the name "Euclidean field theory." 

Concretely this means that in Euclidean field theory the [[local field theory|locality]] condition on the [[net of observables|net of]] [[quantum observables]] requires observables $A, B$ to [[commutator|commute]] as soon as their [[spacetime supports]] are [[disjoint subset|disjoint]] at all

$$
  supp(A) \cap supp(B) = \emptyset
  \;\;\;\;\Rightarrow\;\;\;\;
  [A,B] = 0
  \,.
$$ 

This is in contrast to the analogous condition in [[relativistic field theory]] whose _[[causal locality]]_ requires this implication only if the two [[supports]] are in addition [[spacelike]]-separated.

Equivalently this means that the [[n-point functions]] of Euclidean field theories are [[distributions of several variables]] with [[singularities]] on the [[fat diagonal]] (instead of on all of the relative [[light cones]], as for [[relativistic field theory]]). This means that Euclidean $n$-point functions [[restriction of distributions|restrict]] to [[non-singular distributions]] on the [[configuration spaces of points|configuration space of n points]], allowing to express [[correlators as differential forms on configuration spaces of points]]. Systematic discussion of [[perturbative quantum field theory|perturbative]] [[renormalization|renormalized]] Euclidean field theory from this perspective is due to [Bergbauer-Brunetti-Kreimer 09](#BergbauerBrunettiKreimer09), [Berghoff 14a](#Berghoff14a), [Berghoff 14b](#Berghoff14b).

This Euclidean locality property applies in particular in [[statistical mechanics]], where the "[[field (physics)|fields]]" of the field theory are not thought of as encoding the [[spacetime]]-behaviour of [[fundamental particles]] as governed by [[quantum physics]], but instead the spatial [[expectation values]] (at any given time) of [[equilibrium]] [[thermodynamics|thermodynamic]]-processes governed by [[classical physics]].

An archetypical example of a Euclidean field theory in this thermodynamic sense is the [[Ising model]]. Generally, most [[2d conformal field theories]] considered are Euclidean field theories and (should) have the interpretation of describing [[thermodynamics|thermodynamical]] systems "at criticality".

However, other Euclidean [[2d CFTs]] are not necessarily regarded as thermodynamical systems, notably the [[worldsheet]]-field theories defining a [[string perturbation series]] in [[perturbative string theory]]. 

Another broad class of examples of Euclidean field theories are [[topological quantum field theories]] after their [[diffeomorphism]]-[[symmetry]] is partially [[gauge fixing|gauge fixed]] by a choice of [[Riemannian metric]]. The archetypical example here is [[perturbative quantum field theory|perturbative]] [[Chern-Simons theory]], see [there](Chern-Simons+theory#FeynmanPerturbationSeries) for more.


### Wick rotation to Relativistic Field theory

Despite this superficially stark contrast between Euclidean and relativistic field theory, the two turn out to be tightly related to each other, at least under some conditions, in a subtle way that involves and generalizes the concept of [[analytic continuation]] from [[complex analysis]], here this is called _[[Wick rotation]]_.

Roughly this says that [[propagators]] and hence [[n-point functions]] of [[relativistic field theory]] on [[Minkowski spacetime]] $\mathbb{R}^{d,1}$ (may) have [[analytic continuation]] to [[complex number|complex values]] of the [[time]]-[[coordinates]], such that replacing [[real number|real]] time with [[imaginary number|imaginary]] time turns these [[n-point functions]] into those of a [[Euclidean field theory]] on $\mathbb{R}^{d+1}$, and vice versa. 

Precise formulation of the conditions that go into this [[Wick rotation]] between [[relativistic field theory]] and Euclidean field theory is the content of the [[Osterwalder-Schrader theorem]].

### Temporal compactification to Thermal relativistic field theory
  {#TemporalCompactificationToThermalRelativisticFieldTheory}

In fact this relation goes deeper still: Under suitable conditions the Euclidean field theory not on $\mathbb{R}^{d+1}$ but on $\mathbb{R}^d \times S^1_\beta$, with the [[circle]]-[[product space|factor]] $S^1_{\beta}$ of [[length]] $\beta$, corresponds to relativistic field theory on [[Minkowski spacetime]] $\mathbb{R}^{d,1}$ in a [[vacuum state]] that represents [[thermal equilibrium]] at [[inverse temperature]] $\beta = 1/T$. (The previous case of Euclidean field theory on $\mathbb{R}^{d+1}$ may be thought of as the special case $\beta \to \infty$, hence $T \to 0$.)  

This curious relation of [[Wick rotation]] with "compact peridodic Euclidean time" makes, when it applies, Euclidean field theory be a unification of [[relativistic field theory]] with [[statistical mechanics]]/[[thermodynamics]], then called _thermal quantum field theory_ or _quantum statistical field theory_ or similar.

$$
  \array{
  \left.
  \array{
     \text{relativistic field theory}
     \\
     \text{on Minkowski spacetime}
     \\
     \mathbb{R}^{d,1}
     \\
     \text{in a thermal equilibrium state}
     \\
     \text{at temperature}\; T
  }
  \right\}
  &
  \;\;\;\;
  \overset{ \text{Wick rotation} }{\leftrightarrow}
  \;\;\;\;
  &
  \left\{
  \array{
    \text{Euclidean field theory}
    \\
    \text{on Euclidean space}
    \\
    \mathbb{R}^d \times S^1_{\beta}
    \\
    \text{with compact/periodic Euclidean time}
    \\
    \text{of length} \; \beta = 1/T
  }
  \right.
  \\
  \phantom{A}
  \\
  \underset{
    {
    \text{equal-time n-point function} 
    \atop 
    \text{of relativistic fields}
    }
    \atop
    \text{ in thermal equilibrium state } \; \vert T\rangle
  }{
  \underbrace{
    \left\langle  T\vert  :\mathbf{\Phi}(x_1,t) \mathbf{\Phi}(x_2,t) \cdots \mathbf{\Phi}(x_n,t) : \vert T \right\rangle_{\mathbb{R}^{d,1}}
  }}
  &\;=\;&
  \underset{
    \text{correlator of Euclidean fields}
    \atop
    \text{ for "Euclidean time" of periodicity}\; \beta = 1/T
  }{
  \underbrace{
  \left\langle 0 \vert \mathbf{\Phi}(x_1,t) \mathbf{\Phi}(x_2,t) \cdots \mathbf{\Phi}(x_n,t)  \vert 0 \right\rangle_{\mathbb{R}^{d} \times S^1_{\beta}}
  }}
  }
$$

<center>
<img src="https://ncatlab.org/nlab/files/EuclideanTime.jpg" width="580">
</center>

> graphics grabbed form [Frolov-Zelnikov 11](#FrolovZelnikov11)

Notice that the evident [[symmetry breaking|breaking]] of [[Lorentz group|Lorentz symmetry]] on the right side of this correspondence is perfectly consistent with what happens on the left hand: A thermal vacuum state in Minkowski spacetime also singles out a preferred Lorentz frame.


The basic idea of this relation seems to go back to [Bloch 58](#Bloch58). The physics literature often states this suggestively but informally in terms of [[path integral]]-imagery, see e.g. [Moore 03, section 1.1](#Moore03).

The first precise formulation seems to be due to [Høegh-Krohn 74](#HoeghKrohn74) (in 1+1 dimensions) and a more comprehensive discussion in view of the [[Osterwalder-Schrader theorem]] for compact Euclidean time is due to [Klein-Landau 81](#KleinLandau81).

The use of a "periodic Euclidean time coordinate" is also known as _[[Matsubara formalism]]_ (e.g. [Landsman-vanWert 87, section 2.3.1](#LandsmanVanWert87)) and specifically the condition that the periodicity has to be $\beta \coloneqq 1/T$ is known as the _[[KMS conditions]]_ for a _[[KMS state]]_ (For _Kubo-Martin-Schwinger_, due to [Kubo 57](#Kubo57), [Martin-Schwinger 59](#MartinSchwinger59) with its final form due to [Haag-Hugenholtz-Winnink 67](#HaagHugenholtzWinnink67), see [Fulling-Ruijsenaars 87, section 3.1](#FullingRuijsenaars87)).

Beware that literature discussing the KMS-condition often does not make the periodicity of Euclidean time explicit, and vice versa. This is clarified in [Fulling-Ruijsenaars 87, sections 2 and 3](#FullingRuijsenaars87).

General introduction to Euclidean and thermal field theory includes [Thoma 00, section 2.2](#Thoma00), [Peeters-Zamaklar 09, section 1.3](#PeetersZamaklar09).



## Examples

* [[Ising model]]

## Related concepts

* [[inverse temperature]]

* [[instanton]], [[caloron]]

* [[2d CFT]]

* [[relativistic field theory]]

* [[lattice gauge theory]]

* [[infinite-temperature thermal field theory]]

## References

### General

General introduction to Euclidean field theory includes

* {#PeetersZamaklar09} [[Kasper Peeters]], [[Marija Zamaklar]], _Euclidean Field Theory_, Lecture notes 2009-2011 ([web](http://maths.dur.ac.uk/users/kasper.peeters/eft.html), [pdf](http://maths.dur.ac.uk/users/kasper.peeters/pdf/eft.pdf))

A systematic development of Euclidean [[renormalization|renormalized]] [[perturbative quantum field theory]] with [[correlators as differential forms on configuration spaces of points]] is described in

* {#BergbauerBrunettiKreimer09} [[Christoph Bergbauer]], [[Romeo Brunetti]], [[Dirk Kreimer]], _Renormalization and resolution of singularities_ ([arXiv:0908.0633](https://arxiv.org/abs/0908.0633))

* {#Bergbauer09} [[Christoph Bergbauer]], _Renormalization and resolution of singularities_, talks as IHES and Boston, 2009 ([pdf](http://www.emg.uni-mainz.de/Dateien/bergbauer.pdf))


* {#Berghoff14a} [[Marko Berghoff]], _Wonderful renormalization_, 2014 ([pdf](http://www2.mathematik.hu-berlin.de/%7Ekreimer/wp-content/uploads/Berghoff-Marko.pdf), [doi:10.18452/17160](https://doi.org/10.18452/17160))

* {#Berghoff14b} [[Marko Berghoff]], _Wonderful compactifications in quantum field theory_,  Communications in Number Theory and Physics Volume 9 (2015) Number 3 ([arXiv:1411.5583](https://arxiv.org/abs/1411.5583))


### Thermal quantum field theory

A good introduction is in 

* {#FullingRuijsenaars87} S.A. Fulling, S.N.M. Ruijsenaars, _Temperature, periodicity and horizons_, Physics Reports Volume 152, Issue 3, August 1987, Pages 135-176 ([pdf](https://www1.maths.leeds.ac.uk/~siru/papers/p26.pdf), <a href="https://doi.org/10.1016/0370-1573(87)90136-0">doi:10.1016/0370-1573(87)90136-0</a>)


The idea of Wick rotating thermal relativistic field theory to compact periodic Euclidean time apparently goes back to 

* {#Bloch58} Claude Bloch, _Sur la détermination de l'état fondamental d'un système de particules_,  Nucl. Phys. 7 (1958) 451

This has maybe first been made precise, for the case of 1+1 dimensions, in 

* {#HoeghKrohn74} [[Raphael Høegh-Krohn]], _Relativistic Quantum Statistical Mechanics in two-dimensional Space-Time_, Communications in Mathematical Physics 38.3 (1974): 195-224 ([pdf](https://www.duo.uio.no/bitstream/handle/10852/44072/1973-22.pdf))

A systematic discussion of the [[Osterwalder-Schrader theorem]] on [[Wick rotation]] for the case of thermal field theory/periodic Euclidean time is in 

* {#KleinLandau81} Abel Klein, Lawrence Landau, _Periodic Gaussian Osterwalder-Schrader positive processes and the two-sided Markov property on the circle_, Pacific Journal of Mathematics, Vol. 94, No. 2, 1981 ([
DOI: 10.2140/pjm.1981.94.341](https://msp.org/pjm/1981/94-2/p12.xhtml), [pdf](https://msp.org/pjm/1981/94-2/pjm-v94-n2-p12-s.pdf))

See also

* [Fulling-Ruijsenaars 87, section 2](#FullingRuijsenaars87)


The formulation of the KMS condition is due to

* {#Kubo57} R. Kubo _Statistical-Mechanical Theory of Irreversible Processes  I. General Theory and Simple Applications to Magnetic and Conduction Problems_, Journal of the Physical Society of Japan 12, 570-586 1957

* {#MartinSchwinger59} Paul C. Martin, [[Julian Schwinger]], _Theory of Many-Particle Systems.  I_, Physical Review 115, 1342-1373 (1959)

and found its final, now generally accepted, form in 

* {#HaagHugenholtzWinnink67} [[Rudolf Haag]], N. M. Hugenholtz, M. Winnink, _On the equilibrium states in quantum statistical mechanics_, Comm. Math. Phys. Volume 5, Number 3 (1967), 215-236 ([euclid:1103840050](https://projecteuclid.org/euclid.cmp/1103840050))

Review of thermal field theory via Euclidean field theory includes

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

In application to [[black hole thermodynamics]]:

* [Fulling-Ruijsenaars 87, section 4](#FullingRuijsenaars87)

* {#GibbonsPerry78} [[Gary Gibbons]], Malcolm J. Perry, _Black Holes and Thermal Green Functions_, Vol. 358, No. 1695 (1978) ([jstor:79482](https://www.jstor.org/stable/79482))

* {#FrolovZelnikov11} [[Valeri Frolov]], Andrei Zelnikov, section F4.4 of _Introduction to black hole physics_, Oxford 2011

Discussion of thermal [[Wick rotation]] on global [[anti-de Sitter spacetime]] (which is already periodic in _real_ time) is in

* {#AllenFolacciGibbons87} B. Allen, A. Folacci, [[Gary Gibbons]], _Anti-de Sitter space at finite temperature_, Physics Letters B Volume 189, Issue 3, 7 May 1987, Pages 304-310 (<a href="https://doi.org/10.1016/0370-2693(87)91437-7">doi:10.1016/0370-2693(87)91437-7</a>)

The expansion of thermal field theory around the [[infinite-temperature thermal field theory|infinite-temperature-limit]] (i.e. around [[inverse temperature]] $\beta = 1/T = 0$, i.e. [[KK-reduction]] in compact/periodic Euclidean time) is discussed in

* {#Ginsparg80} [[Paul Ginsparg]], _First and second order phase transitions in gauge theories at finite temperature_, Nuclear Physics B Volume 170, Issue 3, 15 December 1980, Pages 388-408 (<a href="https://doi.org/10.1016/0550-3213(80)90418-6">doi:10.1016/0550-3213(80)90418-6</a>)

* {#AppelquistPisarski81} Thomas Appelquist, [[Robert Pisarski]], _High-temperature Yang-Mills theories and three-dimensional quantum chromodynamics_, Phys. Rev. D 23, 2305 (1981) ([doi:10.1103/PhysRevD.23.2305](https://doi.org/10.1103/PhysRevD.23.2305))

* {#Nadkarni83} Sudhir Nadkarni, _Dimensional reduction in finite-temperature quantum chromodynamics_, Phys. Rev. D 27, 917 (1983) ([doi:10.1103/PhysRevD.27.917](https://doi.org/10.1103/PhysRevD.27.917))

* {#Nadkarni88} Sudhir Nadkarni, _Dimensional reduction in finite-temperature quantum chromodynamics. II_, Phys. Rev. D 38, 3287 (1988) ([doi:10.1103/PhysRevD.38.3287](https://doi.org/10.1103/PhysRevD.38.3287))

* {#Jourjine84} Alexander N Jourjine, _Quantum field theory in the infinite temperature limit_, Annals of Physics Volume 155, Issue 2, July 1984, Pages 305-332 (<a href="https://doi.org/10.1016/0003-4916(84)90003-4">doi:10.1016/0003-4916(84)90003-4</a>)

* [[Klaas Landsman]], _Limitations to dimensional reduction at high temperature_, Nuclear Physics B Volume 322, Issue 2, 14 August 1989, Pages 498-530 (<a href="https://doi.org/10.1016/0550-3213(89)90424-0">doi:10.1016/0550-3213(89)90424-0</a>)

* T. Reisz, _Realization of dimensional reduction at high temperature_, Z. Phys. C - Particles and Fields (1992) 53: 169 ([doi:10.1007/BF01483886](https://doi.org/10.1007/BF01483886))

* {#Braaten95} Eric Braaten, _Solution to the Perturbative Infrared Catastrophe of Hot Gauge Theories_, Phys. Rev. Lett. 74, 2164 (1995) ([doi:10.1103/PhysRevLett.74.2164](https://doi.org/10.1103/PhysRevLett.74.2164))

* {#KajantieaLaineRummukainenShaposhnikov96} K. Kajantiea, M. Laine, K. Rummukainen, M. Shaposhnikov, _Generic rules for high temperature dimensional reduction and their application to the standard model_, Nuclear Physics B Volume 458, Issues 1–2, 1 January 1996, Pages 90-136 (<a href="https://doi.org/10.1016/0550-3213(95)00549-8">doi:10.1016/0550-3213(95)00549-8</a>)

and specifically with an eye to discussion of the [[quark-gluon plasma]] in

* {#BlaizotIancuRebhan03} Jean-Paul Blaizot, Edmond Iancu, Anton Rebhan, _Thermodynamics of the high temperature quark gluon plasma_, Quark–Gluon Plasma 3, pp. 60-122 (2004) ([arXiv:hep-ph/0303185](https://arxiv.org/abs/hep-ph/0303185), [spire:615570](http://inspirehep.net/record/615570))

General discussion for [[QCD]]:

* Jacopo Ghiglieri, Aleksi Kurkela, Michael Strickland, Aleksi Vuorinen, _Perturbative Thermal QCD: Formalism and Applications_ ([arXiv:2002.10188](https://arxiv.org/abs/2002.10188))


See also

* Wikipedia, _[Thermal quantum field theory](https://en.wikipedia.org/wiki/Thermal_quantum_field_theory)_

* Wikipedia, _[Matsubara frequency](https://en.wikipedia.org/wiki/Matsubara_frequency)_

* Wolfram Math World, _[KMS condition](http://mathworld.wolfram.com/KMSCondition.html)_

[[!redirects Euclidean field theories]]

[[!redirects thermal quantum field theory]]
[[!redirects thermal quantum field theories]]
[[!redirects thermal QFT]]


[[!redirects thermal field theory]]
[[!redirects thermal field theories]]


[[!redirects Matsubara formalism]]
[[!redirects Matsubara formalisms]]

[[!redirects Matsubara frequency]]
[[!redirects Matsubara frequencies]]



[[!redirects KMS condition]]
[[!redirects KMS conditions]]
