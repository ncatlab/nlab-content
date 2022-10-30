
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Perturbative quantum field theory is [[quantum field theory]] where the [[interaction]] (between [[field (physics)|fields]]/[[particles]]) is treated as a tiny [[perturbation]] of the [[free field theory]], so that the resulting [[quantum observables]] are [[formal power series]] (in [[Planck's constant]] and) in the [[coupling constant]] which measures the strength of the interaction ("[[perturbation theory]]"). 

For all interesting theories this [[formal power series]] has vanishing [[radius of convergence]] ([Dyson 52](perturbation+theory#Dyson52)) and is regarded as an [[asymptotic series]]. Despite this apparent restriction, the perturbative quantum field theory of the [[standard model of particle physics]], where just the first handful of terms in the [[Feynman perturbation series]] is used, are in agreement with [[experiment]] to high precision. There are however [[non-perturbative effects]] which are not captured (such as [[instantons in QCD]]).

A rigorous formulation of perturbative quantum field theory is given by _[[causal perturbation theory]]_ and its extension to _[[perturbative algebraic quantum field theory]]_. See there for more. A key step in the construction is the _[[renormalization]]_ of the point interactions, see there for more.

The prescription for the construction of the perturbative [[S-matrix]] in [[causal perturbation theory]] and the perturbative [[local net of quantum observables]] (see [here](S-matrix#CausalLocality)) used to be ad-hoc, albeit well motivated by [[analogy]] with [[quantum mechanics]] and justified by it producing, rigorousy, the [[Feynman perturbation series]] of the [[S-matrix]] ([Keller 10 (IV.12)](#Keller10)).

Historically the [[Feynman perturbation series]] was motivated from intuition about the would-be [[path integral]], and this is still a popular point of view, albeit its lack of rigorous formulation. One may understand the axiomatics on the [[S-matrix]] in [[causal perturbation theory]] as defining the result of the perturbative path integral without actually doing an integration over field configurations.

But while [[path integral quantization]] for perturbative quantum field theory remains elusive, it has been shown that the (re-)normalized [[perturbative quantum field theory]] thus constructed via [[causal perturbation theory]] is, at least under favorable circumstances, equivalently the ([[Fedosov deformation quantization|Fedosov]]) [[formal deformation quantization]] of the [[covariant phase space]] induced by the given interacting [[Lagrangian density]] ([Collini 16](#Collini16)). This identifies the [[renormalization]] freedom with the usual freedom in choosing [[formal deformation quantization]]. 

This also suggest that the construction of the full [[non-perturbative quantum field theory]] ought to be given by a [[strict deformation quantization]] of the [[covariant phase space]]. But presently no example of such for non-trivial interaction in [[spacetime]] [[dimension]] $\geq 4$ is known.
In particular the [[phenomenology|phenomenologically]] interesting case of a complete construction of interacting field theories on 4-dimensional spacetimes is presently unknown. For the case of [[Yang-Mills theory]] this open problem is one of the "Millenium Problems" (see at _[[quantization of Yang-Mills theory]]_).


## Properties

* [[main theorem of perturbative renormalization theory]]

## Related concepts

* [[renormalization]]

* [[causal perturbation theory]]

* [[non-perturbative field theory]]

## References

The rigorous formulation of perturbative quantum field theory in terms of [[causal perturbation theory]] was first accomplished in 

* {#EpsteinGlaser73} [[Henri Epstein]], [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211 ([Numdam](http://www.numdam.org/item?id=AIHPA_1973__19_3_211_0 ))

Concrete examples have been spelled out for [[quantum electrodynamics]] in

* {#Scharf95} [[Günter Scharf]], _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

and for [[Yang-Mills theory]], [[quantum chromodynamics]] and perturbative [[quantum gravity]] in

* {#Scharf01} [[Günter Scharf]], _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001

For more see the references at _[[perturbative algebraic quantum field theory]]_.

The relation of the construction via [[causal perturbation theory]] to the [[Feynman perturbation series]] in terms of [[Feynman diagrams]] was understood in 

* {#GarciaBondiaLazzarini00} J.M. Gracia-Bondia, S. Lazzarini, _Connes-Kreimer-Epstein-Glaser Renormalization_ ([arXiv:hep-th/0006106](https://arxiv.org/abs/hep-th/0006106))

* {#Keller10} [[Kai Keller]], chapter IV of _Dimensional Regularization in Position Space and a Forest Formula for Regularized Epstein-Glaser Renormalization_, PhD thesis ([arXxiv:1006.2148](https://arxiv.org/abs/1006.2148))

* {#DuetschFredenhagenKellerRejzner14} [[Michael Dütsch]], [[Klaus Fredenhagen]], [[Kai Keller]], [[Katarzyna Rejzner]], _Dimensional Regularization in Position Space, and a Forest Formula for Epstein-Glaser Renormalization_, J. Math. Phy.
55(12), 122303 (2014) ([arXiv:1311.5424](https://arxiv.org/abs/1311.5424))




[[!redirects perturbative field theory]]

[[!redirects perturbative quantum field theories]]
