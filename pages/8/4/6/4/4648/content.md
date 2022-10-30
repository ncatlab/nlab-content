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

The _geometric Langlands program_ is the analogue of the [[Langlands program]] with [[number fields]] replaced by [[function fields]]. 

The conjectured _geometric Langlands correspondence_ asserts that for $G$ a  [[reductive group]] there is an equivalence of [[derived categories]] of [[D-module]]s on the [[moduli stack]] of $G$-[[principal bundle]]s over a given [[curve]], and [[quasi-coherent sheaves]] on the moduli space of ${}^L G$-[[local system]]s 

$$
  \mathcal{D} Mod( Bun_G)
  \simeq
  \mathcal{O}Mod(Loc_{{}^L G})
$$

for ${}^L G$ the [[Langlands dual group]].

This equivalence is a certain limit of the more general [[quantum geometric Langlands correspondence]] that identifies twisted $D$-modules on both sides.

## Properties 
 {#Properties}


### Abelian case

In the case where $G$ is the [[multiplicative group]], hence where all bundles in question are [[line bundles]], geometric Langlands duality is well understood and is in fact a slight variant of a [[Fourier-Mukai transform]] ([Frenkel 05, section 4.4, 4.5](#Frenkel05)).


### Relation to S-duality
 {#RelationToSDuality}

The [[Kapustin-Witten TQFT]] ([KapustinWitten 2007](#KapustinWitten06)) is supposed to exhibit geometric Langlands duality as a special case of [[S-duality]]. 

See also at _[KK-compactification -- Formalization](http://ncatlab.org/nlab/show/Kaluza-Klein+mechanism#Formalization)_

[[!include geometric Langlands QFT -- table -- table]]


[[!include gauge theory from AdS-CFT -- table]]


### Relation to T-duality
 {#RelationToTDuality}

In some cases the passage between a Lie group and its [[Langlands dual group]] can be understood as a special case of [[T-duality]]. ([Daenzer-vanErp](#DaenzerErp))

## Related concepts

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

* [[Alexander Beilinson]], [[Vladimir Drinfeld]], _Quantization of the Hitchin system and Hecke eigensheaves_, draft, [pdf](http://www.math.uchicago.edu/~mitya/langlands/hitchin/BD-hitchin.pdf)
* Gerard Laumon, _Travaux de Frenkel, Gaitsgory et Vilonen sur la correspondance de Drinfeld-Langlands_, [math.AG/0207078](http://arxiv.org/abs/math.AG/0207078)

Discussion of what the geometric theory ultimately should be from the point of view of [[derived algebraic geometry]] are in

* {#GaitsgoryRozenblyum} [[Dennis Gaitsgory]],  [[Nick Rozenblyum]], _Notes on Geometric Langlands -- A study in derived algebraic geometry_ ([web](http://www.math.harvard.edu/~gaitsgde/GL/))

and in less category-theoretic terms in 

* {#Langlands13} [[Robert Langlands]], _The Search for a Mathematically Satisfying Geometric Theory of Automorphic Forms_, Notes for a lecture at Mostow-Fest, Yale 2013 ([IAS page](http://publications.ias.edu/rpl/paper/2578), [video](http://www.youtube.com/watch?v=pfpzET8UkF4), [pdf](http://publications.ias.edu/sites/default/files/lecture_6.pdf))


### Surveys and reviews

A classical survey is

* {#Frenkel05} [[Edward Frenkel]], _Lectures on the Langlands Program and Conformal Field Theory_ ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172)).


Another set of lecture notes on geometric Langlands and [[nonabelian Hodge theory]] is

* [[Ron Donagi]], [[Tony Pantev]], _Lectures on the geometric Langlands
conjecture and non-abelian Hodge theory_, 2009 ([pdf](http://www.icmat.es/seminarios/langlands/school/handouts/pantev.pdf))

More exposition of the relation to [[string theory]] and [[S-duality]] is in

* {#Frenkel09} [[Edward Frenkel]], _Gauge Theory and Langlands Duality_, S&#233;minaire Bourbaki no 1010, June 2009 ([arXiv:0906.2747](http://arxiv.org/abs/0906.2747))

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

and discussed in bigger picture of [[S-duality]] arising as the conformal invariance of the [[6d (2,0)-superconformal QFT]] in 

* {#Witten09} [[Edward Witten]], _Geometric Langlands From Six Dimensions_, in Peter Kotiuga (ed.) _A Celebration of the Mathematical Legacy of Raoul Bott_, AMS 2010 ([arXiv:0905.2720](http://arxiv.org/abs/0905.2720))

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


A relation to [[T-duality]] (of the group manifolds!) is discussed in

* {#DaenzerErp} Calder Daenzer, Erik Van Erp, _T-Duality for Langlands Dual Groups_ ([arXiv:1211.0763](http://arxiv.org/abs/1211.0763))

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