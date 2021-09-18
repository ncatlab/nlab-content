

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algbraic Quantum Field Theory
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
 {#Idea}

The Haag--Kastler axioms ([Haag-Kastler 64](#HaagKastler64)) (sometimes also called Araki--Haag--Kastler axioms) try to capture in a mathematically precise way the notion of [[quantum field theory]] (QFT), by axiomatizing how its algebras of [[quantum observables]] should depend on [[spacetime]] regions, namely as _[[local nets of observables]]_. 

The main point of these axioms is to say that

1. to every [[causally closed subset]] $\mathcal{O} \subset X$ of [[spacetime]] $X$ there is associated a [[C*-algebra]] $\mathcal{A}(\mathcal{O})$;

1. for every inclusion $\mathcal{O}_1 \hookrightarrow \mathcal{O}_2$ of such spacetime regions there is a corresponding inclusion $\mathcal{A}(\mathcal{O}_1) \hookrightarrow \mathcal{A}(\mathcal{O}_2)$

1. such that this respects [[composition]] of inclusions (hence such that $\mathcal{A}$ is a [[functor]] from the [[poset]] of [[causally closed subsets]] to [[C*-algebras]])

1. ([[causal locality]]) and such that whenever $\mathcal{O}_1, \mathcal{O}_2 \subset \mathcal{O} \subset X$ are [[spacelike]] separated, then the elements of the corresponding algebras of observables (graded-)commute with each other:

   $$
     [\mathcal{A}(\mathcal{O}_1), \mathcal{A}(\mathcal{O}_2)]
     = t
     0
     \phantom{AAAA}
     \in \mathcal{A}(\mathcal{O})
     \,.
   $$

Moreover one wants these assignments to behave well with spacetime symmetry.

The formulation of [[quantum field theory]] via these axioms has come to be known as _[[algebraic quantum field theory]]_ or _[[AQFT]]_, for short. There are various further axioms in the list such as the [[time slice axiom]]. 
The precise details of the list of axioms is in flux as the theory develops.


The Haag-Kastler axioms in their original form aim for the description of [[non-perturbative quantum field theory]] on [[Minkowski spacetime]]. They could be used to give rigorous [[proof]] of structural statements of [[QFT]] such as the [[spin-statistics theorem]] or the [[PCT theorem]], but examples of interacting field theories in dimensions $\geq 4$ are missing.

There are however variants:

* In [[perturbative AQFT]] one drops the requirement of [[C*-algebras]] and instead considers just [[formal power series algebras]] (in [[Planck's constant]] $\hbar$) in order to describe [[perturbative quantum field theory]] and connect to the traditional construction of pQFTs via the [[Feynman perturbation series]].

The observation that [[causal perturbation theory]] yields [[quantum observables]] that satisfy the Haag-Kastler axioms, except that [[C*-algebras]] are replaced by [[formal power series algebras]], is due to ([Il'in-Slavnov 78](#IlinSlavnov78), [Brunetti-Fredenhagen 00](#BrunettiFredenhagen00), [Brunetti-D&#252;tsch-Fredenhagen 09](#BrunettiDuetschFredenhagen09)). See at _[S-Matrix -- Causal Locality and Quantum Observables](S-matrix#CausalLocality)_.

* In [[locally covariant perturbative AQFT]] one generalizes from [[Minkowski spacetime]] to more general [[globally hyperbolic spacetimes]] in order to describe [[QFT on curved spacetimes]].

* In [[homotopical AQFT]] one consider [[homotopical algebras]] and commutativity only up to [[coherence law|coherent]] [[homotopy]] in order to discuss [[gauge theory]] with non-trivial topological ([[instanton]]) sectors.

### Terminology
 {#Terminology}

The approch to quantum field theory based on these axioms is often called _[[AQFT]]_ : either for **axiomatic quantum field theory** (since it was among the first attempts to put the edifice of QFT on solid [[axiom]]atic grounds) or **algebraic quantum field theory** (since it amplifies the algebras of local [[observable]]s over the spaces of [[state]]s). Neither of these terms is very descriptive. First there is  another, dual, axiomatization which does axiomatize the propagation of [[states]] -- see _[[FQFT]]_ -- which, second, is also "algebraic" in some sense, even though algebras of observables to not appear directly.

Another common term for these axioms is **local quantum field theory** (see the title of the standard textbook ([Haag](#Haag))) since, as becomes clear [below](#Formulation), they are focused on encoding the locality properties of QFT in terms of the algebras of observables. However, also the core aspect of _[[extended topological quantum field theory|extended]]_ [[FQFT]] is all about the notion of locality  of QFT. 

Therefore neither of the traditional terms for QFT as axiomatized by Haag-Kastler is truly descriptive in that it genuinely distinguishes from the other, the Atiyah-Segal axiomatization by [[FQFT]]. What does distinguish the two approaches  may be characterized in traditional terminology of quantum theory as follows ([Schreiber](#Schreiber), [SatiSchreiber](#SatiSchreiber)): 

* [[FQFT]] axiomatizes the _[[Schrödinger picture]]_ of QFT, which encodes the propagation of [[state]]s through spacetimes;

* [[AQFT]] axiomatizes the _[[Heisenberg picture]]_ of QFT, which encodes the way that [[observable]]s depend on spacetime.


### Motivation
 {#Motivation}

A central difference between the Haag-Kastler axioms and traditionally more widespread formulations of QFT (usually far from being formalized in any way) is the emphasis of the [[algebra of observables]]  of a QFT (Heisenberg picture) and the de-emphasis of the ([[Hilbert space|Hilbert]]) [[spaces of states]] ([[Schrödinger picture]]). This emphasis receives motivation from the the fact that many technical problems of QFT simply disappear when one is not trying to form its spaces of states, while at the same time no real information about the theory is lost.

Examples of technical problems that formulation in terms of spaces of states bring with them are the following:

* In [[quantum field theory]] as opposed to [[quantum mechanics]], the [[Stone-von Neumann theorem]] fails, making the [[unitary representation]] of the [[Heisenberg group]] on the spaces of states non-unique, hence requiring an explicit choice of representation. There is no generally good theory available for how to make this choice.

* More seriously, [[Haag's theorem]] says that at a crucial step in [[perturbation theory]] where one wants to pass from the representation "free fields" to that of "interacting fields", the two representations are necessarily inequivalent, contrary to what is (silently or explicitly) assumed in much traditional QFT literature (see [EarmanFraser](#EarmanFraser)).

* In the [[renormalization]] or [[perturbation theory]] the formulation in terms of states brings with it _infrared problems_ that are simply absent when formulating renormalization just in terms of observables ([DuetschFredenhagen](#DuetschFredenhagen)).

## Formulation
 {#Formulation}

We formulate the ideas of the core axioms of Haag-Kastler, and their intended physical meaning. For more details see [[local net of observables]].

1. **spacetime locality** 

   Since the _fields_ in [[quantum field theory]] (such as the [[electromagnetic field]]) exhibit and are characterized by
their _local excitations_ (for instance the value of the electric/magnetic [[field strength]] at any point) having effects only locally (the field excitations at two points a finite distance apart do not directly influence each other) the fields over any region of [[spacetime]] form a [[subsystem]] of the fields of any larger region and
in particular of the total system.

   If "[[quantum mechanical system]]" is formalized as "[[C-star algebra]]" (of [[observables]]) then "[[subsystem]]" translates to "sub-$C^*$-algebra". Therefore the above sentence translates into: quantum fields form a [[copresheaf]] of [[C-star algebras]] on [[spacetimes]] whose co-restriction morphisms are [[monomorphism]]s. 

   In [[AQFT]] such is called an **[[local net|isotonic net of algebras]]** .

   There are different approaches to define what kind of spacetime regions the algebras of observables are assigned to, hence different approaches as to what exactly the [[site]] is on which the co-presheaf is defined. A common approach is to take all [[bounded space|bounded]] [[open subspace|open]] subsets of [[Minkowski space|Minkowski]] [[spacetime]]. For more general setups see [[AQFT on curved spacetimes]].

1. **causal locality**

   If two regions of [[spacetime]] are [[spacelike]] separated, then there can be no influence between them whatsoever. Not only do the field excitations in one of the two regions not _directly_ influence those in the other region (as per item 1), but they do not even influence _indirectly_ : no [[waves]] of excitations (for instance [[electromagnetic waves]]: [[light]]) can run from one region to a spacelike separated region. Therefore the two [[subsystems]] constituted by these two regions accordording to the first point are even _[[independent subsystems]]_ . This is called _[[causal locality]]_.

   The formalization of "two [[independent subsystems]]" in [[quantum mechanics]] is: two subalgebras that _commute_ with each other inside the larger [[C-star algebra]]. (And usually one adds: and such that the algebra they generate in the larger algebra is [[isomorphic]] to their [[tensor product]].)

   Therefore this translates into the axiom: quantum fields on a
spacetime form an isotonic copresheaf of algebras such that the
algebras assigned to any two spacelike separated regions commute with
each other inside the algebra assigned to any larger region containing
these two regions.


1. **spacetime covariance**

   The geometric symmetry operations map the algebra of a region onto the algebra of the transformed region.

   (this is not an extra axiom if one defines the [[site]] of spacetime regions general enough...)

   In Minkowski spacetime the geometric symmetry group is usually taken to be the [[Poincaré group]], but note that some authors consider subgroups of the full Poincar&#233; group, like the subgroup of translations (Borchers: "Translation group and particle representations in quantum field theory").

1. **positivity of energy**

   An axiom is needed to ensure that only nonnegative energies occur -- one possibility is the "spectrum condition", which says that the spectrum (to be more precise: the support of the [[spectral measure]]) of the operator associated with a translation is contained in the closed forward light cone, for all translations. 

## Properties

### Structural theorems

It is possible to prove both a [[spin-statistics theorem]] and a [[PCT theorem]] in the Haag-Kastler approach. The mathematically precise, model independent statements and their proofs are considered to be a major breakthrough of the theory.


### Relation to Wightman axioms

Unlike the [[Wightman axioms]], the Haag--Kastler axioms do not need the notion of "[[physical field|field]]": the fields in the Wightman axioms are -- from the Haag--Kastler point of view -- only necessary to describe how the algebras of observables are constructed; any way to consistently construct the net of algebras would suffice.


## Related concepts

* [[quantum field theory]]

  * [[AQFT]]

    * **Haag-Kastler axioms**

    * [[local net of observables]], [[conformal net]]

    * [[causal perturbation theory]]

    * [[locally covariant perturbative AQFT]]

    * [[scattering amplitude]]

    * [[modular theory]]

  * [[FQFT]]

## References 

The original article that introduced these axioms is

* {#Haag64} [[Rudolf Haag]], [[Daniel Kastler]], _An algebraic approach to quantum field theory_, Journal of Mathematical Physics, Bd.5, 1964, S.848-861 ([doi:10.1063/1.1704187](https://doi.org/10.1063/1.1704187), [spire:9124](https://inspirehep.net/literature/9124))

following

* {#Haag59} [[Rudolf Haag]], _Discussion des "axiomes" et des propri&#233;t&#233;s asymptotiques d&#8217;une th&#233;orie des champs locales avec particules compos&#233;es, Les Probl&#232;mes Math&#233;matiques de la Th&#233;orie Quantique des Champs_, Colloque Internationaux du CNRS LXXV (Lille 1957), CNRS Paris (1959), 151.

translated to English as: 

* [[Rudolf Haag]], *Discussion of the ‘axioms’ and the asymptotic properties of a local field theory with composite particles*, EPJ H 35, 243–253 (2010) ([doi:10.1140/epjh/e2010-10041-3](https://doi.org/10.1140/epjh/e2010-10041-3))


Textbook accounts include

* {#Haag} [[Rudolf Haag]], _[[Local Quantum Physics -- Fields, Particles, Algebras]]_ Springer (1992) 2nd., rev. and enlarged ed. Springer (1996) ([ISBN 978-3-642-61458-3] (https://www.springer.com/gp/book/9783540610496))


* [[Huzihiro Araki]]: _[[Mathematical Theory of Quantum Fields]]_ Oxford University Press 1999 [ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0998.81501&format=complete). 

precursors include

* Bogolyubov, Logunov, Oksak, Todorov: _General principles of quantum field theory._ ([ZMATH entry] (http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0732.46040&format=complete))

An online reference page is here:

* Stephen J. Summers: [AQFT online] (http://www.math.ufl.edu/~sjs/aqft.html)

See also the references at _[[AQFT]]_ and at _[[perturbative AQFT]]_. 

One of the founding fathers of [[perturbative quantum field theory]] wrote:

* {#Dyson72} [[Freeman Dyson]] _Missed opportunities_, Bulletin of the AMS, Volume 78, Number 5, September 1972 ([pdf](https://www.math.uh.edu/~tomforde/Articles/Missed-Opportunities-Dyson.pdf))

  > These  axioms,  taken  together  with  the  axioms  defining  a  C*-algebra  are  a  distillation  into  abstract  mathematical  language  of  all  the   general  truths  that  we  have  learned  about  the  physics  of  microscopic   systems  during  the  last  50 years. They  describe a  mathematical  structure of  great  elegance  whose  properties  correspond  in  many  respects  to  the facts  of  experimental  physics.  In  some  sense,  the  axioms  represent  the most  serious  attempt  that  has  yet  been  made  to  define  precisely  what physicists mean by the words "observability, causality, locality, relativistic invariance," which  they are constantly  using  or  abusing  in their  everyday speech. $[$...$]$ I  therefore  propose  as  an  outstanding  opportunity  still  open  to  the  pure mathematicians, to  create a mathematical structure preserving the  main   features  of  the  Haag-Kastler axioms but possessing E-invariance instead of P-invariance. 

  (on the latter see _[[AQFT on curved spacetimes]]_)

The observation that [[causal perturbation theory]] yields [[quantum observables]] that satisfy the Haag-Kastler axioms, except that [[C*-algebras]] are replaced by [[formal power series algebras]] is due to


* {#IlinSlavnov78} V. A. Il'in and D. S. Slavnov, _Observable algebras in the S-matrix approach_, Theor. Math. Phys. 36 (1978) 32. ([spire](http://inspirehep.net/record/135575), [doi](http://dx.doi.org/10.1007/BF01035870))

* {#BrunettiFredenhagen00} [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_, Commun. Math. Phys. 208 : 623-661, 2000 ([math-ph/9903028](https://arxiv.org/abs/math-ph/9903028))

* {#BrunettiDuetschFredenhagen09} [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](http://arxiv.org/abs/0901.2038))




An introduction into Tomita-Takesaki modular theory is here:

* Stephen J. Summers: "Tomita-Takesaki Modular Theory" ([arXiv] (http://xxx.uni-augsburg.de/abs/math-ph/0511034))

...while a paper that puts it to serious work is this:

* H.J. Borchers: "On Revolutionizing of Quantum Field Theory
with Tomita's Modular Theory", ([ESI preprint page] (http://www.esi.ac.at/preprints/ESI-Preprints.html))

A discussion of how the Haag-Kastler axioms (those concerning locality) follow from an extended [[FQFT]] with Lorentzian structure is in 

* {#Schreiber} [[Urs Schreiber]], _AQFT from $n$-functorial QFT_ , Comm. Math. Phys., Volume 291, Issue 2, pp.357-401 ([pdf](http://ncatlab.org/schreiber/files/AQFTfromFQFT.pdf))
 

A discussion putting the state of the art of the [[AQFT]]-axiomatization in context with that of the [[FQFT]]-axiomatization is in 

* {#SatiSchreiber} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Mathematical Foundations of Quantum Field and String Theory]]_
 

A discussion of [[perturbation theory]] and [[renormalization]] in terms of the Haag-Kastler axioms is in 

* {#DuetschFredenhagen} [[Michael Dütsch]], [[Klaus Fredenhagen]], _A local (perturbative)_ construction of observables in gauge theores: the example of qed_ , Commun. Math. Phys. 203 (1999), no.1, 71-105,  ([arXiv:hep-th/9807078](http://xxx.uni-augsburg.de/ps/hep-th/9807078)). 
 
[[Haag's theorem]] and its meaning and implication is discussed thoroughly in 

* {#EarmanFraser} John Earman, Doreer Fraser, _Haag's theorem and its implications for the foundations of quantum field theory_ ([pdf](http://philsci-archive.pitt.edu/2673/1/earmanfraserfinalrevd.pdf))
 



[[!redirects Haag-Kastler approach]]
[[!redirects Haag–Kastler approach]]
[[!redirects Haag--Kastler approach]]

[[!redirects Haag-Kastler axiom]]
[[!redirects Haag-Kastler axioms]]
[[!redirects Haag–Kastler axiom]]
[[!redirects Haag–Kastler axioms]]
[[!redirects Haag--Kastler axiom]]
[[!redirects Haag--Kastler axioms]]
[[!redirects Araki-Haag-Kastler axiom]]
[[!redirects Araki-Haag-Kastler axioms]]
[[!redirects Araki–Haag–Kastler axiom]]
[[!redirects Araki–Haag–Kastler axioms]]
[[!redirects Araki--Haag--Kastler axiom]]
[[!redirects Araki--Haag--Kastler axioms]]

[[!redirects Haag-Kastler net]]
[[!redirects Haag-Kastler nets]]
[[!redirects Haag–Kastler net]]
[[!redirects Haag–Kastler nets]]
[[!redirects Haag--Kastler net]]
[[!redirects Haag--Kastler nets]]
