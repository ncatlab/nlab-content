
> This page is a non-maintained mirror of [ncatlab.org/schreiber/show/Hypothesis+H](https://ncatlab.org/schreiber/show/Hypothesis+H). See there for the up-to-date version.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

**Hypothesis H** is a hypothesis about the mathematical formulation of the theory of fundamental physics known as _[[M-theory]]_. The core statement of the hypothesis is that quantum [[charge quantization]] in [[M-theory]] happens in the [[non-abelian cohomology]] theory called *[[cohomotopy]]* (in more detail: *[[twisted cohomotopy]]*). This originates with an observation due to [Sati 2013](#Sati13) ([Sec. 2.5](https://arxiv.org/pdf/1310.1060.pdf#page=17)) and has become the theme of a research program developed by [[Hisham Sati]] and [[Urs Schreiber]], see the list of references [below](#References).

(In a play on how the "M" in "M-theory" has been [said](https://ncatlab.org/nlab/show/M-theory#MagicMysteryQuote) to be either for "Membrane" or for "Mystery", so the "H" in "Hypothesis H" may be read as being either for "Homotopy" or for "Hisham".)

## The open problem of formulating M-Theory
 {#TheOpenProblemOfFormulatingMTheory}

It is an open problem to mathematically formulate _[[M-theory]]_: Supposedly a single coherent [[theory (physics)|theory of physics]] whose various [[limit of a sequence|limiting]] cases reproduce the zoo of [[perturbative string theory|perturbative string theories]] ([[heterotic string theory|HET]]/[[type I string theory|I]]/[[type IIA string theory|IIA]]/[[type IIB string theory|IIB]]&[[F-theory|F]]/[[D=11 supergravity|11d SuGra]]) and the expected [[duality in string theory|dualities]] relating them; but which also makes mathematical sense of [[non-perturbative effect|non-perturbative]] [[D-brane|D-]]/[[M-brane]] physics, and hence solves, via [[intersecting D-brane models]] of [[confinement|confined]] [[quantization of Yang-Mills theory|quantum]] [[Yang-Mills theory]] ([[holographic QCD]]), the [[mass gap problem|last of the Millennium Problems]]:

<center>
<a href="https://ncatlab.org/schreiber/files/Schreiber-MTheoryMathematics2020-v200126.pdf#page=8">
<img src="https://ncatlab.org/schreiber/files/ProblemQCDToProblemM230120.jpg" width="670">
</a>
</center>

In the [[physics]]-minded [[string theory]] community, parts of the literature tends to forget or downplay the [[conjecture|conjectural]] nature of many assumptions and leaps of faiths that are being made when it comes to discussion of [[D-brane]]/[[M-brane]] dynamics and generally of [[non-perturbative effects]] in [[string theory]]. More widely recognized is the fact that the theory of [[intersecting branes|coincident]] [[M5-branes]] is missing, together with the formulation of its expected decoupling limit to the [[D=6 N=(2,0) SCFT]] -- but of course these major open problems are but one aspect of full [[M-theory]].
For string-theoretic references that do highlight the open problem of formulating [[M-theory]] see at _[M-theory -- The open problem](https://ncatlab.org/nlab/show/M-theory#TheOpenProblem)_.

In [[mathematics]], it is rare but not unfamiliar that an open problem is not the proof of a theorem within an established theory, but is the establishing of a theory in the first place. A famous example of such a situation is the search for a theory of "absolute geometry" over the "[[field with one element]]". In this [[analogy]], the various [[perturbative string theories]] ([[heterotic string theory|HET]], [[type I string theory|I]], [[type IIA string theory|IIA]], [[type IIB string theory|IIB]] and their [[KK-compactification|KK-compactified]] [[perturbative string theory vacua]]) correspond to [[arithmetic geometry|arithmetic geometries]] over [[ground field|base]] [[prime fields]] $\mathbb{F}_p$ for $p \geq 2$, and the would-be [[M-theory]] corresponds to a  theory of a "[[field with one element]]" that unifies and completes all this, by describing it at a deeper level (literally: a deeper base). 

Hence the task here is to conjure a mathematical theory $\mathcal{X}$, hypothesize that and explain how $\mathcal{X}$ _is_ the putative [[M-theory]], and then rigorously work out the mathematical implications of $\mathcal{X}$ in order to check to which extent they include the required design criterion "$\mathcal{X} \Rightarrow ST$". To the extent that $\mathcal{X}$ implies known or expected phenomena in [[perturbative string theory]] the hypothesis that $\mathcal{X}$ _is_ [[M-theory]] finds support, to the extent that it doesn't $\mathcal{X}$ needs to be modified to or be replaced by some $\mathcal{X}'$, and the process re-started. 

## Hypothesis H

### Statement
 {#StatementOfHypothesisH}

In the large-[[scale]]/low-[[energy]] [[limit of a sequence|limit]] of [[M-theory]] given by [[D=11 supergravity]], the [[covariant phase space]] must consist of [[torsion constraints in supergravity|super-torsion free]] [[super Cartan geometry|super orbi]] $\mathbb{R}^{10,1\vert \mathbf{32}}$[[V-manifold|-folds]]  equipped with a suitable [[higher gauge field]]: the [[C-field]]. 

<center>
<a href="https://ncatlab.org/schreiber/files/Schreiber-MTheoryMathematics2020-v200126.pdf#page=12">
<img src="https://ncatlab.org/schreiber/files/MTheoryInSupergravityLimit200123.jpg" width="670">
</a>
</center>

The first ingredient of a [[non-perturbative effect|non-perturbative]] [[quantum gravity|quantization]] of this [[phase space]] must be a choice of [[Dirac charge quantization]]-condition for the [[C-field]].

<center>
<a href="https://ncatlab.org/schreiber/files/Schreiber-MTheoryMathematics2020-v200126.pdf#page=14">
<img src="https://ncatlab.org/schreiber/files/HypothesisH200123.jpg" width="670">
</a>
</center>

{#HypothesisH} **Hypothesis H:** ([FSS 19b](#FSS19b),[FSS 19c](#FSS19c)) _The [[C-field]] is [[Dirac charge quantization|charge quantized]] in [[J-homomorphism|J-]][[twisted cohomotopy|twisted]] [[cohomotopy cohomology theory]]_.

<center>
<a href="https://ncatlab.org/schreiber/files/Schreiber-MTheoryMathematics2020-v200126.pdf#page=21">
<img src="https://ncatlab.org/schreiber/files/HypothesisH.jpg" width="640">
</a>
</center>

<div style="float:right;margin:0 10px 10px 0;">
<a href="https://arxiv.org/pdf/1903.02834.pdf#page=14">
<img src="https://ncatlab.org/schreiber/files/TheRational4SphereAppears.jpg" width="380">
</a>
</div>

### Motivation from homotopy theoretic re-analysis of the brane-scan
 {#MotivationFromHomotopyTheoreticReanalysisOfBraneScan}

The [Hypothesis H](#HypothesisH) ([above](#StatementOfHypothesisH)) is motivated from re-analysis (based on [Sati 13, Sec. 2.5](#Sati13)  see [FSS 19a](#FSS19a) for comprehensive review) of [[geometry of physics -- fundamental super p-branes|super p-brane WZ terms]] in [[super homotopy theory]]. The resulting _[[schreiber:brane bouquet]]_ _proves_ that -- in the approximation of [[rational homotopy theory]] -- [[M-brane]] charge is in [[rational cohomotopy]] in exactly the same way that [[D-brane charge quantization in K-theory|D-brane charge is in twisted K-theory]].

<a href="https://arxiv.org/pdf/1606.03206.pdf#page=20">
<img src="https://ncatlab.org/schreiber/files/SupercocyclesRationalTwistedKTheory.jpg" width="440">
</a>

Detailed lecture note on this point are at _[[geometry of physics -- fundamental super p-branes]]_, in the section _[M-Flux fields](https://ncatlab.org/nlab/show/geometry+of+physics+--+fundamental+super+p-branes#MFluxFields)_.

***

<center>
<a href="https://ncatlab.org/schreiber/files/EquivariantSuperHomotopyTheory120314a.pdf#page=74">
<img src="https://ncatlab.org/schreiber/files/BraneBouquetAnimated.gif" width="450>"
</a>
</center>

## Implications
 {#Implications}

Assuming [Hypothesis H](#HypothesisH), we have a well-defined [[covariant phase space]] and may rigorously derive properties of the resulting [[states]] and [[observables]]. These are the implications of [Hypothesis H](#HypothesisH). To the extent that these implications match known facts of [[perturbative string theory]] and to the extent that they match [[folklore]] about [[M-theory]], [Hypothesis H](#HypothesisH) finds support, to the extend that they do not [Hypothesis H](#HypothesisH) may need to be adjusted or abandoned.

### Anomaly cancellation

What physicists call _[[anomalies]]_ are what mathematician call _[[obstructions]]_ to the construction of a [[theory (physics)|physical theory]]. Hence [[anomaly cancellation|cancellation]] of all [[anomalies]] in every [[quantum field theory]] that [[folklore]] expects to be a [[limit of a sequence|limiting case]] of [[M-theory]] is strictly necessary for [[M-theory]] to exist: Any remaining anomaly is an [[obstruction]] against the existence of the theory that it is an anomaly of. 

A long list of anomaly cancellation conditions in M-theory has been argued for in the literature, obtained from a variety of different arguments and under various assumptions, but supported by a web of consistency checks.

**Theorem** ([FSS 19b](#FSS19b), [FSS 19c](#FSS19c), [SS 19a](#SS19a)) 

_[Hypothesis H](##HypothesisH) implies the following list of [[anomaly cancellation]] consistency conditions expected in the [[M-theory]] [[folklore]]_:

<center>
<a href="https://arxiv.org/pdf/1904.10207.pdf#page=2">
<img src="https://ncatlab.org/schreiber/files/HypothesisHImplications.jpg" width="740">
</a>
</center>

#### On curved but non-singular 8-manifolds
 {#OnCurvedButNonSingularManifolds}

Here is a quick survey of the implications of _[Hypothesis H](#HypothesisH)_ on expected M-theory anomaly cancellation conditions for [[M-theory on 8-manifolds]]:

  **download:** [[schreiber:HypothesisHIntroductionAndSurvey191125.pdf:file]]

<center>
<a href="https://arxiv.org/pdf/1904.10207.pdf#page=2">
<img src="https://ncatlab.org/schreiber/files/AnmlCnclltnInMThryOn8MfdsViaHypothesisH.jpg" width="740">
</a>
</center>

#### On flat but singular orbifolds:

<div style="float:right;margin:0 10px 10px 0;">
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=5">
<img src="https://ncatlab.org/schreiber/files/AbsoluteDBraneOPlaneCharge.jpg" width="500">
</a>
</div>

[Hypothesis H](#HypothesisH) implies [[RR-field tadpole cancellation]] on [[flat orbifolds]] with [[ADE-singularities]], including the _absolute_ [[O-plane charge]] and hence the [[SemiSpin(32)]]-[[gauge group]] of [[type I' string theory]], [[duality between type I and heterotic string theory|dually]] of [[heterotic string theory]]. This is the heart of what came to be known as the "first string theory revolution" ([Schwarz 07](https://ncatlab.org/nlab/show/string+theory#Schwarz07)).

From [SS 19a](#SS19a):

<center>
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=2">
<img src="https://ncatlab.org/schreiber/files/RRFieldTadpoleCancellationViaHypothesisH.jpg" width="740">
</a>
</center>

### Microscopic brane physics

The core aspect of [[D-brane]] physics is the [[folklore]] (see [BMSS 19, p. 3](#BMSS19)) that, at low [[energy]], [[coincident branes|coincident]] [[D-branes]] carry [[Yang-Mills theory|Yang-Mills]] [[gauge theory]] on their [[worldvolumes]]. This is the starting point of [[geometric engineering of quantum field theory]] in [[intersecting D-brane models]] and without this phenomenon, string theory would be irrelevant for [[phenomenology]]. 

Moreover, [[folklore]] has it (but see the issues with the [[nonabelian DBI action]] [here](https://ncatlab.org/nlab/show/M-theory#OpenProblemNonabelianDBI)) that at small-[[scale]]/high-[[energy]] [[intersecting brane|intersecting]] [[branes]] show the deep quantum phenomena associated with [[monopoles in Yang-Mills theory]], which ultimately lead to the partial formulation of [[M-theory]] via the [[BFSS matrix model]] and the [[BMN matrix model]].

[Hypothesis H](#HypothesisH) implies that the [[states]] and [[observables]] of [[M-theory]] reflect the following expected phenomena for [[Dp-D(p+2)-brane intersections]]:

From [SS 19c](#SS19c):

<a href="https://ncatlab.org/schreiber/files/DifferentialCohomotopyIntersectingBranes200116.pdf#page=3">
<img src="https://ncatlab.org/schreiber/files/EmergenceOfIntersectinBraneObservablesII.jpg" width="800">
</a>

## See also

* [[twisted cohomotopy]]

* [[equivariant cohomotopy]] 

* [[differential cohomotopy]]

## FAQ
 {#FAQ}

* [MO-question:377071/381](https://mathoverflow.net/q/377071/381): 

  > "In M-theory, what can hypothesis H tell us that quantization in ordinary cohomology cannot?"

  answer at: [MO-answer:377154/381](https://mathoverflow.net/a/377154/381)

### References for the [FAQ](#FAQ)

* {#DMW00} E. Diaconescu, G. Moore, E. Witten, _$E_8$ Gauge Theory, and a Derivation of K-Theory from M-Theory_, Adv. Theor. Math. Phys. 6:1031-1134, 2003 ([arXiv:hep-th/0005090](http://arxiv.org/abs/hep-th/0005090)), summarised in: _A Derivation of K-Theory from M-Theory_ ([arXiv:hep-th/0005091](http://arxiv.org/abs/hep-th/0005091))

* {#HS02} M Hopkins, I. Singer, *[[nLab:Quadratic Functions in Geometry, Topology, and M-Theory]]*_, J. Differential Geom. Volume 70, Number 3 (2005), 329-452 ([arXiv:math.AT/0211216](http://arxiv.org/abs/math.AT/0211216), [euclid:1143642908](https://projecteuclid.org/euclid.jdg/1143642908))

* {#DFM03} E. Diaconescu, D. Freed, G. Moore,  _The $M$-theory 3-form and $E_8$-gauge theory_, chapter in: _Elliptic Cohomology Geometry, Applications, and Higher Chromatic Analogues_, Cambridge University Press 2007 ([arXiv:hep-th/0312069](http://arxiv.org/abs/hep-th/0312069), [doi:10.1017/CBO9780511721489](https:
//doi.org/10.1017/CBO9780511721489))

* {#MSa03} V. Mathai, H. Sati, _Some Relations between Twisted K-theory and E8 Gauge Theory_, JHEP 0403:016, 2004 ([arXiv:hep-th/0312033](https://arxiv.org/abs/hep-th/0312033), [doi:10.1088/1126-6708/2004/03/016](https://iopscience.iop.org/article/10.1088/1126-6708/2004/03/016))

* {#Sa13} H. Sati, _Framed M-branes, corners, and topological invariants_, J. Math. Phys. 59 (2018), 062304 ([arXiv:1310.1060](http://arxiv.org/abs/1310.1060))

* {#FSS15} D. Fiorenza, H. Sati, U. Schreiber,  _The WZW term of the M5-brane and differential cohomotopy_, J. Math. Phys. 56, 102301 (2015) ([arXiv:1506.07557](http://arxiv.org/abs/1506.07557), [doi:10.1063/1.4932618](http://scitation.aip.org/content/aip/journal/jmp/56/10/10.1063/1.4932618))
 
* {#FSS16} D. Fiorenza, H. Sati, U. Schreiber, _Rational sphere valued supercocycles in M-theory and type IIA string theory_, J. Geom. Phys., Vol 114 (2017) ([arXiv:1606.03206](http://arxiv.org/abs/1606.03206), [doi:10.1016/j.geomphys.2016.11.024](http://dx.doi.org/10.1016/j.geomphys.2016.11.024))

* {#BMSS18} V. Braunack-Mayer, H. Sati, U. Schreiber, _Gauge enhancement of super M-branes via parametrized stable homotopy theory_, Comm. Math. Phys. 371: 197 (2019) ([arXiv:1806.01115](https://arxiv.org/abs/1806.01115), [doi:10.1007/s00220-019-03441-4](https://doi.org/10.1007/s00220-019-03441-4))

* {#BSS18} S. Burton, H. Sati, U. Schreiber, _Lift of fractional D-brane charge to equivariant Cohomotopy theory_, J. Geom. Phys., 2020 (in print) ([arXiv:1812.09679](https://arxiv.org/abs/1812.09679))

* {#FSS19a} D. Fiorenza, H. Sati, U. Schreiber, _The rational higher structure of M-theory_, in: _Proceedings of Higher Structures in M-Theory 2018_, Fortsch. Phys. 2019 ([arXiv:1903.02834](https://arxiv.org/abs/1903.02834), [doi:10.1002/prop.201910017](https://doi.org/10.1002/prop.201910017))    

* {#FSS19b} D. Fiorenza, H. Sati, U. Schreiber, _Twisted Cohomotopy implies M-Theory anomaly cancellation on 8-manifolds_, Comm. Math. Phys.  377(3), 1961-2025 (2020) ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207), [doi:10.1007/s00220-020-03707-2](https://doi.org/10.1007/s00220-020-03707-2))

* {#FSS19c} D. Fiorenza, H. Sati, U. Schreiber, _Twisted Cohomotopy implies level quantization of the full 6d Wess-Zumino-term of the M5-brane_, Comm. Math. Phys. 2020 (in print) ([arXiv:1906.07417](https://arxiv.org/abs/1906.07417))

* {#FSS19d} D. Fiorenza, H. Sati, U. Schreiber, _Twistorial Cohomotopy Implies Green-Schwarz anomaly cancellation_ ([arXiv:2008.08544](https://arxiv.org/abs/2008.08544))

* {#SS19a} H. Sati, U. Schreiber, _Equivariant Cohomotopy implies orientifold tadpole cancellation_ J. Geom. Phys. Vol 156, 2020, 103775 ([arXiv:1909.12277](https://arxiv.org/abs/1909.12277), [doi:10.1016/j.geomphys.2020.103775](https://doi.org/10.1016/j.geomphys.2020.103775))

* {#SS19b} H. Sati, U. Schreiber, _Differential Cohomotopy implies intersecting brane observables via configuration spaces and chord diagrams_ ([arXiv:1912.10425](https://arxiv.org/abs/1912.10425))

* {#SS20a} H. Sati, U. Schreiber, _Twisted Cohomotopy implies M5-brane anomaly cancellation_ ([arXiv:2002.07737](https://arxiv.org/abs/2002.07737))

* {#SS20b} H. Sati, U. Schreiber, _The character map in equivariant twistorial Cohomotopy implies the Green-Schwarz mechanism with heterotic M5-branes_ ([arXiv:2011.06533](https://arxiv.org/abs/2011.06533))

* {#Sa20} H. Sati, _M-theory and cohomotopy_, talk at _M-Theory and Mathematics_, NYUAD 2020 ([pdf](https://ncatlab.org/nlab/files/SatiMTheoryCohomotopy2020.pdf))

* {#Sc20} U. Schreiber, _Microscopic brane physics from Cohomotopy theory_, talk at _M-Theory and Mathematics_, NYUAD 2020 ([pdf](https://ncatlab.org/schreiber/files/Schreiber-MTheoryMathematics2020-v200126a.pdf))

## References
 {#References}

Introduction and survey:

* {#IntroductionToHypothsisH} [[Hisham Sati]], [[Urs Schreiber]], *[[schreiber:Introduction to Hypothesis H]]*.

More references:

* [Motivation by results in rational Cohomotopy](#ReferencesInRational)

* [Formulation in full Cohomotopy](#ReferencesFormulationInFullCohomotopyTheory)

* [Exposition and talk notes](#ExpositionAndTalkNotes)
  
### Motivation by results in rational Cohomotopy
 {#ReferencesInRational}

[Hypothesis H](#HypothesisH) is motivated by analysis of [[geometry of physics -- fundamental super p-branes|super p-brane WZ terms]] in [[super homotopy theory]], which _proves_ that -- in the approximation of [[rational homotopy theory]] -- [[M-brane]] charge is in [[rational Cohomotopy]] in exactly the same way that [[D-brane charge]] is in [[twisted K-theory]].

This is due to:

* {#Sati13} [[Hisham Sati]]: 

  Section 2.5 of: 

  **Framed M-branes, corners, and topological invariants**

  J. Math. Phys. **59** (2018) 062304 

  [doi:10.1063/1.5007185](https://doi.org/10.1063/1.5007185)

  [arXiv:1310.1060](http://arxiv.org/abs/1310.1060)

and was further developed in:

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:The WZW term of the M5-brane and differential cohomotopy]]**

  J. Math. Phys. **56** (2015) 102301

  [doi:10.1063/1.4932618](http://scitation.aip.org/content/aip/journal/jmp/56/10/10.1063/1.4932618)

  [arXiv:1506.07557](http://arxiv.org/abs/1506.07557)


* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Rational sphere valued supercocycles in M-theory|Rational sphere valued supercocycles in M-theory and type IIA string theory]]**

  J. Geom. Phys. **114** (2017) 91-108

  [doi:10.1016/j.geomphys.2016.11.024](http://dx.doi.org/10.1016/j.geomphys.2016.11.024)

  [arXiv:1606.03206](http://arxiv.org/abs/1606.03206)

  > (see [Grady 2025](#Grady25) for details)


* [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Higher T-duality of super M-branes]]**

  Phys. Lett. B **781** (2018) 694-698
  
  [doi:10.1016/j.physletb.2018.04.058](https://doi.org/10.1016/j.physletb.2018.04.058)

  [arXiv:1805.00233](https://arxiv.org/abs/1805.00233) 


* [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]**

  Comm. Math. Phys. **371** (2019) 425–524

  [doi:10.1007/s00220-019-03442-3](https://doi.org/10.1007/s00220-019-03442-3)

  [arXiv:1805.05987](https://arxiv.org/abs/1805.05987) 


* {#BMSS19} [[Vincent Braunack-Mayer]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Gauge enhancement of Super M-Branes|Gauge enhancement of super M-branes via parametrized stable homotopy theory]]**

  Comm. Math. Phys. **371** (2019) 197–265

  [doi:10.1007/s00220-019-03441-4](https://doi.org/10.1007/s00220-019-03441-4)

  [arXiv:1806.01115](https://arxiv.org/abs/1806.01115)


Exposition and review of the rational situation is in:

* {#FSS19a} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:The rational higher structure of M-theory]]**

  Fort. Phys. (2019) 

  _Proceedings of the [LMS-EPSRC Durham Symposium](http://www.maths.dur.ac.uk/lms/):_ 

  *[[Higher Structures in M-Theory 2018]]*

  [doi:10.1002/prop.201910017](https://doi.org/10.1002/prop.201910017)

  [arXiv:1903.02834](https://arxiv.org/abs/1903.02834)
  

Partial derivation of the [[M5-brane]]-model at this rational level:

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Super-exceptional embedding construction of the M5-brane]]**

  J. High Energy Phys. **2020** 107 (2020). 

  <a href="https://doi.org/10.1007/JHEP02(2020)107">doi:10.1007/JHEP02(2020)107</a>

  [arxiv:1908.00042](https://arxiv.org/abs/1908.00042)

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Super-exceptional M5-brane model -- Emergence of SU(2)-flavor sector]]**

  J. Geom. Phys. **170**(2021) 104349

  [doi:10.1016/j.geomphys.2021.104349](https://doi.org/10.1016/j.geomphys.2021.104349)

  [arXiv:2006.00012](https://arxiv.org/abs/2006.00012)

On [[U-duality]] (and possibly [[mysterious duality]]) as [[automorphisms]] of [[iterated loop space|iterated]] ([[Sullivan model of loop space|rational]]) [[cyclic loop spaces]] of the ([[rational n-sphere|rational]]) [[4-sphere]]:

* [[Hisham Sati]], [[Alexander Voronov]], *Mysterious triality* ([arXiv:2111.14810](https://arxiv.org/abs/2111.14810))

### Formulation in full Cohomotopy theory
 {#ReferencesFormulationInFullCohomotopyTheory}

The detailed form of the [Hypothesis H](#HypothesisH) (that the above rational situation should lift to full [[twisted Cohomotopy|twisted]] [[equivariant Cohomotopy|equivariant]] [[differential Cohomotopy|differential]] [[Cohomotopy theory]])
was formulated, and first consistency checks were made, in:

* {#FSS19b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation on 8-manifolds]]**

  Comm Math. Phys **377** 3 (2020) 1961-2025 

  [doi:10.1007/s00220-020-03707-2](https://doi.org/10.1007/s00220-020-03707-2)

  [arXiv:1904.10207](https://arxiv.org/abs/1904.10207)

* {#FSS19c} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization]]**

  Comm. Math. Phys. **384** 403–432 (2021)

  [doi:10.1007/s00220-021-03951-0](https://doi.org/10.1007/s00220-021-03951-0)

  [arXiv:1906.07417](https://arxiv.org/abs/1906.07417)

* {#GS20} [[Daniel Grady]], [[Hisham Sati]]:

  **Differential cohomotopy versus differential cohomology for M-theory** 

  J. Geom. Phys. **165** (2021) 104203

  [https://doi.org/10.1016/j.geomphys.2021.104203](doi:10.1016/j.geomphys.2021.104203)

  [arXiv:2001.07640](https://arxiv.org/abs/2001.07640)


* {#SS19a} [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Equivariant Cohomotopy implies orientifold tadpole cancellation]]**

  J. Geom. Phy. **156** (2020) 103775

  [doi:10.1016/j.geomphys.2020.103775](https://doi.org/10.1016/j.geomphys.2020.103775)

  [arXiv:1909.12277](https://arxiv.org/abs/1909.12277)



* {#SS19b} [[Hisham Sati]], [[Urs Schreiber]]: 

  **[[schreiber:Lift of fractional D-brane charge to equivariant Cohomotopy theory]]** 

  J. Geom. Phys. **161** (2021) 104034

  [doi:10.1016/j.geomphys.2020.104034](https://doi.org/10.1016/j.geomphys.2020.104034)

  [arXiv:1812.09679](https://arxiv.org/abs/1812.09679)



* {#SS20a} [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Twisted Cohomotopy implies M5-brane anomaly cancellation]]**

  Lett. Math. Phys. **111** 120 (2021)

  [doi:10.1007/s11005-021-01452-8](https://doi.org/10.1007/s11005-021-01452-8)

  [arXiv:2002.07737](https://arxiv.org/abs/2002.07737)



* {#FSS20a} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Twisted Cohomotopy implies twisted String structure on M5-branes]]**

  J. Math. Phys. **62** 042301 (2021)

  [doi:10.1063/5.0037786](https://doi.org/10.1063/5.0037786)

  [arXiv:2002.11093](https://arxiv.org/abs/2002.11093)



* {#SS19c} [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Differential Cohomotopy implies intersecting brane observables]]**

  Adv. Theor. Math. Physics **26** 4 (2022)

  [arXiv:1912.10425](https://arxiv.org/abs/1912.10425)



* {#CSS21a} [[David Corfield]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Fundamental weight systems are quantum states]]**

  [arXiv:2105.02871](https://arxiv.org/abs/2105.02871)



* {#SS20b} [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Proper Orbifold Cohomology]]**

  [arXiv:2008.01101](https://arxiv.org/abs/2008.01101)



* {#FSS20b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Twistorial Cohomotopy implies Green-Schwarz anomaly cancellation]]**

  Rev. Math. Phys. **34** 05 (2022) 2250013

  [arXiv:2008.08544](https://arxiv.org/abs/2008.08544)



* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:The Character Map in Twisted Non-Abelian Cohomology]]**

  [arXiv:2009.11909](https://arxiv.org/abs/2009.11909)



* [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:The Character Map in Twisted Equivariant Nonabelian Cohomology]]**

  [arXiv:2011.06533](https://arxiv.org/abs/2011.06533)



* [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:M-Theory as Mf-Theory|M/F-Theory as Mf-Theory]]**

  [arXiv:2103.01877](https://arxiv.org/abs/2103.01877)


* [[Hisham Sati]], [[Urs Schreiber]]:

  **[[schreiber:Anyonic defect branes in TED-K-theory]]**



See also:

* [[David Michael Roberts]]:

  **Topological sectors for heterotic M5-brane charges under Hypothesis H*

   J. High Energ. Phys. **2020** 52 (2020)

  <a href=" https://doi.org/10.1007/JHEP06(2020)052">doi:10.1007/JHEP06(2020)052</a>

  [arXiv:2003.09832](https://arxiv.org/abs/2003.09832)

Proof that [[supergravity C-field|C-field]] [[geometry of physics -- flux quantization|flux quantization]] in [[stable Cohomotopy]] implies the desired divisibility by 6 of the [[D=11 supergravity]] [[action functional]]:

* {#Grady25} [[Daniel Grady]]: *Cohomotopy and flux quantization in M-theory* &lbrack;[arXiv:2505.24696](https://arxiv.org/abs/2505.24696)&rbrack;




### Exposition and talk notes
 {#ExpositionAndTalkNotes}

* [[Luigi Alfonsi]], §4 in: *Higher geometry in physics*, in: *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2312.07308](https://arxiv.org/abs/2312.07308)&rbrack;


* *[[schreiber:Some Quantum States of M-Branes under Hypothesis H]]*

  talk at [Centre for Research in String Theory](https://strings.ph.qmul.ac.uk/welcome-crst)

  Queen Mary University London, 2021


* _[[schreiber:Proper Orbifold Cohomotopy for M-Theory]]_

  talk at [String and M-Theory: The New Geometry of the 21st Century – II](https://ims.nus.edu.sg/events/string-and-m-theory-the-new-geometry-of-the-21st-century-ii/)

  via NUS Singapore, 2021

* _[[schreiber:Microscopic Brane Physics from Cohomotopy]]_

  talk at [[M-Theory and Mathematics]]

  NYU Abu Dhabi, 2020

*  _[[schreiber:Strings2019|Twisted Cohomotopy implies M-theory anomaly cancellation]]_

   presentation at [Strings2019](https://sis-pc15.ulb.ac.be/event/2/)

   Brussels, 2019


* _[[schreiber:StringMath2017|Super p-Brane Theory emerging from Super Homotopy Theory]]_ 

  talk at [[String Math 2017]], 

  Hamburg, 2017



* _[[schreiber:Equivariant Cohomotopy and Branes]]_ 

  talk at _[String and M-Theory: The New Geometry of the 21st Century](http://ims.nus.edu.sg/events/2018/wstring/index.php)_

  NUS Singapore, 2018


* _[[schreiber:The Higher Structure of 11d Supergravity]]_ 

   talk at _[Souriau 2019](http://souriau2019.fr/)_

   IHP Paris, 2019

* _[[schreiber:Equivariant Cohomotopy of toroidal orbifolds]]_

  talk at [[Sadok Kallel|Prof. Sadok Kallel]]‘s group seminar

  AUS Sharjah, 2019

* _[[schreiber:Cohomotopy Theory and Branes]]_

  talk at _Geometry, topology and Physics_ 

  NYU Abu Dhabi, 2020

* _[[schreiber:Equivariant Stable Cohomotopy and Branes]]_ 

  talk at _Geometry, Topology and Physics_

  NYU Abu Dhabi, 2018

* _[[schreiber:Equivariant cohomology of M2/M5-branes]]_

  talk at _Seminar on Higher Structures_

  MPI Bonn, 2016


* [[schreiber:ToposesCohomologyPhysics201002.pdf:file]]

* [[schreiber:CenturyOfChargeQuantization201012.pdf:file]]

See also:

* *[[schreiber:New Foundations for TDA -- Cohomotopy]]*


