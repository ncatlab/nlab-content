

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
#### Cosmology
+-- {: .hide}
[[!include cosmology -- contents]]
=--
=--
=--






#Contents#
* table of contents
{:toc}

## Idea

In theories of [[gravity]] and [[cosmology]] a _cosmological constant_ refers to an [[energy]] contribution associated with the [[vacuum]] itself.

This is called a _cosmological constant_ because the simplest way to see this effect in [[theory (physics)|theory]] is by a summand to the [[Einstein-Hilbert action]] which is proportional to the [[volume]] of [[spacetime]], with proportionality factor some "constant" $\lambda$, as in  (eq:EinsteinHilbertWithCosmologicalConstant) below.

See below 

* _[In classical gravity](#InClassicalGravity)_

More generally, almost-constant contributions to matter fields may effectively have the same kind of effect.

Specifically in [[perturbative quantum field theory]] [[AQFT on curved spacetimes|on curved spacetimes]] the [[vacuum expectation value]] of the [[stress-energy tensor]] of the various [[matter]]-fields receives constant or essentially constant contributions, notably from [[renormalization]] freedom (e.g. [Hack 15, section 3.2.1](#Hack15)). 

See below

* _[In perturbative quantum gravity](#InPerturbativeQuantumGravity)_

In [[perturbative string theory]] the [[string perturbation series]] associated with a [[2d SCFT]] is (supposedly) UV-finite and hence has "chosen its own [[renormalization]]" already, hence here the cosmological constant may in principle be read off from a choice of [[perturbative string theory vacuum]]. See below 

* _[In string theory](#ReferencesInStringTheory)_


Observation shows that the effective cosmological constant of the [[observable universe]] is comparatively small but [[positive real number|positive]], see 

* _[Observation](#Observation)_.


 
## Details

### In classical gravity
 {#InClassicalGravity}

In an [[action functional]] on a space of [[pseudo-Riemannian manifolds]] -- such as the [[Einstein-Hilbert action]] functional for [[gravity]] -- a **cosmological constant** is a term proportional to the [[volume]] 

$$
  S_{cc} \;\colon\;  (X,g) \mapsto \lambda \int_X dvol_g
  \,,
$$

where $\lambda \in \mathbb{R}$ is the _cosmological constant_ .

For instance, pure Einstein-Hilbert gravity with cosmological constant (and no other fields) is given by the functional

$$
  \label{EinsteinHilbertWithCosmologicalConstant}
  S_{EH} + S_{cc} :  (X,g) \mapsto \int_X R\, dvol + \lambda \int_X d vol_g
  \,,
$$

Generically it happens that one considers action functionals where $\lambda$ is in fact not a constant, but a function of other fields $\phi$ on $X$. 

$$
  S \;\colon\; (X,g,\phi) \mapsto \int_X \lambda(\phi) dvol_g
  \,.
$$

In this context those solutions to the [[Euler-Lagrange equation]]s are of interest in which $\lambda(\phi)$ happens to be exactly or approximately constant. Many such models of not-really-constant-but-effectively-constant terms proportional to the volume are being proposed and considered in attempts to explain observed or speculated dynamics of the cosmos.

See in particular at _[[FRW model]]_ for the role of the cosmological constant in homogeneous and isotropic models as in the [[standard model of cosmology]]. In that context the cosmological constant is also called the _dark energy_ (density), which makes up about 70% of the energy density of the [[observable universe]] (the rest being [[dark matter]]) and a comparatively little bit of [[baryon|baryonic]] [[matter]].


### In perturbative quantum gravity
 {#InPerturbativeQuantumGravity}

In [[perturbative quantum field theory]] [[QFT on curved spacetime|on curved spacetimes]] the cosmological constant receives contributions from the [[vacuum expectation value]] of the [[stress-energy tensor]] of the [[matter]] [[field (physics)|fields]]. There is [[renormalization]]-freedom in this contribution  ([Wald 78](#Wald78), [Tichy-Flanagan 98](#TichyFlanagan98) [Moretti 01](#Moretti01)). 

Explicitly for [[FRW models]] this is discussed in ([Dappiaggi-Fredenhagen-Pinamonti 08](#DappiaggiFredenhagenPinamonti08), [Dappiagi-Hack-Moeller-Pinamonti 10](#DappiagiHackMollerPinamonti10)).
Specifically for the [[standard model of cosmology]] see ([Hack 13, around (4)](#Hack13)).

A useful review is in ([Hack 15, section 3.2.1](#Hack15)).

This means that apart from the freedom of choosing a classical comsological constant in the [[Einstein-Hilbert action]] as above, its [perturbative quantization](A+first+idea+of+quantum+field+theory#InteractingQuantumFields) ([[perturbative quantum gravity]]) introduces [[renormalization]] freedom to the value of the cosmological constant.

The folklore discussion of the "cosmological constant problem" (see the references [below](#CCProblemReferences)) tends not to take this freedom in the theory into account (see the discussion at _[[naturalness]]_).

### In inhomogeneous cosmology
 {#InInhomogeneousCosmology}

It has been suggested the observed cosmological constant/dark energy may be but an artifact of the overly idealistic approximation of cosmic homogeneity, and that a more accurate [[inhomogeneous cosmology]] would not need to assume any dark energy (e.g. [Buchert 07](#Buchert07), [Buchert 11](#Buchert11), [Buchert-Rasanen 11](#BucherRasanen11), [Scharf 13](#Scharf13)).

A seminal argument that it _is_ consistent to neglect cosmic inhomogeneity due to ([Green-Wald 10](#GreenWald10), [Green-Wald 13](#GreenWald13)), has been called into question in [Buchert et al. 15](#BuchertEtAl15), where it is concluded that the question is more subtle and remains open. Recent review is in [Belejko-Korzyński 16](#BelejkoKorzynski16).

If the apparent small positive [[cosmological constant]] were but an artifact of neglecting backreaction of inhomogeneities, some theoretical puzzlement regarding [[quantum gravity]] on [[de Sitter spacetimes]] would disappear (see [Rajaraman 16](de+Sitter+spacetime#Rajaraman16) for general discussion and [Danielsson-VanRiet 18, p. 27](#DanielssonVanRiet18) for discussion of [[perturbative string theory vacua]]).


### Observation
 {#Observation}

<img src="http://ncatlab.org/nlab/files/DarkEnergyConcordance.gif" width="500">

(e.g. [Einasto 09, fig 17](#Einasto09))


## Related concepts

* [[phantom dark energy]]

* [[quintessence]]

* [[FRW model]]

* [[cosmology]]

* [[inhomogeneous cosmology]] 

* [[Witten's Dark Fantasy]]

* [[energy]]

  * [[matter]], [[radiation]], **cosmological constant**



## References

### General

Introduction and review:

* Konstantinos Xenos, _An Introduction to FRW Cosmology and dark energy models_ ([arXiv:2101.06135](https://arxiv.org/abs/2101.06135))

Careful discussion in [[perturbative quantum gravity]]:

* [[John Donoghue]], *The cosmological constant and the use of cutoffs* ([arXiv:2009.00728](https://arxiv.org/abs/2009.00728))


### Observation

(...)

### Non-Observation
 {#NonObservation}

Cautioning against the interpretation of type Ia [[supernovae]] as indicative of a small positive cosmological constant ([[de Sitter spacetime]]) as in the current [[standard model of cosmology]] includes the following (see also at _[[inhomogeneous cosmology]]_ and at _[[Witten's Dark Fantasy]]_):

* [[Subir Sarkar]], _Is the evidence for dark energy secure?_, Gen. Rel. Grav. 40:269-284, 2008 ([arXiv:0710.5307](https://arxiv.org/abs/0710.5307))

* {#NielsenGuffantiSarkar16} J. T. Nielsen, A. Guffanti & [[Subir Sarkar]], _Marginal evidence for cosmic acceleration from Type Ia supernovae_, Nature Scientific Reports volume 6, Article number: 35596 (2016) ([arXiv:1506.01354](https://arxiv.org/abs/1506.01354), [web discussion](https://4gravitons.wordpress.com/2016/11/11/a-response-from-nielsen-guffanti-and-sarkar/))

* Koushik Dutta, Ruchika, Anirban Roy, Anjan A. Sen, M.M. Sheikh-Jabbari, _Negative Cosmological Constant is Consistent with Cosmological Data_ ([arXiv:1808.06623](https://arxiv.org/abs/1808.06623))

* Rui-Yun Guo, Jing-Fei Zhang, Xin Zhang, _Can the $H_0$ tension be resolved in extensions to ΛCDM cosmology?_ ([arXiv:1809.02340](https://arxiv.org/abs/1809.02340))

* Yijung Kang, Young-Wook Lee, Young-Lo Kim, Chul Chung, Chang Hee Ree, _Early-type Host Galaxies of Type Ia Supernovae. II. Evidence for Luminosity Evolution in Supernova Cosmology_, Astrophysical Journal  ([arXiv:1912.04903](https://arxiv.org/abs/1912.04903))

  exposition:

  _[New evidence shows that the key assumption made in the discovery of dark energy is in error](https://phys.org/news/2020-01-evidence-key-assumption-discovery-dark.amp?__twitter_impression=true)_

* Eleonora Di Valentino, Alessandro Melchiorri, Joseph Silk, _Cosmic Discordance: Planck and luminosity distance data exclude LCDM_ ([arXiv:2003.04935](https://arxiv.org/abs/2003.04935))

  (preferring [[phantom dark energy]])


* {#MRS21} [[Roya Mohayaee]], [[Mohamed Rameez]], [[Subir Sarkar]], *Do supernovae indicate an accelerating universe?* ([arXiv:2106.03119](https://arxiv.org/abs/2106.03119))




### In pAQFT
 {#ReferencedInpAQFT}

Discussion of the cosmological constant in the rigorous formulation of [[perturbative AQFT]] [[AQFT on curved spacetimes|on curved spacetimes]] includes the following.

The freedom of [[renormalization]] of the [[vacuum expectation value]] of any [[stress-energy tensor]], hence of the cosmological constant, was discussed in

* {#Wald78} [[Robert Wald]], _Trace anomaly of a conformally invariant quantum field in curved spacetime_, Phys. Rev. D 17, 1477 1978 ([doi:10.1103/PhysRevD.17.1477](https://doi.org/10.1103/PhysRevD.17.1477))

Notice that ([Wald 78](#Wald78)) is based on 

* {#Wald77} [[Robert Wald]], _The back reaction effect in particle creation in curved spacetime_, Commun. Math. Phys. (1977) 54: 1. ([doi:10.1007/BF01609833](https://doi.org/10.1007/BF01609833))

which claimed _no_ freedom of renormalization, but [Wald 78](#Wald78) explains that this was due to a mistake inherited from a citation.

Further development of this includes

* {#TichyFlanagan98} Wolfgang Tichy, Eanna E. Flanagan, _How unique is the expected stress-energy tensor of a massive scalar field?_, Phys.Rev. D58 (1998) 124007 ([arXiv:gr-qc/9807015](https://arxiv.org/abs/gr-qc/9807015))

* {#Moretti01} [[Valter Moretti]], _Comments on the Stress-Energy Tensor Operator in Curved Spacetime_, Commun. Math. Phys. 232 (2003) 189-221 ([arXiv:gr-qc/0109048](https://arxiv.org/abs/gr-qc/0109048))


A useful review is in 

* {#Hack15} [[Thomas-Paul Hack]], section 3.2.1, _Cosmological Applications of Algebraic Quantum Field Theory in Curved Spacetimes_, Springer 2016 ([arXiv:1506.01869](https://arxiv.org/abs/1506.01869), [doi:10.1007/978-3-319-21894-6](https://doi.org/10.1007/978-3-319-21894-6))

Realization of renormalization of stress-energy/cosmological constant in concrete [[FRW models]] is discussed in

* {#DappiaggiFredenhagenPinamonti08} [[Claudio Dappiaggi]], [[Klaus Fredenhagen]], [[Nicola Pinamonti]], _Stable cosmological models driven by a free quantum scalar field_, Phys. Rev. D77:104015, 2008 ([arXiv:0801.2850](https://arxiv.org/abs/0801.2850))

* {#DappiagiHackMollerPinamonti10} [[Claudio Dappiaggi]], [[Thomas-Paul Hack]], Jan Möller, [[Nicola Pinamonti]], _Dark Energy from Quantum Matter_ ([arXiv:1007.5009](https://arxiv.org/abs/1007.5009))

Discussion specifically for the [[standard model of cosmology]] is in

* {#Hack13} [[Thomas-Paul Hack]], _The Lambda CDM-model in quantum field theory on curved spacetime and Dark Radiation_ ([arXiv:1306.3074](https://arxiv.org/abs/1306.3074))


More on subtleties of [[renormalization]] of the cosmological constant:

* [[John Donoghue]], _The cosmological constant and the use of cutoffs_ ([arXiv:2009.00728](https://arxiv.org/abs/2009.00728))


### From higher curvature corrections
 {#ReferencesFromHigherCurvatureCorrections}

Effective dark energy from [[higher curvature corrections]], as in the [[Starobinsky model of cosmic inflation]]:

* Michal Artymowski, Zygmunt Lalak, _Inflation and dark energy from $f(R)$ gravity_, JCAP09(2014)036 ([arXiv:1405.7818](https://arxiv.org/abs/1405.7818))

* Michal Artymowski, Zygmunt Lalak, Marek Lewicki, _Inflation and dark energy from $f(R)$ gravity_ ([arXiv:1510.04864](https://arxiv.org/abs/1510.04864))

### From inhomogeneous cosmology

Discussion of the cosmological constant as an artefact of [[inhomogeneous cosmology]] (see there for more) includes the following

* {#Buchert07} [[Thomas Buchert]], _Dark Energy from structure: a status report_, Gen.Rel.Grav.40:467-527, 2008 ([arXiv:0707.2153](http://xxx.lanl.gov/abs/0707.2153))

* {#GreenWald10} Stephen R. Green, [[Robert Wald]], _A new framework for analyzing the effects of small scale inhomogeneities in cosmology_, Phys.Rev.D83:084020, 2011 ([arXiv:1011.4920](https://arxiv.org/abs/1011.4920))

* {#Buchert11} [[Thomas Buchert]], _Toward physical cosmology: focus on inhomogeneous geometry and its non-perturbative effects_, Class.Quant.Grav.28:164007, 2011 ([arXiv:1103.2016](https://arxiv.org/abs/1103.2016))

* {#BuchertRasanen11} [[Thomas Buchert]], Syksy Rasanen, _Backreaction in late-time cosmology_, Annual Review of Nuclear and Particle Science 62 (2012) 57-79 ([arXiv:1112.5335](https://arxiv.org/abs/1112.5335))

* {#GreenWald13} Stephen Green, [[Robert Wald]], _Examples of backreaction of small scale inhomogeneities in cosmology_, Phys.Rev.D87:124037, 2013 ([arxiv:1304.2318](https://arxiv.org/abs/1304.2318))

* {#Scharf13} [[Günter Scharf]], _Inhomogeneous cosmology in the cosmic rest frame without dark stuff_, chapter 6 in the latest edition of _[[Quantum Gauge Theories -- A True Ghost Story]]_, Wiley 2001 ([arXiv:1312.2695](https://arxiv.org/abs/1312.2695))

* {#BuchertEtAl15} [[Thomas Buchert]] et. al, _Is there proof that backreaction of inhomogeneities is irrelevant in cosmology?_, Class. Quantum Grav. 32 215021, 2015 ([arXiv:1505.07800](https://arxiv.org/abs/1505.07800))

  exposition in _[The Universe is inhomogeneous. Does it matter?](https://cqgplus.com/2016/01/20/the-universe-is-inhomogeneous-does-it-matter/)_ CQG+, 2016

* {#BelejkoKorzynski16} Krzysztof Bolejko, Mikołaj Korzyński, _Inhomogeneous cosmology and backreaction: Current status and future prospects_, Int. J. Mod. Phys. D 26, 1730011 (2017) ([arXiv:1612.08222](https://arxiv.org/abs/1612.08222))

* {#DanielssonVanRiet18} [[Ulf Danielsson]], Thomas Van Riet,  _What if string theory has no de Sitter vacua?_ ([arXiv:1804.01120](https://arxiv.org/abs/1804.01120))


See also at _[[inhomogeneous cosmology]]_.


### The "cosmological constant problem"
 {#CCProblemReferences}

Discussion of the experimentally observed tiny cosmological constant and the folklore theoretical problem with that includes the following

* Subir Sarkar, _New results in cosmology_ ([arXiv:hep-ph/0201140](https://arxiv.org/abs/hep-ph/0201140))

* Stefanus Nobbenhuis, _The cosmological constant problem -- an inspiration for new physics_ PhD thesis (2006) ([web](http://igitur-archive.library.uu.nl/dissertations/2006-0615-200938/) [pdf](http://igitur-archive.library.uu.nl/dissertations/2006-0615-200938/c1.pdf))

* Joan Sola, _Cosmological constant and vacuum energy: old and new ideas_, J.Phys.Conf.Ser. 453 (2013) 012015 ([arXiv:1306.1527](https://arxiv.org/abs/1306.1527))
 
* Ioanna Kourkoulou, Alberto Nicolis, Guanhao Sun, _A technical analog of the cosmological constant problem and a solution thereof_ ([arXiv:2101.11620](https://arxiv.org/abs/2101.11620), [talk rec](https://t.co/0jV2L9R79q?amp=1))



### In string theory
  {#ReferencesInStringTheory}

Discussion from the point of view of [[perturbative string theory]], where the cosmological constant is fixed by the choice of [[perturbative string theory vacuum]].

#### For fundamentally vanishing cc ("Witten's Dark Fantasy")
{#ReferencesStringTheoryVanishingCC}

An argument for [[non-perturbative effect|non-perturbative]] non-[[supersymmetry|supersymmetric]] 4d [[string phenomenology]] with fundamentally vanishing [[cosmological constant]], based on 3d [[M-theory on 8-manifolds]] decompactified at strong coupling to 4d via [[duality between M-theory and type IIA string theory]] (recall the [[super 2-brane in 4d]]):

* {#Witten00} [[Edward Witten]], _The Cosmological Constant From The Viewpoint Of String Theory_, lecture at [DM2000](http://inspirehep.net/record/972507) ([arXiv:hep-ph/0002297](https://arxiv.org/abs/hep-ph/0002297))

  (see p. 7)

* [[Edward Witten]], _Strong coupling and the cosmological constant_, Mod. Phys. Lett. A 10:2153-2156, 1995 ([arXiv:hep-th/9506101](https://arxiv.org/abs/hep-th/9506101))

* [[Edward Witten]], Section 3 of _Some Comments On String Dynamics_, talk at [Strings95](https://cds.cern.ch/record/305869) ([arXiv:hep-th/9507121](http://arxiv.org/abs/hep-th/9507121))

This suggestion was called _[[Witten's Dark Fantasy]]_ in [Heckmann-Lawrie-Lin-Zoccarato 19, Section 8](#HeckmannLawrieLinZoccarato19),
where a concrete realization of this scenario in [[F-theory]] is claimed:

* [[Cumrun Vafa]], Section 4.3 of: _Evidence for F-Theory_, Nucl. Phys. B469:403-418, 1996 ([arxiv:hep-th/9602022](https://arxiv.org/abs/hep-th/9602022))

* {#HeckmannLawrieLinZoccarato19} [[Jonathan Heckman]], Craig Lawrie, Ling Lin, [[Gianluca Zoccarato]], _F-theory and Dark Energy_, Fortschritte der Physik  ([arXiv:1811.01959](https://arxiv.org/abs/1811.01959), [doi:10.1002/prop.201900057]( https://doi.org/10.1002/prop.201900057))

* [[Jonathan Heckman]], Craig Lawrie, Ling Lin, Jeremy Sakstein, [[Gianluca Zoccarato]], _Pixelated Dark Energy_ ([arXiv:1901.10489](https://arxiv.org/abs/1901.10489))

#### For fundamentally non-vanishing cc

But a) there might be a large space of [[perturbative string theory vacua]]  and b) the [[de Sitter spacetime|de Sitter vacua]] that seem to correspond to observation tend to exist (only) as metastable vacua:

* {#KachruKalloshLindeTrivedi03} [[Shamit Kachru]], [[Renata Kallosh]], [[Andrei Linde]], [[Sandip Trivedi]], _de Sitter Vacua in String Theory_, Phys.Rev.D68:046005, 2003 ([arXiv:hep-th/0301240](https://arxiv.org/abs/hep-th/0301240))

This observation led to the discussion of the "[[landscape of string theory vacua]]".

For review see

* {#Kallosh05} [[Renata Kallosh]], section 3 of _de Sitter vacua and the landscape of string theory_, J. Phys. Conf. Ser. 24 (2005) 87-110 ([spire](http://inspirehep.net/record/701033/))

However, consistency problems of these arguments are raised in

* {#DanielssonVanRiet18} [[Ulf Danielsson]], Thomas Van Riet,  _What if string theory has no de Sitter vacua?_ ([arXiv:1804.01120](https://arxiv.org/abs/1804.01120))
 

[[!redirects dark energy]]

