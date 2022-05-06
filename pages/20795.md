

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

[[bound state]] of [[D-brane|Dp-]] with [[D-brane|D(p+2)-branes]].

## Examples

* [[Dp-D(p+2)-brane bound state]]

  * [[D1-D3-brane bound state]]

  * [[D2-D4-brane bound state]]

  * [[D6-D8-brane bound state]]


## Properties




[[!include Dp-D(p+2)-brane intersections in fuzzy funnels -- section]]



### $\mathrm{D}6 \perp \mathrm{D}8$-brane intersections

Specifically for $p = 6$, i.e. for [[D6-D8 brane intersections]], this fits with the [[Witten-Sakai-Sugimoto model]] [[geometric engineering of QFT|geometrically engineering]] [[quantum chromodynamics]], and then gives a [[geometric engineering of QFT|geometric engineering]] of the [[Yang-Mills monopoles]] in actual [[QCD]] ([HLPY 08, p. 16](#HLPY08)).

<center>
<img src="https://ncatlab.org/nlab/files/WSSBraneConfigurationEngineeringQCDII.jpg" width="740"/>
</center>

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/D8D6NS5.jpg" width="350"/>
</div>

Here we are showing

1. the [[color charge|color]] [[D4-branes]];

1. the [[flavour (particle physics)|flavor]] [[D8-branes]];

   with

   1. the [[5d Chern-Simons theory]] on their [[worldvolume]]

   1. the corresponding [[4d WZW model]] on the boundary

   both exhibiting the [[meson fields]]

1. the [[baryon]] [[D4-branes]]

   (see below at _[WSS -- Baryons](Witten-Sakai-Sugimoto+model#Baryons)_)

1. the [[Yang-Mills monopole]] [[D6-branes]] 

   (see at _[[D6-D8-brane bound state]]_)

1. the [[NS5-branes]].


### The s-rule

What has come to be known as the _[[s-rule]]_ is the conjecture that the configuration of [[Dp-D(p+2)-brane bound states]] with the [[D-brane|Dp-branes]] stretching from the [[D-brane|D(p+2)-branes]] to  [[NS5-branes]], can be [[supersymmetry|supersymmetric]] only if at most one D$p$-brane ends on any one D$(p+2)$-brane.

For [[D4-D6 brane intersections]]:

<center>
<img src="https://ncatlab.org/nlab/files/D4D6BraneInsersectionSubjectToSRule.jpg" width="700">
</center>

> graphics grabbed from [Fazzi 17](D4-D6-brane+intersection#Fazzi17)

For [[D6-D8 brane intersections]]:

<center>
<img src="https://ncatlab.org/nlab/files/D6D8BraneIntersectionsSubjetToSRule.jpg" width="600">
</center>

> graphics grabbed from [Fazzi 17](D6-D8-brane+intersection#Fazzi17)


<img src="https://ncatlab.org/nlab/files/GaiottoNS5D6.jpg" width="600">

> graphics grabbed from [Gaiotto-Tomasiello 14](D6-D8-brane+intersection#GaiottoTomasiello14)



\linebreak

\linebreak


### Single trace observables as $\mathfrak{su}(2)$-weight systems on chord diagrams
  {#SingleTraceObservablesAsWeightSystemsOnChordDiagrams}

We discuss how the [[single trace observables]] on the [[fuzzy 2-sphere]]-sections  of [[Dp-D(p+2) brane intersection]] [[fuzzy funnels]] are given by [[su(2)]]-[[Lie algebra weight systems]] on [[chord diagrams]] (following [Ramgoolam-Spence-Thomas 04](#RamgoolamSpenceThomas04), [McNamara-Papageorgakis 05](#McNamaraPapageorgakis05), see [McNamara 06, Section 4](#McNamara06) for review). 

For more see at _[[weight systems on chord diagrams in physics]]_.


<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/WeightSystemsAsShapeObservabesOnFuzzySphere.jpg" width="400">
</div>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

\linebreak


While in the commutative [[large N limit]], all powers of the [[radius]] function on the [[fuzzy 2-sphere]] are equal

$$
  \underset{N\to \infty}{\lim}
  \int_{S^2_N} R^{2 k}
  \;=\;  
  4 \pi 
  \,;
$$

for [[finite number|finite]] $N$ there is an ordering ambiguity: In fact, the number of functions on the [[fuzzy 2-sphere]] at [[finite number|finite]] $N$ that all go to the same function $R^{2k}$ in the [[large N limit]] grows rapidly with $k$.

At $k = 1$ there is the single radius observable (eq:RadiusOfFuzzy2Sphere)

$$
  \int_{S^2_N} R^2 
  \;=\; 
  \int_{S^2_N}
  \underset{i}{\sum} X_i \cdot X_i
  \;=\;
  4 \pi \tfrac{ N }{ \sqrt{N^2 -1} }
$$

At $k = 2$ there are, under the integral (eq:FuzzyS2Integration), two radius observables:

1. $ \int_{S^2_N} \underset{i,j}{\sum} X_i X_i X_j X_j$

1. $\int_{S^2_N} \underset{i,j}{\sum} X_i X_j X_j X_i$

(Here we are using that under the integral/trace, a [[cyclic permutation]] of the factors in the integrand does not change the result).

Similarly for higher $k$, where the number of possible orderings increases rapidly. The [[combinatorics]] that appears here is familiar in [[knot theory]]:

Every ordering of operators, up to cyclic permutation, in the [[single trace observable]] $Tr(R^2)^n$ is encoded in a [[chord diagram]] and the value of the corresponding [[single trace observable]] is the value of the [[su(2)]]-[[Lie algebra weight system]] on this chord diagram.

### Parallel intersection

Parallel: dissolves ([Gava-Narain-Sarmadi 97](#GavaNarainSarmadi97))



## Related concepts

* [[fuzzy funnel]]

\linebreak

[[!include brane bound states -- table]]



## References

### For parallel intersection

For parallel intersection:

* {#GavaNarainSarmadi97}  E. Gava, K.S. Narain, M.H. Sarmadi, _On the Bound States of $p$- and $(p+2)$-Branes_, Nucl. Phys. B504 (1997) 214-238 ([arxiv:hep-th/9704006](https://arxiv.org/abs/hep-th/9704006))

### For transversal intersections

#### As spikes/BIons
 {#AsSpikesBIons}

On [[Dp-D(p+2) brane intersections]] as spikes/[[BIons]] 

* [[Curtis Callan]], [[Juan Maldacena]], _Brane Dynamics From the Born-Infeld Action_, Nucl. Phys. B513 (1998) 198-212 ([arXiv:hep-th/9708147](https://arxiv.org/abs/hep-th/9708147))

* [[Paul Howe]], [[Neil Lambert]], [[Peter West]], _The Self-Dual String Soliton_, Nucl. Phys. B515 (1998) 203-216 ([arXiv:hep-th/9709014](https://arxiv.org/abs/hep-th/9709014))

* [[Gary Gibbons]], _Born-Infeld particles and Dirichlet p-branes_,  	Nucl. Phys. B514: 603-639, 1998 ([arXiv:hep-th/9709027](https://arxiv.org/abs/hep-th/9709027))

from the [[M5-brane]]:

* {#HoweLambertWest97} [[Paul Howe]], [[Neil Lambert]], [[Peter West]], _The Self-Dual String Soliton_, Nucl. Phys. B515 (1998) 203-216 ([arXiv:hep-th/9709014](https://arxiv.org/abs/hep-th/9709014))

#### As fuzzy funnels/Yang-Mills monopoles
 {#ReferencesRelationToMonopoles}

On transversal [[Dp-D(p+2) brane intersections]] as [[Yang-Mills monopoles]] / [[fuzzy funnel]]-solutions to [[Nahm's equation]]:

For transversal [[D1-D3 brane intersections]]:

* {#Diaconescu97} Duiliu-Emanuel Diaconescu,  _D-branes, Monopoles and Nahm Equations_, Nucl. Phys. B503 (1997) 220-238 ([arxiv:hep-th/9608163](https://arxiv.org/abs/hep-th/9608163))

* [[Amihay Hanany]], [[Edward Witten]], _Type IIB Superstrings, BPS Monopoles, And Three-Dimensional Gauge Dynamics_, Nucl. Phys. B492:152-190, 1997 ([arxiv:hep-th/9611230](https://arxiv.org/abs/hep-th/9611230))

* {#ConstableMyers99} [[Neil Constable]], [[Robert Myers]], Oyvind Tafjord, _The Noncommutative Bion Core_, Phys. Rev. D61 (2000) 106009 ([arXiv:hep-th/9911136](https://arxiv.org/abs/hep-th/9911136))

* [[Robert Myers]], Section 4 of: _Nonabelian D-branes and Noncommutative Geometry_, J. Math. Phys. 42: 2781-2797, 2001 ([arXiv:hep-th/0106178](https://arxiv.org/abs/hep-th/0106178))

* [[Neil Constable]], [[Neil Lambert]], _Calibrations, Monopoles and Fuzzy Funnels_, Phys. Rev. D66 (2002) 065016 ([arXiv:hep-th/0206243](https://arxiv.org/abs/hep-th/0206243))


* Jessica K. Barrett, Peter Bowcock, _Using D-Strings to Describe Monopole Scattering_ ([arxiv:hep-th/0402163](https://arxiv.org/abs/hep-th/0402163))

* Jessica K. Barrett, Peter Bowcock, _Using D-Strings to Describe Monopole Scattering - Numerical Calculations_ ([arxiv:hep-th/0512211](https://arxiv.org/abs/hep-th/0512211))


* {#ThomasWard06} Steven Thomas, John Ward, _Electrified Fuzzy Spheres and Funnels in Curved Backgrounds_, JHEP 0611:019, 2006 ([arXiv:hep-th/0602071](https://arxiv.org/abs/hep-th/0602071))

For transversal [[D2-D4-brane bound states]] (with an eye towards [[AdS/QCD]]):

* {#GZZ09} Alexander Gorsky, Valentin Zakharov, Ariel Zhitnitsky, _On Classification of QCD defects via holography_, Phys. Rev. D79:106003, 2009 ([arxiv:0902.1842](https://arxiv.org/abs/0902.1842))

For transversal [[D3-D5 brane intersections]]:

* {#GaiottoWitten08} [[Davide Gaiotto]], [[Edward Witten]], Section 2.4 of: _Supersymmetric Boundary Conditions in N=4 Super Yang-Mills Theory_, J Stat Phys (2009) 135: 789 ([arXiv:0804.2902](https://arxiv.org/abs/0804.2902))

For transversal [[D6-D8 brane intersections]] (with an eye towards [[AdS/QCD]]):

* {#HLPY08} Deog Ki Hong, Ki-Myeong Lee, Cheonsoo Park, Ho-Ung Yee, Section V of: _Holographic Monopole Catalysis of Baryon Decay_, JHEP 0808:018, 2008 ([https:arXiv:0804.1326](https://arxiv.org/abs/0804.1326))

and as transversal [[D6-D8-brane bound states]] on a [[half NS5-brane]] in [[type I' string theory]]:

* {#HananyZaffaroni99} [[Amihay Hanany]], [[Alberto Zaffaroni]], _Monopoles in String Theory_, JHEP 9912 (1999) 014 ([arxiv:hep-th/9911113](https://arxiv.org/abs/hep-th/9911113))

Making explicit the completion of the $\mathfrak{su}(2)_{\mathbb{C}} \simeq \mathfrak{sl}(2,\mathbb{C})$-representation to a $\mathfrak{gl}(2,\mathbb{C})$-representation by adjoining the gauge field component $A_y$ to the scalar fields $\vec X$:

* [Gaiotto-Witten 08, Section 3.1.1](#GaiottoWitten08)

* [[Sergey Cherkis]], _Instantons on Gravitons_, around (21) in: Commun. Math. Phys. 306:449-483, 2011 ([arXiv:1007.0044](https://arxiv.org/abs/1007.0044))


#### Relation to Vassiliev braid invariants
 {#ReferencesRelationToKnotInvariants}

Relation of [[Dp-D(p+2)-brane bound states]] ([hence](#ReferencesRelationToMonopoles)
[[Yang-Mills monopoles]]) to [[Vassiliev braid invariants]] via [[chord diagrams]] computing [[radii]] of [[fuzzy spheres]]:

* [[Sanyaje Ramgoolam]], [[Bill Spence]], S. Thomas, Section 3.2 of: _Resolving brane collapse with $1/N$ corrections in non-Abelian DBI_, Nucl. Phys. B703 (2004) 236-276 ([arxiv:hep-th/0405256](https://arxiv.org/abs/hep-th/0405256))

* [[Simon McNamara]], [[Constantinos Papageorgakis]], [[Sanyaje Ramgoolam]], [[Bill Spence]], Appendix A of: _Finite $N$ effects on the collapse of fuzzy spheres_, JHEP 0605:060, 2006 ([arxiv:hep-th/0512145](https://arxiv.org/abs/hep-th/0512145))

* {#McNamara06} [[Simon McNamara]], Section 4 of: _Twistor Inspired Methods in Perturbative Field Theory and Fuzzy Funnels_, 2006 ([spire:1351861](http://inspirehep.net/record/1351861), [pdf](https://strings.ph.qmul.ac.uk/sites/default/files/Mcnamaraphd.pdf), [[McNamara06.pdf:file]])

* [[Constantinos Papageorgakis]], p. 161-162 of: _On matrix D-brane dynamics and fuzzy spheres_, 2006 ([[Papageorgakis06.pdf:file]])

#### Lift to M2-M5-brane bound states
 {#ReferencesLiftToMTheory}

The lift of [[Dp-D(p+2)-brane bound states]] in [[string theory]] to [[M2-M5-brane bound states]]/[[E-strings]] in  [[M-theory]], under [[duality between M-theory and type IIA string theory]]+[[T-duality]], via generalization of [[Nahm's equation]] (this eventually motivated the [[BLG-model]]/[[ABJM model]]):

* [[Anirban Basu]], [[Jeffrey Harvey]], _The M2-M5 Brane System and a Generalized Nahm's Equation_, Nucl.Phys. B713 (2005) 136-150 ([arXiv:hep-th/0412310](https://arxiv.org/abs/hep-th/0412310))

* {#BaggerLambertMukhiPapageorgakis13} [[Jonathan Bagger]], [[Neil Lambert]], [[Sunil Mukhi]], [[Constantinos Papageorgakis]], Section 2.2.1 of _Multiple Membranes in M-theory_, Physics Reports, Volume 527, Issue 1, 1 June 2013, Pages 1-100 ([arXiv:1203.3546](http://arxiv.org/abs/1203.3546), [doi:10.1016/j.physrep.2013.01.006](https://doi.org/10.1016/j.physrep.2013.01.006))

### Single trace observables as weight systems on chord duagrams

Relation of [[single trace observables]] in the [[non-abelian DBI action]] on [[Dp-D(p+2)-brane bound states]] ([hence](Dp-Dp+2-brane+bound+states#ReferencesRelationToMonopoles)
[[Yang-Mills monopoles]]) to [[su(2)]]-[[Lie algebra weight systems]] on [[chord diagrams]] computing [[radii]] averages of [[fuzzy spheres]]:

* {#RamgoolamSpenceThomas04} [[Sanyaje Ramgoolam]], [[Bill Spence]], S. Thomas, Section 3.2 of: _Resolving brane collapse with $1/N$ corrections in non-Abelian DBI_, Nucl. Phys. B703 (2004) 236-276 ([arxiv:hep-th/0405256](https://arxiv.org/abs/hep-th/0405256))

* {#McNamaraPapageorgakis05} [[Simon McNamara]], [[Constantinos Papageorgakis]], [[Sanyaje Ramgoolam]], [[Bill Spence]], Appendix A of: _Finite $N$ effects on the collapse of fuzzy spheres_, JHEP 0605:060, 2006 ([arxiv:hep-th/0512145](https://arxiv.org/abs/hep-th/0512145))

* {#McNamara06} [[Simon McNamara]], Section 4 of: _Twistor Inspired Methods in Perturbative FieldTheory and Fuzzy Funnels_, 2006 ([spire:1351861](http://inspirehep.net/record/1351861), [pdf](https://strings.ph.qmul.ac.uk/sites/default/files/Mcnamaraphd.pdf), [[McNamara06.pdf:file]])

* [[Constantinos Papageorgakis]], p. 161-162 of: _On matrix D-brane dynamics and fuzzy spheres_, 2006 ([[Papageorgakis06.pdf:file]])



[[!redirects Dp-D(p+2)-brane bound states]]

[[!redirects Dp-D(p+2) brane bound state]]
[[!redirects Dp-D(p+2) brane bound states]]

[[!redirects Dp-Dp+2-brane bound state]]
[[!redirects Dp-Dp+2-brane bound states]]

[[!redirects Dp-Dpplus2-brane bound state]]
[[!redirects Dp-Dpplus2-brane bound states]]


[[!redirects DpDp2-brane bound state]]


[[!redirects Dp/D(p+2)-bound state]]
[[!redirects Dp/D(p+2)-bound states]]


[[!redirects Dp-D(p+2) brane intersection]]
[[!redirects Dp-D(p+2) brane intersections]]
[[!redirects Dp/D(p+2) brane intersection]]
[[!redirects Dp/D(p+2) brane intersections]]


[[!redirects Dp-D(p+2)-brane intersection]]
[[!redirects Dp-D(p+2)-brane intersections]]
[[!redirects Dp/D(p+2)-brane intersection]]
[[!redirects Dp/D(p+2)-brane intersections]]

[[!redirects Dp/D(p+2)-brane bound states]]
[[!redirects Dp/D(p+2)-brane bound state]]

