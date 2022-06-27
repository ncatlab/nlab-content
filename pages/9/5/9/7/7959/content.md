
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


# Contents #
* table of contents
{:toc}


## Idea

_String phenomenology_ is [[phenomenology]] in [[particle physics]] and [[cosmology]] based on [[model (in particle physics)|models]] that are derived or at least motivated from [[string theory]] (as [[effective QFTs]] from string [[vacua]]).

Broadly speaking, _string phenomenology_ refers to investigations of the connection of [[string theory]] to experimentally observed [[physics]]. More restrictively it refers to constructions of string theory [[vacua]] whose [[effective field theory]] reproduces the [[standard model of particle physics]] and/or the [[standard model of cosmology]].

String theory models naturally match the _general_ conceptual structure of the [[standard model of particle physics]] plus [[gravity]] (which is what drives the interest in string theory in the first place): for instance the standard model is a four dimensional [[QFT]] with a [[gauge theory|non-Abelian gauge symmetry]], several [[family of elementary particles|families]] of [[chiral fermions]] and hierarchical [[Yukawa couplings]] -- and the same is true for the generic [[Kaluza-Klein mechanism|compactification]] of the [[effective QFT]] that describes [[heterotic string theory]] on a 6-dimensional compact space ([CHSW85](#CHSW85)) as well as for [[11-dimensional supergravity]]/[[M-theory]] compactified on a [[G2-manifold]] ([AW01](#AW01)).

This structure alone already implies a variety of 3-body decays of the heavier fermions into the lighter ones and the existence of massive [[vector bosons]] coupling to [[charged currents]], which in the observed [[standard model of particle physics]] are the [[W-boson]], etc. (See section III of [AKK12](#AKK12) for an exposition.)

Therefore it is not hard to find string theory compactifications that resemble the observed particle physics in _broad_ strokes. Under some simplifying assumptions many string models have been built that very closely resemble also the fine-structure of the standard model. 

A central technical issue with string [[model (in particle physics)|model building]] is that of the [[Kaluza-Klein mechanism]] involved: the [[moduli stabilization]]. Historically there had been the hope that the consistency condition of moduli stabilization on string models is so strong that it strongly reduces the number of models that look like the standard model. Arguments that the number is still "not small" even with various extra assumptions lead to the term of a [[landscape of string theory vacua|landscape]] ([[moduli space]]) of string theory models, which remains, however, poorly understood. Arguments for properties of low-energy [[effective QFTs]] that rule out a possible string-theoretic model have been brought forward for instance in ([Vafa05](http://arxiv.org/abs/hep-th/0509212)). A review of what is known about the space of possibilities is in ([Taylor11](#Taylor11)).

While all this remains poorly understood, a noteworthy difference of string phenomenology to [[model (in particle physics)|model building]] in bare [[QFT]] is that a) there is a larger framework at all in which to search for models and b) with every model automatically comes a [[UV-completion]], which is the basic motivation for embedding the standard model of particle physics in a broader theory of [[quantum gravity]] in the first place. 

A good account of what it means to have a realistic string theory model and what the subtleties are, and in which sense they have already been found abundantly or not at all, is in the introduction of ([Dolan-Krippendorf-Quevedo](#DolanKrippendorfQuevedo11)).

## Top-down models and bottom-up models
 {#TopDownAndBottomUpModels}

Since a realistic string theoretic model is, by design, a unification of the [[standard model of particle physics]] with [[quantum gravity]] aspects and hence  at least with aspects of the [[standard model of cosmology]], there are more constraints on such a model than are usually imposed on model building in particle physics alone: the model is not only supposed to reproduce the [[fundamental particle]] content but also address [[moduli stabilization]], the [[cosmological constant]] and [[dark matter]] (see e.g. [Dolan-Krippendorf-Quevedo 11, p. 3](#DolanKrippendorfQuevedo11)).

Accordingly one strategy to build models is to first aim for the correct fundamental particle content, and then incrementally adjust to account for the global gravitational constraints. For instance in [type II intersecting brane models](#ModelsInTypeIIWithIntersectingBranes) people often consider just an [[open neighbourhood]] of a singular point in a [[Kaluza-Klein mechanism|KK-compactification space]], adjust the model there, and then later ask about embedding this local construction into an actually globally defined compactification space (typically a [[Calabi-Yau manifold]] for compactifications aiming for $N=1$ low energy supersymmetry in the effective 4d model).

This approach is known as the **[[bottom-up model building|bottom-up approach]]** to string model building ([AIQU 00](#AIQU00)).

Contrary to this is the historically older **[[top-down model building|top-down approach]]** (usually attributed to ([Candelas-Horowitz-Strominger-Witten 85](#CHSW85))) in the [[heterotic string theory]] compactification models (see [below](#HeteroticStandardModels)).

## Semi-realistic models in string theory
 {#SemiRealisticModels}

Examples of [[model (in particle physics)|models]] in string phenomenology include

* _[Models in heterotic string theory](#HeteroticStandardModels)_

* _[Models in type II string theory with intersecting branes](#ModelsInTypeIIWithIntersectingBranes)_

* _[Models in M-theory](#ModelsInMTheory)_

See at _[References - Models](#ReferencesModels)_ below.

### Models in heterotic string theory
 {#HeteroticStandardModels}

The models in [[heterotic string theory]] follow the historically original and hence oldest strategy of finding semi-realistic [[GUT]] models in string theory (see ([Witten 02](#Witten02)) for a brief list of motivations for these models): one considers a [[Kaluza-Klein compactification]] of [[heterotic string theory]]/[[heterotic supergravity]] on a [[closed manifold]] of dimension 6 with a non-trivial [[gauge field]] configuration on it. By choosing different values of the [[holonomy]] of this gauge field around non-trivial [[singular homology|singular 1-cycles]] in the compact space (usually referred to as "[[Wilson lines]]" in this context) one obtains different [[effective quantum field theory|effective physics]] in the remaining 4-dimensional space.

Since most of string model building was aimed for reproducing the minimally [[supersymmetry|supersymmetric]] extension of the [[standard model of particle physics]], these approaches usually take that compact 6-manifold to be a complex 3-dimensional [[Calabi-Yau manifold]].

In more detail, the paradigm of this approach is compactification of
the [[E8]]$\times$ [[E8]] [[heterotic string theory]] on a [[Calabi-Yau manifold]] of [[Euler characteristic]] $\chi = \pm 6$, leading to a three-generation [[E6]]-model. Further gauge [[spontaneous symmetry breaking]] may be achieved e.g. by
the addition of [[Wilson lines]] and a final breakdown of $D = 4$, $N = 1$ supersymmetry is assumed to take place due to some field-theoretical [[non-perturbative effects]].

See at _[References - Models in heterotic string theory](#ReferencesHeteroticModels)_

The lift of these heterotic CY3-compactifications to [[M-theory]] is _[[M-theory on G2-manifolds]]_, discussed [below](#ModelsInMTheory).

### Models in type II string theory / F-theory
 {#ModelsInTypeIIWithIntersectingBranes}

In contrast to the construction of "heterotic standard models" [above](#HeteroticStandardModels), which are basically plain variants of the old [[Kaluza-Klein compactification]] mechanism where the effective [[gauge fields]] in 4-dimensional [[spacetime]] arise as components of the field of [[gravity]] in higher dimensions, in [[type II string theory]] with [[D-branes]] there are [[open strings]] whose massless excitations yield [[gauge fields]] "directly". The precise nature of these gauge fields and their couplings depends on the precise [[boundary conditions]] of these open strings, hence on the choice of [[D-branes]] that they end on.

Therefore in what are called "[[intersecting D-brane models]]" one considers [[Kaluza-Klein compactifications]] of [[type II string theory]] with [[D-branes]] that [[brane intersection|intersect]] in an intricate pattern in the compactification space. By choosing this [[brane intersection|intersection]] geometry suitably, one obtains various different realizations of [[gauge theory]] in the [[effective field theory|effective]] 4-dimensional physics. 

The [[intersecting branes]] of main relevance in [[type IIA string theory]] are [[D6-branes]] (e.g. [L&#252;st 04](#Lust04), [Ibanez-Uranga 12, section 10](#IbanezUranga12)), which, under [[T-duality]], correspond in [[type IIB string theory|type IIB]] to [[D7-branes]]. These are precisely the ones whose lift to [[M-theory]] correspond to [[conifold]]/[[ADE orbifold]] [[singularities]] of [[KK-monopoles]], see also at _[[F-branes -- table]]_.

One way to neatly reorganize the required data for such type II compactifications is to formulate them in terms of "[[F-theory]]", which is why some of this type II model building now goes by names like "F-theory phenomenology" or similar.

The [[moduli stabilization]] in these type of models can be achieved by choosing the various [[RR-field]] and [[B-field]] [[field strength]] (the "fluxes") on the compactification space such that its [[curvature]] forms have certain specified [[periods]] on non-trivial [[singular cohomology|singular cycles]] of the compactification space. See ([Denef 08](#Denef08)) for introduction and review of such type IIB [[flux compactification]].

Since there are only finitely many -- but many -- such choices, it is in this context that people first tried to count the number of possibilities of building models (under all these assumptions, though) and found these large finite numbers such as the meanwhile proverbial number $10^{500}$ (coming from an estimate of the number of non-trivial cycles in a generic Calabi-Yau and the number of choices of periods of the "flux" fields) which then led them to speak of the "[[landscape of string theory vacua]]". (Which of course without making a bunch of assumptions is vastly bigger, even.)

Due to the relation between [[supersymmetry and Calabi-Yau manifolds]], of particular interest is the case of [[F/M-theory on elliptically fibered Calabi-Yau 4-folds]], see there for more.

For references see below at _[References - Models in type II string theory](#ReferencesTypeIIModels)_

#### Computer scan of Gepner-model compactifications
 {#ComputerScanOfGepnerModelCompactifications}

Discussion of [[string phenomenology]] of [[intersecting D-brane models]] [[KK-compactification|KK-compactified]] with non-geometric [[fibers]] such that the would-be string [[sigma-models]] with these [[target spaces]] are in fact [[Gepner models]] (in the sense of _[Spectral Standard Model and String Compactifications](https://www.physicsforums.com/insights/spectral-standard-model-string-compactifications/)_) is in ([Dijkstra-Huiszoon-Schellekens 04a](#DijkstraHuiszoonSchellekens04a), [Dijkstra-Huiszoon-Schellekens 04b](#DijkstraHuiszoonSchellekens04b)):


<center>
<img src="https://ncatlab.org/nlab/files/SchellekensSuperGepnerModelScanII.jpg" width="600">
</center>

>  A plot of [[standard model of particle physics|standard model]]-like [[coupling constants]] in a computer scan of [[Gepner model]]-[[KK-compactification]] of [[intersecting D-brane models]] according to [Dijkstra-Huiszoon-Schellekens 04b](#DijkstraHuiszoonSchellekens04b). 

>  The blue dot indicates the couplings in $SU(5)$-[[GUT]] theory. The faint lines are NOT drawn by hand, but reflect increased density of Gepner models as seen by the computer scan.



### Models in M-theory
 {#ModelsInMTheory}

The lift of the [heterotic models](#HeteroticStandardModels) compactified on [[Calabi-Yau manifolds]] to  [[11-dimensional supergravity]] with some of its "[[M-theory]]"-corrections taken into account is _[[M-theory on G2-manifolds]], hence M-theory  [[Kaluza-Klein compactification|KK-compactified]] on [[G2-manifolds]] (or rather: [[orbifolds]]) of, necessarily, [[dimension]] 7. 

Accordingly, models in this context go by the name _[[G2-MSSM]]_.

See at _[References - Models in M-theory](#ReferencesMTheoryModels)_.

### Non-supersymmetric models
 {#NonsusyModels}

All of the above models aim for $N = 1$ [[supersymmetry]] in the low-energy [[effective field theory]], because it was a wide-spread thought that this is what describes the observable world at [[electroweak symmetry breaking]]-scale. However, new experimental results at the [[LHC]] make this low energy supersymmetry scenario increasingly unlikely (even if not fully ruled out yet). Accordingly people start to look for string models now that do not display low energy supersymmetry (of course all of them have high energy local supersymmetry, in that they are theories of [[supergravity]]).

See for instance ([MRS 09](#MRS09)) and citations given there.


## Related concepts

* [[string inspired model]]

* [string theory FAQ -- Is string theory testable?](string+theory+FAQ#IsStringTheoryTestable)

* [string theory FAQ - Did string theory provide any insight relevant in experimental particle physics?](string+theory+FAQ#InsightInParticlePhysics)

* [[Brandenberger-Vafa mechanism]]


## References

### Surveys

Useful broad survey is in 

* Fernando Marchesano, _String phenomenology today_, talk at _[StringPheno14](http://stringpheno2014.ictp.it)_ ([pdf](https://indico.cern.ch/event/366801/contributions/1784430/attachments/729154/1000461/MarchesanoHEP.pdf))

Technical surveys on particle physics string phenomenology include

* {#Nilles04} [[Hans-Peter Nilles]], _String phenomenology_ (2004) ([pdf](http://www.th.physik.uni-bonn.de/nilles/db/HPtalks/1204desy.pdf))

* [[Ralph Blumenhagen]], Boris Kors, [[Dieter Lüst]], Stephan Stieberger, _Four-dimensional String Compactifications with D-Branes, Orientifolds and Fluxes_, Phys.Rept.445:1-193,2007 ([arXiv:hep-th/0610327](http://arxiv.org/abs/hep-th/0610327))


* {#DouglasEtAl07} [[Michael Douglas]] et. al. (eds.), _[[String theory and the real world]]_, Les Houches  Session LXXXVII 2007

* Tatsuo Kobayashi, _String phenomenology_ 2009 ([pdf slides](http://www-tap.scphys.kyoto-u.ac.jp/sc2/Kobayashi.pdf))


* [[Washington Taylor]], _TASI Lectures on Supergravity and String Vacua in Various Dimensions_ ([arXiv:1104.2051](http://arxiv.org/abs/1104.2051))

* {#AKK12} [[Bobby Acharya]], [[Gordon Kane]], [[Piyush Kumar]], _Compactified String Theories -- Generic Predictions for Particle Physics_ ([arXiv:1204.2795](http://arxiv.org/abs/1204.2795))

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

 
* {#Wijnholt14} [[Martin Wijnholt]], _String compactification_, [PITP 2014](https://pitp2014.ias.edu) lecture notes ([[WijnholtCompactification14.pdf:file]], [slides for lecture 1](https://static.ias.edu/pitp/2014/sites/pitp2014.ias.edu/files/PITP2014_P3_wijnholt.pdf), [slides for lecture 2](https://static.ias.edu/pitp/2014/sites/pitp2014.ias.edu/files/PITP2014_P2_wijnholt.pdf), [slides for lecture 3](https://static.ias.edu/pitp/2014/sites/pitp2014.ias.edu/files/PITP2014_P3_wijnholt.pdf))

* [[Eran Palti]], _Review of Model Building in String Theory_, talk at [String Phenomenology 2014](http://stringpheno2014.ictp.it/program.html) ([pdf](http://stringpheno2014.ictp.it/lecturenotes/Palti.pdf))

Technical surveys on cosmological string phenomenology include

* S. F. King, J. P. Roberts, _Natural Dark Matter from Type I String Theory_ ([arXiv:hep-ph/0608135](http://arxiv.org/abs/hep-ph/0608135))

The "[[bottom-up model building|bottom-up approach]]" to string model building is attributed to

* {#AIQU00} G. Aldazabal, [[Luis Ibáñez]], F. Quevedo, [[Angel Uranga]], _D-Branes at Singularities : A Bottom-Up Approach to the String Embedding of the Standard Model_, JHEP 0008:002 2000 ([arXiv:hep-th/0005067](http://xxx.lanl.gov/abs/hep-th/0005067))
 
See also

* [[Hans-Peter Nilles]], Patrick K.S. Vaudrevange, _Geography of Fields in Extra Dimensions: String Theory Lessons for Particle Physics_, Perspectives on String Phenomenology" (World Scientific) ([arXiv:1403.1597](http://arxiv.org/abs/1403.1597))

For [[Gepner models]]:

* Christian Reppel, _Phenomenological Aspects of Gepner Models_, 2007 ([pdf](https://www.ru.nl/publish/pages/760962/christiaan_reppel.pdf))


### Original articles

* {#CHSW85} [[Philip Candelas]], [[Gary Horowitz]], [[Andrew Strominger]], [[Edward Witten]], _Vacuum configurations for superstrings_, Nuclear Physics B Volume 258, 1985, Pages 46-74 Nucl. Phys. B 258, 46 (1985) (<a href="https://doi.org/10.1016/0550-3213(85)90602-9">doi:10.1016/0550-3213(85)90602-9</a>)


 
* {#AW01} [[Bobby Acharya]], [[Edward Witten]], _Chiral Fermions from Manifolds of $G_2$ Holonomy_ ([arXiv:hep-th/0109152](http://arxiv.org/abs/hep-th/0109152))
 

* [[Cumrun Vafa]], _The String Landscape and the Swampland_ ([arXiv:hep-th/0509212](http://arxiv.org/abs/hep-th/0509212))




[[!include heterotic string phenomenology -- references]]





### Further Models
 {#ReferencesModels}



#### Type II string theory models
 {#ReferencesTypeIIModels}

The canonical textbook for [[type II superstring]] phenomenology via [[intersecting D-brane models]] is 

* [Ibanez-Uranga 12](#IbanezUranga12)

The [[bottom-up model building|bottom-up]] [[intersecting D-brane model building]] originates with

* [Aldazabal-Ibáñez-Quevedo-Uranga 00](#AIQU00)

See also

* {#Denef08} [[Frederik Denef]], _Les Houches Lectures on Constructing String Vacua_, in _[[String theory and the real world]]_ ([arXiv:0803.1194](http://arxiv.org/abs/0803.1194))

Reviews of [[intersecting D-brane model]] in [[type II string theory]] (in [[orientifold]] [[flux compactifications]]) include

* {#Lust04} [[Dieter Lüst]], _Intersecting Brane Worlds -- A Path to the Standard Model ?_, Class. Quant. Grav.21 : S1399-1424, 2004 ([arXiv:hep-th/0401156](http://arxiv.org/abs/hep-th/0401156))

* [[Ralph Blumenhagen]], [[Volker Braun]], Boris Kors, [[Dieter Lüst]], _The Standard Model on the Quintic_, Summary of Talks at SUSY02, 1st Intl. Conference on String Phenomenology in Oxford, Strings 2002 and 35th Ahrenshoop Symposium. ([arXiv:hep-th/0210083](http://arxiv.org/abs/hep-th/0210083))

* [[Ralph Blumenhagen]], [[Mirjam Cvetic]], Paul Langacker, [[Gary Shiu]], _Towards Realistic Intersecting D-Brane Models_, Ann.Rev.Nucl.Part.Sci.55:71-139, 2005 ([arXiv:hep-th/0502005](http://arxiv.org/abs/hep-th/0502005))

* Ching-Ming Chen, Tianjun Li, Dimitri V. Nanopoulos, _Standard-Like Model Building on Type II Orientifolds_, Nucl.Phys.B732:224-242,2006 ([arXiv:hep-th/0509059](http://arxiv.org/abs/hep-th/0509059))


* [[Angel Uranga]], _The standard model from D-branes in string theory_, talk at Padova, January 2008 ([pdf](http://active.pd.infn.it/g4/seminars/2008/files/uranga.pdf))

* {#DolanKrippendorfQuevedo11} Matthew J. Dolan, Sven Krippendorf, Fernando Quevedo, _Towards a Systematic Construction of Realistic D-brane Models on a del Pezzo Singularity_, JHEP 1110 (2011) 024 ([arXiv:1106.6039](http://arxiv.org/abs/1106.6039))
 
* Anshuman Maharana, [[Eran Palti]], _Models of Particle Physics from Type IIB String Theory and F-theory: A Review_ ([arXiv:1212.0555](http://arxiv.org/abs/1212.0555))

Computer scan of [[Gepner model]]-[[KK-compactifications]] of [[intersecting D-brane models]]:

* {#DijkstraHuiszoonSchellekens04a} T.P.T. Dijkstra, L. R. Huiszoon, [[Bert Schellekens]], _Chiral Supersymmetric Standard Model Spectra from Orientifolds of Gepner Models_, Phys.Lett. B609 (2005) 408-417 ([arXiv:hep-th/0403196](https://arxiv.org/abs/hep-th/0403196))

* {#DijkstraHuiszoonSchellekens04b} T.P.T. Dijkstra, L. R. Huiszoon, [[Bert Schellekens]], _Supersymmetric Standard Model Spectra from RCFT orientifolds_, Nucl.Phys.B710:3-57,2005 ([arXiv:hep-th/0411129](https://arxiv.org/abs/hep-th/0411129))

Computer scan of [[toroidal orbifold]]-[[KK-compactification]] of [[intersecting D-brane models]]:

* [[Ralph Blumenhagen]], [[Florian Gmeiner]], [[Gabriele Honecker]], [[Dieter Lüst]], [[Timo Weigand]], _The Statistics of Supersymmetric D-brane Models_, Nucl.Phys.B713:83-135, 2005 ([arXiv:hep-th/0411173](https://arxiv.org/abs/hep-th/0411173))

* {#GBHLW05} [[Florian Gmeiner]], [[Ralph Blumenhagen]], [[Gabriele Honecker]], [[Dieter Lüst]], [[Timo Weigand]], _One in a Billion: MSSM-like D-Brane Statistics_, JHEP 0601:004, 2006 ([arXiv:hep-th/0510170](https://arxiv.org/abs/hep-th/0510170))

Realistic [[Yukawa couplings]] and [[fermion]] [[masses]] in an [[MSSM]] [[Pati-Salam GUT model]] with 3 [[generations of fermions]] realized on [[intersecting D-brane model|intersecting]] [[D6-branes]] [[KK-compactification|KK-compactified]] on a [[toroidal orbifold]] $T^6\sslash (\mathbb{Z}_2 \times \mathbb{Z}_2)$ are claimed in

* {#ChenLiMayesNanopoulos07a} Ching-Ming Chen, Tianjun Li, [[Van Eric Mayes]], [[Dimitri Nanopoulos]], _A Realistic World from Intersecting D6-Branes_, Phys.Lett.B665:267-270, 2008 ([arXiv:hep-th/0703280](https://arxiv.org/abs/hep-th/0703280), [doi:10.1016/j.physletb.2008.06.024](https://doi.org/10.1016/j.physletb.2008.06.024))

* {#ChenLiMayesNanopoulos07b} Ching-Ming Chen, Tianjun Li, [[Van Eric Mayes]], [[Dimitri Nanopoulos]], _Realistic Yukawa Textures and SUSY Spectra from Intersecting Branes_, Phys.Rev.D77:125023, 2008 ([arXiv:0711.0396](https://arxiv.org/abs/0711.0396))

* {#Mayes19} [[Van Eric Mayes]], _All Fermion Masses and Mixings in an Intersecting D-brane World_ ([arXiv:1902.00983](https://arxiv.org/abs/1902.00983))

* {#GemillHowingtonMayes19} Jordan Gemmill, Evan Howington, [[Van Eric Mayes]], _One String to Rule Them All: Neutrino Masses and Mixing Angles_ ([arXiv:1907.07106](https://arxiv.org/abs/1907.07106))

* Tianjun Li, Adeel Mansha, Rui Sun, _Revisiting the Supersymmetric Pati-Salam Models from Intersecting D6-branes_ ([arXiv:1910.04530](https://arxiv.org/abs/1910.04530))

* Tianjun Li, Adeel Mansha, Rui Sun, _Generalized Supersymmetric Pati-Salam Models from Intersecting D6-branes_ ([arXiv:1912.11633](https://arxiv.org/abs/1912.11633))

See also

* Erik Parr, Patrick K.S. Vaudrevange, Martin Wimmer, _Predicting the orbifold origin of the MSSM_ ([arXiv:2003.01732](https://arxiv.org/abs/2003.01732))


#### Type I string theory model
 {#ReferencesTypeIStringTheorymodels}

Discussion for [[type I string theory]]:

* {#MMRB86} H.S. Mani, A. Mukherjee, R. Ramachandran, A.P. Balachandran, _Embedding of $SU(5)$ GUT in $SO(32)$ superstring theories_, Nuclear Physics B Volume 263, Issues 3–4, 27 January 1986, Pages 621-628 (<a href="https://doi.org/10.1016/0550-3213(86)90277-4">arXiv:10.1016/0550-3213(86)90277-4</a>)

* {#IbanezMunozRigolin98} [[Luis Ibáñez]], C. Muñoz, S. Rigolin, _Aspects of Type I String Phenomenology_, Nucl.Phys. B553 (1999) 43-80 ([arXiv:hep-ph/9812397](https://arxiv.org/abs/hep-ph/9812397))

* {#Dudas00} Emilian Dudas, _Theory and Phenomenology of Type I strings and M-theory_, Class. Quant. Grav.17:R41-R116, 2000 ([arXiv:hep-ph/0006190](https://arxiv.org/abs/hep-ph/0006190))

* {#Yamatsu17} Naoki Yamatsu, _String-Inspired Special Grand Unification_ ([arXiv:1708.02078](https://arxiv.org/abs/1708.02078))




#### F-Theory models

Discussion of [[GUT]] [[model (physics)|models]] via [[F-theory]] is in 

* [[Chris Beasley]], [[Jonathan Heckman]], [[Cumrun Vafa]], _GUTs and Exceptional Branes in F-theory - I_ ([arxiv:0802.3391](http://arxiv.org/abs/0802.3391)), _II: Experimental Predictions_ ([arxiv:0806.0102](http://arxiv.org/abs/0806.0102))

A direct [[geometric engineering]] of the [[MSSM]] within [[F-theory]] is claimed in 

* {#CLLO18} [[Mirjam Cvetič]], Ling Lin, Muyang Liu, Paul-Konstantin Oehlmann, _An F-theory Realization of the Chiral MSSM with $\mathbb{Z}_2$-Parity_ ([arXiv:1807.01320](https://arxiv.org/abs/1807.01320))

Discussion of the _exact_ [[gauge group]] of the [[standard model of particle physics]], $G = \big( SU(3) \times SU(2) \times U(1)\big)/\mathbb{Z}_6 $ including its $\mathbb{Z}_6$-[[quotient group|quotient]] (see [there](standard+model+of+particle+physics#GaugeGroup)) and the exact [[fermion]] field content, realized in F-theory is in

* Denis Klevers, Damian Kaloni Mayorga Pena, Paul-Konstantin Oehlmann, Hernan Piragua, Jonas Reuter, _F-Theory on all Toric Hypersurface Fibrations and its Higgs Branches_, JHEP01(2015)142 ([arXiv:1408.4808](https://arxiv.org/abs/1408.4808))

* {#CveticLin17} [[Mirjam Cvetic]], Ling Lin, section 3.3 of _The global gauge group structure of F-theory compactifications with $U(1)$s_ ([arXiv:1706.08521](https://arxiv.org/abs/1706.08521))

Based on this, a large number of realizations of the exact field content of the [[standard model of particle physics]] (or rather the [[MSSM]]) in [[F-theory]] is claimed to be realized in

* [[Mirjam Cvetic]], [[James Halverson]], Ling Lin, Muyang Liu, Jiahua Tian, _A Quadrillion Standard Models from F-theory_ ([arXiv:1903.00009](https://arxiv.org/abs/1903.00009))


* {#TaylorTurner19} [[Washington Taylor]], Andrew P. Turner, _Generic construction of the Standard Model gauge group and matter representations in F-theory_ ([arXiv:1906.11092](https://arxiv.org/abs/1906.11092))

#### M-theory models
 {#ReferencesMTheoryModels}

A comprehensive account on models in [[M-theory on G2-manifolds]] and the [[G2-MSSM]] is in 

* [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Jing Shao, _The $G_2$-MSSM - An $M$ Theory motivated model of Particle Physics_ ([arXiv:0801.0478](http://arxiv.org/abs/0801.0478))

* [[Bobby Acharya]], [[Gordon Kane]], [[Piyush Kumar]], _Compactified String Theories -- Generic Predictions for Particle Physics_,  Int. J. Mod. Phys. A, Volume 27 (2012) 1230012 ([arXiv:1204.2795](http://arxiv.org/abs/1204.2795))

* {#Kane16} [[Gordon Kane]], _String/M-theories About Our World Are Testable in the traditional Physics Way_ ([arXiv:1601.07511](http://arxiv.org/abs/1601.07511), [video recording](https://videoonline.edu.lmu.de/en/node/7485))

with comments on comparison to more recent experiments in 

* [[Gordon Kane]], Ran Lu, Bob Zheng, _Review and Update of the Compactified M/string Theory Prediction of the Higgs Boson Mass and Properties_, Int. J. Mod. Phys. A Volume 28 (2013) 1330002 ([arXiv:1211.2231](http://arxiv.org/abs/1211.2231))

Original articles include

* [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Jing Shao, _Explaining the Electroweak Scale and Stabilizing Moduli in M Theory_ ([arXiv:hep-th/0701034](http://xxx.lanl.gov/abs/hep-th/0701034)) 

* [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Diana Vaman, _An M theory Solution to the Hierarchy Problem_ ([arXiv:hep-th/0606262](http://arxiv.org/abs/hepth/0606262))

* [[Bobby Acharya]], Konstantin Bobkov, _K&#228;hler Independence of the $G_2$-MSSM_, JHEP ([arXiv:0810.3285](http://arxiv.org/abs/0810.3285))

See also

* {#Anderson08} [[Lara Anderson]], _Heterotic and M-theory Compactifications for String Phenomenology_ ([arXiv:0808.3621](https://arxiv.org/abs/0808.3621))

Alternatively, discussion in [[Hořava-Witten theory]]:

* {#Ovrut18} [[Burt Ovrut]], _Vacuum Constraints for Realistic Heterotic M-Theories_ ([arXiv:1811.08892](https://arxiv.org/abs/1811.08892))


#### Heterotic M-theory models

Discussion in [[heterotic M-theory]]:

* {#DOPW99} [[Ron Donagi]], [[Burt Ovrut]], [[Tony Pantev]], [[Daniel Waldram]], _Standard Models from Heterotic M-theory_, Adv. Theor. Math. Phys. 5 (2002) 93-137 ([arXiv:hep-th/9912208](https://arxiv.org/abs/hep-th/9912208))

* {#DOPW00} [[Ron Donagi]], [[Burt Ovrut]], [[Tony Pantev]], [[Daniel Waldram]], _Standard Model Vacua in Heterotic M-Theory_, talk at [Strings '99](http://strings99.aei.mpg.de/), Potsdam, Germany, 19 - 24 Jul 1999 ([arXiv:hep-th/0001101](https://arxiv.org/abs/hep-th/0001101))

and with emphasis on [[heterotic line bundle]]-models:

* [[Sebastian Dumitru]], *The strongly coupled $E_8 \times E_8$ heterotic string: Geometry & Phenomenology* &lbrack;[arXiv:2206.12310](https://arxiv.org/abs/2206.12310)&rbrack;


#### Non-supersymmetric models

A survey of string model buidling without low energy susy is in 

* [[Emil Martinec]], Daniel Robbins, Savdeep Sethi, _Non-Supersymmetric String Theory_ ([arXiv:0904.3498](http://arxiv.org/abs/0904.3498))
 {#MRS09}

An old observation on string models without low energy susy, recently re-appreciated, is

* [[Keith Dienes]], _How Strings Make Do without Supersymmetry: An Introduction to Misaligned Supersymmetry_ ([arXiv:hep-th/9409114](http://arxiv.org/abs/hep-th/9409114))

A newer observation that received much more attention is

* [[Nima Arkani-Hamed]], Savas Dimopoulos, _Supersymmetric Unification Without Low Energy Supersymmetry And Signatures for Fine-Tuning at the LHC_ ([arXiv:hep-th/0405159](http://arxiv.org/abs/hep-th/0405159))


### String Phenomenology conferences


* String Phenomenology 2002 ([home page](http://www-thphys.physics.ox.ac.uk/users/AlonFaraggi/sp2002/conference.html)) 

* String Phenomenology 2003 ([home page](http://www.ippp.dur.ac.uk/old/SP03/welcome.shtml)) 

* String Phenomenology 2004 ([home page](http://www.umich.edu/%7Emctp/SciPrgPgs/events/2004/2004sph/index.html)) 

* String Phenomenology 2005 ([home page](http://wwwth.mppmu.mpg.de/members/blumenha/main.html)) 

* String Phenomenology 2006 ([home page](http://www.kitp.ucsb.edu/activities/auto2/?id=352)) 

* String Phenomenology 2007 ([home page](http://people.roma2.infn.it/%7Estringpheno2007/)) 

* String Phenomenology 2008 ([home page](http://www.math.upenn.edu/StringPhenom2008/local.html)) 

* String Phenomenology 2009 ([home page](http://www.fuw.edu.pl/~sp09/)) 

* String Phenomenology 2010 ([home page](http://stringpheno.cpht.polytechnique.fr/)) 

* String Phenomenology 2011 ([home page](http://conferencing.uwex.edu/conferences/stringpheno2011/), [talks](http://conferencing.uwex.edu/conferences/stringpheno2011/PlenarySessions.cfm))

* String Phenomenology 2012 ([home page](http://www.newton.ac.uk/programmes/BSM/bsmw05.html), [talks](http://www.newton.ac.uk/programmes/BSM/bsmw05p.html))

* String Phenomenology 2013 ([home page](http://stringpheno2013.desy.de/))

* String Phenomenology 2014 ([home page](http://stringpheno2014.ictp.it))

* String Phenomenology 2018 ([home page](http://sp18.fuw.edu.pl/))

* String Phenomenology 2019 ([home page](https://indico.cern.ch/event/782251/))


### String cosmic inflation

In [[string theory]] the [[inflaton]] field for models of [[cosmic inflation]] field can be modeled by various effects, such as 

* [[open string]] stretching between [[D-brane]]-[[anti D-brane]] pairs.

For a review and further pointers to the literature see at

* Cliff Burgess, M. Cicoli, F. Quevedo, _String Inflation After Planck 2013_ ([arXiv:1306.3512](http://arxiv.org/abs/1306.3512))


### Axion phenomenology

On stringy [[axion]] [[phenomenology]]:

* Joseph P. Conlon, M.C. David Marsh, _Searching for a 0.1-1 keV Cosmic Axion Background_ ([arXiv:1305.3603](http://arxiv.org/abs/1305.3603))

  > Primordial decays of [[string theory]] [[moduli stabilization|moduli]] at $z \sim 10^{12}$ naturally generate a [[dark radiation]] Cosmic Axion Background (CAB) with $0.1 - 1 keV$ energies. This CAB can be detected through axion-[[photon]] conversion in astrophysical [[magnetic fields]] to give quasi-thermal excesses in the extreme ultraviolet and soft X-ray bands. Substantial and observable luminosities may be generated even for axion-photon couplings $\ll 10^{-11} GeV^{-1}$. We propose that axion-photon conversion may explain the observed excess emission of soft X-rays from galaxy clusters, and may also contribute to the diffuse unresolved cosmic X-ray background. We list a number of correlated predictions of the scenario. 



[[!redirects string phenonemology]]
[[!redirects string phenomenology]]
[[!redirects intersecting D-brane standard models]]
[[!redirects heterotic standard models]]

[[!redirects string theory phenomenology]]
