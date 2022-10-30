
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

What is called _causal perturbation theory_ is a mathematically rigorous construction of _[[perturbative quantum field theory|perturbative]]_ ([[gauge theory|gauge]]-) [[quantum field theory]], such as [[quantum electrodynamics]], based on a mathematical formulation of [[renormalization]] by St&#252;ckelberg-Bogoliubov-Epstein-Glaser ([Epstein-Glaser 73](#EpsteinGlaser73)).


A key idea of causal perturbation theory is that the [[interaction]] term $V$ is considered multiplied with some [[smooth function]] $g$ which has [[compact support]] on [[spacetime]]. This hence serves as a spacetime-dependent "[[coupling constant]]" which "switches off" the interaction outside a compact region, but not discontinuously as in many other schemes, but smoothly, hence "adiabatically" in terminology borrowed from [[thermodynamics]]. Therefore this is often called the "adiabatic switching" function, or similar

The corresponding [[S-matrix]] would informally be given by the expression

$$
  S_g \coloneqq T \exp\left( \int_X g(x) V(x) d\mu(x)_X \right)
$$

for $V$ the [[interaction]] term, and "$T$" indicating the [[time-ordered product]]. Causal perturbation theory proceeds by [[axiom|axiomatizing]] the key properties of this "adiabaticlly switched" [[S-matrix]] and then proving by [[induction]] that solutions to these axioms exist.  

One of these axioms is [[causal locality]], whence the name of the approach. This axiom asks that if adiabatic switching functions $g$ and $h$ have [[spacelike]] separated [[supports]] then the S-matrix _factors_

$$
  S_{g + h} = S_g S_h
  \,.
$$  

The [[time-ordered products]] $T(..)$ of [[field (physics)|fields]] are handled by splitting of [[distributions]] using tools from [[microlocal analysis]]. This is the mathematically rigorous step that takes care of what in other approaches are the "ultraviolet divergencies".

Originally the idea was that in the end the [[limit of a sequence|limit]] $g \to 1$ had to be taken, removing the adiabatic switching of the the compact support of the interaction. In general this limit does not exist ("infrared divergencies", e.g. [AAS 10, section 6](#AAS10)).

But in ([Ilin-Slavnov 78](#IlinSlavnov78)) it was observed that in fact the [[algebra of observables]] on any [[bounded subsets|bounded]] region may be computed with a $g$ whose [[compact support]] contains that region. Later in ([Brunetti-Fredenhagen 00](#BrunettiFredenhagen00)) it was pointed out that this means that causal perturbation theory in fact serves to construct the [[local net of observables]] of the [[perturbative quantum field theory]], as in the [[axioms]] for [[AQFT]], but with values in [[formal power series algebras]] (as befits a [[perturbation theory]]) instead of [[C*-algebras]] (suitable for [[non-perturbative quantum field theory]]). This leads to a unification of AQFT-concepts with [[perturbation theory]] in the theory of **[[locally covariant perturbative quantum field theory]]**.




## Related concepts

* [[locally covariant perturbative quantum field theory]]

## References



The method is due to

* {#EpsteinGlaser73} [[Henri Epstein]] and [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211.

It has been applied in detail to [[quantum electrodynamics]] in

* {#Scharf95} [[Günter Scharf]], _Finite Quantum Electrodynamics: The Causal Approach_, Berlin: Springer-Verlag, 1995, 2nd edition

and to general [[gauge theories]] in 

* [[Günter Scharf]], Quantum gauge theories: a true ghost story, Wiley, New York 2001. 

The observation that the method naturally leads to [[locally covariant perturbative quantum field theory]] is due to 

* {#IlinSlavnov78} V. A. Il'in and D. S. Slavnov, _Observable algebras in the S-matrix approach_, Theor. Math. Phys. 36 (1978) 32.

and was re-discovered and then popularized in

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661,2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))


Technical review includes

* {#AAS10} Andreas Aste, Cyrill von Arx, [[Günter Scharf]], _Regularization in quantum field theory from the causal point of view_, Prog. Part. Nucl. Phys.64:61-119, 2010 ([arXiv:0906.1952](https://arxiv.org/abs/0906.1952))

* Christian P&#246;selt, _The method of Epstein and Glaser I_, 2002 ([pdf](http://wwwthep.physik.uni-mainz.de/~scheck/Poeselt.pdf))

and, with an eye towards [[locally covariant perturbative quantum field theory]],

* {#FredenhagenRejzner15} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], section 4.1 of _Perturbative Construction of Models of Algebraic Quantum Field Theory_ ([arXiv:1503.07814](https://arxiv.org/abs/1503.07814))

Non-technical exposition includes

* [[Arnold Neumaier]], _[Causal Perturbation Theory](https://www.physicsforums.com/insights/causal-perturbation-theory/)_ (2015)

* [[Arnold Neumaier]], _[Action-based quantum field theory and causal perturbation theory](https://www.mat.univie.ac.at/~neum/physfaq/topics/causalQFT.html)_ (one section in _[A theoretical physics FAQ](http://www.mat.univie.ac.at/~neum/physfaq/physics-faq.html)_)


[[!redirects causal perturbation theories]]