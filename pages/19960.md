

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[geometric engineering of QFT|geometric engineering]] of [[quantum chromodynamics]] via [[D4-D8-brane bound state]] [[intersecting D-brane models]] is traditionally referred to as the _AdS/QCD correspondence_ or as _holographic QCD_, or similar, referring to the use of the _[[AdS/CFT correspondence]]_. (Notice "CFT" as opposed to "QCD").

The [[AdS-CFT correspondence]] applies _exactly_ only to a few highly symmetric [[quantum field theories]], notably to [[N=4 D=4 super Yang-Mills theory]]. However, away from these special points in field theory space the correspondence does not completely break down, but continues to apply in some approximation and/or with suitable modifications on the [[gravity]]-side of the correspondence.


Notably [[quantum chromodynamics]] (one sector of the [[standard model of particle physics]]) is crucially different from, but still similar enough to, [[N=4 D=4 super Yang-Mills theory]] that some of its [[observables]], in particular otherwise intractable [[non-perturbative effects]], have been argued to be usefully approximated by [[AdS-CFT]]-type [[duality in string theory|dual]] [[supergravity]]-[[observables]].

In particular, the realization of [[quantum chromodynamics]] by [[intersecting D-brane models]] gives a conceptual analytic handle on [[confinement|confined]] [[hadron]] spectra, hence of the physics of ordinary [[atomic nuclei]] (see [below](#Hadrons)). This means ([Witten 98](#Witten98)) that AdS/QCD provides a conceptual solution to the _[[mass gap problem]]_ (albeit not yet a rigorous one), which is out of reach for [[perturbative quantum field theory|perturbation theory]] and otherwise computable only via the blind numerics of [[lattice QCD]].

<center>
<img src="https://ncatlab.org/nlab/files/AdSCFTForQCD.jpg" width="600" />
</center>

> graphics grabbed from [Aoki-Hashimoto-Iizuka 12](#AHI12)

Another example of such observables is the [[shear viscosity]] of the [[quark-gluon plasma]]. 

This approach is hence called the _AdS/QCD-correspondence_ or _holographic QCD_ or similar (see also [[AdS-CFT in condensed matter physics]] for similar relations).

{#FromSNM16} From [Suganuma-Nakagawa-Matsumoto 16, p. 1](#SuganumaNakagawaMatsumoto16):

> Since 1973, [[quantum chromodynamics]] (QCD) has been established as the fundamental theory of the [[strong nuclear force|strong interaction]]. Nevertheless, it is very difficult to solve QCD directly in an analytical manner, and many effective models of QCD have been used instead of QCD, but most models cannot be derived from QCD and its connection to QCD is unclear. 

> To analyze nonperturbative QCD, the [[lattice QCD]] Monte Carlo simulation has been also used as a first-principle calculation of the strong interaction. However, it has several weak points. For example, the [[quantum state|state]] information (e.g. the [[wave function]]) is severely limited, because [[lattice QCD]] is based on the [[path-integral]] formalism. Also, it is difficult to take the [[chiral fermion|chiral]] limit, because zero-mass [[pions]] require [[large volume limit|infinite volume lattices]]. There appears a notorious "[sign problem](lattice+gauge+theory#SignProblem)" at finite density.

> On the other hand, [[holographic QCD]] has a direct connection to [[QCD]], and can be derived from QCD in some limit. In fact, [[holographic QCD]] is equivalent to infrared QCD in [[large N limit|large Nc]] and strong [['t Hooft coupling]] $\lambda$, via gauge/gravity correspondence. Remarkably, holographic QCD is successful to reproduce many hadron phenomenology such as vector meson dominance, the KSRF relation, hidden local symmetry, the GSW model and the Skyrme soliton picture. Unlike lattice QCD simulations, holographic QCD is usually formulated in the chiral limit, and does not have the [sign problem](lattice+gauge+theory#SignProblem) at finite density.



## Models 
 {#Models}

In approaches to $AdS/QCD$ one distinguishes [[top-down model building]] -- where the ambition is to first set up a globally consistent ambient [[intersecting D-brane model]] where a [[Yang-Mills theory]] at least similar to [[QCD]] arises on suitable [[D-branes]] ([[geometric engineering of gauge theories]]) -- from [[bottom-up model building]] approaches which are more cavalier about global consistency and first focus on accurately fitting the intended [[phenomenology]] of [[QCD]] as the [[asymptotic boundary|asymptotic]] [[boundary field theory]] of [[gravity]]+[[gauge theory]] on some [[anti de Sitter spacetime]]. (Eventually both these approaches should meet "in the middle" to produce a [[model (in theoretical physics)|model]] which is both [[standard model of particle physics|realistic]] as well as globally consistent as a [[string vacuum]]; see also at _[[string phenomenology]]_.)

<center>
<img src="https://ncatlab.org/nlab/files/BottomUpAndTopDownIntersDBraneModelBuilding.png" width="700"/>
</center>

>  graphics grabbed from [Aldazabal-Ibáñez-Quevedo-Uranga 00](bottom-up+and+top-down+model+building#AldazabalIbanezQuevedoUranga00)


### Top-down models
 {#TopDownModels}

#### Witten-Sakai-Sugimoto model
  {#WittenSakaiSugimotoModel}

A good [[top-down model building]]-approach to AdS/QCD is due to [Sakai-Sugimoto 04](#SakaiSugimoto04), [Sakai-Sugimoto 05](#SakaiSugimoto05) based on [Witten 98](#Witten98), see [Rebhan 14](#Rebhan14), [Sugimoto 16](#Sugimoto16) for review. 

##### Brane configuration
 {#WSSBraneConfiguration}

The [[Witten-Sakai-Sugimoto model]] [[geometric engineering of QFT|geometrically engineers]] something at least close to [[QCD]]: on the [[worldvolume]] of [[intersecting D-brane models|coincident]] [[black brane|black]] [[M5-branes]] with [[near horizon geometry]] a [[KK-compactification]] of $AdS_7 \times S^4$ in the decoupling limit where the [[worldvolume]] theory becomes the [[6d (2,0)-superconformal SCFT]]. Here the [[KK-compactification]] is on a [[torus]] with anti-periodic boundary conditions for the [[fermions]] in one direction, thus [[spontaneous symmetry breaking|breaking]] all [[supersymmetry]] ([[Scherk-Schwarz mechanism]]). Here the first circle [[KK-compactification|reduction]] realizes, under [[duality between M-theory and type IIA string theory]], the [[M5-branes]] as [[D4-branes]], hence the model now looks like 5d [[Yang-Mills theory]] further [[KK-compactification|compactified]] on a circle. ([Witten 98, section 4](#Witten98)). 

The further introduction of [[intersecting D-brane model|intersecting]] [[D8-branes]] and [[anti D-brane|anti]] [[D8-branes]] to [[D4-D8 brane bound states]] makes a sensible sector of [[chiral fermions]] appear in this model ([Sakai-Sugimoto 04](#SakaiSugimoto04), [Sakai-Sugimoto 05](#SakaiSugimoto05))

{#BraneConfigurationDiagram} The following diagram indicates the Witten-Sakai-Sugimoto [[intersecting D-brane model]] that [[geometric engineering of QFT|geometrically engineers]] [[QCD]]:

<center>
<img src="https://ncatlab.org/nlab/files/WSSBraneConfigurationEngineeringQCDII.jpg" width="740"/>
</center>

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/D8D6NS5.jpg" width="380"/>
</div>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

Here we are showing

1. the [[color charge|color]] [[D4-branes]];

1. the [[flavour (particle physics)|flavor]] [[D8-branes]];

   with

   1. the [[5d Chern-Simons theory]] on their [[worldvolume]]

   1. the corresponding [[4d WZW model]] on the boundary

   both exhibiting the [[meson fields]];

1. the [[baryon]] [[D4-branes]]

   (see below at _[Baryons](#Baryons)_);

1. the [[Yang-Mills monopole]] [[D6-branes]] 

   (see at _[[D6-D8-brane bound state]]_);

1. the [[NS5-branes]] (often not considered here).

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

\linebreak

\linebreak

\linebreak

Here are some further illustrations, taken from the literature:


<center>
<img src="https://ncatlab.org/nlab/files/SakaiSugimotoModel.jpg" width="600">
</center>

> graphics grabbed from [Erlich 09, section 1.1](#Erlich09)


<center>
<img src="https://ncatlab.org/nlab/files/IntersectingBranesSSWModel.jpg" width="700">
</center>

> graphics grabbed from [Rebhan 14](#Rebhan14)

##### Glueballs

Already before adding the D8-branes (hence already in the Witten model) this produces a pure [[Yang-Mills theory]] whose [[glueball]]-spectra may usefully be compared to those of [[QCD]]:

<center>
<img src="https://ncatlab.org/nlab/files/GlueballSpectrumSSWModel.jpg" width="700">
</center>

> graphics grabbed from [Rebhan 14](#Rebhan14)


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

For review see [Sugimoto 16](#Sugimoto16), also [Rebhan 14, around (18)](#Rebhan14).

<center>
<img src="https://ncatlab.org/nlab/files/BaryonsAsD4Branes.jpg" width="700">
</center>

> graphics grabbed from [Sugimoto 16](#Sugimoto16)


Equivalently, these baryon states are the [[Yang-Mills instantons]] on the [[D8-brane]] giving the [[D4-D8 brane bound state]] ([Sakai-Sugimoto 04, 5.7](#SakaiSugimoto04)) as a special case of the general situation for [[Dp-D(p+4)-brane bound states]] (e.g. [Tong 05, 1.4](Dp-D%28p%2B4%29-brane+bound+state#Tong05)).

<center>
<img src="https://ncatlab.org/nlab/files/BaryonVertexDefectInAdSQCD.jpg" width="490">
</center>

> graphics grabbed from [Cai-Li 17](#CaiLi17)


<center>
<img src="https://ncatlab.org/nlab/files/D6InD8InAdSQCD.jpg" width="700">
</center>

> graphics grabbed from [ABBCN 18](#ABBCN18)


This already produces [[baryon]] [[mass]] spectra with moderate quantitative agreement with [[experiment]] ([HSSY 07](#HSSY07)):


<center>
<img src="https://ncatlab.org/nlab/files/BaryonSpectrumInSakaiSugimoto.jpg" width="700">
</center>

> graphics grabbed from [Sugimoto 16](#Sugimoto16)


Moreover, the above 4-brane model for baryons is claimed to be equivalent to the old **[[Skyrmion]] model** (see [Sakai-Sugimoto 04, section 5.2](#SakaiSugimoto04), [Sakai-Sugimoto 05, section 3.3](#SakaiSugimoto05), [Sugimoto 16, 15.4.1](#Sugimoto16), [Bartolini 17](#Bartolini17)). 

But the Skyrmion model of baryons has been shown to apply also to [[bound states]] of [[baryons]], namely the [[atomic nuclei]]  ([Riska 93](Skyrmion#Riska93), [Battye-Manton-Sutcliffe 10](Skyrmion#BattyeMantonSutcliffe10), [Manton 16](Skyrmion#Manton16), [Naya-Sutcliffe 18](Skyrmion#NayaSutcliffe18)), at least for small [[atomic number]].

For instance, various [[experiment|experimentally]] observed resonances of the [[carbon]] [[nucleus]] are modeled well by a Skyrmion with [[atomic number]] 6 and hence baryon number 12 ([Lau-Manton 14](Skyrmion#LauMaonton14)): 

\begin{center}
<img src="https://ncatlab.org/nlab/files/SkyrmionB12.jpg" width="200">
\end{center}

> graphics grabbed form [Lau-Manton 14](Skyrmion#LauMaonton14)

More generally, the [[Skyrmion]]-model of [[atomic nuclei]] gives good matches with [[experiment]] if not just the [[pi meson]] but also the [[rho meson]]-background is included ([Naya-Sutcliffe 18](Skyrmion#NayaSutcliffe18)):

\begin{center}
<img src="https://ncatlab.org/nlab/files/SkyrmionsWithRho.jpg" width="800">
\end{center}

> graphics grabbed form [Naya-Sutcliffe 18](Skyrmion#NayaSutcliffe18)


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

Computations due to [Katz-Lewandowski-Schwartz 05](#KatzLewandowskiSchwartz05) find the following comparison of AdS/QCD predictions to [[QCD]]-[[experiment]]

<center>
<img src="https://ncatlab.org/nlab/files/HardWallModelPredictions.jpg" width="400">
</center>

> graphics grabbed from [Erlich 09, section 1.2](#Erlich09)

Further refinement to the "soft-wall model" is due to [KKSS 06](#KKSS06) and further to "improved holographic QCD" is due to [Gursoy-Kiritsis-Nitti 07](#GursoyKiritsisNitti07), [Gursoy-Kiritsis 08](#GursoyKiritsis08), see [GKMMN 10](#GKMMN10).


<center>
<img src="https://ncatlab.org/nlab/files/GlueballMasses.jpg" width="660">
</center>

> graphics grabbed from [GKMMN 10](#GKMMN10)


<center>
<img src="https://ncatlab.org/nlab/files/ImprovedAdSQCD.jpg" width="680">
</center>

> graphics grabbed from [GKMMN 10](#GKMMN10)

These computations shown so far all use just the field theory in the bulk, not yet the stringy modes ([[limit of a sequence|limit]] of vanishing [[string length]] $\sqrt{\alpha'} \to 0$). Incorporating bulk string corrections further improves these results, see [Sonnenschein-Weissman 18](#SonnenscheinWeissman18).

### Embedding into a full standard model


[Nastase 03, p. 2](#Nastase03):

> An obvious question then is can one lift this D brane construction for the holographic dual of [[QCD]] to a [[standard model of particle physics|Standard Model]] embedding?  I study this question in the context of [[intersecting D-brane models|D-brane-world]] [[GUT]] models and find that one needs to have [[TeV-scale string theory]].


## Related concepts

* [[holographic entanglement entropy]]

* [[AdS-CFT in condensed matter physics]]

* [[holography as Koszul duality]]

* [[lattice QCD]]


## References

### General
 {#ReferencesGeneral}

Review:

* {#Aharony02} [[Ofer Aharony]], _The non-AdS/non-CFT correspondence, or three different paths to QCD_, Progress in string, field and particle theory. Springer, Dordrecht, 2003. 3-24 ([arXiv:hep-th/0212193](https://arxiv.org/abs/hep-th/0212193))

* {#Erlich09} Joshua Erlich, _How Well Does AdS/QCD Describe QCD?_,  	Int. J. Mod. Phys.A25:411-421,2010 ([arXiv:0908.0312](https://arxiv.org/abs/0908.0312))

* Marco Panero, _QCD thermodynamics in the large-$N$ limit_, 2010 ([[PaneroAdsQCD.pdf:file|pdf]])



* Youngman Kim and Deokhyun Yi, _Holography at Work for Nuclear and Hadron Physics_, Advances in High Energy Physics, Volume 2011, Article ID 259025, 62 pages
([arXiv:1107.0155](https://arxiv.org/abs/1107.0155), [doi:10.1155/2011/259025](http://dx.doi.org/10.1155/2011/259025))


* M. R. Pahlavani, R. Morad, _Application of AdS/CFT in Nuclear Physics_, Advances in High Energy Physics ([arXiv:1403.2501](https://arxiv.org/abs/1403.2501))

* Jorge Casalderrey-Solana, Hong Liu, David Mateos, Krishna Rajagopal, Urs Achim Wiedemann,

  _Gauge/string duality, hot QCD and heavy ion collisions_, 

  Cambridge University Press, 2014 ([arXiv:1101.0618](https://arxiv.org/abs/1101.0618))
-7+9
32
* {#AHI12} Sinya Aoki, [[Koji Hashimoto]], Norihiro Iizuka, _Matrix Theory for Baryons: An Overview of Holographic QCD for Nuclear Physics_, Reports on Progress in Physics, Volume 76, Number 10 ([arxiv:1203.5386](https://arxiv.org/abs/1203.5386))



* Youngman Kim, Ik Jae Shin, Takuya Tsukioka, _Holographic QCD: Past, Present, and Future_, Progress in Particle and Nuclear Physics
Volume 68, January 2013, Pages 55-112 Progress in Particle and Nuclear Physics ([arXiv:1205.4852](https://arxiv.org/abs/1205.4852))

* Joshua Erlich, _An Introduction to Holographic QCD for Nonspecialists_,  Contemporary Physics ([arXiv:1407.5002](https://arxiv.org/abs/1407.5002))

* {#Guijosa16} Alberto Guijosa, _QCD, with Strings Attached_, IJMPE Vol. 25, No. 10 (2016) 1630006 ([arXiv:1611.07472](https://arxiv.org/abs/1611.07472))

See also

* Wikipedia, _[AdS/QCD correspondence](https://en.wikipedia.org/wiki/AdS/QCD_correspondence)_ 


The top-down Sakai-Sugimoto model is due to 

* {#SakaiSugimoto04} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _Low energy hadron physics in holographic QCD_, Progr. Theor. Phys. 113: 843-882, 2005 ([arXiv:hep-th/0412141](https://arxiv.org/abs/hep-th/0412141))

* {#SakaiSugimoto05} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _More on a holographic dual of QCD_, Progr. Theor. Phys. 114: 1083-1118, 2005 ([arXiv:hep-th/0507073](https://arxiv.org/abs/hep-th/0507073))

along the lines of

* [[Andreas Karch]], [[Emanuel Katz]],  _Adding flavor to AdS/CFT_, JHEP 0206:043, 2002 ([arxiv:hep-th/0205236](https://arxiv.org/abs/hep-th/0205236))


and based on 

* {#Witten98} [[Edward Witten]], _Anti-de Sitter Space, Thermal Phase Transition, And Confinement In Gauge Theories_, Adv. Theor. Math. Phys.2:505-532, 1998 ([arXiv:hep-th/9803131](https://arxiv.org/abs/hep-th/9803131))

further developed in 

* {#Bartolini17} Lorenzo Bartolini, [[Stefano Bolognesi]], Andrea Proto, _From the Sakai-Sugimoto Model to the Generalized Skyrme Model_, Phys. Rev. D 97, 014024 2018 ([arXiv:1711.03873](https://arxiv.org/abs/1711.03873))

reviewed in 

* {#Rebhan14} Anton Rebhan, _The Witten-Sakai-Sugimoto model: A brief review and some recent results_, 3rd International Conference on New Frontiers in Physics, Kolymbari, Crete, 2014 ([arXiv:1410.8858](https://arxiv.org/abs/1410.8858))

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



The bottom-up hard-wall model is due to

* {#ErlichKatzSonStephanov05} Joshua Erlich, [[Emanuel Katz]], Dam T. Son, Mikhail A. Stephanov, _QCD and a Holographic Model of Hadrons_, Phys.Rev.Lett.95:261602, 2005 ([arXiv:hep-ph/0501128](https://arxiv.org/abs/hep-ph/0501128))

while the soft-wall refinement is due to 

* {#KKSS06} [[Andreas Karch]], [[Emanuel Katz]], Dam T. Son, Mikhail A. Stephanov, _Linear Confinement and AdS/QCD_, Phys.Rev.D74:015005, 2006 ([arXiv:hep-ph/0602229](https://arxiv.org/abs/hep-ph/0602229))





see also

* Alfredo Vega, Paulina Cabrera, _Family of dilatons and metrics for AdS/QCD models_, Phys. Rev. D 93, 114026 (2016) ([arXiv:1601.05999](https://arxiv.org/abs/1601.05999))

* Alfonso Ballon-Bayona, Luis A. H. Mamani, _Nonlinear realisation of chiral symmetry breaking in holographic soft wall models_ ([arXiv:2002.00075](https://arxiv.org/abs/2002.00075))

and the version _improved holographic QCD_ is due to

* {#GursoyKiritsis08} Umut Gursoy, [[Elias Kiritsis]], _Exploring improved holographic theories for QCD: Part I_, JHEP 0802:032, 2008 ([arXiv:0707.1324](https://arxiv.org/abs/0707.1324))

* {#GursoyKiritsisNitti07} Umut Gursoy, [[Elias Kiritsis]], Francesco Nitti, _Exploring improved holographic theories for QCD: Part II_, JHEP 0802:019, 2008 ([arXiv:0707.1349](https://arxiv.org/abs/0707.1349))

reviewed in 

* {#GKMMN10} Umut Gürsoy, [[Elias Kiritsis]], Liuba Mazzanti, Georgios Michalogiorgakis, Francesco Nitti, _Improved Holographic QCD_, Lect.Notes Phys.828:79-146,2011 ([arXiv:1006.5461](https://arxiv.org/abs/1006.5461))

More developments on improved holographic QCD:

* Takaaki Ishii, Matti Järvinen, Govert Nijs, _Cool baryon and quark matter in holographic QCD_ ([arXiv:1903.06169](https://arxiv.org/abs/1903.06169))

The extreme form of bottom-up holographic model building is explored in

* {#HashimotoEtAl18} [[Koji Hashimoto]], Sotaro Sugishita, Akinori Tanaka, Akio Tomiya, _Deep Learning and Holographic QCD_, Phys. Rev. D 98, 106014 (2018) ([arXiv:1809.10536](https://arxiv.org/abs/1809.10536))

where an appropriate [[bulk]] geometry is computer-generated from specified boundary behaviour.

A [[semiclassical approximation]] of bottom-up AdS/QCD is _[[holographic light front QCD]]_, reviewed in

* {#ZhouDosch18} Liping Zou, H.G. Dosch, _A very Practical Guide to Light Front Holographic QCD_, ([arXiv:1801.00607](https://arxiv.org/abs/1801.00607))

see also

* Harun Omer, _Embedding LFHQCD in Worldsheet String Theory_ ([arXiv:1909.12866](https://arxiv.org/abs/1909.12866))

* Stanley J. Brodsky, _Color Confinement and Supersymmetric Properties of Hadron Physics from Light-Front Holography_ ([arXiv:1912.12578](https://arxiv.org/abs/1912.12578))

and in relation to [[B-meson]] physics

* [[Mohammad Ahmady]], _Holographic light-front QCD in B meson phenomenology_ ([arXiv:2001.00266](https://arxiv.org/abs/2001.00266))


### String- and M-theory corrections
 {#StringAndMTheoryCorrection}

On [[perturbative string theory]]-corrections (for small [['t Hooft coupling]] $\lambda = g_{YM}^2 N$) and/or [[M-theory]]-corrections (for [[large N limit|small N]]) to the [[supergravity]]-approximation of the [[AdS/CFT correspondence]], i.e. the [[large 1/N limit]] of the correspondence:

On the general need for [[M-theory]] at small $N_c$ in gauge/gravity duality:

* [[Leonard Susskind]], _Another Conjecture about M(atrix) Theory_ ([arXiv:hep-th/9704080](https://arxiv.org/abs/hep-th/9704080)) 

* [[Nissan Itzhaki]], [[Juan Maldacena]], [[Jacob Sonnenschein]], [[Shimon Yankielowicz]], Section 6 of: _Supergravity and The Large $N$ Limit of Theories With Sixteen Supercharges_, Phys. Rev. D 58, 046004 (1998) ([arXiv:hep-th/9802042](https://arxiv.org/abs/hep-th/9802042))

On stringy corrections in the [[AdS/QCD correspondence]]:

* B. Basso, _Cusp anomalous dimension in planar maximally supersymmetric Yang-Mills theory_ ([spire:858223](http://inspirehep.net/record/858223))

  > "The result $[$(29)$]$ coincides exactly with the recent two-loop stringy correction computed in [Alday-Maldacena 07](https://arxiv.org/abs/0708.0672), providing a striking confirmation of the AdS/CFT correspondence."

Specifically for AdS/QCD:

* H. Dorn, H.-J. Otto, _On Wilson loops and $Q\bar Q$-potentials from the AdS/CFT relation at $T\geq 0$_, In: A. Ceresole, C. Kounnas , [[Dieter Lüst]], [[Stefan Theisen]]  (eds.) _Quantum Aspects of Gauge Theories, Supersymmetry and Unification_ Lecture Notes in Physics, vol 525. Springer 2007 ([arXiv:hep-th/9812109](https://arxiv.org/abs/hep-th/9812109), 
[doi:10.1007/BFb0104268](https://doi.org/10.1007/BFb0104268))


* Csaba Csaki, [[Matthew Reece]], John Terning, _The AdS/QCD Correspondence: Still Undelivered_, JHEP 0905:067, 2009 ([arXiv:0811.3001](https://arxiv.org/abs/0811.3001))

Discussion of [[large N limit|small N]] effects in [[M-theory]] [[AdS4/CFT3]] and using the [[conformal bootstrap]]:

* Nathan B. Agmon, Shai M. Chester, Silviu S. Pufu, _Solving M-theory with the Conformal Bootstrap_, JHEP 06 (2018) 159 ([arXiv:1711.07343](https://arxiv.org/abs/1711.07343))







### Hadron physics

Application to [[confinement|confined]] [[hadron]]-physics:

Review:

* Henrique Boschi-Filho, _Hadrons in AdS/QCD models_, Journal of Physics: Conference Series, Volume 706, Section 4 2008 ([doi:10.1088/1742-6596/706/4/042008](http://iopscience.iop.org/article/10.1088/1742-6596/706/4/042008))

* Kanabu Nawa, Hideo Suganuma, Toru Kojo, _Baryons in Holographic QCD_, Phys.Rev.D75:086003, 2007 ([arXiv:hep-th/0612187](https://arxiv.org/abs/hep-th/0612187))

* Deog Ki Hong, Mannque Rho, Ho-Ung Yee, Piljin Yi, _Chiral Dynamics of Baryons from String Theory_, Phys.Rev.D76:061901, 2007 ([arXiv:hep-th/0701276](https://arxiv.org/abs/hep-th/0701276))

* Deog Ki Hong, _Baryons in holographic QCD_, talk at _[From Strings to Things 2008](http://www.int.washington.edu/PROGRAMS/08-1.html)_ ([pdf](http://www.int.washington.edu/talks/WorkShops/int_08_1/People/Hong_D/Hong.pdf))

* Johanna Erdmenger, Nick Evans, Ingo Kirsch, Ed Threlfall, _Mesons in Gauge/Gravity Duals - A Review_, Eur. Phys. J. A35:81-133, 2008 ([arXiv:0711.4467](https://arxiv.org/abs/0711.4467))

* Stanley J. Brodsky, _Hadron Spectroscopy and Dynamics from Light-Front Holography and Superconformal Algebra_ ([arXiv:1802.08552](https://arxiv.org/abs/1802.08552))

* [[Koji Hashimoto]], [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _Holographic Baryons : Static Properties and Form Factors from Gauge/String Duality_, Prog. Theor. Phys.120:1093-1137, 2008 ([arXiv:0806.3122](https://arxiv.org/abs/0806.3122))

* Alex Pomarol, Andrea Wulzer, _Baryon Physics in Holographic QCD_, Nucl. Phys. B809:347-361, 2009 ([arXiv:0807.0316](https://arxiv.org/abs/0807.0316))

* Thomas Gutsche, Valery E. Lyubovitskij, Ivan Schmidt, Alfredo Vega, _Nuclear physics in soft-wall AdS/QCD: Deuteron electromagnetic form factors_, Phys. Rev. D 91, 114001 (2015) ([arXiv:1501.02738](https://arxiv.org/abs/1501.02738))

* Marco Claudio Traini, _Generalized Parton Distributions: confining potential effects within AdS/QCD_, Eur. Phys. J. C (2017) 77:246 ([arXiv:1608.08410](https://arxiv.org/abs/1608.08410))

* {#CaiLi17} Wenhe Cai, Si-wen Li, _Holographic three flavor baryon in the Witten-Sakai-Sugimoto model with the D0-D4 background_, Eur. Phys. J. C (2018) 78: 446 ([arXiv:1712.06304](https://arxiv.org/abs/1712.06304))




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

* {#SonnenscheinWeissman18} Jacob Sonnenschein, Dorin Weissman, _Excited mesons, baryons, glueballs and tetraquarks: Predictions of the Holography Inspired Stringy Hadron model_, ([arXiv:1812.01619](https://arxiv.org/abs/1812.01619))


* Kazem Bitaghsir Fadafan, Farideh Kazemian, Andreas Schmitt, _Towards a holographic quark-hadron continuity_ ([arXiv:1811.08698](https://arxiv.org/abs/1811.08698))

* {#AbdolmalekiBoroun18} M. Abdolmaleki, G.R. Boroun, _The Survey of Proton Structure Function with the AdS/QCD Correspondence_ Phys.Part.Nucl.Lett. 15 (2018) no.6, 581-584 ([doi:10.1134/S154747711806002X](https://doi.org/10.1134/S154747711806002X))

On relation to [[type 0 string theory]]:

* {#GLMR00} Roberto Grena, Simone Lelli, Michele Maggiore, Anna Rissone, _Confinement, asymptotic freedom and renormalons in type 0 string duals_, JHEP 0007 (2000) 005 ([arXiv:hep-th/0005213](https://arxiv.org/abs/hep-th/0005213))

* {#AAS19} Mohammad Akhond, Adi Armoni, Stefano Speziali, _Phases of $U(N_c)$ $QCD_3$ from Type 0 Strings and Seiberg Duality_ ([arxiv:1908.04324](https://arxiv.org/abs/1908.04324))


See also

* S. S. Afonin, _AdS/QCD without Kaluza-Klein modes: Radial spectrum from higher dimensional QCD operators_ ([arXiv:1905.13086](https://arxiv.org/abs/1905.13086))



#### Baryons as wrapped branes 

[[baryons]] as [[wrapped brane|wrapped]] [[D4-branes]]:

original articles:

* {#Witten98b} [[Edward Witten]], _Baryons And Branes In Anti de Sitter Space_, JHEP 9807:006, 1998 ([arXiv:hep-th/9805112](https://arxiv.org/abs/hep-th/9805112))

* {#GrossOoguri98} [[David Gross]], [[Hirosi Ooguri]], _Aspects of Large N Gauge Theory Dynamics as Seen by String Theory_, Phys. Rev. D58:106002,1998 ([arXiv:hep-th/9805129](https://arxiv.org/abs/hep-th/9805129))

* {#BISY98} A. Brandhuber, N. Itzhaki, J. Sonnenschein, S. Yankielowicz  _Baryons from Supergravity_, JHEP 9807:020,1998 ([arxiv:hep-th/9806158](https://arxiv.org/abs/hep-th/9806158))


* Yosuke Imamura, _Supersymmetries and BPS Configurations on Anti-de Sitter Space_, Nucl. Phys. B537:184-202,1999 ([arxiv:hep-th/9807179](https://arxiv.org/abs/hep-th/9807179))


* {#CGS98} Curtis G. Callan, Alberto Guijosa, Konstantin G. Savvidy, _Baryons and String Creation from the Fivebrane Worldvolume Action_ ([arxiv:hep-th/9810092](https://arxiv.org/abs/hep-th/9810092))


* Curtis G. Callan, Alberto Guijosa, Konstantin G. Savvidy, Oyvind Tafjord, _Baryons and Flux Tubes in Confining Gauge Theories from Brane Actions_, Nucl. Phys. B555 (1999) 183-200 ([arxiv:hep-th/9902197](https://arxiv.org/abs/hep-th/9902197))

Review:

* P. Yi, _Two Approaches to Holographic Baryons/Nuclei_, Few-Body Syst (2013) 54: 77. ([doi:10.1007/s00601-012-0373-7](https://doi.org/10.1007/s00601-012-0373-7))


#### Baryons as Skyrmions
 {#ReferencesBaryonsSkyrmions}

[[baryons]] as [[Skyrmions]]:

Review:

* {#Sugimoto16} [[Shigeki Sugimoto]], _Skyrmion and String theory_, chapter 15 in [[Mannque Rho]], [[Ismail Zahed]] (eds.) _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

Original articles



* Kanabu Nawa, Hideo Suganuma, Toru Kojo, _Brane-induced Skyrmions: Baryons in Holographic QCD_, Prog.Theor.Phys.Suppl.168:231-236, 2007 ([arXiv:hep-th/0701007](https://arxiv.org/abs/hep-th/0701007))



* Hovhannes R. Grigoryan, _Baryon as skyrmion-like soliton from the
holographic dual model of QCD_, talk at _[From Strings to Things 2008](http://www.int.washington.edu/PROGRAMS/08-1.html)_ ([pdf](https://www.jlab.org/div_dept/theory/talks/2008/grigoryan08_INT.pdf))

* [[Paul Sutcliffe]], _Skyrmions, instantons and holography_, JHEP 1008:019, 2010 ([arXiv:1003.0023](https://arxiv.org/abs/1003.0023)) 

* [[Stefano Bolognesi]], [[Paul Sutcliffe]], _The Sakai-Sugimoto soliton_, JHEP 1401:078, 2014 ([arXiv:1309.1396](https://arxiv.org/abs/1309.1396))

* [[Paul Sutcliffe]], _Holographic Skyrmions_, Mod. Phys. Lett. B29 (2015) no. 16, 1540051 ([spire:1383608](http://inspirehep.net/record/1383608))





#### Pentaquarks

[[pentaquarks]]:

* Kazuo Ghoroku, Akihiro Nakamura, Tomoki Taminato, Fumihiko Toyoda, _Holographic Penta and Hepta Quark State in Confining Gauge Theories_,
JHEP 1008:007,2010 ([arxiv:1003.3698](https://arxiv.org/abs/1003.3698))


### Glueball physics

* {#Suzuki01} Kenji Suzuki, _D0-D4 system and $QCD_{3+1}$_, Phys.Rev. D63 (2001) 084011 ([arXiv:hep-th/0001057](https://arxiv.org/abs/hep-th/0001057))

* S.S. Afonin, A.D. Katanaeva, _Glueballs and deconfinement temperature in AdS/QCD_ ([arXiv:1809.07730](https://arxiv.org/abs/1809.07730))


* S. S. Afonin, A. D. Katanaeva, E. V. Prokhvatilov, M. I. Vyazovsky, _Deconfinement temperature in AdS/QCD from the spectrum of scalar glueballs_ ([arXiv:2001.07990](https://arxiv.org/abs/2001.07990))






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


### Application to lepton anomalous magnetic moment

Application to [[anomalous magnetic moment]] of the [[muon]]:

* Luigi Cappiello, _What does Holographic QCD predict for anomalous $(g-2)_\mu$?_, 2015 ([pdf](https://agenda.infn.it/getFile.py/access?contribId=19&sessionId=5&resId=0&materialId=paper&confId=9430))


### Application to Higgs field
  {#ReferencesApplicationToHiggsField}

Application to [[Higgs field]]:

* {#EspiruKatanaeva18} Domenec Espriu, Alisa Katanaeva, _Composite Higgs Models: a new holographic approach_ ([arXiv:1812.01523](https://arxiv.org/abs/1812.01523))

### Application to $\theta$-angle axions and strong CP-problem

Realization of [[axions]] and solution of [[strong CP-problem]]:

* Francesco Bigazzi, Alessio Caddeo, Aldo L. Cotrone, Paolo Di Vecchia, Andrea Marzolla, _The Holographic QCD Axion_ ([arXiv:1906.12117](https://arxiv.org/abs/1906.12117))

Discussion of the [[theta angle]] via the the [[graviphoton]] in the [[higher WZW term]] of the [[D4-brane]]:

*  Si-wen Li, around (3.1) of _The theta-dependent Yang-Mills theory at finite temperature in a holographic description_ ([arXiv:1907.10277](https://arxiv.org/abs/1907.10277))

Discussion of the Witten-Veneziano mechanism

* Josef Leutgeb, Anton Rebhan, _Witten-Veneziano mechanism and pseudoscalar glueball-meson mixing in holographic QCD_ ([arxiv:1909.12352](https://arxiv.org/abs/1909.12352))



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

* Kazem Bitaghsir Fadafan, Jesus Cruz Rojas, Nick Evans, _A Holographic Description of Colour Superconductivity_ ([arXiv:1803.03107](https://arxiv.org/abs/1803.03107))

to [[confinement]]/[[quark-gluon plasma|deconfinement]] phase transiton:

* {#LYY18} Meng-Wei Li, Yi Yang, Pei-Hung Yuan  _Imprints of Early Universe on Gravitational Waves from First-Order Phase Transition in QCD_ ([arXiv:1812.09676](https://arxiv.org/abs/1812.09676))

See also

* Yosuke Imamura, _Baryon Mass and Phase Transitions in Large N Gauge Theory_, Prog. Theor. Phys. 100 (1998) 1263-1272 ([arxiv:hep-th/9806162](https://arxiv.org/abs/hep-th/9806162))

* Varun Sethi, _A study of phases in two flavour holographic QCD_  ([arXiv:1906.10932](https://arxiv.org/abs/1906.10932))

* {#ABBCN18} Riccardo Argurio, Matteo Bertolini, Francesco Bigazzi, Aldo L. Cotrone, Pierluigi Niro, _QCD domain walls, Chern-Simons theories and holography_, J. High Energ. Phys. (2018) 2018: 90 ([arXiv:1806.08292](https://arxiv.org/abs/1806.08292))

* Nicolas Kovensky, Andreas Schmitt, _Heavy Holographic QCD_ ([arxiv:1911.08433](https://arxiv.org/abs/1911.08433))


### Application to meson physics

Application to [[meson]] physics:


* Daniel Ávila, Leonardo Patiño, _Melting holographic mesons by cooling a magnetized quark gluon plasma_ ([arXiv:2002.02470](https://arxiv.org/abs/2002.02470))

Application to [[quarkonium]]:

* Rico Zöllner, Burkhard Kampfer, _Holographic vector meson melting in a thermal gravity-dilaton background related to QCD_ ([arXiv:2002.07200](https://arxiv.org/abs/2002.07200))



[[!include application of holographic QCD to B-meson physics -- references]]


### Relation to holographic entanglement entropy

Relating to [[holographic entanglement entropy]]:

* Zhibin Li, Kun Xu, Mei Huang, _The entanglement properties of holographic QCD model with a critical end point_ ([arXiv:2002.08650](https://arxiv.org/abs/2002.08650))


### Application to defects

Application to QCD [[QFT with defects|with defects]]:

* Alexander Gorsky, Valentin Zakharov, Ariel Zhitnitsky, _On Classification of QCD defects via holography_, Phys. Rev. D79:106003, 2009 ([arxiv:0902.1842](https://arxiv.org/abs/0902.1842))



[[!redirects AdS-QCD correspondences]]

[[!redirects AdS/QCD correspondence]]

[[!redirects AdS-QCD]]
[[!redirects AdS/QCD]]

[[!redirects AdS-QCD duality]]
[[!redirects AdS-QCD dualities]]

[[!redirects Sakai-Sugimoto model]]
[[!redirects Sakai-Sugimoto models]]

[[!redirects Witten-Sakai-Sugimoto model]]
[[!redirects Witten-Sakai-Sugimoto models]]

[[!redirects Sakai-Sugimoto-Witten model]]
[[!redirects Sakai-Sugimoto-Witten models]]

[[!redirects WSS model]]
[[!redirects WSS models]]

[[!redirects holographic QCD]]
[[!redirects holographic quantum chromodynamics]]

[[!redirects improved holographic QCD]]
[[!redirects improved holographic quantum chromodynamics]]

[[!redirects Ads/QCD]]


