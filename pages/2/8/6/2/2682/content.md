

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

### recalling the context ##

The undertaking called [[string theory]] started out as _perturbative string theory_ where the idea was to encode [[spacetime]] [[physics]] in [[perturbation theory]] by an [[S-matrix]] that is obtained by a sum of the integrals of the [[correlators]] of a fixed [[2d superconformal field theory]] over the [[moduli spaces]] of conformal structures on surfaces of all possible genera -- thought of as the [[second quantization]] of a [[string]] [[sigma-model]].

The [[S-matrix]] elements obtained this way from the [[string perturbation series]] could be seen to be approximated by an ordinary [[effective QFT]] (some flavor of [[supergravity]] coupled to [[gauge theory]] and [[fermion]]s) on [[target space]]. 

(The _first superstring revolution_ was given by the realization that this makes sense: the effective background theories obtained this way are indeed free of [[quantum anomaly|quantum anomalies]].)


Hence it is the chocie of [[worldsheet]] [[2d SCFT]] which in [[perturbative string theory]] translates products of "field insertions" into [[scattering amplitudes]]. In [[perturbative AQFT]] it is the choice of [[vacuum state]] which does this, and therefore [[2d SCFTs]] are the [[perturbative string theory vacua]]. 


### narrowing in on the issue ##

The _second superstring revolution_ was given by the realization that all these background field theories seem to fit into one single bigger context that seems to exists independently of their perturbatve definitions. 

Aspects of this bigger non-perturbative context are known as [[M-theory]]. While one couldn't figure out what that actually is, the circumstancial evidence suggested that whatever it is, it has a low-energy limit where it also looks like an effective background field theory, this time [[11-dimensional supergravity]].

In a different but similar manner, other background field theories were found whose classical solutions are thought to encode "stable solutions" ("[[vacuum]] solutions") of whatever physical theory this non-perturbative definition of string theory is.

Here, when talking about a "stable solution" one thinks of solutions of these theories of [[gravity]] with plenty of extra fields that look like [[Minkowski space]] times something else, such that all these extra fields are constant in time (using the simple Minkowsi-space-times-internal-part-ansatz to say what "constant in time" means), hence sitting at the bottom of their corresponding effective potentials.

Solutions with this property, in particular for all the scalar fields that appear, are said to have _stabilized moduli_ : the scalar fields that encode various properties of the geometry of the solution are constant in time.

Since these geometric properties determine, in the fashion of [[Kaluza-Klein theory]], the effective physics in the remaining [[Minkowski space]] factor, it is these "moduli-stabilized" solutions that have a first chance of being candidate solutions of whatever that theory is we are talking about, which describe the real world.

### the landscape 

At some point there had been the hope that only very few such solutions exist. When arguments were put forward that this is far from being true, the term **landscape** for the collection of all such solutions was invented.


So, to summarize in a few words, the landscape of string theory vacua is...

## Flux compactifications 

One widely studied class of modli-stabilized solutions to the string-theory background equations is that of **[[flux compactifications]]**.

These are classical solutions to the corresponding [[supergravity]] theory that are of the form $M^4 \times CY$ with $CY$ some [[Calabi-Yau manifold]] of six real dimensions such that the [[RR-field]] in the solution has nontrivial values on $CY$. Its components are called the _[[fluxes]]_ .

The presence of this [[RR-field]] in the solution induces an effective potential for the scalar moduli fields that parameterize the geometry of CY. Hence by choosing the [[RR-field]] suitably one can find classical solutions in which all these moduli have values that are constant in time.

A review of flux compactifications is for instance in ([Gra&#241;a 05](#Grana05))

## Computer scans of Gepner model compactifications

Discussion of [[string phenomenology]] of [[intersecting D-brane models]] [[KK-compactification|KK-compactified]] with non-geometric [[fibers]] such that the would-be string [[sigma-models]] with these [[target spaces]] are in fact [[Gepner models]] (in the sense of _[Spectral Standard Model and String Compactifications](https://www.physicsforums.com/insights/spectral-standard-model-string-compactifications/)_) is in ([Dijkstra-Huiszoon-Schellekens 04a](#DijkstraHuiszoonSchellekens04a), [Dijkstra-Huiszoon-Schellekens 04b](#DijkstraHuiszoonSchellekens04b)):


<center>
<img src="https://ncatlab.org/nlab/files/SchellekensSuperGepnerModelScanII.jpg" width="600">
</center>

>  A plot of [[standard model of particle physics|standard model]]-like [[coupling constants]] in a computer scan of [[Gepner model]]-[[KK-compactification]] of [[intersecting D-brane models]] according to [Dijkstra-Huiszoon-Schellekens 04b](#DijkstraHuiszoonSchellekens04b). 

>  The blue dot indicates the couplings in $SU(5)$-[[GUT]] theory. The faint lines are NOT drawn by hand, but reflect increased density of Gepner models as seen by the computer scan.


## Related concepts

> at least one thing missing in the discussion here is the subtlety explained out by [[Jacques Distler]] in blog dicussion [here](http://golem.ph.utexas.edu/category/2009/10/structural_foundations_of_quan.html#c028474)

* [[cosmological constant]]

* [[axionic landscape]]

* [[string theory]]

  * [[heterotic string theory]]

    * [[Green-Schwarz mechanism]]

   * [[dual heterotic string theory]]

  * [[type II string theory]]

* **[[vacuum]]**

  * [[vacuum state]], [[Hadamard state]]

  * [[interacting vacuum]]

  * [[vacuum expectation value]], [[vacuum amplitude]], [[vacuum fluctuation]]

  * [[vacuum energy]]

  * [[vacuum diagram]]

  * [[vacuum stability]]

  * [[false vacuum]], [[tachyon]], [[Coleman-De Luccia instanton]]

  * [[theta vacuum]]

  * [[perturbative string theory vacuum]]

  * [[landscape of string theory vacua]]


* [[moduli field]], [[multiverse]]

* [[model (in particle physics)]]

  * [[standard model of particle physics]]

  * [[Grand Unified Theory]], [[MSSM]]

* [[Brandenberger-Vafa mechanism]]

* [string theory FAQ - Does string theory make predictions?](string+theory+FAQ#HowDoesStringTheoryMakePredictions)

* [string theory FAQ -- What does it mean to say that string theory has a "landscape of solutions"?](http://ncatlab.org/nlab/show/string+theory+FAQ#WhatDoesItMeanToSayStringTheoryHasALandscapeOfSolutions)

## References

### F-theory flux compactification

Surveys of the general story of [[flux compactification]] in [[F-theory]] includes

* {#Denef08} [[Frederik Denef]], _Les Houches Lectures on Constructing String Vacua_, in _[[String theory and the real world]]_ ([arXiv:0803.1194](http://arxiv.org/abs/0803.1194))


### Landscape of Type II vacua

Scan of the moduli space of semi-realistic [[type II string theory|type IIB]] [[intersecting D-brane model]] [[KK-compactifications]] on [[orbifolds]] of [[Gepner models]] is in 

* {#DijkstraHuiszoonSchellekens04a} T.P.T. Dijkstra, L. R. Huiszoon, [[Bert Schellekens]], _Chiral Supersymmetric Standard Model Spectra from Orientifolds of Gepner Models_, Phys.Lett. B609 (2005) 408-417 ([arXiv:hep-th/0403196](https://arxiv.org/abs/hep-th/0403196))

* {#DijkstraHuiszoonSchellekens04b} T.P.T. Dijkstra, L. R. Huiszoon, [[Bert Schellekens]], _Supersymmetric Standard Model Spectra from RCFT orientifolds_, Nucl.Phys.B710:3-57,2005 ([arXiv:hep-th/0411129](https://arxiv.org/abs/hep-th/0411129))

and scan [[type II string theory|type IIB]] [[intersecting D-brane model]] [[KK-compactifications]] on [[toroidal orbifolds]] is in

* [[Ralph Blumenhagen]], [[Florian Gmeiner]], [[Gabriele Honecker]], [[Dieter Lüst]], [[Timo Weigand]], _The Statistics of Supersymmetric D-brane Models_, Nucl.Phys.B713:83-135, 2005 ([arXiv:hep-th/0411173](https://arxiv.org/abs/hep-th/0411173))

* {#GBHLW05} [[Florian Gmeiner]], [[Ralph Blumenhagen]], [[Gabriele Honecker]], [[Dieter Lüst]], [[Timo Weigand]], _One in a Billion: MSSM-like D-Brane Statistics_, JHEP 0601:004, 2006 ([arXiv:hep-th/0510170](https://arxiv.org/abs/hep-th/0510170))

### Landscape of heterotic vacua

The origin of all [[string phenomenology]] is the [[top-down model building|top-down approach]] in the [[heterotic string]] due to ([Candelas-Horowitz-Strominger-Witten 85](heterotic+string+theory#CHSW85)).

A brief review of motivations for [[GUT]] models in [[heterotic string theory]] is in 

* {#Witten02} [[Edward Witten]], _Quest For Unification_, Heinrich Hertz lecture at [SUSY 2002](http://www.desy.de/susy02/) at DESY, Hamburg ([arXiv:hep-ph/0207124](http://arxiv.org/abs/hep-ph/0207124))
 
The following articles establish the existences of exact realization of the [[gauge group]] and [[matter]]-content of the [[MSSM]] in [[heterotic string theory]] (not yet checking [[Yukawa couplings]]):

* [[Volker Braun]], [[Yang-Hui He]], [[Burt Ovrut]], [[Tony Pantev]], _A Heterotic Standard Model_, Phys. Lett. B618 : 252-258 2005 ([arXiv:hep-th/0501070](http://arxiv.org/abs/hep-th/0501070))

* {#BraunHeOvrutPantev06} [[Volker Braun]], [[Yang-Hui He]], [[Burt Ovrut]], [[Tony Pantev]], _The Exact MSSM Spectrum from String Theory_, JHEP 0605:043,2006 ([arXiv:hep-th/0512177](http://arxiv.org/abs/hep-th/0512177))

* [[Vincent Bouchard]], [[Ron Donagi]], _An SU(5) Heterotic Standard Model_, Phys. Lett. B633:783-791,2006 ([arXiv:hep-th/0512149](http://arxiv.org/abs/hep-th/0512149))


A computer search through the "[[landscape of string theory vacua|landscape]]" of [[Calabi-Yau varieties]] showed severeal hundreds more such exact heterotic standard models (about one billionth of all CYs searched, and most of them arising as $SU(5)$-[[GUTs]])


* [[Lara Anderson]], [[Yang-Hui He]], [[Andre Lukas]], _Heterotic Compactification, An Algorithmic Approach_, JHEP 0707:049, 2007 ([arXiv:hep-th/0702210](https://arxiv.org/abs/hep-th/0702210))

* {#AndersonGrayLukasPalti11} [[Lara Anderson]], James Gray, [[Andre Lukas]], [[Eran Palti]], _Two Hundred Heterotic Standard Models on Smooth Calabi-Yau Threefolds_ ([arXiv:1106.4804](http://arxiv.org/abs/1106.4804))

* [[Lara Anderson]], James Gray, [[Andre Lukas]], [[Eran Palti]], _Heterotic Line Bundle Standard Models_ JHEP06(2012)113 ([arXiv:1202.1757](https://arxiv.org/abs/1202.1757))

* [[Lara Anderson]], Andrei Constantin, James Gray, [[Andre Lukas]], [[Eran Palti]], _A Comprehensive Scan for Heterotic SU(5) GUT models_, JHEP01(2014)047 ([arXiv:1307.4787](https://arxiv.org/abs/1307.4787))

* [[Yang-Hui He]], Seung-Joo Lee, [[Andre Lukas]], Chuang Sun, _Heterotic Model Building: 16 Special Manifolds_ ([arXiv:1309.0223](http://arxiv.org/abs/1309.0223))

* {#CHE18} Andrei Constantin, [[Yang-Hui He]], [[Andre Lukas]], _Counting String Theory Standard Models_ ([arXiv:1810.00444](https://arxiv.org/abs/1810.00444))

The resulting database of compactifications is here:

* [[Lara Anderson]], James Gray, [[Andre Lukas]], [[Eran Palti]], _Heterotic standard model database_ ([web](http://www-thphys.physics.ox.ac.uk/projects/CalabiYau/linebundlemodels/index.html.))

Review includes

* [[Lara Anderson]], _New aspects of heterotic geometry and phenomenology_, talk at [Strings2012](http://wwwth.mpp.mpg.de/conf/strings2012/), Munich 2012 ([pdf](http://wwwth.mpp.mpg.de/members/strings/strings2012/strings_files/program/Talks/Wednesday/Anderson.pdf))

* {#He18a} [[Yang-Hui He]], _The Calabi-Yau Landscape: from Geometry, to Physics, to Machine-Learning_ ([arXiv:1812.02893](https://arxiv.org/abs/1812.02893))

* {#He18b} [[Yang-Hui He]], _Deep-learning the landscape_, talk at _[String and M-Theory: The new geometry of the 21st century](https://ims.nus.edu.sg/events/2018/wstring/wk.php)_ ([pdf slides](https://ims.nus.edu.sg/events/2018/wstring/files/yang.pdf), [video recording](https://www.youtube.com/watch?v=x3ThgBgkPlE))


Computation of [[metrics]] on these Calabi-Yau compactifications (eventually needed for computing their induced [[Yukawa couplings]]) is started in 

* [[Volker Braun]], Tamaz Brelidze, [[Michael Douglas]], [[Burt Ovrut]], _Calabi-Yau Metrics for Quotients and Complete Intersections_, JHEP 0805:080, 2008 ([arXiv:0712.3563](https://arxiv.org/abs/0712.3563))

This "heterotic standard model" has a "hidden sector" copy of the actual standard model, more details of which are discussed here:

* [[Volker Braun]], [[Yang-Hui He]], [[Burt Ovrut]], _Supersymmetric Hidden Sectors for Heterotic Standard Models_ ([arXiv:1301.6767](http://arxiv.org/abs/1301.6767))



The issue of [[moduli stabilization]] in these kinds of models is discussed in 

* Michele Cicoli, Senarath de Alwis, Alexander Westphal, _Heterotic Moduli Stabilization_ ([arXiv:1304.1809](http://arxiv.org/abs/1304.1809))

* [[Lara Anderson]], James Gray, [[Andre Lukas]], [[Burt Ovrut]], _Vacuum Varieties, Holomorphic Bundles and Complex Structure Stabilization in Heterotic Theories_ ([arXiv:1304.2704](http://arxiv.org/abs/1304.2704))


Principles singling out heterotic models with three generations of fundamental particles are discussed in:

* [[Philip Candelas]], [[Xenia de la Ossa]], [[Yang-Hui He]], Balazs Szendroi, _Triadophilia: A Special Corner in the Landscape_, Adv.Theor.Math.Phys.12:2,2008 ([arXiv:0706.3134](http://arxiv.org/abs/0706.3134))

See also 

* Hajime Otsuka, _$SO(32)$ heterotic line bundle models_, ([arXiv:1801.03684](https://arxiv.org/abs/1801.03684))


### Moduli space of 2d SCFTs

Some general thoughts on what a [[moduli space]] of 2d CFTs should be are in 

* [[Michael Douglas]], _Spaces of Quantum Field Theories_ ([arXiv:1005.2779](http://arxiv.org/abs/1005.2779))

The compactness results mentioned there are discussed in 

* {#Soibelman11} [[Yan Soibelman]], _Collapsing CFTs, spaces with non-negative Ricci curvature and nc geometry_ in [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011)

based on conjectures in 

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Homological Mirror Symmetry and torus fibrations_, ([math.SG/0011041](http://arxiv.org/abs/math/0011041))

Discussion of aspects of [[effective field theories]] which might rule them out as having a [[UV-completion]] by a [[string theory]] [[vacuum]] has been initiated in 

* {#Vafa05} [[Cumrun Vafa]], _The String Landscape and the Swampland_ ([arXiv:hepth/0509212](http://arxiv.org/abs/hepth/0509212))

See also

* {#BrennanCartaVafa17} T. Daniel Brennan, Federico Carta, [[Cumrun Vafa]], _The String Landscape, the Swampland, and the Missing Corner_ ([arXiv:1711.00864](https://arxiv.org/abs/1711.00864))

* Ben Heidenreich, [[Matthew Reece]], Tom Rudelius, _Emergence and the Swampland Conjectures_ ([arXiv:1802.08698](https://arxiv.org/abs/1802.08698))

### Phenomenological speculation
 {#ReferencesPhenomenologicalSpeculation}

Early and technical articles that amplified the existence of a finite but very large number of string theory compactifications are

* {#LercheLustSchellekens86} [[Wolfgang Lerche]], [[Dieter Lüst]], [[Bert Schellekens]], _Ten dimensional heterotic strings from Niemeier lattices_, Physics Letters B, Volume 181, Issues 1-2, 1986 ([pdf](http://cds.cern.ch/record/170910/files/198609340.pdf))

which says on p. 2

> Although the consistency requirements which string theories have to satisfy are quite restrictive, it has become clear that there are more solutions than one originally expected. [...] Although the possibility of making Lorentz rotations suggests a continuous infinity of new ten dimensional theories, there is actually only a discrete set of theories that makes physical sense, as we will explain below.

and

* {#LercheLustSchellekens87} [[Wolfgang Lerche]], [[Dieter Lüst]], [[Bert Schellekens]], _Chiral Four-dimensional Heterotic Strings from Self-dual Lattices_  Nucl. Phys. B 287, 477, 1987 ([pdf](http://lerche.web.cern.ch/lerche/papers/4dhetstrings.pdf))

which says in conclusion on page 45-46

> Although the number of chiral theories of this type is finite, our results suggest that there exist very many of them, so that a complete enumeration appears impossible.

A popular account of these observations was given in

* {#Schellekens98} [[Bert Schellekens]], _Naar een waardig slot_, inauguration speech ar University of Nijmegen, September 1998, ISBN 90-9012073-4

a commented translation of which later appeared as

* {#Schellekens06} [[Bert Schellekens]], _The Landscape "avant la lettre"_ ([arXiv:physics/0604134](http://arxiv.org/abs/physics/0604134))

Similarly

* {#Schellekens08} [[Bert Schellekens]], _The Emperor's Last Clothes?_, Rept.Prog.Phys.71:072201,2008 ([arXiv:0807.3249](https://arxiv.org/abs/0807.3249))

* {#Schellekens16} [[Bert Schellekens]], _Big Numbers in String Theory_ ([arXiv:1601.02462](http://arxiv.org/abs/1601.02462))



The articles [Lerche-L&#252;st-Schellekens 86](#LercheLustSchellekens86), [Lerche-L&#252;st-Schellekens 87](#LercheLustSchellekens87), and the speech [Schellekens 98](#Schellekens98), did not cause much of excitement then. Also they did not discuss [[moduli stabilization]], which could still have been thought to reduce the number of vacua. Excitement was only later caused instead by more vague discussion of flux compactification vacua with moduli stabilization in type IIB string theory:

That there are $10^{hundreds}$ different flux compactifications was maybe first said explicitly in 

* [[Raphael Bousso]], [[Joseph Polchinski]], _Quantization of Four-form Fluxes and Dynamical Neutralization of the Cosmological Constant_ ([arXiv:hep-th/0004134](http://arxiv.org/abs/hep-th/0004134))

The idea became popular in discussion of the [[cosmological constant]] with the alleged construction of a large set of metastable [[de Sitter spacetime]]-vacua in

* {#KKLT03} [[Shamit Kachru]], [[Renata Kallosh]], [[Andrei Linde]], [[Sandip  Trivedi]], _de Sitter Vacua in String Theory_, Phys. Rev. D68:046005, 2003 ([arXiv:hep-th/0301240](http://arxiv.org/abs/hep-th/0301240))

  ("KKLT", a good quick review is in [Danielsson-VanRiet 18 section 2.5.1](#DanielssonVanRiet18), also [Ibanez-Uranga 12, section 15.3.1](#IbanezUranga12))

and the amplification of the complication of the [KKLT 03](#KKLT03)-construction its alleged vastness in

* {#Susskind03} [[Leonard Susskind]], _The Anthropic Landscape of String Theory_, in B. Carr (ed.) _Universe or multiverse_, 247-266 ([arXiv:hep-th/0302219](http://arxiv.org/abs/hep-th/0302219))

  "The vacua in [KKLT 03](#KKLT03) are not at all simple.  They are jury-rigged, [Rube Goldberg contraptions](https://en.wikipedia.org/wiki/Rube_Goldberg_machine) that could hardly have fundamental significance." (p. 5)

* [[Joseph Polchinski]], _The Cosmological Constant and the String Landscape_ ([arXiv:hep-th/0603249](http://arxiv.org/abs/hep-th/0603249))

Review includes

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 15.3 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012

(Beware that the approach of [KKLT 03](#KKLT03) is argued to be false in [DanielssonVanRiet 18](#Danielsson-VanRiet18) and is being abandoned in [Obied-Ooguri-Spodyneiko-Vafa 18](#ObiedOoguriSpodyneikoVafa18), [Danielsson et. al 18](#de+Sitter+spacetime#BDDGS18)).


The specific (but arbitrary) value  "$10^{500}$" for the typical number of flux compactification, which became iconic in public discussion of the issue, originates in 

* {#Douglas04} [[Michael Douglas]], p. 4 of _Basic results in vacuum statistics_, Comptes Rendus Physique, vol. 5, pp. 965&#8211;977, 2004 ([arXiv:hep-th/0409207](http://arxiv.org/abs/hep-th/0409207))

* [[Ralph Blumenhagen]], [[Florian Gmeiner]], [[Gabriele Honecker]], [[Dieter Lüst]], [[Timo Weigand]], p.3 of _The Statistics of Supersymmetric D-brane Models_, Nucl.Phys.B713:83-135, 2005 ([arXiv:hep-th/0411173](http://arxiv.org/abs/hep-th/0411173))

* [[Michael Douglas]], [[Shamit Kachru]], p. 55 of _Flux Compactification_, Rev.Mod.Phys.79:733-796,2007 ([arXiv:hep-th/0610102](https://arxiv.org/abs/hep-th/0610102))


Previously 

* [[Suyay Ashok]], [[Michael Douglas]], _Counting flux vacua_, JHEP, vol. 0401, p. 060, 2004

had considered $10^{120}$ and earlier [Lerche-L&#252;st-Schellekens 87](#LercheLustSchellekens87) had $10^{1500}$.

A review of the issue of flux compactifications is in

* {#Grana05} [[Mariana Graña]], _Flux compactifications in string theory: a comprehensive review_ ([arXiv:hep-th/0509003](http://arxiv.org/abs/hep-th/0509003))
 

General considerations on this state of affairs are in

* [[Frank Wilczek]], _Multiversality_ ([arXiv:1307.7376](http://arxiv.org/abs/1307.7376))


The fact that in principle all the parameters of the "landscape" of string theory vacua are dynamical (are moduli fields) and the idea that an [[eternal cosmic inflation]] might be something like an [[ergodic process]] in this landscape has led to ideas to connect this to [[phenomenology]] and the [[standard model of cosmology]]/[[standard model of particle physics]] by way of [[statistical mechanics]].

Summaries of this line of thinking include

* [[Raphael Bousso]], _The State of the Multiverse:
The String Landscape, the Cosmological
Constant, and the Arrow of Time_, 2011 ([pdf](http://www.ctc.cam.ac.uk/stephen70/talks/swh70_bousso.pdf))

For more on this see the references at _[[multiverse]]_ and _[[eternal inflation]]_.

On the other hand, discussion casting doubt on the existence of a large number of [[de Sitter spacetime]] [[perturbative string theory vacua]] includes the following:

* [[Tom Banks]], _The Top $10^{500}$ Reasons Not to Believe in the Landscape_ ([arXiv:1208.5715](https://arxiv.org/abs/1208.5715))

* [Brennan-Carta-Vafa 17](#BrennanCartaVafa17)

* [[David Kutasov]], Travis Maxfield, Ilarion Melnikov, [[Savdeep Sethi]], _Constraining de Sitter Space in String Theory_, Phys. Rev. Lett. 115, 071305 (2015) ([arXiv:1504.00056](https://arxiv.org/abs/1504.00056))

* Jakob Moritz, Ander Retolaza, Alexander Westphal, _Towards de Sitter from 10D_, Phys. Rev. D 97, 046010 (2018) ([arXiv:1707.08678](https://arxiv.org/abs/1707.08678))

* {#Sethi17} [[Savdeep Sethi]], _Supersymmetry Breaking by Fluxes_ ([arXiv:1709.03554](https://arxiv.org/abs/1709.03554))

* {#DanielssonVanRiet18} [[Ulf Danielsson]], [[Thomas Van Riet]],  _What if string theory has no de Sitter vacua?_ ([arXiv:1804.01120](https://arxiv.org/abs/1804.01120))

* {#vanRiet18} [[Thomas Van Riet]], _Is dS space in the Swampland_, talk at [StringPheno18](http://sp18.fuw.edu.pl/) ([pdf slides](http://sp18.fuw.edu.pl/wp-content/uploads/participants-database/thomasvanriet.pdf))

* {#vanRiet18a} [[Thomas Van Riet]], _Status of KKLT_, talk at _[Simons summer workshop 2018](http://scgp.stonybrook.edu/archives/24870)_ ([recording](http://scgp.stonybrook.edu/video_portal/video.php?id=3730))

* Jakob Moritz, Ander Retolaza, Alexander Westphal, _On uplifts by warped anti-D3-branes_ ([arXiv:1809.06618](https://arxiv.org/abs/1809.06618))

Implications of the possible non-existence of de Sitter vacua in string theory are explored in

* {#ObiedOoguriSpodyneikoVafa18} Georges Obied, [[Hirosi Ooguri]], Lev Spodyneiko, [[Cumrun Vafa]], _De Sitter Space and the Swampland_ ([arXiv:1806.08362](https://arxiv.org/abs/1806.08362))

* {#AgrawalObiedSteinhardtVafa18} Prateek Agrawal, Georges Obied, Paul Steinhardt, [[Cumrun Vafa]], _On the Cosmological Implications of the String Swampland_ ([arXiv:1806.09718](https://arxiv.org/abs/1806.09718))

* {#Vafa18} [[Cumrun Vafa]], _Cosmology and the String Swampland_, talk at _[Strings 2018](https://indico.oist.jp/indico/event/5/)_ ([pdf slides](https://indico.oist.jp/indico/event/5/picture/96.pdf), [recording](https://www.youtube.com/watch?v=fU8sJRCRz24&t=1904s))

* [[Frederik Denef]], Arthur Hebecker, Timm Wrase, _The dS swampland conjecture and the Higgs potential_ ([arXiv:1807.06581](https://arxiv.org/abs/1807.06581))






