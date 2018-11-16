
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Phyics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _AdS-CFT correspondence_ is at its basis the observation ([Witten 98, Section 2.4](#Witten98)) that the classical [[action functionals]] for various [[field (physics)|fields]] coupled to [[Einstein gravity]] on [[anti de Sitter spacetime]] are, when expressed as [[functions]] of the [[asymptotic boundary]]-values of the [[field (physics)|fields]], equal to the [[generating functions]] for the [[correlators]]/[[n-point functions]] of a [[conformal field theory]] on that asymptotic boundary. 

In extrapolation of these elementary computations, the AdS/CFT correspondence [[conjecture|conjecturally]] extends to a more general identification of [[states]] of [[gravity]] ([[quantum gravity]]) on asymptotically [[anti de Sitter spacetimes]] of [[dimension]] $d+1$ with [[correlators]]/[[n-point functions]] of [[conformal field theories]] on the [[asymptotic boundary]] of dimension $d$ ([Gubser-Klebanov-Polyakov 98 (12)](#GubserKlebanovPolyakov98), [Witten 98, (2.11)](#Witten98)), such that [[perturbative quantum field theory|perturbation theory]] on one side of the correspondence relates to [[non-perturbative effects|non-perturbation]] on the other side.

While this works to some extent quite generally (see e.g. [Natsuume 15](#Natsuume15) for review), the tightest form of the correspondence relates the [[large N limit]] of [[superconformal field theories]] ([[super Yang-Mills theories]]) on the [[asymptotic boundaries]] of [[near-horizon limits]] of $N$ coincident [[black brane|black]] [[M2-brane]]/[[D3-brane]]/[[M5-brane]] to corresponding sectors of the [[string theory]]/[[M-theory]] [[quantum gravity]] in the [[bulk]] [[spacetime]] away from the brane.

A quick way to see that these [[supersymmetric]]-cases of AdS/CFT must be special is to observe that these are the only dimensions in which there are [[super anti de Sitter spacetime]]-enhancement of [[anti de Sitter spacetime]], matching the classification of simple [[superconformal geometry|superconformal symmetries]], see [there](supersymmetry#ClassificationSuperconformal).


[[!include superconformal symmetry -- table]]

Before the proposal for the actual matching rule of ADS/CFT ([Gubser-Klebanov-Polyakov 98 (12)](#GubserKlebanovPolyakov98), [Witten 98, (2.11)](#Witten98)) it was by matching of [[BPS-states]] in these situations that a AdS/CFT correspondence was proposed in ([Maldacena 97a](#Maldacena97a), [Maldacena 97b](#Maldacena97b)), and these articles are now widely regarded as the origin of the idea of the AdS/CFT correspondence, even though there have of been precursors:

Generally, AdS/CFT correspondence is an incarnation of [[open/closed string duality]], which is based on the simple observation that the [[string scattering amplitude]] of a [[cylinder]]-shaped [[worldsheet]] has two equivalent interpretations: On the one hand, reading [[worldsheet]]-time along the [[circle]]-direction of the cylinder, it is a [[loop order|1-loop]] [[open string]]-[[vacuum amplitude]] for an [[open string]] attached to some [[D-brane]], while on the other hand, with [[worldsheet]]-time real in the orthogonal direction, it is a [[closed string]] [[loop order|tree-level]] amplitidude describing a [[closed string]] emanating from/absorbed by that [[D-brane]]. Since the excitations of the [[open string]] are the quanta of the ("[[Chan-Paton gauge field|Chan-Paton]]")-[[gauge fields]] on the [[D-brane]], while the excitations of the [[closed string]] include the [[gravitons]] witnessing the [[gravity|gravitational]] backreaction of the D-branes, this already indicates that there must be some close relation between the [[worldvolume]] [[super Yang-Mills theory]] on the [[D-brane]] and the [[quantum gravity]] of the ambient [[bulk]] [[spacetime]].

More specifically, it was shown in ([Duff-Sutton 88](#DuffSutton88), [Duff 98](#Duff98)) that the field theory of small perturbation  of a [[Green-Schwarz sigma-model]] for a [[fundamental brane]] stretched over the [[asymptotic boundary]] of the AdS  [[near horizon geometry]] of its own [[black brane]] incarnation is, after [[diffeomorphism]] [[gauge fixing]], a [[conformal field theory]]. This was further developed in [Claus-Kallosh-Proeyen 97](#ClausKalloshProeyen97), [DGGGTT 98](#DGGGTT98), [Claus-Kallosh-Kumar-Townsend 98](#ClausKalloshKumarTownsend98), [Pasti-Sorokin-Tonin 99](#PastiSorokinTonin99). See also at _[super p-brane -- As part of the AdS-CFT correspondence](Green-Schwarz+action+functional#AsPartOfTheAdSCFTCorrespodence)

For the archetypical case of AdS/CFT relating [[N=4 D=4 super Yang-Mills theory]] to [[type IIB string theory]] on [[super anti de Sitter spacetime]] $AdS_5 \times S^5$, fine detailed checks of the correspondence have been performed ([Beisert et al. 10](#BeisertEtAl10), [Escobedo 12](#Escobedo12)), see the section _[Checks](#Checks)_ below. 

If one relaxes the various assumptions that go into this exact form of the correspondence ([[conformal invariance]], [[supersymmetry]], [[large N limit]], [[anti de Sitter spacetime|anti de Sitter geometry]]) there is still a correspondence, albeit less exact. Such approximate forms of the AdS/CFT correspondence are being argued to be of use for understanding of the [[quark-gluon plasma]] in [[quantum chromodynamics]] ([Policastro-Son-Starinets 01](#PolicastroSonStarinets01)) and for various models in [[solid state physics]] (see [Hartnoll-Lucas-Sachdev 16](#HartnollLucasSachdev16)_[[AdS-CFT in condensed matter physics]]_).



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

The hypothesis ([Maldacena 97, section 3.1](#Maldacena97a)) (see ([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 6.1.1](#AharonyGubserMaldacenaOoguriOz99)) for a review) 
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


{#CommentSezginSundell} Indeed, in ([SezginSundell 2002, section 7](#SezginSundell)) more detailed arguments are given that the 7-dimensional dual to the free 6d theory is a [[higher spin gauge theory]] for a higher spin [[gauge group]] extending the ([[superconformal group|super]]) [[conformal group]] $SO(6,2)$.

A [[non-perturbative quantum field theory|non-perturbative]] description of this nonabelian [[7d Chern-Simons theory]] as a [[local prequantum field theory]] (hence defined [[non-perturbative quantum field theory|non-perturbatively]] on the global [[moduli stack]] of [[field (physics)|fields]] ([[twisted differential string structures]], in fact)) was discussed in ([FSS 12a](#FSS12a), [FSS 12b](#FSS12b)).

General discussion of [[boundary field theory|boundary]] [[local prequantum field theories]] relating higher Chern-Simons-type and higher WZW-type theories is in ([[schreiber:differential cohomology in a cohesive topos|dcct 13, section 3.9.14]]). Specifically, a characterization along these lines of the [[Green-Schwarz action functional]] of the [[M5-brane]] as a holographic [[infinity-Wess-Zumino-Witten theory - contents|higher WZW-type]] boundary theory of a 7d Chern-Simons theory is found in ([FSS 13](#FSS13)).

Analogous discussion of the 6d theory as a higher WZW analog of a 7d Chern-Simons theory phrased in terms of [[extended quantum field theory]] is ([[4-3-2 8-7-6|Freed 12]]).

### $AdS_4 / CFT_3$ --Horizon limit of M2-branes
 {#AdS4CFT3}

[[11d supergravity]]/[[M-theory]] on the asymptotic $AdS_4$
spacetime of an [[M2-brane]].

([Maldacena 97, section 3.2](#Maldacena97a), [Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 6.1.2](#AharonyGubserMaldacenaOoguriOz99), [Klebanov-Torri 10](KlebanovTorri10))


### $AdS_3 / CFT_2$ -- Horizon limit of D1-D5 brane bound states
 {#AdS3CFT2}

[[D1-D5 brane system]] in [[type IIB string theory]]

([Maldacena 97, section 4](#Maldacena97a))

([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 5](#AharonyGubserMaldacenaOoguriOz99))

see also at _[[AdS3-CFT2 and CS-WZW correspondence]]_

(...)

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

## Checks
 {#Checks}

At the heart of the duality is the observation that the classical [[action functionals]] for various [[field (physics)|fields]] coupled to [[Einstein gravity]] on [[anti de Sitter spacetime]] are, when expressed as [[functions]] of the [[asymptotic boundary]] values of the [[field (physics)|fields]], equal to the [[generating functions]] for the [[correlators]]/[[n-point functions]] of a [[conformal field theory]] on that asymptotic boundary. 

These computations were laid out in [Witten 98, section 2.4 "Some sample computation"](#Witten98). These follow from elementary manipulation in [[differential geometry]] (involving neither [[supersymmetry]] nor [[string theory]]).

For the more ambitious matching of the spectrum of the dilatation operator of [[N=4 D=4 super Yang-Mills theory]] to the corresponding spectrum of the [[Green-Schwarz superstring]] on the [[super anti de Sitter spacetime]] $AdS_5 \times S^5$ detailed checks are summarized in [Beisert et al. 10](#BeisertEtAl10), [Escobedo 12](#Escobedo12)


<center>
<img src="https://ncatlab.org/nlab/files/AdSCFTFrolovTseytlinLimitCheck.jpg" width="600">
</center>

> graphics grabbed from [Escobedo 12](#Escobedo12) spring

## Formalizations

The full formalization of AdS/CFT is still very much out of reach, but maybe mostly for lack of trying. 

But see [Anderson 04](#Anderson04).

One proposal for a formalization of a toy version in the context of [[AQFT]] is [[Rehren duality]]. However, it does not seem that this actually formalizes AdS-CFT, but something else.


## Related concepts

* [[near-horizon geometry]]

* [[Fefferman-Graham ambient construction]]

* [[holographic entanglement entropy]]

* [[duality in physics]], [[duality in string theory]]

  * [[T-duality]], [[S-duality]], [[U-duality]]

  * [[open/closed string duality]]

     * [[KLT relations]]

* [[black hole in anti de Sitter spacetime]]

* [[S-matrix theory]]

* [[anti de Sitter gravity]]

* [[Randall-Sundrum model]]

* [[Sachdev-Ye-Kitaev model]]

* [[p-adic AdS-CFT]]

[[!include table of branes]]

## References

### Original articles

The original articles are

* {#Maldacena97a} [[Juan Maldacena]], _The Large N limit of superconformal field theories and supergravity_, Adv. Theor. Math. Phys. 2:231, 1998 ([hep-th/9711200](http://arxiv.org/abs/hep-th/9711200))

* {#Maldacena97b} [[Juan Maldacena]], _Wilson loops in Large $N$ field theories_, Phys. Rev. Lett. __80__ (1998) 4859 ([hep-th/9803002](http://arxiv.org/abs/hep-th/9803002))

The actual rule for matching [[bulk field theory|bulk]] [[states]] to [[generating functions]] for [[boundary field theory|boundary]] [[correlators]]/[[n-point functions]] is due to

* {#GubserKlebanovPolyakov98} [[Steven Gubser]], [[Igor Klebanov]], [[Alexander Polyakov]], around (12) of _Gauge theory correlators from non-critical string theory_, Physics Letters B428: 105&#8211;114 (1998) ([hep-th/9802109](http://arxiv.org/abs/hep-th/9802109))

* {#Witten98} [[Edward Witten]], around (2.11) of _Anti-de Sitter space and holography_, Advances in Theoretical and Mathematical Physics 2: 253&#8211;291, 1998 ([hep-th/9802150](http://arxiv.org/abs/hep-th/9802150))

See also


* {#Giraldo12} Carlos Andrés Cardona Giraldo, _Correlation functions in AdS/CFT correspondence_, 2012 ([spire:1652794](inspirehep.net/record/1652794), [pdf](https://digital.bl.fcen.uba.ar/download/tesis/tesis_n5179_CardonaGiraldo.pdf))


Discussion of how [[Green-Schwarz action functionals]] for super $p$-branes in AdS target spaces induce, after [[diffeomorphism]] [[gauge fixing]], superconformal field theory on the [[worldvolumes]] (see _[[singleton representation]]_) goes back to

* {#DuffSutton88} [[Mike Duff]], C. Sutton, _The Membrane at the End of the Universe_, New Sci. 118 (1988) 67-71 ([spire:268230](http://inspirehep.net/record/268230?ln=en))

* {#Duff98} [[Mike Duff]], _Anti-de Sitter space, branes, singletons, superconformal field theories and all that_, Int.J.Mod.Phys.A14:815-844,1999 ([arXiv:hep-th/9808100](https://arxiv.org/abs/hep-th/9808100))

and was further developed in

* {#ClausKalloshProeyen97} Piet Claus, [[Renata Kallosh]], [[Antoine Van Proeyen]], _M 5-brane and superconformal $(0,2)$ tensor multiplet in 6 dimensions_, Nucl.Phys. B518 (1998) 117-150 ([arXiv:hep-th/9711161](http://arxiv.org/abs/hep-th/9711161))

* {#DGGGTT98} [[Gianguido Dall'Agata]], Davide Fabbri, Christophe Fraser, [[Pietro Fré]], Piet Termonia, Mario Trigiante, _The $Osp(8|4)$ singleton action from the supermembrane_, Nucl.Phys.B542:157-194, 1999 ([arXiv:hep-th/9807115](http://arxiv.org/abs/hep-th/9807115))

* {#ClausKalloshKumarTownsend98} Piet Claus, [[Renata Kallosh]], J. Kumar, [[Paul Townsend]], [[Antoine Van Proeyen]], _Conformal Theory of M2, D3, M5 and 'D1+D5' Branes_, JHEP 9806 (1998) 004 ([arXiv:hep-th/9801206](http://arxiv.org/abs/hep-th/9801206))


* {#PastiSorokinTonin99} [[Paolo Pasti]], [[Dmitri Sorokin]], Mario Tonin, _Branes in Super-AdS Backgrounds and Superconformal Theories_ ([arXiv:hep-th/9912076](http://arxiv.org/abs/hep-th/9912076))

See also at _[super p-brane -- As part of the AdS-CFT correspondence](Green-Schwarz+action+functional#AsPartOfTheAdSCFTCorrespodence)_.


### Introductions and surveys

Surveys and introductions include

* {#AharonyGubserMaldacenaOoguriOz99} [[Ofer Aharony]], S.S. Gubser, [[Juan Maldacena]], H. Ooguri, Y. Oz, _Large N Field Theories, String Theory and Gravity_, Phys.Rept.323:183-386,2000 ([arXiv:hep-th/9905111](http://arxiv.org/abs/hep-th/9905111))

* {#Anderson04} Michael T. Anderson, _Geometric aspects of the AdS/CFT correspondence_ ([arXiv:hep-th/0403087](https://arxiv.org/abs/hep-th/0403087)) 

* {#Duff99} [[Mike Duff]], _TASI Lectures on Branes, Black Holes and Anti-de Sitter Space_ ([arXiv:hep-th/9912164](https://arxiv.org/abs/hep-th/9912164))

* [[Horatiu Nastase]], _Introduction to AdS-CFT_ ([arXiv:0712.0689](http://arxiv.org/abs/0712.0689))


* [[Gaston Giribet]], _Black hole physics and $AdS^3/CFT_2$_, lectures and proceedings of [[Croatian black hole school]]. 

* Jens L. Petersen, _Introduction to the Maldacena Conjecture on AdS/CFT_, Int.J.Mod.Phys. A14 (1999) 3597-3672, [hep-th/9902131](http://arxiv.org/abs/hep-th/9902131) , [doi](http://dx.doi.org/10.1142/S0217751X99001676)

* Jan de Boer, _Introduction to AdS/CFT correspondence_, [pdf](http://www-library.desy.de/preparch/desy/proc/proc02-02/Proceedings/pl.6/deboer_pr.pdf)

* {#Natsuume15} [[Makoto Natsuume]], _AdS/CFT Duality User Guide_, Lecture Notes in Physics 903, Springer 2015 ([arXiv:1409.3575](https://arxiv.org/abs/1409.3575))

* wikipedia: [AdS/CFT correspondence](http://en.wikipedia.org/wiki/AdS/CFT_correspondence)

* an AdS/CFT [bibliography](http://www.personal.uni-jena.de/~p5thul2/notes/adscft.html)

Further references include:

* Gary T. Horowitz, [[Joseph Polchinski]], _Gauge/gravity duality_, [gr-qc/0602037](http://arxiv.org/abs/gr-qc/0602037)
 

* [[Edward Witten]], _Three-dimensional gravity revisited_, [arxiv/0706.3359](http://arxiv.org/abs/0706.3359)

* C.R. Graham, [[Edward Witten]], _Conformal anomaly of submanifold observables in AdS/CFT correspondence_, [hepth/9901021](http://arxiv.org/abs/hep-th/9901021).

* [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012))

Review of [[Yangian]] symmetry includes


* [[Alessandro Torrielli]], _Yangians, S-matrices and AdS/CFT_,	  J.Phys.A44:263001,2011 ([arXiv:1104.2474](http://arxiv.org/abs/1104.2474))


### $AdS_4 / CFT_3$

* {#KlebanovTorri10} [[Igor Klebanov]], Giuseppe Torri, _M2-branes and AdS/CFT_,  	Int.J.Mod.Phys.A25:332-350,2010 ([arXiv:0909.1580](http://arxiv.org/abs/0909.1580))
  



### $AdS_5 / CFT_4$

* {#BeisertEtAl10} N. Beisert et al., _Review of AdS/CFT Integrability, An Overview_, Lett. Math. Phys. vv, pp (2011), ([arXiv:1012.3982](http://arxiv.org/abs/1012.3982)).

* {#Escobedo12} Jorge Escobedo, _Integrability in AdS/CFT: Exact Results for Correlation Functions_, 2012 ([spire:1264432](http://inspirehep.net/record/1264432))


### $AdS_7 / CFT_6$

We list references specific to $AdS_7/CFT_6$.


In 

* {#WittenI} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_ J. Geom. Phys.22:103-133,1997 ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))
 

* {#Witten98} [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ JHEP 9812:012,1998 ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012)) 
 

it is argued that the [[conformal blocks]] of the [[6d (2,0)-superconformal QFT]] are entirely controled just by the effective [[higher dimensional Chern-Simons theory|7d Chern-Simons theory]] inside [[11-dimensional supergravity]], but only the abelian piece is discussed explicitly.

The fact that this Chern-Simons term is in fact a _nonabelian_ [[higher dimensional Chern-Simons theory]] in $d = 7$, due the [[quantum anomaly]] cancellation, is clear from the original source, equation (3.14) of

* {#DLM} [[Michael Duff]], James T. Liu, R. Minasian, _Eleven Dimensional Origin of String/String Duality: A One Loop Test_ ([arXiv:hep-th/9506126](http://arxiv.org/abs/hep-th/9506126))
  

but seems not to be noted explicitly in the context of $AdS_7/CFT_6$ before the references

* H. L&#252;, Yi Pang, _Seven-Dimensional Gravity with Topological Terms_ Phys.Rev.D81:085016 (2010) ([arXiv:1001.0042](http://arxiv.org/abs/1001.0042))

* {#LuWang} H. Lu, Zhao-Long Wang, _On M-Theory Embedding of Topologically Massive Gravity_ Int.J.Mod.Phys.D19:1197 (2010) ([arXiv:1001.2349](http://arxiv.org/abs/1001.2349))
  

There is in fact one more quantization condition to be taken into account. 

Discussion of this nonabeloan [[7d Chern-Simons theory]] terms as a [[local prequantum field theory]] is in 

* {#FSS12a} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane|Multiple M5-branes, String 2-connections, and 7d nonabelian Chern-Simons theory]]_, Advances in Theoretical and Mathematical Physics (2014) ([arXiv:1201.5277](http://arxiv.org/abs/1201.5277))

and a corresponding non-perturbative discussion of the [[supergravity C-field]] that enters this Lagrangian is given in 

{#FSS12b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The moduli 3-stack of the C-field|The E8 moduli 3-stack of the C-field]]_ ([arXiv:1202.2455](http://arxiv.org/abs/1202.2455))

Up to the further twists discussed there, this means that the gauge group of the effective 7d theory is some contraction of the [[Spin group]] $Spin(10,1)$. The asymptotic AdS condition suggests maybe that it should be $Spin(6,2)$.

In fact, in 

* {#SezginSundell} [[Ergin Sezgin]], P. Sundell, _Massless Higher Spins and Holography_ ([hep-th/0205131](http://arxiv.org/abs/hep-th/0205131))
 

arguments are given that the 7d theory is a [[higher spin gauge theory]] extension of $SO(6,2)$.

More on the relation between the [[M5-brane]] and supergravity on $AdS_7 \times S^4$ and arguments for the $SO(5)$ [[R-symmetry]] group on the 6d theory from the 7d theory are given in 

* A. J. Nurmagambetov, I. Y. Park, _On the M5 and the AdS7/CFT6 Correspondence_ ([arXiv:hep-th/0110192](http://arxiv.org/abs/hep-th/0110192))

See also 

* M. Nishimura, Y. Tanii, _Local Symmetries in the AdS_7/CFT_6 Correspondence_, Mod. Phys. Lett. A14 (1999) 2709-2720 ([arXiv:hep-th/9910192](http://arxiv.org/abs/hep-th/9910192))

An explicit relalization of the [[Green-Schwarz action functional]] of the [[M5-brane]] as a boundary field theory to the fermionic Chern-Simons term in the [[11-dimensional supergravity]] action functional is given in 

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))


### Generalizations

* Gianluca Grignani, Troels Harmark, Andrea Marini, Marta Orselli, _The Born-Infeld/Gravity Correspondence_, Phys. Rev. D 94, 066009 (2016) ([arXiv:1602.01640](https://arxiv.org/abs/1602.01640))

### Applications
 {#Appications}

#### To gravity

Discussion of [[event horizons]] of [[black holes]] in terms of AdS/CFT (the "[[firewall problem]]") is in

* Kyriakos Papadodimas, Suvrat Raju, _An Infalling Observer in AdS/CFT_ ([arXiv:1211.6767](http://arxiv.org/abs/1211.6767))

To [[black hole]] interiors:

* [[Juan Maldacena]], _Toy models for black holes II_, talk at PiTP 2018 _From QBits to spacetime_ ([recording](https://video.ias.edu/PiTP/2018/0726-JuanMaldacena))

> The [[SYK model]] gives us a glimpse into the interior of an [[extremal black hole]]...That's the feature of SYK that I find most interesting...It is a feature this model has, that I think no other model has


#### To particle physics

* [[Joseph Polchinski]], [[Matthew Strassler]], _Hard Scattering and Gauge/String Duality_, Phys.Rev.Lett.88:031601,2002, ([arXiv:hep-th/0109174](http://lanl.arxiv.org/abs/hep-th/0109174))

#### To condensed matter physics
 {#ToCondensedMatterPhysics}

Application of [[AdS-CFT in condensed matter physics]] goes back to

* {#PolicastroSonStarinets01} [[Giuseppe Policastro]], D.T. Son, A.O. Starinets, _Shear viscosity of strongly coupled N=4 supersymmetric Yang-Mills plasma_, Phys. Rev. Lett.87:081601, 2001 ([arXiv:hep-th/0104066](http://arxiv.org/abs/hep-th/0104066))

A comprehensive textbook account is in

* {#HartnollLucasSachdev16} Sean A. Hartnoll, Andrew Lucas, [[Subir Sachdev]], _Holographic quantum matter_, MIT Press 2018 ([arXiv:1612.07324](https://arxiv.org/abs/1612.07324), [publisher](https://mitpress.ublish.com/book/holographic-quantum-matter))

Further reviews include the following:

* A S T Pires, _Ads/CFT correspondence in condensed matter_ ([arXiv:1006.5838](http://arxiv.org/abs/1006.5838))

* [[Subir Sachdev]], _Condensed matter and AdS/CFT_ ([arXiv:1002.2947](http://arxiv.org/abs/1002.2947))

* Yuri V. Kovchegov, _AdS/CFT applications to relativistic heavy ion collisions: a brief review_ ([arXiv:1112.5403](http://arxiv.org/abs/1112.5403))

* Alberto Salvio, _Superconductivity, Superfluidity and Holography_ ([arXiv:1301.0201](http://arxiv.org/abs/1301.0201))

* _[Holography and Extreme Chromodynamics](http://igfae.usc.es/~holoquark2018/)_, Santiago de Compostela, July 2018

[[!redirects AdS/CFT]]

[[!redirects AdS/CFT correspondence]]
[[!redirects AdS-CFT correspondence]]
[[!redirects AdS-CFT correspondence]]
[[!redirects AdS/CFT correspondence]]

[[!redirects AdS-CFT duality]]

[[!redirects AdS7-CFT6]]
[[!redirects AdS7-CFT6 duality]]

[[!redirects AdS5-CFT4]]
[[!redirects AdS5-CFT4 duality]]

[[!redirects AdS4-CFT3]]
[[!redirects AdS4-CFT3 duality]]
