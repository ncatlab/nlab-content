
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents# 
* automatic table of contents goes here
{:toc}

## Idea

_Quantum field theory_ is the general framework for the description of the fundamental processes in [[physics]] as understood today. Notably the [[standard model of particle physics]] is a quantum field theory and has been the main motivation for the development of the concept in general. 

Historically quantum field theory grew out of attempts to combine [[classical field theory]] in the context of [[special relativity]] with [[quantum mechanics]]. While some aspects of it are understood in exceeding detail, the overall picture of what quantum field theory actually is used to be quite mysterious. There are two main approaches for axiomatizing and formalizing the notion:

* algebraic quantum field theory: [[AQFT]] -- this encodes a quantum field theory as an assignment of [[operator algebra]]s "of observables" to patches of [[spacetime]];

* functorial quantum field theory: [[FQFT]] -- this encodes a quantum field theory as an assignment of _spaces of quantum states_ to patches of [[codimension]] 1, and of maps between spaces of states -- the time evolution opeator -- to [[cobordism]]s between such patches.

Both these approaches try to capture the notion of a _full_ quantum field theory. On the other hand, much activity in physics is concerned with [[perturbative quantum field theory]]. This is a priori to be thought of as an approximation to a full quantum field theory akin to the approximation of a function by its Taylor series, but not the least because it is often the only available technique, the tools of perturbative quantum field theory are to some extent also taken as a definition of quantum field theory. 

The gap for instance between the formal study of the [[AQFT]] axioms and physics as done in practice by physicists had to a large extent been due to the fact that [[AQFT]] had little to say about perturbative quantum field theory. But recently this has been changing. See [[perturbative quantum field theory]] for more.


Recent times have seen major progress in understanding these axiomatizations and connecting them to the structures studied in [[physics]] (see the references below), but still the number of interesting phenomena in quantum field theory that physicist handle semi-rigorously and that are waiting for a fully formal understanding is large.



## Higher categories in quantum field theory

Even though _quantum field theory_ has been around for decades and has been very successful both as a phenomenological model in experimental physics as well as a source of deep mathematical structures and theorems, from a mathematical perspective it is still to a large extent mysterious, though recently much progress is being made.

There are essentially two alternative approaches for formalizing quantum field theory and making it accessible to mathematical treatment: 

 * _algebraic quantum field theory_: [[AQFT]] 

 * _functorial quantum field theory_: [[FQFT]]. 

(Other structures which are used to define quantum field theories, such as [[vertex operator algebra]]s are now more or less understood to be special cases of these two approaches. See there for details.)

Both [[AQFT]] and [[FQFT]] involve the language of [[category theory]] and  [[higher category theory]]. In fact, a couple of important higher categorical structures were motivated from and first considered in the context of quantum field theory. For instance 

* John Roberts first conceived the idea of $\infty$-categorical [[nonabelian cohomology]] in the context of [[AQFT]].

* the description of 2-dimensional [[CFT]] and 3-dimentional [[TFT]] in terms of [[modular tensor categories]] provides a major application of the theory of [[monoidal categories]];

* the notion of the [[(∞,n)-category of cobordisms]], which is thought to play a role analogous to and as fundamental as the [[sphere spectrum]] was motivated from [[FQFT]];

* In early 1990s [[A-∞ categories]] first appeared in works of [[Maxim Kontsevich|Kontsevich]] and Fukaya on the categorical description of twisted [[sigma model]]s what is then used in the formulation of [[homological mirror symmetry]].

* the [[cobordism hypothesis]] was formulated by [[John Baez]] and [[Jim Dolan] in the context of extended [[topological quantum field theory|topological]] [[FQFT]].

* various structures involving [[(∞,1)-operad]]s, such as [[topological chiral homology]] and [[blob homology]] are motivated by and find their application in the algebraic description of quantum field theory;

* the description of higher background [[gauge field]]s very much motivated the development and study of [[differential cohomology]], which like all notions of [[cohomology]] is intrinsically about [[(∞,1)-topos]] theory.

There are some indications that such [[higher category theory|higher categorical structures]], such as those appearing in [[groupoidification]], are essential for clarifying some of the mysteries of quantum field theory, such as the [[path integral]]. While this is far from being clarified, this is what motivates research in higher categorical structures in QFT. 

Ours is the age to figure this out.


## References

* P. Deligne, P. Etingof, D.S. Freed, L. Jeffrey, D. Kazhdan, J. Morgan, D.R. Morrison and E. Witten, eds.  _Quantum fields and strings, A course for mathematicians_, 2 vols. Amer. Math. Soc. Providence 1999. ([web version](http://www.math.ias.edu/qft))

* V. S. Varadarajan, _Supersymmetry for mathematicians: an introduction_, AMS and Courant Institute, 2004.

* R. E. [[Borcherds]], A. Barnard, _Lectures on QFT_, [arxiv:math-ph/0204014](http://arxiv.org/abs/math-ph/0204014)

A short introduction to different aspects of QFT usually covered in a first course is this:

* Gerald B. Folland, _Quantum field theory: A tourist guide for mathematicians_, Math. Surveys and Monographs __149__ ([ZMATH] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1155.81003&format=complete))

An extensive compilation of QFT from the viewpoint of a mathematician: 

* [[Eberhard Zeidler]], _Quantum field theory. A bridge between mathematicians and physicists. I: Basics in mathematics and physics._ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1124.81002&format=complete)), _II: Quantum electrodynamics_ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1155.81005&format=complete))

Differential geometric and topological aspects (e.g. connections to index theorems and moduli spaces) are emphasized in

* Charles Nash, _Differential topology and quantum field theory_, Acad. Press 1991. 

* [[Albert Schwarz]], Quantum field theory and topology, Grundlehren der Math. Wissen. __307__, Springer 1993.  

* [[Branislav Jurco]], [[Hisham Sati]], [[Urs Schreiber]], _Mathematical foundations of quantum field and perturbative string theory_ Proceedings of Symposia in Pure Mathematics, AMS (<a href="http://ncatlab.org/schreiber/show/Mathematical+Foundations+of+Quantum+Field+and+Perturbative+String+Theory">web</a>).

For further references see [[FQFT]] and [[AQFT]].



[[!redirects QFT]]
[[!redirects quantum field theories]]
