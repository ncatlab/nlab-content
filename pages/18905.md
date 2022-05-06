

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

In [[field theory]] one speaks of _Euclidean field theory_ if the underlying [[spaces]] on which the [[field (physics)|fields]] are defined are [[Riemannian manifolds]], as opposed to [[Lorentzian  manifold|Lorentzian]] [[spacetimes]] used in [[relativistic field theory]]. Hence in Euclidean field theory there is no "[[time]]", one may understand this as essentially being [[statistical mechanics]]. 

In good situations [[Wick rotation]] relates Euclidean field theory with [[relativistic field theory]].




### Thermal quantum field theory via periodic Euclidean time
 {#ThermalQuantumFieldTheoryViaPeriodicEuclideanTime}

The equal-time [[n-point functions]] in [[relativistic field theory]] on [[Minkowski spacetime]] $\mathbb{R}^{d,1}$ in a [[vacuum state]] reflecting equilibrium at [[finite number|finite]] [[temperature]] $T$ may be argued ([Bloch 58](#Bloch58)) to be computed equivalently by Euclidean field theory on the [[Cartesian product]] $\mathbb{R}^d \times S^1$ of [[Euclidean space]] $\mathbb{R}^d$ with a [[circle]] $S^1$ of [[length|circumference]] $\beta \coloneqq 1/T$ (e.g. [Moore 03, section 1.1](#Moore03)):

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


This perspective is known as _[[thermal quantum field theory]]_ or similar, the use of a "periodic Euclidean time coordinate" is also known as _[[Matsubara formalism]]_ and specifically the condition that the periodicity has to be $\beta \coloneqq 1/T$ is known as the _[[KMS conditions]]_.

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

The idea goes back to 

* {#Bloch58} Claude Bloch, _Sur la détermination de l'état fondamental d'un système de particules_,  Nucl. Phys. 7 (1958) 451

Review includes

* [[Jean Zinn-Justin]], _Quantum Field Theory at Finite Temperature: An Introduction_ ([arXiv:hep-ph/0005272](https://arxiv.org/abs/hep-ph/0005272))

* {#Thoma00} Markus H. Thoma, _New Developments and Applications of Thermal Field Theory_ ([arXiv:hep-ph/0010164](https://arxiv.org/abs/hep-ph/0010164))

* Yuhao Yang, _An Introduction to Thermal Field Theory_, 2011 ([pdf](https://www.imperial.ac.uk/media/imperial-college/research-centres-and-groups/theoretical-physics/msc/dissertations/2011/Yuhao-Yang-Dissertation.pdf))

* Yi-Cheng Huang, _Field Theory in the Imaginary-time Formulation_ ([arXiv:1311.1990v4](https://arxiv.org/abs/1311.1990v4))

Further discussion:

* Christian D. Jäkel, _The Reeh–Schlieder property for thermal field theories_, Journal of Mathematical Physics 41, 1745 2000 ([doi:10.1063/1.533208](https://doi.org/10.1063/1.533208))

* {#JaehelRobl11} Christian D. Jäkel, Florian Robl, _The relativistic KMS condition for the thermal $n$-point functions of the $P(\phi)_2$ model_ ([arXiv:1103.3609](https://arxiv.org/abs/1103.3609))



With an eye towards [[lattice gauge theory]]:

* {#Moore03} Guy Moore, _Informal lectures on lattice gauge theory_, 2003 ([pdf](https://theorie.ikp.physik.tu-darmstadt.de/qcd/moore/latt_lectures.pdf))

With an eye towards [[black hole thermodynamics]]:

* {#FrolovZelnikov11} [[Valeri Frolov]], Andrei Zelnikov, section F4.4 of _Introduction to black hole physics_, Oxford 2011

See also

* Wikipedia, _[Thermal quantum field theory](https://en.wikipedia.org/wiki/Thermal_quantum_field_theory)_

* Wikipedia, _[Matsubara frequency](https://en.wikipedia.org/wiki/Matsubara_frequency)_

* Wolfram Math World, _[KMS condition](http://mathworld.wolfram.com/KMSCondition.html)_

[[!redirects Euclidean field theories]]

[[!redirects thermal quantum field theory]]
[[!redirects thermal quantum field theories]]

[[!redirects Matsubara formalism]]
[[!redirects Matsubara formalisms]]

[[!redirects Matsubara frequency]]
[[!redirects Matsubara frequencies]]



[[!redirects KMS condition]]
[[!redirects KMS conditions]]
