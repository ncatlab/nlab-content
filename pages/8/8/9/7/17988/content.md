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

In the context of [[quantum field theory]] (QFT) the term _asymptotic safety_ ([Weinstein 79](#Weinstein79)) refers to the situation where a QFT may not be [[renormalization|renormalizable]] (is not defined on all scales by the choice of a [[finite number]] of [[coupling constants]]), but has the property that its [[renormalization group flow]] has a non-trivial [[non-perturbative effect|non-perturbative]] [[fixed point]] such that the subspace of the space of [[coupling constants]] whose RG-flow converges to this fixed point is [[finite number|finite]] [[dimension|dimensional]]. 

> One defines the "UV-critical hypersurface" as the set of all those points in the infinite-dimensional theory space which are "pulled" into the fixed point by the inverse RG flow: trajectories lying in this surface approach the fixed point for increasing momentum scales. General arguments and known examples suggest that the UV-critical hypersurface has a finite dimensionality. This dimensionality equals the number of (infrared-) relevant couplings, i.e. couplings which get attracted to the fixed point in the UV. The important point is that once the value of these (few) couplings are known at some scale all other (irrelevant) couplings are fixed by requiring an asymptotically safe theory, that is a trajectory which lies entirely in the UV-critical hypersurface. By this means we achieve that, first, the couplings are determined by a finite number of measurements rendering the theory predictive, and, second, the UV behavior is unproblematic without any unphysical divergences. ([Nink-Reuter 12, p. 2](#NinkReuter12))

A key example of a non-renormalizable QFT is [[Einstein gravity]], and there is speculation that it might be asymptotically safe, and that this might be the solution to the construction of [[quantum gravity]] ([Reuter 96](#Reuter96)).

Issues that the program of asymptotic safety of gravity is facing include the following:

1. All existing computations that see hints for a UV-fixed point do so by first applying a drastic truncation to the space of couplings, and then checking only whether there is a UV-fixed point for the RG-flow in the remaining small subspace. It seems unclear to which extent these approximate considerations may be extrapolated.

1. Most existing computations consider only pure Einstein gravity without matter coupling. It seems unclear to which extent these results may be extrapolated to the situation where matter is taken account of (but see [Biemans-Platania-Saueressig 17](#BiemansPlataniaSaueressig17)).

1. If one assumes (as is widely, but no generally believed) that [[Bekenstein-Hawking entropy]] seen in classical gravity is to correspond to a microscopic [[entropy]] of its quantum degrees of freedom, then the scaling of this entropy with area as opposed to volume contradicts the assumption that [[quantum gravity]] is a [[local field theory]] at small scales and higher energies ([Shomer 07, section IV](#Shomer07)) and hence then it contradicts the asymptotic safety of gravity. 

   Similarly, if one trusts the [[AdS/CFT correspondence]] then gravity is fundamentally not a local field theory, only its boundary [[CFT]] is, in contradiction with asymptotic safety of gravity ([Shomer 07, section IV](#Shomer07)).

## References

The idea of asymptotic safety as such and as a cure for [[quantum gravity]] is due to

* {#Weinstein79} [[Steven Weinberg]], _Ultraviolet divergences in quantum theories of gravitation_, in "General Relativity: An Einstein centenary survey", ed. S. W. Hawking and W. Israel. Cambridge University Press. pp. 790&#8211;831 (1979) ([spire](https://inspirehep.net/record/159043/))

It gained new popularity with this result:

* {#Reuter96} [[Martin Reuter]], _Nonperturbative Evolution Equation for Quantum Gravity_, Phys.Rev. D57 (1998) 971-985 ([arXiv:hep-th/9605030](https://arxiv.org/abs/hep-th/9605030))

An attempt to conceptually explain why [[gravity]] might have a UV-fixed point is in this article:

* {#NinkReuter12} Andreas Nink, [[Martin Reuter]], _On quantum gravity, Asymptotic Safety, and paramagnetic dominance_, Int. J. Mod. Phys. D22 (2013) 1330008 ([arXiv:1212.4325](https://arxiv.org/abs/1212.4325))

Review of the asymptotic safety program includes these:

* {#Niedermaier06} [[Max Niedermaier]], _The Asymptotic Safety Scenario in Quantum Gravity -- An Introduction_, Class.Quant.Grav.24:R171-230,2007 ([arXiv:gr-qc/0610018](https://arxiv.org/abs/gr-qc/0610018))

* [[Max Niedermaier]], [[Martin Reuter]], _The Asymptotic Safety Scenario in Quantum Gravity_, Living Reviews in Relativity December 2006, 9:5 [doi:10.12942/lrr-2006-5](http://link.springer.com/article/10.12942/lrr-2006-5)

The following review provides concise background on actual technical details:

* {#Shomer07} Assaf Shomer, _A pedagogical explanation for the non-renormalizability of gravity_ ([arXiv:0709.3555](https://arxiv.org/abs/0709.3555))

See also

* {#BiemansPlataniaSaueressig17} Jorn Biemans, Alessia Platania, Frank Saueressig, _Renormalization group fixed points of foliated gravity-matter systems_ ([arXiv:1702.06539](https://arxiv.org/abs/1702.06539))


