

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Chern-Weil theory
+-- {: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Algebraic Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

By the [[Nahm transform]], the [[moduli space]] of time-translation invariant [[self-dual Yang-Mills theory]] [[solitons]] on 4d [[Minkowski spacetime]] $\mathbb{R}^{3,1}$ is equivalently the space of solutions to the [[Bogomolny equations]] on 3d [[Euclidean space]], which in tur# iN n may be thought of as [[magnetic monopoles]] in 3d [[Euclidean field theory|Euclidean]] [[Yang-Mills theory]] coupled to a charged [[scalar field]] (a "[[Higgs field]]"). Therefore this moduli space is traditionally referred to simply as the _moduli space of magnetic monopoles_ (e.g. [Atiyah-Hitchin 88](#AtiyahHitchin88)) or just the _moduli space of monopoles_.

## Definition

The moduli space 

\[
  \label{ModuliSpaceOfkMonopoles}
  \mathcal{M}_k
  \;\coloneqq\;
  \cdots
\]

of $k$ monopoles is ... ([Atiyah-Hitchin 88, p. 15-16](#AtiyahHitchin88)).

## Properties

### Scattering amplitudes of monopoles
 {#ScatteringAmplitudesofMonopoles}

Write

\[
  \label{SpaceOfRationalFunctionsOfDegreek}
  Maps_{cplx\,rtnl}^{\ast/}\big( \mathbb{C}P^1, \mathbb{C}P^1 \big)_k
  \;\subset\;
  Maps_{cplx\,rtnl}^{\ast/}\big( \mathbb{C}P^1, \mathbb{C}P^1 \big)
  \;\subset\;
  Maps^{\ast/}\big( S^2, S^2 \big)
\]

for the [[space of maps|space of]] [[pointed topological space|pointed]] [[rational functions]] from the [[Riemann sphere]] to itself, of [[degree of a continuous function|degree]] $k \in \mathbb{N}$, inside the full [[Cohomotopy]] [[cocycle space]]. The [[homotopy type]] of $R_k$ is discussed in [Segal 79](#Segal79).

To each configuration $ c \in \mathcal{M}_k$ of $k \in \mathbb{N}$ magnetic monopoles is associated a [[scattering amplitude]] 

\[
  \label{ScatteringAmplitudes}
  S(c) 
    \in    
  Maps_{cplx\,rtnl}^{\ast/}\big( \mathbb{C}P^1, \mathbb{C}P^1 \big)_k

\]

([Atiyah-Hitchin 88 (2.8)](#AtiyahHitchin88))

\linebreak

### Charge quantization in Cohomotopy

+-- {: .num_prop #ModuliSpaceOfKMonopolesIsSpaceOfComplexRationalFunctions}
###### Proposition
**([[moduli space of monopoles|moduli space of k monopoles]] is [[space of maps|space of]] [[degree of a continuous function|degree]] $k$ [[complex number|complex]]-[[rational functions]] from [[Riemann sphere]] to itself)**

The assignment (eq:ScatteringAmplitudes) is a [[diffeomorphism]]
identifying the moduli space (eq:ModuliSpaceOfkMonopoles) of $k$ magnetic monopoles with the space (eq:SpaceOfRationalFunctionsOfDegreek) of complex-[[rational functions]] from the [[Riemann sphere]] to itself, of [[degree of a continuous function|degree]] $k$ (hence the [[cocycle space]] of complex-rational 2-[[Cohomotopy]]) 

$$
  \mathcal{M}_k
  \;
  \underoverset{
    \simeq_{diff}
  }{ 
    S 
  }{
    \;\;\longrightarrow\;\;
  }
  \;
  Maps_{cplx\,rtnl}^{\ast/}
  \big( 
    \mathbb{C}P^1, \mathbb{C}P^1 
  \big)_k
$$

=--

(due to [Donaldson 84](#Donaldson84), see also [Atiyah-Hitchin 88, Theorem 2.10](#AtiyahHitchin88)).

+-- {: .num_prop #SpaceOfComplexRationalMapsOnRiemannSpherekEquivalentToCohomotopyCocycleSpace}
###### Proposition
**([[space of maps|space of]] [[degree of a continuous function|degree]] $k$ [[complex number|complex]]-[[rational functions]] from [[Riemann sphere]] to itself is [[n-equivalence|k-equivalent]] to [[Cohomotopy]] [[cocycle space]] in degree $k$)**

The inclusion of the complex rational self-maps maps of [[degree of a continuous function|degree]] $k$ into the full based [[space of maps]] of [[degree of a continuous function|degree]] $k$ (hence the $k$-component of the second [[iterated loop space]] of the [[2-sphere]], and hence the plain [[Cohomotopy]] [[cocycle space]]) induces an [[isomorphism]] of [[homotopy groups]] in degrees $\leq k$ (in particular a [[n-equivalence|k-equivalence]]):

$$
  Maps_{cplx\,rtnl}^{\ast/}
  \big( 
    \mathbb{C}P^1, \mathbb{C}P^1 
  \big)_k
  \;
  \underset{
    \simeq_{\leq k}
  }{
    \;\;\hookrightarrow\;\;
  }
  \;
  Maps^{\ast/}\big( S^2, S^2 \big)_k
$$


=--

([Segal 79, Prop. 1.1](#Segal79))

Hence, Prop. \ref{ModuliSpaceOfKMonopolesIsSpaceOfComplexRationalFunctions} and Prop. \ref{SpaceOfComplexRationalMapsOnRiemannSpherekEquivalentToCohomotopyCocycleSpace} together say that the moduli space of $k$-monopoles is $k$-equivalent to the Cohomotopy cocycle space $\mathbf{\pi}^2\big( S^2 \big)_k$.

$$
  \mathcal{M}_k
  \;
  \underoverset{
    \simeq_{diff}
  }{ 
    S 
  }{
    \;\;\longrightarrow\;\;
  }
  \;
  Maps_{cplx\,rtnl}^{\ast/}
  \big( 
    \mathbb{C}P^1, \mathbb{C}P^1 
  \big)_k
  \;
  \underset{
    \simeq_{\leq k}
  }{
    \;\;\hookrightarrow\;\;
  }
  \;
  Maps^{\ast/}\big( S^2, S^2 \big)_k
$$

This is a [[non-abelian group|non-abelian]] analog of the [[Dirac charge quantization]] of the [[electromagnetic field]], with [[ordinary cohomology]] replaced by [[Cohomotopy]] [[generalized cohomology theory|cohomology theory]]:


{#Illustration} $\,$


<center>
<img src="https://ncatlab.org/nlab/files/AtiyahHitchinChargeQuantizationII.jpg" width="640">
</center>

\linebreak


### Relation to braid groups

+-- {: .num_prop #ModuliSpaceOfkMonopolesStablyWeakHomotopyEquivbalentToClassifyingSpaceOfBraids}
###### Proposition
**([[moduli space of monopoles]] is [[stable weak homotopy equivalence|stably weak homotopy equivalent]] to [[classifying space]] of [[braid group]])**

For $k \in \mathbb{N}$ there is a [[stable weak homotopy equivalence]] between the [[moduli space of k monopoles]] (eq:ModuliSpaceOfkInstantons) and the [[classifying space]] of the [[braid group]] $Braids_{2k}$ on $2 k$ strands:

$$
  \Sigma^\infty \mathcal{M}_k
  \;\simeq\;
  \Sigma^\infty Braids_{2k}
$$

=--

([Cohen-Cohen-Mann-Milgram 91](#CohenCohenMannMilgram91))

\linebreak

### Geometric engineering by D$p$-D$(p+2)$-brane intersections
 {#GeometricEngineeringByIntersectingBranes}

Generally [[Dp-D(p+2)-brane intersections]] [[geometric engineering of QFT|geometrically engineer]] [[Yang-Mills monopoles]] in the [[worldvolume]] of the higher dimensional D$(p+2)$-branes.

Specifically for $p = 6$, i.e. for [[D6-D8-brane intersections]], this fits with the [[Witten-Sakai-Sugimoto model]] [[geometric engineering of QFT|geometrically engineering]] [[quantum chromodynamics]], and then gives a [[geometric engineering of QFT|geometric engineering]] of the [[Yang-Mills monopoles]] in actual [[QCD]] ([HLPY 08, p. 16](D6-D8-brane+bound+state#HLPY08)).

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

   both exhibiting the [[meson fields]]

1. the [[baryon]] [[D4-branes]]

   (see below at _[WSS -- Baryons](Witten-Sakai-Sugimoto+model#Baryons)_)

1. the [[Yang-Mills monopole]] [[D6-branes]] 

   (see at _[[D6-D8-brane bound state]]_)

1. the [[NS5-branes]].



\linebreak

## Related concepts

* [[Nahm transform]], [[Bogomolny equation]]

[[!include moduli spaces -- contents]]


## References

### General

* {#Donaldson84} [[Simon Donaldson]], _Nahm's Equations and the Classification of Monopoles_, Comm. Math. Phys., Volume 96, Number 3 (1984), 387-407, ([euclid:cmp.1103941858](https://projecteuclid.org/euclid.cmp/1103941858))

* {#AtiyahHitchin88} [[Michael Atiyah]], [[Nigel Hitchin]], _The geometry and dynamics of magnetic monopoles_ , M. B. Porter Lectures. Princeton University Press, Princeton, NJ, 1988 ([jstor:j.ctt7zv206](https://www.jstor.org/stable/j.ctt7zv206))

* {#Segal79} [[Graeme Segal]], _The topology of spaces of rational functions_, Acta Math. Volume 143 (1979), 39-72 ([euclid:1485890033](https://projecteuclid.org/euclid.acta/1485890033))

* [[Michael Atiyah]], [[Nigel Hitchin]], J. T. Stuart and M. Tabor, _Low-Energy Scattering of Non-Abelian Magnetic Monopoles_, Philosophical Transactions of the Royal Society of London. Series A, Mathematical and Physical Sciences Vol. 315, No. 1533, New Developments in the Theory and Application of Solitons (Aug. 13, 1985), pp. 459-469 ([jstor:37546](https://www.jstor.org/stable/37546))

* {#GibbonsManton86} [[Gary Gibbons]], [[Nicholas Manton]], _Classical and Quantum Dynamics of BPS Monopoles_, Nucl. Phys. B274 (1986) 183-224 ([spire:18322](http://inspirehep.net/record/18322), <a href="https://doi.org/10.1016/0550-3213(86)90624-3">doi:10.1016/0550-3213(86)90624-3</a>)

* [[Ralph Cohen]], _Stability phenomena in the topology of moduli spaces_ ([arXiv:0908.1938](https://arxiv.org/abs/0908.1938))

See also

* Wikipedia, _[Monopole moduli space](https://en.wikipedia.org/wiki/Monopole_moduli_space)_

### As transversal D$p$/D$(p+2)$-brane intersections

In [[string theory]] [[Yang-Mills monopoles]] are [[geometric engineering of QFT|geometrically engineeted]] as transversally [[intersecting brane|intersecting]] [[Dp-D(p+2)-brane bound states]]:

For transversal [[D1-D3-brane bound states]]:

* {#Diaconescu97} Duiliu-Emanuel Diaconescu,  _D-branes, Monopoles and Nahm Equations_, Nucl. Phys. B503 (1997) 220-238 ([arxiv:hep-th/9608163](https://arxiv.org/abs/hep-th/9608163))

* [[Amihay Hanany]], [[Edward Witten]], _Type IIB Superstrings, BPS Monopoles, And Three-Dimensional Gauge Dynamics_, Nucl. Phys. B492:152-190, 1997 ([arxiv:hep-th/9611230](https://arxiv.org/abs/hep-th/9611230))

* Jessica K. Barrett, Peter Bowcock, _Using D-Strings to Describe Monopole Scattering_ ([arxiv:hep-th/0402163](https://arxiv.org/abs/hep-th/0402163))

* Jessica K. Barrett, Peter Bowcock, _Using D-Strings to Describe Monopole Scattering - Numerical Calculations_ ([arxiv:hep-th/0512211](https://arxiv.org/abs/hep-th/0512211))


For transversal [[D2-D4 brane intersections]] (with an eye towards [[AdS/QCD]]):

* Alexander Gorsky, Valentin Zakharov, Ariel Zhitnitsky, _On Classification of QCD defects via holography_, Phys. Rev. D79:106003, 2009 ([arxiv:0902.1842](https://arxiv.org/abs/0902.1842))

For transversal [[D3-D5 brane intersections]]:

* {#GaiottoWitten08} [[Davide Gaiotto]], [[Edward Witten]], _Supersymmetric Boundary Conditions in N=4 Super Yang-Mills Theory_, J Stat Phys (2009) 135: 789 ([arXiv:0804.2902](https://arxiv.org/abs/0804.2902))


For transversal [[D6-D8-brane intersections]] (with an eye towards [[AdS/QCD]]):

* {#HLPY08} Deog Ki Hong, Ki-Myeong Lee, Cheonsoo Park, Ho-Ung Yee, Section V of: _Holographic Monopole Catalysis of Baryon Decay_, JHEP 0808:018, 2008 ([https:arXiv:0804.1326](https://arxiv.org/abs/0804.1326))

With emphasis on [[half NS5-branes]] in [[type I' string theory]]:

* {#HananyZaffaroni99} [[Amihay Hanany]], [[Alberto Zaffaroni]], _Monopoles in String Theory_, JHEP 9912 (1999) 014 ([arxiv:hep-th/9911113](https://arxiv.org/abs/hep-th/9911113))

The moduli space of monopoles appears also in the [[KK-compactification]] of the [[M5-brane]] on a complex surface ([[AGT-correspondence]]):

* Benjamin Assel, [[Sakura Schafer-Nameki]], Jin-Mann Wong, _M5-branes on $S^2 \times M_4$: Nahm's Equations and 4d Topological Sigma-models_, J. High Energ. Phys. (2016) 2016: 120 ([arxiv:1604.03606](https://arxiv.org/abs/1604.03606))

### As Coulomb branches of $D=3$ $\mathcal{N}=4$ SYM

Identification of the [[Coulomb branch]] of [[D=3 N=4 super Yang-Mills theory]] with the [[moduli space of monopoles]] in [[Yang-Mills theory]]:

* {#SeibergWitten96} [[Nathan Seiberg]], [[Edward Witten]], _Gauge Dynamics And Compactification To Three Dimensions_, In: J.M. Drouffe, J.B. Zuber (eds.) _The mathematical beauty of physics: A memorial volume for Claude Itzykson_ Proceedings, Conference, Saclay, France, June 5-7, 1996 ([arXiv:hep-th/9607163](http://arxiv.org/abs/hep-th/9607163), [spire:420925](http://inspirehep.net/record/420925))

* N. Dorey, V. V. Khoze, M. P. Mattis, [[David Tong]], S. Vandoren, _Instantons, Three-Dimensional Gauge Theory, and the Atiyah-Hitchin Manifold_, Nucl. Phys. B502 (1997) 59-93 ([arXiv:hep-th/9703228](https://arxiv.org/abs/hep-th/9703228))

* [[David Tong]], _Three-Dimensional Gauge Theories and ADE Monopoles_, Phys. Lett. B448 (1999) 33-36 ([arXiv:hep-th/9803148](https://arxiv.org/abs/hep-th/9803148))

* [[Mathew Bullimore]], [[Tudor Dimofte]], [[Davide Gaiotto]], _The Coulomb Branch of 3d $\mathcal{N}=4$ Theories_, Commun. Math. Phys. (2017) 354: 671 ([arXiv:1503.04817](https://arxiv.org/abs/1503.04817))

### Rozansky-Witten invariants

Discussion of [[Rozansky-Witten invariants]] of [[moduli spaces of monopoles]]:

* {#RozanskyWitten96} [[Lev Rozansky]], [[Edward Witten]], p. 36 of: _Hyper-K&#228;hler geometry and invariants of 3-manifolds_, Selecta Math., New Ser. __3__ (1997), 401&#8211;458 ([arXiv:hep-th/9612216](https://arxiv.org/abs/hep-th/9612216), [doi:10.1007/s000290050016](https://doi.org/10.1007/s000290050016), [MR98m:57041](http://www.ams.org/mathscinet-getitem?mr=98m:57041))


### Relation to braids

Relation to [[braid groups]]:

* {#CohenCohenMannMilgram91} [[Fred Cohen]], [[Ralph Cohen]], B. M. Mann, R. J. Milgram, _The topology of rational functions and divisors of surfaces_, Acta Math (1991) 166: 163 ([doi:10.1007/BF02398886](https://doi.org/10.1007/BF02398886))

* [[Ralph Cohen]], John D. S. Jones  _Monopoles, braid groups, and the Dirac operator_, Comm. Math. Phys. Volume 158, Number 2 (1993), 241-266 ([euclid:cmp/1104254240](https://projecteuclid.org/euclid.cmp/1104254240))



Relation of [[Dp-D(p+2)-brane bound states]] ([hence](Dp-Dp+2-brane+bound+states#ReferencesRelationToMonopoles)
[[Yang-Mills monopoles]]) to [[Vassiliev braid invariants]] via [[chord diagrams]] computing [[radii]] of [[fuzzy spheres]]:

* [[Sanyaje Ramgoolam]], [[Bill Spence]], S. Thomas, Section 3.2 of: _Resolving brane collapse with $1/N$ corrections in non-Abelian DBI_, Nucl. Phys. B703 (2004) 236-276 ([arxiv:hep-th/0405256](https://arxiv.org/abs/hep-th/0405256))

* [[Simon McNamara]], [[Constantinos Papageorgakis]], [[Sanyaje Ramgoolam]], [[Bill Spence]], Appendix A of: _Finite $N$ effects on the collapse of fuzzy spheres_, JHEP 0605:060, 2006 ([arxiv:hep-th/0512145](https://arxiv.org/abs/hep-th/0512145))

* [[Simon McNamara]], Section 4 of: _Twistor Inspired Methods in Perturbative FieldTheory and Fuzzy Funnels_, 2006 ([spire:1351861](http://inspirehep.net/record/1351861), [pdf](https://strings.ph.qmul.ac.uk/sites/default/files/Mcnamaraphd.pdf), [[McNamara06.pdf:file]])

* [[Constantinos Papageorgakis]], p. 161-162 of: _On matrix D-brane dynamics and fuzzy spheres_, 2006 ([[Papageorgakis06.pdf:file]])



[[!redirects moduli spaces of monopoles]]

[[!redirects moduli space of k monopoles]]
[[!redirects moduli spaces of k monopoles]]

[[!redirects Atiyah-Hitchin charge quantization]]

[[!redirects Yang-Mills monopole]]
[[!redirects Yang-Mills monopoles]]

[[!redirects monopole in Yang-Mills theory]]
[[!redirects monopoles in Yang-Mills theory]]


