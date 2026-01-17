
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Modal type theory_ is a flavor of [[type theory]] with [[type formation rules]] for [[modalities]], hence [[type theory]] which on [[propositions]] reduces to [[modal logic]]. 

Following ([Moggi91](#Moggi91), [Benton, Bierman & de Paiva 1998](#BentonBiermanPaiva98); [Bierman & de Paiva 1996](#BiermanDePaiva96), [2000](#BiermanDePaiva96); [Kobayashi 1997](#Kobayashi97)) modal type theory  is specifically understood as being a type theory equipped with  ([[comonad|co-]])[[monads]] on its type system, representing the intended [[modal operators]]. Since [[monad (in computer science)|monads in computer science]] embody a notion of [[computation]], some authors also speak of _[[computational type theory]]_ here ([Benton, Bierman & de Paiva 1998](#BentonBiermanPaiva98), [Fairtlough-Mendler 02](#FairtloughMendler02)).

According to ([Benton, Bierman & de Paiva 1998, p. 1-2](#BentonBiermanPaiva98)) this matches well with the default interpretation of ([[S4]]) [[modal logic]] as being about the [[modality]] $T$ of "[[possibility]]":

> The starting point for Moggi's work is an explicit semantic distinction between _computations_ and _values_. If $A$ is an object which interprets the values of a particular type, then $T(A)$ is the object which models computation of that type $A$. $[...]$ For a wide variety of notions of computation, the unary operator $T(-)$ turns out to have the categorical structure of a _strong monad_ on an underlying cartesian closed category of values. $[...]$ On a purely intuitive level and particularly if one thinks about non-termination, there is certainly something appealing about the idea that a computation of type $A$ represents the possibility of a value of type $A$.


When the underlying type theory is [[homotopy type theory]] these modalities are a "higher" generalization of traditional modalities, with "higher" in the sense of [[higher category theory]]: they have [[categorical semantics]] in [[(∞,1)-categories]] given by [[(∞,1)-monads]]. See ([Shulman 12](#Shulman),  [Rijke, Shulman, Spitters](#RSS) ) for definition of such _higher modalities_, and see at _[[reflective subuniverse]]_.


## Properties

### Relation to monads
 {#RelationToMonads}

At least in many cases, modalities in type theory are identified with [[monads (in computer science)|monads]] or comonads on the underlying [[type]] [[universe]], or on the subuniverse of [[propositions]].

See for instance ([Benton, Bierman & de Paiva 1998, section 3.2](#BentonBiermanPaiva98)), ([Kobayashi](#Kobayashi)), ([Gabbay-Nanevski, section 8](#GabbayNanevski)), ([Gaubault-Larrecq, Goubault, section 5.1](#Gaubault-LarrecqGoubault)), ([Park-Harper, section 2.6](#ParkHarper)), ([Shulman](#Shulman)) as examples of the first, and ([Moggi, def. 4.7](#Moggi)), ([Awodey-Birkedal, section 4.2](#AwodeyBirkedal)) as examples of the second.

### Relation to endo-adjunctions
An endo-adjunction on a [[lex category]] gives rise to a modal type theory satisfying the modal axiom K; see [dependent right adjoint](#dradjoint). This also gives rise to a sound sound and complete interpretation of Fitch-style modal $\lambda$-calculus.

## Examples

### Geometric modality -- Grothendieck topology
 {#GeometricModality}

As a special case of the [modalities-are-monads](#RelationToMonads) relation,
a [[Grothendieck topology]] on the [[site]] underlying a [[presheaf topos]] is equivalently encoded in the [[sheafification]] [[monad]] $PSh(C) \to Sh(C) \hookrightarrow PSh(C)$ induced by the [[sheaf topos]] [[geometric embedding]].  More generally, any geometric subtopos is equivalently represented by a left-exact idempotent monad.

When restricted to act on [[truncated object|(-1)-truncated objects]] (i.e. [[subterminal objects]] or more generally [[monomorphisms]]), this becomes a [[universal closure operator]].  When internalized as an operation on the [[subobject classifier]], this becomes the corresponding [[Lawvere-Tierney operator]]. This modal perspective on sheafification was maybe first made explicit by [[Bill Lawvere]]:

> A Grothendieck 'topology' appears most naturally as a modal operator of the nature 'it is locally the case that' ([Lawvere](#Lawvere)).

Here, "It is locally the case that [X is [[metric space#metrizable_spaces|metrizable]]/Euclidean/etc]," corresponds to, "X is locally metrizable/Euclidean/etc," in the usual parlance.

More discussion is in ([Goldblatt](#Goldblatt)), where this kind of modality is called a _geometric modality_.

For [[higher toposes]], it is no longer true in general that a subtopos is determined by its behavior on the $(-1)$-truncated objects, but we can still regard the entire sheafification monad as a [[higher modality]] in the internal [[homotopy type theory]].

### Closure modality

The canonical monad on a [[local topos]] gives rise to a closure modality on propositions in its internal language, as described in ([Awodey-Birkedal](#AwodeyBirkedal)).

### Necessity and possibility

See at _[[necessity and possibility]]_ the section _[Possible worlds via dependent type theory](https://ncatlab.org/nlab/show/necessity+and+possibility#InFirstOrderLogicAndTypeTheory)_

### Cohesive and differential modality

By adding to [[homotopy type theory]] three (higher) modalities that encode [[discrete object|discrete types]] and [[codiscrete object|codiscrete types]] and hence implicitly a non-(co)-discrete notion of [[cohesion]] one obtained _[[cohesive homotopy type theory]]_. Adding furthermore modalities for _infinitesimal_ (co)discreteness yields [[differential homotopy type theory]].

## Related concepts

* [[closure operator]]

* [[idempotent monad]], [[idempotent (∞,1)-monad]]

* [[modal type]], [[anti-modal type]]

* [[modal homotopy type theory]]

* [[adjoint logic]]

* [[reflective subuniverse]]

* [[geometric type theory]]




## References
 {#References}

The clear identification of [[modal operators]] on types with [[monads]] (see at _[[monad (in computer science)]]_) is due to 

* {#Moggi91} [[Eugenio Moggi]], _Notions of computation and monads. Information and Computation_, 93(1), 1991. ([pdf](http://www.disi.unige.it/person/MoggiE/ftp/ic91.pdf))
 

This was observed (independently) to systematically yield constructive [[modal logic]] in (see also at [[computational type theory]])

* {#BentonBiermanPaiva98} [[Nick Benton]], [[Gavin Bierman]], [[Valeria de Paiva]], *Computational Types from a Logical Perspective*, Journal of Functional Programming **8** 2  (1998) 177-193 &lbrack;[doi:10.1017/S0956796898002998](https://doi.org/10.1017/S0956796898002998), [web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.36.5778)&rbrack;

* {#BiermanDePaiva96} [[Gavin M. Bierman]], [[Valeria de Paiva]], *Intuitionistic necessity revisited*, School of Computer Science research reports-University of Birmingham CSR (1996) &lbrack;[researchgate](https://www.researchgate.net/publication/2810611_Intuitionistic_Necessity_Revisited), [[Bierman-dePaiva-NecessityRevisited.pdf:file]]&rbrack;

* {#BiermanDePaiva00} [[Gavin M. Bierman]], [[Valeria de Paiva]], *On an Intuitionistic Modal Logic*, Studia Logica **65** (2000) 383–416 &lbrack;[doi:10.1023/A:1005291931660](https://doi.org/10.1023/A:1005291931660), [pdf] (https://www.researchgate.net/profile/Valeria-De-Paiva/publication/226515897_On_An_Intuitionistic_Modal_Logic/links/00b4951ed416906ccc000000/On-An-Intuitionistic-Modal-Logic.pdf)&rbrack;

* {#Kobayashi97} [[Satoshi Kobayashi]], *Monad as modality*, Theoretical Computer Science **175** 1 (1997) 29-74 &lbrack;<a href="https://doi.org/10.1016/S0304-3975(96)00169-7">doi:10.1016/S0304-3975(96)00169-7</a>&rbrack;
 
* {#FairloughMendler} M. Fairlough, Michael Mendler, _Propositional lax logic_, Information and computation 137(1):1-33 (1997) &lbrack;[pdf](https://www.uni-bamberg.de/fileadmin/uni/fakultaeten/wiai_professuren/grundlagen_informatik/papersMM/pll.pdf)&rbrack;
 
* [[Steve Awodey]], p. 279 in: *Category theory*, Oxford University Press (2006, 2010) &lbrack;[doi:10.1093/acprof:oso/9780198568612.001.0001](https://doi.org/10.1093/acprof:oso/9780198568612.001.0001), [ISBN:9780199237180](https://global.oup.com/ukhe/product/category-theory-9780199237180), [pdf](http://englishonlineclub.com/pdf/Category%20Teory%20%5BEnglishOnlineClub.com%5D.pdf)&rbrack;


See also the type-theoretic generalization of _[[adjoint logic]]_, as discussed in

* {#LicataShulman} [[Dan Licata]], [[Mike Shulman]], _Adjoint logic with a 2-category of modes_, in _[Logical Foundations of Computer Science 2016](http://lfcs.info/lfcs-2016/)_ ([pdf](http://dlicata.web.wesleyan.edu/pubs/ls15adjoint/ls15adjoint.pdf), [slides](http://dlicata.web.wesleyan.edu/pubs/ls15adjoint/ls15adjoint-lfcs-slides.pdf))

The modal systems "CL" and "PLL" in ([Benton, Bierman & de Paiva 1998](#BentonBiermanPaiva)) and ([Fairlough-Mendler](#FairloughMendler)), respectively,  turn out to be equivalent to the geometric modality of [Goldblatt](#Goldblatt). The system CS4 in ([Kobayashi 1997](#Kobayashi97)) yields a constructive version of [[S4 modal logic]].


Explicit mentioning of type theory equipped with such a monad as _modal type theory_ or [[computational type theory]] is in

* {#FairtloughMendler02} Matt Fairtlough, Michael Mendler, _On the Logical Content of Computational Type Theory: A Solution to Curry's Problem_, Types for Proofs and Programs Lecture Notes in Computer Science Volume 2277, 2002, pp 63-78
 

Discussion of modal operators explicitly in [[dependent type theory]] (and with a brief mentioning of the relation to [[monad (in computer science)|monads]]) is in 

* {#NanevskiPfenningPientka05} [[Aleksandar Nanevski]], [[Frank Pfenning]], Brigitte Pientka, _Contextual Modal Type Theory_ (2005) &lbrack;[web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.61.2356), [slides](http://wips.cs.umn.edu/slides/pientka.pdf)&rbrack;

* [[Valeria de Paiva]], Eike Ritter, _Fibrational Modal Type Theory_, Electronic Notes in Theoretical Computer Science Volume 323, 11 July 2016, Proceedings of the Tenth Workshop on Logical and Semantic Frameworks, with Applications (LSFA 2015), pp. 143&#8211;161 ([doi:10.1016/j.entcs.2016.06.010](http://www.sciencedirect.com/science/article/pii/S1571066116300378))

* Daniel Gratzer, [[Jonathan Sterling]], [[Lars Birkedal]], _Implementing Modal Dependent Type Theory_, ([pdf](https://jozefg.github.io/papers/2019-implementing-modal-dependent-type-theory.pdf), [GitHub](https://github.com/jozefg/blott))

* Daniel Gratzer, _Implementing Modal Dependent Type Theory_, talk at [ICFP 19](https://icfp19.sigplan.org/) ([slides pdf](https://jozefg.github.io/papers/2019-icfp-modal-slides.pdf))

* [[Daniel Gratzer]], [[G. Alex Kavvos]], [[Andreas Nuyts]], [[Lars Birkedal]]: _Multimodal Dependent Type Theory_, Logical Methods in Computer Science **17** 3 (2021) lmcs:7713 &lbrack;[arXiv:2011.15021](https://arxiv.org/abs/2011.15021), <a href="https://doi.org/10.46298/lmcs-17(3:11)2021">doi:10.46298/lmcs-17(3:11)2021</a>&rbrack;

* [[Mike Shulman]], _Semantics of multimodal adjoint type theory_ ([arXiv:2303.02572](https://arxiv.org/abs/2303.02572)) 

* [[Daniel Gratzer]], *Syntax and semantics of modal type theory*, PhD Aarhus (2023) &lbrack;[pdf](https://jozefg.github.io/papers/phd-thesis.pdf)&rbrack;

A survey of the field of modal type theory is in the collections

* M. Fairtlough, M. Mendler, [[Eugenio Moggi]] (eds.), _Modalities in Type Theory_, Mathematical Structures in Computer Science, Vol. 11, No. 4, (2001)

* {#PaivaGoreMendler} [[Valeria de Paiva]], Rajeev Gor&#233;, Michael Mendler, _Modalities in constructive logics and type theories_, Special issue of the Journal of Logic and Computation, editorial pp. 439-446, Vol. 14, No. 4, Oxford University Press, (2004) ([pdf](http://www.cs.bham.ac.uk/~vdp/publications/final-preface.pdf))
 
* [[Valeria de Paiva]], Brigitte Pientka (eds.) _Intuitionistic Modal Logic and Applications (IMLA 2008)_, . Inf. Comput. 209(12): 1435-1436 (2011) ([web](http://www.sciencedirect.com/science/article/pii/S089054011100143X))


The historically first modal type theory, the interpretation of [[sheafification]] as a modality in the internal language of a [[Grothendieck]] topos goes back to the notion of [[Lawvere-Tierney operator]] 

* {#Lawvere} [[Bill Lawvere]], _Quantifiers and sheaves_, Actes, Congr&#232;s intern, math., 1970. Tome 1, p. 329 &#224; 334 ([pdf](https://pdfs.semanticscholar.org/6630/846a00261a071b71e264e0f532e29cd9152f.pdf))
 

reviewed in

* {#Goldblatt} [[Robert Goldblatt]], _Grothendieck topology as geometric modality_, Mathematical Logic Quarterly, Volume 27, Issue 31-35, pages 495&#8211;529, (1981)
 
Modal type theory with an eye towards [[homotopy type theory]] is discussed in 

* [[UF-IAS-2012]], _[Modal type theory](http://uf-ias-2012.wikispaces.com/Modal+type+theory)_

Formalization of modalities in [[homotopy type theory]] ([[modal homotopy type theory]]) is discussed in

* {#Shulman} [[Mike Shulman]], _Higher modalities_, talk at [[UF-IAS-2012]], October 2012  ([pdf](http://uf-ias-2012.wikispaces.com/file/view/modalitt.pdf))

* {#RSS} [[Egbert Rijke]], [[Mike Shulman]], [[Bas Spitters]], *Modalities in homotopy type theory*,  Logical Methods in Computer Science, **16** 1 (2020) &lbrack;[arXiv:1706.07526](https://arxiv.org/abs/1706.07526), [episciences:6015](https://lmcs.episciences.org/6015), <a href="https://doi.org/10.23638/LMCS-16(1:2)2020">doi:10.23638/LMCS-16(1:2)2020</a>&rbrack;

* [[Mike Shulman]], _[http://homotopytypetheory.org/2015/07/05/modules-for-modalities/](http://homotopytypetheory.org/2015/07/05/modules-for-modalities/)_  (2015)

* [[Egbert Rijke]], [[Bas Spitters]], around def. 1.11 of _Sets in homotopy type theory_ ([arXiv:1305.3835](http://arxiv.org/abs/1305.3835))

* Kevin Quirin and Nicolas Tabareau, _Lawvere-Tierney Sheafification in Homotopy Type Theory_, [Workshop](http://hott-uf.gforge.inria.fr/2015/) talk 2015 ([pdf](http://hott-uf.gforge.inria.fr/2015/HOTTUF_Kevin.pdf)), Kevin Quirin [thesis](https://kevinquirin.github.io/thesis/main.pdf)

and specifically in [[cohesive homotopy type theory]] in 

* [[Urs Schreiber]], [[Michael Shulman]], _[[schreiber:Quantum gauge field theory in Cohesive homotopy type theory]]_, in [[Ross Duncan]], [[Prakash Panangaden]] (eds.) _Proceedings 9th Workshop on Quantum Physics and Logic_, Brussels, Belgium, 10-12 October 2012 ([arXiv:1408.0054](http://arxiv.org/abs/1408.0054))

* {#Shulman15} [[Mike Shulman]], _Brouwer's fixed-point theorem in real-cohesive homotopy type theory_, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Wellen18} [[Felix Wellen]], _[[schreiber:thesis Wellen|Cartan Geometry in Modal Homotopy Type Theory]]_ ([arXiv:1806.05966](https://arxiv.org/abs/1806.05966), [thesis pdf](http://www.math.kit.edu/iag3/~wellen/media/diss.pdf))

* [[David Jaz Myers]], _Good Fibrations through the Modal Prism_ ([arXiv:1908.08034v2](https://arxiv.org/abs/1908.08034v2))

A monograph aimed at [[philosophy|philosophers]] is in

* {#Corfield20} [[David Corfield]], _Modal homotopy type theory_, Oxford University Press 2020 ([ISBN: 9780198853404](https://global.oup.com/academic/product/modal-homotopy-type-theory-9780198853404))

following

* [[David Corfield]], _Modal homotopy type theory_, 2017 ([PhilSci archive:15260](http://philsci-archive.pitt.edu/15260/))



Monadic modal type theory with [[idempotent monads]]/monadic reflection is discussed in

* [[Andrzej Filinski]], _Representing Layered Monads_, POPL 1999. ([pdf](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.46.2016))
    
* [[Andrzej Filinski]], _On the Relations between Monadic Semantics_, TCS 375:1-3, 2007. ([pdf](http://www.itu.dk/people/birkedal/teaching/advanced-semantics-Spring-2007/OtRbMS.pdf))

* [[Andrzej Filinski]], _Monads in Action_, POPL 2010. ([pdf](http://hjemmesider.diku.dk/~andrzej/papers/popl10-mia.pdf))

* Oleg Kiselyov and Chung-chieh Shan, _Embedded Probabilistic Programming. Working conference on domain-specific languages_, (2009) ([pdf](https://link.springer.com/content/pdf/10.1007/978-3-642-03034-5_17.pdf))

A general framework is discussed in

* {#LicataShulman16} [[Dan Licata]], [[Mike Shulman]], _Adjoint logic with a 2-category of modes_, in _[Logical Foundations of Computer Science 2016](http://lfcs.info/lfcs-2016/)_ ([pdf](http://dlicata.web.wesleyan.edu/pubs/ls15adjoint/ls15adjoint.pdf), [slides](http://dlicata.web.wesleyan.edu/pubs/ls15adjoint/ls15adjoint-lfcs-slides.pdf))

  (for [[modal type theory|modal]] [[unary type theory]])

* {#LicataShulman17} [[Daniel Licata]], [[Mike Shulman]], and [[Mitchell Riley]], _A Fibrational Framework for Substructural and Modal Logics (extended version)_, in Proceedings of 2nd International Conference on Formal Structures for Computation and Deduction (FSCD 2017) ([doi: 10.4230/LIPIcs.FSCD.2017.25](http://drops.dagstuhl.de/opus/volltexte/2017/7740/), [pdf](http://dlicata.web.wesleyan.edu/pubs/lsr17multi/lsr17multi-ex.pdf))

  (for [[modal type theory|modal]] [[simple type theory]])

{#ReferencesReview} Review includes

* {#LicataWellen18} [[Dan Licata]], [[Felix Wellen]], _Synthetic Mathematics in Modal Dependent Type Theories_, tutorial at _[Types, Homotopy Theory and Verification](https://www.him.uni-bonn.de/programs/current-trimester-program/types-sets-constructions/workshop-types-homotopy-type-theory-and-verification/)_, 2018

  Tutorial 1, Dan Licata:  _A Fibrational Framework for Modal Simple Type Theories_ ([recording](https://www.youtube.com/watch?v=uLLbSAYd3yI))

  Tutorial 2, Felix Wellen: _The Shape Modality in Real cohesive HoTT and Covering Spaces_ ([recording](https://www.youtube.com/watch?v=ACGjJDarEc4))

  Tutorial 3, Dan Licata: _Discrete and Codiscrete Modalities in Cohesive HoTT_ ([recording](https://www.youtube.com/watch?v=OHN9vEVPBN8))

  Tutorial 4, Felix Wellen, _Discrete and Codiscrete Modalities in Cohesive HoTT, II_ ([recording](https://www.youtube.com/watch?v=KXx9UDQdWPw))

  Tutorial 5, Dan Licata: _A Fibrational Framework for Modal Dependent Type Theories_ ([recording](https://www.youtube.com/watch?v=R4SsxUnIcng))

  Tutorial 6, Felix Wellen: _Differential Cohesive HoTT_, ([recording](https://www.youtube.com/watch?v=uEZXHPdwvJU&t=226s))


* {#Licata18} [[Dan Licata]], _Synthetic Mathematics in Modal Dependent Type Theories_, notes for tutorial at _[Types, Homotopy Theory and Verification](https://www.him.uni-bonn.de/programs/current-trimester-program/types-sets-constructions/workshop-types-homotopy-type-theory-and-verification/)_, 2018 ([pdf](http://dlicata.web.wesleyan.edu/pubs/lsr17multi/him-tutorial.pdf))

* {#Shulman19} [[Michael Shulman]], _Semantics of higher modalities_, talk at _[Geometry in Modal HoTT (2019)](https://felix-cherubini.de/modal-workshop.html)_ ([pdf slides](http://home.sandiego.edu/~shulman/papers/cmu2019b.pdf), [video recording](https://www.youtube.com/watch?v=Wcpi1vVMrCs))

* [[Felix Cherubini]], _Geometry in Modal HoTT_, talk at _[Geometry in Modal HoTT (2019)](https://felix-cherubini.de/modal-workshop.html)_ ([video recording](https://www.youtube.com/watch?v=oHc552-hzBY))

* [[Egbert Rijke]], _Reflective subuniverses and modalities_, talk at _[Geometry in Modal HoTT (2019)](https://felix-cherubini.de/modal-workshop.html)_ ([video recording](https://youtu.be/OQthe5HpiKM))

* [[Egbert Rijke]]: _Modal descent_, talk at _[Geometry in Modal HoTT (2019)](https://felix-cherubini.de/modal-workshop.html)_ ([video recording](https://youtu.be/InaRkqKdyp4))


See also

* [[Frank Pfenning]], _Towards modal type theory_ (2000) &lbrack;[pdf](http://www.cs.cmu.edu/~fp/talks/mantova00-talk.pdf)&rbrack;

* [[Frank Pfenning]], _Intensionality, Extensionality, and Proof Irrelevance in Modal Type Theory_, in: Symposium on Logic in Computer Science (2001) 221&-230 &lbrack;[web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.28.5884)&rbrack;


* Giuseppe Primiero, _A multi-modal dependent type theory_ ([pdf](http://logica.ugent.be/centrum/preprints/primiero_PSPL10.pdf))

* {#GabbayNanevski} Murdoch Gabbay, [[Aleksandar Nanevski]], _Denotation of contextual modal type theory (CMTT): syntax and metaprogramming_ ([pdf](http://www.gabbay.org.uk/papers/dencmt.pdf))
 
* G. A. Kavvos, _Modalities, Cohesion, and Information Flow_, ([arXiv:1809.07897](https://arxiv.org/abs/1809.07897))

* Y. Nishiwaki, Y. Kakutani, Y. Murase, _Modality via Iterated Enrichment_, MFPS 2018 ([pdf](https://www.mathstat.dal.ca/mfps2018/preproc/paper_15.pdf))

A modality in the [[internal language]] of a [[local topos]] is discussed in section 4.2 of 

* {#AwodeyBirkedal} [[Steve Awodey]], [[Lars Birkedal]], _Elementary axioms for local maps of toposes_, Journal of Pure and Applied Algebra, 177(3):215-230, (2003) ([ps](http://www.itu.dk/people/birkedal/papers/elealm.ps.gz), [[AwodeyBirkedalLocalTopos.pdf:file]] )
 

* {#Gaubault-LarrecqGoubault} Jean Goubault-Larrecq, &#201;ric Goubault, _On the geometry of intuitionistic S4 proofs_, Homology, homotopy and applications vol 5(2) (2003)
 
* {#ParkHarper} Sungwoo Park, [[Robert Harper]], _A modal language for Effects_ (2004) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.2.8252))
 

* {#LicataHarper} [[Dan Licata]], [[Robert Harper]], _A Monadic Formalization of ML5_ ([arXiv:1009.2793](http://arxiv.org/abs/1009.2793))
 
* {#dradjoint} Ranald Clouston, Bassel Mannaa, Rasmus Ejlers Møgelberg, Andrew M. Pitts, Bas Spitters, _Modal Dependent Type Theory and Dependent Right Adjoints_ [Arxiv](https://arxiv.org/abs/1804.05236), 2018

* [[Felix Cherubini]], [[Egbert Rijke]]: _Modal Descent_, Mathematical Structures in Computer Science **31** 4 (2021) 363-391 &lbrack;[arXiv:2003.09713](https://arxiv.org/abs/2003.09713), [doi:10.1017/S0960129520000201](https://doi.org/10.1017/S0960129520000201)&rbrack;


A list of related references is also kept at

* [[Valeria de Paiva]], _Intuitionistic Modal Logic Selected Publications_ ([web](https://docs.google.com/document/pub?id=1ASo__R-_Bzq9D9lGUo0xrfIxt_I9az7oqSg-wmP1K10))

[[!redirects modal type theory]]
[[!redirects modal type theories]]
[[!redirects modal dependent type theory]]
[[!redirects modal dependent type theories]]

[[!redirects multimodal type theory]]
[[!redirects multimodal type theories]]
[[!redirects multimodal dependent type theory]]
[[!redirects multimodal dependent type theories]]

[[!redirects geometric modality]]
[[!redirects geometric modalities]]

[[!redirects higher modality]]
[[!redirects higher modalities]]