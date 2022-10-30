

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[AdS-CFT correspondence]] applies _exactly_ only to a few highly symmetric [[quantum field theories]], notably to [[N=4 D=4 super Yang-Mills theory]]. However, away from these special points in field theory space the correspondence does not completely break down, but continues to apply in some approximation and/or with suitable modifications on the [[gravity]]-side of the correspondence.

Notably [[quantum chromodynamics]] (one sector of the [[standard model of particle physics]]) is crucially different from but still similar enough to [[N=4 D=4 super Yang-Mills theory]] that some of its [[observables]], in particular otherwise intractable [[non-perturbative effects]], have been argued to be usefully approximated by [[AdS-CFT]]-type [[duality in string theory|dual]] [[supergravity]]-[[observables]].

In particular, the realization of [[quantum chromodynamics]] by [[intersecting D-brane models]] gives a conceptual analytic handle on [[confinement|confined]] [[hadron]] spectra, hence of the physics of ordinary [[atomic nuclei]] (see [below](#Hadrons)), which is otherwise computable only via the blind numerics of [[lattice QCD]].

<center>
<img src="https://ncatlab.org/nlab/files/AdSCFTForQCD.jpg" width="600" />
</center>

> graphics grabbed from [Aoki-Hashimoto-Iizuka 12](#AHI12)

Other examples of such observables is the [[shear viscosity]] of the [[quark-gluon plasma]]. 

This approach is hence called the _AdS/QCD-correspondence_ or _holographic QCD_ or similar (see also [[AdS-CFT in condensed matter physics]] for similar relations).

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

This model realizes something close to [[QCD]] on [[intersecting D-brane models|coincident]] [[black brane|black]] [[M5-branes]] with [[near horizon geometry]] a [[KK-compactification]] of $AdS_7 \times S^4$ in the decoupling limit where the [[worldvolume]] theory becomes the [[6d (2,0)-superconformal SCFT]]. The [[KK-compactification]] is on a [[torus]] with anti-periodic boundary conditions for the [[fermions]] in one direction, thus [[spontaneous symmetry breaking|breaking]] all [[supersymmetry]]. Here the first circle [[KK-compactification|reduction]] realizes, under [[duality between M-theory and type IIA string theory]], the [[M5-branes]] as [[D4-branes]], hence the model now looks like 5d [[Yang-Mills theory]] further [[KK-compactification|compactified]] on a circle. ([Witten 98, section 4](#Witten98)). 

This already produces a pure [[Yang-Mills theory]] whose [[glueball]]-spectra  may usefully be compared to those of [[QCD]]:

<center>
<img src="https://ncatlab.org/nlab/files/GlueballSpectrumSSWModel.jpg" width="700">
</center>

> graphics grabbed from [Rebhan 14](#Rebhan14)

The further introduction of [[intersecting D-brane model|intersecting]] [[D8-branes]] and [[anti D-brane|anti]] [[D8-branes]] to [[D4-D8 brane bound states]] makes a sensible sector of [[chiral fermions]] appear in this model ([Sakai-Sugimoto 04](#SakaiSugimoto04), [Sakai-Sugimoto 05](#SakaiSugimoto05))

<center>
<img src="https://ncatlab.org/nlab/files/SakaiSugimotoModel.jpg" width="600">
</center>

> graphics grabbed from [Erlich 09, section 1.1](#Erlich09)


<center>
<img src="https://ncatlab.org/nlab/files/IntersectingBranesSSWModel.jpg" width="700">
</center>

> graphics grabbed from [Rebhan 14](#Rebhan14)

##### Hadrons
  {#Hadrons}


In this [[Witten-Sakai-Sugimoto model]] for [[non-perturbative effect|strongly coupled]] [[QCD]] the [[hadrons]] in [[QCD]] correspond to [[string theory|string-theoretic]]-phenomena in the [[bulk field theory]]:

1. the [[mesons]] ([[bound states]] of 2 [[quarks]]) correspond to [[open strings]] in the bulk, whose two endpoints on the [[asymptotic boundary]] correspond to the two quarks

1. [[baryons]] ([[bound states]] of $N_c$ [[quarks]]) appear in two different but equivalent ([Sugimoto 16, 15.4.1](#Sugimoto16)) guises:

   1. as [[wrapped brane|wrapped]] [[D4-branes]] with $N_c$ [[open strings]] connecting them to the [[D8-brane]]

      ([Witten 98b](#Witten98b), [Gross-Ooguri 98, Sec. 5](#GrossOoguri98), [BISY 98](#BISY98), [CGS98](#CGS98))

   1. as [[skyrmions]] 

      ([Sakai-Sugimoto 04, section 5.2](#SakaiSugimoto04), [Sakai-Sugimoto 05, section 3.3](#SakaiSugimoto05), see [Bartolini 17](#Bartolini17)). 

For review see [Sugimoto 16](#Sugimoto16), also [Rebhan 14, around (18)](#Rebhan14).

<center>
<img src="https://ncatlab.org/nlab/files/BaryonsAsD4Branes.jpg" width="700">
</center>

> graphics grabbed from [Sugimoto 16](#Sugimoto16)

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



## Related concepts

* [[holographic entanglement entropy]]

* [[AdS-CFT in condensed matter physics]]

* [[lattice QCD]]


## References

### General

Review:

* {#Aharony02} [[Ofer Aharony]], _The non-AdS/non-CFT correspondence, or three different paths to QCD_, Progress in string, field and particle theory. Springer, Dordrecht, 2003. 3-24 ([arXiv:hep-th/0212193](https://xxx.lanl.gov/abs/hep-th/0212193))

* {#Erlich09} Joshua Erlich, _How Well Does AdS/QCD Describe QCD?_,  	Int. J. Mod. Phys.A25:411-421,2010 ([arXiv:0908.0312](https://arxiv.org/abs/0908.0312))

* M. R. Pahlavani, R. Morad, _Application of AdS/CFT in Nuclear Physics_, Advances in High Energy Physics ([arXiv:1403.2501](https://arxiv.org/abs/1403.2501))

* Jorge Casalderrey-Solana, Hong Liu, David Mateos, Krishna Rajagopal, Urs Achim Wiedemann,

  _Gauge/string duality, hot QCD and heavy ion collisions_, 

  Cambridge University Press, 2014 ([arXiv:1101.0618](https://arxiv.org/abs/1101.0618))

* {#AHI12} Sinya Aoki, [[Koji Hashimoto]], Norihiro Iizuka, _Matrix Theory for Baryons: An Overview of Holographic QCD for Nuclear Physics_, Reports on Progress in Physics, Volume 76, Number 10 ([arxiv:1203.5386](https://arxiv.org/abs/1203.5386))



* Youngman Kim, Ik Jae Shin, Takuya Tsukioka, _Holographic QCD: Past, Present, and Future_, Progress in Particle and Nuclear Physics
Volume 68, January 2013, Pages 55-112 Progress in Particle and Nuclear Physics ([arXiv:1205.4852](https://arxiv.org/abs/1205.4852))

* Joshua Erlich, _An Introduction to Holographic QCD for Nonspecialists_,  Contemporary Physics ([arXiv:1407.5002](https://arxiv.org/abs/1407.5002))

* {#Guijosa16} Alberto Guijosa, _QCD, with Strings Attached_, IJMPE Vol. 25, No. 10 (2016) 1630006 ([arXiv:1611.07472](https://arxiv.org/abs/1611.07472))

* {#ZhouDosch18} Liping Zou, H.G. Dosch, _A very Practical Guide to Light Front Holographic QCD_, ([arXiv:1801.00607](https://arxiv.org/abs/1801.00607))

The top-down Sakai-Sugimoto model is due to 

* {#SakaiSugimoto04} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _Low energy hadron physics in holographic QCD_, Prog.Theor.Phys.113:843-882, 2005 ([arXiv:hep-th/0412141](https://arxiv.org/abs/hep-th/0412141))

* {#SakaiSugimoto05} [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _More on a holographic dual of QCD_, Prog.Theor.Phys.114:1083-1118, 2005 ([arXiv:hep-th/0507073](https://arxiv.org/abs/hep-th/0507073))

based on 

* {#Witten98} [[Edward Witten]], _Anti-de Sitter Space, Thermal Phase Transition, And Confinement In Gauge Theories_, Adv. Theor. Math. Phys.2:505-532, 1998 ([arXiv:hep-th/9803131](https://arxiv.org/abs/hep-th/9803131))

further developed in 

* {#Bartolini17} Lorenzo Bartolini, Stefano Bolognesi, Andrea Proto, _From the Sakai-Sugimoto Model to the Generalized Skyrme Model_, Phys. Rev. D 97, 014024 2018 ([arXiv:1711.03873](https://arxiv.org/abs/1711.03873))

reviewed in 

* {#Rebhan14} Anton Rebhan, _The Witten-Sakai-Sugimoto model: A brief review and some recent results_, 3rd International Conference on New Frontiers in Physics, Kolymbari, Crete, 2014 ([arXiv:1410.8858](https://arxiv.org/abs/1410.8858))

The Sakai-Sugimoto model at [[O-planes]]: 

* {#ImotoSakaiSugimoto09} Toshiya Imoto, [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], _$O(N)$ and $USp(N)$ QCD from String Theory_, Prog.Theor.Phys.122:1433-1453, 2010 ([arXiv:0907.2968](https://arxiv.org/abs/0907.2968))

* Hee-Cheol Kim, Sung-Soo Kim, Kimyeong Lee, _5-dim Superconformal Index with Enhanced En Global Symmetry_, JHEP 1210 (2012) 142 ([arXiv:1206.6781](https://arxiv.org/abs/1206.6781))

The bottom-up hard-wall model is due to

* {#ErlichKatzSonStephanov05} Joshua Erlich, Emanuel Katz, Dam T. Son, Mikhail A. Stephanov, _QCD and a Holographic Model of Hadrons_, Phys.Rev.Lett.95:261602, 2005 ([arXiv:hep-ph/0501128](https://arxiv.org/abs/hep-ph/0501128))

while the soft-wall refinement is due to 

* {#KKSS06} [[Andreas Karch]], Emanuel Katz, Dam T. Son, Mikhail A. Stephanov, _Linear Confinement and AdS/QCD_, Phys.Rev.D74:015005, 2006 ([arXiv:hep-ph/0602229](https://arxiv.org/abs/hep-ph/0602229))

see also

* Alfredo Vega, Paulina Cabrera, _Family of dilatons and metrics for AdS/QCD models_, Phys. Rev. D 93, 114026 (2016) ([arXiv:1601.05999](https://arxiv.org/abs/1601.05999))

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

The light-front holography approach is 

reviewed in [Zhou-Dosch 18](#ZhouDosch18)

Discussion of [[phase transition]]:

* Varun Sethi, _A study of phases in two flavour holographic QCD_  ([arXiv:1906.10932](https://arxiv.org/abs/1906.10932))


* Wikipedia, _[AdS/QCD correspondence](https://en.wikipedia.org/wiki/AdS/QCD_correspondence)_ 


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


#### Baryons as instantons

[[baryons]] as [[instantons]]:

* {#KatzLewandowskiSchwartz05} Emanuel Katz, Adam Lewandowski, Matthew D. Schwartz, Phys. Rev. D74:086004, 2006 ([arXiv:hep-ph/0510388](https://arxiv.org/abs/hep-ph/0510388))

* {#HSSY07} Hiroyuki Hata, [[Tadakatsu Sakai]], [[Shigeki Sugimoto]], Shinichiro Yamato, _Baryons from instantons in holographic QCD_, Prog.Theor.Phys.117:1157, 2007 ([arXiv:hep-th/0701280](https://arxiv.org/abs/hep-th/0701280))



* Salvatore Baldino, Stefano Bolognesi, Sven Bjarke Gudnason, Deniz Koksal, _A Solitonic Approach to Holographic Nuclear Physics_, Phys. Rev. D 96, 034008 (2017) ([arXiv:1703.08695](https://arxiv.org/abs/1703.08695))

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

* Yosuke Imamura, _Baryon Mass and Phase Transitions in Large N Gauge Theory_, Prog. Theor. Phys. 100 (1998) 1263-1272 ([arxiv:hep-th/9806162](https://arxiv.org/abs/hep-th/9806162))

* Yosuke Imamura, _Supersymmetries and BPS Configurations on Anti-de Sitter Space_, Nucl. Phys. B537:184-202,1999 ([arxiv:hep-th/9807179](https://arxiv.org/abs/hep-th/9807179))


* {#CGS98} Curtis G. Callan, Alberto Guijosa, Konstantin G. Savvidy, _Baryons and String Creation from the Fivebrane Worldvolume Action_ ([arxiv:hep-th/9810092](https://arxiv.org/abs/hep-th/9810092))


* Curtis G. Callan, Alberto Guijosa, Konstantin G. Savvidy, Oyvind Tafjord, _Baryons and Flux Tubes in Confining Gauge Theories from Brane Actions_, Nucl. Phys. B555 (1999) 183-200 ([arxiv:hep-th/9902197](https://arxiv.org/abs/hep-th/9902197))

Review:

* P. Yi, _Two Approaches to Holographic Baryons/Nuclei_, Few-Body Syst (2013) 54: 77. ([doi:10.1007/s00601-012-0373-7](https://doi.org/10.1007/s00601-012-0373-7))


#### Baryons as Skyrmions
 {#ReferencesBaryonsSkyrmions}

[[baryons]] as [[Skyrmions]]:

Review:

* {#Sugimoto16} [[Shigeki Sugimoto]], _Skyrmion and String theory_, chapter 15 in M. Rho, Ismail Zahed (eds.) _The Multifaceted Skyrmion_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

Original articles



* Kanabu Nawa, Hideo Suganuma, Toru Kojo, _Brane-induced Skyrmions: Baryons in Holographic QCD_, Prog.Theor.Phys.Suppl.168:231-236, 2007 ([arXiv:hep-th/0701007](https://arxiv.org/abs/hep-th/0701007))



* Hovhannes R. Grigoryan, _Baryon as skyrmion-like soliton from the
holographic dual model of QCD_, talk at _[From Strings to Things 2008](http://www.int.washington.edu/PROGRAMS/08-1.html)_ ([pdf](https://www.jlab.org/div_dept/theory/talks/2008/grigoryan08_INT.pdf))

* Paul Sutcliffe, _Skyrmions, instantons and holography_, JHEP 1008:019, 2010 ([arXiv:1003.0023](https://arxiv.org/abs/1003.0023)) 

* Paul Sutcliffe, _Holographic Skyrmions_, Mod.Phys.Lett. B29 (2015) no.16, 1540051 ([spire:1383608](http://inspirehep.net/record/1383608))

* Stefano Bolognesi, Paul Sutcliffe, _The Sakai-Sugimoto soliton_, JHEP 1401:078, 2014 ([arXiv:1309.1396](https://arxiv.org/abs/1309.1396))




#### Pentaquarks

[[pentaquarks]]:

* Kazuo Ghoroku, Akihiro Nakamura, Tomoki Taminato, Fumihiko Toyoda, _Holographic Penta and Hepta Quark State in Confining Gauge Theories_,
JHEP 1008:007,2010 ([arxiv:1003.3698](https://arxiv.org/abs/1003.3698))


### Glueball physics

* {#Suzuki01} Kenji Suzuki, _D0-D4 system and $QCD_{3+1}$_, Phys.Rev. D63 (2001) 084011 ([arXiv:hep-th/0001057](https://arxiv.org/abs/hep-th/0001057))

* S.S. Afonin, A.D. Katanaeva, _Glueballs and deconfinement temperature in AdS/QCD_ ([arXiv:1809.07730](https://arxiv.org/abs/1809.07730))



### Application to the quark-gluon plasma

Application to the [[quark-gluon plasma]]:

Expositions and reviews include

* Pavel Kovtun, _Quark-Gluon Plasma and String Theory_, RHIC news (2009) ([blog entry](http://www.bnl.gov/rhic/news/091107/story2.asp))

* Makoto Natsuume, _String theory and quark-gluon plasma_ ([arXiv:hep-ph/0701201](http://arxiv.org/abs/hep-ph/0701201))

* [[Steven Gubser]], _Using string theory to study the quark-gluon plasma: progress and perils_ ([arXiv:0907.4808](http://arxiv.org/abs/0907.4808))

* {#BiagazziCotrone12} Francesco Biagazzi, A. Cotrone, _Holography and the quark-gluon plasma_, AIP Conference Proceedings 1492, 307 (2012) ([doi:10.1063/1.4763537]( https://doi.org/10.1063/1.4763537), [slides pdf](http://cp3-origins.dk/content/movies/2013-01-14-bigazzi.pdf))

* {#Brambilla14} Brambilla et al., section 9.2.2 of _QCD and strongly coupled gauge theories: challenges and perspectives_, Eur Phys J C Part Fields. 2014; 74(10): 2981 ([doi:10.1140/epjc/s10052-014-2981-5](https://link.springer.com/article/10.1140%2Fepjc%2Fs10052-014-2981-5))


Holographic discussion of the [[shear viscosity]] of the quark-gluon plasma goes back to

* {#PolicastroSonStarinets01} [[Giuseppe Policastro]], D.T. Son, A.O. Starinets, _Shear viscosity of strongly coupled $N=4$ supersymmetric Yang-Mills plasma_, Phys. Rev. Lett.87:081601, 2001 ([arXiv:hep-th/0104066](http://arxiv.org/abs/hep-th/0104066))


Other original articles include:

* Hovhannes R. Grigoryan, Paul M. Hohler, Mikhail A. Stephanov, _Towards the Gravity Dual of Quarkonium in the Strongly Coupled QCD Plasma_ ([arXiv:1003.1138](http://arxiv.org/abs/1003.1138))

* Brett McInnes, _Holography of the Quark Matter Triple Point_ ([arXiv:0910.4456](http://arxiv.org/abs/0910.4456))

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


### Application to QCD phases
 {#ReferencesColourSuperconductivity}

Application to [[phase of matter|phases]] of QCD


to [[colour superconductivity]]:

* Kazem Bitaghsir Fadafan, Jesus Cruz Rojas, Nick Evans, _A Holographic Description of Colour Superconductivity_ ([arXiv:1803.03107](https://arxiv.org/abs/1803.03107))

to [[confinement]]/[[quark-gluon plasma|deconfinement]] phase transiton:

* {#LYY18} Meng-Wei Li, Yi Yang, Pei-Hung Yuan  _Imprints of Early Universe on Gravitational Waves from First-Order Phase Transition in QCD_ ([arXiv:1812.09676](https://arxiv.org/abs/1812.09676))

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



