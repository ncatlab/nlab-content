
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Fields and quanta
+-- {: .hide}
[[!include fields and quanta - table]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

The [[observable universe]] at large scales seems to behave as if it contains large amount of [[matter]] which does have a [[gravity|gravitational effect]] but does not emit [[electromagnetic radiation]] and hence remains "dark" to telescopes. This hypothetical matter is therefore called _dark matter_.

There are various astronomical observations that suggest the existence of dark matter

1. galaxy rotation curves -- the speed of rotation of [[galaxies]] as a function of the distance from their center cannot be explained by the observed visible matter, but an explanation of this dependence by gravitating matter requires the presence of plenty of dark matter;

1. cosmic microwave background fluctuations -- the measured fluctuations in the [[cosmic microwave background]] are very well fitted by the [[standard model of cosmology]] with cold dark matter (CDM) included. (see also [Resonaances, 18 Jan 2013](#Resonaances)).

1. Simulations of [[structure formation]] in the universe seem to require existence of dark matter in order to reproduce results compatible with observation.

Any further details about the nature of this hypothetical dark matter remain elusive to date. Possible classes of candidates go by various names. For instance "[[weakly interacting massivle particle|weakly interacting massive particles]]" ("[[WIMP]]"s), hence massive particles that interact via [[gravity]] and the [[weak nuclear force]], but not via [[electromagnetism]].
Certain [[neutrino]]-dark matter scenarios are being discussed ([Neutrino White 16](#NeutrinoWhite16))
 In [[supersymmetry|supersymmetric]] [[theory (physics)|theories]] with [[R-parity]] imposed, the _lightest supersmmetric particle_ (LSP, such as the [[gravitino]] or the [[neutralino]]) is traditionally regarded as a natural candidate for dark matter ([EHNOS 84](#EHNOS84), reviewed in [Ellis-Olive 10](#EllisOlive10)).

## On galactic scales
 {#Properties}

The cold dark matter paradigm always worked excellently on cosmic scales, while seemingly facing problems with reproducing various observations on the scale of [[galaxies]]. But various recent computer simulations (e.g. with [FIRE](structure+formation#ReferencesFIRE), see the references [below](#ReferencesComputerSimulation)) point to these problems all going away when the complex dynamics of star-formation feedback/back-reaction on galactic [[structure formation]] (see there for more) is taken into account. We discuss this for:

1. _[The cusp-core behaviour](#CuspCoreProblem)_

1. _[Galactic rotation profiles](#GalacticRotationCurves)_

1. _[Missing satellites](#MissingSatellites)_

### Cusp-core behaviour
 {#CuspCoreProblem}

Early numerical simulation of dark matter exhibited dark matter halos around galaxies with a sharp density maximum at the center of the galaxy -- called a "cusp" in the density profile -- while observation on actual galaxies tends to favour a noticeably smoother density distribution at the center -- called a "core" of the density profile.

This discrepancy between [[theory (physics)|theory]] and [[experiment]] is (or was) known as the _cusp-core problem_ for dark matter [[model (physics)|models]] (see the references [below](#ReferencesCoreCuspProblem)). It is (or was) one of several issues that the dark matter model has (or had) on the scale of galaxies and smaller.

There are two potential resolutions to this problem: a) Either dark matter is more "exotic" than assumed in these simulations, such as being [[fuzzy dark matter]] or similar. Or, b), more mundanely, the existing simulations do not properly resolve a subtle effect shown already by more ordinary dark matter.

Recent investigations support possibility b), indicating that the density cusps seen in previous simulations are but an artifact of overly simplified numerical models, and that would-be cusps are diluted and hence smoothed out by bursty star formation leading to dark matter heating ([Pontzen-Governato 14](#PontzenGovernato14), [Read-Walker-Steger-18](#ReadWalkerSteger18)) and/or by dynamical friction in the interstallar medium ([ESH 01](#ESH01)). See [Read 19](#Read19) for review.


From [[Justin Read]] [22 Aug 2018](https://twitter.com/ReadDark/status/1032176578808168448) on [Read-Walker-Steger 18](#ReadWalkerSteger18):

> On large scales, the [[standard model of cosmology|standard cosmological model]] (LCDM) gives an excellent description of the [[cosmic microwave background]] [[radiation]] and the [[structure formation|growth of structure]]. However, on small scales, in our cosmic backyard known as the Local Group, there have been long-standing puzzles.  The oldest of these is the “cusp-core” problem. Gas rich dwarf galaxies have much less dark matter (DM) in their inner regions than early numerical models predicted. This could point to more exotic DM models, or to a failure of the cosmological model.

> However, there is a simpler solution. The early numerical models, above, considered a universe that contains only DM. Recent models that include gas cooling, star formation, and gas blow-out due to exploding stars find that star formation in dwarfs is bursty.

> This bursty star formation occurs due to repeated cycles of gas inflow and outflow. These cause the inner gravitational potential of the dwarf galaxy to fluctuate, kinematically "heating up" the dark matter and lowering its inner density ([Pontzen-Governato 14](#PontzenGovernato14)).

>  A key prediction of such models is that, at a fixed dark matter halo mass, more star formation leads to more dark matter "heating" and, therefore, a lower inner dark matter density, at least in dwarf galaxies. This is the prediction we set out to test in [Read-Walker-Steger 18](#ReadWalkerSteger18). 


\linebreak

### Galactic rotation profile
 {#GalacticRotationCurves}

Computer simulation ([FIRE](https://fire.northwestern.edu)) of [[galaxy|galactic]] [[structure formation]] using the [[standard model of cosmology|standard]] [[cold dark matter]] [[model (physics)|model]] qualitatively reproduces the peculiar [[galactic rotation curves]] that motivated dark matter (or [[MOND]], for that matter) in the first place ([Hopkins et al. 17, Figure 4, Figure 5](#Hopkins17)):

\begin{center}
\begin{imagefromfile}
  "file_name": "FIRE2GalacticRotationCurves.jpg",
  "width": 800
\end{imagefromfile}
\end{center}

> graphics grabbed from ([Hopkins et al. 17](#Hopkins17))

and also reproduces well the baryonic [[Tully-Fisher relation]] ([El-Badry et al. 18, Figure 4](#ElBadry18)) which used to be an issue in the [[standard model of cosmology|standard]] [[cold dark matter]] [[model (physics)|model]]:


\begin{center}
\begin{imagefromfile}
  "file_name": "FIRE2TullyFisher.jpg",
  "width": 500
\end{imagefromfile}
\end{center}

> graphics grabbed from ([El-Badry et al. 18](#ElBadry18))

More in detail, [[galaxy rotation curves]] exhibit a close correlation between [[angular velocity]] and total _visible_ enclosed math at any given [[radius]], called the _[[radial acceleration relation]]_ (RAR) or _[[mass-discrepancy acceleration relation]]_. This, too, is reproduced in [[cold dark matter]]-[[model (in theoretical physics)]]  computer simulation ([Santos-Santos et al. 15](#SantosSantosEtAl15), [Cintio-Lelli 15](#CintioLelli15), [Keller-Wadsley 16](#KellerWadsley16), [Ludlow et al 16](#LudlowEtAl16)). These early simulations were not found conclusive in [Lelli et al 16, section 8.2](#LelliEtAl16). But more detailed analysis ([PSF 18](#PSF18)) and more refined simulation ([Dutton-Maccio-Obreja-Buck 19](#DuttonMaccioObrejaBuck19)) has then been claimed to confirm the statement.

A conceptual explanation of the mechanism by stellar feedback is discussed in [GBFH 19](#GBFH19).

### Missing satellites?
 {#MissingSatellites}

On the apparent resolution of the [missing satellite problem](https://en.wikipedia.org/wiki/Dwarf_galaxy_problem): 

[Garrison-Kimmel et al. 17 ](#GarrisonKimmel17), see [Garrison-Kimmel 18](#GarrisonKimmel18)


\linebreak


## Related concepts

* [[bullet cluster]]

* [[fuzzy dark matter]]

* [[dark energy]], [[dark radiation]]

* [[standard model of cosmology]]

* [[MOND]]


## References

### General

Review includes

* {#Einasto09} Jaan Einasto, _Dark matter_ ([arXiv:0901.0632](https://arxiv.org/abs/0901.0632)) 2009

* [[Syksy Räsänen]], _Dark matter_ cosmo 2015 lecture notes ([pdf](http://www.courses.physics.helsinki.fi/teor/cos1/cosmo2015_07.pdf))

* Wikipedia, _[Dark matter](http://en.wikipedia.org/wiki/Dark_matter)_

* [[Matthew Strassler]], _[Current hints of dark matter](http://profmattstrassler.com/articles-and-posts/relativity-space-astronomy-and-cosmology/dark-matter/current-hints-of-dark-matter-413/)_

* {#Resonaances} Resonaances, _[How many neutrinos in the sky](http://resonaances.blogspot.de/2013/01/how-many-neutrinos-in-sky.html)_

* {#BertoneHooper16} Gianfranco Bertone, Dan Hooper, _A History of Dark Matter_ ([arXiv:1605.04909](https://arxiv.org/abs/1605.04909))

* {#Hooper18} [[Daniel Hooper]], _In Defense of Dark Matter_, 2018 ([web](http://online.kitp.ucsb.edu/online/cdm-c18/hooper/))

Discussion of possible matter representations that could serve as dark matter:

* Marco Cirelli, Nicolao Fornengo, [[Alessandro Strumia]], _Minimal Dark Matter_, Nucl.Phys.B753:178-194, 2006 ([arXiv:hep-ph/0512090](https://arxiv.org/abs/hep-ph/0512090))

Discussion of [[neutrino]]-dark matter: 

* {#NeutrinoWhite16} _A White Paper on keV Sterile Neutrino Dark Matter_,  Journal of Cosmology and Astroparticle Physics, Volume 2017, January 2017 ([arXiv:1602.04816](https://arxiv.org/abs/1602.04816))

Issues with defining gravitating mass on non-stationary spacetimes:

* Zhi-Wei Wang, Samuel L. Braunstein, _Could dark matter be a natural consequence of a dynamical universe?_ ([arXiv:2011.09923](https://arxiv.org/abs/2011.09923))


### Evidence
 {#Evidence}

Evidence for dark matter on large cosmic scales is extremely strong, see the above reviews (...). Evidence on smaller scales, starting around the scale of galaxies is problematic, see the above reviews (...). In particular, as yet there is no direct detection of any dark matter particle.

(...)



Outlook on prospect of direct detection of dark matter, as of 2018:

* Gianfranco Bertone, Tim M. P. Tait, _A New Era in the Quest for Dark Matter_, Nature volume 562, pages 51–56 (2018)  ([arXiv:1810.01668](https://arxiv.org/abs/1810.01668))

Argument that dark matter has already be seen across a range of direct detection experiments, but mis-interpreted as noise, due to negligence of the possibility of [[inelastic scattering|inelastic]] [[plasmon]] excitations in [[crystal|crystalline]] [[solid state physics|solid state]] detector materials:

* {#KBKK20} Noah Kurinsky, Daniel Baxter, Yonatan Kahn, Gordan Krnjaic, _A Dark Matter Interpretation of Excesses in Multiple Direct Detection Experiments_ ([arXiv:2002.06937](https://arxiv.org/abs/2002.06937))

* Yonatan Kahn, from slide 27 on in: _Dark matter review_, talk at Lake Louise Winter Institute, 2020 ([cern:event/846070/contributions/3693217/](https://indico.cern.ch/event/846070/contributions/3693217/))

Claimed rebuttal:

* Alan E. Robinson, Émile Michaud, _Comment on A dark matter interpretation of excesses in multiple direct detection experiments [arXiv:2002.06937]_ ([arXiv:2002.08893](https://arxiv.org/abs/2002.08893))


> The result of [Kurinsky et al.](#KBKK20) should not be taken as evidence for dark matter, although it does highlight the ongoing need to investigate the effect of collective modes how [sic] we detect radiation.

Reply:

* Noah Kurinsky, Daniel Baxter, Yonatan Kahn, Gordan Krnjaic, Peter Abbamonte, _Reply to Robinson and Michaud, arXiv:2002.08893_ ([arXiv:2003.00101](https://arxiv.org/abs/2003.00101))

> the points raised by RM do not invalidate our primary conclusions, as they pertain to a much different energy scale than we discuss in our paper.



### Core-cusp problem
  {#ReferencesCoreCuspProblem}

* {#ESH01} Amr El-Zant, Isaac Shlosman, Yehuda Hoffman, _Dark Halos: The Flattening of the Density Cusp by Dynamical Friction_,  The Astrophysical Journal, Volume 560, Number 2 ([arXiv:astro-ph/0103386](https://arxiv.org/abs/astro-ph/0103386))

* {#PontzenGovernato14} Andrew Pontzen, Fabio Governato, _Cold dark matter heats up_, Nature, 506, 171 - 178 (13 Feb 2014) ([arXiv:1402.1764](https://arxiv.org/abs/1402.1764))

* Jose Oñorbe, Michael Boylan-Kolchin, James S. Bullock, Philip F. Hopkins, Dušan Kerěs, Claude-André Faucher-Giguère, Eliot Quataert, Norman Murray, _Forged in FIRE: cusps, cores, and baryons in low-mass dwarf galaxies_, Monthly Notices of the Royal Astronomical Society, Volume 454, Issue 2, 1 December 2015 ([arXiv:1502.02036](https://arxiv.org/abs/1502.02036)) 

* [[Justin Read]], O. Agertz, M. L. M. Collins, _Dark matter cores all the way down_, Monthly Notices of the Royal Astronomical Society, Volume 459, Issue 3, 1 July 2016 ([arXiv:1508.04143](https://arxiv.org/abs/1508.04143))

* {#ReadWalkerSteger18} [[Justin Read]], M. G. Walker, P. Steger, _Dark matter heats up in dwarf galaxies_, Monthly Notices of the Royal Astronomical Society  ([arXiv:1808.06634](https://arxiv.org/abs/1808.06634), [doi:10.1093/mnras/sty3404](https://doi.org/10.1093/mnras/sty3404),  [talk recording](http://online.kitp.ucsb.edu/online/cdm-c18/read/), [press release](https://www.surrey.ac.uk/news/dark-matter-move))

* {#Read19} [[Justin Read]], _[Dark matter heats up in dwarf galaxies](https://www.simonsfoundation.org/event/dark-matter-heats-up-in-dwarf-galaxies/)_, Simons Foundation Lecture 2019

See also

* Wikipedia, _[Cuspy halo problem](https://en.wikipedia.org/wiki/Cuspy_halo_problem)_


### Computer simulation
 {#ReferencesComputerSimulation}

Discussion of computer simulation of [[dark matter]] [[structure formation]] on [[galaxy]]-scales:

* {#Hopkins17} Hopkins et al. _FIRE-2 Simulations: Physics versus Numerics in Galaxy Formation_. Monthly Notices of the Royal Astronomical Society, Volume 480, Issue 1, 11 October 2018, Pages 800–863 ([arXiv:1702.06148](https://arxiv.org/abs/1702.06148), [doi:10.1093/mnras/sty1690](https://doi.org/10.1093/mnras/sty1690))

* {#ElBadry18} El-Badry et al. _Gas Kinematics in FIRE Simulated Galaxies Compared to Spatially Unresolved HI Observations_, Monthly Notices of the Royal Astronomical Society, Volume 477, Issue 2, 21 June 2018, Pages 1536–1548 ([arXiv:1801.03933](https://arxiv.org/abs/1801.03933), [doi:10.1093/mnras/sty730](https://doi.org/10.1093/mnras/sty730))

* {#GarrisonKimmel17} Shea Garrison-Kimmel et al. _Not so lumpy after all: modeling the depletion of dark matter subhalos by Milky Way-like galaxies_ ([arXiv:1701.03792](https://arxiv.org/abs/1701.03792))

* {#GarrisonKimmel18} Shea Garrison-Kimmel, _Next-generation Galaxy Formation Simulations with FIRE_, 2018 ([video recording](https://youtu.be/sSkrm66uDvw))

See also

* Jie Wang, Sownak Bose, Carlos S. Frenk, Liang Gao, Adrian Jenkins, Volker Springel, Simon D. M. White, _Universality in the structure of dark matter haloes over twenty orders of magnitude in halo mass_ ([arXiv:1911.09720](https://arxiv.org/abs/1911.09720))

### Galaxy rotation curves

On the [[radial acceleration relation]]:

* {#CintioLelli15} Arianna Di Cintio, Federico Lelli, _The mass discrepancy acceleration relation in a $\Lambda CDM$ context_, Monthly Notices of the Royal Astronomical Society: Letters, Volume 456, Issue 1, 11 February 2016, Pages L127–L131 ([arXiv:1511.06616](https://arxiv.org/abs/1511.06616), [doi:10.1093/mnrasl/slv185](https://doi.org/10.1093/mnrasl/slv185))

* {#SantosSantosEtAl15} Isabel M. Santos-Santos et al. _The distribution of mass components in simulated disc galaxies_ ([arXiv:1510.02474](https://arxiv.org/abs/1510.02474))

* {#KellerWadsley16} B.W. Keller, J.W. Wadsley, _$\Lambda CDM$ is Consistent with SPARC Radial Acceleration Relation_ ([arXiv:1610.06183](https://arxiv.org/abs/1610.06183))

* {#LudlowEtAl16} Aaron D. Ludlow et. al. _The Mass-Discrepancy Acceleration Relation: a Natural Outcome of Galaxy Formation in Cold Dark Matter halos_, Phys. Rev. Lett. 118, 161103 (2017) ([arXiv:1610.07663](https://arxiv.org/abs/1610.07663))

* {#PSF18} Chiara Di Paolo, Paolo Salucci, Jean Philippe Fontaine, _The Radial Acceleration Relation (RAR): the crucial cases of Dwarf Discs and of Low Surface Brightness galaxies_, ApJ 2019 ([arXiv:1810.08472](https://arxiv.org/abs/1810.08472))


* {#PSF18} Chiara Di Paolo, Paolo Salucci, Jean Philippe Fontaine, _The Radial Acceleration Relation (RAR): the crucial cases of Dwarf Discs and of Low Surface Brightness galaxies_, ApJ 2019 ([arXiv:1810.08472](https://arxiv.org/abs/1810.08472))

* {#DuttonMaccioObrejaBuck19} Aaron A. Dutton, Andrea V. Macciò, Aura Obreja, Tobias Buck, _NIHAO XVIII: Origin of the MOND phenomenology of galactic rotation curves in a LCDM universe_ ([arXiv:1902.06751](https://arxiv.org/abs/1902.06751))

Critical comments in

* {#LelliEtAl16} Federico Lelli, Stacy S. McGaugh, James M. Schombert, Marcel S. Pawlowski, section 8.2 of _One Law To Rule Them All: The Radial Acceleration Relation of Galaxies_ ([arXiv:1610.08981](https://arxiv.org/abs/1610.08981))

Conceptual explanation by stellar feedback:

* {#GBFH19} Michael Y. Grudić, Michael Boylan-Kolchin, Claude-André Faucher-Giguère, Philip Hopkins, _Stellar feedback sets the universal acceleration scale in galaxies_ ([arxiv:1910.06345](https://arxiv.org/abs/1910.06345))



### Axions

The observation that the "invisible [[axion]]" is a candidate for dark 
matter is due to three groups:

* {#PreskillWiseWilcek83} [[John Preskill]], M. Wise, [[Frank Wilcek]], _Cosmology of the invisible axion_, Phys. Lett. B 120:127-32 (1983)

* {#AbbottSikivie83} L.F. Abbott, P. Sikivie, _A Cosmological Bound on the Invisible Axion_, Phys.Lett. B120:133-36 (1983)

* {#DineFischler83} [[Michael Dine]], [[Willy Fischler]], _The Not So Harmless Axion_, Phys.Lett. B120:137-141 (1983)

A proposal that [[axions]] account for [[fuzzy dark matter]], and thus fix the [[WIMP]] model for dark matter with its problem of reproducing galactic rotation curves, is in

* {#HOTW16} Lam Hui, Jeremiah P. Ostriker, Scott Tremaine, [[Edward Witten]], _On the hypothesis that cosmological dark matter is composed of ultra-light bosons_, Phys. Rev. D 95, 043541 (2017) ([arXiv:1610.08297](https://arxiv.org/abs/1610.08297))

### Lightest super-partner 


The observation that the lightest supersymmetric particle would be a natural dark matter candidate goes back to 

* {#EHNOS84} [[John Ellis]],  J.S. Hagelin, Dimitri V. Nanopoulos, [[Keith Olive]], M. Srednicki  _Supersymmetric relics from the Big Bang_, Nuclear Physics B 238[2]: 453-76, 1984 ([SPIRE](http://inspirehep.net/record/191839?ln=en))

with review in 

* {#EllisOlive10} [[John Ellis]], [[Keith Olive]], _Supersymmetric Dark Matter Candidates_ ([arXiv:1001.3651](http://arxiv.org/abs/1001.3651))

### Gravitinos
 {#ReferencesGravitinos}

On the [[gravitino]] as a dark matter candidate:

* {#EllisOlive10} [[John Ellis]], [[Keith Olive]], _Supersymmetric Dark Matter Candidates_ ([arXiv:1001.3651](http://arxiv.org/abs/1001.3651))


A proposal for super-heavy [[gravitinos]] as [[dark matter]], by embedding [[D=4 N=8 supergravity]] into [[E10]]-[[U-duality]]-invariant [[M-theory]]:

* {#MeissnerNicolai18a} Krzysztof A. Meissner, [[Hermann Nicolai]], _Standard Model Fermions and Infinite-Dimensional R-Symmetries_, Phys. Rev. Lett. 121, 091601 (2018) ([arXiv:1804.09606](https://arxiv.org/abs/1804.09606))

* {#MeissnerNicolai18b} Krzysztof A. Meissner, [[Hermann Nicolai]], _Planck Mass Charged Gravitino Dark Matter_, Phys. Rev. D 100, 035001 (2019) ([arXiv:1809.01441](https://arxiv.org/abs/1809.01441))

following the proposal towards the end of

* {#GellMann83} [[Murray Gell-Mann]], introductory talk at _[Shelter Island II](https://en.wikipedia.org/wiki/Shelter_Island_Conference)_, 1983 ([[Gell-Mann_ShelterIslandII_1983.pdf:file]]) 

  in: _Shelter Island II: Proceedings of the 1983 Shelter Island Conference on Quantum Field Theory and the Fundamental Problems of Physics_. MIT Press. pp. 301&#8211;343. ISBN 0-262-10031-2.

Further discussion:

* Krzysztof A. Meissner, [[Hermann Nicolai]], _Supermassive gravitinos and giant primordial black holes_ ([arXiv:2007.11889](https://arxiv.org/abs/2007.11889))


### Flavour anomalies

Attempts to link dark matter to the apparently observed [[flavour anomalies]]:

* {#Baek19} Seungwon Baek, _Scalar dark matter behind $b \to s \mu \mu$ anomaly_ ([arXiv:1901.04761](https://arxiv.org/abs/1901.04761))

* {#CCMRM19} D.G. Cerdeno, A. Cheek, P. Martin-Ramiro, J.M. Moreno, _B anomalies and dark matter: a complex connection_ ([arXiv:1902.01789](https://arxiv.org/abs/1902.01789))


[[!redirects cold dark matter]]


[[!redirects core-cusp problem]]
[[!redirects core-cusp problems]]

[[!redirects cusp-core problem]]
[[!redirects cusp-core problems]]


[[!redirects cuspy halo problem]]
[[!redirects cuspy halo problems]]

[[!redirects missing satellite problem]]
[[!redirects missing satellite problems]]

[[!redirects dwarf galaxy problem]]
[[!redirects dwarf galaxy problems]]



