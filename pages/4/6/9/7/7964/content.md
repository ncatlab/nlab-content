
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

The [[rest mass]] of the Higgs particle observed at the [[LHC]] [[experiment]] is about $125$ [[GeV]] ([ATLAS Collaboration 12](#ATLAS12), [CMS Collaboration 12](#CMS12), [ATLAS Collaboration 15](#ATLAS15), see [Gibbs 11a](#Gibbs11a), [HLL 11](#HLL11) for early discussion).

This is determined by a [[local minimum]] of the Higgs [[potential energy|potential]] (see [Kusenko 15](#Kusenko15) for exposition):

\begin{imagefromfile}
  "file_name": "HiggsPotentials.png",
  "width": 500
\end{imagefromfile}


{#Curiously} Curiously, the Higgs [[potential energy|potential]] is such that the Higgs field at this mass is at least close to being at the border between [[vacuum stability]] and [[false vacuum]]. This was highlighted before the actual measurement ([EEGHR 09](#EEGHR09), [Gibbs 11b](#Gibbs11b)): 

\begin{imagefromfile}
  "file_name": "HiggsVacuumStabilityIII.png",
  "width": 700
\end{imagefromfile}

Then it was amplified again after the detection of the Higgs particle at the [[LHC]] ([DVEEGI 12](#DVEEGI12)):

\begin{imagefromfile}
  "file_name": "HiggsVacuumStability.png",
  "width": 700
\end{imagefromfile}

More detailed computation at [[2-loop]] confirmed this result, showing that the observed Higgs vacuum is indeed very close to the boundary between the [[vacuum stability|stable]] and the meta-stable region ([BKPV 15](#BKPV15)):

\begin{imagefromfile}
  "file_name": "HiggsVacuumStabilityII.png",
  "width": 400
\end{imagefromfile}

{#SeeAlsoAFS18} See also [AFS 18](#AFS18):

\begin{imagefromfile}
  "file_name": "HiggsVacuumStability4.png",
  "width": 800
\end{imagefromfile}

In summary ([Kusenko 15](#Kusenko15)):

> $[$The$]$ conclusion is that the best theoretical fit to measured parameters, including the Higgs and top-quark masses, points to a metastable Universe. However, their analysis also concludes that values of parameters are closer to a region of absolute stability than suggested by previous studies: it is possible for the Universe to be fully stable (and for the standard model to work all the way up to the Planck scale), if the true values of measured parameters are only 1.3 standard deviations away from the current best estimates.

And more recently ([PDG 18, p. 9](#PDG18)):

> {#PDG18OnVacuumMetastability} However, for the value of Higgs mass experimentally measured, the EW vacuum of the Higgs potential is most likely metastable. Indeed, the high energy evolution of $\lambda$ shows that it becomes [[negative number|negative]] at [[energies]] $\Lambda = \mathcal{O}(10^{10}-10^{12})$ [[GeV]], with a broader range if the [[top quark]] [[mass]] exceeds its current measured value by [[statistical significance|3σ]]. When this occurs, the [[standard model of particle physics|SM]] Higgs potential develops an instability and the long term existence of the [[electroweak symmetry breaking|EW]] [[vacuum]] is challenged. This behavior may call for new physics at an intermediate scale before the instability develops, i.e., below [[Planck mass|M_Planck]], otherwise, the electroweak vacuum remains metastable.

> 


However [[quantum tunneling]]/[[vacuum decay]] is an intrinsically [[non-perturbative effect]] which needs careful treatment beyond [[perturbative quantum field theory]] (e.g. [AFFS 17](#AFFS17))

\begin{centre}
  \begin{imagefromfile}
    "file_name": "NonPerturbativeTunneling.jpg",
    "width": 600
  \end{imagefromfile}
\end{centre}

> graphics grabbed form [Schwartz 15, slide 44](#Schwartz15)

\linebreak


### Possible causes of the near criticality
 {#PossibleCausesOfNEarCriticality}

Given, by the [above](#MassAndVacuumInstability) discussion, that the parameters of the Higgs field are observed to be inside a special reason of their potential parameter space, it is natural to speculate that there is some mechanism that enforces or at least prefers this position.

In [BDGGSSS 13, Section 5.2](#BDGGSSS13) is speculation that for dynamics over a [[landscape of string theory vacua|landscape of vacua]] critical points may generally serve as attractors.

More specifically, [Isidori-Pattori 17](#IsidoriPattori17) claims that, under reasonable assumptions (including [[gauge coupling unification]], but excluding "[[naturalness]]") [[supersymmetry|supersymmetric]]-extensions of the [[standard model of particle physics]] ([[MSSM]]) predict a parameter range for the [[top quark]] and Higgs field [[mass]] that is close to coinciding with the corresponding parameter space for Higgs field near criticality:


\begin{center}
\begin{imagefromfile}
  "file_name": "IsidoriPattoriViable.jpg",
  "width": 600
\end{imagefromfile}
\end{center}


> graphics grabbed from [Isidori-Pattori 17](#IsidoriPattori17)

That [[supersymmetry]], possibly in a [[G2-MSSM]], would be a natural mechanism behind the near criticality of the Higgs field was also claimed in [Kane 18, "Clue 4"](#Kane18).



### Cosmological instability?
 {#CosmologicalInstability}

However, it has been argued that an actual [[false vacuum]] of the Higgs is incompatible with [[cosmology]], as due to [[vacuum fluctuations]] during [[inflation]] the [[vacuum decay]] would not have been avoided ([EGR 07](#EGR07), [HKSZ 14](#HKSZ14), [EGMRSST 15](#EGMRSST15), [EKSYZ 16](#EKSYZ16)). In ([BDGGSSS 13, section 7](#BDGGSSS13), [Kane 18 , "Clue 4"](#Kane18)) it was argued that this suggests a further principle which prevents the vacuum instability and that a natural such principle is [[supersymmetry]]. (This argument has a long history, see [Gibbs 11b](#Gibbs11b)).


### Asymptotic safety?
 {#AsymtoticSafetyOrNot}

The near criticality of the Higgs field [[vacuum]] discussed [above](#MassAndVacuumInstability) implies that the [[coefficient]] $\lambda$ of the quartic part of the Higgs potential is close to zero after [[renormalization group flow]] ("RGE") to around the [[Planck scale]] of about $10^{19}$ [[GeV]] (e.g. [BDGGSSS 13, p. 17-18](#BDGGSSS13)):

\begin{imagefromfile}
  "file_name": "HiggsQuarticCoupling.png",
  "width": 400
\end{imagefromfile}

In fact also the [[beta function]] $\beta_\lambda$ of the quartic coupling $\lambda$ (i.e. its logarithmic [[derivative]] with respect to [[scale]]) is close to zero around the [[Planck scale]] of about $10^{19}$ [[GeV]] ([BDGGSSS 13, p. 18](#BDGGSSS13)):

\begin{imagefromfile}
  "file_name": "HiggsQuarticBetaFunctionRelative.png",
  "width": 400
\end{imagefromfile}

Earlier it has been suggested that this reflects the principle of [[asymptotic safety]] ([Shaposhnikov-Wetterich 09](#ShaposhnikovWetterich09)). But this would mean that not only $\lambda$ and its [[beta function|RGE-derivative]] $\beta_\lambda$ vanish around the [[Planck scale]], but that in fact all higher derivatives do, too (see e.g. [Niedermaier 06, equation (1.5)](asymptotic+safety#Niedermaier06)) hence that $\beta_\lambda$ asymptotes to zero. But this does not seem to be the case; in ([BDGGSSS 13, p. 17-18](#BDGGSSS13)) it says:

>  As shown in fig. 2 (upper right), the corresponding Higgs quartic [[beta-function]] vanishes at a [[scale]] of about $10^{17}$-$10^{18}$ [[GeV]]. In order to quantify the degree of cancellation in the β-function, we plot in fig. 2 (lower right) $\beta_\lambda$ in units of its pure [[top quark]] contribution.  The vanishing of $\beta_\lambda$ looks  more  like  an  accidental  cancellation  between  various  large  contributions, rather than an asymptotic approach to zero.

\begin{imagefromfile}
  "file_name": "HiggsQuarticBetaFunction.png",
  "width": 800
\end{imagefromfile}


### Higgs inflation?
 {#HiggsInflation}

Starting with [Jegerlehner 13](cosmic+inflation#Jegerlehner13) has been argued that the near-criticality of the Higgs potential is in fact consistent or even necessary for [[Higgs inflation]] to be a viable model. See [Jegerlehner 18](cosmic+inflation#Jegerlehner18).



## Models

There is no lack of proposals for realizing the Higgs field in various big schemes of mathematical structures modelling physics. 

### Gauge-Higgs unification

A mechanis, of _gauge-Higgs unification_ ([Manton 79](#Manton79), [Hosotani 83](#Hosotani83)) also known as the _Hosotani mechanism_ (see [Hosotani 12](#Hosotani12)) refers to hypothetical [[model (in theoretical physics)|models]] of [[particle physics]] where the [[Higgs field]] on 4d [[spacetimes]] arises as a component of a [[gauge field]] in higher dimensions, either after [[Kaluza-Klein compactification]] or by passage to a 4d [[asymptotic boundary]] in a [[Randall-Sundrum model]] or similar.


<center>
<img src="https://ncatlab.org/nlab/files/GaugeHiggsUnification.jpg" width="500">
</center>

> graphics grabbed from [Lim 09](#Lim09)

Gauge-Higgs unification is naturally combined with [[GUT|grand unification]] of gauge groups, whence one then also speaks of _gauge-Higgs grand unification_ (e.g. [Hosotani-Yamatsu 15](#HosotaniYamatsu15))

Also the [[Connes-Lott models]] realize gauge-Higgs unification, in a [[non-commutative geometry|non-commutative geometric]] [[KK-compactification]].


### In string theory

In [[string theory]] (see _[[string phenomenology]]_) a Higgs mechanism can arise in a variety of ways. 

#### In intersecting D-brane models

Notably in [[intersecting D-brane models]] it arises naturally from brane recombination at intersections: ([Cremades-Ibanez-Marchesano 02, section 7](#CremadesIbanezMarchesano02)):

\begin{imagefromfile}
  "file_name": "BraneRecombination.png",
  "width": 600
\end{imagefromfile}

Further developments in [Ibanez-Marchesano-Rabadan 01](#IbanezMarchesanoRabadan01), [Hebecker-Knochel-Weigand 13](#HebeckerKnochelWeigand13) and specifically via [[string field theory]] in [HINSS 18](#HINSS18).

For review see [Ibanez-Uranga 12, fig 10.2](intersecting+D-brane+model#IbanezUranga12):

#### In $G_2$-MSSM

Discussion of the Higgs mechanism in the [[G2-MSSM]]: [Kane 11](#Kane11), [Kane-Kumar-Lu-Zheng 11](#KaneKumarLuZheng11), for review see [Kane 17](#Kane17), [Kane 18](#Kane18)

### Other

* in the [[technicolor]] model the Higgs field is not a fundamental particle but a compound of [[fermions]]. This realizes the Higgs effect entirely in ordinary [[gauge theory]]; 

* in [[Connes-Lott-Chamseddine-Barrett models]] it has been [shown](standard+model+of+particle+physics#NCGeometry) that the Higgs may be modeled as a component of the gauge bosons assuming that the [[Kaluza-Klein mechanism|KK-reduction]] is over a certain non-commutative space of classical dimension 0.

## History

The Higgs mechanism was proposed in 1963-1964 by a fair number of authors essentially simultaneously, see the [References](#References) below. The explicit prediction of the Higgs boson implied by this mechanism though seems to be solely due to ([Higgs 64](#Higgs64)).

The Higgs boson (or at least something very much like it) was finally detected in 2013 at the [[LHC]] [[experiment]].

So for the Higgs particle prediction and experimental detection lie apart by about 50 years. Compare maybe to the [[neutrino]], which was predicted in 1930 and detected in 1956, about 26 years later. 

## Related concepts

* [[gauge-Higgs unification]]

* [[massive Yang-Mills theory]]

* [['t Hooft-Polyakov monopole]]

* [[phi^n interaction]]

* [[electroweak field]]

* [[inflaton field]]

* [[composite Higgs model]]

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

Review includes

* {#PDG18} Particle Data Group [Review of particle physics](http://pdg.lbl.gov/), _Status of Higgs Boson Physics_, 2018 ([pdf](http://pdg.lbl.gov/2018/reviews/rpp2018-rev-higgs-boson.pdf), [[StatusOfHiggsBosonPhysics2018.pdf:file]])

* [[Antonio Pich]], _Electroweak Symmetry Breaking and the Higgs Boson_, [Acta Phys. Pol. B 47, 151](https://www.actaphys.uj.edu.pl/index_n.php?I=R&V=47&N=1#151) (2016) ([arXiv:1512.08749](https://arxiv.org/abs/1512.08749))

* Sally Dawson, Christoph Englert, Tilman Plehn, _Higgs Physics: It ain't over till it's over_, Physics Reports ([arXiv:1808.01324](https://arxiv.org/abs/1808.01324))

The general theory of [[spontaneous symmetry breaking]] is reviewed in

* Jeremy Bernstein, _Spontaneous symmetry breaking, gauge theories, the Higgs mechanism and all that_, Rev. Mod. Phys. 46, 7&#8211;48 (1974)  ([pdf](http://www.calstatela.edu/faculty/kaniol/p544/rmp46_p7_higgs_goldstone.pdf))

The [[phenomenology]] of Higgs [[model (in particle physics)|models]] is discussed in 

* Marcela Carena, Howard E. Haber, _Higgs Boson Theory and Phenomenology_, Prog.Part.Nucl.Phys.50:63-152,2003 ([arXiv:hep-ph/0208209](http://arxiv.org/abs/hep-ph/0208209))

### Detection

Early discussion of the detection of a Higgs field of 125 [[GeV]] at [[LHC]] is in

* {#Gibbs11a} [[Philip Gibbs]], _Seminar Watch (Higgs Special), Rumoured Higgs at 125 GeV and What Would a Higgs at 125 GeV Tell Us?_, Prespacetime Journal, December 2011, Vol. 2 Issue 12 pp. 1899-1905 ([web](http://prespacetime.com/index.php/pst/article/view/308/298))

* {#HLL11} Martin Holthausen, Kher Sham Lim, Manfred Lindner, _Planck Scale Boundary Conditions and the Higgs Mass_, JHEP 1202 (2012) 037 ([arXiv:1112.2415](https://arxiv.org/abs/1112.2415))

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

* {#DVEEGI12} Giuseppe Degrassi, Stefano Di Vita, Joan Elias-Miró, José R. Espinosa, [[Gian Giudice]], Gino Isidori, _Higgs mass and vacuum stability in the Standard Model at NNLO_, J. High Energ. Phys. (2012) 2012: 98 ([arrXiv:1205.6497](https://arxiv.org/abs/1205.6497), [doi:10.1007/JHEP&lpar;2012&rpar;098](https://doi.org/10.1007/JHEP08%282012%29098))

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


Speculation about what this near-criticality of the Higgs vacuum could be pointing to:

attractor mechanism in a [[landscape of string theory vacua|landscape of vacua]]:

* {#BDGGSSS13} Dario Buttazzo, Giuseppe Degrassi, Pier Paolo Giardino, [[Gian Giudice]], Filippo Sala, Alberto Salvio, [[Alessandro Strumia]], section 7 of _Investigating the near-criticality of the Higgs boson_, JHEP12(2013)089 ([arXiv:1307.3536](https://arxiv.org/abs/1307.3536))

an [[supersymmetry|supersymmetric]]-extension of the [[standard model of particle physics]] (e.g. [[MSSM]], [[G2-MSSM]], ...)

* {#IsidoriPattori17} Gino Isidori, Andrea Pattori, _On the tuning in the $(m_h, m_t)$ plane: Standard Model criticality vs. High-scale SUSY_, Physics Letters B Volume 782, 10 July 2018, Pages 551-558 ([arXiv:1710.11060](https://arxiv.org/abs/1710.11060))

as well as [Kane 18, "Clue 4"](#Kane18)

and more generally in view of [[split supersymmetry]]:

* {#GiudiceStrumia11} [[Gian Giudice]], [[Alessandro Strumia]], _Probing High-Scale and Split Supersymmetry with Higgs Mass Measurements_, Nuclear Physics B Volume 858, Issue 1, 1 May 2012, Pages 63-83 ([arXiv:1108.6077](https://arxiv.org/abs/1108.6077))

Arguments that a false Higgs vacuum is incompatible with [[cosmology|cosmological]] evolution ([[inflation]]) include the following:


* {#EGR07} J.R. Espinosa, [[Gian Giudice]], A. Riotto, _Cosmological implications of the Higgs mass measurement_, JCAP 0805:002, 2008 ([arXiv:0710.2484](https://arxiv.org/abs/0710.2484))


* {#HKSZ14} Anson Hook, John Kearney, Bibhushan Shakya, Kathryn M. Zurek, _Probable or Improbable Universe? Correlating Electroweak Vacuum Instability with the Scale of Inflation_, J. High Energ. Phys. (2015) 2015: 61 ([arXiv:1404.5953](https://arxiv.org/abs/1404.5953))

* {#EGMRSST15} Jose R. Espinosa, [[Gian Giudice]], Enrico Morgante, Antonio Riotto, Leonardo Senatore, [[Alessandro Strumia]], Nikolaos Tetradis, _The cosmological Higgstory of the vacuum instability_ ([arXiv:1505.04825](https://arxiv.org/abs/1505.04825))

* {#EKSYZ16} William E. East, John Kearney, Bibhushan Shakya, Hojin Yoo, Kathryn M. Zurek, _Spacetime Dynamics of a Higgs Vacuum Instability During Inflation_, Phys. Rev. D 95, 023526 (2017) ([arXiv:1607.00381](https://arxiv.org/abs/1607.00381))

But see 

* Mark P. Hertzberg, Mudit Jain, _Explanation for why the Early Universe was Stable and Dominated by the Standard Model_, JCAP 2020 ([arXiv:1911.04648](https://arxiv.org/abs/1911.04648))

for a possible solution by strong [[interaction]] between the Higgs field and the [[inflaton]].


The interpretation in terms of [[asymptotic safety]] is discussed in

* {#ShaposhnikovWetterich09} M. Shaposhnikov and C. Wetterich, _Asymptotic safety of gravity and the Higgs boson mass_, Phys. Lett. B 683 (2010) 196 ([arXiv:0912.0208](https://arxiv.org/abs/0912.0208))

### Diphoton decay

On [[renormalization]] of the [[Higgs field]]'s diphoton decay using [[causal perturbation theory]]:

* [[Pawel Duch]], [[Michael Duetsch]], [[Jose Gracia-Bondia]], _Diphoton decay of the higgs from the Epstein--Glaser viewpoint_ ([arXiv:2011.12675](https://arxiv.org/abs/2011.12675))



### Gauge-Higgs unification

Discussion of [[gauge-Higgs unification]]:

The mechanism is due to 

* {#Manton79} [[Nicholas Manton]], _A new six-dimensional approach to the Weinberg-Salam model_, Nuclear Physics B Volume 158, Issue 1, 8 October 1979, Pages 141-153 (<a href="https://doi.org/10.1016/0550-3213(79)90192-5">doi:10.1016/0550-3213(79)90192-5</a>)

* {#Hosotani83} [[Yutaka Hosotani]], _Dynamical Mass Generation by Compact Extra Dimensions_, Phys. Lett. 126B (1983) 309-313 ([spire:188768](http://inspirehep.net/record/188768), <a href="https://doi.org/10.1016/0370-2693(83)90170-3">doi:10.1016/0370-2693(83)90170-3</a>)

* {#Hosotani89} [[Yutaka Hosotani]], _Dynamics of non-integrable phases and gauge symmetry breaking_, Annals of Physics Volume 190, Issue 2, March 1989, Pages 233-253 (<a href="https://doi.org/10.1016/0003-4916(89)90015-8">doi:10.1016/0003-4916(89)90015-8</a>)

and was revived with:

* H. Hatanaka, T. Inami, C.S. Lim, _The Gauge Hierarchy Problem and Higher Dimensional Gauge Theories_, Mod. Phys. Lett. A13 (1998) 2601-2612 ([arXiv:hep-th/9805067](https://arxiv.org/abs/hep-th/9805067))

Review:

* {#Hosotani12} [[Yutaka Hosotani]], _Gauge-Higgs Unification Approach_, AIP Conference Proceedings 1467, 208 (2012) ([arXiv:1206.0552](https://arxiv.org/abs/1206.0552))

See also:

* Naoyuki Haba, Kazunori Takenaga, Toshifumi Yamashita, _Higgs mass in the gauge-Higgs unification_, Phys. Lett. B615 (2005) 247-256 ([arXiv:hep-ph/0411250](https://arxiv.org/abs/hep-ph/0411250))

* {#Lim09} C. S. Lim, _Precision Tests and CP Violation in Gauge-Higgs Unification_, 2009 ([slides pdf](https://www.iop.vast.ac.vn/theor/conferences/icfp09/files/Lim))


Discussion of [[gauge-Higgs unification]] in [[Spin(11)]]-[[GUT]] ("SO(11)-GUT"):

* {#HosotaniYamatsu15} [[Yutaka Hosotani]], Naoki Yamatsu, _Gauge–Higgs grand unification_, Progress of Theoretical and Experimental Physics, Volume 2015, Issue 11, November 2015 ([arXiv:1504.03817](https://arxiv.org/abs/1504.03817), [doi:10.1093/ptep/ptw116](https://doi.org/10.1093/ptep/ptw116))

* {#FuruiHosotaniYamatsu16} Atsushi Furui, [[Yutaka Hosotani]], Naoki Yamatsu, _Toward Realistic Gauge-Higgs Grand Unification_, Progress of Theoretical and Experimental Physics, Volume 2016, Issue 9, September 2016, 093B01 ([arXiv:1606.07222](https://arxiv.org/abs/1606.07222))

* {#Hosotoni16} [[Yutaka Hosotani]], _Gauge-Higgs EW and Grand Unification_, International Journal of Modern Physics AVol. 31, No. 20n21, 1630031 (2016)  ([arXiv:1606.08108](https://arxiv.org/abs/1606.08108))

* {#Hosotani17} [[Yutaka Hosotani]], _New dimensions from gauge-Higgs unification_ ([arXiv:1702.08161](https://arxiv.org/abs/1702.08161))

* {#HosotaniYamatsu17} [[Yutaka Hosotani]], Naoki Yamatsu, _Electroweak Symmetry Breaking and Mass Spectra in Six-Dimensional Gauge-Higgs Grand Unification_ ([arXiv:1710.04811](https://arxiv.org/abs/1710.04811))


Discussion of [[gauge-Higgs unification]] in [[Spin(11)]]-[[GUT]] ("SO(11)-GUT"):

* S. Rajpoot and P. Sithikong, _Implications of the $SO(12)$ gauge symmetry for grand unification_, Phys. Rev. D 23, 1649 (1981) ([doi:10.1103/PhysRevD.23.1649](https://doi.org/10.1103/PhysRevD.23.1649))

* {#NomuraSato08} Takaaki Nomura, Joe Sato, _Standard(-like) Model from an $SO(12)$ Grand Unified Theory in six-dimensions with $S^2$ extra-space_, Nucl.Phys.B811:109-122, 2009 ([arXiv:0810.0898](https://arxiv.org/abs/0810.0898))

* {#Nomura09} Takaaki Nomura, _Physics beyond the standard model with $S^2$ extra-space_, 2009 ([pdf](http://krishna.th.phy.saitama-u.ac.jp/joe/doctor/nomura-doctor.pdf), [[NomuraSO12GUT.pdf:file]])

* {#ChiangNomuraSato11} Cheng-Wei Chiang, Takaaki Nomura, Joe Sato, _Gauge-Higgs unification models in six dimensions with $S^2/\mathbb{Z}_2$ extra space and GUT gauge symmetry_ ([arXiv:1109.5835](https://arxiv.org/abs/1109.5835))


### In string theory

Discussion of the Higgs field from [[intersecting D-brane models]] is due to

* {#IbanezMarchesanoRabadan01} [[Luis Ibáñez]], [[Fernando Marchesano]], R. Rabadan, section 7 of _Getting just the Standard Model at Intersecting Branes_, JHEP 0111:002, 2001 ([arXiv:hep-th/0105155](https://arxiv.org/abs/hep-th/0105155))

* {#CremadesIbanezMarchesano02} D. Cremades, [[Luis Ibáñez]], [[Fernando Marchesano]], _Intersecting brane models of particle physics and the Higgs mechanism_, JHEP, 0207, 022 2002 ([arXiv:hep-th/0203160](https://arxiv.org/abs/hep-th/0203160))

* {#HebeckerKnochelWeigand13} Arthur Hebecker, Alexander K. Knochel, [[Timo Weigand]], _The Higgs mass from a String-Theoretic Perspective_,  Nucl.Phys. B874 (2013) 1-35 ([arXiv:1304.2767](https://arxiv.org/abs/1304.2767))

* {#HINSS18} Manami Noumi Hashi, Hiroshi Isono, Toshifumi Noumi, [[Gary Shiu]], Pablo Soler, _Higgs Mechanism in Nonlocal Field Theories_, JHEP08 (2018) 064 ([arXiv:1805.02676](https://arxiv.org/abs/1805.02676))


Discussion of the Higgs mechanism in the [[G2-MSSM]] and related models is due to

* {#Kane11} [[Gordon Kane]], _String theory and generic predictions for our world &#8211; superpartner masses, LHC signatures, dark matter, EWSB, cosmological history of universe, etc_, talk at String phenomenology 2011, August 2011 ([pdf](http://conferencing.uwex.edu/conferences/stringpheno2011/documents/kane.pdf))

* {#KaneKumarLuZheng11} [[Gordon Kane]], Piyush Kumar, Ran Lu, Bob Zheng, _Higgs Mass Prediction for Realistic String/M Theory Vacua_, Phys. Rev. D 85, 075026 ([arXiv:1112.1059](http://arxiv.org/abs/1112.1059))

  (a useful informed comment is [here](http://www.math.columbia.edu/~woit/wordpress/?p=4262&cpage=1#comment-101525))

and related to the issue of the [[vacuum stability]] in

* {#Kane18} [[Gordon Kane]], _Exciting Implications of LHC Higgs Boson Data_ ([arXiv:1802.05199](https://arxiv.org/abs/1802.05199))

which is based on

* {#Kane17} [[Gordon Kane]], _String theory and the real world_, Morgan & Claypool, 2017 ([doi:0.1088/978-1-6817-4489-6](http://iopscience.iop.org/book/978-1-6817-4489-6">doi:0.1088/978-1-6817-4489-6))

See also

* Lawrence J. Hall, Yasunori Nomura, _Grand Unification and Intermediate Scale Supersymmetry_, JHEP02 (2014) 129 ([arXiv:1312.6695](https://arxiv.org/abs/1312.6695))

* Lawrence J. Hall, Yasunori Nomura, Satoshi Shirai, _Grand Unification, Axion, and Inflation in Intermediate Scale Supersymmetry_ ([arXiv:1403.8138](https://arxiv.org/abs/1403.8138))



* David Dunsky, Lawrence J. Hall, Keisuke Harigaya, _Dark Matter Detection, Standard Model Parameters, and Intermediate Scale Supersymmetry_ ([arXiv:2011.12302](https://arxiv.org/abs/2011.12302))


Discussion in [[holographic QCD]]:

* {#EspiruKatanaeva18} Domenec Espriu, Alisa Katanaeva, _Composite Higgs Models: a new holographic approach_ ([arXiv:1812.01523](https://arxiv.org/abs/1812.01523))


* Johanna Erdmenger, Nick Evans, Werner Porod, Konstantinos S. Rigatos, _Gauge/gravity dual dynamics for the strongly coupled sector of composite Higgs models_ ([arXiv:2010.10279](https://arxiv.org/abs/2010.10279))

Discussion in [[heterotic string theory]]:

* Steven Abel, [[Keith Dienes]],
*Calculating the Higgs Mass in String Theory* ([arXiv:2106.04622](https://arxiv.org/abs/2106.04622))








[[!redirects Higgs fields]]

[[!redirects Higgs mechanism]]

[[!redirects Higgs effect]]
[[!redirects Higgs effects]]


[[!redirects Higgs particle]]
[[!redirects Higgs particles]]

