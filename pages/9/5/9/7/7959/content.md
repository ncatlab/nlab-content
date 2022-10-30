
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

# Contents
* table of contents
{: toc}

## Idea

_String phenomenology_ is [[phenomenology]] in [[particle physics]] based on [[model (in particle physics)|models]] that are derived or at least motivated from [[string theory]] (as [[effective QFTs]] from string [[vacua]]).

Broadly speaking, _string phenomenology_ refers to investigations of the connection of [[string theory]] to experimentally observed [[physics]]. More restrictively it refers to constructions of string theory [[vacua]] whose [[effective field theory]] reproduces the [[standard model of particle physics]] and/or the [[standard model of cosmology]].

String theory models natually match the _general_ conceptual structure of the [[standard model of particle physics]] plus [[gravity]] (which is what drives the interest in string theory in the first place): for instance the standard model is a four dimensional [[QFT]] with a [[gauge theory|non-Abelian gauge symmetry]], several [[family of elementary particles|families]] of [[chiral fermions]] and hierarchical [[Yukawa couplings]] -- and the same is true for the generic [[Kaluza-Klein mechanism|compactification]] of the [[effective QFT]] that describes [[heterotic string theory]] on a 6-dimensional compact space ([CHSW85](#CHSW85)) as well as for [[11-dimensional supergravity]]/[[M-theory]] compactified on a [[G2-manifold]] ([AW01](#AW01)).

This structure alone already implies a variety of 3-body decays of the heavier fermions into the lighter ones and the existence of massive [[vector bosons]] coupling to [[charged currents]], which in the observed [[standard model of particle physics]] are the [[W-boson]], etc. (See section III of [AKK12](#AKK12) for an exposition.)

Therefore it is not hard to find string theory compactifications that resemble the observed particle physics in _broad_ strokes. Under some simplifying assumptions many string models have been built that very closely resemble also the fine-structure of the standard model. 

A central technical issue with string [[model (in particle physics)|model building]] is that of the [[Kaluza-Klein mechanism]] involved: the [[moduli stabilization]]. Historically there had been the hope that the consistency condition of moduli stabilization on string models is so strong that it strongly reduces the number of models that look like the standard model. Arguments that the number is still "not small" even with various extra assumptions lead to the term of a [[landscape of string theory vacua|landscape]] ([[moduli space]]) of string theory models, which remains, however, poorly understood. Arguments for properties of low-energy [[effective QFTs]] that rule out a possibe string-theoretic model have been brought forward for instance in ([Vafa05](http://arxiv.org/abs/hep-th/0509212)). A review of what is known about the space of possibilities is in ([Taylor11](#Taylor11)).

While all this remains poorly understood, a noteworthy difference of string phenomenology to [[model (in particle physics)|model building]] in bare [[QFT]] is that a) there is a larger framework at all in which to search for models and b) with every model automatically comes a [[UV-completion]], which is the basic motivation for embedding the standard model of particle physics in a broader theory of [[quantum gravity]] in the first place. 

A good account of what it means to have a realistic string theory model and what the subtleties are, and in which sense they have already been found abundantly or not at all, is in the introduction of ([Dolan-Krippendorf-Quevedo](#DolanKrippendorfQuevedo11)).

## Top-down models and bottom-up models
 {#TopDownAndBottomUpModels}

Since a realistic string theoretic model is, by desing, a unification of the [[standard model of particle physics]] with [[quantum gravity]] aspects and hence  at least with aspects of the [[standard model of cosmology]], there are more constraints on such a model than are usually imposed on model building in particle physics alone: the model is not only supposed to reproduce the [[fundamental particle]] content but also address [[moduli stabilization]], the [[cosmological constant]] and [[dark matter]] (see e.g. [Dolan-Krippendorf-Quevedo 11, p. 3](#DolanKrippendorfQuevedo11)).

Accordingly one strategy to build models is to first aim for the correct fundamental particle content, and then incrementally adjust to account for the global gravitational constraints. For instance in [type II intersecting brane models](#ModelsInTypeIIWithIntersectingBranes) people often consider just an [[open neighbourhood]] of a singular point in a [[Kaluza-Klein mechanism|KK-compactification space]], adjust the model there, and then later ask about embedding this local construction into an actually globally defined compactification space (typically a [[Calabi-Yau manifold]] for compactifications aiming for $N=1$ low energy supersymmetry in the effective 4d model).

This approach is known as the **bottom-up approach** to string model building ([AIQU 00](#AIQU00)).

Contrary to this is the historically older **top-down approach** (usually attributed to ([Candelas-Horowitz-Strominger-Witten 85](#CHSW85))) in the [[heterotic string theory]] compactification models (see [below](#HeteroticStandardModels)).

## Semi-realistic models in string theory
 {#SemiRealisticModels}

Examples of [[model (in particle physics)|models]] in string phenomenology include

* _[Models in heterotic string theory](#HeteroticStandardModels)_

* _[Models in type II string theory with intersecting branes](#ModelsInTypeIIWithIntersectingBranes)_

* _[Models in M-theory](#ModelsInMTheory)_

See at _[References - Models](#ReferencesModels)_ below.

### Models in heterotic string theory
 {#HeteroticStandardModels}

The models in [[heterotic string theory]] follow the historically original and hence oldest strategy of finding semi-realitsic [[GUT]] models in string theory (see ([Witten 02](#Witten02)) for a brief list of motivations for these models): one considers a [[Kaluza-Klein compactification]] of [[heterotic string theory]]/[[heterotic supergravity]] on a [[closed manifold]] of dimension 6 with a non-trivial [[gauge field]] configuration on it. By choosing different values of the [[holonomy]] of this gauge field around non-trivial [[singular homology|singular 1-cycles]] in the compact space (usually referred to as "[[Wilson lines]]" in this context) one obtains different [[effective quantum field theory|effective physics]] in the remainind 4-dimensional space.

Since most of string model building was aimed for reproducing the minimally [[supersymmetry|supersymmetric]] exension of the [[standard model of particle physics]], these approaches usually take that compact 6-manifold to be a complex 3-dimensional [[Calabi-Yau manifold]].

More in detail, the paradigm of this approach compactification of
the [[E8]]$\times$ [[E8]] [[heterotic string theory]] on a [[Calabi-Yau manifold]] [[Euler characteristic]] $\chi = \pm 6$, leading to a three-generation [[E6]]-model. Further gauge [[spontaneous symmetry breaking]] may be achieved e.g. by
the addition of [[Wilson lines]] and a final breakdown of $D = 4$, $N = 1$ supersymmetry is assumed to take place due to some field-theoretical [[non-perturbative effects]].

See at _[References - Models in heterotic string theory](#ReferencesHeteroticModels)_

The lift of these heterotic CY3-compactifications to [[M-theory]] is _[[M-theory on G2-manifolds]]_, discussed [below](#ModelsInMTheory).

### Models in type II string theory / F-theory
 {#ModelsInTypeIIWithIntersectingBranes}

In contrast to the construction of "heterotic standard models" [above](#HeteroticStandardModels), which are basically plain variants of the old [[Kaluza-Klein compactification]] mechanism where the effective [[gauge fields]] in 4-dimensional [[spacetime]] arise as components of the field of [[gravity]] in higher dimensions, in [[type II string theory]] with [[D-branes]] there are [[open strings]] whose massless excitations yield [[gauge fields]] "directly". The precise nature of these gauge fields and their couplings depends on the precise [[boundary conditions]] of these open strings, hence on the choice of [[D-branes]] that they end on.

Therefore in what are called "intersecting D-brane models" one considers [[Kaluza-Klein compactifications]] of [[type II string theory]] with [[D-branes]] that intersect in an intricate pattern in the compactification space. By choosing this intersection geometry suitably, one obtains various different realizations of [[gauge theory]] in the [[effective field theory|effective]] 4-dimensional physics. 

One way to neatly reorganize the required data for such type II compactifications is to formulate them in terms of "[[F-theory]]", which is why some of this type II model building now goes by names like "F-theory phenomenology" or similar.

The [[moduli stabilization]] in these type of models can be achieved by choosing the various [[RR-field]] and [[B-field]] [[field strength]] (the "fluxes") on the compactification space such that its [[curvature]] forms have certain specified [[periods]] on non-trivial [[singular cohomology|singular cycles]] of the compactification space. See ([Denef 08](#Denef08)) for introduction and review of such type IIB [[flux compactification]].

Since there are only finitely many -- but many -- such choices, it is in this context that people first tried to count the number of possibilities of building models (under all these assumptions, though) and found these large finite numbers such as the meanwhile proverbial number $10^{500}$ (coming from an estimate of the number of non-tivial cycles in a generic Calabi-Yau and the number of choices of periods of the "flux" fields) which then led them to speak of the "[[landscape of string theory vacua]]". (Which of course without making a bunch of assumptions is vastly bigger, even.)

Due to the relation between [[supersymmetry and Calabi-Yau manifolds]], of particular interest is the case of [[F/M-theory on elliptically fibered Calabi-Yau 4-folds]], see there for more.

For references see below at _[References - Models in type II string theory](#ReferencesTypeIIModels)_


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

* [string theory FAQ -- Is string theory testable?](string+theory+FAQ#IsStringTheoryTestable)

* [string theory FAQ - Did string theory provide any insight relevant in experimental particle physics?](string+theory+FAQ#InsightInParticlePhysics)

* [[Brandenberger-Vafa mechanism]]


## References

### Surveys

Technical surveys on particle physics string phenomenology include

* {#DouglasEtAl07} [[Michael Douglas]] et. al. (eds.), _[[String theory and the real world]]_, Les Houches  Session LXXXVII 2007

* [[Hans-Peter Nilles]], _String phenomenology_ (2004) ([pdf](http://www.th.physik.uni-bonn.de/nilles/db/HPtalks/1204desy.pdf))

* Tatsuo Kobayashi, _String phenomenology_ ([pdf](http://www-tap.scphys.kyoto-u.ac.jp/sc2/Kobayashi.pdf))

* [[Washington Taylor]], _TASI Lectures on Supergravity and String Vacua in Various Dimensions_ ([arXiv:1104.2051](http://arxiv.org/abs/1104.2051))

* {#AKK12} [[Bobby Acharya]], [[Gordon Kane]], [[Piyush Kumar]], _Compactified String Theories -- Generic Predictions for Particle Physics_ ([arXiv:1204.2795](http://arxiv.org/abs/1204.2795))
 
* {#Wijhnholt14} [[Martin Wijnholt]], _String compactification_, [PITP 2014](https://pitp2014.ias.edu) lecture notes ([[WijnholtCompactification14.pdf:file]], [slides for lecture 1](https://pitp2014.ias.edu/sites/pitp2014.ias.edu/files/PITP2014_P1_wijnholt.pdf), [slides for lecture 2](https://pitp2014.ias.edu/sites/pitp2014.ias.edu/files/PITP2014_P2_wijnholt.pdf), [slides for lecture 3](https://pitp2014.ias.edu/sites/pitp2014.ias.edu/files/PITP2014_P3_wijnholt.pdf))

* E. Palti _Review of Model Building in String Theory_, talk at [String Phenomenology 2014](http://stringpheno2014.ictp.it/program.html) ([pdf](http://stringpheno2014.ictp.it/lecturenotes/Palti.pdf))

Technical surveys on cosmological string phenomenology include

* S. F. King, J. P. Roberts, _Natural Dark Matter from Type I String Theory_ ([arXiv:hep-ph/0608135](http://arxiv.org/abs/hep-ph/0608135))

The "bottom-up approach" to string model building is attributed to

* {#AIQU00} G. Aldazabal, L. E. Ibanez, F. Quevedo, [[Angel Uranga]], _D-Branes at Singularities : A Bottom-Up Approach to the String Embedding of the Standard Model_, JHEP 0008:002 2000 ([arXiv:hep-th/0005067](http://xxx.lanl.gov/abs/hep-th/0005067))
 
See also

* [[Hans-Peter Nilles]], Patrick K.S. Vaudrevange, _Geography of Fields in Extra Dimensions: String Theory Lessons for Particle Physics_, Perspectives on String Phenomenology" (World Scientific) ([arXiv:1403.1597](http://arxiv.org/abs/1403.1597))

### Original articles

* {#CHSW85} [[Philip Candelas]], [[Gary Horowitz]], [[Andrew Strominger]], [[Edward Witten]], Nucl. Phys. B 258, 46 (1985)
 
 
* {#AW01} [[Bobby Acharya]], [[Edward Witten]], _Chiral Fermions from Manifolds of $G_2$ Holonomy_ ([arXiv:hep-th/0109152](http://arxiv.org/abs/hep-th/0109152))
 

* [[Cumrun Vafa]], _The String Landscape and the Swampland_ ([arXiv:hep-th/0509212](http://arxiv.org/abs/hep-th/0509212))

### Models
 {#ReferencesModels}

#### Heterotic models
 {#ReferencesHeteroticModels}

The origin of all [[heterotic string theory]] models and the "top down approach" of string model building is ([CHSW 85](#CHSW85))

A brief review of motivations for [[GUT]] models in heterotic string theory is in 

* [[Edward Witten]], _Quest For Unification_, Heinrich Hertz lecture at [SUSY 2002](http://www.desy.de/susy02/) at DESY, Hamburg ([arXiv:hep-ph/0207124](http://arxiv.org/abs/hep-ph/0207124))
 {#Witten02}

The following articles are usually regarded as the first semi-realistic approximations to the [[MSSM]] realized in [[heterotic string theory]]:

* Vincent Bouchard, Ron Donagi, _An SU(5) Heterotic Standard Model_, Phys. Lett. B633:783-791,2006 ([arXiv:hep-th/0512149](http://arxiv.org/abs/hep-th/0512149))

* [[Volker Braun]], Yang-Hui He, [[Burt Ovrut]], [[Tony Pantev]], _A Heterotic Standard Model_,  	Phys. Lett. B618 : 252-258 2005 ([arXiv:hep-th/0501070](http://arxiv.org/abs/hep-th/0501070))

* [[Volker Braun]], Yang-Hui He, [[Burt Ovrut]], [[Tony Pantev]], _The Exact MSSM Spectrum from String Theory_, JHEP 0605:043,2006 ([arXiv:hep-th/0512177](http://arxiv.org/abs/hep-th/0512177))

This "heterotic standard model" has a "hidden sector" copy of the actual standard model, more details of which are discussed here:

* [[Volker Braun]], Yang-Hui He, [[Burt Ovrut]], _Supersymmetric Hidden Sectors for Heterotic Standard Models_ ([arXiv:1301.6767](http://arxiv.org/abs/1301.6767))

More such "heterotic standard models" are discussed in the following articles, which aim for an "algorithmic" way of scanning the space of all semi-realistic heterotic compactifications, subject to some constraints.

A survey is here:

* [[Lara Anderson]], _New aspects of heterotic geometry and phenomenology_, talk at String2012, Munich 2012 ([pdf](http://wwwth.mpp.mpg.de/members/strings/strings2012/strings_files/program/Talks/Wednesday/Anderson.pdf))

Original articles in this program include


* [[Lara Anderson]], James Gray, Andre Lukas, Eran Palti, _Two Hundred Heterotic Standard Models on Smooth Calabi-Yau Threefolds_ ([arXiv:1106.4804](http://arxiv.org/abs/1106.4804))

* [[Lara Anderson]], James Gray, Andre Lukas, Eran Palti, _Heterotic Line Bundle Standard Models_ ([arXiv:1202.1757](http://arxiv.org/abs/1202.1757))

* [[Lara Anderson]], James Gray, Andre Lukas, Eran Palti, _Heterotic standard model database_ ([web](http://www-thphys.physics.ox.ac.uk/projects/CalabiYau/linebundlemodels/index.html.))

The issue of [[moduli stabilization]] in these kinds of models is discussed in 

* Michele Cicoli, Senarath de Alwis, Alexander Westphal, _Heterotic Moduli Stabilization_ ([arXiv:1304.1809](http://arxiv.org/abs/1304.1809))

* [[Lara Anderson]], James Gray, Andre Lukas, Burt Ovrut, _Vacuum Varieties, Holomorphic Bundles and Complex Structure Stabilization in Heterotic Theories_ ([arXiv:1304.2704](http://arxiv.org/abs/1304.2704))

List of models are discussed in 

* Yang-Hui He, Seung-Joo Lee, Andre Lukas, Chuang Sun, _Heterotic Model Building: 16 Special Manifolds_ ([arXiv:1309.0223](http://arxiv.org/abs/1309.0223))

#### Type II / F-theory models
 {#ReferencesTypeIIModels}

* {#Denef08} [[Frederik Denef]], _Les Houches Lectures on Constructing String Vacua_, in _[[String theory and the real world]]_ ([arXiv:0803.1194](http://arxiv.org/abs/0803.1194))

Reviews of intersecting [[D-brane]] models in [[type II string theory]] (in [[orientifold]] [[flux compactifications]]) include

* [[Ralph Blumenhagen]], [[Volker Braun]], Boris Kors, [[Dieter Lüst]], _The Standard Model on the Quintic_, Summary of Talks at SUSY02, 1st Intl. Conference on String Phenomenology in Oxford, Strings 2002 and 35th Ahrenshoop Symposium. ([arXiv:hep-th/0210083](http://arxiv.org/abs/hep-th/0210083))

* [[Ralph Blumenhagen]], [[Mirjam Cvetic]], Paul Langacker, Gary Shiu, _Towards Realistic Intersecting D-Brane Models_, Ann.Rev.Nucl.Part.Sci.55:71-139, 2005 ([arXiv:hep-th/0502005](http://arxiv.org/abs/hep-th/0502005))

* Ching-Ming Chen, Tianjun Li, Dimitri V. Nanopoulos, _Standard-Like Model Building on Type II Orientifolds_, Nucl.Phys.B732:224-242,2006 ([arXiv:hep-th/0509059](http://arxiv.org/abs/hep-th/0509059))

* [[Angel Uranga]], _The standard model from D-branes in string theory_, talk at Padova, January 2008 ([pdf](http://active.pd.infn.it/g4/seminars/2008/files/uranga.pdf))

* Matthew J. Dolan, Sven Krippendorf, Fernando Quevedo, _Towards a Systematic Construction of Realistic D-brane Models on a del Pezzo Singularity_, JHEP 1110 (2011) 024 ([arXiv:1106.6039](http://arxiv.org/abs/1106.6039))
 {#DolanKrippendorfQuevedo11}

* Anshuman Maharana, Eran Palti, _Models of Particle Physics from Type IIB String Theory and F-theory: A Review_ ([arXiv:1212.0555](http://arxiv.org/abs/1212.0555))

Discussion of [[GUT]] models via [[F-theory]] is in 

* [[Chris Beasley]], Jonathan J. Heckman, [[Cumrun Vafa]], _GUTs and Exceptional Branes in F-theory - I_ ([arxiv:0802.3391](http://arxiv.org/abs/0802.3391)), _II: Experimental Predictions_ ([arxiv:0806.0102](http://arxiv.org/abs/0806.0102))


#### M-theory models
 {#ReferencesMTheoryModels}

A comprehensive account on the [[G2-MSSM]] is in 

* [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Jing Shao, _The $G_2$-MSSM - An $M$ Theory motivated model of Particle Physics_ ([arXiv:0801.0478](http://arxiv.org/abs/0801.0478))

* [[Bobby Acharya]], [[Gordon Kane]], [[Piyush Kumar]], _Compactified String Theories -- Generic Predictions for Particle Physics_,  Int. J. Mod. Phys. A, Volume 27 (2012) 1230012 ([arXiv:1204.2795](http://arxiv.org/abs/1204.2795))

with comments on comparison to more recent experiments in 

* [[Gordon Kane]], Ran Lu, Bob Zheng, _Review and Update of the Compactified M/string Theory Prediction of the Higgs Boson Mass and Properties_, Int. J. Mod. Phys. A Volume 28 (2013) 1330002 ([arXiv:1211.2231](http://arxiv.org/abs/1211.2231))

Original articles include

* [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Jing Shao, _Explaining the Electroweak Scale and Stabilizing Moduli in M Theory_ ([arXiv:hep-th/0701034](http://xxx.lanl.gov/abs/hep-th/0701034)) 

* [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Diana Vaman, _An M theory Solution to the Hierarchy Problem_ ([arXiv:hep-th/0606262](http://arxiv.org/abs/hepth/0606262))

* [[Bobby Acharya]], Konstantin Bobkov, _K&#228;hler Independence of the $G_2$-MSSM_, JHEP ([arXiv:0810.3285](http://arxiv.org/abs/0810.3285))

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