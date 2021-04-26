

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
#### Topological physics
+--{: .hide}
[[!include topological physics -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}



## Idea


> [[Tony Skyrme|Skyrme]] had studied with attention [[On Vortex Atoms|Kelvin's ideas on vortex atoms]]. 

> ([Ranada-Trueba 01, p. 200](On+Vortex+Atoms#RanadaTrueba01))

A _Skyrmion_ is a [[soliton]] in certain ([[flavour physics|flavour]]) [[gauge field theories]]. The concept exists quite generally (see [Rho-Zahed 16](#RhoZahed16)), but its original use ([Skyrme 62](#Skyrme62)), and still the most important one, realizes _[[baryons]]_ and [[atomic nuclei]] as [[solitons]] in the [[light meson]]-[[field (physics)|fields]] of [[chiral perturbation theory]], thus serving as a putative theory of [[non-perturbative quantum field theory|non-perturbative]] [[quantum chromodynamics]], the formulation of the latter being by and large an open problem (due to [[confinement]], see _[[mass gap problem]]_). 


\begin{center}
<img src="https://ncatlab.org/nlab/files/FirstEightSkyrmions.jpg" width="660">
\end{center}

> graphics grabbed from [Manton 11](#Manton11)



\begin{center}
<img src="https://ncatlab.org/nlab/files/SkyrmionB20.jpg" width="500">
\end{center}

> graphics grabbed form [FLM 12](#FLM12)


## Definition
 {#Definition}

For $G$ a [[simple Lie group]] with [[semisimple Lie algebra]] denoted $\mathfrak{g}$, with [[Lie bracket]] $[-,-]$ and with [[Killing form]] $\langle -,-\rangle$,
the Skyrme fields are [[smooth functions]]

$$
  U \;\colon\; \mathbb{R}^3 \longrightarrow G
$$

and the Skyrme [[Lagrangian density]] is

$$
  \mathbf{L}
  \;=\;
  -\tfrac{1}{2}
  \left\langle
    U^{-1}\mathbf{d}U \wedge \star U^{-1}\mathbf{d}U
  \right\rangle
  +
  \tfrac{1}{16}
  \Big(
    \big[
       U^{-1}\mathbf{d}U
       \wedge
       U^{-1}\mathbf{d}U
    \big]
    \wedge \star
    \big[
       U^{-1}\mathbf{d}U
       \wedge
       U^{-1}\mathbf{d}U
    \big]  
  \Big)
$$

where $U^{-1} \mathbf{d}U = U^\ast \theta$ is the [[pullback of differential forms|pullback]] of the [[Maurer-Cartan form]] on $G$, and where $\ast$ denotes the standard [[Hodge star operator]] on [[Euclidean space]] $\mathbb{R}^3$. 

(e.g. [Manton 11 (2.2)](#Manton11), [Cork 18b (1)](#Cork18b)) 

A _classical Skyrmion_ is a solution to the corresponding [[Euler-Lagrange equations]] which

1. is [[vanishing at infinity]] $U(r \to \infty) \to e \in G$

1. [[critical point|extremizes]] the [[energy]] implied by the above [[Lagrangian]].

## Properties

### Relation to chiral perturbation theory

* [[Dmitri Diakonov]], [[Victor Petrov]], _Exotic baryon resonances in the Skyrme model_ ([arXiv:0812.1212](https://arxiv.org/abs/0812.1212), [doi:10.1142/9789814704410_0004](https://doi.org/10.1142/9789814704410_0004)), Chapter 3 in: _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

> It is astounding that [[Tony Skyrme|Skyrme]] had suggested [[Skyrmion|his model]] as early as in 1961 before it has been generally accepted that [[pions]] are (pseudo) [[Goldstone bosons]] associated with the [[spontaneous symmetry breaking|spontaneous breaking]] of [[chiral symmetry]], and of course long before [[QCD|Quantum Chromodynamics (QCD)]] has been put forward as the microscopic theory of [[strong nuclear force|strong interactions]].

> The revival of the Skyrme idea in 1983 is [due to Witten](Skyrmion#Witten83) who explained the _raison d'ˆetre_ of the [[Skyrmion|Skyrme model]] from the viewpoint of [[QCD]]. In the [[chiral perturbation theory|chiral limit]] when the light [[quark]] masses $m_u$, $m_d$, $m_s$ tend to zero, such that the octet of the pseudoscalar mesons [[pion|π]], [[kaon|K]] , η become nearly massless (pseudo) [[Goldstone bosons]], they are the lightest degrees of freedom of [[QCD]]. The [[effective field theory|effective]] chiral Lagrangian (EχL) for pseudoscalar mesons, understood as an infinite expansion in the derivatives of the pseudoscalar (or chiral) fields, encodes, in principle, full information about QCD. The famous two-term Skyrme Lagrangian can be understood as a low-energy truncation of this infinite series. Witten has added an important four-derivative [[WZW-term|Wess–Zumino term]] to the original Skyrme Lagrangian and pointed out that the overall coefficient in front of the EχL is proportional to the number of quark [[color charge|colours]] $N_c$.

> $[...]$

> Soon after Witten's work it has been realized that it is possible to bring the Skyrme model and the Skyrmion even closer to QCD and to the more customary language of constituent quarks. It has been first noticed $[$[6](#DiakonovEides83), [7a](#DharWadia84), [7b](#DarShankarWadia85), [8](#DiakonovPetrov86)$]$ that a simple chiral invariant Lagrangian for massive (constituent) quarks $Q$ interacting with the octet chiral field $\pi_A$ $(A = 1, ..., 8)$,

> $$\mathcal{L} = \overline{Q} \left( \partial\!\!\!\!/ - M e^{ \tfrac{i \pi^A \lambda^A \gamma_5}{F_\pi}  }  \right) Q$$

> induces, via a quark loop in the external pseudoscalar fields (see Fig. 3.1), the EχL whose lowest-derivative terms coincide with the Skyrme Lagrangian, including
automatically the Wess–Zumino term, with the correct coefficient!

<center>
<img src="https://ncatlab.org/nlab/files/DiakonovPetrovQuarkLoop.jpg" width="600">
</center>

> $[...]$

> The condition that the winding number of the trial field is unity needs to be imposed to get a deeply bound state, that is to guarantee that the baryon number is unity. $[$[9](#DiakonovPetrovPobylitsa88)$]$ The Skyrmion is, thus, nothing but the **mean chiral field binding quarks in a baryon**.

<center>
<img src="https://ncatlab.org/nlab/files/DiakonovPetrovMeanField.jpg" width="600">
</center>

\linebreak

* {#DiakonovEides83} [[Dmitri Diakonov]], Michael I. Eides, _Chiral Lagrangian from a functional integral over quarks_, JETP Letters 38.7 (1983): 433-436 ([pdf](http://jetpletters.ac.ru/ps/1483/article_22635.pdf), [[DiakonovEides83.pdf:file]])

* {#DharWadia84} A. Dhar, Spenta R. Wadia, _Nambu—Jona-Lasinio Model: An Effective Lagrangian for Quantum Chromodynamics at Intermediate Length Scales_, Phys. Rev. Lett. 52, 959 (1984) ([doi:10.1103/PhysRevLett.52.959](https://doi.org/10.1103/PhysRevLett.52.959))

* {#DarShankarWadia85} Avinash Dhar, R. Shankar, Spenta R. Wadia, _Nambu–Jona-Lasinio–type effective Lagrangian: Anomalies and nonlinear Lagrangian of low-energy, large-N QCD_, Phys. Rev. D 31, 3256 (1985) ([doi:10.1103/PhysRevD.31.3256](https://doi.org/10.1103/PhysRevD.31.3256))

* {#DiakonovPetrov86} [[Dmitri Diakonov]], [[Victor Petrov]], _A theory of light quarks in the instanton vacuum_, Nuclear Physics B Volume 272, Issue 2, 21 July 1986, Pages 457-489 (<a href="https://doi.org/10.1016/0550-3213(86)90011-8">doi:10.1016/0550-3213(86)90011-8</a>)

* {#DiakonovPetrovPobylitsa88} [[Dmitri Diakonov]], [[Victor Petrov]], P.V. Pobylitsa, _A Chiral Theory of Nucleons_, Nucl. Phys. B306 (1988) 809 ([spire:247700](http://inspirehep.net/record/247700), <a href="https://doi.org/10.1016/0550-3213(88)90443-9">doi:10.1016/0550-3213(88)90443-9</a>)




### As a model for atomic nuclei
 {#AsAModelForBaryonsAndNuclei}

Skyrmions are candidate models for [[baryons]] and even some aspects of [[atomic nuclei]] ([Riska 93](#Riska93), [Battye-Manton-Sutcliffe 10](#BattyeMantonSutcliffe10), [Manton 16](#Manton16), [Naya-Sutcliffe 18a](#NayaSutcliffe18a), [Naya-Sutcliffe 18b](#NayaSutcliffe18b}).


For instance various resonances of the [[carbon]] [[nucleus]] are modeled well by a Skyrmion with baryon number 12 ([Lau-Manton 14](#LauManton14)): 

\begin{center}
<img src="https://ncatlab.org/nlab/files/SkyrmionB12.jpg" width="300">
\end{center}

> graphics grabbed form [Lau-Manton 14](#LauManton14)

{#IncludingTowerOfMesons} For Skyrmion models of nuclei to match well to [[experiment]], not just the [[pion field]] but also the tower of [[vector mesons]] need to be included in the construction. 

Including the [[rho meson]] gives good results for light nuclei ([Naya-Sutcliffe 18a](#NayaSutcliffe18a), [Naya-Sutcliffe 18b](#NayaSutcliffe18b))


\begin{center}
<img src="https://ncatlab.org/nlab/files/SkyrmionsWithRho.jpg" width="800">
\end{center}

> graphics grabbed form [Naya-Sutcliffe 18a](#NayaSutcliffe18a)

An analogous discussion for inclusion of [[omega-mesons]] is in [Gudnason-Speight 20](#GudnasonSpeight20).


### As a holographic boundary theory
 {#AsBoundaryFieldTheory}

The Skyrmions in 4d spacetime [above](#Definition), with [[vector meson]]-contributions included, are the [[AdS-CFT|holographic]]/[[KK-theory]] reduction of [[instantons]] in [[D=5 Yang-Mills theory]] ([Sakai-Sugimoto 04, Section 5.2](#SakaiSugimoto04), [Sakai-Sugimoto 05, Section 3.3](#SakaiSugimoto05), reviewed in [Sugimoto 16, Section 15.3.4](#Sugimoto16), [Bartolini 17, Section 2](#Bartolini17).

This phenomenon is essentially the theorem of [Atiyah-Manton 89](#AtiyahManton89), this is highlighted and developed in [Sutcliffe 10](#Sutcliffe10), [Sutcliffe 15](#Sutcliffe15).

In this way Skyrmions (and hence [[baryons]] and [[atomic nuclei]], see [below](#AsAModelForBaryonsAndNuclei)) appear in the [[Witten-Sakai-Sugimoto model]], which realizes (something close to) [[non-perturbative quantum field theory|non-perturbative]] [[QCD]] as a [[D4-D8-brane intersection|D4/D8]]-[[intersecting D-brane model]] described by the [[AdS-QCD correspondence]] ("[[holographic QCD]]").

This way, via the equivalence between [[D4-D8-brane intersections]] with [[instantons]] in the [[D8-brane]]-[[worldvolume]], the Skyrme model becomes equivalent to a model of [[baryons]] by [[wrapped brane|wrapped]] [[D4-branes]] ([Sugimoto 16, 15.4.1](#Sugimoto16)):

\begin{center}
<img src="https://ncatlab.org/nlab/files/BaryonsAsD4Branes.jpg" width="800">
\end{center}

> graphics grabbed from [Sugimoto 16](#Sugimoto16)


\linebreak

### As the ultimate bag model

> The [[Skyrmion]] is the ultimate [[soliton|topological]] [[quark bag model|bag model]] with zero size bag radius, lending further credence to the [[Cheshire cat principle]]. ([Nielsen-Zahed 09](Cheshire+cat+principle#NielsenZahed09))



## Related concepts

* [[soliton]], [[vortex]] 

* [[instanton]], [[caloron]]

* [[baryon]]

* [[Witten-Sakai-Sugimoto model]] for [[non-perturbative effect|non-perturbative]] [[QCD]]

[[!include effective field theories of nuclear physics -- contents]]


## History

From [Rho-Zahed 10, Preface](#RhoZahed10):

> Two path-breaking developments took place consecutively in physics in the years 1983 and 1984: First in nuclear physics with the rediscovery of Skyrme’s seminal idea on the structure of baryons and then a ["revolution" in string theory](string+theory#ReferencesHistory) in the following year. 

> $[\cdots]$ at that time the most unconventional idea of Skyrme that [[fermion|fermionic]] [[baryons]] could emerge as topological [[solitons]] from [[π-meson]] cloud was confirmed in the context of [[quantum chromodynamics]] (QCD) in the large number-of-[[color charge|color]] ($N_c$) limit. It also confirmed how the solitonic structure of [[baryons]], in particular, the [[nucleons]], reconciled nuclear physics — which had been making an impressive progress [[phenomenology|phenomenologically]], aided mostly by [[experiments]] — with [[QCD]], the fundamental theory of [[strong nuclear force|strong interactions]]. Immediately after the rediscovery of what is now generically called "skyrmion" came the [first string theory revolution](string+theory#ReferencesHistory) which then took most of the principal actors who played the dominant role in reviving the skyrmion picture away from that problem and swept them into the mainstream of [[string theory]] reaching out to a much higher [[energy]] [[scale]]. This was in some sense unfortunate for the skyrmion model _per se_ but fortunate for nuclear physics, for it was then mostly nuclear theorists who picked up what was left behind in the wake of the celebrated string revolution and proceeded to uncover fascinating novel aspects of nuclear structure which otherwise would
have eluded physicists, notably concepts such as the ‘Cheshire Cat phenomenon’ in hadronic dynamics.

> What has taken place since 1983 is a beautiful story in [[physics]]. It has not only profoundly influenced nuclear physics — which was Skyrme’s original aim — but also brought to light hitherto unforseen phenomena in other areas of physics, such as [[condensed matter physics]], [[astrophysics]] and [[string theory]].

## References

### General

The original articles are

* {#Skyrme62} [[Tony Skyrme]], _A unified field theory of mesons and baryons_, Nuclear Physics Volume 31, March–April 1962, Pages 556-569 (<a href="https://doi.org/10.1016/0029-5582(62)90775-7">doi:10.1016/0029-5582(62)90775-7</a>)


* {#AdkinsNappiWitten83} [[Gregory Adkins]], [[Chiara Nappi]], [[Edward Witten]], _Static Properties of Nucleons in the Skyrme Model_, Nucl. Phys. B228 (1983) 552 ([spire:190174](http://inspirehep.net/record/190174), <a href="https://doi.org/10.1016/0550-3213(83)90559-X">doi:10.1016/0550-3213(83)90559-X</a>)


Review:

* [[Edward Witten]], _Skyrmions and QCD_, in: Current Algebra and Anomalies, pp. 529-537, World Scientific (1985) ([doi:10.1142/9789814503044_0010](https://doi.org/10.1142/9789814503044_0010))

> If one assumes [[confinement]], then $[$[[SU(N)]]$]$-[[QCD]] is equivalent to a theory of [[mesons]] (and [[glueballs]]) in which the (quartic) [[meson]] [[coupling constant]] is $1/N$.

> $[..]$

> $[$here to stress that$]$ [[QCD]] is equivalent for any $N$, including $N=3$, to a meson theory in which $1/N$ is the coupling constant, [[large N limit|Large N]] is special only in that the meson coupling is only moderately weak.

> $[..]$

> These considerations remove all of the obstacles to interpreting baryons as the solitons of meson physics

> $[..]$

> There is every evidence that Skyrmions physics with varying couplings reproduces QCD baryons of varying $N$.


> $[..]$

> The [[large N limit|1/N expansion]] of [[QCD]], as understood from [[Feynman diagrams]], is the road map which makes the success of  [[Skyrmion]] physics rationally comprehensible.


* [[Eric D'Hoker]], Edward Farhi, _The Proton as a Topological Twist: A model of elementary particles, without reference to quarks, contains topological structures whose properties match experimental observations remarkably well_, American Scientist Vol. 73, No. 6 (November-December 1985), pp. 533-540 ([jstor:27853483](https://www.jstor.org/stable/27853483))


* {#BrownRho88} G. E. Brown, [[Mannque Rho]], _The Chiral Bag_, Comments Nucl. Part. Phys. 18 (1988) no.1, 1-29 ([spire:18025](http://inspirehep.net/record/18025))

  (in relation to the [[bag model of quark confinement]])

* [[Igor Klebanov]], _Strangeness in the Skyrme model_, in: D. Vauthrin, F. Lenz, J. W. Negele,  _Hadrons and Hadronic Matter_, Plenum Press 1989 ([doi:10.1007/978-1-4684-1336-6](https://link.springer.com/book/10.1007/978-1-4684-1336-6))

  (with emphasis on includion [[heavy mesons]])

* [[Maciej Nowak]], [[Mannque Rho]], [[Ismail Zahed]], Chapter 7 of: _[[Chiral Nuclear Dynamics]]_,  World Scientific 1996 ([doi:10.1142/1681](https://doi.org/10.1142/1681))

* {#Weigel96} [[Herbert Weigel]], _Baryons as Three Flavor Solitons_,  	Int. J. Mod. Phys. A11:2419-2544, 1996 ([arXiv:hep-ph/9509398](https://arxiv.org/abs/hep-ph/9509398), [cds:288541](http://cds.cern.ch/record/288541), [doi:10.1142/S0217751X96001218](https://doi.org/10.1142/S0217751X96001218))

* {#Weigel08} [[Herbert Weigel]], _Chiral Soliton Models for Baryons_,  Lecture Notes in Physics book series, volume 743, Springer 2008 ([doi:10.1007/978-3-540-75436-7](https://doi.org/10.1007/978-3-540-75436-7))

* Yong-Liang Ma, Masayasu Harada, _Lecture notes on the Skyrme model_ ([arXiv:1604.04850](https://arxiv.org/abs/1604.04850), [spire:1448311](https://inspirehep.net/literature/1448311))


* {#RhoZahed16} [[Mannque Rho]], [[Ismail Zahed]] (eds.) _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

See also

* Wikipedia, _[Skyrmion](https://en.wikipedia.org/wiki/Skyrmion)_


Further development:

* {#Manton11} [[Nicholas Manton]], _Classical Skyrmions -- Static Solutions and Dynamics_, Mathematical Methods in the applied Sciences, Volume35, Issue10, 2012, Pages 1188-1204 ([arXiv:1106.1298](https://arxiv.org/abs/1106.1298), [doi:10.1002/mma.2512]( https://doi.org/10.1002/mma.2512))

* {#NST11} Atsushi Nakamula, Shin Sasaki, Koki Takesue, _Atiyah-Manton Construction of Skyrmions in Eight Dimensions_, JHEP 03 (2017) 076 ([arXiv:1612.06957](https://arxiv.org/abs/1612.06957))

* {#FLM12} D. T. J. Feist, P. H. C. Lau, [[Nicholas Manton]], _Skyrmions up to Baryon Number 108_ ([arXiv:1210.1712](https://arxiv.org/abs/1210.1712))

* {#Manton17} [[Nicholas Manton]], _Lightly Bound Skyrmions, Tetrahedra and Magic Numbers_ ([arXiv:1707.04073](https://arxiv.org/abs/1707.04073))

* Avner Karasik, _Skyrmions, Quantum Hall Droplets, and one current to rule them all_ ([arXiv:2003.07893](https://arxiv.org/abs/2003.07893))


* [[Carlos Naya]], K. Oles, _Background fields and self-dual Skyrmions_ ([arXiv:2004.07069](https://arxiv.org/abs/2004.07069))

* C. Adam, K. Oles, A. Wereszczynski, _The Dielectric Skyrme model_ ([arXiv:2005.00018](https://arxiv.org/abs/2005.00018))

* Sven Bjarke Gudnason, Marco Barsanti, Stefano Bolognesi, _Near-BPS baby Skyrmions_ ([arXiv:2006.01726](https://arxiv.org/abs/2006.01726))


* Sven Bjarke Gudnason, _Dielectric Skyrmions_ ([arXiv:2009.03082](https://arxiv.org/abs/2009.03082))

* Francisco Correa, Andreas Fring, Takanobu Taira, _Complex BPS Skyrmions with real energy_ ([arXiv:2102.05781](https://arxiv.org/abs/2102.05781))

* [[Chris Halcrow]], [[Thomas Winyard]], _A consistent two-skyrmion configuration space from instantons_ ([arXiv:2103.15669](https://arxiv.org/abs/2103.15669))



[[scattering amplitudes]]:

* T. Gisiger, M. B. Paranjape, _Skyrmion-Skyrmion Scattering_ ([arXiv:hep-th/9310050](https://arxiv.org/abs/hep-th/9310050))

[[nucleon]]$\,$[[interaction]]:

* [[Chris Halcrow]], [[Derek Harland]], _An attractive spin-orbit potential from the Skyrme model_ ([arXiv:2007.01304](https://arxiv.org/abs/2007.01304))

* [[Derek Harland]], [[Chris Halcrow]], _Nucleon-nucleon potential from skyrmion dipole interactions_ ([arXiv:2101.02633](https://arxiv.org/abs/2101.02633))

> The topic of this paper has a history of mistakes and
sign errors in the literature. For both these reasons, we present our calculation in painstaking detail. $[...]$.  

> Compared with earlier attempts based on the Skyrme model, we obtain a very good match with the long-range parts of the Paris potential. Overall, these results provide an excellent starting point for describing the nucleon-nucleon interaction from the Skyrme model. Importantly, we can describe many features of the nucleon-nucleon interaction using a purely pionic theory. $[...]$

> our approach could be adapted to any model which treats nuclei as quantised solitons. This includes [[holographic QCD]], where nuclei are described as instantons on a curved spacetime

* [[Horatiu Nastase]], [[Jacob Sonnenschein]], _A $T \bar T$-like deformation of the Skyrme model and the Heisenberg model of nucleon-nucleon scattering_ ([arXiv:2101.08232](https://arxiv.org/abs/2101.08232))

  > (via [[TT deformation]])

In strong [[magnetic fields]]:

* {#ChenQiuFukushima21} Shi Chen, Zebin Qiu, Kenji Fukushima, *Skyrmions in a magnetic field and $\pi^0$ domain wall formation in dense nuclear matter* ([arXiv:2104.11482](https://arxiv.org/abs/2104.11482))







Mathematical discussion in [[differential geometry]]:

* Christian Gross, _Differential Forms on the Skyrmion Bundle_, In: Antoine JP., Ali S.T., Lisiecki W., Mladenov I.M., Odzijewicz A. (eds.) _Quantization, Coherent States, and Complex Structures_, Springer 1995 ([doi:10.1007/978-1-4899-1060-8_7](https://doi.org/10.1007/978-1-4899-1060-8_7))

and in [[algebraic topology]]:

* Christian Gross, _Topology of the skyrmion bundle_, Journal of Mathematical Physics 36, 4406 (1995) ([doi:10.1063/1.530899](https://doi.org/10.1063/1.530899))

Relation to the [[complex Hopf fibration]]:

* {#GudnasonNitta20} [[Sven Bjarke Gudnason]], [[Muneto Nitta]], _Linking number of vortices as baryon number_ ([arXiv:2002.01762](https://arxiv.org/abs/2002.01762), [spire:1778698/](http://inspirehep.net/record/1778698/))

Generalization to [[SU(N)]]:

* Pedro D. Alvarez, Sergio L. Cacciatori, Fabrizio Canfora, [[Bianca Cerchiai]], _Analytic $SU(N)$ Skyrmions at finite Baryon density_ ([arXiv:2005.11301](https://arxiv.org/abs/2005.11301))



Further resources:

* _[Geometric models of Nuclear Matter Conference 2014](https://www.kent.ac.uk/smsas/personal/skyrmions/conference.html)_ 



[[!include Skyrme hadrodynamics with vector mesons -- references ]]


[[!include Skyrme hadrodynamics with heavy mesons -- references]]


[[!include WZW term of QCD chiral perturbation theory -- references]]


[[!include hadrons as KK-modes of 5d Yang-Mills theory -- references]]



### As models for atomic nculei
 {#ReferencesAsModelsForAtomicNuclei}

Skyrmions modelling [[atomic nuclei]]:

* {#Riska93} D. O. Riska, _Baryons and nuclei as skyrmions_,  Czech J Phys (1993) 43: 449 ([doi:10.1007/BF01589856](https://doi.org/10.1007/BF01589856))

* {#BattyeMantonSutcliffe10} R. A. Battye, [[Nicholas Manton]], [[Paul Sutcliffe]], _Skyrmions and Nuclei_, pp. 3-39 (2010) ([doi:10.1142/9789814280709_0001](https://doi.org/10.1142/9789814280709_0001)) in:  [[Mannque Rho]], [[Ismail Zahed]] (eds.) _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))


* {#Manton16} [[Nicholas Manton]], _Skyrmions and Nuclei_, talk at Brookhaven National Lab, November 2016 ([pdf](https://quark.phy.bnl.gov/~pisarski/talks/Manton_SkyBNL.pdf))

* {#NayaSutcliffe18a} [[Carlos Naya]], [[Paul Sutcliffe]], _Skyrmions and clustering in light nuclei_, Phys. Rev. Lett. 121, 232002 (2018) ([arXiv:1811.02064](https://arxiv.org/abs/1811.02064)) 

* {#NayaSutcliffe18b} [[Carlos Naya]], [[Paul Sutcliffe]], _Skyrmions in models with pions and rho_, JHEP 05 (2018) 174 ([arXiv:1803.06098](https://arxiv.org/abs/1803.06098))


  APS Synopsis: _[Revamping the Skyrmion Model](https://physics.aps.org/synopsis-for/10.1103/PhysRevLett.121.232002)_, 2018 


For [[carbon]]:

* {#LauManton14} P.H.C. Lau, [[Nicholas Manton]], _States of Carbon-12 in the Skyrme Model_,  Phys. Rev. Lett. 113, 232503 (2014) ([arXiv:1408.6680](https://arxiv.org/abs/1408.6680))




### As models for neutron stars

Discussion of [[model (in theoretical physics)|models]] of [[neutron stars]] by [[Skyrmions]]:

* C. Adam, [[Carlos Naya]], J. Sanchez-Guillen, R. Vazquez, A. Wereszczynski, _BPS Skyrmions as neutron stars_, Physics Letters B
Volume 742, 6 March 2015, Pages 136-142 ([arXiv:1407.3799](https://arxiv.org/abs/1407.3799))

* C. Adam, [[Carlos Naya]], J. Sanchez-Guillen, R. Vazquez, A. Wereszczynski, _Neutron stars in the BPS Skyrme model: mean-field limit vs. full field theory_, Phys. Rev. C 92, 025802 (2015) ([arXiv:1503.03095](https://arxiv.org/abs/1503.03095))


* Xiang-Hai Liu, Yong-Liang Ma, [[Mannque Rho]], _Topology change and nuclear symmetry energy in compact-star matter_, Phys. Rev. C 99, 055808 (2019) ([arXiv:1811.10012](https://arxiv.org/abs/1811.10012))


* [[Carlos Naya]], _Neutron stars within the Skyrme model_, 	Int. J. Mod. Phys. E 28, 1930006 (2019) ([arXiv:1910.01145](https://arxiv.org/abs/1910.01145))

* C. Adam, J. Sanchez-Guillen, R. Vazquez, A. Wereszczynski, _Adding crust to BPS Skyrme neutron stars_ ([arXiv:2004.03610](https://arxiv.org/abs/2004.03610))

* Christoph Adam, Alberto García Martín-Caro, Miguel Huidobro García, Ricardo Vázquez, Andrzej Wereszczynski, _A new consistent Neutron Star Equation of State from a Generalized Skyrme model_ ([arXiv:2006.07983](https://arxiv.org/abs/2006.07983))

* Christoph Adam, Alberto García Martín-Caro, Miguel Huidobro, Ricardo Vázquez, Andrzej Wereszczynski, _Quasi-universal relations for generalized Skyrme stars_ ([arXiv:2011.08573](https://arxiv.org/abs/2011.08573))



With [[higher curvature corrections]] included ([[Starobinsky model of cosmic inflation|Starobinsky model]]):
 
* C. Adam, M. Huidobro, R. Vazquez, A. Wereszczynski, _BPS Skyrme neutron s tars in generalized gravity_ ([arXiv:2005.10834](https://arxiv.org/abs/2005.10834))


See also:

* [[Mannque Rho]], _Fractionalized Quasiparticles and the Hadron-Quark Duality in Dense Baryonic Matter_ ([arXiv:2004.09082](https://arxiv.org/abs/2004.09082))




### Relation to instantons, calorons, solitons, monopoles

The construction of Skyrmions from [[instantons]] is due to 

* {#AtiyahManton89} [[Michael Atiyah]], [[Nicholas Manton]], _Skyrmions from instantons_, Phys.  Lett.  B, 222(3):438–442, 1989 (<a href="https://doi.org/10.1016/0370-2693(89)90340-7">doi:10.1016/0370-2693(89)90340-7</a>)

The relation between skyrmions, [[instantons]], [[calorons]], [[solitons]] and [[monopoles]] is usefully reviewed and further developed in 

* {#Cork18a} [[Josh Cork]], _Calorons, symmetry, and the soliton trinity_, PhD thesis, University of Leeds 2018 ([web](http://etheses.whiterose.ac.uk/22097/))

* {#Cork18b} [[Josh Cork]], _Skyrmions from calorons_, J. High Energ. Phys. (2018) 2018: 137 ([arXiv:1810.04143](https://arxiv.org/abs/1810.04143))

based on 

* {#Sutcliffe10} [[Paul Sutcliffe]], _Skyrmions, instantons and holography_, JHEP 1008:019, 2010 ([arXiv:1003.0023](https://arxiv.org/abs/1003.0023))

which in turn relates to a [[Minkowski spacetime]]-version of the holographic realization of Skyrmions in the [[Sakai-Sugimoto model]] ([[AdS/QCD correspondence]]).



### In solid state physics

In [[solid state physics]] skyrmions in the magnetization of thin atomic layers are known as _magnetic skyrmions_. 

See:

* Wikipedia, _[Magnetic skyrmions](https://en.m.wikipedia.org/wiki/Magnetic_skyrmion)_








[[!redirects skyrmions]]

[[!redirects Skyrmion]]
[[!redirects Skyrmions]]

[[!redirects Skyrme model]]
[[!redirects skyrmion model]]
[[!redirects Skyrmion model]]

