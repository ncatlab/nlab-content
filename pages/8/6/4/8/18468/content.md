
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
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


The formulation of [[quantum field theory]] has many aspects and perspectives. Two prominent threads are the following:

**1) [[perturbation theory]] by means of [[formal geometry|formal]] [[Feynman diagram]] expansions of ([[Wick rotation|Wick rotated]]) [[path integrals]]**

   This is the approach predominant in [[phenomenology]]. 

   It produces the [[observable]] [[numbers]] which are checked to great precision in [[experiments]] starting from the early development of [[quantum electrodynamics]], fully established with the success of [[quantum chromodynamics]] and recently culminating in the [[Higgs field]] physics seen at the [[LHC]] experiment, confirming the [[standard model of particle physics]].

   While many of the mathematical intricacies of this approach have found solutions over the decades, most of these rely on global properties of [[Minkowski spacetime]] such as translation invariance and existence of an invariant [[vacuum]] [[quantum state]], hence on a consistent concept of [[particles]], none of which generalizes robustly to [[quantum field theory on curved spacetimes]] of relevance in [[cosmology]], [[black hole radiation]] or the [[instanton in QCD|instanton vacuum of QCD]].


**2) [[algebraic quantum field theory]] by means of [[local nets]] of [[C*-algebras]] of [[observables]]**

   This is the approach predominant in [[mathematical physics]]. 

   It produces the structural [[theorems]] of quantum field theory, such as the [[PCT theorem]] and the [[spin-statistics theorem]] and it seamlessly generalizes to [[QFT on curved spacetimes]].

   In its insistence on [[C*-algebras]] its ambition is to describe the full [[non-perturbative quantum field theory|non-perturbative]] quantum field theory. But as a matter of fact not a single relevant example ([[interaction|interacting]] QFT in spacetime dimensions 4 or greater) is known. Indeed, the construction of the motivating example, [[quantization of Yang-Mills theory]], is one of the open "millenium problems".

$\,$

But more recently a synthesis of these two threads has been developed:

**3) [[locally covariant perturbative quantum field theory]] by means of [[local nets]] of [[formal power series]] [[algebras of observables]]**

This rests on the observation ([Il'in-Slavnov 78](#IlinSlavnov78), [Brunetti-Fredenhagen 00](#BrunettiFredenhagen00)) that the formulation of [[renormalization]] by [Epstein-Glaser 73](#EpsteinGlaser73) naturally produces a [[local net]] of [[formal power series]] [[algebras of observables]]. Applied to [[gauge theory]] such as [[quantum electrodynamics]] this is known as _[[causal perturbation theory]]_ ([Scharf 95](#Scharf95)).

This formulation hence allows to construct the usual examples of [[perturbative quantum field theories]] in a rigorous fashion, and extend them to [[quantum field theory on curved spacetimes]], such as in formulation of perturbative [[quantum gravity]] ([Brunetti-Fredenhagen-Rejzner 13](#BrunettiFredenhagenRejzner13)).

$\,$

There remains however one problem: When applied to [[gauge theory]] on [[quantum field theory on curved spacetime|on curved spacetime]] the usual axioms on a [[local net]] break: either they enforce all [[characteristic classes]] of the [[gauge field]] ("[[instanton sectors]]") to be trivial, or else the axioms encoding locality are broken. This remaining issue is lifted by passing from plain [[algebras of observables]] to [[homotopical algebra|homotopical algebras]] ([[higher algebra|higher algebras]]), and hence to a formulation of [[homotopical algebraic quantum field theory]]. This is still in the making.

## References

Survey of locally covariant quantum field theory is in

* {#FredenhagenRejzner12} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative algebraic quantum field theory_, In _Mathematical Aspects of Quantum Field Theories_, Springer 2016 ([arXiv:1208.1428](https://arxiv.org/abs/1208.1428))

* {#FredenhagenRejzner15} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative Construction of Models of Algebraic Quantum Field Theory_ ([arXiv:1503.07814](https://arxiv.org/abs/1503.07814))

based on

* {#EpsteinGlaser73} [[Henri Epstein]] and [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211.

* {#IlinSlavnov78} V. A. Il'in and D. S. Slavnov, _Observable algebras in the S-matrix approach_, Theor. Math. Phys. 36 (1978) 32.

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661,2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

and developed as [[causal perturbation theory]] for [[gauge theory]] such as [[quantum electrodynamics]] in 

* {#Scharf95} [[Günter Scharf]], _Finite Quantum Electrodynamics: The Causal Approach_, Berlin: Springer-Verlag, 1995, 2nd edition

Discussion of perturbative [[quantum gravity]] in this perspective is in 

* {#BrunettiFredenhagenRejzner13} [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Quantum gravity from the point of view of locally covariant quantum field theory_ ([arXiv:1306.1058](https://arxiv.org/abs/1306.1058))

