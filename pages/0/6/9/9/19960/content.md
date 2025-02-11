+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}


\begin{imagefromfile}
    "file_name": "HardWallModelPredictions.jpg",
    "float": "right",
    "width": 440,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Erlich 09, section 1.2](#Erlich09)"
\end{imagefromfile}


What is called _holographic QCD_ or _AdS/QCD correspondence_ or similar (review includes [Aharony 02](#Aharony02), [Erlich 09](#Erlich09), [Kim-Yi 11](#KimYi11), [Erlich 14](#Erlich14), [Rebhan 14](#Rebhan14), [Rho-Zahed 16](#RhoZahed16)) is a quantitatively predictive [[model (in theoretical physics)|model]] for [[quantum chromodynamics]] ("[[QCD]]", the [[strong nuclear force]]-sector of the [[standard model of particle physics]]) via "holography" (as in the [[AdS/CFT correspondence]]), hence regarding it as the [[boundary field theory]] of an (at least) [[D=5 super Yang-Mills theory|5-dimensional]] [[Yang-Mills theory]] ("[[bottom-up model building|bottom-up]] holographic QCD"), specifically one [[geometric engineering|geometrically engineered]] on [[intersecting D-brane model|intersecting D-branes]] ("[[top-down model building|top-down]] holographic QCD") and here specifically on [[D4-D8 brane intersections]] (the _[[Witten-Sakai-Sugimoto model]]_ due to [Witten 98](#Witten98), [Karch-Katz 02](#KarchKatz02), [Sakai-Sugimoto 04](#SakaiSugimoto04), [Sakai-Sugimoto 05](#SakaiSugimoto05)). 

{#QCDNotManifestlyAnSCFT} While [[QCD]], taken at face value, is not a [[quantum field theory]] of the kind considered in the plain [[AdS-CFT correspondence]] -- since it is not a [[conformal field theory]] (but see [KPV22](confinement#KPV22)) and not [[supersymmetry|supersymmetric]] (hence not an [[SCFT]], but see at *[[hadron supersymmetry]]*) and does not have a large number $N$ of [[color charge|colors]] (but see [below](#SmallNOpenProblem)), it is thought that approximations/deformations of [[AdS-CFT]] may still usefully apply.

Holographic QCD captures the [[non-perturbative effect|non-perturbative]] [[confinement|confined]] regime of [[QCD]], which is otherwise elusive (the [[mass gap problem|Mass Gap Millennium Problem]]), where the would-be [[quarks]] are all [[bound state|bound]]/[[confinement|confined]] inside [[color charge|color]]-less [[hadrons]], with the [[meson]] [[field (physics)|fields]] instead being the [[gauge field]] of a [[flavour (particle physics)|flavour]]-[[chiral perturbation theory|gauge theory]] (holographic dictionary, e.g. [Kim-Yi 11 (3.1)](#KimYi11), see also "[[hidden local symmetry]]") and the [[baryons]] being [[solitons]] of this flavour/meson field, namely _[[skyrmions]]_.

\begin{imagefromfile}
    "file_name": "IntersectingBranesSSWModel.jpg",
    "float": "right",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Rebhan 14](#Rebhan14)"
\end{imagefromfile}

This [[duality in string theory|dual]] description of the [[color charge|color]] [[gauge theory]] of [[quarks]] and [[gluons]] instead as [[flavour (particle physics)|flavour]] [[gauge theory]] of [[baryons]] and [[mesons]] is [[geometric engineering of QFT|geometrically brought out]] by the [[D4-D8 brane intersections]] of the [[Witten-Sakai-Sugimoto model|Witten-Sakai-Sugimoto]] [[intersecting D-brane model]]: Here the [[open strings]] on the [[D4-branes|D4]] _[[color branes]]_ give the [[color charge|color]]/[[gluon]] gauge field, while those on the [[D8-brane|D8]] _[[flavor branes]]_ give the [[flavour (particle physics)|flavour]]/[[meson]] gauge field, those stretching between D4 and D8 give the [[quarks]] and the [[closed strings]] give the [[glueballs]].
(See at _[WSS brane configuration](#WSSBraneConfiguration)_ below.) This way [[color charge|color]]/[[flavour (particle physics)|flavor]] [[duality in physics|duality]] is mapped to [[open/closed string duality]] (as the [[D8-branes]] are treated as probe branes).
 

Notice that the [[flavour physics|flavour sector]] is where most of the open problems regarding the [[standard model of particle physics]] are located ([[flavour problem]], [[flavour anomalies]]).


\begin{imagefromfile}
    "file_name": "SakaiSugimotoModel.jpg",
    "float": "right",
    "width": 570,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Erlich 09, section 1.1](#Erlich09)"
\end{imagefromfile}

Various fundamental characteristics of [[QCD]] that remain mysterious in the [[color charge|colored]]-[[quark]] model readily find a conceptual explanation in terms of this [[geometric engineering of QFT|geometric engineering]] of  [[flavour physics]], notably the phenomena of [[confinement]] and of [[chiral symmetry breaking]], but also for instance [[vector meson dominance]] and the [[Cheshire cat principle]].

\begin{imagefromfile}
    "file_name": "AdSCFTForQCD.jpg",
    "float": "right",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Aoki-Hashimoto-Iizuka 12](#AHI12)"
\end{imagefromfile}


Indeed, holographic QCD gives accurate quantitative predictions of [[confinement|confined]] [[hadron]] spectra, hence of the physics of ordinary [[atomic nuclei]] (see comparison between [[experiment]] and predictions of holographic QCD [below](#BottomUpModels)) which is out of reach for [[perturbative quantum field theory|perturbation theory]] and otherwise computable, at best, via the blind numerics of [[lattice QCD]]. This means ([Witten 98](#Witten98)) that holographic QCD provides a conceptual solution to the _[[mass gap problem]]_ (not yet a rigorous proof, but a proof strategy).

Concretely, much of the [[phenomenology|phenomenological]] success of [[holographic QCD]] is (review in [Rho-Zahed 16, Chapter III](#RhoZahed16)) due to the holographic emergence of the time-honored but _ad hoc_ [[Skyrmion]]-[[model (in theoretical physics)|model]] of [[baryons]], as [[solitons]] in the [[meson]] [[flavour (particle physics)|flavour]]-[[gauge field]]. 

\begin{imagefromfile}
    "file_name": "FirstEightSkyrmions.jpg",
    "width": 450,
    "unit": "px",
    "caption": "From [Manton 11](Skyrmion#Manton11)"
\end{imagefromfile}
 

Moreover, in holographic QCD this [[Skyrmion]] model of [[baryons]] emerges in its modern improved form, where the [[pion]] [[field (physics)|field]] is accompanied by the whole tower of [[vector mesons]] (the [[rho meson]] etc.): these [[meson]] species are holographically unified as the transversal [[KK-mechanism|KK-modes]] in the holographic theory. Already just adjoining the [[rho meson]] to the [[pion]] makes the resulting [[Skyrmions]], and hence holographic QCD, give accurate results for light [[nuclei]] all the way up to  [[carbon]] ([Naya-Sutcliffe 18a](Skyrmion#NayaSutcliffe18a), [Naya-Sutcliffe 18b](Skyrmion#NayaSutcliffe18b)).

\begin{imagefromfile}
    "file_name": "SkyrmionsWithRho.jpg",
    "width": 540,
    "unit": "px",
    "caption": "From [Naya-Sutcliffe 18](Skyrmion#NayaSutcliffe18)"
\end{imagefromfile}


The mechanism behind this description of [[baryons]] and [[nuclei]] via [[holographic QCD]] is the theorem of [Atiyah-Manton 89](skyrmion#AtiyahManton89) (highlighted as such in [Sutcliffe 10](skyrmion#Sutcliffe10)) which identifies [[Skyrmions]] in 3+1-dimensional [[Yang-Mills theory]] with [[Kaluza-Klein 
mechanism|KK modes]] (transversal [[holonomies]]) of [[instantons]] in 4+1-dimensional YM theory:

$$
  \text{baryons}
  \;\;
  \overset{\text{Skyrme}}{\leftrightarrow}
  \;\;
  {
    {\text{Skyrmions}}
    \atop
    {\text{in}\; d=3+1}
  }
  \;\;
  \overset{\text{Atiyah-Manton}}{\leftrightarrow}
  \;\;
  {
    {\text{Instantons}}
    \atop
    {\text{in}\; d=4+1}
  }
$$

This fact (of [[experiment]]/[[phenomenology]] on the left and of [[mathematics]] on the right) combined with the emergence of [[strings]] in the [['t Hooft limit]] of [[QCD]] reveals a _de facto_ [[AdS/CFT correspondence|holographic]] nature of [[QCD]]. The task in [[holographic QCD]] is to sort out the fine-print.

{#SmallNOpenProblem} A key open problem here is that the [[AdS/CFT correspondence]] is currently well understood only in the [[large N limit]], where the number $N_c$ of [[color charge|colors]] and the [['t Hooft coupling]] $\lambda$ are both large. But for [[QCD]] the number of colors is small, $N_c = 3$.  While the correspondence is thought to hold also in the [[small N limit]], here the [[classical field theory|classical]] [[supergravity|super]]-[[gravity]]-computations on the dual (AdS) side will receive [[small N limit|small-N corrections]] (highlighted for holographic QCD e.g. in [Sugimoto 16](#Sugimoto16), see references [below](#StringAndMTheoryCorrection)) from [[perturbative string theory]] (for small [['t Hooft coupling]]) which are hard to compute, and then from [[M-theory]] (for small $N_c$) which are largely unknown, as [formulating M-theory remains an open problem](M-theory#TheOpenProblem). Hence from the perspective of [[small N limit|small-N corrected]] [[holographic QCD]], the [[mass gap problem]]/[confinement problem](confinement#OpenProblem) translates to the problem of formulating [[M-theory]]:

<center>
<a href="https://ncatlab.org/schreiber/files/Schreiber-MTheoryMathematics2020-v200126.pdf#page=8">
<img src="https://ncatlab.org/schreiber/files/ProblemQCDToProblemM230120.jpg" width="670">
</a>
</center>


\linebreak

\linebreak

From [Yi 09](#Yi09):

> [[QCD]] is a challenging theory. Its most interesting aspects, namely the [[confinement]] of [[color charge|color]] and the [[chiral symmetry breaking]], have defied all analytical approaches. While there are now many data accumulated from the [[lattice gauge theory]], the methodology falls well short of giving us insights on how one may understand these phenomena analytically, nor does it give us a systematic way of obtaining a low energy theory of [[QCD]] below the [[confinement]] [[scale]]. 

> $[...]$

> it has been proposed early on that [[baryons]] are topological [[solitons]], namely [[Skyrmions]]  $[$but$]$ the usual [[Skyrmion]] picture of the [[baryon]] has to be modified significantly in the context of full [[QCD]]. 

> $[...]$ 

> the [[AdS/CFT|holographic picture]] naturally brings a gauge principle in the [[bulk spacetime|bulk]] description of the [[flavor physics|flavor]] dynamics in such a way that all spin one [[mesons]] as well as [[pions]] would enter the $[$ [[Skyrmion|skyrmionic]]-$]$construction of [[baryons]] on the equal footing.

> $[...]$

> [[holographic QCD]] is similar to the [[chiral perturbation theory]] in the sense that we deal with exclusively [[gauge invariance|gauge-invariant]] [[observables|operators]] of the theory. The huge difference is, however, that this new approach tends to treat all [[gauge invariance|gauge-invariant]] objects together. Not only the light [[meson]] [[field (physics)|fields]] like [[pions]] but also heavy [[vector mesons]] and [[baryons]] appear together, at least in principle. In other words, a [[holographic QCD]] deals with all [[color charge|color]]-[[trivial representation|singlets]] simultaneously, giving us a lot more predictive power.

> $[...]$


> The expectation that there exists a more intelligent theory consisting only of [[gauge invariance|gauge-invariant]] objects in the [[large N limit|large Nc limit]] is thus realized via [[string theory]] in a somewhat surprising manner that the master fields, those truly physical degrees of freedom, actually live not in four dimensional Minkowskian world but in five or
higher dimensional curved geometry. This is not however completely unanticipated, and was heralded in the celebrated work by [Eguchi and Kawai in early 1980's](#EguchiKawai82) which is all the more remarkable in retrospect. 

> $[...]$

> To compare against actual [[QCD]], we must fix $[$the [['t Hooft coupling]] and the [[Kaluza-Klein compactification|KK]]-[[scale]]$]$ to fit
both the [[pion]] decay constant $f_\pi$ and the [[mass]] of the first [[vector meson]]. After this fitting, all other infinite number of [[masses]] and [[coupling constants]] are fixed. This version $[$the holographic [[WSS model]]$]$ of the [[holographic QCD]]  is extremely predictive.

> $[...]$

> $[$this$]$ elevates the classic [[skyrmion|Skyrme picture]] based on [[pions]] to a unified model involving all [[vector meson|spin one mesons]] in addition to [[pions]]. This is why the picture is extremely predictive. 

> As we saw in this note, for low momentum processes, such as soft [[pion]] [[scattering amplitude|processes]], soft [[rho meson]] exchanges, and soft elastic scattering of [[photons]], the $[$holographic [[WSS model|WSS]]-$]$model's predictions compare extremely well with experimental data. It is somewhat mysterious that the [[baryon]] sector works out almost as well as the [[meson]] sector

\linebreak

{#FromSNM16} From [Suganuma-Nakagawa-Matsumoto 16, p. 1](#SuganumaNakagawaMatsumoto16):

> Since 1973, [[quantum chromodynamics]] (QCD) has been established as the fundamental theory of the [[strong nuclear force|strong interaction]]. Nevertheless, it is very difficult to solve QCD directly in an analytical manner, and many effective models of QCD have been used instead of QCD, but most models cannot be derived from QCD and its connection to QCD is unclear. 

> To analyze nonperturbative QCD, the [[lattice QCD]] Monte Carlo simulation has been also used as a first-principle calculation of the strong interaction. However, it has several weak points. For example, the [[quantum state|state]] information (e.g. the [[wave function]]) is severely limited, because [[lattice QCD]] is based on the [[path-integral]] formalism. Also, it is difficult to take the [[chiral fermion|chiral]] limit, because zero-mass [[pions]] require [[large volume limit|infinite volume lattices]]. There appears a notorious "[sign problem](lattice+gauge+theory#SignProblem)" at finite density.

> On the other hand, [[holographic QCD]] has a direct connection to [[QCD]], and can be derived from QCD in some limit. In fact, [[holographic QCD]] is equivalent to infrared QCD in [[large N limit|large Nc]] and strong [['t Hooft coupling]] $\lambda$, via [[gauge/gravity correspondence]]. Remarkably, [[holographic QCD]] is successful to reproduce many [[hadron]] [[phenomenology]] such as [[vector meson dominance]], the KSRF relation, hidden local symmetry, the GSW model and the [[skyrmion|Skyrme soliton picture]]. Unlike [[lattice QCD]] simulations, holographic QCD is usually formulated in the chiral limit, and does not have the [sign problem](lattice+gauge+theory#SignProblem) at finite density.

\linebreak

From [Rho et a. 16](#RhoEtAl16):

> One can make $[$[[chiral perturbation theory]]$]$ consistent with [[QCD]] by suitably matching the [[correlators]] of the [[effective field theory|effective theory]] to those of [[QCD]] at a [[scale]] near $\Lambda$. Clearly this procedure is not limited to only one set of [[vector mesons]]; in fact, one can readily generalize it to an infinite number of hidden [[gauge fields]] in an [[effective field theory|effective]] [[Lagrangian density|Lagrangian]]. In so doing, it turns out that a fifth dimension is "deconstructed" in a (4+1)-dimensional (or 5D) [[Yang-Mills theory|Yang–Mills]] type form. We will see in Part III that such a structure arises, [[top-down model building|top-down]], in [[string theory]].

> $[...]$

> $[$this [[holographic QCD]]$]$ model comes out to describe — unexpectedly well — low-energy properties of both [[mesons]] and [[baryons]], in particular those properties reliably described in quenched [[lattice QCD]] simulations.

> $[...]$

> One of the most noticeable results of this [[AdS/QCD|holographic model]] is the first derivation of [[vector meson dominance|vector dominance]] (VD) that holds both for [[mesons]] and for [[baryons]]. It has been somewhat of an oddity and a puzzle that [[Jun John Sakurai|Sakurai's]] [[vector meson dominance|vector dominance]] — with the lowest [[vector mesons]] [[rho meson|ρ]] and ω — which held very well for [[pion|pionic]] [[form factors]] at low momentum transfers famously failed for [[nucleon]] [[form factors]]. In this [[AdS/QCD|holographic model]], the [[vector meson dominance|VD]] comes out automatically for both the [[pion]] and the [[nucleon]] provided that the infinite $[$[[Kaluza-Klein mechanism|KK-]]$]$tower is included. While the [[vector meson dominance|VD]] for the [[pion]] with the infinite tower is not surprising given the successful Sakurai VD, that the [[vector meson dominance|VD]] holds also for the [[nucleons]] is highly nontrivial. $[...]$ It turns out to be a consequence of a [[AdS/QCD|holographic]] [[Cheshire cat principle|Cheshire Cat phenomenon]] 

\linebreak



[[!include Polyakov gauge-string duality -- section]]




\linebreak


## Models 
 {#Models}

In approaches to $AdS/QCD$ one distinguishes [[top-down model building]] -- where the ambition is to first set up a globally consistent ambient [[intersecting D-brane model]] where a [[Yang-Mills theory]] at least similar to [[QCD]] arises on suitable [[D-branes]] ([[geometric engineering of gauge theories]]) -- from [[bottom-up model building]] approaches which are more cavalier about global consistency and first focus on accurately fitting the intended [[phenomenology]] of [[QCD]] as the [[asymptotic boundary|asymptotic]] [[boundary field theory]] of [[gravity]]+[[gauge theory]] on some [[anti de Sitter spacetime]]. (Eventually both these approaches should meet "in the middle" to produce a [[model (in theoretical physics)|model]] which is both [[standard model of particle physics|realistic]] as well as globally consistent as a [[string vacuum]]; see also at _[[string phenomenology]]_.)

<center>
<img src="https://ncatlab.org/nlab/files/BottomUpAndTopDownIntersDBraneModelBuilding.png" width="700"/>
</center>

>  graphics from [Aldazabal-Ibáñez-Quevedo-Uranga 00](bottom-up+and+top-down+model+building#AldazabalIbanezQuevedoUranga00)


### Top-down models
 {#TopDownModels}

#### Witten-Sakai-Sugimoto model
  {#WittenSakaiSugimotoModel}

A good [[top-down model building]]-approach to AdS/QCD is due to [Sakai-Sugimoto 04](#SakaiSugimoto04), [Sakai-Sugimoto 05](#SakaiSugimoto05) based on [Witten 98](#Witten98), see [Rebhan 14](#Rebhan14), [Sugimoto 16](#Sugimoto16) for review. 

##### Brane configuration
 {#WSSBraneConfiguration}

The [[Witten-Sakai-Sugimoto model]] [[geometric engineering of QFT|geometrically engineers]] something at least close to [[QCD]]: on the [[worldvolume]] of [[intersecting D-brane models|coincident]] [[black brane|black]] [[M5-branes]] with [[near horizon geometry]] a [[KK-compactification]] of $AdS_7 \times S^4$ in the decoupling limit where the [[worldvolume]] theory becomes the [[6d (2,0)-superconformal SCFT]]. Here the [[KK-compactification]] is on a [[torus]] with anti-periodic boundary conditions for the [[fermions]] in one direction, thus [[spontaneous symmetry breaking|breaking]] all [[supersymmetry]] ([[Scherk-Schwarz mechanism]]), where the first circle [[KK-compactification|reduction]] realizes, under [[duality between M-theory and type IIA string theory]], the [[M5-branes]] as [[D4-branes]], hence the model now looks like 5d [[Yang-Mills theory]] further [[KK-compactification|compactified]] on a circle. ([Witten 98, section 4](#Witten98)). 

The further introduction of [[intersecting D-brane model|intersecting]] [[D8-branes]] and [[anti D-brane|anti]] [[D8-branes]] to [[D4-D8 brane bound states]] makes a sensible sector of [[chiral fermions]] appear in this model ([Sakai-Sugimoto 04](#SakaiSugimoto04), [Sakai-Sugimoto 05](#SakaiSugimoto05))

{#BraneConfigurationDiagram} The following diagram indicates the Witten-Sakai-Sugimoto [[intersecting D-brane model]] that [[geometric engineering of QFT|geometrically engineers]] [[QCD]]:

<center>
<img src="https://ncatlab.org/nlab/files/WSSBraneConfigurationEngineeringQCDII.jpg" width="740"/>
</center>

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/D8D6NS5.jpg" width="380"/>
</div>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]


Here we are showing:

1. the [[color brane|color]] [[D4-branes]];

1. the [[flavor brane|flavor]] [[D8-branes]];

   with

   1. the [[5d Chern-Simons theory]] on their [[worldvolume]]

   1. the corresponding [[4d WZW model]] on the boundary

   exhibiting the [[vector meson fields]] in the [[Skyrmion model]];

1. the [[baryon]] [[D4-branes]]

   (see below at _[Baryons](#Baryons)_);

1. the [[Yang-Mills monopole]] [[D6-branes]] 

   (see at _[[D6-D8-brane bound state]]_);

1. the [[NS5-branes]] (often not considered here).

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

\linebreak

\linebreak

\linebreak




##### Glueballs
 {#WSSModelGlueballs}

Already before adding the D8-branes (hence already in the pure Witten model) this produces a pure [[Yang-Mills theory]] whose [[glueball]]-spectra may usefully be compared to those of [[QCD]]:

<center>
<img src="https://ncatlab.org/nlab/files/GlueballSpectrumSSWModel.jpg" width="700">
</center>

> graphics from [Rebhan 14](#Rebhan14)


##### Hadrons
  {#Hadrons}


In this [[Witten-Sakai-Sugimoto model]] for [[non-perturbative effect|strongly coupled]] [[QCD]] the [[hadrons]] in [[QCD]] correspond to [[string theory|string-theoretic]]-phenomena in the [[bulk field theory]]:

###### Mesons


The [[mesons]] ([[bound states]] of 2 [[quarks]]) correspond to [[open strings]] in the bulk, whose two endpoints on the [[asymptotic boundary]] correspond to the two quarks

###### Baryons
 {#Baryons}

The [[baryons]] ([[bound states]] of $N_c$ [[quarks]]) appear in two different but equivalent ([Sugimoto 16, 15.4.1](#Sugimoto16)) guises:

1. as [[wrapped brane|wrapped]] [[D4-branes]] with $N_c$ [[open strings]] connecting them to the [[D8-brane]]

   ([Witten 98b](#Witten98b), [Gross-Ooguri 98, Sec. 5](#GrossOoguri98), [BISY 98](#BISY98), [CGS98](#CGS98))

1. as [[skyrmions]] 

   ([Sakai-Sugimoto 04, section 5.2](#SakaiSugimoto04), [Sakai-Sugimoto 05, section 3.3](#SakaiSugimoto05), see [Bartolini 17](#Bartolini17)). 

For review see [Sugimoto 16](#Sugimoto16), [Yi 09](#Yi09), [Yi 11](#Yi11), [Yi 13](#Yi13),  also [Rebhan 14, around (18)](#Rebhan14).

<center>
<img src="https://ncatlab.org/nlab/files/BaryonsAsD4Branes.jpg" width="700">
</center>

> graphics from [Sugimoto 16](#Sugimoto16)


Equivalently, these baryon states are the [[Yang-Mills instantons]] on the [[D8-brane]] giving the [[D4-D8 brane bound state]] ([Sakai-Sugimoto 04, 5.7](#SakaiSugimoto04)) as a special case of the general situation for [[Dp-D(p+4)-brane bound states]] (e.g. [Tong 05, 1.4](Dp-D%28p%2B4%29-brane+bound+state#Tong05)).

<center>
<img src="https://ncatlab.org/nlab/files/BaryonVertexDefectInAdSQCD.jpg" width="490">
</center>

> graphics from [Cai-Li 17](#CaiLi17)


<center>
<img src="https://ncatlab.org/nlab/files/D6InD8InAdSQCD.jpg" width="700">
</center>

> graphics from [ABBCN 18](#ABBCN18)


This already produces [[baryon]] [[mass]] spectra with moderate quantitative agreement with [[experiment]] ([HSSY 07](#HSSY07)):


<center>
<img src="https://ncatlab.org/nlab/files/BaryonSpectrumInSakaiSugimoto.jpg" width="700">
</center>

> graphics from [Sugimoto 16](#Sugimoto16)


Moreover, the above 4-brane model for baryons is claimed to be equivalent to the old **[[Skyrmion]] model** (see [Sakai-Sugimoto 04, section 5.2](#SakaiSugimoto04), [Sakai-Sugimoto 05, section 3.3](#SakaiSugimoto05), [Sugimoto 16, 15.4.1](#Sugimoto16), [Bartolini 17](#Bartolini17)). 

But the Skyrmion model of baryons has been shown to apply also to [[bound states]] of [[baryons]], namely the [[atomic nuclei]]  ([Riska 93](Skyrmion#Riska93), [Battye-Manton-Sutcliffe 10](Skyrmion#BattyeMantonSutcliffe10), [Manton 16](Skyrmion#Manton16), [Naya-Sutcliffe 18](Skyrmion#NayaSutcliffe18)), at least for small [[atomic number]].

For instance, various [[experiment|experimentally]] observed resonances of the [[carbon]] [[nucleus]] are modeled well by a Skyrmion with [[atomic number]] 6 and hence baryon number 12 ([Lau-Manton 14](Skyrmion#LauMaonton14)): 

\begin{center}
<img src="https://ncatlab.org/nlab/files/SkyrmionB12.jpg" width="200">
\end{center}

> graphics form [Lau-Manton 14](Skyrmion#LauMaonton14)

More generally, the [[Skyrmion]]-model of [[atomic nuclei]] gives good matches with [[experiment]] if not just the [[pi meson]] but also the [[rho meson]]-background is included ([Naya-Sutcliffe 18](Skyrmion#NayaSutcliffe18)):

\begin{center}
<img src="https://ncatlab.org/nlab/files/SkyrmionsWithRho.jpg" width="800">
\end{center}

> graphics form [Naya-Sutcliffe 18](Skyrmion#NayaSutcliffe18)


<br/>

#### WSS-type model for 2d QCD
 {#WSSTypeModelFor2dQCD}

There is a direct analogue for [[2d QCD]] of the [above](#WittenSakaiSugimotoModel) [[WSS model]] for 4d [[QCD]]
([Gao-Xu-Zeng 06](#GaoXuZeng06), [Yee-Zahed 11](#YeeZahed11)). 

The corresponding [[intersecting D-brane model]] is much as that for 4d QCD [above](#WSSBraneConfiguration), just with 

1. [[colour charge|color]] [[D2-branes]] instead of [[D4-branes]];

1. [[baryon]]$\,$ [[D6-branes]] instead of [[D4-branes]];

1. [[meson]]$\,$ [[field (physics)|fields]] given by  3d [[Chern-Simons theory]] instead of [[5d Chern-Simons theory]]:

<center>
<img src="https://ncatlab.org/nlab/files/WSSBraneConfigurationEngineering2dQCD.jpg" width="740"/>
</center>







#### Type0B/$YM_4$-correspondence
 {#Type0StringCorrespondence}

Instead of starting with [[M5-branes]] in [[supergravity|locally supersymmetric]] [[M-theory]] and then [[spontaneously broken symmetry|spontaneously breaking]] all [[supersymmetry]] by suitable [[KK-compactification]] as in the [Witten-Sakai-Sugimoto model](#WittenSakaiSugimotoModel), one may start with a non-supersymmetric [[bulk field theory|bulk]] [[string theory]] in the first place. 

In this vein, it has been argued in [GLMR 00](#GLMR00) that there is holographic duality between [[type 0 string theory]] and non-supersymmetric 4d [[Yang-Mills theory]] (hence potentially something close to [[QCD]]). See also [AAS 19](#AAS19).


### Bottom-up models
  {#BottomUpModels}

A popular [[bottom-up model building|bottom-up approach]] of AdS/QCD is known as the _hard-wall model_ ([Erlich-Katz-Son-Stephanov 05](#ErlichKatzSonStephanov05)).

Further refinement to the "soft-wall model" is due to [KKSS 06](#KKSS06) and further to "improved holographic QCD" is due to [Gursoy-Kiritsis-Nitti 07](#GursoyKiritsisNitti07), [Gursoy-Kiritsis 08](#GursoyKiritsis08), see [GKMMN 10](#GKMMN10).


## Comparison with experiment
 {#ComparisonWithExperiment}

Comparison of holographic QCD models with [[experiment]] (mostly using bottom-up models).
 
Computations due to [Katz-Lewandowski-Schwartz 05](#KatzLewandowskiSchwartz05) using the hard-wall model ([Erlich-Katz-Son-Stephanov 05](#ErlichKatzSonStephanov05)) find the following comparison of AdS/QCD predictions to [[QCD]]-[[experiment]]

<center>
<img src="https://ncatlab.org/nlab/files/HardWallModelPredictions.jpg" width="400">
</center>

> graphics from [Erlich 09, section 1.2](#Erlich09)

Computations due to [KKSS 06](#KKSS06), [Gursoy-Kiritsis-Nitti 07](#GursoyKiritsisNitti07), [Gursoy-Kiritsis 08](#GursoyKiritsis08), see [GKMMN 10](#GKMMN10):


<center>
<img src="https://ncatlab.org/nlab/files/GlueballMasses.jpg" width="660">
</center>

> graphics from [GKMMN 10](#GKMMN10)


<center>
<img src="https://ncatlab.org/nlab/files/ImprovedAdSQCD.jpg" width="680">
</center>

> graphics from [GKMMN 10](#GKMMN10)


\linebreak

From [Pomarol-Wulzer 09](#PomarolWulzer09):

<center>
<img src="https://ncatlab.org/nlab/files/PomarolHolographicBaryonMasses.jpg" width="500">
</center>

\linebreak

{#TablesdRocha21} From [da Rocha 21](#daRocha21), for [[vector mesons]]:

for [[upsilon-mesons]]:

\begin{imagefromfile}
    "file_name": "daRocha2021-HolographicMesonMasses-Table1a.jpg",
    "width": 440,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [da Rocha 21](#daRocha21)"
\end{imagefromfile}


for [[psi-mesons]]:

\begin{imagefromfile}
    "file_name": "daRocha2021-HolographicMesonMasses-Table2.jpg",
    "width": 440,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [da Rocha 21](#daRocha21)"
\end{imagefromfile}

for [[omega-mesons]]:

\begin{imagefromfile}
    "file_name": "daRocha2021-HolographicMesonMasses-Table3.jpg",
    "width": 440,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [da Rocha 21](#daRocha21)"
\end{imagefromfile}

for [[phi-mesons]]:

\begin{imagefromfile}
    "file_name": "daRocha2021-HolographicMesonMasses-Table4.jpg",
    "width": 440,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [da Rocha 21](#daRocha21)"
\end{imagefromfile}


{#PredictionsIncludingFirstHeavyQuarks} Including the first [[heavy quarks]]:

\begin{imagefromfile}
    "file_name": "ChenHuang_HolographicQCD_2021_TableII.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [Chen & Huang 2021](#ChenHuang21)"
\end{imagefromfile}

\linebreak

From [CLFH22](#CLFH22):


\begin{imagefromfile}
    "file_name": "MesonMassSpectraFromCLFH22.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [CLFH22](#CLFH22)"
\end{imagefromfile}


\linebreak

On properties of the [[quark-gluon plasma]] in comparison to [[lattice QCD]] results:

[Jokela, Järvinen & Piispa 2924](#JokelaJärvinenPiispa24):

> "[[holographic QCD|Holographic QCD]] has reached the level of sophistication that allows for a detailed reproduction of numerous [[lattice QCD]] outcomes"

\linebreak

NB: These computations so far all use just the field theory in the bulk, not yet the stringy modes ([[limit of a sequence|limit]] of vanishing [[string length]] $\sqrt{\alpha'} \to 0$). Incorporating bulk string corrections further improves these results, see [Sonnenschein & Weissman 2018](#SonnenscheinWeissman18). 



## Embedding into the standard model of particle physics


[Nastase 03, p. 2](#Nastase03):

> An obvious question then is can one lift this [[intersecting D-brane model|D brane construction]] for the [[holographic QCD|holographic dual of QCD]] to a [[standard model of particle physics|Standard Model]] embedding?  I study this question in the context of [[intersecting D-brane models|D-brane-world]] [[GUT]] models and find that one needs to have [[TeV-scale string theory]].


## Related concepts

* [[hadron supersymmetry]], [[hadron Kaluza-Klein theory]]

* [[D=5 Yang-Mills theory]] 

* [[confinement]]

  * [[chiral perturbation theory]]

  * [[quark bag model]], [[Cheshire cat principle]]

  * [[Skyrmions]]

* [[lattice QCD]]

* [[AdS-CFT in condensed matter physics]]

* [[holographic Schwinger effect]]

* [[holographic entanglement entropy]]

* [[holography as Koszul duality]]


[[!include effective field theories of nuclear physics -- contents]]



## References


[[!include Polyakov gauge-string duality -- references]]





### General
 {#ReferencesGeneral}


#### Review and introduction

Concerning the modern formulation of QCD via [[AdS/CFT duality]]:

* {#Aharony02} [[Ofer Aharony]], *The non-AdS/non-CFT correspondence, or three different paths to QCD*, in: *Progress in string, field and particle theory*, Springer, (2003) 3-24 &lbrack;[arXiv:hep-th/0212193](https://arxiv.org/abs/hep-th/0212193), [doi:10.1007/978-94-010-0211-0](https://doi.org/10.1007/978-94-010-0211-0)&rbrack;

* [[Stanley J. Brodsky]], [[Guy F. de Teramond]], *AdS/CFT and Light-Front QCD*, in: *Search for the “Totally Unexpected” in the LHC Era*, Proceedings of the *International School of Subnuclear Physics, Erice 2007*, World Scientific (2009) 139-176/183 &lbrack;[arXiv:0802.0514](https://arxiv.org/abs/0802.0514), [doi:10.1142/7586](https://doi.org/10.1142/7586), discussion: [[BrodskyTeramond-AdSCFTLectureDiscussion.pdf:file]]&rbrack;

* [[Hans Günter Dosch]], *A Practical Guide to AdS/CFT*, lecture notes (2009) &lbrack;[pdf](https://www.thphys.uni-heidelberg.de/~dosch/wuhantot.pdf), [[Dosch-AdSCFT.pdf:file]]&rbrack;

* {#Erlich09} [[Joshua Erlich]], *How Well Does AdS/QCD Describe QCD?*,	Int. J. Mod. Phys.A **25** (2010) 411-421 &lbrack;[arXiv:0908.0312](https://arxiv.org/abs/0908.0312), [doi:10.1142/S0217751X10048718](https://doi.org/10.1142/S0217751X10048718)&rbrack;

* Marco Panero, _QCD thermodynamics in the large-$N$ limit_, 2010 ([[PaneroAdsQCD.pdf:file|pdf]])

* {#KimYi11} Youngman Kim, Deokhyun Yi, _Holography at Work for Nuclear and Hadron Physics_, Advances in High Energy Physics, Volume 2011, Article ID 259025, 62 pages ([arXiv:1107.0155](https://arxiv.org/abs/1107.0155), [doi:10.1155/2011/259025](http://dx.doi.org/10.1155/2011/259025))


* [[Antoine Van Proeyen]], [[Daniel Freedman]], Chapter VIII of: _Supergravity_, Cambridge University Press (2012) &lbrack;[doi:10.1017/CBO9781139026833]( https://doi.org/10.1017/CBO9781139026833)&rbrack;


* [[Koji Hashimoto]], §6.4 in: _D-Brane -- Superstrings and New Perspective of Our World_, Springer (2012) &lbrack;[doi:10.1007/978-3-642-23574-0](https://link.springer.com/book/10.1007%2F978-3-642-23574-0), [spire:1188897](http://inspirehep.net/record/1188897)&rbrack;


* M. R. Pahlavani, R. Morad, _Application of AdS/CFT in Nuclear Physics_, Advances in High Energy Physics ([arXiv:1403.2501](https://arxiv.org/abs/1403.2501))

* Jorge Casalderrey-Solana, Hong Liu, [[David Mateos]], Krishna Rajagopal, Urs Achim Wiedemann, _Gauge/string duality, hot QCD and heavy ion collisions_,  Cambridge University Press, 2014 ([arXiv:1101.0618](https://arxiv.org/abs/1101.0618))


* {#AHI12} Sinya Aoki, [[Koji Hashimoto]], [[Norihiro Iizuka]], _Matrix Theory for Baryons: An Overview of Holographic QCD for Nuclear Physics_, Reports on Progress in Physics, Volume 76, Number 10 ([arxiv:1203.5386](https://arxiv.org/abs/1203.5386))

* Youngman Kim, Ik Jae Shin, Takuya Tsukioka, _Holographic QCD: Past, Present, and Future_, Progress in Particle and Nuclear Physics **68** (2013) 55-112 &lbrack;[arXiv:1205.4852](https://arxiv.org/abs/1205.4852)&rbrack;

* {#Erlich14} [[Joshua Erlich]], *An Introduction to Holographic QCD for Nonspecialists*, Contemporary Physics, **56** 2 (2015) &lbrack;[arXiv:1407.5002](https://arxiv.org/abs/1407.5002), [doi:10.1080/00107514.2014.942079](https://doi.org/10.1080/00107514.2014.942079)&rbrack;

* {#Guijosa16} Alberto Guijosa, _QCD, with Strings Attached_, IJMPE Vol. 25, No. 10 (2016) 1630006 &lbrack;[arXiv:1611.07472](https://arxiv.org/abs/1611.07472)&rbrack;

* [[Mannque Rho]], [[Ismail Zahed]] (eds.) Part 4 "String Theory" of: _[[The Multifaceted Skyrmion]]_,  World Scientific (2016) &lbrack;[doi:10.1142/9710](https://doi.org/10.1142/9710)&rbrack;

* Sophia K Domokos, Robert Bell, Trinh La, Patrick Mazza, *A Pedagogical Introduction to Holographic Hadrons*, published as: *Holographic hadron masses in the language of quantum mechanics*,  European Journal of Physics **42** 6 (2021) 065801 &lbrack;[arXiv:2106.13136](https://arxiv.org/abs/2106.13136), [doi:10.1088/1361-6404/ac1abb](https://iopscience.iop.org/article/10.1088/1361-6404/ac1abb)&rbrack;

With emphasis on application to the [QCD phase diagram](QCD#PhaseDiagram) and to the description of [[neutron stars]]:

* [[Matti Järvinen]], *Holographic modeling of nuclear matter and neutron stars*,  Eur. Phys. J. C. **56** (2021) &lbrack;[arXiv:2110.08281](https://arxiv.org/abs/2110.08281), [doi:10.1140/epjc/s10052-022-10227-x](https://doi.org/10.1140/epjc/s10052-022-10227-x)&rbrack;

* [[Niko Jokela]], *NICER view on holographic QCD*, EPJ Web of Conferences **258** (2022) 07004 &lbrack;[arXiv:2111.07940](https://arxiv.org/abs/2111.07940), [doi:10.1051/epjconf/202225807004](https://doi.org/10.1051/epjconf/202225807004)&rbrack;




See also:

* Wikipedia, _[AdS/QCD correspondence](https://en.wikipedia.org/wiki/AdS/QCD_correspondence)_ 

Emphasis of the AdS-QCD correspondence at annual String-conferences:

* {#Klebanov21} [[Igor Klebanov]], *Remarks on Color Confinement*, talk at *[Strings 2021](https://www.ictp-saifr.org/strings2021/)* ([pdf](https://www.ictp-saifr.org/wp-content/uploads/2021/06/DiscussionConfinementKlebanov.pdf), [video](https://youtu.be/B9NI2LE7d68?t=262))

* {#Dubovsky21} [[Sergei Dubovsky]], *Comments on (mostly long) QCD strings*, talk at *[Strings 2021](https://www.ictp-saifr.org/strings2021/)* ([pdf](https://www.ictp-saifr.org/wp-content/uploads/2021/06/Sergei.pdf), [video](https://youtu.be/B9NI2LE7d68?t=1183))

* [[Nick Evans]], *Holography for Multi-Representation and Chiral Matter*, talk at *[[Strings 2022]]* &lbrack;[indico:4940848](https://indico.cern.ch/event/1085701/contributions/4940848), [slides](https://indico.cern.ch/event/1085701/contributions/4940848/attachments/2482358/4261644/Nick%20Evans%20Tuesday-Research-Evans.pdf), [video](https://ustream.univie.ac.at/media/core.html?id=aecca42b-c952-42f0-84c6-5b23230534b7)&rbrack;

  > (emphasis on [[DBI action]]-effects)

* [[Umut Gürsoy]], *Recent developments in gauge-gravity duality applied to quantum many-body systems*, talk at *[[Strings 2022]]* &lbrack;[indico:4940863](https://indico.cern.ch/event/1085701/contributions/4940863), [pdf](https://indico.cern.ch/event/1085701/contributions/4940863/attachments/2483542/4263813/Slides_Gursoy.pdf), [video](https://ustream.univie.ac.at/media/core.html?id=69bc5a22-b77a-4830-97b8-49c7d6aa1c29) &rbrack;

* [[Edward Witten]], *Some Milestones in the Study of Confinement*, talk at *[[Prospects in Theoretical Physics 2023 -- Understanding Confinement]]*, IAS (2023) &lbrack;[web](https://www.ias.edu/video/some-milestones-study-confinement), [YT](https://youtu.be/TvIz-6YOdKs)&rbrack;

> [40:13](https://youtu.be/TvIz-6YOdKs?t=2413): "Personally, I think [[AdS/QCD|this setup]] really implies that pure [[Yang-Mills theory|$SU(N)$ gauge theory]] is [[gauge-string duality|dual]] to a [[string theory]]. The 'only' problem is that to get the pure gauge theory we need to make a relevant deformation and then take the limit that the deformation parameter is large..."


#### Top-down models 

##### Witten-Sakai-Sugimoto model

Precursor developments:

* {#EguchiKawai82} [[Tohru Eguchi]], [[Hikaru Kawai]], _Reduction of Dynamical Degrees of Freedom in the Large-$N$ Gauge Theory_, Phys. Rev. Lett. 48, 1063 (1982) ([spire:176459](http://inspirehep.net/record/176459), [doi:10.1103/PhysRevLett.48.1063](https://doi.org/10.1103/PhysRevLett.48.1063))

* [[Joseph Polchinski]], [[Matthew Strassler]], _The String Dual of a Confining Four-Dimensional Gauge Theory_ ([arXiv:hep-th/0003136](https://arxiv.org/abs/hep-th/0003136))

  > (discussion of [[confinement]] via [[AdS/CFT]] with a [[Myers effect]] in the bulk)

The top-down Sakai-Sugimoto model is due to 

* {#SakaiSugimoto04} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _Low energy hadron physics in holographic QCD_, Progr. Theor. Phys. **113** (2005) 843-882 &lbrack;[arXiv:hep-th/0412141](https://arxiv.org/abs/hep-th/0412141), [doi:10.1143/PTP.113.843](https://doi.org/10.1143/PTP.113.843)&rbrack;

* {#SakaiSugimoto05} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _More on a holographic dual of QCD_, Progr. Theor. Phys. 114: 1083-1118, 2005 ([arXiv:hep-th/0507073](https://arxiv.org/abs/hep-th/0507073))

along the lines of

* {#KarchKatz02} [[Andreas Karch]], [[Emanuel Katz]],  _Adding flavor to AdS/CFT_, JHEP 0206:043, 2002 ([arxiv:hep-th/0205236](https://arxiv.org/abs/hep-th/0205236))

and based on 

* {#Witten98} [[Edward Witten]], *Anti-de Sitter Space, Thermal Phase Transition, And Confinement In Gauge Theories*, Adv. Theor. Math. Phys. **2** 3 (1998) 505-532 &lbrack;[arXiv:hep-th/9803131](https://arxiv.org/abs/hep-th/9803131), [doi:10.4310/ATMP.1998.v2.n3.a3](https://dx.doi.org/10.4310/ATMP.1998.v2.n3.a3)&rbrack;

further developed in 


* {#Bartolini17} Lorenzo Bartolini, [[Stefano Bolognesi]], Andrea Proto, _From the Sakai-Sugimoto Model to the Generalized Skyrme Model_, Phys. Rev. D 97, 014024 2018 ([arXiv:1711.03873](https://arxiv.org/abs/1711.03873))

reviewed in:

* Piljin Yi, _Topics in D4-D8 holographic QCD_, 2009 ([[YiD4D8HolographicQCD.pdf:file]])

* [[Shigeki Sugimoto]], _Holographic QCD -- Status and perspectives_, 2012 ([[Sugimoto12.pdf:file]])

* {#Rebhan14} [[Anton Rebhan]], *The Witten-Sakai-Sugimoto model: A brief review and some recent results*, in Proceedings of: *3rd International Conference on New Frontiers in Physics, Kolymbari, Crete 2014*,  EPJ Web of Conferences
**95** 02005 (2015) &lbrack;[arXiv:1410.8858](https://arxiv.org/abs/1410.8858), [doi:10.1051/epjconf/20159502005 ](https://doi.org/10.1051/epjconf/20159502005 )&rbrack;

* {#RhoZahed16} [[Mannque Rho]], [[Ismail Zahed]] (eds.) _[[The Multifaceted Skyrmion]]_,  World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

* Si-wen Li, Xiao-tong Zhang, *The D4/D8 model and holographic QCD* &lbrack;[arXiv:2304.10826](https://arxiv.org/abs/2304.10826)&rbrack;


See also:

* Vikas Yadav, *String/$\mathcal{M}$-theory Dual of Large-$N$ Thermal QCD-Like Theories at Intermediate Gauge/'t Hooft Coupling and Holographic Phenomenology* ([arXiv:2111.12655](https://arxiv.org/abs/2111.12655))


More on [[D4-D8 brane bound states]]:

* {#Nastase03} [[Horatiu Nastase]], Sections 2, 3 of: _On Dp-Dp+4 systems, QCD dual and phenomenology_ ([arXiv:hep-th/0305069](https://arxiv.org/abs/hep-th/0305069))

The Witten-Sakai-Sugimoto model with [[orthogonal group|orthogonal]]  [[gauge groups]] realized by [[D4-D8 brane bound states]] at [[O-planes]]: 

* {#ImotoSakaiSugimoto09} Toshiya Imoto, [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _$O(N)$ and $USp(N)$ QCD from String Theory_, Prog.Theor.Phys.122:1433-1453, 2010 ([arXiv:0907.2968](https://arxiv.org/abs/0907.2968))

* Hee-Cheol Kim, Sung-Soo Kim, Kimyeong Lee, _5-dim Superconformal Index with Enhanced $E_n$ Global Symmetry_, JHEP 1210 (2012) 142 ([arXiv:1206.6781](https://arxiv.org/abs/1206.6781))

Analogous discussion for [[flavour (particle physics)|flavour]] [[D6-branes]]:

* [[Jérôme Gaillard]], _On $G$-structures in gauge/string duality_, 2011 ([cronfa:42569](https://cronfa.swan.ac.uk/Record/cronfa42569) [spire:1340775](http://inspirehep.net/record/1340775), [[GaillardGStructure.pdf:file]])

  (with emphasis of [[G-structures]])


The analogoue of the WSS model for [[2d QCD]]:

* {#GaoXuZeng06} Yi-hong Gao, Weishui Xu, Ding-fang Zeng, _NGN, $QCD_2$ and chiral phase transition from string theory_, Nucl.Phys. B400:181-210, 1993 ([arXiv:hep-th/0605138](https://arxiv.org/abs/hep-th/0605138))

Specifically concerning the 3d [[Chern-Simons theory]] on the [[D8-branes]]:

* {#YeeZahed11} Ho-Ung Yee, Ismail Zahed, _Holographic two dimensional QCD and Chern-Simons term_, JHEP 1107:033, 2011 ([arXiv:1103.6286](https://arxiv.org/abs/1103.6286))

and its relation to [[baryons]]:

* {#SuganumaNakagawaMatsumoto16} Hideo Suganuma, Yuya Nakagawa, Kohei Matsumoto, _1+1 Large $N_c$ QCD and its Holographic Dual $\sim$ Soliton Picture of Baryons in Single-Flavor World_, JPS Conf. Proc. 13, 020013 (2017) ([arXiv:1610.02074](https://arxiv.org/abs/1610.02074))

On [[jet bundle]] [[cohomology]] in the Sakai-Sugimoto model:

* Ekkehart Winterroth, *Variational cohomology and Chern-Simons gauge theories in higher dimensions* ([arXiv:2103.03037](https://arxiv.org/abs/2103.03037))

Comparison of the WSS model To [[lattice QCD]]:


* {#KovenskySchmitt24} [[Nicolas Kovensky]], [[Andreas Schmitt]]: *Thermal pion condensation: holography meets lattice QCD* &lbrack;[arXiv:2407.12641](https://arxiv.org/abs/2407.12641)&rbrack;







##### Further models

Variant with [[D4-brane|D4]] [[flavor branes]]:

* [[Mark Van Raamsdonk]], Kevin Whyte, _Baryon charge from embedding topology and a continuous meson spectrum in a new holographic gauge theory_, JHEP 1005:073, 2010 ([arXiv:0912.0752](https://arxiv.org/abs/0912.0752))

* Shigenori Seki, _Intersecting D4-branes Model of Holographic QCD and Tachyon Condensation_, JHEP 1007:091, 2010 ([arXiv:1003.2971](https://arxiv.org/abs/1003.2971))

See also:

* [[Nick Evans]], [[Jack Mitchell]], *Domain Wall AdS/QCD*, Phys. Rev. D **104** (2021) 094018 &lbrack;[arXiv:2108.12152](https://arxiv.org/abs/2108.12152), [doi:10.1103/PhysRevD.104.094018](https://doi.org/10.1103/PhysRevD.104.094018)&rbrack;

* [[Nick Evans]], [[Jack Mitchell]], *Thermal Transitions in Domain Wall AdS/QCD* &lbrack;[arXiv:2207.10374](https://arxiv.org/abs/2207.10374)&rbrack;






#### Bottom-up models

##### Hard- and soft-wall model

The bottom-up hard-wall model is due to

* {#ErlichKatzSonStephanov05} Joshua Erlich, [[Emanuel Katz]], Dam T. Son, Mikhail A. Stephanov, _QCD and a Holographic Model of Hadrons_, Phys.Rev.Lett.95:261602, 2005 ([arXiv:hep-ph/0501128](https://arxiv.org/abs/hep-ph/0501128))

while the soft-wall refinement is due to 

* {#KKSS06} [[Andreas Karch]], [[Emanuel Katz]], Dam T. Son, Mikhail A. Stephanov, _Linear Confinement and AdS/QCD_, Phys.Rev.D74:015005, 2006 ([arXiv:hep-ph/0602229](https://arxiv.org/abs/hep-ph/0602229))

reviewed in 

* Sergey Afonin, Timofey Solomko, *Motivations for the Soft Wall holographic approach to strong interactions* &lbrack;[arXiv:2209.09042](https://arxiv.org/abs/2209.09042)&rbrack;


see also

* Alfredo Vega, Paulina Cabrera, _Family of dilatons and metrics for AdS/QCD models_, Phys. Rev. D 93, 114026 (2016) ([arXiv:1601.05999](https://arxiv.org/abs/1601.05999))

* Alfonso Ballon-Bayona, Luis A. H. Mamani, _Nonlinear realisation of chiral symmetry breaking in holographic soft wall models_ ([arXiv:2002.00075](https://arxiv.org/abs/2002.00075))

and the version _improved holographic QCD_ is due to

* {#GursoyKiritsis08} Umut Gursoy, [[Elias Kiritsis]], _Exploring improved holographic theories for QCD: Part I_, JHEP 0802:032, 2008 ([arXiv:0707.1324](https://arxiv.org/abs/0707.1324))

* {#GursoyKiritsisNitti07} Umut Gursoy, [[Elias Kiritsis]], Francesco Nitti, _Exploring improved holographic theories for QCD: Part II_, JHEP 0802:019, 2008 ([arXiv:0707.1349](https://arxiv.org/abs/0707.1349))

reviewed in 

* {#GKMMN10} Umut Gürsoy, [[Elias Kiritsis]], Liuba Mazzanti, Georgios Michalogiorgakis, Francesco Nitti, _Improved Holographic QCD_, Lect.Notes Phys.828:79-146,2011 ([arXiv:1006.5461](https://arxiv.org/abs/1006.5461))

More developments on improved holographic QCD:

* Takaaki Ishii, [[Matti Järvinen]], Govert Nijs, _Cool baryon and quark matter in holographic QCD_,  J. High Energ. Phys. **2019** 3 (2019) &lbrack;<a href="https://doi.org/10.1007/JHEP07(2019)003">doi:10.1007/JHEP07(2019)003</a>, [arXiv:1903.06169](https://arxiv.org/abs/1903.06169)&rbrack;

The extreme form of bottom-up holographic model building is explored in

* {#HashimotoEtAl18} [[Koji Hashimoto]], Sotaro Sugishita, Akinori Tanaka, Akio Tomiya, _Deep Learning and Holographic QCD_, Phys. Rev. D 98, 106014 (2018) ([arXiv:1809.10536](https://arxiv.org/abs/1809.10536))

where an appropriate [[bulk]] geometry is computer-generated from specified boundary behaviour.

More on this:

* Tetsuya Akutagawa, Koji Hashimoto, Takayuki Sumimoto, _Deep Learning and AdS/QCD_ ([arXiv:2005.02636](https://arxiv.org/abs/2005.02636))

On the other hand, an embedding of the hard-wall model into [[type IIB string theory]] is discussed in:

* [[Akash Singh]], [[K. P. Yogendran]], *Phases of a 10-D Holographic hard wall model* &lbrack;[arXiv:2208.09387](https://arxiv.org/abs/2208.09387)&rbrack;

* Saulo Diles, *On the spectrum of open strings in the Hard-Wall model of AdS/QCD: the role of $S^5$* &lbrack;[arXiv:2404.10183](https://arxiv.org/abs/2404.10183)&rbrack;



##### Holographic light-front QCD

The holographic formulation of [[light cone gauge|light cone quantized]] [[QCD]] as [[holographic light front QCD]]:

Original articles:

* [[Stanley Brodsky]], [[Guy de Teramond]], _Light-Front Hadron Dynamics and AdS/CFT Correspondence_, Phys. Lett. B582:211-221, 2004 ([arXiv:hep-th/0310227](https://arxiv.org/abs/hep-th/0310227))

* [[Guy de Teramond]], [[Stanley Brodsky]], _Light-Front Holography: A First Approximation to QCD_, Phys. Rev. Lett. 102:081601, 2009 ([arXiv:0809.4899](https://arxiv.org/abs/0809.4899))



Review in:

* [[Stanley Brodsky]], [[Guy de Teramond]],  [[Hans Günter Dosch]], [[Joshua Erlich]], 
_Light-Front Holographic QCD and Emerging Confinement_, Physics Reports Volume 584, 8 July 2015, Pages 1-105 ([arXiv:1407.8131](https://arxiv.org/abs/1407.8131))

* {#ZhouDosch18} Liping Zou, [[Hans Günter Dosch]], _A very Practical Guide to Light Front Holographic QCD_, ([arXiv:1801.00607](https://arxiv.org/abs/1801.00607))

* [[Stanley Brodsky]], _Color Confinement and Supersymmetric Properties of Hadron Physics from Light-Front Holography_, International Conference on Beauty, Charm and Hyperon Hadrons (BEACH 2018) 17–23 June 2018, Peniche, Portugal ([arXiv:1912.12578](https://arxiv.org/abs/1912.12578))

* Ruben Sandapen, _An overview of light-front holography_ ([arXiv:2001.03479](https://arxiv.org/abs/2001.03479))

* [[Stanley Brodsky]], *Supersymmetric and Other Novel Features of Hadron Physics from Light-Front Holography*,  Proceedings of the 24th Workshop, "What Comes Beyond the Standard Models" ([arXiv:2112.02453](https://arxiv.org/abs/2112.02453))


See also

* Harun Omer, _Embedding LFHQCD in Worldsheet String Theory_ ([arXiv:1909.12866](https://arxiv.org/abs/1909.12866))



Application to [[B-meson]] physics:

* [[Mohammad Ahmady]], _Holographic light-front QCD in B meson phenomenology_ ([arXiv:2001.00266](https://arxiv.org/abs/2001.00266))

##### Relation to hadron supersymmetry

Discussion of [[hadron supersymmetry]] via [[light cone gauge|light cone]] [[supersymmetric quantum mechanics]] in [[holographic light front QCD]]:

* {#dTDB14}  [[Guy de Teramond]], [[Hans Günter Dosch]], [[Stanley Brodsky]], _Baryon Spectrum from Superconformal Quantum Mechanics and its Light-Front Holographic Embedding_, Phys. Rev. D 91, 045040 (2015) ([arXiv:1411.5243](https://arxiv.org/abs/1411.5243))


* [[Hans Günter Dosch]], [[Guy de Teramond]], [[Stanley Brodsky]], _Supersymmetry Across the Light and Heavy-Light Hadronic Spectrum_, Phys. Rev. D 92, 074010 (2015) ([arXiv:1504.05112](https://arxiv.org/abs/1504.05112))


* {#BTDL16}  [[Stanley Brodsky]], [[Guy de Téramond]], [[Hans Günter Dosch]], Cédric Lorcé, _Meson/Baryon/Tetraquark Supersymmetry from Superconformal Algebra and Light-Front Holography_, International Journal of Modern Physics AVol. 31, No. 19, 1630029 (2016) ([arXiv:1606.04638](https://arxiv.org/abs/1606.04638))



* [[Hans Günter Dosch]], [[Guy de Teramond]], [[Stanley Brodsky]], _Supersymmetry Across the Light and Heavy-Light Hadronic Spectrum II_, Phys. Rev. D 95, 034016 (2017) ([arXiv:1612.02370](https://arxiv.org/abs/1612.02370))

* {#NielsenBrodsky18} [[Marina Nielsen]], [[Stanley Brodsky]], _Hadronic Superpartners from Superconformal and Supersymmetric Algebra_, Phys. Rev. D 97, 114001 (2018) ([arXiv:1802.09652](https://arxiv.org/abs/1802.09652))


* [[Marina Nielsen]], [[Stanley Brodsky]], Guy F. de Téramond, [[Hans Günter Dosch]], Fernando S. Navarra, Liping Zou, _Supersymmetry in the Double-Heavy Hadronic Spectrum_, Phys. Rev. D 98, 034002 (2018) ([arXiv:1805.11567](https://arxiv.org/abs/1805.11567))



#### String- and M-theory corrections
 {#StringAndMTheoryCorrection}

Generally on [[perturbative string theory]]-corrections (for small [['t Hooft coupling]] $\lambda = g_{YM}^2 N$) and/or [[M-theory]]-corrections ([[large N limit|small N]]) to the [[supergravity]]-approximation of the [[AdS/CFT correspondence]], i.e. the [[small N corrections]] to the correspondence:

On the general need for [[M-theory]] at small $N_c$ in gauge/gravity duality:

* [[Leonard Susskind]], _Another Conjecture about M(atrix) Theory_ ([arXiv:hep-th/9704080](https://arxiv.org/abs/hep-th/9704080)) 

* [[Nissan Itzhaki]], [[Juan Maldacena]], [[Jacob Sonnenschein]], [[Shimon Yankielowicz]], Section 6 of: _Supergravity and The Large $N$ Limit of Theories With Sixteen Supercharges_, Phys. Rev. D 58, 046004 (1998) ([arXiv:hep-th/9802042](https://arxiv.org/abs/hep-th/9802042))

Discussion of [[large N limit|small N]] effects in [[M-theory]] [[AdS4/CFT3]] and using the [[conformal bootstrap]]:

* Nathan B. Agmon, Shai M. Chester, Silviu S. Pufu, _Solving M-theory with the Conformal Bootstrap_, JHEP 06 (2018) 159 ([arXiv:1711.07343](https://arxiv.org/abs/1711.07343))

\linebreak

Specifically on [[small N corrections]] in [[holographic QCD]]:

* {#Basso08} B. Basso, _Cusp anomalous dimension in planar maximally supersymmetric Yang-Mills theory_, Continuous Advances in QCD 2008, pp. 317-328 (2008) ([spire:858223](http://inspirehep.net/record/858223), [doi:10.1142/9789812838667_0027](https://doi.org/10.1142/9789812838667_0027))

  > "The result $[$(29)$]$ coincides exactly with the recent two-loop stringy correction computed in [Alday-Maldacena 07](https://arxiv.org/abs/0708.0672), providing a striking confirmation of the AdS/CFT correspondence."

* H. Dorn, H.-J. Otto, _On Wilson loops and $Q\bar Q$-potentials from the AdS/CFT relation at $T\geq 0$_, In: [[Anna Ceresole]], C. Kounnas , [[Dieter Lüst]], [[Stefan Theisen]]  (eds.) _Quantum Aspects of Gauge Theories, Supersymmetry and Unification_, Lecture Notes in Physics, vol 525. Springer 2007 ([arXiv:hep-th/9812109](https://arxiv.org/abs/hep-th/9812109), 
[doi:10.1007/BFb0104268](https://doi.org/10.1007/BFb0104268))

* Masayasu Harada, Shinya Matsuzaki, and Koichi Yamawaki, _Implications of holographic QCD in chiral perturbation theory with hidden local symmetry_, Phys. Rev. D 74, 076004 (2006) ([doi:10.1103/PhysRevD.74.076004](https://doi.org/10.1103/PhysRevD.74.076004))

  (with an eye towards [[hidden local symmetry]])

* Csaba Csaki, [[Matthew Reece]], John Terning, _The AdS/QCD Correspondence: Still Undelivered_, JHEP 0905:067, 2009 ([arXiv:0811.3001](https://arxiv.org/abs/0811.3001))

* Salvatore Baldino, [[Stefano Bolognesi]], Sven Bjarke Gudnason, Deniz Koksal, _A Solitonic Approach to Holographic Nuclear Physics_, Phys. Rev. D 96, 034008 (2017) ([arXiv:1703.08695](https://arxiv.org/abs/1703.08695))

* Vikas Yadav, Aalok Misra, *On M-Theory Dual of Large-$N$ Thermal QCD-Like Theories up to $\mathcal{O}(R^4)$ and $G$-Structure Classification of Underlying Non-Supersymmetric Geometries* ([arXiv:2004.07259](https://arxiv.org/abs/2004.07259))




[[!include hadrons as KK-modes of 5d Yang-Mills theory -- references]]






### Hadron physics

Application to [[confinement|confined]] [[hadron]]-physics:

Review:

* Henrique Boschi-Filho, _Hadrons in AdS/QCD models_, Journal of Physics: Conference Series, Volume 706, Section 4 2008 ([doi:10.1088/1742-6596/706/4/042008](http://iopscience.iop.org/article/10.1088/1742-6596/706/4/042008))

* Kanabu Nawa, Hideo Suganuma, Toru Kojo, _Baryons in Holographic QCD_, Phys.Rev.D75:086003, 2007 ([arXiv:hep-th/0612187](https://arxiv.org/abs/hep-th/0612187))

* Deog Ki Hong, Mannque Rho, Ho-Ung Yee, [[Piljin Yi]], _Chiral Dynamics of Baryons from String Theory_, Phys. Rev. D76:061901, 2007 ([arXiv:hep-th/0701276](https://arxiv.org/abs/hep-th/0701276))

* Deog Ki Hong, _Baryons in holographic QCD_, talk at _[From Strings to Things 2008](http://www.int.washington.edu/PROGRAMS/08-1.html)_ ([pdf](http://www.int.washington.edu/talks/WorkShops/int_08_1/People/Hong_D/Hong.pdf))

* [[Johanna Erdmenger]], [[Nick Evans]], [[Ingo Kirsch]], [[Ed Threlfall]], _Mesons in Gauge/Gravity Duals - A Review_, Eur. Phys. J. A **35** (2008) 81-133 &lbrack;[arXiv:0711.4467](https://arxiv.org/abs/0711.4467), [doi:10.1140/epja/i2007-10540-1](https://doi.org/10.1140/epja/i2007-10540-1)&rbrack;

* [[Stanley Brodsky]], _Hadron Spectroscopy and Dynamics from Light-Front Holography and Superconformal Algebra_ ([arXiv:1802.08552](https://arxiv.org/abs/1802.08552))

* [[Koji Hashimoto]], [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _Holographic Baryons : Static Properties and Form Factors from Gauge/String Duality_, Prog. Theor. Phys.120:1093-1137, 2008 ([arXiv:0806.3122](https://arxiv.org/abs/0806.3122))

* Alex Pomarol, Andrea Wulzer, _Baryon Physics in Holographic QCD_, Nucl. Phys. B809:347-361, 2009 ([arXiv:0807.0316](https://arxiv.org/abs/0807.0316))

* Thomas Gutsche, Valery E. Lyubovitskij, Ivan Schmidt, Alfredo Vega, _Nuclear physics in soft-wall AdS/QCD: Deuteron electromagnetic form factors_, Phys. Rev. D 91, 114001 (2015) ([arXiv:1501.02738](https://arxiv.org/abs/1501.02738))

* {#PomarolWulzer09} Alex Pomarol, Andrea Wulzer, _Baryon physics in a five-dimensional model of hadrons_ ([arXiv:0904.2272](https://arxiv.org/abs/0904.2272)), Chapter 18 in: [[Mannque Rho]], [[Ismail Zahed]] (eds.) _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

* Marco Claudio Traini, _Generalized Parton Distributions: confining potential effects within AdS/QCD_, Eur. Phys. J. C (2017) 77:246 ([arXiv:1608.08410](https://arxiv.org/abs/1608.08410))

* {#CaiLi17} Wenhe Cai, Si-wen Li, _Holographic three flavor baryon in the Witten-Sakai-Sugimoto model with the D0-D4 background_, Eur. Phys. J. C (2018) 78: 446 ([arXiv:1712.06304](https://arxiv.org/abs/1712.06304))

* Valery E. Lyubovitskij, Ivan Schmidt, _Gluon parton densities in soft-wall AdS/QCD_ ([arXiv:2012.01334](https://arxiv.org/abs/2012.01334))

* Lorenzo Bartolini, Sven Bjarke Gudnason, *Symmetry energy in holographic QCD* &lbrack;[arXiv:2209.14309](https://arxiv.org/abs/2209.14309)&rbrack;

See also:

* {#CLFH22} Ruixiang Chen, Danning Li, Kazem Bitaghsir Fadafan, Mei Huang, *The hadron spectra and pion form factor in dynamical holographic QCD model with anomalous 5D mass of scalar field* &lbrack;[arXiv:2212.10363](https://arxiv.org/abs/2212.10363)&rbrack;




#### Baryons as instantons

[[baryons]] as [[instantons]]:

* {#KatzLewandowskiSchwartz05} Emanuel Katz, Adam Lewandowski, Matthew D. Schwartz, Phys. Rev. D74:086004, 2006 ([arXiv:hep-ph/0510388](https://arxiv.org/abs/hep-ph/0510388))

* {#HSSY07} Hiroyuki Hata, [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], Shinichiro Yamato, _Baryons from instantons in holographic QCD_, Prog.Theor.Phys.117:1157, 2007 ([arXiv:hep-th/0701280](https://arxiv.org/abs/hep-th/0701280))

* Hiroyuki Hata, Masaki Murata, _Baryons and the Chern-Simons term in holographic QCD with three flavors_ ([arXiv:0710.2579](https://arxiv.org/abs/0710.2579))


* Salvatore Baldino, [[Stefano Bolognesi]], Sven Bjarke Gudnason, Deniz Koksal, _A Solitonic Approach to Holographic Nuclear Physics_, Phys. Rev. D 96, 034008 (2017) ([arXiv:1703.08695](https://arxiv.org/abs/1703.08695))

* Chandan Mondal, Dipankar Chakrabarti, Xingbo Zhao, _Deuteron transverse densities in holographic QCD_, Eur. Phys. J. A 53, 106 (2017) ([arXiv:1705.05808](https://arxiv.org/abs/1705.05808))

* Stanley J. Brodsky, _Color Confinement, Hadron Dynamics, and Hadron Spectroscopy from Light-Front Holography and Superconformal Algebra_ ([arXiv:1709.01191](https://arxiv.org/abs/1709.01191))

* Alfredo Vega, M. A. Martin Contreras, _Melting of scalar hadrons in an AdS/QCD model modified by a thermal dilaton_ ([arXiv:1808.09096](https://arxiv.org/abs/1808.09096))

* Meng Lv, Danning Li, Song He, _Pion condensation in a soft-wall AdS/QCD model_ ([arXiv:1811.03828](https://arxiv.org/abs/1811.03828))

* Kazem Bitaghsir Fadafan, Farideh Kazemian, Andreas Schmitt, _Towards a holographic quark-hadron continuity_ ([arXiv:1811.08698](https://arxiv.org/abs/1811.08698))

* {#SonnenscheinWeissman18} [[Jacob Sonnenschein]], Dorin Weissman, _Excited mesons, baryons, glueballs and tetraquarks: Predictions of the Holography Inspired Stringy Hadron model_, ([arXiv:1812.01619](https://arxiv.org/abs/1812.01619))


* Kazem Bitaghsir Fadafan, Farideh Kazemian, Andreas Schmitt, _Towards a holographic quark-hadron continuity_ ([arXiv:1811.08698](https://arxiv.org/abs/1811.08698))

* {#AbdolmalekiBoroun18} M. Abdolmaleki, G.R. Boroun, _The Survey of Proton Structure Function with the AdS/QCD Correspondence_ Phys.Part.Nucl.Lett. 15 (2018) no.6, 581-584 ([doi:10.1134/S154747711806002X](https://doi.org/10.1134/S154747711806002X))

* Si-wen Li, Hao-qian Li, Sen-kai Luo, *Corrections to the instanton configuration as baryon in holographic QCD* &lbrack;[arXiv:2209.12521](https://arxiv.org/abs/2209.12521)&rbrack;

* Si-wen Li, Hao-qian Li, Yi-peng Zhang: *The worldvolume fermion as baryon in holographic QCD with instanton* &lbrack;[arXiv:2402.01197](https://arxiv.org/abs/2402.01197)&rbrack;


On relation to [[type 0 string theory]]:

* {#GLMR00} Roberto Grena, Simone Lelli, Michele Maggiore, Anna Rissone, _Confinement, asymptotic freedom and renormalons in type 0 string duals_, JHEP 0007 (2000) 005 ([arXiv:hep-th/0005213](https://arxiv.org/abs/hep-th/0005213))

* {#AAS19} Mohammad Akhond, Adi Armoni, Stefano Speziali, _Phases of $U(N_c)$ $QCD_3$ from Type 0 Strings and Seiberg Duality_ ([arxiv:1908.04324](https://arxiv.org/abs/1908.04324))


See also

* S. S. Afonin, _AdS/QCD without Kaluza-Klein modes: Radial spectrum from higher dimensional QCD operators_ ([arXiv:1905.13086](https://arxiv.org/abs/1905.13086))


In relation to the [[open string]] [[tachyon]]:

* [[Matti Järvinen]], [[Elias Kiritsis]], F. Nitti, E. Préau, *Tachyon-dependent Chern-Simons terms and the V-QCD Baryon*,  J. High Energ. Phys. **2022** 160 (2022) &lbrack;<a href="https://doi.org/10.1007/JHEP12(2022)160">doi:10.1007/JHEP12(2022)160</a>, [arXiv:2209.05868](https://arxiv.org/abs/2209.05868)&rbrack;

See also:

* Keiichiro Hori, Hideo Suganuma, Hiroki Kanda, *Numerical analysis of a baryon and its dilatation modes in holographic QCD* &lbrack;[arXiv:2307.16590](https://arxiv.org/abs/2307.16590)&rbrack;



#### Baryons as wrapped branes 

[[baryons]] as [[wrapped brane|wrapped]] [[D4-branes]]:

original articles:

* {#Witten98b} [[Edward Witten]], _Baryons And Branes In Anti de Sitter Space_, JHEP 9807:006, 1998 ([arXiv:hep-th/9805112](https://arxiv.org/abs/hep-th/9805112))

* {#GrossOoguri98} [[David Gross]], [[Hirosi Ooguri]], _Aspects of Large $N$ Gauge Theory Dynamics as Seen by String Theory_, Phys. Rev. D58:106002, 1998 ([arXiv:hep-th/9805129](https://arxiv.org/abs/hep-th/9805129))

* {#BISY98} A. Brandhuber, N. Itzhaki, [[Jacob Sonnenschein]], [[Shimon Yankielowicz]],  _Baryons from Supergravity_, JHEP 9807:020, 1998 ([arxiv:hep-th/9806158](https://arxiv.org/abs/hep-th/9806158))


* Yosuke Imamura, _Supersymmetries and BPS Configurations on Anti-de Sitter Space_, Nucl. Phys. B537:184-202, 1999 ([arxiv:hep-th/9807179](https://arxiv.org/abs/hep-th/9807179))


* {#CGS98} [[Curtis Callan]], Alberto Guijosa, Konstantin G. Savvidy, _Baryons and String Creation from the Fivebrane Worldvolume Action_ ([arxiv:hep-th/9810092](https://arxiv.org/abs/hep-th/9810092))


* [[Curtis Callan]], Alberto Guijosa, Konstantin G. Savvidy, Oyvind Tafjord, _Baryons and Flux Tubes in Confining Gauge Theories from Brane Actions_, Nucl. Phys. B555 (1999) 183-200 ([arxiv:hep-th/9902197](https://arxiv.org/abs/hep-th/9902197))

Review:

* {#Yi09} [[Piljin Yi]], _Holographic Baryons_ ([arXiv:0902.4515](https://arxiv.org/abs/0902.4515), [doi:10.1142/9789814280709_0016](https://www.worldscientific.com/doi/abs/10.1142/9789814280709_0016)), Chapter 16 in: [[Mannque Rho]], [[Ismail Zahed]] (eds.) _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

* {#Yi11} [[Piljin Yi]], _Precision Holographic Baryons_, AIP Conference Proceedings 1388, 106 (2011) ([arXiv:1103.1684](https://arxiv.org/abs/1103.1684), [doi:10.1063/1.3647358](https://aip.scitation.org/doi/abs/10.1063/1.3647358))

* {#Yi13} [[Piljin Yi]], _Two Approaches to Holographic Baryons/Nuclei_, Few-Body Syst (2013) 54: 77. ([doi:10.1007/s00601-012-0373-7](https://doi.org/10.1007/s00601-012-0373-7))


#### Baryons as Skyrmions
 {#ReferencesBaryonsSkyrmions}

[[baryons]] as [[Skyrmions]]:

Review:

* {#Sugimoto16} [[Shigeki Sugimoto]], _Skyrmion and String theory_, chapter 15 in [[Mannque Rho]], [[Ismail Zahed]] (eds.) _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

* {#RhoEtAl16} [[Mannque Rho]] et al., Introduction to _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710), [pdf](https://www.worldscientific.com/doi/suppl/10.1142/9710/suppl_file/9710_intro.pdf))

Original articles



* Kanabu Nawa, Hideo Suganuma, Toru Kojo, _Brane-induced Skyrmions: Baryons in Holographic QCD_, Prog.Theor.Phys.Suppl.168:231-236, 2007 ([arXiv:hep-th/0701007](https://arxiv.org/abs/hep-th/0701007))



* Hovhannes R. Grigoryan, _Baryon as skyrmion-like soliton from the
holographic dual model of QCD_, talk at _[From Strings to Things 2008](http://www.int.washington.edu/PROGRAMS/08-1.html)_ ([pdf](https://www.jlab.org/div_dept/theory/talks/2008/grigoryan08_INT.pdf))

* [[Paul Sutcliffe]], _Skyrmions, instantons and holography_, JHEP 1008:019, 2010 ([arXiv:1003.0023](https://arxiv.org/abs/1003.0023)) 

* [[Stefano Bolognesi]], [[Paul Sutcliffe]], _The Sakai-Sugimoto soliton_, JHEP 1401:078, 2014 ([arXiv:1309.1396](https://arxiv.org/abs/1309.1396))

* [[Paul Sutcliffe]], _Holographic Skyrmions_, Mod. Phys. Lett. B29 (2015) no. 16, 1540051 ([spire:1383608](http://inspirehep.net/record/1383608))

#### Nucleons


nucleon [[form factors]] via [[holographic QCD]]:

* Kiminad A. Mamo, [[Ismail Zahed]],  _Nucleon mass radii and distribution: Holographic QCD, Lattice QCD and GlueX data_ ([arXiv:2103.03186](https://arxiv.org/abs/2103.03186))

* [[Roldão da Rocha]], *Information entropy of nuclear electromagnetic transitions in AdS/QCD* &lbrack;[arXiv:2208.07191](https://arxiv.org/abs/2208.07191)&rbrack;

>  The derived parameters are shown
to corroborate experimental data with great accuracy


via a [[nuclear matrix model]]:

* [[Koji Hashimoto]], [[Norihiro Iizuka]], [[Piljin Yi]], _A Matrix Model for Baryons and Nuclear Forces_, JHEP 1010:003, 2010 ([arXiv:1003.4988](https://arxiv.org/abs/1003.4988))

* Si-wen Li, Tuo Jia, _Matrix model and Holographic Baryons in the D0-D4 background_, Phys. Rev. D 92, 046007 (2015) ([arXiv:1506.00068](https://arxiv.org/abs/1506.00068))


* [[Koji Hashimoto]], [[Yoshinori Matsuo]], [[Takeshi Morita]], _Nuclear states and spectra in holographic QCD_, JHEP12 (2019) 001 ([arXiv:1902.07444](https://arxiv.org/abs/1902.07444))

* Yasuhiro Hayashi, Takahiro Ogino, [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _Stringy excited baryons in holographic QCD_, Prog Theor Exp Phys (2020) ([arXiv:2001.01461](https://arxiv.org/abs/2001.01461))




nuclear binding energy 

* Salvatore Baldino, Lorenzo Bartolini, [[Stefano Bolognesi]], Sven Bjarke Gudnason, _Holographic Nuclear Physics with Massive Quarks_ ([arXiv:2102.00680](https://arxiv.org/abs/2102.00680))


nuclear binding energy via the [[nuclear matrix model]]:

* [[Koji Hashimoto]], [[Yoshinori Matsuo]], _Nuclear binding energy in holographic QCD_ ([arXiv:2103.03563](https://arxiv.org/abs/2103.03563))

See also:

* Federico Castellani, *Nucleon electric and magnetic polarizabilities in Holographic QCD* &lbrack;[arXiv:2402.07553](https://arxiv.org/abs/2402.07553)&rbrack;

* Kazuo Ghoroku, Kouji Kashiwa, Yoshimasa Nakano, Motoi Tachibana, Fumihiko Toyoda: *Chiral condensate in a holographic dilute nuclear matter* &lbrack;[arXiv:2409.03268](https://arxiv.org/abs/2409.03268)&rbrack;




#### Pentaquarks

[[pentaquarks]]:

* Kazuo Ghoroku, Akihiro Nakamura, Tomoki Taminato, Fumihiko Toyoda, _Holographic Penta and Hepta Quark State in Confining Gauge Theories_,
JHEP 1008:007,2010 ([arxiv:1003.3698](https://arxiv.org/abs/1003.3698))

#### Parton distribution functions


* Matteo Rinaldi, _Double parton correlations in mesons within AdS/QCD soft-wall models: a first comparison with lattice data_ ([arXiv:2003.09400](https://arxiv.org/abs/2003.09400))



[[!include heavy flavor hadrodynamics via holographic QCD -- references]]




### Flux string breaking

* Oleg Andreev, _String Breaking, Baryons, Medium, and Gauge/String Duality_ ([arXiv:2003.09880](https://arxiv.org/abs/2003.09880))



### Glueball physics


* {#Suzuki01} Kenji Suzuki, _D0-D4 system and $QCD_{3+1}$_, Phys.Rev. D63 (2001) 084011 ([arXiv:hep-th/0001057](https://arxiv.org/abs/hep-th/0001057))

* Alex S. Miranda, C. A. Ballon Bayona, [[Henrique Boschi-Filho]], [[Nelson R. F. Braga]], _Glueballs at finite temperature from AdS/QCD_, Nucl. Phys. Proc. Suppl. **199** (2010) 107-112 &lbrack;[arXiv:0910.4319](https://arxiv.org/abs/0910.4319), [doi:10.1016/j.nuclphysbps.2010.02.013](https://doi.org/10.1016/j.nuclphysbps.2010.02.013)&rbrack;


* S.S. Afonin, A.D. Katanaeva, _Glueballs and deconfinement temperature in AdS/QCD_ ([arXiv:1809.07730](https://arxiv.org/abs/1809.07730))


* S. S. Afonin, A. D. Katanaeva, E. V. Prokhvatilov, M. I. Vyazovsky, _Deconfinement temperature in AdS/QCD from the spectrum of scalar glueballs_ ([arXiv:2001.07990](https://arxiv.org/abs/2001.07990))

* Cornélio Rodrigues Filho, _Glueballs in the Klebanov-Strassler Theory: Pseudoscalars vs Scalars_ ([arXiv:2011.12689](https://arxiv.org/abs/2011.12689))




[[!include holographic Schwinger effect -- references]]



### Application to vector meson dominance

Derivation of [[vector meson dominance]] via [[holographic QCD]]:

* D.T. Son, M.A. Stephanov, _QCD and dimensional deconstruction_, Phys. Rev. D69 (2004) 065020 ([arXiv:hep-ph/0304182](https://arxiv.org/abs/hep-ph/0304182))

* Sungho Hong, Sukjin Yoon, [[Matthew Strassler]], _On the Couplings of Vector Mesons in AdS/QCD_, JHEP 0604 (2006) 003 ([arXiv:hep-th/0409118](https://arxiv.org/abs/hep-th/0409118))

* Sungho Hong, Sukjin Yoon, [[Matthew Strassler]], _On the Couplings of the Rho Meson in AdS/QCD_ ([cds:816440](https://cds.cern.ch/record/816440), [arXiv:hep-ph/0501197](https://arxiv.org/abs/hep-ph/0501197))

* Leandro Da Rold, Alex Pomarol, _Chiral symmetry breaking from five dimensional spaces_, Nucl. Phys. B721:79-97, 2005 ([arXiv:hep-ph/0501218](https://arxiv.org/abs/hep-ph/0501218))

and specifically in the [[Witten-Sakai-Sugimoto model]]:

* {#SakaiSugimoto05} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], p. 18 and Section 5 of: _More on a holographic dual of QCD_, Progr. Theor. Phys. 114: 1083-1118, 2005 ([arXiv:hep-th/0507073](https://arxiv.org/abs/hep-th/0507073))





### Application to the quark-gluon plasma

Application to the [[quark-gluon plasma]]:

Expositions and reviews include

* Pavel Kovtun, _Quark-Gluon Plasma and String Theory_, RHIC news (2009) ([blog entry](http://www.bnl.gov/rhic/news/091107/story2.asp))

* Makoto Natsuume, _String theory and quark-gluon plasma_ ([arXiv:hep-ph/0701201](http://arxiv.org/abs/hep-ph/0701201))

* [[Steven Gubser]], _Using string theory to study the quark-gluon plasma: progress and perils_ ([arXiv:0907.4808](http://arxiv.org/abs/0907.4808))

* {#BiagazziCotrone12} Francesco Biagazzi, A. Cotrone, _Holography and the quark-gluon plasma_, AIP Conference Proceedings 1492, 307 (2012) ([doi:10.1063/1.4763537]( https://doi.org/10.1063/1.4763537), [slides pdf](http://cp3-origins.dk/content/movies/2013-01-14-bigazzi.pdf))

* {#Brambilla14} Brambilla et al., section 9.2.2 of _[[QCD and strongly coupled gauge theories - challenges and perspectives]]_, Eur Phys J C Part Fields. 2014; 74(10): 2981 ([doi:10.1140/epjc/s10052-014-2981-5](https://link.springer.com/article/10.1140%2Fepjc%2Fs10052-014-2981-5))


Holographic discussion of the [[shear viscosity]] of the quark-gluon plasma goes back to

* {#PolicastroSonStarinets01} [[Giuseppe Policastro]], D.T. Son, A.O. Starinets, _Shear viscosity of strongly coupled $N=4$ supersymmetric Yang-Mills plasma_, Phys. Rev. Lett.87:081601, 2001 ([arXiv:hep-th/0104066](http://arxiv.org/abs/hep-th/0104066))


Other original articles include:

* Brett McInnes, _Holography of the Quark Matter Triple Point_ ([arXiv:0910.4456](http://arxiv.org/abs/0910.4456))

* Hovhannes R. Grigoryan, Paul M. Hohler, Mikhail A. Stephanov, _Towards the Gravity Dual of Quarkonium in the Strongly Coupled QCD Plasma_ ([arXiv:1003.1138](http://arxiv.org/abs/1003.1138))

* Mansi Dhuria, Aalok Misra, _Towards MQGP_, JHEP 1311 (2013) 001 ([arXiv:1306.4339](https://arxiv.org/abs/1306.4339))

* Irina Ya. Aref'eva, Kristina Rannu, Pavel Slepov, _Energy Loss in Holographic Anisotropic Model for Heavy Quarks in External Magnetic Field_ ([arXiv:2012.05758](https://arxiv.org/abs/2012.05758))

See also:

* Si-wen Li, Yi-peng Zhang, *Correlation function of fundamental fermion in holographic QCD* &lbrack;[arXiv:2307.13357](https://arxiv.org/abs/2307.13357)&rbrack;

* [[Nelson R. F. Braga]], Octavio C. Junqueira, *Hawking-Page transition in holographic QCD at finite density*, Phys. Lett. B **855** (2024) 138813 &lbrack;[arXiv:2404.04683](https://arxiv.org/abs/2404.04683), [doi:10.1016/j.physletb.2024.138813](https://doi.org/10.1016/j.physletb.2024.138813)&rbrack;

* {#JokelaJärvinenPiispa24} [[Niko Jokela]], [[Matti Järvinen]], Aleksi Piispa, *Refining holographic models of the quark-gluon plasma* &lbrack;[arXiv:2405.02394](https://arxiv.org/abs/2405.02394)&rbrack;

  > "[[holographic QCD|Holographic QCD]] has reached the level of sophistication that allows for a detailed reproduction of numerous [[lattice QCD]] outcomes"

* [[Tuna Demircik]], [[Niko Jokela]], [[Matti Järvinen]], Aleksi Piispa, *Is holographic quark-gluon plasma homogeneous?* &lbrack;[arXiv:2405.02392](https://arxiv.org/abs/2405.02392)&rbrack;



### Application to lepton anomalous magnetic moment

Application to [[anomalous magnetic moment]] of the [[muon]]:

* Luigi Cappiello, _What does Holographic QCD predict for anomalous $(g-2)_\mu$?_, 2015 ([pdf](https://agenda.infn.it/getFile.py/access?contribId=19&sessionId=5&resId=0&materialId=paper&confId=9430))


* [[Josef Leutgeb]], [[Anton Rebhan]], _Axial vector transition form factors in holographic QCD and their contribution to the anomalous magnetic moment of the muon_ ([arXiv:1912.01596](https://arxiv.org/abs/1912.01596))

* [[Josef Leutgeb]], [[Anton Rebhan]], _Axial vector transition form factors in holographic QCD and their contribution to the muon $g-2$_ ([arXiv:2012.06514](https://arxiv.org/abs/2012.06514))

* [[Josef Leutgeb]], Jonas Mager, [[Anton Rebhan]], *Holographic QCD and the muon anomalous magnetic moment* ([arXiv:2110.07458](https://arxiv.org/abs/2110.07458))




### Application to the Higgs field
  {#ReferencesApplicationToHiggsField}

Application to the [[Higgs field]]:

* {#EspiruKatanaeva18} Domenec Espriu, Alisa Katanaeva, _Composite Higgs Models: a new holographic approach_ ([arXiv:1812.01523](https://arxiv.org/abs/1812.01523))


* [[Johanna Erdmenger]], [[Nick Evans]], [[Werner Porod]], [[Konstantinos Rigatos]], *Gauge/gravity dual dynamics for the strongly coupled sector of composite Higgs models*, JHEP **58** (2021) &lbrack;[arXiv:2010.10279](https://arxiv.org/abs/2010.10279), <a href="https://doi.org/10.1007/JHEP02(2021)058">doi:10.1007/JHEP02(2021)058</a>&rbrack;



### Application to $\theta$-angle axions and strong CP-problem

Realization of [[axions]] and solution of [[strong CP-problem]]:

* Francesco Bigazzi, Alessio Caddeo, Aldo L. Cotrone, Paolo Di Vecchia, Andrea Marzolla, _The Holographic QCD Axion_ ([arXiv:1906.12117](https://arxiv.org/abs/1906.12117))

Discussion of the [[theta angle]] via the the [[graviphoton]] in the [[higher WZW term]] of the [[D4-brane]]:

*  Si-wen Li, around (3.1) of _The theta-dependent Yang-Mills theory at finite temperature in a holographic description_ ([arXiv:1907.10277](https://arxiv.org/abs/1907.10277))

Discussion of the Witten-Veneziano mechanism

* [[Josef Leutgeb]], [[Anton Rebhan]], _Witten-Veneziano mechanism and pseudoscalar glueball-meson mixing in holographic QCD_ ([arxiv:1909.12352](https://arxiv.org/abs/1909.12352))

See also:

* Si-wen Li, Hao-qian Li, Yi-peng Zhang, *The worldvolume fermion as baryon in holographic QCD with a theta angle* &lbrack;[arXiv:2402.01197](https://arxiv.org/abs/2402.01197)&rbrack;




### Application to the QCD trace anomaly

Discussion of the [[QCD trace anomaly]]:

* Jose L. Goity, Roberto C. Trinchero, _Holographic models and the QCD trace anomaly_, Phys. Rev. D 86, 034033 – 2012 ([arXiv:1204.6327](https://arxiv.org/abs/1204.6327))

* Aalok Misra, Charles Gale, _The QCD Trace Anomaly at Strong Coupling from M-Theory_ ([arXiv:1909.04062](https://arxiv.org/abs/1909.04062))

The [[QCD trace anomaly]] affects notably the [[equation of state]] of the [[quark-gluon plasma]], see there at _[References -- Holographic description of quark-gluon plasma](quark-gluon+plasma#ReferencesViaAdSCFT)_

### Application to parton distribution

* Akira Watanabe, Takahiro Sawada, Mei Huang, _Extraction of gluon distributions from structure functions at small x in holographic QCD_ ([arxiv:1910.10008](https://arxiv.org/abs/1910.10008))

> Understanding the nucleon structure is one of the most
important research topics in fundamental science, and tremendous efforts have been done to deepen our knowledge over several decades. $[...]$ Since $[these]$ are highly nonperturbative physical quantities, in principle they are not calculable by the direct use of QCD. Furthermore, although there is available data, this has large errors. These facts cause the huge uncertainties which can be seen in the preceding studies based on the global QCD analysis.

> In this work, we investigate the gluon distribution in nuclei by calculating the structure functions in the framework of holographic QCD, which is constructed based on the AdS/CFT correspondence.



### Application to QCD phases
 {#ReferencesColourSuperconductivity}

Application to [[phase of matter|phases]] of [[QCD]]:

* R. Narayanan, H. Neuberger, _A survey of large $N$ continuum phase transitions_, PoSLAT 2007:020, 2007 ([arXiv:0710.0098](https://arxiv.org/abs/0710.0098))


To [[colour superconductivity]]:

* Kazem Bitaghsir Fadafan, Jesus Cruz Rojas, [[Nick Evans]], _A Holographic Description of Colour Superconductivity_, Phys. Rev. D **98** (2018) 066010  &lbrack;[arXiv:1803.03107](https://arxiv.org/abs/1803.03107), [doi:10.1103/PhysRevD.98.066010](https://doi.org/10.1103/PhysRevD.98.066010)&rbrack;

to [[confinement]]/[[quark-gluon plasma|deconfinement]] phase transiton:

* {#LYY18} Meng-Wei Li, Yi Yang, Pei-Hung Yuan  _Imprints of Early Universe on Gravitational Waves from First-Order Phase Transition in QCD_ ([arXiv:1812.09676](https://arxiv.org/abs/1812.09676))

With [[magnetic fields]]:

* Umut Gursoy, *Holographic QCD and magnetic fields* ([arXiv:2104.02839](https://arxiv.org/abs/2104.02839))

Of relevance in [[neutron stars]]:

* [[Carlos Hoyos]], [[Niko Jokela]], [[Matti Järvinen]], Javier G. Subils, Javier Tarrio, Aleksi Vuorinen, *Transport in strongly coupled quark matter*, Phys. Rev. Lett. **125** (2020) 241601 7Lbrack;[arXiv:2005.14205](https://arxiv.org/abs/2005.14205), [doi:10.1103/PhysRevLett.125.241601](https://doi.org/10.1103/PhysRevLett.125.241601)&rbrack;

* [[Carlos Hoyos]], [[Niko Jokela]], [[Matti Järvinen]], Javier G. Subils, Javier Tarrio, Aleksi Vuorinen, *Holographic approach to transport in dense QCD matter*, Phys. Rev. D **105** 6 (2022) 066014 &lbrack;[arXiv:2109.12122](https://arxiv.org/abs/2109.12122), [doi:10.1103/PhysRevD.105.066014](https://doi.org/10.1103/PhysRevD.105.066014)&rbrack;

* [[Matti Järvinen]], *Holographic modeling of nuclear matter and neutron stars*,  Eur. Phys. J. C. **56** (2021) &lbrack;[arXiv:2110.08281](https://arxiv.org/abs/2110.08281), [doi:10.1140/epjc/s10052-022-10227-x](https://doi.org/10.1140/epjc/s10052-022-10227-x)&rbrack;

* [[Carlos Hoyos]], [[Niko Jokela]], Aleksi Vuorinen, *Holographic approach to compact stars and their binary mergers*, Prog. Part. Nucl. Phys. **126** (2022) 103972 &lbrack;[arXiv:2112.08422] (https://arxiv.org/abs/2112.08422), [doi:10.1016/j.ppnp.2022.103972](https://doi.org/10.1016/j.ppnp.2022.103972)&rbrack;


See also

* Yosuke Imamura, _Baryon Mass and Phase Transitions in Large N Gauge Theory_, Prog. Theor. Phys. 100 (1998) 1263-1272 ([arxiv:hep-th/9806162](https://arxiv.org/abs/hep-th/9806162))

* Varun Sethi, _A study of phases in two flavour holographic QCD_  ([arXiv:1906.10932](https://arxiv.org/abs/1906.10932))

* {#ABBCN18} Riccardo Argurio, Matteo Bertolini, Francesco Bigazzi, Aldo L. Cotrone, Pierluigi Niro, _QCD domain walls, Chern-Simons theories and holography_, J. High Energ. Phys. (2018) 2018: 90 ([arXiv:1806.08292](https://arxiv.org/abs/1806.08292))

* Alfonso Ballon-Bayona, Jonathan P. Shock, Dimitrios Zoakos, _Magnetic catalysis and the chiral condensate in holographic QCD_ ([arXiv:2005.00500](https://arxiv.org/abs/2005.00500))

* Yi Yang, Pei-Hung Yuan, _QCD Phase Diagram by Holography_ ([arXiv:2011.11941](https://arxiv.org/abs/2011.11941))

* Nicolas Kovensky, Aaron Poole, Andreas Schmitt, *Phases of cold holographic QCD: baryons, pions and rho mesons* &lbrack;[arXiv:2302.10675](https://arxiv.org/abs/2302.10675)&rbrack;

* Jesús Cruz Rojas, [[Tuna Demircik]], [[Matti Järvinen]], *Modulated instabilities and the $AdS_2$ point in dense holographic matter* &lbrack;[arXiv:2405.02399](https://arxiv.org/abs/2405.02399)&rbrack;

* Akash Singh, K. P. Yogendran: *Condensate phases of nuclear matter from AdS Hardwall models* &lbrack;[arXiv:2502.05666](https://arxiv.org/abs/2502.05666)&rbrack;








### Application to meson physics

Application to [[meson]] physics:


* Daniel Ávila, Leonardo Patiño, _Melting holographic mesons by cooling a magnetized quark gluon plasma_ ([arXiv:2002.02470](https://arxiv.org/abs/2002.02470))

* Xuanmin Cao, Hui Liu, Danning Li, _Pion quasiparticles and QCD phase transitions at finite temperature and isospin density from holography_, Phys. Rev. D 102, 126014 (2020) ([arXiv:2009.00289](https://arxiv.org/abs/2009.00289))


* Xuanmin Cao, Songyu Qiu, Hui Liu, Danning Li, _Thermal properties of light mesons from holography_ ([arXiv:2102.10946](https://arxiv.org/abs/2102.10946))

* Daisuke Fujii, Akihiro Iwanaka, Mitsuru Tanaka: *Gravitational form factors of pion from top-down holographic QCD* &lbrack;[arXiv:2407.21113](https://arxiv.org/abs/2407.21113)&rbrack;


Application to [[quarkonium]]:

* Hovhannes R. Grigoryan, Paul M. Hohler, Mikhail A. Stephanov, _Towards the Gravity Dual of Quarkonium in the Strongly Coupled QCD Plasma_ ([arXiv:1003.1138](http://arxiv.org/abs/1003.1138))

* Rico Zöllner, Burkhard Kampfer, _Holographic vector meson melting in a thermal gravity-dilaton background related to QCD_ ([arXiv:2002.07200](https://arxiv.org/abs/2002.07200))

* Miguel Angel Martin Contreras, Saulo Diles, Alfredo Vega, _Heavy quarkonia spectroscopy at zero and finite temperature in bottom-up AdS/QCD_ ([arXiv:2101.06212](https://arxiv.org/abs/2101.06212))



[[!include application of holographic QCD to B-meson physics -- references]]


### Relation to holographic entanglement entropy

Relating to [[holographic entanglement entropy]]:

* Zhibin Li, Kun Xu, Mei Huang, _The entanglement properties of holographic QCD model with a critical end point_ ([arXiv:2002.08650](https://arxiv.org/abs/2002.08650))


### Application to defects

Application to QCD [[QFT with defects|with defects]]:

* Alexander Gorsky, Valentin Zakharov, Ariel Zhitnitsky, _On Classification of QCD defects via holography_, Phys. Rev. D79:106003, 2009 ([arxiv:0902.1842](https://arxiv.org/abs/0902.1842))


### Application to thermal QCD

Application to [[thermal field theory|thermal]] [[QCD]]:

* Vikas Yadav, Aalok Misra, _Towards Thermal QCD from M theory at Intermediate 't Hooft Coupling and G-Structure Classification of Non-supersymmetric Underlying Geometries_ ([arXiv:2004.07259](https://arxiv.org/abs/2004.07259))

* Alfonso Ballon-Bayona, Luis A. H. Mamani, Alex S. Miranda, Vilson T. Zanchin, _Effective holographic models for QCD: Thermodynamics and viscosity coefficients_ ([arXiv:2103.14188](https://arxiv.org/abs/2103.14188))

* Qingxuan Fu, Song He, Li Li, Zhibin Li, *Revisiting holographic model for thermal and dense QCD with a critical point* &lbrack;[arXiv:2404.12109](https://arxiv.org/abs/2404.12109)&rbrack;

### Application to anomalies

* Domingo Gallegos, [[Matti Järvinen]], Eamonn Weitz, *Chiral Separation Effect from Holographic QCD* &lbrack;[arXiv:2406.07617](https://arxiv.org/abs/2406.07617)&rbrack;





[[!redirects AdS-QCD correspondences]]

[[!redirects AdS/QCD correspondence]]

[[!redirects AdS-QCD]]
[[!redirects AdS/QCD]]

[[!redirects AdS-QCD duality]]
[[!redirects AdS-QCD dualities]]

[[!redirects AdS/QCD duality]]
[[!redirects AdS/QCD dualities]]

[[!redirects Sakai-Sugimoto model]]
[[!redirects Sakai-Sugimoto models]]

[[!redirects Witten-Sakai-Sugimoto model]]
[[!redirects Witten-Sakai-Sugimoto models]]

[[!redirects Sakai-Sugimoto-Witten model]]
[[!redirects Sakai-Sugimoto-Witten models]]

[[!redirects WSS model]]
[[!redirects WSS models]]

[[!redirects WSS-model]]
[[!redirects WSS-models]]

[[!redirects holographic QCD]]
[[!redirects holographic quantum chromodynamics]]

[[!redirects improved holographic QCD]]
[[!redirects improved holographic quantum chromodynamics]]

[[!redirects Ads/QCD]]


