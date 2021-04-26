
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the context of [[nuclear physics]], by the *sign problem* in [[lattice quantum chromodynamics]] is is meant the issue that 

* for computational effectivity the [[partition function]] needs to be written as a (discretized) [[path integral]] of the exponentiated [[Euclidean field theory|Euclidean]] [[action functional]] against a [[probability density]] (the "quark matrix"), 

but 

* in many situations, notably at finite [[chemical potential]], the would-be [[probability]] [[measure]] turns out not to be positive definite, and in fact typically turns out to be [[complex number|complex]], 

* which means that various numerical evaluation methods fail.

The sign problem is one of the reasons that [[lattice QCD]] fails to be a fully satisfactory construction of [[non-perturbative quantum field theory|non-perturbative]] [[QCD]] even for practical purposes. For instance, much of the [[phase diagram]] of [[QCD]] remains unknown (e.g. [de Forcrand 13](#deForcrand13) [CQF21](#skyrmion#ChenQiuFukushima21)), since the sign problem prevents lattice QCD computations at "almost all points" in phase space ([Hsu-Reeb 08](#HsuReeb08)).
 
## References

Exposition:

* {#deForcrand13} Philippe de Forcrand, *The sign problem in Lattice QCD*, ETH 2013 ([pdf](https://www.int.washington.edu/talks/WorkShops/int_13_2a/People/deForcrand_P/deForcrand.pdf))

Original articles

* {#HsuReeb08} Stephen D.H. Hsu, David Reeb, *On the sign problem in dense QCD*, Int. J. Mod. Phys. A 25, pp. 53-67 (2010) ([arXiv:0808.2987](https://arxiv.org/abs/0808.2987))

* V. A. Goy, V. Bornyakov, D. Boyda, A. Molochkov, A. Nakamura, A. Nikolaev, V. Zakharov, *Sign problem in finite density lattice QCD*, Prog Theor Exp Phys (2017) 2017 (3): 031D01 ([arXiv:1611.08093](https://arxiv.org/abs/1611.08093))


See also:

* Wikipedia, _[Numerical sign problem](https://en.wikipedia.org/wiki/Numerical_sign_problem)_

[[!redirects sign problems in lattice QCD]]

[[!redirects sign problem]]
[[!redirects sign problems]]

