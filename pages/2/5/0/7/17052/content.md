

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum Field Theory
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

Calorons are topologically non-trivial [[field (physics)|field]]-configurations in [[Yang-Mills theory]] at [[thermal field theory|positive temperature]] $T \gt 0$. They correspond to what at vanishing [[temperature]] $T =  0$ are called [[instantons]], specifically [[BPST instantons]] (but there is no continuous limit relating the two).

While the physical reality of [[instantons]] is at best subtle (they are interpreted as witnessing [[quantum tunneling]] between actual [[vacua]]) calorons are meant to correspond to actual [[vacua]] of [[Yang-Mills theory]] at [[thermal field theory|positive temperature]], reflecting the general statement that [[Wick rotation]] has good physical meaning at positive temperature.

More in detail:

Upon [[Wick rotation]], $G$-[[Yang-Mills theory]] on [[Minkowski spacetime]] $\mathbb{R}^{3,1}$ in a [[KMS state]] of [[positive number|positive]] [[temperature]] $T$ is expressed by [[Euclidean field theory]] on the [[Riemannian manifold]] $\mathbb{R}^3 \times S^1_{\beta}$, where the first factor is 3-dimensional [[Euclidean space]] and the second factor is a [[circle]] of [[length]] $\beta \coloneqq 1/T$ (proportional to) the inverse [[temperature]].

A _caloron_ is a [[gauge field]]-configuration in this Euclidean Yang-Mills theory on $\mathbb{R}^3 \times S^1_\beta$ [[vanishing at infinity]]. By the [[clutching construction]] the topological class of these bundles (their [[second Chern class]] for [[gauge group]] a  [[simple Lie group]]) is given by [[homotopy classes]] of maps

$$
  S^2 \times S^1 \longrightarrow G
$$

hence

$$
  S^3 \times S^1 \longrightarrow B G
$$

For the case $G = $ [[special unitary group|SU(2)]] $\simeq S^3$ and via the usual math/physics translation of terminology ([here](BPST-instanton#FromTheMathsToThePhysicsStory)) this was first considered in [Harrington-Shepard 77, p. 3](#HarringtonShepard77), and baptized a "caloron"-configuration in [Harrington-Shepard 78, p. 1](#HarringtonShepard78).

A further refinement of the construction included the nonzero [[vacuum expectation value]] $\langle (A_4)^3\rangle$ of the "time" component of the [[vector potential]], called the _KvBLL caloron_ ([Kraan-van Baal 98a](#KraanVanBaal98a), [Kraan-van Baal 98b](#KraanVanBaal98b), [Lee-Lu 98](#LeeLu98)).

This solution revealed the substructure: it  gets  split  into $N_c$ (number  of  colors)  separate  (anti)self- dual  3d  solitons  with  nonzero  (Euclidean)  electric  and  magnetic charges (see e.g. [Larsen-Shuryak 14](#LarsenShuryak14)).




## Properties

### Relation to confinement
 {#RelationToConfinement}

As part of a possible solution to the [[confinement]]/[[mass gap]]-problem:

[Greensite 11, section 8.5](#Greensite11):

> it is natural to wonder if [[confinement]] could be derived from some [[semiclassical approximation|semiclassical]] treatment of [[Yang–Mills theory]] based on the [[instanton]] solutions of [[nonabelian group|non-abelian]] [[gauge theories]]. The [[BPST instanton|standard]] [[instantons]], introduced by Belavin et al. ([40](BPST-instanton#BelavinPolyakovSchwartzTyupkin75)), do not seem to work; their [[field strengths]] fall off too rapidly to produce the desired  magnetic  disorder in the vacuum.  

> In  recent  years,  however, it has been realized that instanton solutions at [[thermal field theory|finite temperature]], known as _calorons_, might do the job. These caloron solutions were introduced independently by Kraan and van Baal  ([41](#KraanVanBaal98), [42](#KraanVanBaal98b)) and Lee and Lu  ([43](#LeeLu98)) (KvBLL), and they have the remarkable property of containing [[monopole]] constituents which may, depending on the type of caloron, be widely separated.

> $[...]$

> The caloron idea is probably the most promising current version of [[monopole]] [[confinement]] in pure non-abelian gauge theories, but it is  basically  (in certain [[gauge fixing|gauges]]) a superposition of [[monopoles]] with spherically  symmetric abelian fields, and this leads to the same questions raised in connection with monopole Coulomb gases.

### Relation to heterotic string theory

The _gauge solution_ of the [[NS5-brane]] in [[heterotic string theory]] contains a [[gauge field]] on the transverse space $\mathbb{R}^4$ which is a [[BPST-instanton]]. Then, if we consider an array of [[NS5-brane]]s at fixed distance along the circle of a compactified transverse space $\mathbb{R}^3\times S^1$, we obtain a Harrington-Shepard [[caloron]] (see e.g. [SasYat16, pag.12](#Sasaki-Yata16)). If we send the radius to zero $R\rightarrow 0$ we obtain a smeared [[NS5-brane]] in [[heterotic string theory]].

## History

The paper [Harrington-Shepard 1978](#Harrington-Shepard_78) considers the contribution from periodic solutions at _positive, finite_ temperature to the [[Yang-Mills equations]] to the action of a 'Yang-Mills gas': an equilibrium ensemble of YM fields. They give explicit solutions to the classical equations of motion 'of charge 1' i.e. representing a generator in the [[homotopy group]] classifying topologically inequivalent solutions. 


[[Werner Nahm|Nahm]] ([Nahm 1984](#Nahm_84)) continued the study of calorons, linking them with self-dual [[monopoles]] and the [[ADHM construction]].

## Related concepts

* [[instanton]], [[soliton]], [[vortex]]

* [[thermal field theory]]

* [[caloron correspondence]]

* [[Nahm transform]]


## References

### General

The concept was introduced in

* {#HarringtonShepard77} Barry J. Harrington, Harvey K. Shepard, _Euclidean solutions and finite temperature gauge theory_, Nuclear Physics B Volume 124, Issue 4, 27 June 1977, Pages 409-412 (<a href="https://doi.org/10.1016/0550-3213(77)90413-8">doi:10.1016/0550-3213(77)90413-8</a>)

* {#HarringtonShepard78} Barry J. Harrington, Harvey K. Shepard, _Periodic Euclidean solutions and the finite-temperature Yang-Mills gas_, Phys. Rev. D 17, 2122 &#8211; April 1978 ([doi:10.1103/PhysRevD.17.2122](https://doi.org/10.1103/PhysRevD.17.2122))

Further development includes

* {#Nahm_84} W. Nahm, _Self-dual monopoles and calorons_, in Group Theoretical Methods in Physics, Ed. G. Denardo, G. Ghirardi, and T. Weber,  Lecture Notes in Physics **201** (1984) pp 189-200. doi:[10.1007/BFb0016145](http://dx.doi.org/10.1007/BFb0016145)

* {#KraanVanBaal98a} Thomas C. Kraan, Pierre van Baal, _Periodic Instantons with non-trivial Holonomy_, Nucl.Phys. B533 (1998) 627-659 ([arXiv:hep-th/9805168](https://arxiv.org/abs/hep-th/9805168))

* {#KraanVanBaal98b} Thomas C. Kraan, Pierre van Baal, _Exact T-duality between Calorons and Taub-NUT spaces_, Phys.Lett.B428:268-276, 1998 ([arXiv:hep-th/9802049](https://arxiv.org/abs/hep-th/9802049))

* {#LeeLu98} Kimyeong Lee, Changhai Lu, _$SU(2)$ Calorons and Magnetic Monopoles_, Phys. Rev. D 58, 025011 (1998) ([arXiv:hep-th/9802108](https://arxiv.org/abs/hep-th/9802108))

See also

* Wikipedia, _[Caloron](https://en.wikipedia.org/wiki/Caloron)_

Discussion in [[lattice gauge theory]]:

* P. Gerhold, E.‐M. Ilgenfritz, M. Müller‐Preussker, B. V. Martemyanov, A. I. Veselov, _Topology and confinement at $T \neq 0$: calorons with non‐trivial holonomy_, AIP Conference Proceedings 892, 213 (2007) ([doi:10.1063/1.2714375](https://doi.org/10.1063/1.2714375))

### Relation to skyrmions, instantons, monopoles

The construction of [[Skyrmions]] from [[instantons]] is due to 

* {#AtiyahManton89} [[Michael Atiyah]], N S Manton, _Skyrmions from instantons_, Phys.  Lett.  B, 222(3):438–442, 1989 (<a href="https://doi.org/10.1016/0370-2693(89)90340-7">doi:10.1016/0370-2693(89)90340-7</a>)

The relation between [[skyrmions]], [[instantons]], [[calorons]], [[solitons]] and [[monopoles]] is usefully reviewed and further developed in 

* {#Cork18a} [[Josh Cork]], _Calorons, symmetry, and the soliton trinity_, PhD thesis, University of Leeds 2018 ([web](http://etheses.whiterose.ac.uk/22097/))

* {#Cork18b} [[Josh Cork]], _Skyrmions from calorons_, J. High Energ. Phys. (2018) 2018: 137 ([arXiv:1810.04143](https://arxiv.org/abs/1810.04143))


### In confinement/mass gap

Discussion as part of a solution to the [[confinement]]/[[mass gap]]-problem:

* {#Greensite11} Jeff Greensite, _An Introduction to the Confinement Problem_, Lecture Notes in Physics, Volume 821, 2011 ([doi:10.1007/978-3-642-14382-3](https://link.springer.com/book/10.1007%2F978-3-642-14382-3))


* P. Gerhold, E.-M. Ilgenfritz, M. Müller-Preussker, _An $SU(2)$ KvBLL caloron gas model and confinement_, Nucl.Phys.B760:1-37, 2007 ([arXiv:hep-ph/0607315](https://arxiv.org/abs/hep-ph/0607315))

* {#LarsenShuryak14}  Rasmus Larsen, [[Edward Shuryak]], _Classical interactions of the instanton-dyons with antidyons_, Nucl. Phys. A **950**, 110 (2016) ([arXiv:1408.6563](https://arxiv.org/abs/1408.6563))

* {#LarsenShuryak15} Rasmus Larsen, [[Edward Shuryak]], _Interacting Ensemble of the Instanton-dyons and Deconfinement Phase Transition in the SU(2) Gauge Theory_, Phys. Rev. D 92, 094022, 2015 ([arXiv:1504.03341](https://arxiv.org/abs/1504.03341))

### Relation to NS5-brane in heterotic string theory

* {#SasakiYata16} Shin Sasaki and Masaya Yata, _Non-geometric five-branes in heterotic supergravity_,  JHEP **1611**, 064, 2016 ([arXiv:1608.01436](https://arxiv.org/abs/1608.01436))



[[!redirects calorons]]