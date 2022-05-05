

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
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

What is called _inhomogeneous cosmology_ is the study of [[cosmology]] via cosmological solutions to [[Einstein's equations]], _without_ assuming or constraining these solutions to be spatially homogeneous (in the technical sense).

This is in contrast to the [[standard model of cosmology]], based on [[FRW model]]-type solutions to [[Einstein's equations]], where [[spacetime]] _is_ assumed to be spatially homogeneous (an assumption also known as the _cosmological principle_). 

Of course the [[observable universe]] is clearly not _exactly_ homogeneous (due to initial [[CMB]] fluctuation and ensuing [[structure formation]]), but the question is whether on cosmic [[scales]] the deviation from homogeneity is small enough that it may be neglected, to first approximation, for the purpose of modelling cosmological evolution, or whether it exerts relevant "backreaction" on the global evolution of spacetime.

It has been shown that the effect of such backreaction is small or invisible if the inhomogeneity is modeled in a Newtonian limit, instead of taking [[general relativity|relativity]] into account ([Buchert 00](#Buchert00), [Buchert-Ehlers 95](#BuchertEhlers95)), which however is the standard approximation currently used in comparing the [[standard model of cosmology]] to data.

## Effective dark energy from inhomogeneity?

The [[standard model of cosmology]] assumes that such inhomogeneities may be neglected to zeroth order, and studies [[structure formation]] as a perturbation about a spatially homogeneous [[FRW model]] [[background field|background]] [[spacetime]].

Given that the [[standard model of cosmology]] faces some issues (e.g. [BCKRW 15](standard+model+of+cosmology#BCKRW15)) related to _[[dark energy]]_ (a [[cosmological constant]], and possibly related issues such as [[cosmic inflation]]), it has been suggested that these may be but an artifact of the overly idealistic approximation of cosmic homogeneity, and that a more accurate inhomogeneous cosmology would not need to assume any [[dark energy]]/[[cosmological constant]]  (e.g. [Célérier 00](#Celerier00), [Buchert 00](#Buchert00), [Wetterich 01](#Wetterich01), [Schwarz 02](#Schwarz02), [Räsänen 03](#Rasanen03), [Alnes-Amarzguioui-Gron 06](#AlnesAmarzguiouiGron06), [Alnes-Amarzguioui 06](#AlnesAmarzguioui06), [Buchert-Larena-Alimi 06](#BuchertLarenaAlimi06), [Enqvist-Mattsson 06](#EnqvistMattsson06) [Buchert 07](#Buchert07), [Sarkar 08](#Sarkar08), [Buchert 11](#Buchert11), [Buchert-Räsänen 11](#BuchertRasanen11), [Scharf 13](#Scharf13), [Smoller-Temple-Vogler 14](#SmollerTempleVogler14), [Moffat 16](#Moffat16)).

{#Qualitative} A qualitative discussion of how inhomogeneity may cause accelerated cosmic expansion is given in [Räsänen 10, section 3: "Understanding acceleration"](#Rasanen10):

> In general, underdense regions $[$"voids"$]$ are negatively curved and expand faster than the average, while overdense regions are positively curved and expand slower. ([Räsänen 03, p. 15](#Rasanen03))

> $[...]$ as the volume occupied by $[$inhomogeneous$]$ structures grows (along with the density contrast of typical structures), the expansion rate becomes dominated by voids, since their volume is large $[...]$ overdense regions slow down more as their density contrast grows, and eventually they turn around and collapse to form stable structures. Underdense regions become ever emptier, and their deceleration decreases. Regions thus become more differentiated, and the variance of the expansion rate grows. ([Räsänen 03, p. 25](#Rasanen03))

> In an inhomogeneous space, different regions expand at different rates.  Regions with faster expansion rate increase their volume more rapidly, by definition. Therefore the fraction of volume in faster expanding regions
rises, so the average expansion rate can rise ([Räsänen 10, p. 8](#Rasanen10))

> The acceleration is not due to regions speeding up locally, but due to the slower region becoming less represented in the average. First the overdense region brings down the expansion rate, but its fraction of the volume falls because of the slower expansion, so eventually the underdense region takes over and the average expansion rate rises.

> $[...]$ After the overdense region stops being important, the expansion rate will be given by the underdense region alone, and the expansion will again decelerate. Acceleration is a transient phenomenon associated with the volume becoming dominated by the underdense region. 

> $[...]$ Whether the expansion accelerates depends on how rapidly the faster expanding regions catch up with the slower ones, roughly speaking by how steeply the $H t$ curve rises.  This is why the variance contributes positively to acceleration: the larger the variance, the bigger the difference between fast and slow regions, and the more rapidly the fast regions take over.  

> $[...]$ So there is no ambiguity:  accelerated average expansion due to inhomogeneities is possible. The question is whether the distribution of structures in the universe is such that this mechanism is realised ([Räsänen 10, p. 10](#Rasanen10))

{#AbstractSmollerTempleVogler14} An analytic proof of this qualitative picture is claimed in [Smoller-Temple-Vogler 14](#SmollerTempleVogler14):

> Our analysis is based on the discovery of a closed ansatz for perturbations of the SM during the p$ = 0$ epoch of the Big Bang which triggers instabilities that create unexpectedly large regions of accelerated uniform expansion  within  Einstein’s  original  theory  without  the  cosmological constant.  We prove that these accelerated regions introduce
precisely the same range of corrections to redshift vs luminosity as are produced by the cosmological constant in the theory of Dark Energy. 

Survey of the field of inhomogeneous cosmology and of attitudes in the community towards open issues is in [Belejko-Korzyński 16](#BelejkoKorzynski16).

If the apparent small positive [[cosmological constant]] ([[dark energy]]) were but an artifact of neglecting backreaction of inhomogeneities, some theoretical puzzlements regarding [[quantum gravity]] on [[de Sitter spacetimes]] would disappear (see [Rajaraman 16](de+Sitter+spacetime#Rajaraman16) for general discussion and [Danielsson-VanRiet 18, p. 27](#DanielssonVanRiet18) for discussion of [[perturbative string theory vacua]]).

## Numerical simulation
 {#NumericalSimulation}

Numerical simulations of inhomogeneous cosmology are in their infancy (see [Belejko-Korzyński 16, p. 7](#BelejkoKorzynski16)), but include the following: [Clesse-Roisin-Füzfa 17](#ClesseRoisinFufza17), [ACDDK 17](#ACDDK17), [Montanari-Räsänen 17](#MontanariRasanen17). 

The conclusion in [Montanari-Räsänen 17, p. 20](#MontanariRasanen17) is as follows:

> $[$the model$]$ shows an increase of the expansion rate of the right order of magnitude, compared to observations, at late times. $[...]$. It is nontrivial that the right order of magnitude in the amplitude and roughly  right timescale of the change in the expansion rate follow simply from the known physics of structure formation. However, the model has shortcomings that would need to be overcome for the results to be more than suggestive.

Dependency of results on the choice of [[gauge fixing]] is highlighted in [ACDDK 17](#ACDDK17):

> We then show numerical results from the fully relativistic weak field $N$-body code _gevolution_. (p.2)

> $[...]$ The conclusion of this work is therefore that there are gauges which are relatively close to what observers measure and in these gauges backreaction is small. We used the example of Poisson gauge, but there would be others, e.g. geodesic light cone gauge [53, 54]. However, comoving synchronous gauge is not well suited to describe observations in the late time clumpy universe.  In this gauge backreaction becomes large and the gauge actually breaks down during structure formation. (p. 4)


## The "backreaction debate"
 {#BackreactionDebate}

A seminal theoretical argument that it _is_ consistent to neglect cosmic inhomogeneity was given by [Green-Wald 10](#GreenWald10), [Green-Wald 13](#GreenWald13), [Green-Wald 16](#GreenWald16). This was called into question in [Buchert et al. 15](#BuchertEtAl15), where it is concluded that the issue is more subtle and remains open. The reply to this criticism by [Green-Wald 15](#GreenWald15) is summarized in [Ostrowski-Roukema 15, p. 4](#OstrowskiRoukema15) as follows:

> Green and Wald state that their formalism does not apply to situations when

> $\ast$ the actual metric (e.g., at recent epochs) is far from FLRW; or

> $\ast$ one wishes to construct an effective metric (or other effective quantities) through some averaging procedure

> This, in principle, ends the debate about whether backreaction has been excluded as a dark energy candidate: the Green and Wald formalism does not apply to the main body of backreaction research; backreaction remains a viable dark energy candidate.

Accordingly, the review [Coley 18, section 3.5](#Coley18) of [[mathematical physics|mathematical]] [[general relativity]] regards the issue as open:

> An important open question in cosmology is whether averaging of inhomogeneities can lead to significant backreaction effects on very large scales. (p. 28)


Indeed, [Smoller-Temple-Vogler 14](#SmollerTempleVogler14) claim an analytic solution which does exhibit inhomogeneity effects mimicking dark energy (see [above](#AbstractSmollerTempleVogler14)).  Also relativistic numerical simulation, albeit in their infancy, seem to exhibit noticeable backreaction (see [above](#NumericalSimulation)).




## Lemaitre-Tolman-Bondi models
 {#LemaitreTolmanBondi}

A particular class of exactly soluable simple examples of inhomogeneous cosmological models are Lemaitre-Tolman-Bondi models. If taken as quasi-realistic models in themselves, these require assuming that we inhabit a position close to a singled-out "center" of the universe, usually the center of an assumed cosmic "void", of low matter density. See e.g. [Moffat 05](#Moffat05), [Enkvist 07](#Enkvist07), [Moffat 16](#Moffat16). 

It has been argued (e.g. [Moffat 16, p. 2](#Moffat16)) that the apparent unlikeliness of such a "spatial coincidence" is relativized in view of the observed  "temporal coincidence" that cosmic acceleration seems to start roughly with the onset of [[structure formation]] (the "coincidence problem" of cosmology), and the perceived fine-tuning of the [[cosmological constant]] required in the [[standard model of cosmology]].

However, this may be over-interpreting the realism of these simple models. According to [Räsänen 03, p. 15](#Rasanen03):

> In order to evaluate the importance of backreaction in the real universe, we need statistical knowledge about complex configurations of dust, not exact information about simplified models.



## Related concepts

* [[structure formation]]

## References

### Theory of backreaction

* {#BuchertEhlers95} [[Thomas Buchert]], Juergen Ehlers, _Averaging inhomogeneous Newtonian cosmologies_, Astron. Astrophys.320:1-7, 1997 ([arXiv:astro-ph/9510056](https://arxiv.org/abs/astro-ph/9510056))

* {#Buchert00} [[Thomas Buchert]], _On average properties of inhomogeneous cosmologies_, Gen.Rel.Grav.9:306-321, 2000 ([arXiv:gr-qc/0001056](https://arxiv.org/abs/gr-qc/0001056))


* {#BuchertLarenaAlimi06} [[Thomas Buchert]], Julien Larena, Jean-Michel Alimi, _Correspondence between kinematical backreaction and scalar field cosmologies - the 'morphon field'_, Class. Quant. Grav.23:6379-6408, 2006 ([arXiv:gr-qc/0606020](https://arxiv.org/abs/gr-qc/0606020))

* {#Rasanen08} Syksy Räsänen, _Evaluating backreaction with the peak model of structure formation_, JCAP 0804:026,2008 ([arXiv:0801.2692](https://arxiv.org/abs/0801.2692))

* {#Rasenen10} Syksy Räsänen, _Backreaction as an alternative to dark energy and modified gravity_ ([arXiv:1012.0784](https://arxiv.org/abs/1012.0784))

* {#GreenWald10} Stephen R. Green, [[Robert Wald]], _A new framework for analyzing the effects of small scale inhomogeneities in cosmology_, Phys.Rev.D83:084020, 2011 ([arXiv:1011.4920](https://arxiv.org/abs/1011.4920))

* {#Buchert11} [[Thomas Buchert]], _Toward physical cosmology: focus on inhomogeneous geometry and its non-perturbative effects_, Class.Quant.Grav.28:164007, 2011 ([arXiv:1103.2016](https://arxiv.org/abs/1103.2016))

* {#GreenWald13} Stephen Green, [[Robert Wald]], _Examples of backreaction of small scale inhomogeneities in cosmology_, Phys.Rev.D87:124037, 2013 ([arxiv:1304.2318](https://arxiv.org/abs/1304.2318))

* {#GreenWald15} Stephen R. Green, [[Robert Wald]], _Comments on Backreaction_ ([arXiv:1506.06452](https://arxiv.org/abs/1506.06452))


* {#BuchertEtAl15} [[Thomas Buchert]] et. al, _Is there proof that backreaction of inhomogeneities is irrelevant in cosmology?_, Class. Quantum Grav. 32 215021, 2015 ([arXiv:1505.07800](https://arxiv.org/abs/1505.07800))

  exposition in _[The Universe is inhomogeneous. Does it matter?](https://cqgplus.com/2016/01/20/the-universe-is-inhomogeneous-does-it-matter/)_ CQG+, 2016


* {#OstrowskiRoukema15} Jan J. Ostrowski, Boudewijn F. Roukema, _On the Green and Wald formalism_, The Fourteenth Marcel Grossmann Meeting ([arXiv:1512.02947](https://arxiv.org/abs/1512.02947), [talk slides pdf](https://cosmoback.sciencesconf.org/data/program/Ostrowski.pdf))

* {#GreenWald16} Stephen Green, [[Robert Wald]], _A Simple, Heuristic Derivation of our "No Backreaction" Results_, Classical and Quantum Gravity, Volume 33, Number 12, 2016 ([arXiv:1601.06789](https://arxiv.org/abs/1601.06789))


* {#MontanariRasanen17} Francesco Montanari, Syksy Räsänen, _Evaluating backreaction with the ellipsoidal collapse model_, JCAP12(2017)008 ([arXiv:1710.02451](https://arxiv.org/abs/1710.02451))

* {#Coley18} [[Alan Coley]], section 3.5 of _Mathematical General Relativity_ ([arXiv:1807.08628](https://arxiv.org/abs/1807.08628))



See also 

* Wikipedia, _[Inhomogeneous cosmology](https://en.wikipedia.org/wiki/Inhomogeneous_cosmology)_

* Wikipedia, _[Accelerating expansion of the universe -- Alternative theories](https://en.wikipedia.org/wiki/Accelerating_expansion_of_the_universe#Alternative_theories)_


### Effective dark energy from inhomogeneity

* {#Celerier00} Marie-Noëlle Célérier, _Do we really see a cosmological constant in the supernovae data?_, Astron.Astrophys.353:63-71,2000

* {#Wetterich01} [[Christof Wetterich]], _Can Structure Formation Influence the Cosmological Evolution?_, Phys.Rev. D67 (2003) 043513 ([arXiv:astro-ph/0111166](https://arxiv.org/abs/astro-ph/0111166))

* {#Schwarz02} Dominik J. Schwarz, _Accelerated expansion without dark energy_ ([arXiv:astro-ph/0209584](https://arxiv.org/abs/astro-ph/0209584))

* {#Rasanen03} Syksy Räsänen, _Dark energy from backreaction_, JCAP 0402:003, 2004 ([arXiv:astro-ph/0311257](https://arxiv.org/abs/astro-ph/0311257))


* {#AlnesAmarzguiouiGron06} H. Alnes, M. Amarzguioui and O. Gron, _An inhomogeneous alternative to dark energy?_, Phys. Rev. D 73, 083519 (2006) ([arXiv:astro-ph/0512006](https://arxiv.org/abs/astro-ph/0512006))


* {#EnqvistMattsson06} Kari Enqvist, Teppo Mattsson, _The effect of inhomogeneous expansion on the supernova observations_, JCAP 0702:019,2007 ([arXiv:astro-ph/0609120](https://arxiv.org/abs/astro-ph/0609120))

* {#AlnesAmarzguioui06} Havard Alnes, Morad Amarzguioui, _The supernova Hubble diagram for off-center observers in a spherically symmetric inhomogeneous universe_, Phys. Rev. D75:023506, 2007 ([arXiv:astro-ph/0610331](https://arxiv.org/abs/astro-ph/0610331))

* {#Buchert07} [[Thomas Buchert]], _Dark Energy from structure: a status report_, Gen.Rel.Grav.40:467-527, 2008 ([arXiv:0707.2153](http://xxx.lanl.gov/abs/0707.2153))

* {#Sarkar08} Subir Sarkar, _Is the evidence for dark energy secure?_, Gen. Rel. Grav.40:269-284, 2008 ([arXiv:0710.5307](https://arxiv.org/abs/0710.5307))

* Alessio Notari, _Can an Inhomogeneous Universe mimic
Dark Energy?_, 2009 ([[NotariInhomogeneousCosmology.pdf:file]])
 
* Michael Blomqvist, _Inhomogeneous cosmologies with clustered dark energy or a local matter void_,  2010 ([web](http://www.diva-portal.org/smash/record.jsf?pid=diva2%3A353689&dswid=2010))


* {#BuchertRasanen11} [[Thomas Buchert]], Syksy Räsänen, _Backreaction in late-time cosmology_, Annual Review of Nuclear and Particle Science 62 (2012) 57-79 ([arXiv:1112.5335](https://arxiv.org/abs/1112.5335))

* {#SmollerTempleVogler14} Joel Smoller, Blake Temple, Zeke Vogler, _An Instability of the Standard Model Creates the Anomalous Acceleration Without Dark Energy_, Proceedings of the Royal Society A, 2017 ([arXiv:1412.4001](https://arxiv.org/abs/1412.4001), [10.1098/rspa.2016.0887](http://rspa.royalsocietypublishing.org/content/473/2207/20160887), detailed talk slides: [[Temple16.pdf:file]], talk [recording I](https://www.youtube.com/watch?v=fV8KPj8vmGw), [recording II](http://cdsweb.cern.ch/record/1371553))

* {#BelejkoKorzynski16} Krzysztof Bolejko, Mikołaj Korzyński, _Inhomogeneous cosmology and backreaction: Current status and future prospects_, Int. J. Mod. Phys. D 26, 1730011 (2017) ([arXiv:1612.08222](https://arxiv.org/abs/1612.08222))


* {#ClesseRoisinFufza17} Sebastien Clesse, Arnaud Roisin, André Füzfa, _Mimicking Dark Energy with the backreactions of gigaparsec inhomogeneities_ ([arXiv:1702.06643](https://arxiv.org/abs/1702.06643))

* {#ACDDK17} Julian Adamek, Chris Clarkson, David Daverio, Ruth Durrer, Martin Kunz, _Safely smoothing spacetime: backreaction in relativistic cosmological simulations_ ([arXiv:1706.09309](https://arxiv.org/abs/1706.09309))

* {#DanielssonVanRiet18} [[Ulf Danielsson]], Thomas Van Riet,  _What if string theory has no de Sitter vacua?_ ([arXiv:1804.01120](https://arxiv.org/abs/1804.01120))

### Lemaitre-Tolman-Bondi models

* {#Moffat05} [[John Moffat]], _Late-time Inhomogeneity and Acceleration Without Dark Energy_, JCAP 0605 (2006) 001 ([arXiv:astro-ph/0505326](https://arxiv.org/abs/astro-ph/0505326))

* {#Enkvist07} Kari Enqvist, _Lemaitre-Tolman-Bondi model and accelerating expansion_, Gen. Rel. Grav.40:451-466, 2008 ([arXiv:0709.2044](https://arxiv.org/abs/0709.2044))

* {#Scharf13} [[Günter Scharf]], _Inhomogeneous cosmology in the cosmic rest frame without dark stuff_, chapter 6 in the latest edition of _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001 ([arXiv:1312.2695](https://arxiv.org/abs/1312.2695))

* {#Moffat16} [[John Moffat]], _Inhomogeneous Cosmology Redux_ ([arXiv:1608.00534](https://arxiv.org/abs/1608.00534))


See also 

* Wikipedia, _[Lemaître–Tolman metric](https://en.wikipedia.org/wiki/Lema%C3%AEtre%E2%80%93Tolman_metric)_


[[!redirects inhomogeneous cosmologies]]

[[!redirects Lemaitre-Tolman-Bondi cosmology]]
[[!redirects Lemaitre-Tolman-Bondi model]]
[[!redirects Lemaitre-Tolman-Bondi models]]

[[!redirects LTB model]]
[[!redirects LTB models]]
