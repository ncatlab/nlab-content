+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In the context of [[quantum field theory]] (QFT) the term _asymptotic safety_ ([Weinberg 79](#Weinstein79)) refers to the situation where a QFT may not be [[renormalization|renormalizable]] (is not defined on all scales by the choice of a [[finite number]] of [[coupling constants]]), but has the property that its [[renormalization group flow]] has a non-trivial [[non-perturbative effect|non-perturbative]] [[fixed point]] such that the subspace of the space of [[coupling constants]] whose RG-flow converges to this fixed point is [[finite number|finite]] [[dimension|dimensional]]. 

> One defines the "UV-critical hypersurface" as the set of all those points in the infinite-dimensional theory space which are "pulled" into the fixed point by the inverse RG flow: trajectories lying in this surface approach the fixed point for increasing momentum scales. General arguments and known examples suggest that the UV-critical hypersurface has a finite dimensionality. This dimensionality equals the number of (infrared-) relevant couplings, i.e. couplings which get attracted to the fixed point in the UV. The important point is that once the value of these (few) couplings are known at some scale all other (irrelevant) couplings are fixed by requiring an asymptotically safe theory, that is a trajectory which lies entirely in the UV-critical hypersurface. By this means we achieve that, first, the couplings are determined by a finite number of measurements rendering the theory predictive, and, second, the UV behavior is unproblematic without any unphysical divergences. ([Nink-Reuter 12, p. 2](#NinkReuter12))

A key example of a non-renormalizable QFT is [[Einstein gravity]], and there is speculation that it might be asymptotically safe, and that this might be the solution to the construction of [[quantum gravity]] ([Reuter 96](#Reuter96)).

## Issues
{#Issues}

Issues that the program of asymptotic safety of gravity is facing include the following:

### Theoretical issues

1. All existing computations that see hints for a UV-fixed point do so by first applying a drastic truncation to the space of couplings, and then checking only whether there is a UV-fixed point for the RG-flow in the remaining small subspace. It seems unclear to which extent these approximate considerations may be extrapolated.

1. Most existing computations consider only pure Einstein gravity without matter coupling. It seems unclear to which extent these results may be extrapolated to the situation where matter is taken account of (but see [Biemans-Platania-Saueressig 17](#BiemansPlataniaSaueressig17)).

1. {#DonoghueSummarizes} [Donoghue 19](#Donoghue19) claims technical problems with the handling of [[renormalization group flow]] in Newton's constant $G_N$ as currently practiced in the asymptotic safety program: 

    1. The "[[running coupling constant|running]]" $G_N(E)$ comes from power-divergent corrections that vanish in [[dimensional regularization]].

      1. Computing different [[Minkowski spacetime]] processes gives different power-divergent corrections: there is no generic common $G_N(E)$. 

      1. There is no generic [[energy]] $E$: some processes depend on $s \sim + E^2$, others on $t \sim -E^2$ and (unlike in the usual log running) this makes a difference.

1. If one assumes (as is widely, but no generally believed) that [[Bekenstein-Hawking entropy]] seen in classical gravity is to correspond to a microscopic [[entropy]] of its quantum degrees of freedom, then the scaling of this entropy with area as opposed to volume contradicts the assumption that [[quantum gravity]] is a [[local field theory]] at small scales and higher energies ([Shomer 07, section IV](#Shomer07)) and hence then it contradicts the asymptotic safety of gravity. 

   Similarly, if one trusts the [[AdS/CFT correspondence]] then gravity is fundamentally not a local field theory, only its boundary [[CFT]] is, in contradiction with asymptotic safety of gravity ([Shomer 07, section IV](#Shomer07)).

### Experimental issues

The near criticality of the [[Higgs field]] [[vacuum]] (see there at _[Higgs mass and vacuum (in-)stability](Higgs+field#MassAndVacuumInstability)_) implies that the [[coefficient]] $\lambda$ of the quartic part of the Higgs potential is close to zero after [[renormalization group flow]] ("RGE") to around the [[Planck scale]] of about $10^{19}$ [[GeV]] (e.g. [BDGGSSS 13, p. 17-18](#BDGGSSS13)):

<img src="https://ncatlab.org/nlab/files/HiggsQuarticCoupling.png" width="400"/>

In fact also the [[beta function]] $\beta_\lambda$ of the quartic coupling $\lambda$ (i.e. its logarithmic [[derivative]] with respect to [[scale]]) is close to zero around the [[Planck scale]] of about $10^{19}$ [[GeV]] ([BDGGSSS 13, p. 18](#BDGGSSS13)):

<img src="https://ncatlab.org/nlab/files/HiggsQuarticBetaFunctionRelative.png" width="400"/>


Earlier it has been suggested that this reflects the principle of asymptotic safety ([Shaposhnikov-Wetterich 09](#ShaposhnikovWetterich09)). But this would mean that not only $\lambda$ and its [[beta-function|RGE-derivative]] $\beta_\lambda$ vanish around the [[Planck scale]], but that in fact all higher derivatives do, too (see e.g [Niedermaier 06, equation (1.5)](#Niedermaier06)) hence that $\beta_\lambda$ asymptotes to zero. But this does not seem to be the case; in ([BDGGSSS 13, p. 17-18](#BDGGSSS13)) it says:

>  As shown in fig. 2 (upper right), the corresponding Higgs quartic [[beta-function]] vanishes at a [[scale]] of about $10^{17}$-$10^{18}$ [[GeV]]. In order to quantify the degree of cancellation in the β-function, we plot in fig. 2 (lower right) $\beta_\lambda$ in units of its pure [[top quark]] contribution.  The vanishing of $\beta_\lambda$ looks  more  like  an  accidental  cancellation  between  various  large  contributions, rather than an asymptotic approach to zero.


<img src="https://ncatlab.org/nlab/files/HiggsQuarticBetaFunction.png" width="800"/>


## References

The idea of asymptotic safety as such and as a cure for [[quantum gravity]] is due to

* {#Weinstein79} [[Steven Weinberg]], _Ultraviolet divergences in quantum theories of gravitation_, in "General Relativity: An Einstein centenary survey", ed. S. W. Hawking and W. Israel. Cambridge University Press. pp. 790&#8211;831 (1979) ([spire](https://inspirehep.net/record/159043/))

It gained new popularity with this result:

* {#Reuter96} [[Martin Reuter]], _Nonperturbative Evolution Equation for Quantum Gravity_, Phys.Rev. D57 (1998) 971-985 ([arXiv:hep-th/9605030](https://arxiv.org/abs/hep-th/9605030))

An attempt to conceptually explain why [[gravity]] might have a UV-fixed point is in this article:

* {#NinkReuter12} Andreas Nink, [[Martin Reuter]], _On quantum gravity, Asymptotic Safety, and paramagnetic dominance_, Int. J. Mod. Phys. D22 (2013) 1330008 ([arXiv:1212.4325](https://arxiv.org/abs/1212.4325))

Observation of a special role of spacetime dimension 2:

* {#LauscherReuter06} O. Lauscher, [[Martin Reuter]], _Asymptotic Safety in Quantum Einstein Gravity: nonperturbative renormalizability and fractal spacetime structure_,  In: Fauser B., Tolksdorf J., Zeidler E. (eds.) )Quantum Gravity_ Birkhäuser Basel 2006 ([arXiv:hep-th/0511260](https://arxiv.org/abs/hep-th/0511260), [doi:10.1007/978-3-7643-7978-0_15](https://doi.org/10.1007/978-3-7643-7978-0_15))

and speculation of this being related to the [[Connes-Lott model]] (see [here](2-spectral+triple#Connes06OnRelationToStringVacua)):

* {#Connes06} [[Alain Connes]],  p. 8 of _Noncommutative Geometry and the standard model with neutrino mixing_, JHEP0611:081,2006 ([arXiv:hep-th/0608226](http://arxiv.org/abs/hep-th/0608226))


Review of the asymptotic safety program includes these:

* {#Niedermaier06} [[Max Niedermaier]], _The Asymptotic Safety Scenario in Quantum Gravity -- An Introduction_, Class.Quant.Grav.24:R171-230,2007 ([arXiv:gr-qc/0610018](https://arxiv.org/abs/gr-qc/0610018))

* [[Max Niedermaier]], [[Martin Reuter]], _The Asymptotic Safety Scenario in Quantum Gravity_, Living Reviews in Relativity December 2006, 9:5 [doi:10.12942/lrr-2006-5](http://link.springer.com/article/10.12942/lrr-2006-5)

Critical review:

* {#Shomer07} Assaf Shomer, _A pedagogical explanation for the non-renormalizability of gravity_ ([arXiv:0709.3555](https://arxiv.org/abs/0709.3555))

* {#Donoghue19} [[John Donoghue]], _A Critique of the Asymptotic Safety Program_,  
Frontiers in Physics 8, 56 (2020)
([arXiv:1911.02967](https://arxiv.org/abs/1911.02967), [doi:10.3389/fphy.2020.00056](https://www.frontiersin.org/articles/10.3389/fphy.2020.00056/full))

See also

* Roberto Percacci, _Asymptotic Safety FAQs_ ([web](http://www.percacci.it/roberto/physics/as/faq.html))

* {#BiemansPlataniaSaueressig17} Jorn Biemans, Alessia Platania, Frank Saueressig, _Renormalization group fixed points of foliated gravity-matter systems_ ([arXiv:1702.06539](https://arxiv.org/abs/1702.06539))

The suggestion that asymptotic safety explains the observed [[mass]] of the [[Higgs particle]] is attributed to

* {#ShaposhnikovWetterich09} M. Shaposhnikov, [[Christof Wetterich]], _Asymptotic safety of gravity and the Higgs boson mass_, Phys. Lett. B 683 (2010) 196 ([arXiv:0912.0208](https://arxiv.org/abs/0912.0208))

but see p. 17 of

* {#BDGGSSS13} Dario Buttazzo, Giuseppe Degrassi, Pier Paolo Giardino, [[Gian Giudice]], Filippo Sala, Alberto Salvio, [[Alessandro Strumia]], section 7 of _Investigating the near-criticality of the Higgs boson_ ([arXiv:1307.3536](https://arxiv.org/abs/1307.3536))

and for more see at _[Higgs field -- Asymptotic safety?](https://ncatlab.org/nlab/show/Higgs%20field#AsymtoticSafetyOrNot)_

Application to [[scattering amplitudes]]:

* Jan H. Kwapisz, Krzysztof A. Meissner, _Asymptotic safety and quantum gravity amplitudes_ ([arXiv:2005.03559](https://arxiv.org/abs/2005.03559))

Unitarity in Asymptotic Safety:

* Alessia Platania, Christof Wetterich, _Non-perturbative unitarity and fictitious ghosts in quantum gravity_ ([arXiv:2009.06637](https://arxiv.org/abs/2009.06637))






