

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea



### General idea

The [[standard model of particle physics]] asserts that the fundamental quantum [[field (physics)|physical fields]] and [[particles]] are modeled as [[sections]] of and [[connection on a bundle|connections]] on a [[vector bundle]] that is [[associated bundle|associated]] to a $G$-[[principal bundle]], where the [[Lie group]] $G$ -- called the [[gauge group]] -- is  the [[product]] of ([[special unitary group|special]]) [[unitary groups]] $G = SU(3) \times SU(2) \times U(1)$ (or rather a [[quotient]] of this by the [[cyclic group]] $Z/6$, see [there](standard+model+of+particle+physics#GaugeGroup)) and where the [[representation]] of $G$ used to form the [[associated bundle|associated]] [[vector bundle]] looks fairly ad hoc on first sight.

A **grand unified theory** ("GUT" for short) in this context is an attempt to realize the standard model as sitting inside a conceptually simpler [[model (in particle physics)|model]], in particular one for which the [[gauge group]] is a bigger but _simpler_ group $\hat{G}$, preferably a _[[simple Lie group]]_ in the technical sense, which contains $G$ as a [[subgroup]]. Such a grand unified theory would be [[phenomenology|phenomenologically]] viable if a process of [[spontaneous symmetry breaking]] at some high [[energy]] scale -- the "GUT scale" -- would reduce the model back to the [[standard model of particle physics]] without adding spurious extra effects that would not be in agreement with existing observations in [[experiment]].

The terminology "grand unified" here refers to the fact that such a single simple group $\hat{G}$ would unify the fundamental [[forces]] of [[electromagnetism]], the [[weak nuclear force]] and the [[strong nuclear force]] in a way that generalizes the way in which the [[electroweak field]] already unifies the [[weak nuclear force]] and [[electromagnetism]], and electromagnetism already unifies, as the word says, electricity and magnetism.


Since no GUT model has been fully validated yet (but see for instance [Fong-Meloni 14](#FongMeloni14)), GUTs are [[model (physics)|models]] "beyond the [[standard model of particle physics|standard model]]". Often quantum physics "beyond the standard model" is expected to also say something sensible about [[quantum gravity]] and hence unify not just the three gauge forces but also the fourth known fundamental force, which is [[gravity]]. Models that aim to do all of this would then "unify" the entire content of the [[standard model of particle physics]] plus the [[standard model of cosmology]], hence "everything that is known about fundamental physics" to date. Therefore such theories are then sometimes called a _[[theory of everything]]_. 

(Here it is important to remember the context, both "grand unified" and "of everything" refers to aspects of presently available models of fundamental physics, and not to deeper philosophical questions of [[ontology]].)

\linebreak

[[length scales]] in the [[observable universe]] (from [[cosmological constant|cosmic]] scales, over [[fundamental particle]]-[[masses]] around the [[electroweak symmetry breaking]] to [[GUT scale]] and [[Planck scale]]):

<center>
<img src="https://ncatlab.org/nlab/files/ScalesInFundamentalPhysics.jpg" width="700">
</center>

> graphics grabbed from [Zupan 19](flavour+in+particle+physics#Zupan19)



### The $SU(5)$-GUT (Georgi-Glashow)
  {#IdeaofSU5GUT}

The argument for the hypothesis of "grand unification" is fairly compelling if one asks for _[[simple objects|simple algebraic structures]]_ in the technical sense ([[simple Lie groups]] and their [[irreducible representations]]): 

The _exact_ gauge group of the [[standard model of particle physics]] is really a [[quotient group]] 

$$
  G_{SM}
  \;=\; 
  \big( U(1) \times SU(2) \times SU(3) \big) / \mathbb{Z}_6
  \,,
$$

where the [[cyclic group]] $\mathbb{Z}_6$ [[free action|acts freely]], hence exhibiting a subtle global twist in the gauge structure. This seemingly ad hoc group turns out to be [[isomorphism|isomorphic]] to the [[subgroup]]

$$
  \underset{
    \simeq \big( U(1) \times SU(2) \times SU(3) \big) / \mathbb{Z}_6  }{
  \underbrace{
    S \big( U(2) \times U(3)\big)
  }}
  \;\subset\;
  SU(5)
$$

of [[special unitary group|SU(5)]] (see [Baez-Huerta 09, p. 33-36](#BaezHuerta09)). The latter happens to be a [[simple Lie group]], thus exhibiting the exact standard model Lie group as being "simply" a "(2+3)-breaking" of a [[simple Lie group]].

Moreover, the [[gauge group]]-[[representation]] $V_{SM}$ that captures one [[generation of fundamental particles]] of the [[standard model of particle physics]], which looks fairly ad hoc as a representation of $G_{SM}$ (e.g. [Baez-Huerta 09, table 1](#BaezHuerta09)), but as a representation of $SU(5)$ it is simply 

$$
  V_{SM} \simeq \Lambda \mathbb{C}^5
$$ 

(see [Baez-Huerta 09, p. 36-41](#BaezHuerta09)).

This leads to the $SU(5)$-GUT due to [Georgi-Glashow 74](#GeorgiGlashow74)

### D-Series GUTs

#### The $Spin(10)$-GUT (known as "$SO(10)$")
 {#TheGUTKnownAsSO10}

There is a further inclusion $SU(5) \hookrightarrow $ [[Spin(10)]] into the [[spin group]] in 10 (Euclidean) dimensions (still a [[simple Lie group]]), and one [[generation of fundamental particles]] regarded as an $SU(5)$-[[representation]] $\Lambda \mathbb{C}^5$ as [above](#IdeaofSU5GUT) extends to a [[spin representation]] (see [Baez-Huerta 09, theorem 2](#BaezHuerta09)). This has the aesthetically pleasing effect that under this identification the 1-[[generation of fermions|generation]] rep $V_{SM}$ is now identified as

$$
  V_{SM} \;\simeq\; \mathbf{16} \oplus \overline{\mathbf{16}}
$$

namely as the [[direct sum]] of [[generalized the|the]] two (complex) [[irreducible representations]] of [[Spin(10)]], together being the [[Dirac representation]] of [[Spin(10)]].

The exact [[gauge group]] of the [[standard model of particle physics]] (see [there](standard+model+of+particle+physics#GaugeGroup)) is [[isomorphism|isomorphic]] to the [[subgroup]] of [[Spin(9)]] $\subset$ [[Spin(10)]] which respects a splitting $\mathbb{H} \oplus \mathbb{H} \simeq_{\mathbb{R}} \mathbb{C} \oplus \mathbb{C}^3$ ([Krasnov 19](Spin9#Krasnov19)).


Again, this means that under the embedding of the gauge group $G_{SM}$ all the way into the [[simple Lie group]] [[Spin(10)]], its ingredients become _simpler_, not just in a naive sense, but in the technical mathematical sense of _[[simple objects|simple algebraic objects]]_.

Discussion of [[SO(10)]] (i.e. [[Spin(10)]]) GUT-models with realistic [[phenomenology]] is in [BLM 09](#BLM09) [Malinský 09](#Malinsky09), [Lavoura-Wolfenstein 10](#LavouraWolfenstein10) [Altarelli-Meloni 13](#AltarelliMeloni13) [Dueck-Rodejohann 13](#DueckRodejohann13) [Ohlsson-Pernow 19](#OhlssonPernow19) [CPS 19](#CPS19). 

\begin{imagefromfile}
  "file_name": "MinimalNonSusySO10GUTMalinsky.jpg",
  "width": 500
\end{imagefromfile}

> slide grabbed from [Malinský 09](#Malinsky09)

Discussion of [[leptoquarks]] in $SO(10)$-models possibly explaining the [[flavour anomalies]]: [AMM 19](#AMM19)


\linebreak


#### The $Spin(11)$-GUT (known as "$SO(11)$")
 {#TheGUTKnownAsSO11}

Models with [[Spin(11)]] ("[[SO(11)]]") GUT group.

Specifically with [[gauge-Higgs unification]] in a [[Randall-Sundrum model]]-like 6d spacetime: [Hosotani-Yamatsu 15](#HosotaniYamatsu15), [Furui-Hosotani-Yamatsu 16](#FuruiHosotaniYamatsu16), [Hosotani 17](#Hosotani17), [Hosotani-Yamatsu 17](#HosotaniYamatsu17)


See the references [below](#ReferencesSpin11).


\linebreak

#### The $Spin(12)$-GUT (known as "$SO(12)$")
 {#TheGUTKnownAsSO12}


Models with [[Spin(12)]] ("[[SO(12)]]") GUT group.

Specifically with [[gauge-Higgs unification]] in a [[Randall-Sundrum model]]-like 6d spacetime: [Nomura-Sato 08](#NomuraSato08), [Nomura 09](#Nomura09), [Chiang-Nomura-Sato 11](#ChiangNomuraSato11))

See the references [below](#ReferencesSpin12).

\linebreak



#### The $Spin(16), Spin(18)$-GUT (known as "$SO(16), SO(18)$")
 {#TheGUTKnownAsSO16}

Models with [[Spin(16)]] ("[[SO(16)]]") GUT group.


[Wilczek-Zee 82](#WilczekZee82), [Senjanovic-Wilczek-Zee 84](#SenjanovicWilczekZee84), [Martínez-Melfo-Nesti-Senjanovic 11](#MartínezMelfoNestiSenjanovic11)

See also [di Lucio 11, p. 44](#diLucio11) and see the references [below](#ReferencesSpin16).

Predicts [[fourth generation of fermions]]...


### E-series GUTs

The most studied choices of GUT-groups $G$ are [[special unitary group|SU(5)]], [[spin group|Spin(10)]] (in the physics literature often referred to as [[special orthogonal group|SO(10)]]) and [[E6]] (review includes [Witten 86, sections 1 and 2](#Witten86)). 

It so happens that, mathematically, the sequence [[special unitary groups|SU(5)]], [[spin group|Spin(10)]], [[E6]] naturally continues (each step by consecutively adding a node to the [[Dynkin diagrams]]) with the [[exceptional Lie groups]] [[E7]], [[E8]] that naturally appear in [[heterotic string theory|heterotic]] [[string phenomenology]] (exposition is in [Witten 02a](#Witten02a)) and conjecturally further via the [[U-duality]] [[Kac-Moody groups]] [[E9]], [[E10]], [[E11]] that are being argued to underly [[M-theory]]. In the context of [[F-theory]] model building, also properties of the observes [[Yukawa couplings]] may point to exceptional GUT groups ([Zoccarato 14, slide 11](#Zoccarato14), [Vafa 15, slide 11](#Vafa15)).

#### The $E_6$-GUT

(...)

review in [Britto 17](#Britto17)

(...)

#### The $E_7$-GUT (?)

(...)

#### The $E_8$-GUT (?)

(...)


## Properties

### Relation to proton decay
  {#RelationToProtonDecay}

Many GUT models imply that the [[proton]] -- which in the [[standard model of particle physics]] is a stable [[bound state]] (of [[quarks]]) -- is in fact unstable, albeit with an extremely long mean liftetime, and hence may decay (e.g. [KM 14](#KM14)). [[experiment|Experimental]] searches for such _[[proton decay]]_ (see there for more) put strong bounds on this effect and hence heavily constrain or rule out many [[GUT]] [[model (physics)|models]].

But in recent years it is claimed that there are in fact realistic $SU(5)$ [[GUT]] [[model (physics)|models]] that do not imply any [[proton decay]], quite generically so for [[MSSM]]-models ([Mütter-Ratz-Vaudrvange 16](#MuetterRatzVaudrvange16)), but also for non-supersymmetric models  ( [Fornal-Grinstein 17](#FornalGrinstein17), [Fornal-Grinstein 18](#FornalGrinstein18), in particular in [[gauge-Higgs grand unification]] such as [[Spin(11)]]- ("[[SO(11)]]"-) and [[Spin(12)]]- ("[[SO(12)]]"-) models: ([Hosotani-Yamatsu 15](#HosotaniYamatsu15), [Furui-Hosotani-Yamatsu 16, Sec. 2.6](#FuruiHosotaniYamatsu16) [Hosotani 17, Section 6](#Hosotani17)).



### Relation to neutrino masses
 {#RelationToNeutrinoMasses}

The high energy scale required by a [[seesaw mechanism]] to produce the experimentally observer [[neutrino]] masses happens to be about the conventional [[GUT scale]], for review see for instance ([Mohapatra 06](#Mohapatra06)).

> I also noted at the same time that interactions between a pair of lepton doublets and a pair of scalar doublets can generate a neutrino mass, which is suppressed only by a factor $M^{-1}$, and that therefore with a reasonable estimate of $M$ could produce observable neutrino oscillations. The subsequent confirmation of neutrino oscillations lends support to the view of the Standard Model as an effective field theory, with M somewhere in the neighborhood of $10^{16} GeV$. ([Weinberg 09, p. 15](neutrino#Weinberg09))


Detailed matching of parameters of non-supersymmetric $Spin(10)$-GUT to [[neutrino]] [[masses]] is discussed in [Ohlsson-Pernow 19](#OhlssonPernow19)



### Relation to leptoquarks
 {#RelationToLeptoquarks}

Generically, GUT-theories predict the existence of [[leptoquarks]] ([Murayama-Yanagida 92](#MurayamaYanagida92)), possibly related to the apparently observed 

* [[flavour anomalies]] ([BDFKFS 18](#BDFKFS18), [AMM 19](#AMM19), [Heek-Teresi 18](#HeekTeresi18), [Heek-Teresi 19](#HeekTeresi19))

* [anomalies](anomalous+magnetic+moment#Anomalies) in [[anomalous magnetic moment]] of [[muon]] and [[electron]]


### Occurrence in string phenomenology
 {#InStringPhenomenology}

Discussion of [[string phenomenology]] of [[intersecting D-brane models]] [[KK-compactification|KK-compactified]] with non-geometric [[fibers]] such that the would-be string [[sigma-models]] with these [[target spaces]] are in fact [[Gepner models]] (in the sense of _[Spectral Standard Model and String Compactifications](https://www.physicsforums.com/insights/spectral-standard-model-string-compactifications/)_) is in ([Dijkstra-Huiszoon-Schellekens 04a](#DijkstraHuiszoonSchellekens04a), [Dijkstra-Huiszoon-Schellekens 04b](#DijkstraHuiszoonSchellekens04b)):


<center>
<img src="https://ncatlab.org/nlab/files/SchellekensSuperGepnerModelScanII.jpg" width="600">
</center>

>  A plot of [[standard model of particle physics|standard model]]-like [[coupling constants]] in a computer scan of [[Gepner model]]-[[KK-compactification]] of [[intersecting D-brane models]] according to [Dijkstra-Huiszoon-Schellekens 04b](#DijkstraHuiszoonSchellekens04b). 

>  The blue dot indicates the couplings in $SU(5)$-[[GUT]] theory. The faint lines are NOT drawn by hand, but reflect increased density of Gepner models as seen by the computer scan.


## Related concepts

* [[theory of everything]]

* [[gauge coupling unification]]

* [[supersymmetry]]

* [[Connes-Lott-Chamseddine-Barrett model]]

[[!include fundamental scales -- contents]]


## References 
 {#References}

### General

Original articles include

* {#PatiSalam74} [[Jogesh Pati]], [[Abdus Salam]], _Lepton number as the fourth "color"_, Phys. Rev. D 10, 275 – Published 1 July 1974 ([doi:10.1103/PhysRevD.10.275](https://doi.org/10.1103/PhysRevD.10.275))


* {#GeorgiGlashow74} [[Howard Georgi]], [[Sheldon Glashow]], _Unity of All Elementary-Particle Forces_, Phys. Rev. Lett. 32, 438, 1974 ([doi:10.1103/PhysRevLett.32.438](https://doi.org/10.1103/PhysRevLett.32.438))


See also

* Wikipedia, _[Pati-Salam model](https://en.wikipedia.org/wiki/Pati%E2%80%93Salam_model)_

* Wikipedia, _[Grand unification energy](https://en.wikipedia.org/wiki/Grand_unification_energy)_

Discussion with an eye towards [[supergravity]] unification:

* {#GellMann83} [[Murray Gell-Mann]], introductory talk at _[Shelter Island II](https://en.wikipedia.org/wiki/Shelter_Island_Conference)_, 1983 ([[Gell-Mann_ShelterIslandII_1983.pdf:file]]) 

  in: _Shelter Island II: Proceedings of the 1983 Shelter Island Conference on Quantum Field Theory and the Fundamental Problems of Physics_. MIT Press. pp. 301&#8211;343. ISBN 0-262-10031-2.


* [[Murray Gell-Mann]], [[Pierre Ramond]], Richard Slansky, _Complex Spinors and Unified Theories_, Supergravity, [[Peter van Nieuwenhuizen]] and D.Z. Freedman, eds, North Holland Publishing Co, 1979, (reprinted as [arXiv:1306.4669](http://arxiv.org/abs/1306.4669))




A basic textbook account is in

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 1.2 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

and a detailed one is in 

* A. Hebecker, J. Hisano, _Grand Unified Theories_, chapter 114. in Particle Data Group's _[The Review of Particle Physics](http://pdg.lbl.gov/2018/)_ 2018 ([pdf](http://pdg.lbl.gov/2018/reviews/rpp2018-rev-guts.pdf))

See also 

* {#diLucio11} Luca di Lucio, _Aspects of Symmetry Breaking inGrand Unified Theories_, 2011 ([pdf](https://www.sissa.it/tpp/phdsection/AlumniThesis/Luca%20Di%20Luzio.pdf))

Survey of arguments for the hypothesis of grand unification includes

* [[Michael Peskin]], _Beyond the Standard Model_ ([arXiv:hep-ph/9705479](http://arxiv.org/abs/hep-ph/9705479))

* [[Jogesh Pati]], _Discovery of Proton Decay: A Must for Theory, a Challenge for Experiment_ ([arXiv:hep-ph/0005095](http://arxiv.org/abs/hep-ph/0005095))



* {#Witten02a} [[Edward Witten]], _Quest For Unification_, Heinrich Hertz lecture at [SUSY 2002](http://www.desy.de/susy02/) at DESY, Hamburg ([arXiv:hep-ph/0207124](http://arxiv.org/abs/hep-ph/0207124))
 

Introduction to GUTs aimed more at mathematicians include

* {#Witten86} [[Edward Witten]], section 1 and 2 of _Physics and geometry_, Proceedings of the international congress of mathematicians, 1986 ([pdf](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0267.0306.ocr.pdf)) 

* {#BaezHuerta09} [[John Baez]], [[John Huerta]], _The Algebra of Grand Unified Theories_, Bull.Am.Math.Soc.47:483-552,2010 ([arXiv:0904.1556](http://arxiv.org/abs/0904.1556))

* {#Britto17} Vivian Anthony Britto, _A mathematical construction of $E_6$ grand unified theory_, Munich 2017 ([pdf](https://www.theorie.physik.uni-muenchen.de/TMP/theses/thesisbritto.pdf), [[BrittoGUT.pdf:file]])



### Proton (non-)decay
  {#ReferencesProtonNonDecay}

Discussion of experimental bounds on [[proton decay]] in GUTs includes

* {#KM14} Helena Kole&#353;ov&#225;, [[Michal Malinský]], _Proton lifetime in the minimal $SO(10)$ GUT and its implications for the LHC_, Phys. Rev. D 90, 115001 (2014) ([arXiv:1409.4961](http://arxiv.org/abs/1409.4961))

Claim that [[proton decay]] may be entirely avoided:

* {#MuetterRatzVaudrvange16} Andreas Mütter, Michael Ratz, Patrick K.S. Vaudrevange, _Grand Unification without Proton Decay_ ([arXiv:1606.02303](https://arxiv.org/abs/1606.02303))

  (claims that many [[string theory]] and [[supergravity]] models have this property)

* {#FornalGrinstein17} Bartosz Fornal, Benjamin Grinstein, _$SU(5)$ Unification without Proton Decay_, Physics Review Letters ([arXiv:1706.08535](https://arxiv.org/abs/1706.08535))

* {#FornalGrinstein18} Bartosz Fornal, Benjamin Grinstein, _Grand Unified Theory with a Stable Proton_, Int. J. Mod. Phys. A 33 (2018) 1844013 ([arXiv:1808.00953](https://arxiv.org/abs/1808.00953))

Claim that [[threshold corrections]] can considerably alter (decrease) proton decay rate predictions in non-supersymmetric GUTs:

* Joydeep Chakrabortty, Stephen F. King, Rinku Maji, _Unification, Proton Decay and Topological Defects in non-SUSY GUTs with Thresholds_ ([arXiv:1901.05867](https://arxiv.org/abs/1901.05867))



### Realistic models and phenomenology
 {#ReferencesRealisticModels}

Discussion of [[phenomenology|phenomenologically]] viable GUT-[[model (in theoretical physics)|models]] (compatible with [[experiment]] and the [[standard model of particle physics]]):

#### $SO(10)$-GUT

The idea of "SO(10)" ([[Spin(10)]]) GUT originates with 

* [[Harald Fritzsch]], [[Peter Minkowski]], _Unified interactions of leptons and hadrons_, Annals of Physics Volume 93, Issues 1–2, 5 September 1975, Pages 193-266 (<a href="https://doi.org/10.1016/0003-4916(75)90211-0">doi:10.1016/0003-4916(75)90211-0</a>)


Review:

* {#Malinsky09} [[Michal Malinský]], _35 years of GUTs - where do we stand?_, 2009 ([pdf](https://www.mpi-hd.mpg.de/lin/seminar_theory/talks/Malinsky.pdf))

* {#BLM09} Stefano Bertolini, Luca Di Luzio, [[Michal Malinský]], _Intermediate mass scales in the non-supersymmetric SO(10) grand unification: a reappraisal_, Phys. Rev. D80:015013, 2009 ([arXiv:0903.4049](https://arxiv.org/abs/0903.4049))


for non-superymmetric [[model (physics)|models]]:

* {#LavouraWolfenstein10} L. Lavoura and Lincoln Wolfenstein, _Resuscitation of minimal $SO(10)$ grand unification_, Phys. Rev. D 48, 264 ([doi:10.1103/PhysRevD.48.264](https://doi.org/10.1103/PhysRevD.48.264))

* {#AltarelliMeloni13} Guido Altarelli, Davide Meloni, _A non Supersymmetric SO(10) Grand Unified Model for All the Physics below $M_{GUT}$_ ([arXiv:1305.1001](https://arxiv.org/abs/1305.1001))

* {#DueckRodejohann13} Alexander Dueck, Werner Rodejohann, _Fits to $SO(10)$ Grand Unified Models_ ([arXiv:1306.4468](http://arxiv.org/abs/1306.4468))

* {#FongMeloni14} Chee Sheng Fong, Davide Meloni, Aurora Meroni, Enrico Nardi, _Leptogenesis in $SO(10)$_ ([arXiv:1412.4776](http://arxiv.org/abs/1412.4776))

  (in view of [[leptogenesis]])

* {#OhlssonPernow19} Tommy Ohlsson, Marcus Pernow, _Fits to Non-Supersymmetric SO(10) Models with Type I and II Seesaw Mechanisms Using Renormalization Group Evolution_ ([arXiv:1903.08241](https://arxiv.org/abs/1903.08241))

* {#CPS19} Mainak Chakraborty, M.K. Parida, Biswonath Sahoo, _Triplet Leptogenesis, Type-II Seesaw Dominance, Intrinsic Dark Matter, Vacuum Stability and Proton Decay in Minimal SO(10) Breakings_ ([arXiv:1906.05601](https://arxiv.org/abs/1906.05601))

  > Results indicating non-SUSY $SO(10)$ as self sufficient theory for neutrino masses, baryon asymmetry, dark matter, vacuum stability of SM scalar potential, origin of three gauge forces, and observed proton stability.

* Nobuchika Okada, Digesh Raut, Qaisar Shafi, _Inflation, Proton Decay, and Higgs-Portal Dark Matter in $SO(10) \times U(1)_\pri$_ ([arXiv:1906.06869](https://arxiv.org/abs/1906.06869))

for [[supersymmetry|supersymmetric]] [[model (physics)|models]]:

* Archana Anandakrishnan, B. Charles Bryant, Stuart Raby, _LHC Phenomenology of $SO(10)$ Models with Yukawa Unification II_ ([arXiv:1404.5628](http://arxiv.org/abs/1404.5628))

* Ila Garg, _New minimal supersymmetric $SO(10)$ GUT phenomenology and its cosmological implications_ ([arXiv:1506.05204](http://arxiv.org/abs/1506.05204))

#### $SO(11)$-GUT
 {#ReferencesSpin11}

Discussion for [[Spin(11)]] GUT group ("[[SO(11)]]"):

* {#HosotaniYamatsu15} [[Yutaka Hosotani]], Naoki Yamatsu, _Gauge–Higgs grand unification_, Progress of Theoretical and Experimental Physics, Volume 2015, Issue 11, November 2015 ([doi:10.1093/ptep/ptv153](https://doi.org/10.1093/ptep/ptv153), [doi:10.1093/ptep/ptw116](https://doi.org/10.1093/ptep/ptw116))

* {#FuruiHosotaniYamatsu16} Atsushi Furui, [[Yutaka Hosotani]], Naoki Yamatsu, _Toward Realistic Gauge-Higgs Grand Unification_, Progress of Theoretical and Experimental Physics, Volume 2016, Issue 9, September 2016, 093B01 ([arXiv:1606.07222](https://arxiv.org/abs/1606.07222))

* {#Hosotoni16} [[Yutaka Hosotani]], _Gauge-Higgs EW and Grand Unification_, International Journal of Modern Physics AVol. 31, No. 20n21, 1630031 (2016)  ([arXiv:1606.08108](https://arxiv.org/abs/1606.08108))


* {#Hosotani17} [[Yutaka Hosotani]], _New dimensions from gauge-Higgs unification_ ([arXiv:1702.08161](https://arxiv.org/abs/1702.08161))

* {#HosotaniYamatsu17} Yutaka Hosotani, Naoki Yamatsu, _Electroweak Symmetry Breaking and Mass Spectra in Six-Dimensional Gauge-Higgs Grand Unification_ ([arXiv:1710.04811](https://arxiv.org/abs/1710.04811))


#### $SO(12)$-GUT
 {#ReferencesSpin12}

Discussion for [[Spin(12)]] GUT group ("[[SO(12)]]"):

* S. Rajpoot and P. Sithikong, _Implications of the $SO(12)$ gauge symmetry for grand unification_, Phys. Rev. D 23, 1649 (1981) ([doi:10.1103/PhysRevD.23.1649](https://doi.org/10.1103/PhysRevD.23.1649))

* {#NomuraSato08} Takaaki Nomura, Joe Sato, _Standard(-like) Model from an $SO(12)$ Grand Unified Theory in six-dimensions with $S^2$ extra-space_, Nucl.Phys.B811:109-122, 2009 ([arXiv:0810.0898](https://arxiv.org/abs/0810.0898))

* {#Nomura09} Takaaki Nomura, _Physics beyond the standard model with $S^2$ extra-space_, 2009 ([pdf](http://krishna.th.phy.saitama-u.ac.jp/joe/doctor/nomura-doctor.pdf), [[NomuraSO12GUT.pdf:file]])

* {#ChiangNomuraSato11} Cheng-Wei Chiang, Takaaki Nomura, Joe Sato, _Gauge-Higgs unification models in six dimensions with $S^2/\mathbb{Z}_2$ extra space and GUT gauge symmetry_ ([arXiv:1109.5835](https://arxiv.org/abs/1109.5835))

#### $SO(16)$- and $Spin(18)$-GUT
 {#ReferencesSpin16}

Discussion for [[Spin(16)]] and [[Spin(18)]] GUT group ("[[SO(16)]]" and "[[SO(18)]]"):

* {#WilczekZee82} [[Frank Wilczek]], [[Anthony Zee]], _Families from spinors_, Phys. Rev. D 25, 553 (1982) ([doi:10.1103/PhysRevD.25.55310.1103/PhysRevD.25.553](https://doi.org/10.1103/PhysRevD.25.553))

* {#SenjanovicWilczekZee84} Goran Senjanović, [[Frank Wilczek]], [[Anthony Zee]], _Reflections on mirror fermions_,  Physics Letters B Volume 141, Issues 5–6, 5 July 1984, Pages 389-394 Physics Letters B (<a href="https://doi.org/10.1016/0370-2693(84)90269-7">doi:10.1016/0370-2693(84)90269-7</a>)

* {#MartínezMelfoNestiSenjanovic11} Homero Martínez, Alejandra Melfo, Fabrizio Nesti, Goran Senjanović, _Three Extra Mirror or Sequential Families: a Case for Heavy Higgs and Inert Doublet_, Phys. Rev. Lett.106:191802, 2011 ([arXiv:1101.3796](https://arxiv.org/abs/1101.3796))

* {#Guigan19} Michael McGuigan, _Dark Horse, Dark Matter: Revisiting the $SO(16) \times SO(16)'$ Nonsupersymmetric Model in the LHC and Dark Energy Era_ ([arXiv:1907.01944](https://arxiv.org/abs/1907.01944))

#### $E_8$-GUT

See at _[heterotic string -- phenomenology](heterotic+string+theory#ReferencesPhenomenology)_

See also:

* Alfredo Aranda, Francisco J. de Anda, Stephen F. King, _Exceptional Unification of Families and Forces_ ([arXiv:2005.03048](https://arxiv.org/abs/2005.03048))

* Alfredo Aranda, Francisco J. de Anda, _Complete $E_8$ Unification in 10 Dimensions_ ([arXiv:2007.13248](https://arxiv.org/abs/2007.13248))

* George Manolakos, Gregory Patellis, George Zoupanos, _$\mathcal{N}=1$ trinification from dimensional reduction of $N=1$, 10D $E_8$ over $SU(3)/U(1)\times U(1) \times \mathbb{Z}_3$ and its phenomenological consequences_ ([arXiv:2009.07059](https://arxiv.org/abs/2009.07059))

* Francisco J. de Anda, Alfredo Aranda, António P. Morais, Roman Pasechnik, _Gauge couplings evolution from the Standard Model, through Pati-Salam theory, into $E_8$ unification of families and forces_ ([arXiv:2011.13902](https://arxiv.org/abs/2011.13902))





[[!include heterotic string phenomenology -- references]]



### In type II string theory

Computer scan of [[Gepner model]]-compactifications in relation to GUT-models is in 

* {#DijkstraHuiszoonSchellekens04a} T.P.T. Dijkstra, L. R. Huiszoon, [[Bert Schellekens]], _Chiral Supersymmetric Standard Model Spectra from Orientifolds of Gepner Models_, Phys.Lett. B609 (2005) 408-417 ([arXiv:hep-th/0403196](https://arxiv.org/abs/hep-th/0403196))

* {#DijkstraHuiszoonSchellekens04b} T.P.T. Dijkstra, L. R. Huiszoon, [[Bert Schellekens]], _Supersymmetric Standard Model Spectra from RCFT orientifolds_, Nucl.Phys.B710:3-57,2005 ([arXiv:hep-th/0411129](https://arxiv.org/abs/hep-th/0411129))


Realization of GUTs in the context of [[M-theory on G2-manifolds]] and possible resolution of the [[doublet-triplet splitting problem]] is discussed in

* {#Witten02b} [[Edward Witten]], _Deconstruction, $G_2$ Holonomy, and Doublet-Triplet Splitting_, ([arXiv:hep-ph/0201018](http://arxiv.org/abs/hep-ph/0201018))

* [[Bobby Acharya]], Krzysztof Bozek, Miguel Crispim Romao, Stephen F. King, Chakrit Pongkitivanichkul, _$SO(10)$ Grand Unification in M theory on a $G_2$ manifold_ ([arXiv:1502.01727](http://arxiv.org/abs/1502.01727))

Discussion of GUTs in [[F-theory]] includes

* [[Chris Beasley]], [[Jonathan Heckman]], [[Cumrun Vafa]], _GUTs and Exceptional Branes in F-theory - I_ ([arxiv:0802.3391](http://arxiv.org/abs/0802.3391)), _II: Experimental Predictions_ ([arxiv:0806.0102](http://arxiv.org/abs/0806.0102))


* [[Chris Beasley]], [[Jonathan Heckman]], [[Cumrun Vafa]], _GUTs and Exceptional Branes in F-theory - I_, JHEP 0901:058,2009 ([arXiv:0802.3391](http://arxiv.org/abs/0802.3391))


* {#Zoccarato14} Gianluca Zoccarato, _Yukawa couplings at the point
of $E_8$ in F-theory_, 2014 ([pdf](http://stringpheno2014.ictp.it/parallels/tuesday/F-theory(B)/zoccarato.pdf))

* {#Vafa15} [[Cumrun Vafa]], _Reflections on F-theory_, 2015 (<a href="http://f-theory15.mpp.mpg.de/talks/Vafa.pdf">pdf</a>)


### In Connes-Lott models

Discussion of GUTs within [[Connes-Lott models]]:

* {#ChamseddineConnesMukhanov14} [[Ali Chamseddine]], [[Alain Connes]], Viatcheslav Mukhanov, _Quanta of Geometry: Noncommutative Aspects_, Phys. Rev. Lett. 114 (2015) 9, 091302 ([arXiv:1409.2471](https://arxiv.org/abs/1409.2471))

* {#ChamseddineConnesMukhanov14} [[Ali Chamseddine]], [[Alain Connes]], Viatcheslav Mukhanov, _Geometry and the Quantum: Basics_, JHEP 12 (2014) 098 ([arXiv:1411.0977](https://arxiv.org/abs/1411.0977))

* {#Connes17} [[Alain Connes]], section 4 of _Geometry and the Quantum_, in _Foundations of Mathematics and Physics One Century After Hilbert_, Springer 2018. 159-196 ([arXiv:1703.02470](https://arxiv.org/abs/1703.02470), [doi:10.1007/978-3-319-64813-2](https://www.springer.com/gp/book/9783319648125))


### Exotica: Leptoquarks, $Z'$-bosons, etc.


Topological defects can play considerable role to constrain the non-SUSY and SUSY GUTs:

* Joydeep Chakrabortty, Rinku Maji, Sunando Kumar Patra, Tripurari Srivastava, Subhendra Mohanty, _Roadmap of left-right models based on GUTs_ 
([arXiv:1711.11391] (https://arxiv.org/abs/1711.11391), Phys.Rev. D97 (2018) no.9, 095010.)


Relation to [[Z'-bosons]]:

* {#Sahoo06} S. Sahoo, _The prediction of mass of $Z'$-boson in an $SO(10)$-based model_, Indian J. Phys. 80 (2), 191-194 (2006) ([pdf](http://arxiv.iacs.res.in:8080/jspui/bitstream/10821/6019/1/The%20Prediction%20of%20Mass%20of%20Z%27-Boson_By%20S%20Sahoo.pdf))


Relation to [[leptoquarks]] and [[flavour anomalies]]:

* {#MurayamaYanagida92} H. Murayama, T. Yanagida, _A viable $SU(5)$ GUT with light leptoquark bosons_, Mod.Phys.Lett. A7 (1992) 147-152 ([arXiv:315898](inspirehep.net/record/315898), [doi:10.1142/S0217732392000070](https://doi.org/10.1142/S0217732392000070))

* {#BDFKFS18} Damir Bečirević, Ilja Doršner, Svjetlana Fajfer, Nejc Košnik, Darius A. Faroughy, Olcyr Sumensari, _Scalar leptoquarks from GUT to accommodate the $B$-physics anomalies_, Phys. Rev. D 98, 055003 (2018) ([arXiv:1806.05689](https://arxiv.org/abs/1806.05689))

* {#AMM19} Ufuk Aydemir, Tanumoy Mandal, Subhadip Mitra, _A single TeV-scale scalar leptoquark in SO(10) grand unification and B-decay anomalies_ ([arXiv:1902.08108](https://arxiv.org/abs/1902.08108))

* {#HeekTeresi18} Julian Heeck, Daniele Teresi, _Pati-Salam explanations of the B-meson anomalies_, JHEP 12 (2018) 103 ([arXiv:1808.07492](https://arxiv.org/abs/1808.07492))

* {#HeekTeresi19} Julian Heeck, Daniele Teresi, _Pati-Salam and lepton universality in B decays_ ([arXiv:1905.05211](https://arxiv.org/abs/1905.05211))

* {#Malinsky19} [[Michal Malinský]], _Lepton non-universality in $B$-decays in the minimal leptoquark gauge model_ ([arXiv:1906.09174](https://arxiv.org/abs/1906.09174))

* Shyam Balaji, Michael A. Schmidt, _A unified $SU(4)$ theory for the $R_D^{(\ast)}$ and $R_K^{(\ast)}$ anomalies_ ([arXiv:1911.08873](https://arxiv.org/abs/1911.08873))






[[!redirects GUTs]]
[[!redirects grand unified theory]]
[[!redirects grand unified theories]]

[[!redirects grand unified field theory]]
[[!redirects grand unified field theories]]


[[!redirects Grand Unified Theory]]

[[!redirects grand unification]]
[[!redirects grand unifications]]

[[!redirects Pati-Salam model]]
[[!redirects Pati-Salam models]]

[[!redirects Pati-Salam GUT model]]
[[!redirects Pati-Salam GUT models]]


[[!redirects GUT scale]]

[[!redirects GUT model]]
[[!redirects GUT models]]


