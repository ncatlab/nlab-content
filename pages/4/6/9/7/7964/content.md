
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fields and quanta
+-- {: .hide}
[[!include fields and quanta - table]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Higgs field_ or _[[Higgs boson]]_ is a [[scalar field|scalar]] [[physical field]]/[[fundamental particle]]  in a [[gauge theory]] such as the [[standard model of particle physics]] supposedly responsible for the [[spontaneously broken symmetry]] of the [[electroweak field]] ([[electroweak symmetry breaking]]) and for giving elementary particles their [[mass|masses]] by the _[[Higgs mechanism]]_. 

## Properties

### Mass and vacuum (in-)stability
 {#MassAndVacuumInstability}

The [[rest mass]] of the Higgs particle observed at the [[LHC]] [[experiment]] is about $125$ [[GeV]] ([ATLAS Collaboration 12](#ATLAS12), [CMS Collaboration 12](#CMS12), [ATLAS Collaboration 15](#ATLAS15), see [Gibbs 11a](#Gibbs11a) for early discussion).

This is determined by a [[local minimum]] of the Higgs [[potential energy|potential]] (see [Kusenko 15](#Kusenko15) for exposition):

<img src="https://ncatlab.org/nlab/files/HiggsPotentials.png" width="500">


Curiously, the Higgs [[potential energy|potential]] is such that the Higgs field at this mass is at least close to being at the border between [[vacuum stability]] and [[false vacuum]]. This was highlighted before the actual measurement ([EEGHR 09](#EEGHR09), [Gibbs 11b](#Gibbs11b)):

<img src="https://ncatlab.org/nlab/files/HiggsVacuumStabilityIII.png" width="700">

Then it was amplified again after the detection of the Higgs particle at the [[LHC]] ([DVEEGI 12](#DVEEGI12)):


<img src="https://ncatlab.org/nlab/files/HiggsVacuumStability.png" width="700">

More detailed computation at [[2-loop]] confirmed this result, showing that the observed Higgs vacuum is indeed very close to the boundary between the [[vacuum stability|stable]] and the meta-stable region ([BKPV 15](#BKPV15)):

<img src="https://ncatlab.org/nlab/files/HiggsVacuumStabilityII.png" width="400">

{#SeeAlsoAFS18} See also [AFS 18](#AFS18):

<img src="https://ncatlab.org/nlab/files/HiggsVacuumStability4.png" width="800">


In summary ([Kusenko 15](#Kusenko15)):

> $[$The$]$ conclusion is that the best theoretical fit to measured parameters, including the Higgs and top-quark masses, points to a metastable Universe. However, their analysis also concludes that values of parameters are closer to a region of absolute stability than suggested by previous studies: it is possible for the Universe to be fully stable (and for the standard model to work all the way up to the Planck scale), if the true values of measured parameters are only 1.3 standard deviations away from the current best estimates.

However [[quantum tunneling]]/[[vacuum decay]] is an intrinsically [[non-perturbative effect]] which needs careful treatment beyond [[perturbative quantum field theory]] (e.g. [AFFS 17](#AFFS17))

<center>
<img src="https://ncatlab.org/nlab/files/NonPerturbativeTunneling.jpg" width="600"/>
</center>

> graphics grabbed form [Schwartz 15, slide 44](#Schwartz15)



$\,$

### Cosmological instability?
 {#CosmologicalInstability}

However, it has been argued that an actual [[false vacuum]] of the Higgs is incompatible with [[cosmology]], as due to [[vacuum fluctuations]] during [[inflation]] the [[vacuum decay]] would not have been avoided ([EGR 07](#EGR07), [HKSZ 14](#HKSZ14), [EGMRSST 15](#EGMRSST15), [EKSYZ 16](#EKSYZ16)). In ([BDGGSSS 13, section 7](#BDGGSSS13), [Kane 18 , "Clue 4"](#Kane18)) it was argued that this suggests a further principle which prevents the vacuum instability and that a natural such principle is [[supersymmetry]]. (This argument has a long history, see [Gibbs 11b](#Gibbs11b)).


### Asymptotic safety?
 {#AsymtoticSafetyOrNot}

The near criticality of the Higgs field [[vacuum]] discussed [above](#MassAndVacuumInstability) implies that the [[coefficient]] $\lambda$ of the quartic part of the Higgs potential is close to zero after [[renormalization group flow]] ("RGE") to around the [[Planck scale]] of about $10^{19}$ [[GeV]] (e.g. [BDGGSSS 13, p. 17-18](#BDGGSSS13)):

<img src="https://ncatlab.org/nlab/files/HiggsQuarticCoupling.png" width="400"/>

In fact also the [[beta function]] $\beta_\lambda$ of the quartic coupling $\lambda$ (i.e. its logarithmic [[derivative]] with respect to [[scale]]) is close to zero around the [[Planck scale]] of about $10^{19}$ [[GeV]] ([BDGGSSS 13, p. 18](#BDGGSSS13)):

<img src="https://ncatlab.org/nlab/files/HiggsQuarticBetaFunctionRelative.png" width="400"/>


Earlier it has been suggested that this reflects the principle of [[asymptotic safety]] ([Shaposhnikov-Wetterich 09](#ShaposhnikovWetterich09)). But this would mean that not only $\lambda$ and its [[beta function|RGE-derivative]] $\beta_\lambda$ vanish around the [[Planck scale]], but that in fact all higher derivatives do, too (see e.g. [Niedermaier 06, equation (1.5)](asymptotic+safety#Niedermaier06)) hence that $\beta_\lambda$ asymptotes to zero. But this does not seem to be the case; in ([BDGGSSS 13, p. 17-18](#BDGGSSS13)) it says:

>  As shown in fig. 2 (upper right), the corresponding Higgs quartic [[beta-function]] vanishes at a [[scale]] of about $10^{17}$-$10^{18}$ [[GeV]]. In order to quantify the degree of cancellation in the β-function, we plot in fig. 2 (lower right) $\beta_\lambda$ in units of its pure [[top quark]] contribution.  The vanishing of $\beta_\lambda$ looks  more  like  an  accidental  cancellation  between  various  large  contributions, rather than an asymptotic approach to zero.


<img src="https://ncatlab.org/nlab/files/HiggsQuarticBetaFunction.png" width="800"/>




## Models

There is no lack of proposals for realizing the Higgs field in various big schemes of mathematical structures modelling physics. 

For instance

* in [[string theory]] (see _[[string phenomenology]]_) a Higgs mechanism can arise in a variety of ways. Notably in [[intersecting D-brane models]] it arises naturally from brane recombination at intersections: ([Cremades-Ibanez-Marchesano 02, section 7](#CremadesIbanezMarchesano02)):

<img src="https://ncatlab.org/nlab/files/BraneRecombination.png" width="600"/>


* in the [[technicolor]] model the Higgs field is not a fundamental particle but a compound of [[fermions]]. This realizes the Higgs effect entirely in ordinary [[gauge theory]]; 

* in [[noncommutative geometry]] it has been [shown](http://ncatlab.org/nlab/show/standard+model+of+particle+physics#NCGeometry) that the Higgs may be modeled as a component of the gauge bosons assuming that the [[Kaluza-Klein mechanism|KK-reduction]] is over a certain non-commutative space of classical dimension 0.

## History

The Higgs mechanism was proposed in 1963-1964 by a fair number of authors essentially simultaneously, see the [References](#References) below. The explicit prediction of the Higgs boson implied by this mechanism though seems to be solely due to ([Higgs 64](#Higgs64)).

The Higgs boson (or at least something very much like it) was finally detected in 2013 at the [[LHC]] [[experiment]].

So for the Higgs particle prediction and experimental detection lie apart by about 50 years. Compare maybe to the [[neutrino]], which was predicted in 1930 and detected in 1956, about 26 years later. 

## Related concepts

* [['t Hooft-Polyakov monopole]]

* [[phi^n interaction]]

* [[electroweak field]]

* [[inflaton field]]

* [[higgsino]]

* [[Higgs bundle]]

[[!include standard model of fundamental physics - table]]


## References
 {#References}


### General

The original articles explaining what is now called the Higgs mechanism by [[spontaneous symmetry breaking]] were

* P. Anderson, _Plasmons, gauge invariance and mass_, Physical Review 130: 439. (1963)

* [[François Englert]], [[Robert Brout]],  _Broken Symmetry and the Mass of Gauge Vector Mesons_, Physical Review Letters 13 (9): 321&#8211;23. (1964)

*  Gerald Guralnik, C. R. Hagen, ; T. W. B. Kibble, _Global Conservation Laws and Massless Particles_ Physical Review  (1964)

* {#Higgs64} [[Peter Higgs]], _Broken Symmetries and the Masses of Gauge Bosons_, Physical Review Letters 13 (16): 508&#8211;509. (1964)
  
While all these articles essentially describe the Higgs mechanism, apparently only the one by Peter Higgs explicitly points out that this mechanism predicts the existence of a new, then unobserved, boson, the one therefore now called the _Higgs boson_.

The general theory of [[spontaneous symmetry breaking]] is reviewed in

* Jeremy Bernstein, _Spontaneous symmetry breaking, gauge theories, the Higgs mechanism and all that_, Rev. Mod. Phys. 46, 7&#8211;48 (1974)  ([pdf](http://www.calstatela.edu/faculty/kaniol/p544/rmp46_p7_higgs_goldstone.pdf))

The [[phenomenology]] of Higgs [[model (in particle physics)|models]] is discussed in 

* Marcela Carena, Howard E. Haber, _Higgs Boson Theory and Phenomenology_, Prog.Part.Nucl.Phys.50:63-152,2003 ([arXiv:hep-ph/0208209](http://arxiv.org/abs/hep-ph/0208209))

### Detection

Early discussion of the detection of a Higgs field of 125 [[GeV]] at [[LHC]] is in

* {#Gibbs11a} [[Philip Gibbs]], _Seminar Watch (Higgs Special), Rumoured Higgs at 125 GeV and What Would a Higgs at 125 GeV Tell Us?_, Prespacetime Journal, December 2011, Vol. 2 Issue 12 pp. 1899-1905 ([web](http://prespacetime.com/index.php/pst/article/view/308/298))

The official announcement of the detection at [[LHC]] is due to

* {#ATLAS12} G. Aad et al. (ATLAS Collaboration), _Observation of a New Particle in the Search for the Standard Model Higgs Boson with the ATLAS Detector at the LHC,_ Phys. Lett. B 716, 1 (2012) ([arXiv:1207.7214](https://arxiv.org/abs/1207.7214))

* {#CMS12} S. Chatrchyan et al. (CMS Collaboration), _Observation of a New Boson at a Mass of 125 GeV with the CMS Experiment at the LHC_, 716, 30 (2012) ([arXiv:1207.7235](https://arxiv.org/abs/1207.7235))

* {#ATLAS15} G. Aad et al. (ATLAS Collaboration, CMS Collaboration), _Combined Measurement of the Higgs Boson Mass in $p p$ Collisions at $\sqrt{s} = 7$ and 8 TeV with the ATLAS and CMS Experiments_, Phys. Rev. Lett. 114, 191803 (2015) ([arXiv:1503.07589](https://arxiv.org/abs/1503.07589))

### Vacuum (in-)stability
 {#ReferencesVacuumInstability}

Before experimental observation of the Higgs mass at the [[LHC]], the three possible outcomes for [[vacuum stability]] were analyzed in 

* {#EEGHR09} [[John Ellis]], J.R. Espinosa, [[Gian Giudice]], A. Hoecker, A. Riotto, _The Probable Fate of the Standard Model_, Phys.Lett.B679:369-375,2009 ([arXiv:0906.0954](https://arxiv.org/abs/0906.0954))

* {#Gibbs11b} [[Philip Gibbs]], _[What would a Higgs at 125 GeV tell us?](https://vixra.wordpress.com/2011/12/04/what-would-a-higgs-at-125-gev-tell-us/)_, in _Seminar Watch (Higgs Special), Rumoured Higgs at 125 GeV and What Would a Higgs at 125 GeV Tell Us?_, Prespacetime Journal, December 2011, Vol. 2 Issue 12 pp. 1899-1905 ([web](http://prespacetime.com/index.php/pst/article/view/308/298))

More discussion of the near-criticality of the [[vacuum stability]] after the observation of the Higgs mass is due to

* {#DVEEGI12} Giuseppe Degrassi, Stefano Di Vita, Joan Elias-Miró, José R. Espinosa, [[Gian Giudice]], Gino Isidori, _Higgs mass and vacuum stability in the Standard Model at NNLO_, J. High Energ. Phys. (2012) 2012: 98 ([arrXiv:1205.6497](https://arxiv.org/abs/1205.6497), <a href="https://doi.org/10.1007/JHEP08(2012)098">doi:10.1007/JHEP08(2012)098</a>)

with a more precise analysis due to

* {#BKPV15} A. V. Bednyakov, B. A. Kniehl, A. F. Pikelner, and O. L. Veretin, _Stability of the Electroweak Vacuum: Gauge Independence and Advanced Precision_, Phys. Rev. Lett. 115, 201802 ([arXiv:1507.08833](https://arxiv.org/abs/1507.08833), [doi:10.1103/PhysRevLett.115.201802](https://doi.org/10.1103/PhysRevLett.115.201802))

Careful discussion of the stability issue under [[renormalization]] is in 

* Anders Andreassen, William Frost, Matthew D. Schwartz, _Consistent Use of the Standard Model Effective Potential_, Phys. Rev. Lett. 113, 241801 (2014) ([arXiv:1408.0292](https://arxiv.org/abs/1408.0292))

and with emphasis on [[non-perturbative effects]] in [[quantum tunneling]]/[[vacuum decay]] 

* {#AFFS17} Anders Andreassen, David Farhi, William Frost, Matthew D. Schwartz, _Precision decay rate calculations in quantum field theory_, Phys. Rev. D 95, 085011 (2017) ([arXiv:1604.06090](https://arxiv.org/abs/1604.06090))

Review includes

* {#Kusenko15} Alexander Kusenko, _[Are We on the Brink of the Higgs Abyss?](https://physics.aps.org/articles/v8/108)_, Physics 8, 108 (2015)

* Sebastian Baum, _On the metastability of the Standard Model_, 2015 ([pdf](https://uu.diva-portal.org/smash/get/diva2:819933/FULLTEXT01.pdf))

* Holger Gies, _Vacuum stability and the mass of the Higgs boson_, 2015 ([pdf](http://physik.uni-graz.at/~dk-user/talks/Gies_20150828.pdf))

* {#Schwartz15} Matthew Schwartz, _Do we know if our universe is stable?_, Rutgers Seminar 2015 ([pdf](https://www.physics.rutgers.edu/het/video/schwartz15a.pdf))

* {#Strumia17} [[Alessandro Strumia]], _Higgs and Vacuum (In)Stability_, talk at GGI 2017 ([pdf](https://indico.cern.ch/event/660870/contributions/2746200/attachments/1538374/2411246/2017-HiggsDecay.pdf))

* {#AFS18} Anders Andreassen, William Frost, Matthew D. Schwartz, _Scale Invariant Instantons and the Complete Lifetime of the Standard Model_, Phys. Rev. D 97, 056006 (2018) ([arXiv:1707.08124](https://arxiv.org/abs/1707.08124))


Speculation about what this near-criticality of the Higgs vacuum could be pointing to is in

* {#BDGGSSS13} Dario Buttazzo, Giuseppe Degrassi, Pier Paolo Giardino, [[Gian Giudice]], Filippo Sala, Alberto Salvio, [[Alessandro Strumia]], section 7 of _Investigating the near-criticality of the Higgs boson_, JHEP12(2013)089 ([arXiv:1307.3536](https://arxiv.org/abs/1307.3536))

as well as [Kane 17, "Clue 4"](#Kane17).

Arguments that a false Higgs vacuum is incompatible with [[cosmology|cosmological]] evolution ([[inflation]]) include the following:


* {#EGR07} J.R. Espinosa, [[Gian Giudice]], A. Riotto, _Cosmological implications of the Higgs mass measurement_, JCAP 0805:002, 2008 ([arXiv:0710.2484](https://arxiv.org/abs/0710.2484))


* {#HKSZ14} Anson Hook, John Kearney, Bibhushan Shakya, Kathryn M. Zurek, _Probable or Improbable Universe? Correlating Electroweak Vacuum Instability with the Scale of Inflation_, J. High Energ. Phys. (2015) 2015: 61 ([arXiv:1404.5953](https://arxiv.org/abs/1404.5953))

* {#EGMRSST15} Jose R. Espinosa, [[Gian Giudice]], Enrico Morgante, Antonio Riotto, Leonardo Senatore, [[Alessandro Strumia]], Nikolaos Tetradis, _The cosmological Higgstory of the vacuum instability_ ([arXiv:1505.04825](https://arxiv.org/abs/1505.04825))

* {#EKSYZ16} William E. East, John Kearney, Bibhushan Shakya, Hojin Yoo, Kathryn M. Zurek, _Spacetime Dynamics of a Higgs Vacuum Instability During Inflation_, Phys. Rev. D 95, 023526 (2017) ([arXiv:1607.00381](https://arxiv.org/abs/1607.00381))

The interpretation in terms of [[asymptotic safety]] is discussed in

* {#ShaposhnikovWetterich09} M. Shaposhnikov and C. Wetterich, _Asymptotic safety of gravity and the Higgs boson mass_, Phys. Lett. B 683 (2010) 196 ([arXiv:0912.0208](https://arxiv.org/abs/0912.0208))

### In string theory

Discussion of the Higgs field from [[intersecting D-brane models]] is due to

* {#CremadesIbanezMarchesano02} D. Cremades, [[Luis Ibáñez]], F. Marchesano, _Intersecting brane models of particle physics and the Higgs mechanism_, JHEP, 0207, 022 2002 ([arXiv:hep-th/0203160](https://arxiv.org/abs/hep-th/0203160))


Discussion of the Higgs mechanism in the [[G2-MSSM]] and related models is due to

* {#Kane11} [[Gordon Kane]], _String theory and generic predictions for our world &#8211; superpartner masses, LHC signatures, dark matter, EWSB, cosmological history of universe, etc_, talk at String phenomenology 2011, August 2011 ([pdf](http://conferencing.uwex.edu/conferences/stringpheno2011/documents/kane.pdf))

* [[Gordon Kane]], Piyush Kumar, Ran Lu, Bob Zheng, _Higgs Mass Prediction for Realistic String/M Theory Vacua_, Phys. Rev. D 85, 075026 ([arXiv:1112.1059](http://arxiv.org/abs/1112.1059))

  (a useful informed comment is [here](http://www.math.columbia.edu/~woit/wordpress/?p=4262&cpage=1#comment-101525))

and related to the issue of the [[vacuum stability]] in

* {#Kane18} [[Gordon Kane]], _Exciting Implications of LHC Higgs Boson Data_ ([arXiv:1802.05199](https://arxiv.org/abs/1802.05199))

which is based on

* {#Kane17} [[Gordon Kane]], _String theory and the real world_, Morgan & Claypool, 2017 (<a href="http://iopscience.iop.org/book/978-1-6817-4489-6">doi:0.1088/978-1-6817-4489-6</a>)



[[!redirects Higgs fields]]

[[!redirects Higgs mechanism]]

[[!redirects Higgs effect]]
[[!redirects Higgs effects]]


[[!redirects Higgs particle]]
[[!redirects Higgs particles]]

