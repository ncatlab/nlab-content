
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

**Algebraic Quantum Field Theory** or **Axiomatic Quantum Field Theory** or **AQFT** for short is a formalization of [[quantum field theory]] (and specifically full, hence [[non-perturbative quantum field theory]]) that axiomatizes the assignment of _[[algebras of observables]]_ to patches of parameter space ([[spacetime]], [[worldvolume]]) that one expects a quantum field theory to provide.

As such, the approach of AQFT is roughly dual to that of [[FQFT]], where instead _spaces of states_ are assigned to boundaries of [[cobordism]]s and propagation maps between state spaces to cobordisms themselves.

One may roughly think of AQFT as being a formalization of what in basic [[quantum mechanics]] textbooks is called the **[[Heisenberg picture]]** of quantum mechanics. On the other hand [[FQFT]] axiomatizes the _[[Schrödinger picture]]_ .

The axioms of traditional AQFT encode the properties of a [[local net]] of observables and are called the [[Haag-Kastler axioms]]. They are one of the oldest systems of axioms that seriously attempt to put [[quantum field theory]] on a solid conceptual footing. 

From the [[nPOV]] we may think of a [[local net]] as a co-flabby [[presheaf|copresheaf]] of [[algebra|algebras]] on spacetime which satisfies a certain _locality_ axiom with respect to the 
[[smooth Lorentzian manifold|Lorentzian structure]] of [[spacetime]]: 

* **locality:** algebras assigned to spacelike separated regions commute with each other when embedded into any joint superalgebra.

This is traditionally formulated (implicitly) as a structure in ordinary [[category theory]]. More recently, with the proof of the [[cobordism hypothesis]] and the corresponding [[(∞,n)-category]]-formulation of [[FQFT]] also [[higher category theory|higher categorical]] versions of systems of local algebras of observables are being put forward and studied. Three structures are curently being studied, that are all conceptually very similar and similar to the Haag-Kastler axioms:


* [[factorization algebra]]s

* [[topological chiral homology]]

* [[blob homology]].

Initially, all three of these encoded what in physics are called _Euclidean_ quantum field theories, whereas only the notion of [[local net]] incorporated the fact that the underlying spacetime of a quantum field theory is a [[smooth Lorentzian space]]. Recent developments in the formalism of [[factorization algebra]]s have extended their theory to globally hyperbolic [[Lorentzian manifolds]]. 
 

In the context of the Haag-Kastler axioms there is a precise theorem, the [[Osterwalder-Schrader theorem]], relating the Euclidean to the Lorentzian formulation: this is the operation known as [[Wick rotation]].

Sheaves are used explicitly in:

* Roberts, John E.: [New light on the mathematical structure of algebraic field theory.](http://books.google.com/books?id=IFjzuLjE43kC&lpg=PA297&ots=5Ld1B3I45m&dq=Operator%20algebras%20and%20applications%2C%20Part%202&pg=PA523#v=onepage&q=Operator%20algebras%20and%20applications,%20Part%202&f=false)  Operator algebras and applications, Part 2 (Kingston, Ont., 1980),  pp. 523&#8211;550, Proc. Sympos. Pure Math., 38, Amer. Math. Soc., Providence, R.I., 1982.

* Roberts, John E.: [Localization in algebraic field theory](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.cmp/1103921341). Comm. Math. Phys. 85 (1982), no. 1, 87&#8211;98.

--- much information to be filled in ---


## Axioms

* [[Wightman axioms]]

* [[Haag-Kastler axioms]]

## Theorems

* [[Reeh-Schlieder theorem]]

* [[Osterwalder-Schrader theorem]]

* [[PCT theorem]]

* [[Bisognano-Wichmann theorem]]

* [[spin-statistics theorem]]

## Properties

Generically the algebra of a relativistic AQFT turns out to be a ([[generalized the|the]]) hyperfinite type $III_1$ [[von Neumann algebra factor]]. See ([Yngvason](#Yngvason))

## Examples
 {#Examples}

Examples of AQFT [[local nets of observables]] that encode interacting quantum field theories are not easy to construct. The construction of _free_ field theories is well understood, see the references [below](#ExamplesReferences). In [[perturbation theory]] also interacting theories can be constructed, see the references [here](#ReferencesPerturbationTheory).

### Free scalar field / Klein Gordon field
 {#FreeScalarField}

A survey of the AQFT description of the [[free field theor|free]] [[scalar field]] on [[Minkowski spacetime]] is in ([Motoya, slides 11-17](#Montoya)). Discussion in more general context of [[AQFT on curved spacetimes]] in ([Brunetti-Fredenhagen, section 5.2](#BrunettiFredenhagen))

### Free fermion / Dirac field


The [[free field theory|free]] [[Dirac field]] and its deformations is discussed for instance in ([DLM, section 3.2](#DLM)), ([Dimock 83](#Dimock82)).


### Electromagnetic field

The quantized [[electromagnetic field]] is discussed for instance in ([Dimock 92](#Dimock92)).

### Proca field

([Furliani](#Furliani))



## Related concepts

* [[quantum mechanics]], [[quantum field theory]], [[perturbative quantum field theory]]

  * **AQFT**

    * [[Haag-Kastler axioms]], [[Wightman axioms]]

    * [[local net of observables]], [[field net]]

    * [[quantum lattice systems]], [[string-localized quantum field]]

    * [[locally covariant AQFT]]

    * [[perturbative AQFT]]

    * [[homotopical algebraic quantum field theory]]

    * [[Haag-Ruelle scattering theory]]


  * [[FQFT]]

* [[constructive quantum field theory]]

[[!include Isbell duality - table]]




## References

### Axioms

The original article that introduced the [[Haag-Kastler axioms]] is

* {#Haag64} [[Rudolf Haag]], [[Daniel Kastler]], _An algebraic approach to quantum field theory_ , Journal of Mathematical Physics, Bd.5, 1964, S.848-861 

following 

* {#Haag59} [[Rudolf Haag]], _Discussion des "axiomes" et des propri&#233;t&#233;s asymptotiques d&#8217;une th&#233;orie des champs locales avec particules compos&#233;es, Les Probl&#232;mes Math&#233;matiques de la Th&#233;orie Quantique des Champs_, Colloque Internationaux du CNRS LXXV (Lille 1957), CNRS Paris (1959), 151.

The generalization of the [[spacetime]] [[site]] from open in [[Minkowski space]] to more general and [[curvature|curved]] spacetimes (see [[AQFT on curved spacetimes]]) is due to

* {#BrunettiFredenhagen} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Quantum field theory on curved spacetimes_ [arXiv:0901.2063](http://arxiv.org/abs/0901.2063)
 

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], [[Rainer Verch]], _The generally covariant locality principle -- A new paradigm for local quantum physics_ Commun. Math. Phys. 237:31-68 (2003) ([arXiv:math-ph/0112041](http://arxiv.org/abs/math-ph/0112041))

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Quantum Field Theory on Curved Backgrounds_ , Proceedings of the Kompaktkurs "Quantenfeldtheorie auf gekruemmten Raumzeiten" held at Universitaet Potsdam, Germany, in 8.-12.10.2007, organized by C. Baer and K. Fredenhagen

See also _[[AQFT on curved spacetimes]]_ .

### Lecture notes and Textbooks

Introductory lecture notes include

* {#Fredenhagen03} [[Klaus Fredenhagen]], _Algebraische Quantenfeldtheorie_, lecture notes, 2003 ([[FredenhagenAQFT2003.pdf:file]])

* {#FewsterRejzner19} [[Christopher Fewster]], [[Kasia Rejzner]], _Algebraic Quantum Field Theory - an introduction_ ([arXiv:1904.04051](https://arxiv.org/abs/1904.04051))

and for just [[quantum mechanics]] in the algebraic perspective:

* {#Gleason09} Jonathan Gleason, _The $C*$-algebraic formalism of quantum mechanics_, 2009 ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2009/REUPapers/Gleason.pdf), [[GleasonAlgebraic.pdf:file]])

Classical textbooks are

* [[Huzihiro Araki]], _[[Mathematical Theory of Quantum Fields]]_

* [[Rudolf Haag]], _[[Local Quantum Physics -- Fields, Particles, Algebras]]_ 

A good account of the mathematical axiomatics of Haag-Kastler AQFT is

* [[Hans Halvorson]], [[Michael Müger]], _Algebraic Quantum Field Theory_ ([arXiv](http://arxiv.org/abs/math-ph/0602036))

This is, among other things, the ideal starting point for pure mathematicians who have always been left puzzled or otherwise unsatisfied by accounts of quantum field theory, even those tagged as being "for mathematicians". AQFT is truly axiomatic and rigorously formal. 

An account written by mathematicians for mathematicians is this:

* [[Hellmut Baumgärtel]], Manfred Wollenberg, _Causal nets of operator algebras._ Berlin: Akademie Verlag 1992 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0749.46038&format=complete))

and this:

* [[Hellmut Baumgärtel]], _Operator algebraic Methods in Quantum Field Theory. A series of lectures._ Akademie Verlag 1995 ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0839.46063&format=complete))

A classic of the trade is this one:

* [[Nikolay Bogolyubov]], Logunov, Oksak, Todorov: _General principles of quantum field theory_ (Mathematical Physics and Applied Mathematics, 10. Dordrecht etc.: Kluwer Academic Publishers, 1990)


### Reviews

Recent account of the principle of locality in AQFT from the point of view of traditional school

* [[Franco Strocchi]], _Relativistic Quantum Mechanics and Field Theory_, Found.Phys. 34 (2004) 501-527 ([arXiv:hep-th/0401143](http://arxiv.org/abs/hep-th/0401143))

* [[Sergio Doplicher]], _The principle of locality: Effectiveness, fate, and challenges_, J. Math. Phys. __51__, 015218 (2010), [doi](http://dx.doi.org/10.1063/1.3276100)

* [[Franco Strocchi]], _An Introduction to Non-Perturbative Foundations of Quantum Field Theory_, Oxford University Press, 2013


Talk slides include

* Edison Montoya, _Algebraic quantum field theory_ (2009) ([pdf](http://www.matmor.unam.mx/~robert/sem/20091021_Montoya.pdf))
 {#Montoya}

### Examples
 {#ExamplesReferences}

Construction of examples is considered for instance in

* [[Jonathan Dimock]], _Dirac quantum fields on a manifold_, Trans. Amer. Math. Soc. 269 (1982), 133-147. ([web](http://www.ams.org/journals/tran/1982-269-01/S0002-9947-1982-0637032-8/home.html))
 {#Dimock82}

* [[Jonathan Dimock]], _Quantized electromagnetic field on a manifdold_, Reviews in mathematical physics, Volume 4, Issue 2 (1992) ([web](http://www.worldscinet.com/rmp/04/0402/S0129055X92000078.html))
 {#Dimock92}

* Edward Furliani, _Quantization of massive vector fields in curved space&#8211;time_, J. Math. Phys. 40, 2611 (1999) ([web](http://jmp.aip.org/resource/1/jmapaq/v40/i6/p2611_s1?isAuthorized=no))
 {#Furliani}

General discussion of AQFT quantization of [[free quantum fields]] is in

* [[Christian Bär]], N. Ginoux, [[Frank Pfäffle]], _Wave Equations on Lorentzian Manifolds and Quantization_, (EMS, 2007) ([arXiv:0806.1036](http://arxiv.org/abs/0806.1036))

* [[Christian Bär]], N. Ginoux, _Classical and quantum fields on lorentzian manifolds_ (2011) ([arXiv:1104.1158](http://arxiv.org/abs/1104.1158))

Examples of [[non-perturbative quantum field theory|non-perturbative]] [[interacting quantum field theory|interacting]] [[scalar field theory]] in _any_ [[spacetime]] [[dimension]] (in particular in $d \geq 4$) are claimed in 

* [[Detlev Buchholz]], [[Klaus Fredenhagen]], _A $C^\ast$-algebraic approach to interacting quantum field theories_ ([arXiv:1902.06062](https://arxiv.org/abs/1902.06062))


### Local gauge theory
 {#LocalGaugeTheory}

Discussion of aspects of [[gauge theory]] includes

* Fabio Ciolli, [[Giuseppe Ruzzi]], Ezio Vasselli, _Causal posets, loops and the construction of nets of local algebras for QFT_ ([arXiv:1109.4824](http://arxiv.org/abs/1109.4824))

* Fabio Ciolli, [[Giuseppe Ruzzi]], Ezio Vasselli, _QED Representation for the Net of Causal Loops_ ([arXiv:1305.7059](http://arxiv.org/abs/1305.7059))

* [[Giuseppe Ruzzi]], _Nets of local algebras and gauge theories_, 2014 ([pdf slides](http://www.aqft14.eu/wp-content/uploads/2014/05/Ruzzi.pdf))


Construction and axiomatization of gauge field AQFT via [[homotopy theory]] and [[homotopical algebra]] (see also at _[[field bundle]]_) is being developed in

* {#BDS} [[Marco Benini]], [[Claudio Dappiaggi]], [[Alexander Schenkel]], _Quantized Abelian principal connections on Lorentzian manifolds_, Communications in Mathematical Physics 2013 ([arXiv:1303.2515](http://arxiv.org/abs/1303.2515))

* {#BeniniSchenkelSzabo15} [[Marco Benini]], [[Alexander Schenkel]], [[Richard Szabo]], _Homotopy colimits and global observables in Abelian gauge theory_ ([arXiv:1503.08839](http://arxiv.org/abs/1503.08839))

* {#BeniniSchenkel16} [[Marco Benini]], [[Alexander Schenkel]], _Quantum field theories on categories fibered in groupoids_ ([arXiv:1610.06071](https://arxiv.org/abs/1610.06071))

The issue of the tension between local gauge invariance and locality and the need to pass to [[stacks]]/[[higher geometry]] is made explicit in

* {#Schenkel14} [[Alexander Schenkel]], _On the problem of gauge theories
in locally covariant QFT_, talk at _[Operator and Geometric Analysis on Quantum Theory](http://www.science.unitn.it/~moretti/convegno/convegno.html)_ Trento, 2014 ([[SchenkelTrento2014.pdf:file]]) (with further emphasis on this point in the companion talk [Schreiber 14](field+bundle#Schreiber14)) 

Further development of this [[homotopical algebraic quantum field theory]] includes

* {#BeniniSchenkel16} [[Marco Benini]], [[Alexander Schenkel]], _Quantum field theories on categories fibered in groupoids_ ([arXiv:1610.06071](https://arxiv.org/abs/1610.06071))


### Perturbation theory and renormalization
 {#ReferencesPerturbationTheory}

[[perturbation theory|Perturbation theory]] and [[renormalization]] in the context of AQFT and  is discussed in the following articles.

The observation that in [[perturbation theory]] the [[renormalization|Stückelberg-Bogoliubov-Epstein-Glaser]] local [[S-matrix|S-matrices]] yield a [[local net of observables]] was first made in 

* V. Il'in, D. Slavnov, _Observable algebras in the S-matrix approach_ Theor. Math. Phys. **36** , 32 (1978)

which was however mostly ignored and forgotten. It is taken up again in

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_  Commun.Math.Phys.208:623-661 (2000) ([arXiv](http://arxiv.org/abs/math-ph/9903028))

(a quick survey is in section 8, details are in section 2).

Further developments along these lines are in

* [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic quantum field theory and deformation quantization_, Proceedings of the Conference on Mathematical Physics in Mathematics and Physics, Siena June 20-25 (2000) ([arXiv:hep-th/0101079](http://xxx.uni-augsburg.de/abs/hep-th/0101079)) 

(relation to [[deformation quantization]])

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_  Commun.Math.Phys.208:623-661 (2000) ([arXiv](http://arxiv.org/abs/math-ph/9903028))

* [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_ Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](http://arxiv.org/abs/0901.2038))

(relation to [[renormalization]])

* [[Michael Dütsch]], [[Klaus Fredenhagen]], _A local (perturbative) construction of observables in gauge theores: the example of qed_ , Commun. Math. Phys. 203 (1999), no.1, 71-105,  ([arXiv:hep-th/9807078](http://xxx.uni-augsburg.de/abs/hep-th/9807078)). 

(relation to [[gauge theory]] and [[QED]])

Lecture notes are in

* [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative algebraic quantum field theory_, In _Mathematical Aspects of Quantum Field Theories_, Springer 2016 ([arXiv:1208.1428](https://arxiv.org/abs/1208.1428))

* [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative Construction of Models of Algebraic Quantum Field Theory_ ([arXiv:1503.07814](https://arxiv.org/abs/1503.07814))

and a textbook acount is in 

* [[Katarzyna Rejzner]], _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([pdf](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))

### Further developments

* {#DLM} [[Claudio Dappiaggi]], [[Gandalf Lechner]], E. Morfa-Morales, _Deformations of quantum field theories on spacetimes with Killing vector fields_, Commun.Math.Phys.305:99-130, (2011), ([arXiv:1006.3548](http://arxiv.org/abs/1006.3548))

* [[Marco Benini]], [[Marco Perin]], [[Alexander Schenkel]], _Model-independent comparison between factorization algebras and algebraic quantum field theory on Lorentzian manifolds_, ([arXiv:1903.03396v2](https://arxiv.org/abs/1903.03396))

### Relation to holographic entanglement entropy

Discussion of [[local nets of observables]] in [[AQFT]] as the natural language for grasping [[holographic entanglement entropy]]:

* [[Edward Witten]], _Notes on Some Entanglement Properties of Quantum Field Theory_, Rev. Mod. Phys. 90, 45003 (2018) ([arXiv:1803.04993](https://arxiv.org/abs/1803.04993))

* [[Thomas Faulkner]], _The holographic map as a conditional expectation_ ([arXiv:2008.04810](https://arxiv.org/abs/2008.04810))
 

### Relation to functorial QFT

A relation to [[FQFT]] is discussed in

* [[Urs Schreiber]], _AQFT from $n$-functorial QFT_ , Comm. Math. Phys., Volume 291, Issue 2, pp.357-401 ([pdf](http://ncatlab.org/schreiber/files/AQFTfromFQFT.pdf))

The role of [[von Neumann algebra factor]]s is discussed in

* J. Yngvason, _The role of type III factors in quantum field theory_ ([arXiv:math-ph/0411058](http://arxiv.org/abs/math-ph/0411058))
 {#Yngvason}

[[!redirects algebraic quantum field theory]]
[[!redirects algebraic quantum field theories]]