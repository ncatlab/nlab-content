
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
 {#Idea}

### General idea

The _AdS-CFT correspondence_ at its heart is the observation ([Witten 98, Section 2.4](#Witten98)) that the [[classical field theory|classical]] [[action functionals]] for various [[field (physics)|fields]] coupled to [[Einstein gravity]] on [[anti de Sitter spacetime]] are, when expressed as [[functions]] of the [[asymptotic boundary]]-values of the [[field (physics)|fields]], of the form of [[generating functions]] for [[correlators]]/[[n-point functions]] of a [[conformal field theory]] on that [[asymptotic boundary]], in a [[large N limit]].

{#HolographicPrincipleInIntroduction} This is traditionally interpreted as a concrete realization of a vague "[[holographic principle]]" according to which [[quantum gravity]] in [[bulk]] spacetimes is controlled, in one way or other, by "[[boundary field theories]]" on effective spacetime boundaries, such as [[event horizons]]. The original and main motivation for the [[holographic principle]] itself was the fact that the apparent [[black hole entropy]] in [[Einstein gravity]] scales with the [[area]] of the [[event horizon]] instead of the black hole's bulk volume (which is not even well-defined), suggesting that gravity encodes or is encoded by some [[boundary field theory]] associated with horizons; an idea that, in turn, seems to find a concrete realization in [[open/closed string duality]] in the [[near horizon geometry|vicinity]] of, more generally, [[black branes]]. The original intuition about holographic black hole entropy has meanwhile found remarkably detailed reflection in the (mathematically fairly rigorous) analysis of [[holographic entanglement entropy]], specifically via holographic [[tensor networks]], which turn out to embody key principles of the AdS/CFT correspondence in the guise of [[quantum information theory]], with concrete applications such as to [[quantum error correcting codes]].


The AdS/CFT correspondence itself crucially involves the exceptional [[isomorphism]] between the [[isometry group]] of [[anti de Sitter spacetime]] $AdS_{d+1}$ (the [[anti de Sitter group]]) and the [[conformal group]] of [[Minkowski spacetime]] of dimension $d$: the [[connected component]] of both is the [[special orthogonal group]] $SO(d,2)$. But the AdS/CFT correspondence is deeper and more subtle than this [[group theory]] underlying it, in particular in how it puts [[field (physics)|fields]] and [[states]] on the gravity side in correspondence with [[sources]] and [[correlators]] on the field theory side, respectively.

In extrapolation of these elementary computations, the AdS/CFT correspondence [[conjecture|conjecturally]] extends to a more general identification of [[states]] of [[gravity]] ([[quantum gravity]]) on asymptotically [[anti de Sitter spacetimes]] of [[dimension]] $d+1$ with [[correlators]]/[[n-point functions]] of [[conformal field theories]] on the [[asymptotic boundary]] of dimension $d$ ([Gubser-Klebanov-Polyakov 98 (12)](#GubserKlebanovPolyakov98), [Witten 98, (2.11)](#Witten98)), such that [[perturbative quantum field theory|perturbation theory]] on one side of the correspondence relates to [[non-perturbative effects|non-perturbation]] on the other side.

While this works to some extent quite generally (see e.g. [Natsuume 15](#Natsuume15) for review), allowing applications such as [[AdS/CFT in condensed matter physics]] and [[AdS/QCD|AdS/CFT in quantum chromodynamics]], the tightest form of the correspondence relates the [[1/N expansion]] of [[superconformal field theories]] ([[super Yang-Mills theories]]) on the [[asymptotic boundaries]] of [[near-horizon limits]] of $N$ coincident [[black brane|black]] [[M2-branes]]/[[D3-branes]]/[[M5-branes]] to corresponding sectors of the [[string theory]]/[[M-theory]] [[quantum gravity]] in the [[bulk]] [[spacetime]] away from the brane.

Before the proposal for the actual matching rule of ADS/CFT ([Gubser-Klebanov-Polyakov 98 (12)](#GubserKlebanovPolyakov98), [Witten 98, (2.11)](#Witten98)) it was by matching of [[BPS-states]] in these situations that the existence of an AdS/CFT correspondence was proposed in [Maldacena 97a](#Maldacena97a), [Maldacena 97b](#Maldacena97b);  these articles are now widely regarded as the origin of the idea of the AdS/CFT correspondence. 

A quick way to see that the [[supersymmetric]]-cases of AdS/CFT for [[near horizon geometries]] of [[M2-branes]], [[D3-branes]] and [[M5-branes]] must be special is to observe that these are the only dimensions in which there are [[super anti-de Sitter spacetime]]-enhancements of [[anti de Sitter spacetime]], matching the classification of simple [[superconformal geometry|superconformal symmetries]], see [there](supersymmetry#ClassificationSuperconformal):

[[!include superconformal symmetry -- table]]

It had already been observed by [Bergshoeff, Duff, Pope & Sezgin](#BDPS87) and [Duff & Sutton 1988](#DuffSutton88) (see also [Duff 1998](#Duff98), [Duff 1999](#Duff99)) that the field theory of small perturbation  of a [[Green-Schwarz sigma-model]] for a [[fundamental brane]] stretched over the [[asymptotic boundary]] of the [[AdS spacetime|AdS]] [[near horizon geometry]] of its own [[black brane]]-incarnation is, after [[diffeomorphism]] [[gauge fixing]], a [[conformal field theory]]. This was further developed in [Claus, Kallosh & Proeyen 1997](#ClausKalloshProeyen97), [DGGGTT 98](#DGGGTT98), [Claus-Kallosh, Kumar & Townsend 1998](#ClausKalloshKumarTownsend98), [Pasti, Sorokin & Tonin 1999](#PastiSorokinTonin99). See also at _[super p-brane -- As part of the AdS-CFT correspondence](Green-Schwarz+action+functional#AsPartOfTheAdSCFTCorrespodence)

More recently, for the archetypical case of AdS/CFT relating [[N=4 D=4 super Yang-Mills theory]] to [[type IIB string theory]] on [[super anti-de Sitter spacetime]] $AdS_5 \times S^5$, fine detailed checks of the correspondence have been performed ([Beisert et al. 10](#BeisertEtAl10), [Escobedo 12](#Escobedo12)), see the section _[Checks](#Checks)_ below. 

Thus regarded as a [[duality in string theory]], the AdS/CFT correspondence is an incarnation of [[open/closed string duality]], reflecting the fact that the physics on [[D-branes]] has two equivalent descriptions: 

1) as a [[Yang-Mills theory|Yang-Mills]]-[[gauge theory]] coming from [[open strings]] attached to the [[brane]]

2) as a [[gravity]] theory coming from [[closed strings]] emitted/absorbed by the brane.


<center>
<img src="https://ncatlab.org/nlab/files/OpenClosedCylinderWorldsheetEndingOnBranes.jpg" width="400">
</center>

> graphics grabbed from [Schomerus 07, Figure 4](open/closed+string+duality#Schomerus07), see also e.g.
[Peschanskia 09, Figure 1](open/closed+string+duality#Peschanskia09)

This gives a vivid intuitive picture of the mechanism underlying the correspondence: An excitation of the gauge field on the brane goes along with an excitation of the field of gravity around the brane, and either is faithfully reflected in the other; at least in the suitable limits.

### Small-$N$ corrections
 {#SmallNCorrections}

The AdS/CFT correspondence has been widely discussed and is mostly understood by default only in the *[[large N limit|large $N$ limit]]* and for large [['t Hooft coupling]], where the given gauge theory is dual to plain [[classical field theory|classical]] [[supergravity]], which stands out as being particularly tractable and well-understood.

But it is expected (cf. [AGMOO99](#AharonyGubserMaldacenaOoguriOz99) [p. 60](https://arxiv.org/pdf/hep-th/9905111.pdf#page=61), [Chester 2018](#Chester18), [Chester & Perlmutter 2018 p. 2](#ChesterPerlmutter18)) that the [[duality in string theory|duality]] still applies in the opposite [[large 1/N limit]], now involving on the [[gravity]]-side corrections 

1. from [[perturbative string theory]] (for small [['t Hooft coupling]], there are some checks of such stringy corrections) and 

1. from putative [[M-theory]] (for the full [[non-perturbative effect|non-perturbative]] [[large 1/N limit]], which remains largely unexplored):

{#AdSCFTForSmallN} $\,$

<center>
<div style="margin:-40px 10px 10px 10px;"><img src="https://ncatlab.org/nlab/files/AdSCFTForSmallN-230627.jpg" width="750">
</div>
</center>


> (graphics adapted from *[[schreiber:Anyonic topological order in TED K-theory|SS22]]*)

Notice that for real-world applications such as to the [[confinement]]/[[mass gap]]-problem of [[quantum chromodynamics]], the value of $N$ typically is indeed small (the number of [[color charge|colors]] in [[quantum chromodynamics]] is $N_c = 3$) so that the [[string theory]]/[[M-theory]]-corrections to the [[AdS/QCD correspondence]] are going to be crucial for the full discussion of these applications:

<center>
<a href="/schreiber/files/Schreiber-MTheoryMathematics2020-v200126.pdf#page=8">
<img src="/schreiber/files/ProblemQCDToProblemM230120.jpg" width="670">
</a>
</center> 

In lack of a full formulation of [[M-theory]] (see [M-theory -- The open problem](M-theory#TheOpenProblem)) approximate forms of the AdS/CFT correspondence away from the case of [[conformal invariance]], [[supersymmetry]], [[large N limit]] and/or exact [[anti de Sitter spacetime|anti de Sitter geometry]] are being argued to be of use for understanding [[quantum chromodynamics]] (for instance the [[quark-gluon plasma]] ([Policastro-Son-Starinets 01](#PolicastroSonStarinets01), but most notably [[confinement|confined]] [[hadron]]-spectra -- the _[[AdS/QCD correspondence]]_) and for various models in [[solid state physics]] (the _[[AdS-CFT in condensed matter physics]]_, see e.g. [Hartnoll-Lucas-Sachdev 16](#HartnollLucasSachdev16)).

More in detail, since the [[near horizon geometry]] of [[BPS state|BPS]] [[black branes]] is conformal to the [[Cartesian product]] of [[anti de Sitter spaces]] with the unit $n$-sphere around the brane, the [[cosmology]] of [[intersecting D-brane models]] realizes the [[observable universe]] on the [[asymptotic boundary]] of an _approximately_ [[anti de Sitter spacetime]] (see for instance [Kaloper 04](#Kaloper04), [Flachi-Minamitsuji 09](#FlachiMinamitsuji09)). The basic structure is hence that of _[[Randall-Sundrum models]]_, but details differ, such as notably in _warped throat_ geometries, see [Uranga 05, section 18](#Uranga05). 

These warped throat models go back to [Klebanov-Strassler 00](#KlebanovStrassler00) which discusses aspects of [[confinement]] in [[Yang-Mills theory]] on conincident ordinary and _[[fractional D-brane|fractional]]_ [[D3-branes]] at the [[singularity]] of a warped [[conifold]]. See also [Klebanov-Witten 98](#KlebanovWitten98)

<center>
<img src="https://ncatlab.org/nlab/files/KlebanovStrassler.jpg" width="640">
</center>

> snippet grabbed from [Uranga 05, section 18](#Uranga05)

> here: "RS"=[[Randall-Sundrum model]]; "KS"=[Klebanov-Strassler 00](#KlebanovStrassler00)

In particular this means that AdS-CFT duality applies in _some approximation_ to [[intersecting D-brane models]] (e.g. [Soda 10](#Soda10), [GHMO 16](#GHMO16)), thus allowing to compute, to some approximation, [[non-perturbative effects]] in the [[Yang-Mills theory]] on the intersecting branes in terms of [[gravity]] on the ambient warped throat $\sim$ [[anti de Sitter spacetime|AdS]] ([Klebanov-Strassler 00, section 6](#KlebanovStrassler00))


### Matching single trace observables to string excitation

The [[single trace operators]]/observables in [[conformal field theories]] such as [[super Yang-Mills theories]] play a special role in the [[AdS-CFT correspondence]]: They correspond to single [[string]] excitations on the [[AdS spacetime|AdS]]-[[supergravity]] side of the correspondence, where, curiously, the "string of characters/letters" in the argument of the trace gets literally mapped to a [[superstring]] in [[spacetime]] (see the references [below](#ReferencesRelationToStringExcitations)).

From [Polyakov 02](#Polyakov02), referring to gauge fields and their [[single trace operators]] as _letter_ and _words_, respectively:

> The picture which slowly arises from the above considerations is that of the space-time gradually disappearing in the regions of large curvature. The natural description in this case is provided by a gauge theory in which the basic objects are the texts formed from the gauge-invariant words. The theory provides us with the expectation values assigned to the various texts, words and sentences.


> These expectation values can be calculated either from the gauge theory or from the strongly coupled 2d sigma model. The coupling in this model is proportional to the target space curvature. This target space can be interpreted as a usual continuous space-time only when the curvature is small. As we increase the coupling, this interpretation becomes more and more fuzzy and finally completely meaningless. 

From [Berenstein-Maldacena-Nastase 02](#BerensteinMaldacenaNastase02), who write $Z$ for the elementary [[field observables]] ("letters") $\mathbf{\Phi}$ above:

> In summary, the "string of $Z$s" becomes the physical string and that each $Z$ carries one unit of $J$ which is one unit of $p_+$. Locality along the worldsheet of the string comes from the fact that planar diagrams allow only contractions of neighboring operators. So the Yang Mills theory gives a [[string bit model]] where each bit is a $Z$ operator. 

On the [[CFT]] side these _[[BMN operators]]_ of fixed length (of "letters") are usefully identified as  [[spin chains]] which, with the [[dilatation operator]] regarded as their [[Hamiltonian]], are [[integrable systems]] ([Minahan-Zarembo 02](#MinahanZarembo02), [Beisert-Staudacher 03](#BeisertStaudacher03)).

This integrability allows a detailed matching between 

* [[single trace operators]]/[[BMN operators]] in [[D=4 N=4 super Yang-Mills theory]] 

* the [[classical field theory|classical]] [[Green-Schwarz superstring]] on [[anti de Sitter spacetime|AdS5]] $\times$ [[5-sphere|S5]]

under [[AdS/CFT duality]] ([Beisert-Frolov-Staudacher-Tseytlin 03](#BeisertFrolovStaudacherTseytlin03), ...). For review see [BBGK 04](#BBGK04), [Beisert et al. 10](#BeisertEtAl10).

(...)


\linebreak


[[!include Polyakov gauge-string duality -- section]]



## Checks
 {#Checks}

At the heart of the duality is the observation that the classical [[action functionals]] for various [[field (physics)|fields]] coupled to [[Einstein gravity]] on [[anti de Sitter spacetime]] are, when expressed as [[functions]] of the [[asymptotic boundary]] values of the [[field (physics)|fields]], equal to the [[generating functions]] for the [[correlators]]/[[n-point functions]] of a [[conformal field theory]] on that asymptotic boundary. 

These computations were laid out in [Witten 98, section 2.4 "Some sample computation"](#Witten98). These follow from elementary manipulation in [[differential geometry]] (involving neither [[supersymmetry]] nor [[string theory]]). A good exposition is in [Hartnoll-Lucas-Sachdev 16, Section 1.6](#HartnollLucasSachdev16)

For the more ambitious matching of the spectrum of the dilatation operator of [[N=4 D=4 super Yang-Mills theory]] to the corresponding spectrum of the [[Green-Schwarz superstring]] on the [[super anti de Sitter spacetime]] $AdS_5 \times S^5$ detailed checks are summarized in [Beisert et al. 10](#BeisertEtAl10), [Escobedo 12](#Escobedo12)


<center>
<img src="https://ncatlab.org/nlab/files/AdSCFTFrolovTseytlinLimitCheck.jpg" width="600">
</center>

> graphics grabbed from [Escobedo 12](#Escobedo12) 

Comparison to [[string scattering amplitudes]] beyond the planar SCFT limit: [ABP 18](#ABP18).

Numerical checks using [[lattice gauge theory]] are reviewed in [Joseph 15](#Joseph15).

Exact duality checks pertaining to the full stringy regime for [[AdS3-CFT2|$AdS_3/CFT_2$]]: [Eberhardt-Gaberdiel 19a](#EberhardtGaberdiel19a), [Eberhardt-Gaberdiel 19b](#EberhardtGaberdiel19b), [Eberhardt-Gaberdiel-Gopakumar 19](#EberhardtGaberdielGopakumar19). For more see the references [there](AdS3-CFT2+and+CS-WZW+correspondence#ReferencesAdS3CFT2).

See also

* Umut Gursoy, Guim Planella Planas, *Worldsheet from worldline* &lbrack;[arXiv:2311.10142](https://arxiv.org/abs/2311.10142)&rbrack;


## Examples

The solutions to [[supergravity]] that preserve the maximum of 32 [[supersymmetries]] are (e.g. [HEGKS 08 (1.1)](BPS+state#HEGKS08))

* $AdS_5 \times S^5$ in [[type II supergravity]]

* $AdS_7 \times S^4$ in [[11-dimensional supergravity]]

* $AdS_4 \times S^7$ in [[11-dimensional supergravity]]

as well as their [[Minkowski spacetime]] and plane wave limits. These are the main [[KK-compactifications]] for the following examples-


### $AdS_5 / CFT_4$ -- Horizon limit of D3-branes
 {#AdS5CFT4}

[[type II string theory]] on 5d [[anti de Sitter spacetime]] (times a 5-sphere) is dual to [[N=4 D=4 super Yang-Mills theory]] on the [[worldvolume]] of a [[D3-brane]] at the [[asymptotic boundary]]

([Maldacena 97, section 2](#Maldacena97a))

([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 3 and 4](#AharonyGubserMaldacenaOoguriOz99))

### $AdS_7 / CFT_6$ -- Horizon limit of M5-branes
 {#AdS7CFT6}

We list some of the conjectured statements and their evidence concerning the case of $AdS_7/CFT_6$-duality.

The hypothesis of [Maldacena 1997, section 3.1](#Maldacena97a) (for review see ([Aharony, Gubser, Maldacena, Ooguri & Oz 1999, section 6.1.1](#AharonyGubserMaldacenaOoguriOz99)) 
is that 

* the [[6d (2,0)-superconformal QFT]] on the [[worldvolume]] of $N$ coincident [[M5-branes]] 

is holographically related to 

* [[11-dimensional supergravity]] [[Kaluza-Klein mechanism|reduced on]] the 4-[[sphere]] $S^4$ with $N$ units of [[flux]] of the [[supergravity C-field]] to [[7d supergravity]] on an asymptotically [[anti de Sitter spacetime]].

In 

* {#WittenI} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_ J. Geom. Phys.22:103-133,1997 ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))
 
effectively this relation was already used to computed the 5-brane [[partition function]] in the abelian case from the states of abelian [[7d Chern-Simons theory]]. (The quadratic refinement of the [[supergravity C-field]] necessary to make this come out right is what led to [[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins-Singer 02]] and hence to the further mathematical development of [[differential cohomology]] and its application in physics.)

In ([Witten 98, section 4](#Witten98)) this construction is argued for from within the framework of AdS/CFT, explicitly identifying the [[7d Chern-Simons theory]] here with the compactification of the 11-dimensional Chern-Simons term of the [[supergravity C-field]] in [[11-dimensional supergravity]], which locally is

$$
  \begin{aligned}
    S_{11d SUGRA, CS}(C_3)
    &=
    \int_{AdS_7} \int_{S^4} C_3 \wedge G_4 \wedge G_4
    \\
    & = N \, \int_{AdS_7} C_3 \wedge G_4
   \end{aligned}
   \,.
$$

But in fact the [[quantum anomaly]] cancellation ([[Green-Schwarz mechanism|GS-type mechanism]]) for 11d sugra introduces a quantum correction to this Chern-Simons term ([DLM, equation (3.14)](\DLM)), making it locally become

$$
  \begin{aligned}
    S(\omega,C_3)
    &=
    \int_{AdS_7} \int_{S^4} C_3 \wedge G_4 \wedge (G_4 + I_8(\omega))
    \\
    & = N \, \int_{AdS_7}
    \left(
       C_3 \wedge G_4
       +
       \frac{1}{48} CS_{p_2}(\omega) - 
        \frac{1}{12} CS_{\frac{1}{2}p_1}(\omega)
        \wedge tr(F_\omega \wedge \omega)
    \right)
   \end{aligned}
   \,,
$$

where now $\omega$ is the local 1-form representative of a [[spin connection]] and where $CS_{p_2}$ is a [[Chern-Simons form]] for the second [[Pontryagin class]] and $CS_{\frac{1}{2}p_1}$ for the first.

That therefore not an abelian, but this _nonabelian_ [[higher dimensional Chern-Simons theory]] should be dual to the nonabelian [[6d (2,0)-superconformal QFT]] was maybe first said explicitly in ([LuWang 2010](#LuWang)).

Its gauge field is hence locally and ignoring the flux quantization subtleties a pair consisting of the abelian 3-form field $C$ and a [[Spin group]] $Spin(6,1)$-valued [[connection on a bundle|connection]] (see _[[supergravity C-field]] for global descriptions of such pairs). Or maybe rather  $Spin(6,2)$ to account for the constraint that the configurations are to be asymptotic [[anti de Sitter spacetimes]] (in analogy to the well-understood situation in [[3d quantum gravity]], see there for more details).


{#CommentSezginSundell} Indeed, in [Sezgin &Sundell 2002, section 7](#SezginSundell) more detailed arguments are given that the 7-dimensional dual to the free 6d theory is a [[higher spin gauge theory]] for a higher spin [[gauge group]] extending the ([[superconformal group|super]]) [[conformal group]] $SO(6,2)$.

A [[non-perturbative quantum field theory|non-perturbative]] description of this nonabelian [[7d Chern-Simons theory]] as a [[local prequantum field theory]] (hence defined [[non-perturbative quantum field theory|non-perturbatively]] on the global [[moduli stack]] of [[field (physics)|fields]] ([[twisted differential string structures]], in fact)) was discussed in ([FSS 12a](#FSS12a), [FSS 12b](#FSS12b)).

General discussion of [[boundary field theory|boundary]] [[local prequantum field theories]] relating higher Chern-Simons-type and higher WZW-type theories is in ([[schreiber:differential cohomology in a cohesive topos|dcct 13, section 3.9.14]]). Specifically, a characterization along these lines of the [[Green-Schwarz action functional]] of the [[M5-brane]] as a holographic [[infinity-Wess-Zumino-Witten theory - contents|higher WZW-type]] boundary theory of a 7d Chern-Simons theory is found in ([FSS 13](#FSS13)).

Analogous discussion of the 6d theory as a higher WZW analog of a 7d Chern-Simons theory phrased in terms of [[extended quantum field theory]] is ([[4-3-2 8-7-6|Freed 12]]).

### $AdS_4 / CFT_3$ --Horizon limit of M2-branes
 {#AdS4CFT3}

[[11d supergravity]]/[[M-theory]] on the asymptotic $AdS_4$
spacetime of an [[M2-brane]].

([Maldacena 97, section 3.2](#Maldacena97a), [Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 6.1.2](#AharonyGubserMaldacenaOoguriOz99), [Klebanov-Torri 10](KlebanovTorri10))






### $AdS_3 / CFT_2$ -- Horizon limit of D$p$-D($p+k$) brane bound states
 {#AdS3CFT2}

(for more see at _[[AdS3-CFT2 and CS-WZW correspondence]]_)


[[D1-D5 brane system]] in [[type IIB string theory]]

([Maldacena 97, section 4](#Maldacena97a))

([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 5](#AharonyGubserMaldacenaOoguriOz99))

[[D6-D8 brane bound state]] with [[D2-D4 brane bound state]] [[defect QFT|defects]] in [[massive type IIA string theory]]

([Dibitetto-Petri 17](#DibitettoPetri17), ...) 

[[D4-D8 brane bound state]] with [[D2-D6 brane bound state]] [[defect QFT|defects]] in [[massive type IIA string theory]]

([Dibitetto-Petri 18](#DibitettoPetri18), ...)

### $AdS_2 / CFT_1$
 {#AdS2CFT1}

see at _[[nearly AdS2/CFT1]]_



### Non-conformal duals

#### Horizon limit of $Dp$-branes for arbitrary $p$

([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 6.1.3](#AharonyGubserMaldacenaOoguriOz99))


#### Horizon limit of NS5-brane

([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 6.1.4](#AharonyGubserMaldacenaOoguriOz99))


#### QCD models

While all of the above horizon limits product [[super Yang-Mills theory]], one can consider certain limits of these in which they look like plain [[QCD]], at least in certain sectors. This leads to a discussion of holographic description of QCD properties that are actually experimentally observed. 

([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 6.2](#AharonyGubserMaldacenaOoguriOz99))

See the _[References -- Applications -- In condensed matter physics](#ToCondensedMatterPhysics)_.



### Further gauge theories induced by compactification and twisting

[[!include gauge theory from AdS-CFT -- table]]



## Formalizations

The full formalization of AdS/CFT is still very much out of reach, but maybe mostly for lack of trying. 

But see [Anderson 04](#Anderson04).

One proposal for a formalization of a toy version in the context of [[AQFT]] is [[Rehren duality]]. However, it does not seem that this actually formalizes AdS-CFT, but something else.


## Related concepts

* [[near-horizon geometry]]

* [[Fefferman-Graham ambient construction]]

* [[holographic entanglement entropy]], [[ER = EPR]]

* [[single trace operator]]

* [[duality in physics]], [[duality in string theory]]

  * [[T-duality]], [[S-duality]], [[U-duality]]

  * [[open/closed string duality]]

     * [[KLT relations]]

* [[black hole in anti de Sitter spacetime]]

* [[S-matrix theory]]

* [[anti de Sitter gravity]]

* [[Randall-Sundrum model]]

* [[Sachdev-Ye-Kitaev model]]

* [[flat space holography]]

* [[p-adic AdS-CFT]]

* [[dS/CFT correspondence]]

[[!include table of branes]]

\linebreak




## References
 {#References}

Long before the modern formulation of the AdS/CFT correspondence, referenced below at

* *[The origin of modern AdS/CFT duality](#ReferencesOriginModernAdSCFTDUality)*

there were developments that must be regarded at least as precursors, referenced at

* *[Polyakov gauge-string duality](#PolyakovGaugeStringDualityReferences)*

* *[Microscopic AdS-CFT via p-brane sigma-models](#ReferencesMicroscopicAdSCFTViapBraneSigmaModesl)*




[[!include Polyakov gauge-string duality -- references]]





[[!include microscopic AdS-CFT via p-brane sigma-models -- references]]





### The origin of modern AdS/CFT duality
 {#ReferencesOriginModernAdSCFTDUality}

The modern guise of AdS/CFT duality as a conjectured [[duality in string theory|duality]] between [[string theory|string]]/[[M-theory]] [[near horizon geometry|near]] [[black branes]] and  [[superconformal field theories]] *on* the [[worldvolume]] of these branes, at least in a suitable [[large-N limit]], is due to:

* {#Maldacena97a} [[Juan Maldacena]], _The Large $N$ limit of superconformal field theories and supergravity_, Adv. Theor. Math. Phys. **2** (1998) 231 &lbrack;[hep-th/9711200](http://arxiv.org/abs/hep-th/9711200), [doi:10.4310/ATMP.1998.v2.n2.a1](https://doi.org/10.4310/ATMP.1998.v2.n2.a1), [inspire:451647](https://inspirehep.net/literature/451647)&rbrack;

* {#Maldacena97b} [[Juan Maldacena]], _Wilson loops in Large $N$ field theories_, Phys. Rev. Lett. **80** (1998) 4859 &lbrack;[hep-th/9803002](http://arxiv.org/abs/hep-th/9803002), [doi:10.1103/PhysRevLett.80.4859](https://doi.org/10.1103/PhysRevLett.80.4859)&rbrack;


An  actual rule for matching, under this [[duality in string theory|duality]], [[bulk field theory|bulk]] [[states]] to [[generating functions]] for [[boundary field theory|boundary]] [[correlators]]/[[n-point functions]] was then given by

* {#GubserKlebanovPolyakov98} [[Steven Gubser]], [[Igor Klebanov]], [[Alexander Polyakov]], around (12) of: *Gauge theory correlators from non-critical string theory*, Physics Letters B **428** 105-114 (1998) &lbrack;[hep-th/9802109](http://arxiv.org/abs/hep-th/9802109), <a href="https://doi.org/10.1016/S0370-2693(98)00377-3">doi:10.1016/S0370-2693(98)00377-3</a>&rbrack;

* {#Witten98} [[Edward Witten]], around (2.11) of _Anti-de Sitter space and holography_, Advances in Theoretical and Mathematical Physics **2** (1998) 253-291 &lbrack;[hep-th/9802150](http://arxiv.org/abs/hep-th/9802150), [doi:10.4310/ATMP.1998.v2.n2.a2](https://dx.doi.org/10.4310/ATMP.1998.v2.n2.a2), [spire:467400](https://inspirehep.net/literature/467400)&rbrack;

now often called "the holographic disctionary" or just "the dictionary" (e.g. [Taylor 2023](#Taylor23)).

See also:

* Wikipedia, _[AdS/CFT correspondence](http://en.wikipedia.org/wiki/AdS/CFT_correspondence)_

* [[Tom Banks]], [[Michael Douglas]], [[Gary Horowitz]], [[Emil Martinec]], _AdS Dynamics from Conformal Field Theory_ ([arXiv:hep-th/9808016](https://arxiv.org/abs/hep-th/9808016), [spire:474214](http://inspirehep.net/record/474214))

* {#Giraldo12} Carlos Andrés Cardona Giraldo, _Correlation functions in AdS/CFT correspondence_, 2012 ([spire:1652794](inspirehep.net/record/1652794), [pdf](https://digital.bl.fcen.uba.ar/download/tesis/tesis_n5179_CardonaGiraldo.pdf))



Sketch of a derivation of AdS/CFT:

* {#Nastase18} [[Horatiu Nastase]], _Towards deriving the AdS/CFT correspondence_ ([arXiv:1812.10347](https://arxiv.org/abs/1812.10347))

* [[Ofer Aharony]], [[Shai Chester]], [[Erez Urbach]], _A Derivation of AdS/CFT for Vector Models_ ([arXiv:2011.06328](https://arxiv.org/abs/2011.06328))



See also:
 

* [[Edward Witten]], _Three-dimensional gravity revisited_, [arxiv/0706.3359](http://arxiv.org/abs/0706.3359)

* C. R. Graham, [[Edward Witten]], _Conformal anomaly of submanifold observables in AdS/CFT correspondence_, [hepth/9901021](http://arxiv.org/abs/hep-th/9901021).

* [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012))

Via [[exceptional field theory]]:

* [[Oscar Varela]]: _Super-Chern-Simons spectra from Exceptional Field Theory_, J. High Energ. Phys. **2021** 283 (2021) &lbrack;[arXiv:2010.09743](https://arxiv.org/abs/2010.09743), <a href="https://doi.org/10.1007/JHEP04(2021)283">doi:10.1007/JHEP04(2021)283</a>&rbrack;


### Introductions and surveys


* [[Edward Witten]], *Baryons and Branes in Anti de Sitter Space* talk at *[String98](https://online.kitp.ucsb.edu/online/strings98/)* (1998) &lbrack;[web](https://online.kitp.ucsb.edu/online/strings98/witten/)&rbrack;
  > (by the title, apparently originally intended to touch on [[AdS-QCD]], but de facto ending with focus on the problem of [[flat space holography]])

* [[Alexander Polyakov]], *The wall of the cave*, Int. J. Mod. Phys. A **14** (1999) 645-658 &lbrack;[arXiv:hep-th/9809057](https://arxiv.org/abs/hep-th/9809057), [doi:10.1142/S0217751X99000324](https://doi.org/10.1142/S0217751X99000324)&rbrack;
  > (early account with focus on [[AdS-QCD duality]])

* [[John Schwarz]], *Introduction to M Theory and AdS/CFT Duality*, in: *Quantum Aspects of Gauge Theories, Supersymmetry and Unification* Lecture Notes in Physics **525**, Springer (1999)  &lbrack;[arXiv:hep-th/9812037](https://arxiv.org/abs/hep-th/9812037), [doi:10.1007/BFb0104239](https://doi.org/10.1007/BFb0104239)&rbrack;
  >  (early review with an eye towards [[M-theory]])

* [[Jens L. Petersen]], _Introduction to the Maldacena Conjecture on AdS/CFT_, Int. J. Mod. Phys. A **14** (1999) 3597-3672 &lbrack;[hep-th/9902131](http://arxiv.org/abs/hep-th/9902131), [doi:10.1142/S0217751X99001676](http://dx.doi.org/10.1142/S0217751X99001676)&rbrack;

* {#AharonyGubserMaldacenaOoguriOz99} [[Ofer Aharony]], [[Steven Gubser]], [[Juan Maldacena]], [[Hirosi Ooguri]], [[Yaron Oz]], _Large $N$ Field Theories, String Theory and Gravity_, Phys. Rept. **323**  183-386 (2000) &lbrack;<a href="https://doi.org/10.1016/S0370-1573(99)00083-6">doi:10.1016/S0370-1573(99)00083-6</a>, [arXiv:hep-th/9905111](http://arxiv.org/abs/hep-th/9905111)&rbrack;

* [[Jan de Boer]], *Introduction to AdS/CFT correspondence*, talk at [SUSY02](http://www-library.desy.de/preparch/desy/proc/proc02-02/SUSY-Start.html) (2002) &lbrack;[pdf](http://www-library.desy.de/preparch/desy/proc/proc02-02/Proceedings/pl.6/deboer_pr.pdf), [[deBoer-IntroAdSCFT.pdf:file]]&rbrack;

* {#Anderson04} Michael T. Anderson, _Geometric aspects of the AdS/CFT correspondence_ &lbrack;[arXiv:hep-th/0403087](https://arxiv.org/abs/hep-th/0403087)&rbrack;

* [[Christopher P. Herzog]], [[Igor R. Klebanov]]: *AdS/CFT Correspondence*, Encyclopedia of Mathematical Physics, Academic Press (2006) 174-183 &lbrack;[doi:10.1016/B0-12-512666-2/00245-5](https://doi.org/10.1016/B0-12-512666-2/00245-5), [[HerzogKlebanov-AdSCFT.pdf:file]]&rbrack;

* [[Horatiu Nastase]], _Introduction to AdS-CFT_ &lbrack;[arXiv:0712.0689](http://arxiv.org/abs/0712.0689)&rbrack;

* [[Horatiu Nastase]], *Introduction to AdS/CFT correspondence*, Cambridge University Press (2015) &lbrack;[cds:1984145](http://cds.cern.ch/record/1984145), [doi:10.1017/CBO9781316090954](https://doi.org/10.1017/CBO9781316090954)&rbrack;

* [[Gary Horowitz]], [[Joseph Polchinski]], _Gauge/gravity duality_ &lbrack;[gr-qc/0602037](http://arxiv.org/abs/gr-qc/0602037)&rbrack;

* [[Alberto Zaffaroni]], *Introduction to the AdS/CFT correspondence*, [LACES](https://laces.web.cern.ch/LACES19/index19.html) lectures (2009) &lbrack;[pdf](https://laces.web.cern.ch/laces09/notes/dbranes/lezionilosanna.pdf), [[Zaffaroni-AdSCFTLectures.pdf:file]]&rbrack;

* [[Hans Günter Dosch]], *A Practical Guide to AdS/CFT*, lecture notes (2009) &lbrack;[pdf](https://www.thphys.uni-heidelberg.de/~dosch/wuhantot.pdf), [[Dosch-AdSCFT.pdf:file]]&rbrack;
  > (with aspects of *[[holographic QCD]]*)

* [[Joseph Polchinski]], _Introduction to Gauge/Gravity Duality_ ([arXiv:1010.6134](https://arxiv.org/abs/1010.6134))

* {#Herzog15} [[Christopher Herzog]], *AdS/CFT*, lecture notes (2015) &lbrack;[pdf](http://insti.physics.sunysb.edu/~cpherzog/stringtheory/AdSCFT.pdf), [[Herzog-AdSCFT.pdf:file]]&rbrack;

* {#Natsuume15} [[Makoto Natsuume]], *AdS/CFT Duality User Guide*, Lecture Notes in Physics **903**, Springer (2015) &lbrack;[arXiv:1409.3575](https://arxiv.org/abs/1409.3575), [doi:10.1007/978-4-431-55441-7](https://doi.org/10.1007/978-4-431-55441-7), [webpage](https://research.kek.jp/people/natsuume/ads-real-world.html)&rbrack;

* [[Sebastian De Haro]], Daniel R. Mayerson, [[Jeremy Butterfield]], *Conceptual Aspects of Gauge/Gravity Duality*, Foundations of Physics **46** 11 (2016) 1381-1425 &lbrack;[arXiv:1509.09231](https://arxiv.org/abs/1509.09231), [doi:10.1007/s10701-016-0037-4](https://doi.org/10.1007/s10701-016-0037-4)&rbrack;

* {#Erdmenger18} [[Johanna Erdmenger]], _Introduction to Gauge/Gravity Duality_, PoS [TASI2017](https://inspirehep.net/conferences/1591386) (2018) 001 &lbrack;[arXiv:1807.09872](https://arxiv.org/abs/1807.09872), [doi:10.22323/1.305.0001](https://doi.org/10.22323/1.305.0001)&rbrack;
  > (focus on [[holographic entanglement entropy]] and [[AdS/CMT duality]])

* [[Matteo Baggioli]]: *Applied Holography -- A Practical Mini-Course*, Springer Briefs in Physics, Springer (2019) &lbrack;[doi:10.1007/978-3-030-35184-7](https://doi.org/10.1007/978-3-030-35184-7)&rbrack;

* Nirmalya Kajuri, *ST4 Lectures on Bulk Reconstruction* &lbrack;[arXiv:2003.00587](https://arxiv.org/abs/2003.00587)&rbrack;

* [[Francesco Benini]]: *Brief Introduction to AdS/CFT* SISSA lecture (2022) &lbrack;[pdf](https://www.sissa.it/tpp/phdsection/OnlineResources/16/SISSA_AdSCFT_course2022.pdf), [[Benini-AdSCFTLecture.pdf:file]]&rbrack; 

* {#Taylor23} Marika Taylor, *Introduction to AdS/CFT and Holography -- The holographic dictionary*, lecture at *pre-SUSY school 2023* &lbrack;[cern:1214657](https://indico.cern.ch/event/1214657), slides: [pdf](https://indico.cern.ch/event/1214657/sessions/480000/attachments/2690349/4676064/susy1.pdf), video: [session 1](https://southampton.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=0f0a6c21-0bc9-42ae-9274-b03e00a8fde3), [sessions 2, 3](https://southampton.cloud.panopto.eu/Panopto/Pages/Viewer.aspx?id=c7e64fe5-675c-4f94-96f2-b03f0083f0d3)&rbrack;


Review of [[Yangian]] symmetry:

* [[Alessandro Torrielli]], _Yangians, S-matrices and AdS/CFT_, J. Phys. A **44** 263001 (2011) &lbrack;[arXiv:1104.2474](http://arxiv.org/abs/1104.2474)&rbrack;

### Lattice gauge theory computations

Review of [[lattice gauge theory]]-numerics for the [[AdS-CFT correspondence]]:

* {#Joseph15} Anosh Joseph, _Review of Lattice Supersymmetry and Gauge-Gravity Duality_
([arXiv:1509.01440](https://arxiv.org/abs/1509.01440))

Using the [[KK-compactification]] of [[D=4 N=4 super Yang-Mills theory]] to the [[BMN matrix model]] for [[lattice gauge theory]]-computations in [[D=4 N=4 SYM]] and for numerical checks of the [[AdS-CFT correspondence]]:

* {#HIKNT13} Masazumi Honda, [[Goro Ishiki]], Sang-Woo Kim, Jun Nishimura, Asato Tsuchiya, _Direct test of the AdS/CFT correspondence by Monte Carlo studies of N=4 super Yang-Mills theory_, JHEP 1311 (2013) 200 ([arXiv:1308.3525](https://arxiv.org/abs/1308.3525))


### On single trace operators

The correspondence of [[single trace operators]] to [[superstring]] excitations under the [[AdS-CFT correspondence]] originates with these articles:

* {#Polyakov02} [[Alexander Polyakov]], _Gauge Fields and Space-Time_, Int. J. Mod. Phys. A17S1 (2002) 119-136 &lbrack;[arXiv:hep-th/0110196](https://arxiv.org/abs/hep-th/0110196), [doi:10.1142/S0217751X02013071](https://doi.org/10.1142/S0217751X02013071)&rbrack;

* {#BerensteinMaldacenaNastase02} [[David Berenstein]], [[Juan Maldacena]], [[Horatiu Nastase]], _Strings in flat space and pp waves from $\mathcal{N} = 4$ Super Yang Mills_, JHEP 0204 (2002) 013 ([arXiv:hep-th/0202021](https://arxiv.org/abs/hep-th/0202021))

  (whence "[[BMN operators]]")

* [[Steven Gubser]], [[Igor Klebanov]], [[Alexander Polyakov]], *A semi-classical limit of the gauge/string correspondence*, Nucl. Phys. B **636** (2002) 99-114 &lbrack;[arXiv:hep-th/0204051](https://arxiv.org/abs/hep-th/0204051), <a href="https://doi.org/10.1016/S0550-3213(02)00373-5">doi:10.1016/S0550-3213(02)00373-5</a>&rbrack;


* {#Kruczenski04} [[Martin Kruczenski]], _Spiky strings and single trace operators in gauge theories_, JHEP 0508:014, 2005 ([arXiv:hep-th/0410226](https://arxiv.org/abs/hep-th/0410226))

The identification of the relevant [[single trace operators]] with [[integrable system|integrable]] [[spin chains]] is due to

* {#MinahanZarembo02}  J. A. Minahan, [[Konstantin Zarembo]], _The Bethe-Ansatz for $N=4$ Super Yang-Mills_, JHEP 0303 (2003) 013 ([arXiv:hep-th/0212208](https://arxiv.org/abs/hep-th/0212208))

* {#BeisertStaudacher03} [[Niklas Beisert]], [[Matthias Staudacher]], _The $\mathcal{N}=4$ SYM Integrable Super Spin Chain_, 
Nucl. Phys. B670:439-463, 2003 ([arXiv:hep-th/0307042](https://arxiv.org/abs/hep-th/0307042))

which led to more detailed matching of [[single trace operators]] to rotating string excitations in

* {#BeisertFrolovStaudacherTseytlin03} [[Niklas Beisert]], [[Sergey Frolov]], [[Matthias Staudacher]], [[Arkady Tseytlin]], _Precision Spectroscopy of AdS/CFT_, JHEP 0310:037, 2003 ([arXiv:hep-th/0308117](https://arxiv.org/abs/hep-th/0308117))

Review includes

* {#BBGK04} A. V. Belitsky, [[Volker Braun]], A. S. Gorsky, G. P. Korchemsky, _Integrability in QCD and beyond_, Int. J. Mod. Phys. A19:4715-4788, 2004 ([arXiv:hep-th/0407232](https://arxiv.org/abs/hep-th/0407232))

* {#BeisertEtAl10} [[Niklas Beisert]], [[Luis Alday]], [[Radu Roiban]], [[Sakura Schafer-Nameki]], [[Matthias Staudacher]], [[Alessandro Torrielli]], [[Arkady Tseytlin]], et. al., _Review of AdS/CFT Integrability: An Overview_, Lett. Math. Phys. 99, 3 (2012) ([arXiv:1012.3982](https://arxiv.org/abs/1012.3982))


[[!include AdS2-CFT1 -- references]]


### On $AdS_3 / CFT_2$
 {#ReferencesAdS3CFT2}

(For more see the references at _[[AdS3/CFT2]]_.)


An exact correspondence of the symmetric [[orbifold]] [[CFT]] of [[Liouville theory]] with a string theory on $AdS_3$ is claimed in:

* {#EberhardtGaberdiel19a} [[Lorenz Eberhardt]], [[Matthias Gaberdiel]], _String theory on $AdS_3$ and the symmetric orbifold of Liouville theory_ ([arXiv:1903.00421](https://arxiv.org/abs/1903.00421))

* {#EberhardtGaberdiel19b} [[Lorenz Eberhardt]], [[Matthias Gaberdiel]], _Strings on $AdS_3 \times S^3 \times S^3 \times S^1$_ ([arXiv:1904.01585](https://arxiv.org/abs/1904.01585))

* {#EberhardtGaberdielGopakumar19} [[Lorenz Eberhardt]], [[Matthias Gaberdiel]], [[Rajesh Gopakumar]], _Deriving the $AdS_3/CFT_2$ Correspondence_ ([arXiv:1911.00378](https://arxiv.org/abs/1911.00378))

* Andrea Dei, [[Lorenz Eberhardt]], _Correlators of the symmetric product orbifold_ ([arXiv:1911.08485](https://arxiv.org/abs/1911.08485))

based on

* Shouvik Datta, [[Lorenz Eberhardt]], [[Matthias Gaberdiel]], _Stringy $\mathcal{N} = (2,2)$ holography for $AdS_3$_ JHEP 1801 (2018) 146 ([arXiv:1709.06393](https://arxiv.org/abs/1709.06393))

See also

* Stefano Speziali, _Spin 2 fluctuations in 1/4 BPS AdS3/CFT2_ ([arxiv:1910.14390](https://arxiv.org/abs/1910.14390))

* [[Lorenz Eberhardt]], _$AdS_3/CFT_2$ at higher genus_ ([arXiv:2002.11729](https://arxiv.org/abs/2002.11729))

* [[Lorenz Eberhardt]], _Summing over Geometries in String Theory_ ([arXiv:2102.12355](https://arxiv.org/abs/2102.12355))



On [[black brane|black]]$\;$[[D6-D8-brane bound states]] in [[massive type IIA string theory]], with [[defect QFT|defect]] [[D2-D4-brane bound states]] inside them realizing [[AdS3-CFT2]] "inside" [[AdS7-CFT6]]:


* {#DibitettoPetri17} [[Giuseppe Dibitetto]], [[Nicolò Petri]], _6d surface defects from massive type IIA_, JHEP 01 (2018) 039 ([arxiv:1707.06154](https://arxiv.org/abs/1707.06154))

* [[Nicolò Petri]], section 6.5 of: _Supersymmetric objects in gauged supergravities_ ([arxiv:1802.04733](https://arxiv.org/abs/1802.04733))


* {#Petri18} [[Nicolò Petri]], _Surface defects in massive IIA_, talk at [Recent Trends in String Theory and Related Topics](http://physics.ipm.ac.ir/conferences/stringtheory3/) 2018 ([pdf](http://physics.ipm.ac.ir/conferences/stringtheory3/note/N.Petri.pdf))

* [[Giuseppe Dibitetto]], [[Nicolò Petri]], _$AdS_3$ vacua and surface defects in massive IIA_ ([arxiv:1904.02455](https://arxiv.org/abs/1904.02455))


* Yolanda Lozano, Niall T. Macpherson, Carlos Nunez, Anayeli Ramirez, $1/4$ BPS $AdS_3/CFT_2$ ([arxiv:1909.09636](https://arxiv.org/abs/1909.09636))


* Yolanda Lozano, Niall T. Macpherson, Carlos Nunez, Anayeli Ramirez, _Two dimensional $N=(0,4)$ quivers dual to $AdS_3$ solutions in massive IIA_ ([arxiv:1909.10510](https://arxiv.org/abs/1909.10510))


* Yolanda Lozano, Niall T. Macpherson, Carlos Nunez, Anayeli Ramirez, _$AdS_3$ solutions in massive IIA, defect CFTs and T-duality_ ([arxiv:1909.11669](https://arxiv.org/abs/1909.11669))

* Kostas Filippas, _Non-integrability on $AdS_3$ supergravity_ ([arxiv:1910.12981](https://arxiv.org/abs/1910.12981))

On [[black brane|black]]$\;$[[D4-D8-brane bound states]] in [[massive type IIA string theory]], with [[defect QFT|defect]] [[D2-D6-brane bound states]] inside them realizing [[AdS3-CFT2]] "inside" [[AdS7-CFT6]]:

* {#DibitettoPetri18} [[Giuseppe Dibitetto]], [[Nicolò Petri]], _Surface defects in the D4 − D8 brane system_, JHEP 01 (2019) 193 ([arxiv:1807.07768](https://arxiv.org/abs/1807.07768))

* [[Giuseppe Dibitetto]], [[Nicolò Petri]], _$AdS_3$ vacua and surface defects in massive IIA_ ([arxiv:1904.02455](https://arxiv.org/abs/1904.02455))


### On $AdS_4 / CFT_3$

* {#KlebanovTorri10} [[Igor Klebanov]], Giuseppe Torri, _M2-branes and AdS/CFT_,  	Int.J.Mod.Phys.A25:332-350,2010 ([arXiv:0909.1580](http://arxiv.org/abs/0909.1580))
  
* Kazuo Hosomichi, _M2-branes and AdS/CFT: A Review_ ([arXiv:2003.13914](https://arxiv.org/abs/2003.13914))

* Silvia Penati, _Exact Results in AdS4/CFT3_ ([arXiv:2004.00841](https://arxiv.org/abs/2004.00841))

* Manikantt Mummalaneni: *AdS4/CFT3: ABJM Theory, Brane Geometry, Correlators and Mellin Space* &lbrack;[arXiv:2408.11835](https://arxiv.org/abs/2408.11835)&rbrack;



### On $AdS_5 / CFT_4$

* [Beisert et. al. 10](#BeisertEtAl10)

* {#Escobedo12} Jorge Escobedo, _Integrability in AdS/CFT: Exact Results for Correlation Functions_, 2012 ([spire:1264432](http://inspirehep.net/record/1264432))

Computing dual [[string scattering amplitudes]] by AdS/CFT beyond the [[planar limit]]:

* {#ABP18} [[Luis Alday]], [[Agnese Bissi]], [[Eric Perlmutter]], _Genus-One String Amplitudes from Conformal Field Theory_, JHEP06(2019) 010 ([arXiv:1809.10670](https://arxiv.org/abs/1809.10670))


### On $AdS_7 / CFT_6$

We list references specific to $AdS_7/CFT_6$.


In 

* {#WittenI} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_ J. Geom. Phys.22:103-133,1997 ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))
 

* {#Witten98} [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ JHEP 9812:012,1998 ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012)) 
 

it is argued that the [[conformal blocks]] of the [[6d (2,0)-superconformal QFT]] are entirely controled just by the effective [[higher dimensional Chern-Simons theory|7d Chern-Simons theory]] inside [[11-dimensional supergravity]], but only the abelian piece is discussed explicitly.

The fact that this Chern-Simons term is in fact a _nonabelian_ [[higher dimensional Chern-Simons theory]] in $d = 7$, due the [[quantum anomaly]] cancellation, is clear from the original source, equation (3.14) of

* {#DLM} [[Michael Duff]], [[James Liu]], [[Ruben Minasian]], _Eleven Dimensional Origin of String/String Duality: A One Loop Test_ ([arXiv:hep-th/9506126](http://arxiv.org/abs/hep-th/9506126))
  
but seems not to be noted explicitly in the context of $AdS_7/CFT_6$ before the references

* H. L&#252;, Yi Pang, _Seven-Dimensional Gravity with Topological Terms_ Phys.Rev.D81:085016 (2010) ([arXiv:1001.0042](http://arxiv.org/abs/1001.0042))

* {#LuWang} H. Lu, Zhao-Long Wang, _On M-Theory Embedding of Topologically Massive Gravity_ Int.J.Mod.Phys.D19:1197 (2010) ([arXiv:1001.2349](http://arxiv.org/abs/1001.2349))

More on the relation between the [[M5-brane]] and supergravity on $AdS_7 \times S^4$ and arguments for the $SO(5)$ [[R-symmetry]] group on the 6d theory from the 7d theory are given in 

* [[Alexei Nurmagambetov]], I. Y. Park, _On the M5 and the AdS7/CFT6 Correspondence_, Phys. Lett. B524 (2002) 185-191 ([arXiv:hep-th/0110192](http://arxiv.org/abs/hep-th/0110192))

See also 

* M. Nishimura, Y. Tanii, _Local Symmetries in the $AdS_7/CFT_6$ Correspondence_, Mod. Phys. Lett. A14 (1999) 2709-2720 ([arXiv:hep-th/9910192](http://arxiv.org/abs/hep-th/9910192))

  
Discussion of the $CFT_6$ in $AdS_7/CFT_6$ via [[conformal bootstrap]]:

* {#Chester18} [[Shai Chester]], _Bootstrapping M-theory_, PhD thesis, Princeton (2018) &lbrack;[[ChesterBootstrappingMTheory.pdf:file]], [ark:88435/dsp01kw52jb833](http://arks.princeton.edu/ark:/88435/dsp01kw52jb833)&rbrack;

* Nathan B. Agmon, [[Shai Chester]], [[Silviu S. Pufu]]: *Solving M-theory with the Conformal Bootstrap*, J. High Energ. Phys. **2018** 159 (2018). &lbrack;[arXiv:1711.07343](https://arxiv.org/abs/1711.07343), <a href="https://doi.org/10.1007/JHEP06(2018)159">doi:10.1007/JHEP06(2018)159</a>&rbrack;

* {#ChesterPerlmutter18} [[Shai Chester]], [[Eric Perlmutter]]: *M-Theory Reconstruction from $(2,0)$ CFT and the Chiral Algebra Conjecture*, J. High Energ. Phys. **2018** 116 (2018) &lbrack;[arXiv:1805.00892](https://arxiv.org/abs/1805.00892), <a href="https://doi.org/10.1007/JHEP08(2018)116">doi:10.1007/JHEP08(2018)116</a>&rbrack;

* [[Luis Alday]], [[Shai Chester]], Himanshu Raj, _6d $(2,0)$ and M-theory at 1-loop_ ([arXiv:2005.07175](https://arxiv.org/abs/2005.07175))




In 

* {#SezginSundell} [[Ergin Sezgin]], P. Sundell, _Massless Higher Spins and Holography_ ([hep-th/0205131](http://arxiv.org/abs/hep-th/0205131))
 
arguments are given that the 7d theory is a [[higher spin gauge theory]] extension of $SO(6,2)$.


### Generalization beyond exact AdS / exact CFT

Discussion for [[cosmology]] of [[intersecting D-brane models]] (ambient $\sim$ [[anti de Sitter spacetimes]] with the $\sim$ conformal intersecting branes at the [[asymptotic boundary]]) includes the following (see also at _[[Randall-Sundrum model]]_):

* {#KlebanovStrassler00} [[Igor Klebanov]], [[Matthew Strassler]], _Supergravity and a Confining Gauge Theory: Duality Cascades and $\chi^{SB}$-Resolution of Naked Singularities_, JHEP 0008:052, 2000 ([arXiv:hep-th/0007191](https://arxiv.org/abs/hep-th/0007191))

* {#KlebanovWitten98} [[Igor Klebanov]], [[Edward Witten]], _Superconformal Field Theory on Threebranes at a Calabi-Yau Singularity_, Nucl.Phys.B536:199-218, 1998 ([arXiv:hep-th/9807080](https://arxiv.org/abs/hep-th/9807080))

* {#Kaloper04} Nemanja Kaloper, _Origami World_, JHEP 0405 (2004) 061 ([arXiv:hep-th/0403208](https://arxiv.org/abs/hep-th/0403208))

* {#Uranga05} [[Angel Uranga]], section 18 of _TASI lectures on String Compactification, Model Building, and Fluxes_, 2005 ([pdf](http://cds.cern.ch/record/933469/files/cer-002601054.pdf))

* {#FlachiMinamitsuji09} Antonino Flachi, Masato Minamitsuji, _Field localization on a brane intersection in anti-de Sitter spacetime_, Phys.Rev.D79:104021, 2009 ([arXiv:0903.0133](https://arxiv.org/abs/0903.0133))

* {#Soda10} Jiro Soda, _AdS/CFT on the brane_, Lect.Notes Phys.828:235-270, 2011 ([arXiv:1001.1011](https://arxiv.org/abs/1001.1011))


* {#Teraguchi07} Shunsuke Teraguchi, around slide 21 _String theory and its relation to particle physics_, 2007 ([pdf](http://phys.cts.ntu.edu.tw/ppp7/talks/PPP7_Shunsuke_Teraguchi.pdf))

* {#GHMO16} Gianluca Grignani, Troels Harmark, Andrea Marini, Marta Orselli, _The Born-Infeld/Gravity Correspondence_, Phys. Rev. D 94, 066009 (2016) ([arXiv:1602.01640](https://arxiv.org/abs/1602.01640))


[[!include pp-waves as Penrose limits of AdS spacetimes -- references]]



### Applications to physics
 {#Appications}


#### To gravity

Discussion of [[event horizons]] of [[black holes]] in terms of AdS/CFT (the "[[firewall problem]]") is in

* Kyriakos Papadodimas, Suvrat Raju, _An Infalling Observer in AdS/CFT_ ([arXiv:1211.6767](http://arxiv.org/abs/1211.6767))

To [[black hole]] interiors:

* [[Juan Maldacena]], _Toy models for black holes II_, talk at PiTP 2018 _From QBits to spacetime_ ([recording](https://video.ias.edu/PiTP/2018/0726-JuanMaldacena))

> The [[SYK model]] gives us a glimpse into the interior of an [[extremal black hole]]...That's the feature of SYK that I find most interesting...It is a feature this model has, that I think no other model has


To [[symmetries]] in gravity:

* {#HarlowOoguri18} [[Daniel Harlow]], [[Hirosi Ooguri]], _Constraints on symmetry from holography_, Phys. Rev. Lett. 122, 191601, 2019 ([arXiv:1810.05337](https://arxiv.org/abs/1810.05337), [doi:10.1103/PhysRevLett.122.191601](https://doi.org/10.1103/PhysRevLett.122.191601))

#### To the quark-gluon plasma

Applications of AdS-CFT to the [[quark-gluon plasma]] of [[QCD]]:



Expositions and reviews:

* Pavel Kovtun, _Quark-Gluon Plasma and String Theory_, RHIC news (2009) ([blog entry](http://www.bnl.gov/rhic/news/091107/story2.asp))

* Makoto Natsuume, _String theory and quark-gluon plasma_ ([arXiv:hep-ph/0701201](http://arxiv.org/abs/hep-ph/0701201))

* [[Steven Gubser]], _Using string theory to study the quark-gluon plasma: progress and perils_ ([arXiv:0907.4808](http://arxiv.org/abs/0907.4808))

* {#Biagazzi12} Francesco Biagazzi, A. l. Cotrone, _Holography and the quark-gluon plasma_, AIP Conference Proceedings 1492, 307 (2012) ([doi:10.1063/1.4763537]( https://doi.org/10.1063/1.4763537), [slides pdf](http://cp3-origins.dk/content/movies/2013-01-14-bigazzi.pdf))

* {#Brambilla14} Brambilla et al., section 9.2.2 of _[[QCD and strongly coupled gauge theories - challenges and perspectives]]_, Eur Phys J C Part Fields. 2014; 74(10): 2981 ([arXiv:1404.3723](https://arxiv.org/abs/1404.3723),  [doi:10.1140/epjc/s10052-014-2981-5](https://link.springer.com/article/10.1140%2Fepjc%2Fs10052-014-2981-5))


Holographic discussion of the [[shear viscosity]] of the quark-gluon plasema goes back to

* {#PolicastroSonStarinets01} [[Giuseppe Policastro]], D.T. Son, A.O. Starinets, _Shear viscosity of strongly coupled N=4 supersymmetric Yang-Mills plasma_, Phys. Rev. Lett.87:081601, 2001 ([arXiv:hep-th/0104066](http://arxiv.org/abs/hep-th/0104066))


Other original articles include:

* Hovhannes R. Grigoryan, Paul M. Hohler, Mikhail A. Stephanov, _Towards the Gravity Dual of Quarkonium in the Strongly Coupled QCD Plasma_ ([arXiv:1003.1138](http://arxiv.org/abs/1003.1138))

* Brett McInnes, _Holography of the Quark Matter Triple Point_ ([arXiv:0910.4456](http://arxiv.org/abs/0910.4456))



#### To particle physics

* [[Joseph Polchinski]], [[Matthew Strassler]], _Hard Scattering and Gauge/String Duality_, Phys. Rev. Lett. 88:031601, 2002, ([arXiv:hep-th/0109174](http://lanl.arxiv.org/abs/hep-th/0109174))

For more see at _[[AdS/QCD correspondence]]_.

#### To fluid dynamics

Application to [[fluid dynamics]] -- see also at _[[fluid/gravity correspondence]]_:

* [[Sayantani Bhattacharyya]], [[Veronika Hubeny]], [[Shiraz Minwalla]], [[Mukund Rangamani]], _Nonlinear Fluid Dynamics from Gravity_, JHEP 0802:045, 2008 ([arXiv:0712.2456](https://arxiv.org/abs/0712.2456))


#### To condensed matter physics
 {#ToCondensedMatterPhysics}

On [[AdS-CFT in condensed matter physics]]:

Textbook account

* {#HartnollLucasSachdev16} [[Sean Hartnoll]], [[Andrew Lucas]], [[Subir Sachdev]], _Holographic quantum matter_, MIT Press 2018 ([arXiv:1612.07324](https://arxiv.org/abs/1612.07324), [publisher](https://mitpress.ublish.com/book/holographic-quantum-matter))

Further reviews include the following:

* A S T Pires, _Ads/CFT correspondence in condensed matter_ ([arXiv:1006.5838](http://arxiv.org/abs/1006.5838))

* [[Subir Sachdev]], _Condensed matter and AdS/CFT_ ([arXiv:1002.2947](http://arxiv.org/abs/1002.2947))

* Yuri V. Kovchegov, _AdS/CFT applications to relativistic heavy ion collisions: a brief review_ ([arXiv:1112.5403](http://arxiv.org/abs/1112.5403))

* Alberto Salvio, _Superconductivity, Superfluidity and Holography_ ([arXiv:1301.0201](http://arxiv.org/abs/1301.0201))

* _[Holography and Extreme Chromodynamics](http://igfae.usc.es/~holoquark2018/)_, Santiago de Compostela, July 2018

On [[AdS-CMT|holographic]] [[superconductors]] via [[AdS4/CFT3 duality]] (hence with the [[bulk]] theory being [[11d supergravity]] aka [[M-theory]]):

The original article (according to [ZLSS15, p. ix](AdS-CMT#ZaanenLiuSunSchalm15)), regarding [[AdS4/CFT3-duality]] (hence with the [[bulk]] theory being [[11d supergravity]], whence "[[M-theory]]") as a tool for understanding [[non-perturbative effect|strongly coupled]] [[condensed matter physics]] (specifically [[superconductivity]]):

* [[Christopher P. Herzog]], [[Pavel Kovtun]], [[Subir Sachdev]], [[Dam Thanh Son]], *Quantum critical transport, duality, and M-theory*, Phys. Rev. D **75** (2007) 085020 &lbrack;[arXiv:hep-th/0701036](https://arxiv.org/abs/hep-th/0701036), [doi:10.1103/PhysRevD.75.085020](https://doi.org/10.1103/PhysRevD.75.085020)&rbrack;

and further discussion:
{#MoreOnHolographicSuperconductorsViaMTheory}

* [[Jerome P. Gauntlett]], [[Julian Sonner]], [[Toby Wiseman]]: *Holographic superconductivity in M-Theory*, Phys. Rev. Lett. **103** (2009) 151601  &lbrack;[arXiv:0907.3796](https://arxiv.org/abs/0907.3796), <a href="https://doi.org/10.1103/PhysRevLett.103.151601">doi:10.1103/PhysRevLett.103.151601</a>&rbrack;

* [[Steven S. Gubser]], [[Silviu S. Pufu]], Fabio D. Rocha: *Quantum critical superconductors in string theory and M-theory*, Phys. Lett. B **683** (2010) 201-204 &lbrack;[arXiv:0908.0011](https://arxiv.org/abs/0908.0011), [doi:10.1016/j.physletb.2009.12.017](https://doi.org/10.1016/j.physletb.2009.12.017)&rbrack;

* [[Jerome Gauntlett]], [[Julian Sonner]], [[Toby Wiseman]]: *Quantum Criticality and Holographic Superconductors in M-theory*, J. High Energ. Phys. **2010** 60 (2010) &lbrack;[arXiv:0912.0512](https://arxiv.org/abs/0912.0512), <a href="https://doi.org/10.1007/JHEP02(2010)060">doi:10.1007/JHEP02(2010)060</a>&rbrack;

* Aristomenis Donos, [[Jerome P. Gauntlett]], [[Julian Sonner]], Benjamin Withers: *Competing orders in M-theory: superfluids, stripes and metamagnetism*, J. High Energ. Phys. **2013** 108 (2013) &lbrack;[arXiv:1212.0871](https://arxiv.org/abs/1212.0871), <a href="https://doi.org/10.1007/JHEP03(2013)108">doi:10.1007/JHEP03(2013)108</a>&rbrack;

* Aristomenis Donos, [[Jerome P. Gauntlett]], Christiana Pantelidou: *Semi-local quantum criticality in string/M-theory*, J. High Energ. Phys. **2013** 103 (2013) &lbrack;<a href="https://doi.org/10.1007/JHEP03(2013)103">doi:10.1007/JHEP03(2013)103</a>, [arXiv:1212.1462](https://arxiv.org/abs/1212.1462)&rbrack;

* Yu-Sen An, Li Li, Fu-Guo Yang, Run-Qiu Yang: *Interior Structure and Complexity Growth Rate of Holographic Superconductor from M-Theory*,  J. High Energ. Phys. **2022** 133 (2022) &lbrack;[arXiv:2205.02442](https://arxiv.org/abs/2205.02442), <a href="https://doi.org/10.1007/JHEP08(2022)133">doi:10.1007/JHEP08(2022)133</a>&rbrack;



### Applications in mathematics

#### To the volume conjecture

Suggestion that the statement of the [[volume conjecture]] is really [[AdS-CFT duality]] combined with the [[3d-3d correspondence]] for [[M5-branes]] [[wrapped brane|wrapped]] on [[hyperbolic 3-manifolds]]:


* {#GangKimLee14b} Dongmin Gang, [[Nakwoo Kim]], Sangmin Lee, Section 3.2_Holography of 3d-3d correspondence at Large $N$_, JHEP04(2015) 091 ([arXiv:1409.6206](https://arxiv.org/abs/1409.6206))


* {#GangKim18} Dongmin Gang, [[Nakwoo Kim]], around (21) of: _Large $N$ twisted partition functions in 3d-3d correspondence and Holography_, Phys. Rev. D 99, 021901 (2019) ([arXiv:1808.02797](https://arxiv.org/abs/1808.02797))

#### To deep learning in neural networks

On the [[deep learning]] algorithm on [[neural networks]] as analogous to the [[AdS/CFT correspondence]]:

* Yi-Zhuang You, Zhao Yang, Xiao-Liang Qi, _Machine Learning Spatial Geometry from Entanglement Features_, Phys. Rev. B 97, 045153 (2018) ([arxiv:1709.01223](https://arxiv.org/abs/1709.01223))

* W. C. Gan and F. W. Shu, _Holography as deep learning_,  Int. J. Mod. Phys. D 26, no. 12, 1743020 (2017) ([arXiv:1705.05750](https://arxiv.org/abs/1705.05750))

* J. W. Lee, _Quantum fields as deep learning_ ([arXiv:1708.07408](https://arxiv.org/abs/1708.07408))

* [[Koji Hashimoto]], Sotaro Sugishita, Akinori Tanaka, Akio Tomiya, _Deep Learning and AdS/CFT_,  Phys. Rev. D 98, 046019 (2018) ([arxiv:1802.08313](https://arxiv.org/abs/1802.08313))

### Philosophy of AdS/CFT

* Radin Dardashti, Richard Dawid, Sean Gryb, Karim Thébault (2020). *On the Empirical Consequences of the AdS/CFT Duality*. In Nick Huggett, Keizo Matsubara, and Christian Wüthrich (Eds.), Beyond Spacetime: The Foundations of Quantum Gravity (pp. 284-303). Cambridge: Cambridge University Press. ([doi:10.1017/9781108655705.016](https://doi.org/10.1017/9781108655705.016), [arXiv:1810.00949](https://arxiv.org/abs/1810.00949))

[[!redirects AdS/CFT]]
[[!redirects AdS-CFT]]

[[!redirects AdS/CFT correspondence]]

[[!redirects AdS-CFT correspondence]]
[[!redirects AdS-CFT correspondence]]

[[!redirects AdS-CFT duality]]
[[!redirects AdS/CFT duality]]


[[!redirects AdS7-CFT6]]
[[!redirects AdS7-CFT6 duality]]
[[!redirects AdS7/CFT6]]

[[!redirects AdS5-CFT4]]
[[!redirects AdS5-CFT4 duality]]
[[!redirects AdS5/CFT4]]
[[!redirects AdS5/CFT4 duality]]

[[!redirects AdS4/CFT3]]
[[!redirects AdS4/CFT3 duality]]
[[!redirects AdS4/CFT3-duality]]

[[!redirects AdS4-CFT3]]
[[!redirects AdS4-CFT3 duality]]
[[!redirects AdS4-CFT3-duality]]

[[!redirects AdS5-CFT4 correspondence]]
[[!redirects AdS5/CFT4 correspondence]]

[[!redirects AdS5-CFT4 duality]]
[[!redirects AdS5/CFT4 duality]]





