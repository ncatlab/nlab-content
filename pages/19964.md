

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
=--
=--



#Contents#

#Contents#
* table of contents
{:toc}



## Idea


> [[Tony Skyrme|Skyrme]] had studied with attention [[On Vortex Atoms|Kelvin's ideas on vortex atoms]]. 

> ([Ranada-Trueba 01, p. 200](On+Vortex+Atoms#RanadaTrueba01))

A _Skyrmion_ is a kind of [[instanton]]/[[soliton]] in certain [[gauge field theories]]. The concept exists quite generally (see [Rho-Zahed 16](#RhoZahed16)), but its original use ([Skyrme 62](#Skyrme62)), and still one of the most important ones, is as a model for _[[baryons]]_ in a putative theory of [[non-perturbative quantum field theory|non-perturbative]] [[quantum chromodynamics]], the formulation of the latter being by and large an open problem (due to [[confinement]], see [[mass gap problem]]). Here in QCD a Skyrmion is specifically a topologically non-trivial field configuration of the [[pion]] [[field (physics)|field]] in [[non-perturbative quantum field theory|non-perturbative]]  [[QCD]].


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

### As a model for atomic nuclei
 {#AsAModelForBaryonsAndNuclei}

Skyrmions are candidate models for [[baryons]] and even some aspects of [[atomic nuclei]] ([Riska 93](#Riska93), [Battye-Manton-Sutcliffe 10](#BattyeMantonSutcliffe10), [Manton 16](#Manton16), [Naya-Sutcliffe 18a](#NayaSutcliffe18a), [Naya-Sutcliffe 18b](#NayaSutcliffe18b}).


For instance various resonances of the [[carbon]] [[nucleus]] are modeled well by a Skyrmion with baryon number 12 ([Lau-Manton 14](#LauManton14)): 

\begin{center}
<img src="https://ncatlab.org/nlab/files/SkyrmionB12.jpg" width="300">
\end{center}

> graphics grabbed form [Lau-Manton 14](#LauManton14)

For Skyrmion models of nuclei to match well to [[experiment]], not just the [[pion field]] but also the heavier [[mesons]] need to be included in the construction. Including the [[rho meson]] gives good results for light nuclei ([Naya-Sutcliffe 18a](#NayaSutcliffe18a), [Naya-Sutcliffe 18b](#NayaSutcliffe18b))


\begin{center}
<img src="https://ncatlab.org/nlab/files/SkyrmionsWithRho.jpg" width="800">
\end{center}

> graphics grabbed form [Naya-Sutcliffe 18](#NayaSutcliffe18)


### As a holographic boundary theory
 {#AsBoundaryFieldTheory}

With suitable care, the Skyrme model [above](#Definition) arises as the [[AdS-CFT|holographic]] [[boundary field theory]] of that of  5d $G$-[[Yang-Mills theory]] ([Sakai-Sugimoto 04, Section 5.2](#SakaiSugimoto04), [Sakai-Sugimoto 05, Section 3.3](#SakaiSugimoto05), reviewed in [Sugimoto 16, Section 15.3.4](#Sugimoto16), [Bartolini 17, Section 2](#Bartolini17).

This is essentially the theorem of [Atiyah-Manton 89](#AtiyahManton89), as highlighted in [Sutcliffe 10](#Sutcliffe10).

In this way Skyrmions (and hence [[baryons]] and [[atomic nuclei]], see [below](#AsAModelForBaryonsAndNuclei)) appear in the [[Witten-Sakai-Sugimoto model]], which realizes (something close to) [[non-perturbative quantum field theory|non-perturbative]] [[QCD]] as an [[intersecting D-brane model]] described by [[AdS-QCD correspondence]].

In this context the Skyrme model becomes equivalent to a model of [[baryons]] by [[wrapped brane|wrapped]] [[D4-branes]]  ([Sugimoto 16, 15.4.1](#Sugimoto16)).

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


## History

From [Rho-Zahed 10, Preface](#RhoZahed10):

> Two path-breaking developments took place consecutively in physics in the years 1983 and 1984: First in nuclear physics with the rediscovery of Skyrme’s seminal idea on the structure of baryons and then a ["revolution" in string theory](string+theory#ReferencesHistory) in the following year. 

> $[\cdots]$ at that time the most unconventional idea of Skyrme that [[fermion|fermionic]] [[baryons]] could emerge as topological [[solitons]] from [[π-meson]] cloud was confirmed in the context of [[quantum chromodynamics]] (QCD) in the large number-of-[[color charge|color]] ($N_c$) limit. It also confirmed how the solitonic structure of [[baryons]], in particular, the [[nucleons]], reconciled nuclear physics — which had been making an impressive progress [[phenomenology|phenomenologically]], aided mostly by [[experiments]] — with [[QCD]], the fundamental theory of [[strong nuclear force|strong interactions]]. Immediately after the rediscovery of what is now generically called "skyrmion" came the [first string theory revolution](string+theory#ReferencesHistory) which then took most of the principal actors who played the dominant role in reviving the skyrmion picture away from that problem and swept them into the mainstream of [[string theory]] reaching out to a much higher [[energy]] [[scale]]. This was in some sense unfortunate for the skyrmion model _per se_ but fortunate for nuclear physics, for it was then mostly nuclear theorists who picked up what was left behind in the wake of the celebrated string revolution and proceeded to uncover fascinating novel aspects of nuclear structure which otherwise would
have eluded physicists, notably concepts such as the ‘Cheshire Cat phenomenon’ in hadronic dynamics.

> What has taken place since 1983 is a beautiful story in [[physics]]. It has not only profoundly influenced nuclear physics — which was Skyrme’s original aim — but also brought to light hitherto unforseen phenomena in other areas of physics, such as [[condensed matter physics]], [[astrophysics]] and [[string theory]].

## References

### General

The original article is

* {#Skyrme62} [[Tony Skyrme]], _A unified field theory of mesons and baryons_, Nuclear Physics Volume 31, March–April 1962, Pages 556-569 (<a href="https://doi.org/10.1016/0029-5582(62)90775-7">doi:10.1016/0029-5582(62)90775-7</a>)

A review is in:

* {#RhoZahed16} [[Mannque Rho]], [[Ismail Zahed]] (eds.) _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

Further development:

* {#Manton11} [[Nicholas Manton]], _Classical Skyrmions -- Static Solutions and Dynamics_, Mathematical Methods in the applied Sciences, Volume35, Issue10, 2012, Pages 1188-1204 ([arXiv:1106.1298](https://arxiv.org/abs/1106.1298), [doi:10.1002/mma.2512]( https://doi.org/10.1002/mma.2512))

* {#NST11} Atsushi Nakamula, Shin Sasaki, Koki Takesue, _Atiyah-Manton Construction of Skyrmions in Eight Dimensions_, JHEP 03 (2017) 076 ([arXiv:1612.06957](https://arxiv.org/abs/1612.06957))

* {#FLM12} D. T. J. Feist, P. H. C. Lau, [[Nicholas Manton]], _Skyrmions up to Baryon Number 108_ ([arXiv:1210.1712](https://arxiv.org/abs/1210.1712))

* {#Manton17} [[Nicholas Manton]], _Lightly Bound Skyrmions, Tetrahedra and Magic Numbers_ ([arXiv:1707.04073](https://arxiv.org/abs/1707.04073))

[[scattering amplitudes]]:

* T.Gisiger, M. B. Paranjape, _Skyrmion-Skyrmion Scattering_ ([arXiv:hep-th/9310050](https://arxiv.org/abs/hep-th/9310050))

Relation to the [[complex Hopf fibration]]:

* Sven Bjarke Gudnason, Muneto Nitta, _Linking number of vortices as baryon number_ ([arXiv:2002.01762](https://arxiv.org/abs/2002.01762))


See also

* Wikipedia, _[Skyrmion](https://en.wikipedia.org/wiki/Skyrmion)_

Further resources

* _[Geometric models of Nuclear Matter Conference 2014](https://www.kent.ac.uk/smsas/personal/skyrmions/conference.html)_ 

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

In [[solid state physics]] skyrmions in the magnetization of thin atomic layers are known as magnetic skyrmions. 

See:

* Wikipedia, _[Magnetic skyrmions](https://en.m.wikipedia.org/wiki/Magnetic_skyrmion)_



### Via holography in string theory

In [[string theory]], specifically in the [[AdS-QCD correspondence]] in the form of the [[Witten-Sakai-Sugimoto model]] the skyrmion was found in

* {#SakaiSugimoto04} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], section 5.2 of _Low energy hadron physics in holographic QCD_, Prog.Theor.Phys.113:843-882, 2005 ([arXiv:hep-th/0412141](https://arxiv.org/abs/hep-th/0412141))

* {#SakaiSugimoto05} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], section 3.3. of _More on a holographic dual of QCD_, Prog.Theor.Phys.114:1083-1118, 2005 ([arXiv:hep-th/0507073](https://arxiv.org/abs/hep-th/0507073))

* {#Bartolini17} Lorenzo Bartolini, [[Stefano Bolognesi]], Andrea Proto, _From the Sakai-Sugimoto Model to the Generalized Skyrme Model_, Phys. Rev. D 97, 014024 2018 ([arXiv:1711.03873](https://arxiv.org/abs/1711.03873))

See also

* [Sutcliffe 10](#Sutcliffe10)

* {#BolognesiSutcliffe13} [[Stefano Bolognesi]], [[Paul Sutcliffe]], _The Sakai-Sugimoto soliton_, JHEP 1401:078, 2014 ([arXiv:1309.1396](https://arxiv.org/abs/1309.1396))

* {#Sutcliffe15} [[Paul Sutcliffe]], _Holographic Skyrmions_, Mod. Phys. Lett. B29 (2015) no. 16, 1540051 ([spire:1383608](http://inspirehep.net/record/1383608))

Review is in

* {#Sugimoto16} [[Shigeki Sugimoto]], _Skyrmion and String theory_, chapter 15 in [[Mannque Rho]], [[Ismail Zahed]] (eds.) _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))


[[!redirects skyrmions]]

[[!redirects Skyrmion]]
[[!redirects Skyrmions]]