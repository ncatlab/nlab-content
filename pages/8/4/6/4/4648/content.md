+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Langlands correspondence
+--{: .hide}
[[!include Langlands correspondence -- contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The [[conjecture|conjectural]] _geometric Langlands correspondence_ is meant to be an [[analogy|analog]] of the [[number theory|number theoretic]] [[Langlands correspondence]] under the [[function field analogy]], hence with [[number fields]] replaced by [[function fields]] and further replaced by [[rational functions]] on [[complex curves]].  The key to this analogy is the [[Weil uniformization theorem]] which expresses the [[moduli stack of G-principal bundles]] over an [[algebraic curve]] as a [[double coset space]] of various function rings (as discussed at _[Moduli of bundles over curves](moduli+space+of+bundles#OverCurvesAndTheLanglandsCorrespondence)_) of just the kind as they appear in the number-theoretic [[Langlands correspondence]] (for instance in the [[Artin reciprocity law]] and in the definition of [[automorphic representations]]).

[[!include Langlands analogies -- table]]

The original version of the conjectured statement of _geometric Langlands duality_ (going back to [Beilinson-Drinfeld 9x](#BeilinsonDrinfeld9x) and reviewed for instance in [Frenkel 05](#Frenkel05)) asserts that for $G$ a [[reductive group]] and for $\Sigma$ an [[algebraic curve]], then there is an [[equivalence of categories|equivalence]] of [[derived categories]] of, on the one hand, [[D-modules]] on the [[moduli stack of G-principal bundles]] on $\Sigma$, and, on the other hand, [[quasi-coherent sheaves]] on the  ${}^L G$-[[moduli stack of local systems]] on $\Sigma$:

$$
  \mathcal{O}Mod\big(Loc_{{}^L G}(\Sigma)\big)
    \stackrel{\simeq}{\longrightarrow}
  \mathcal{D} Mod\big( Bun_G(\Sigma)\big)
$$

for ${}^L G$ the [[Langlands dual group]]. Moreover, the conjecture asserts that there is canonical such an equivalence which is a [[non-abelian cohomology|non-abelian]] analogue of the [[Fourier-Mukai transform|Fourier-Mukai]] [[integral transform]] and takes [[skyscraper sheaves]] on the left ([[categorification|categorified]] [[Dirac distributions]]) to what are called "[[Hecke eigensheaves]]" on the right.
This equivalence is in turn supposed to be a certain limit of the more general [[quantum geometric Langlands correspondence]] that identifies [[twisted D-modules]] on both sides.

For the [[abelian group|abelian]] case that $G$ is a [[torus]] the above equivalence has indeed been proven, given by a [[Fourier-Mukai transform]]  ([Laumon 85](#Laumon85), [Laumon 96](#Laumon96), [Rothstein 96](#Rothstein96)), see also [below](#AbelianCase).

{#However} However, in general the above version of the conjecture is false. For instance it fails in the case $G = SL_2$ and $\Sigma= \mathbb{P}^1$ ([Lafforgue 09](#Lafforgue09)).

A refined formulation of the conjecture due to [Arinkin & Gaitsgory 12](#ArinkinGaitsgory12), meant to fix this failure, replaces plain quasicoherent sheaves with certain "nilpotent" [[ind-objects]] of quasicoherent sheaves and refines [[derived categories]] to [[stable (∞,1)-categories]], to make the conjecture read

$$
  \bigg(Ind
  \Big(
    \mathcal{O}Mod
    \big(
      Loc_{{}^L G}(\Sigma)
    \big)
  \Big)
  \bigg)_{Nilp_{Glob}}
    \overset{\simeq}{\longrightarrow}
  \mathcal{D} Mod\big( 
    Bun_G(\Sigma)
  \big)
  \,.
$$

([Arinkin & Gaitsgory 12, conjecture 0.1.6](#ArinkinGaitsgory12)).

This form is called the [[categorical geometric Langlands conjecture]]. A proof was given by [Gaitsgory et al. 2025](#GaitsgoryGLCWebpage).

Since [[D-modules]] on [[moduli stacks of G-principal bundles]] play a central role in [[gauge theory|gauge]] [[quantum field theory]] (in particular as [[Hitchin connections]] on bundles of [[conformal blocks]] of $G$-[[Chern-Simons theory]] [[holographic principle|holographically]] dual to the [[WZW model]] [[2d conformal field theory]]) and since the [[Langlands dual group]] also appears in [[electric-magnetic duality]], it has long been suggested ([Atiyah 77](S-duality#Atiyah77)) that geometric Langlands duality has a distinguished meaning also in [[mathematical physics]] in general and in [[string theory]] in particular. One proposal for a realization of the correspondence as an incarnation of [[mirror symmetry]]/[[S-duality]] is due to ([Kapustin & Witten 06](#KapustinWitten06)), which however has not been turned into [[theorems]] yet. Another proposal for realizing the [[local Langlands correspondence|local]] correspondence via another incarnation of [[mirror symmetry]] is due to [Gerasimov, Lebedev & Oblezin 09](#GerasimovLebedevOblezin09).

The geometric Langlands conjecture has been motivated from the [[number theory|number theoretic]] [[Langlands correspondence]] via the [[function field analogy]] and some educated guessing, but there is to date no formalization of this analogy that would allow to regard number-theoretic and the geometric correspondence as two special cases of one "global" [[arithmetic geometry]]/[[global analytic geometry]] statement. Cautioning remarks on the accuracy of the analogy and on the rigour of the mirror-symmetric proposals may be found in ([Langlands 14](#Langlands14)). Some discussion of how to possibly start to go about making the analogy more systematic are at _[[differential cohesion and idelic structure]]_.

[[!include function field analogy -- table]]


## Properties 
 {#Properties}


### Abelian case
 {#AbelianCase}

In the case where $G$ is the [[multiplicative group]], hence where all bundles in question are [[line bundles]], geometric Langlands duality is well understood and is in fact a slight variant of a [[Fourier-Mukai transform]] ([Frenkel 05, section 4.4, 4.5](#Frenkel05)).


### Relation to S-duality
 {#RelationToSDuality}

The [[Kapustin-Witten TQFT]] ([KapustinWitten 2007](#KapustinWitten06)) is supposed to exhibit geometric Langlands duality as a special case of [[S-duality]]. 

See also at _[KK-compactification -- Formalization](http://ncatlab.org/nlab/show/Kaluza-Klein+mechanism#Formalization)_

[[!include geometric Langlands QFT -- table]]


[[!include gauge theory from AdS-CFT -- table]]


### Relation to T-duality
 {#RelationToTDuality}

In some cases the passage between a Lie group and its [[Langlands dual group]] can be understood as a special case of [[T-duality]]. ([Daenzer-vanErp](#DaenzerErp))

## Related concepts

* [[geometric class field theory]]

* [[geometric Satake equivalence]]

* [[Hitchin fibration]]

* [[topologically twisted D=4 super Yang-Mills theory]]

[[duality in physics]], [[duality in string theory]]

* [[S-duality]]

  * [[electro-magnetic duality]]

    * [[Montonen-Olive duality]]

  * [[Seiberg duality]]

  * **geometric Langlands correspondence**

    * [[S-duality]], [[Kapustin-Witten TQFT]]

  * [[quantum geometric Langlands correspondence]]

## References

### Original
 {#ReferencesOriginal}

The conjecture goes back to 

* {#BeilinsonDrinfeld9x} [[Alexander Beilinson]], [[Vladimir Drinfeld]], section 5.2.7 of _Quantization of the Hitchin system and Hecke eigensheaves_, ([pdf](https://math.uchicago.edu/~drinfeld/langlands/QuantizationHitchin.pdf), [other pdf link](http://www.math.uchicago.edu/~mitya/langlands/hitchin/BD-hitchin.pdf))

based on

* {#Laumon87} [[Gérard Laumon]], sections 5.3 and 4.3.3. of _Correspondance de Langlands g&#233;om&#233;trique pour les corps de fonctions_, Duke Math. Jour., vol. 54 (1987), 309-359

Proof in the abelian case is due to

* {#Laumon85} [[Gérard Laumon]], _Transformation de Fourier g&#233;om&#233;trique_ Preprint IHES/85/M/52 (1985)

* {#Laumon96} [[Gérard Laumon]], _Transformation de Fourier g&#233;n&#233;ralis&#233;e_ ([arXiv:alg-geom/9603004](http://arxiv.org/abs/alg-geom/9603004))

* [[Gérard Laumon]], _Travaux de Frenkel, Gaitsgory et Vilonen sur la correspondance de Drinfeld-Langlands_, [math.AG/0207078](http://arxiv.org/abs/math.AG/0207078)

* {#Rothstein96} M. Rothstein. _Sheaves with connection on abelian varieties_, Duke Math. J., 84(3):565&#8211;598, 1996

  _Correction to: "Sheaves with connection on abelian varieties." Duke Math. J., 87(1):205&#8211;211, 1997.

Proof that the original version of the conjecture is false in general is due to

* {#Lafforgue09} [[Vincent Lafforgue]], _Quelques calculs reli&#233;s &#224; la correspondance de Langlands g&#233;om&#233;trique pour $\mathbb{P}^1$ (version provisoire)_ 2009 ([web](http://www.math.jussieu.fr/~vlafforg/), [pdf](http://vlafforg.perso.math.cnrs.fr/geom.pdf))

The refined version of the conjecture stated in [[derived algebraic geometry]], called the [[categorical geometric Langlands conjecture]], is due to

* {#GaitsgoryRozenblyum} [[Dennis Gaitsgory]],  [[Nick Rozenblyum]], _[[Notes on geometric Langlands]], ([web](http://www.math.harvard.edu/~gaitsgde/GL/))

* {#ArinkinGaitsgory12} [[Dima Arinkin]], [[Dennis Gaitsgory]], _Singular support of coherent sheaves, and the geometric Langlands conjecture_ ([arXiv.1201.6343](http://arxiv.org/abs/1201.6343))

Other comments on the relation to [[TQFT]] include

* {#Kapranov95} [[Mikhail Kapranov]], _Analogies between the Langlands Correspondence and Topological Quantum Field Theory_, in _Functional Analysis on the Eve of the 21st Century_ Progress in Mathematics Volume 131/132, 1995, pp 119-151


Comments on the development of the geometric duality by [[Robert Langlands]] himself:

* {#Langlands13} [[Robert Langlands]], _The Search for a Mathematically Satisfying Geometric Theory of Automorphic Forms_, Notes for a lecture at Mostow-Fest, Yale 2013 ([IAS page](http://publications.ias.edu/rpl/paper/2578), [video](http://www.youtube.com/watch?v=pfpzET8UkF4), [pdf](http://publications.ias.edu/sites/default/files/lecture_6.pdf))

* {#Langlands14} [[Robert Langlands]], _[[Problems in the theory of automorphic forms -- 45 years later]]_, talk at [Symmetries and correspondences in number theory, geometry, algebra, physics: intra-disciplinary trends](https://www.maths.nottingham.ac.uk/personal/ibf/files/sc3.html), Oxford, July 5 - July 8, 2014

Langlands's doubts about or dissatifaction with the "geometric Langlands program" expressed in these talks (where he suggests that his name not be associated with the "geometric" part of the program) eventually led to 

* [[Robert Langlands]], _Об аналитическом виде геометрической теории автоморфных форм_, IAS 2018 ([ias:2678](http://publications.ias.edu/rpl/paper/2678), [pdf](http://publications.ias.edu/sites/default/files/iztvestiya_3.pdf))

This in turn led to the reaction

* [[Edward Frenkel]], _Is there an analytic theory of automorphic functions for complex algebraic curves?_ ([arXiv:1812.08160](https://arxiv.org/abs/1812.08160))


See also the deformation to the [[quantum geometric Langlands correspondence]], such as

* [[Mina Aganagic]], [[Edward Frenkel]], [[Andrei Okounkov]], _Quantum $q$-Langlands Correspondence_ ([arXiv:1701.03146](https://arxiv.org/abs/1701.03146))


Proof of the [[categorical geometric Langlands conjecture]]:

* {#GaitsgoryGLCWebpage} [[Dennis Gaitsgory]]: *Proof of the geometric Langlands conjecture* (2025) &lbrack;[webpage](https://people.mpim-bonn.mpg.de/gaitsgde/GLC/)&rbrack;

* [[Dennis Gaitsgory]], [[Sam Raskin]]: *Proof of the geometric Langlands conjecture I: construction of the functor* &lbrack;[arXiv:2405.03599](https://arxiv.org/abs/2405.03599), [pdf](https://people.mpim-bonn.mpg.de/gaitsgde/GLC/functor.pdf)&rbrack;

* [[Dima Arinkin]], D. Beraldo, Justin Campbell, L. Chen, [[Dennis Gaitsgory]], J. Faergeman, Kevin Lin, [[Sam Raskin]], [[Nick Rozenblyum]]: *Proof of the geometric Langlands conjecture II: Kac-Moody localization and the FLE* &lbrack;[arXiv:2405.03648](https://arxiv.org/abs/2405.03648), [pdf](https://people.mpim-bonn.mpg.de/gaitsgde/GLC/Loc.pdf)&rbrack;

* Justin Campbell, Lin Chen, Joakim Faergeman, [[Dennis Gaitsgory]], Kevin Lin, [[Sam Raskin]], [[Nick Rozenblyum]]: *Proof of the geometric Langlands conjecture III: compatibility with parabolic induction* &lbrack;[arXiv:2409.07051](https://arxiv.org/abs/2409.07051), [pdf](https://people.mpim-bonn.mpg.de/gaitsgde/GLC/Eis.pdf)&rbrack;

* [[Dima Arinkin]], D. Beraldo, L. Chen, J. Faergeman, [[Dennis Gaitsgory]], Kevin Lin, [[Sam Raskin]], [[Nick Rozenblyum]]: *Proof of the geometric Langlands conjecture IV: ambidexterity* &lbrack;[arXiv:2409.08670](https://arxiv.org/abs/2409.08670), [pdf](https://people.mpim-bonn.mpg.de/gaitsgde/GLC/ambidex.pdf)&rbrack;

* [[Dennis Gaitsgory]], [[Sam Raskin]]: *Proof of the geometric Langlands conjecture V: the multiplicity one theorem* &lbrack;[arXiv:2409.09856](https://arxiv.org/abs/2409.09856), [pdf](https://people.mpim-bonn.mpg.de/gaitsgde/GLC/multone.pdf)&rbrack;

Review:

* [[Dennis Gaitsgory]]: *On the Proof of the Geometric Langlands Correspondance*, IHES News (5 August 2024) &lbrack;[www.ihes.fr/en/gaitsgory-glc](https://www.ihes.fr/en/gaitsgory-glc)&rbrack;





### Surveys and reviews


* {#Frenkel05} [[Edward Frenkel]], _Lectures on the Langlands Program and Conformal Field Theory_, in _Frontiers in number theory, physics, and geometry II_, Springer Berlin Heidelberg, 2007. 387-533. ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172))


* [[Ron Donagi]], [[Tony Pantev]], _Lectures on the geometric Langlands
conjecture and non-abelian Hodge theory_, 2009 ([pdf](http://www.icmat.es/seminarios/langlands/school/handouts/pantev.pdf))

  > (with an eye towards [[nonabelian Hodge theory]])

More on the relation to [[string theory]] and [[S-duality]]:

* {#Frenkel09} [[Edward Frenkel]], _Gauge Theory and Langlands Duality_, S&#233;minaire Bourbaki no 1010, June 2009 ([arXiv:0906.2747](http://arxiv.org/abs/0906.2747))

With emphasis on the role of [[magnetic monopoles]] and [['t Hoof lines]]:

* [[Alexander B. Atanasov]], *Magnetic Monopoles, 't Hooft Lines, and the Geometric Langlands Correspondence*, 2018 ([pdf](http://abatanasov.com/Files/Thesis.pdf), [slides](http://abatanasov.com/Files/Thesis%20Presentation.pdf))


### Further resources

Collections of resources are here;

* [[David Ben-Zvi]], Geometric Langlands -- Lectures and Resources ([web](http://www.math.utexas.edu/users/benzvi/Langlands.html))

* geometric Laglands [page](http://www.math.uchicago.edu/~mitya/langlands)

Notes on two introductory lecture talks are here:

* [Pantev on Langlands I](http://golem.ph.utexas.edu/string/archives/000806.html)

  [Pantev on Langlands II](http://golem.ph.utexas.edu/string/archives/000807.html)


See also


* Ng&#244; B&#7843;o Ch&#226;u, _Le lemme fondamental pour les algebres de Lie_, [arxiv/0806.4566](http://arxiv4.library.cornell.edu/abs/0806.4566)


* James Arthur, _The Work of Ng&#244; B&#7843;o Ch&#226;u_, Proc. ICM Hyderabad 2010, [pdf](http://www.icm2010.org.in/wp-content/icmfiles/laudaions/fields2.pdf)

* lecture notes on an introductory talk by [[Tony Pantev]]: [Pantev on Langlands I](http://golem.ph.utexas.edu/string/archives/000806.html), [Pantev on Langlands II](http://golem.ph.utexas.edu/string/archives/000807.html)

* [[Edward Frenkel]], _Langlands correspondence for loop groups_, [description](http://math.berkeley.edu/~frenkel/NEWBOOK), [pdf](http://math.berkeley.edu/~frenkel/loop.pdf)


* [[Edward Frenkel]], a Bourbaki exposition, [pdf](http://math.berkeley.edu/~frenkel/BOOK/bourbaki.pdf)

* [[Edward Frenkel]], _Langlands duality for representations of quantum groups_, [arxiv/0809.4453](http://arxiv.org/abs/0809.4453)





### Interpretation in string theory
 {#ReferencesInterpretationInStringTheory}

#### Global

An interpretation of the global geometric Langlands correspondence as describing [[S-duality]] of [[topological twist|topologically twisted]] [[super Yang-Mills theory]], incarnated in [[mirror symmetry]] on its [[KK-compactification]] to 2d [[sigma-models]] ([[A-model]]/[[B-model]]-type) was given in

* {#KapustinWitten06} [[Anton Kapustin]], [[Edward Witten]], _Electric-Magnetic Duality And The Geometric Langlands Program_ , Communications in number theory and physics, Volume 1, Number 1, 1&#8211;236 (2007) ([arXiv:hep-th/0604151](http://arxiv.org/abs/hep-th/0604151))

* {#FrenkelWitten07} [[Edward Frenkel]], [[Edward Witten]], _Geometric Endoscopy and Mirror Symmetry_ ([arXiv:0710.5939](http://arxiv.org/abs/0710.5939))
 
* {#Witten08} [[Edward Witten]], _Mirror Symmetry, Hitchin's Equations, And Langlands Duality_ ([arXiv:0802.0999](http://arxiv.org/abs/0802.0999))

and discussed in the bigger picture of [[S-duality]] arising as the conformal invariance of the [[6d (2,0)-superconformal QFT]] in 

* {#Witten09} [[Edward Witten]], _Geometric Langlands From Six Dimensions_, in Peter Kotiuga (ed.) _A Celebration of the Mathematical Legacy of Raoul Bott_, AMS 2010 ([arXiv:0905.2720](http://arxiv.org/abs/0905.2720))

Reflections on the history (and possible future) of this insight are in

* interview with [[Edward Witten]] by [[Hirosi Ooguri]], 2014 ([pdf](http://www.ams.org/notices/201505/rnoti-p491.pdf))


An exposition of the relation to [[S-duality]] and [[electro-magnetic duality]] is in ([Frenkel 09](#Frenkel09)) and in

* [[Edward Frenkel]],  _What Do Fermat's Last Theorem and Electro-magnetic Duality Have in Common?_ KITP talk 2011 ([web](http://online.kitp.ucsb.edu/online/bblunch/frenkel/))

* [[Edward Frenkel]], _Overview of the links between the Langlands program and 4D super Yang--Mills theory_, KITP talk 2010, [video page](http://online.kitp.ucsb.edu/online/duallang_m10/frenkel), notes [pdf](http://online.kitp.ucsb.edu/online/duallang_m10/frenkel/pdf/Frenkel_LanglandsQFT_KITP.pdf)


Further developments are surveyed in 

* [[David Ben-Zvi]], _[[Loop Groups, Characters and Elliptic Curves]]_, 2012

Further discussion is also in 

* Tamas Hausel, _Global topology of the Hitchin system_ ([arXiv:1102.1717](http://arxiv.org/abs/1102.1717), [pdf slides](http://geom.epfl.ch/files/content/sites/geom/files/Calgary0312.pdf))

* Kevin Setter, _Topological quantum field theory and the geometric Langlands correspondence_. Dissertation (Ph.D.), California Institute of Technology 2013 ([web](http://resolver.caltech.edu/CaltechTHESIS:09192012-150137728))

Discussion from the point of view of [[M-theory]] is in 

* [[Meng-Chwan Tan]], _M-Theoretic Derivations of 4d-2d Dualities: From a Geometric Langlands Duality for Surfaces, to the AGT Correspondence, to Integrable Systems_ ([arXiv:1301.1977](http://arxiv.org/abs/1301.1977))

* [[Meer Ashwinkumar]], [[Meng-Chwan Tan]], _Unifying Lattice Models, Links and Quantum Geometric Langlands via Branes in String Theory_ ([arXiv:1910.01134](https://arxiv.org/abs/1910.01134))




A relation to [[T-duality]] (of the group manifolds!) is discussed in

* {#DaenzerErp} [[Calder Daenzer]], [[Erik van Erp]], _T-Duality for Langlands Dual Groups_ ([arXiv:1211.0763](http://arxiv.org/abs/1211.0763))

#### Local
 
Discussion of  [[local Langlands correspondence|local]] [[archimedean field|Archimedean]] Langlands duality for [[Whittaker functions]] as [[mirror symmetry]] of a suitable [[A-model]] and [[B-model]] is discussed in 

* {#GerasimovLebedevOblezin09} [[Anton Gerasimov]], Dimitri Lebedev, [[Sergey Oblezin]], 

  _Archimedean L-factors and Topological Field Theories I_ ([arXiv:0906.1065](http://arxiv.org/abs/0906.1065))

  _Archimedean L-factors and Topological Field Theories II_ ([arXiv:0909.2016](http://arxiv.org/abs/0909.2016))

  _Parabolic Whittaker Functions and Topological Field Theories I_ ([arXiv:1002.2622](http://arxiv.org/abs/1002.2622))


[[!redirects geometric Langlands duality]]

[[!redirects geometric Langlands program]]

[[!redirects geometric Langlands theory]]
[[!redirects geometric Langlands duality]]
[[!redirects geometric Langlands]]

[[!redirects geometric Langlands conjecture]]