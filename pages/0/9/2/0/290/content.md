
> This entry provides some broad pointers. For a detailed introduction see _[[geometry of physics -- perturbative quantum field theory]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Functorial Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--



#Contents# 
* table of contents
{:toc}

## Idea

_Quantum field theory_ is the general framework for the description of the fundamental processes in [[physics]] as understood today. These are carried by configurations of [[field (physics)|fields]] under the generalized rules of [[quantum mechanics]], therefore the name. Notably the [[standard model of particle physics]] is a quantum field theory and has been the main motivation for the development of the concept in general. 

Historically quantum field theory grew out of attempts to combine [[classical field theory]] in the context of [[special relativity]] with [[quantum mechanics]]. While some aspects of it are understood in exceeding detail, the overall picture of what quantum field theory actually is used to be quite mysterious. There are two main approaches for axiomatizing and formalizing the notion:

* algebraic quantum field theory: [[AQFT]] -- this encodes a quantum field theory as an assignment of [[operator algebra]]s "of observables" to patches of [[spacetime]];

* functorial quantum field theory: [[FQFT]] -- this encodes a quantum field theory as an assignment of _spaces of quantum states_ to patches of [[codimension]] 1, and of maps between spaces of states -- the time evolution operator -- to [[cobordism]]s between such patches.

Both these approaches try to capture the notion of a _full_ quantum field theory. On the other hand, much activity in physics is concerned with [[perturbative quantum field theory]]. This is a priori to be thought of as an approximation to a full quantum field theory akin to the approximation of a function by its Taylor series, but not the least because it is often the only available technique, the tools of perturbative quantum field theory are to some extent also taken as a definition of quantum field theory. 

The gap for instance between the formal study of the [[AQFT]] axioms and physics as done in practice by physicists had to a large extent been due to the fact that [[AQFT]] had little to say about perturbative quantum field theory. But recently this has been changing. See [[perturbative quantum field theory]] for more.

Recent times have seen major progress in understanding these axiomatizations and connecting them to the structures studied in [[physics]] (see the references below), but still the number of interesting phenomena in quantum field theory that physicists handle semi-rigorously and that are waiting for a fully formal understanding is large.


## Locally covariant perturbative quantum field theory
 {#LocallyCoveriantPerturbativeQuantumFieldTheory}

The formulation of [[quantum field theory]] has many aspects and perspectives. Two almost complementary threads are the following:

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

This rests on the observation ([Il'in-Slavnov 78](#IlinSlavnov78), [Brunetti-Fredenhagen 00](#BrunettiFredenhagen00)) that the formulation of [[renormalization]] in [[causal perturbation theory]] ([Epstein-Glaser 73](#EpsteinGlaser73), [Scharf 95](#Scharf95)) produces a [[local net]] of [[formal power series]] [[algebras of observables]]. 

This formulation hence allows to construct the usual examples of [[perturbative quantum field theories]] in a rigorous fashion, and then to extend them to [[quantum field theory on curved spacetimes]], such as in formulation of perturbative [[quantum gravity]] ([Brunetti-Fredenhagen-Rejzner 13](#BrunettiFredenhagenRejzner13)).

There remains just one problem: 

When applied to [[gauge theory]] on [[quantum field theory on curved spacetime|on curved spacetime]] the usual axioms on a [[local net]] break: either they enforce all [[characteristic classes]] of the [[gauge field]] ("[[instanton sectors]]") to be trivial, or else the axioms encoding locality are broken (see [Schenkel 14](#Schenkel14), [Schreiber 14](https://ncatlab.org/schreiber/show/Higher+field+bundles+for+gauge+fields)).

This remaining problem is solved by passing from plain [[algebras of observables]] to [[homotopical algebra|homotopical algebras]] ([[higher algebra|higher algebras]]), and hence to a formulation of **[[homotopical algebraic quantum field theory]]** (see [Schenkel 17](#Schenkel17)). This is still in the making.


## Higher categories in quantum field theory

(See also [[higher category theory and physics]] and ([SatiSchreiber](#SatiSchreiber))).

Even though _quantum field theory_ has been around for decades and has been very successful both as a phenomenological model in experimental physics as well as a source of deep mathematical structures and theorems, from a mathematical perspective it is still to a large extent mysterious, though recently much progress is being made.

There are essentially two alternative approaches for formalizing quantum field theory and making it accessible to mathematical treatment: 

 * _algebraic quantum field theory_: [[AQFT]] 

 * _functorial quantum field theory_: [[FQFT]]. 

(Other structures which are used to define quantum field theories, such as [[vertex operator algebra]]s are now more or less understood to be special cases of these two approaches. See there for details.)

Both [[AQFT]] and [[FQFT]] involve the language of [[category theory]] and  [[higher category theory]]. In fact, a couple of important higher categorical structures were motivated from and first considered in the context of quantum field theory. For instance 

* [[John Roberts]] first conceived the idea of $\infty$-categorical [[nonabelian cohomology]] in the context of [[AQFT]].

* the description of 2-dimensional [[CFT]] and 3-dimensional [[TFT]] in terms of [[modular tensor categories]] provides a major application of the theory of [[monoidal categories]];

* the notion of the [[(∞,n)-category of cobordisms]], which is thought to play a role analogous to, and as fundamental as, that of the [[sphere spectrum]] was motivated from [[FQFT]];

* In early 1990s [[A-∞ categories]] first appeared in works of [[Maxim Kontsevich|Kontsevich]] and Fukaya on the categorical description of twisted [[sigma model]]s what is then used in the formulation of [[homological mirror symmetry]].

* the [[cobordism hypothesis]] was formulated by [[John Baez]] and [[Jim Dolan]] in the context of extended [[topological quantum field theory|topological]] [[FQFT]].

* various structures involving [[(∞,1)-operad]]s, such as [[topological chiral homology]] and [[blob homology]] are motivated by, and find their application in, the algebraic description of quantum field theory;

* the description of higher background [[gauge field]]s very much motivated the development and study of [[differential cohomology]], which like all notions of [[cohomology]] is intrinsically about [[(∞,1)-topos]] theory.

There are some indications that such [[higher category theory|higher categorical structures]], such as those appearing in [[groupoidification]], are essential for clarifying some of the mysteries of quantum field theory, such as the [[path integral]]. While this is far from being clarified, this is what motivates research in higher categorical structures in QFT. 

Ours is the age to figure this out.

## Examples

* [[free field theory]]

* [$\phi^4$ theory](http://ncatlab.org/nlab/show/phi%5E4+theory)

* [[topological quantum field theory]]

* [[gauge theory]]

  * [[electromagnetism]]: [[QED]], 

  * [[Yang-Mills theory]]: [[QCD]]

* [[conformal field theory]]

## Related concepts

* [[relativistic quantum field theory]]

* [[Euclidean quantum field theory]], [[thermal quantum field theory]]

* [[scattering amplitude]]

* [[perturbation theory]] 

  * [[Feynman diagram]], 

  * [[Feynman rule]], [[worldline formalism]]

  * [[renormalization]]

* [[non-perturbative quantum field theory]]

* [[AQFT]], [[FQFT]], 

  * [[local quantum field theory]], [[extended quantum field theory]]

  * [[topological quantum field theory]]

* [[constructive quantum field theory]]

* [[prequantum field theory]]

  * [[Lagrangian]], [[extended Lagrangian]], [[action functional]]

* [[geometry of physics -- perturbative quantum field theory]]

* [[QFT on non-commutative spacetime]]


## References

The early history of the subject is outlined in 

* [[Rudolf Haag]], _Early papers on quantum field theory (1929-1930)_ ([pdf](https://link.springer.com/content/pdf/bfm%3A978-3-642-70078-1%2F1%2F1.pdf))

* [Scharf 95, section 0.0](#Scharf95)


Introductions include

* _[[geometry of physics -- perturbative quantum field theory]]_

* [[Arnold Neumaier]], chapter B of _[Theoretical Physics FAQ](http://www.mat.univie.ac.at/~neum/physfaq/physics-faq.html)_

* Gerald B. Folland, _Quantum field theory: A tourist guide for mathematicians_, Math. Surveys and Monographs __149__ ([ZMATH] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1155.81003&format=complete))

* [[Richard Borcherds]], A. Barnard, _Lectures on QFT_, ([arxiv:math-ph/0204014](http://arxiv.org/abs/math-ph/0204014))

A standard textbook written from the perspective of [[effective field theory]] is

* {#Weinberg95} [[Steven Weinberg]] _The Quantum Theory of Fields_, Cambridge University Press (1995)



An extensive compilation of material on QFT aiming for mathematical precision is

* [[Eberhard Zeidler]], _Quantum field theory. A bridge between mathematicians and physicists. I: Basics in mathematics and physics._ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1124.81002&format=complete)), _II: Quantum electrodynamics_ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1155.81005&format=complete)), _III: Gauge theory_ ([ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1228.81005&format=complete)).


Survey of the mathematically rigorous discussion in [[locally covariant perturbative quantum field theory]] is in

* {#FredenhagenRejzner12} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative algebraic quantum field theory_, In _Mathematical Aspects of Quantum Field Theories_, Springer 2016 ([arXiv:1208.1428](https://arxiv.org/abs/1208.1428))

* {#FredenhagenRejzner15} [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative Construction of Models of Algebraic Quantum Field Theory_ ([arXiv:1503.07814](https://arxiv.org/abs/1503.07814))

based on the [[causal perturbation theory]] of

* {#EpsteinGlaser73} [[Henri Epstein]] and [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211.

* {#IlinSlavnov78} V. A. Il'in and D. S. Slavnov, _Observable algebras in the S-matrix approach_, Theor. Math. Phys. 36 (1978) 32.

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661,2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

and developed as [[causal perturbation theory]] for [[gauge theory]] such as [[quantum electrodynamics]] in 

* {#Scharf95} [[Günter Scharf]], _[[Finite Quantum Electrodynamics -- The Causal Approach]]_, Berlin: Springer-Verlag, 1995, 2nd edition

and for [[quantum chromodynamics]] and perturbative [[quantum gravity]] in 

* {#Scharf01} [[Günter Scharf]], _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001



Discussion of perturbative [[quantum gravity]] in this perspective is in 

* {#BrunettiFredenhagenRejzner13} [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Quantum gravity from the point of view of locally covariant quantum field theory_ ([arXiv:1306.1058](https://arxiv.org/abs/1306.1058))

and survey of the generalization to [[gauge theory]] via [[homotopical algebraic quantum field theory]] is in 

* {#Schenkel14} [[Alexander Schenkel]], _On the problem of gauge theories
in locally covariant QFT_, talk at _[Operator and Geometric Analysis on Quantum Theory](http://www.science.unitn.it/~moretti/convegno/convegno.html)_ Trento, 2014 ([[SchenkelTrento2014.pdf:file]]) (with further emphasis on this point in the companion talk [Schreiber 14](field+bundle#Schreiber14)) 

* {#Schenkel17} [[Alexander Schenkel]], _Towards Homotopical Algebraic Quantum Field Theory_, talk at _[Foundational and Structural Aspects of Gauge Theories](https://indico.mitp.uni-mainz.de/event/76/overview)_,
Mainz Institute for Theoretical Physics, 29 May &#8211; 2 June 2017. ([pdf](http://aschenkel.eu/Mainz17.pdf))



A discussion of aspects of QFT with an eye towards applications in [[string theory]] and _aimed_ at mathematicians (though requiring more of a physicist's mindset than many pure mathematicians will find themselves in) is

* [[Pierre Deligne]], P. Etingof, [[Dan Freed]], L. Jeffrey, D. Kazhdan, J. Morgan, D.R. Morrison and [[Edward Witten]], eds.  _[[Quantum Fields and Strings]], A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))


Aspects of [[topology]] and [[differential geometry]]  (e.g. connections to [[index theorems]] and [[moduli spaces]]) are emphasized in

* Charles Nash, _Differential topology and quantum field theory_, Acad. Press 1991. 

An indication of the modern foundational picture of quantum mechanics is attempted in

* {#SatiSchreiber} [[Hisham Sati]], [[Urs Schreiber]], _Mathematical foundations of quantum field and perturbative string theory_ Proceedings of Symposia in Pure Mathematics, AMS (<a href="http://ncatlab.org/schreiber/show/Mathematical+Foundations+of+Quantum+Field+and+Perturbative+String+Theory">web</a>).
 

See also

* [[Albert Schwarz]], _Quantum field theory and topology_, Grundlehren der Math. Wissen. __307__, Springer 1993.  


* [[Graeme Segal]], _[[Three Roles of Quantum Field Theory]]_ , Felix Klein lectures, Bonn (2011)

For further references see _[[FQFT]]_ and _[[AQFT]]_.


See also

* [[Tom Banks]], _Modern quantum field theory, A concise introduction_ ([pdf](http://web.phys.ntnu.no/~mika/banks.pdf))

[[!redirects quantum field theories]]


[[!redirects QFT]]
[[!redirects QFTs]]




