
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

In the context of [[string theory]] the _NS5-brane_ is a certain extended physical objects -- a [[brane]] -- that appears in/is predicted by the theory.

There are different incarnations of this object:

For instance the [[effective QFT|effective background QFT]] of the [[type II string theory|type II string]] -- [[type II supergravity]] -- admits solutions to its generalized [[Einstein equations]] which describe higher dimensional analogs of charged [[black holes]] in ordinary gravity. Among them is a 5+1-dimensional "black brane" which is [[magnetic charge|magnetically charged]] under the [[Kalb-Ramond field]]. Since the KR field and the field of [[gravity]] constituting this solution of type II supergravity have as quanta the [[worldsheet]] excitations of the [[spinning string]] [[sigma-model]] that sit in what is called the [[Neveu-Schwarz sector]] one calls this the **NS5-brane**. 

This is to distinguish it from the [[D-brane|D5-brane]] which is instead charged under the [[RR-field]] whose quanta come from the [[Ramond-Ramond sector]] of the [[superstring]].



There are other incarnations of the NS 5-brane:

by the general logic of [[Kalb-Ramond field|higher electromagnetism]] the (1+1)-dimensional string has under [[electric-magnetic duality]] a _magnetic dual_ . By dimension counting this is a 5-brane. If we think of the string this way as the structure that supports the [[sigma-model]] that defines perturbative [[string theory]],  we also call it the _F1-brane_ (the _fundamental_ 1-brane). In this sense the the corresponding magnetic dual is the _F5-brane_ -- the _fundamental_ fivebrane.

One can understand the NS5-"black brane" solution to [[type II supergravity]] as being the solitonic incarnation of the fundamental 5-brane in much the same way as an ordinary [[black hole]] in ordinary [[gravity]] is a solitonic incarnation of the [[fundamental particle]]: as the particle, the black hole it is characterized just by [[mass]], [[charge]] and [[angular momentum]]. 

Similarly, the "black" NS5-brane is characterizes by [[mass]], [[B-field]] charge and [[angular momentum]]. 


## Properties

### As a black brane

[[!include black branes in supergravity -- table]]


### Relation to little string theory

By the [[brane scan]], on the [[worldvolume]] of an NS5-brane propagates a [[superstring]]. This is called the _[[little string]]_, see there for more.

### D-branes ending on NS5-branes
 {#DBranesEndingOnNS5Branes}

The [[black brane|black]] [[D-branes]] may end on [[black brane|black]] NS5-branes ([Callan-Harvey-Strominger 91, sections IV.C and V.B](#CallanHarveyStrominger91), [Tseytlin 96](#Tseytlin96), [Argurio-Englert-Houart 97](#ArgurioEnglertHouart97), [Brodie-Hanany 97](#BrodieHanany97), [EGKRS 00](#EGKRS00)). 

This ought to be this way if [[S-duality]] and [[T-duality]] work as expected, since:

$$
  \array{
    \text{F1 on D5} 
    &\overset{\text{S}}{\leftrightarrow}&
    \text{D1 on NS5}
    \\
    && \updownarrow\mathrlap{T}
    \\
    &&
    \text{D2 on NS5}
    \\
    && \updownarrow\mathrlap{T}
    \\
    &&
    \text{D3 on NS5}
    &\overset{\text{S}}{\leftrightarrow}&
    \text{D3 on D5}
    \\
    && \updownarrow\mathrlap{T}
    \\
    &&
    \vdots
  }
$$

This leads to what is called [[geometric engineering of quantum field theory]] on the [[worldvolume]] of these branes (following [Hanany-Witten 97](#HananyWitten97), review includes [Fazzi 17](#Fazzi17)).


#### Open D$p$-brane theories on the NS5

Combining the above two items, the corresponding [[worldvolume]] theories of the NS5-branes (see also at [[little string theory]]) in the presence of light D$p$-branes ending on/inside them are also referred to as "open D$p$-brane theories" or "OD$p$ theories" ([Gopakumar-Minwalla-Seiberg-Strominger 00, section 6](#GopakumarMinwallaSeibergStrominger00), [Harmark 00, section 4.2](#Harmark00), [Lu 06, section 6](#Lu06))



#### D4-branes ending on NS5-branes

see [Witten 97](#Witten97)

<img src="https://ncatlab.org/nlab/files/NS5-D4.jpg" width="440"/>

> graphics grabbed from [EGKRS 00](#EGKRS00)

#### D6-branes ending on NS5-branes
  {#D6BranesEndingOnNS5Branes}

Consider a [[black brane|black]] NS5-brane with [[near horizon geometry]] $  \underset{\sim AdS_7}{\underbrace{ \mathbb{R}^{5,1} \times \mathbb{R}_{\phi} }} \times S^3$ ([EGKRS 00, p. 8](#EGKRS00)):

<img src="https://ncatlab.org/nlab/files/BlackNS5BraneII.png"/>

The [[3-sphere]] factor $S^3$ is the [[unit sphere]] around the black NS5-brane [[worldvolume]] $\mathbb{R}^{5,1}$, and $\mathbb{R}_{\phi}$ parameterizes the radial distance from it.

Placing a [[D6-brane]] at one point of the $S^3$-factor ([EGKRS 00, p. 20](#EGKRS00))

<img src="https://ncatlab.org/nlab/files/NS5InD6a.png"/>

means to take its [[worldvolume]] to be the factor $\mathbb{R}^{5,1} \times \mathbb{R}_\phi$, hence extending to one side of the NS5-brane ([EGKRS 00, p. 7](#EGKRS00)):

<img src="https://ncatlab.org/nlab/files/NS5BoundingD6.png"/>

Placing another [[D6-brane]] at the corresponding antipodal point means to have it extend also to the other side ([EGKRS 00, p. 5](#EGKRS00)):

<img src="https://ncatlab.org/nlab/files/NS5InD6.png"/>

or else to have embedded the black NS5-brane into a single [[D6-brane]].

Special properties [[D6-branes]] ending on NS5-branes were highlighted in ([Brodie-Hanany 97, section 2.4](#BrodieHanany97)): the [[worldvolume]] theory becomes [[chiral fermion|chiral]].

The [[M-theory]]-lift of this situation should be the [[4-sphere|4-spherical]] [[orbifold]] [[near horizon geometry]] of an [[M5-brane]] ([MFF 12, section 8.3](#MFF12))

$$
  \underset{\sim AdS_7}{\underbrace{\mathbb{R}^{5,1} \times \mathbb{R}_\phi}} \times S^4/G_{ADE}
$$

where $G_{ADE} \subset SU(2)$ is a [[finite group|finite]] [[subgroup]] of [[special unitary group|SU(2)]] (hence in the [[ADE classification]]), [[action|acting]] via the identification $S^4 \simeq S(\mathbb{H} \oplus \mathbb{R})$ (see at _[[4-sphere]]_ the section _[SU(2)-action](4-sphere#QuaternionAction)_).
For non-trivial $G_{ADE}$, this [[action]] has precisely two [[fixed points]] $S^0 \hookrightarrow S^4 \to S^3$. Hence $\mathbb{R}^{5,1} \times \mathbb{R}_\phi \times S^0$ must be the [[worldvolume]] of two [[KK-monopoles]] of [[11d supergravity]], which is the M-theory lift of the two [[D6-branes]]. While the M-theory lift of the NS5-brane is the [[M5-brane]] with [[worldvolume]] $\mathbb{R}^{5,1}$. 
See also [Fazzi 17, p. 38](#Fazzi17):

> The NS5-D6 Hanany–Witten setup engineering six-dimensional $(1,0)$ theories is equivalent to M5-branes at an $A_k$ singularity in eleven dimensions.


Next, this construction may be repeated, having the [[D6-branes]] end on different NS5-branes, hence "suspended between NS5-branes" (graphics from [Fazzi 17, p. 33](#Fazzi17)): 

<img src="https://ncatlab.org/nlab/files/D6SuspendedNS5.png"/>


#### D6 branes intersecting D8-branes over NS5-branes

And on the other end the D6-branes may end on [[D8-branes]] over an NS5-brane ([Janssen-Meessen-Ortin 99, Section 3](#JanssenMeessenOrtin99)) yielding [[D6-D8 brane intersections]]:

<img src="https://ncatlab.org/nlab/files/GaiottoNS5D6.jpg" width="600">

> graphics grabbed from [Gaiotto-Tomasiello 14](#GaiottoTomasiello14)

Subject to the [[s-rule]]:

<center>
<img src="https://ncatlab.org/nlab/files/D6D8BraneIntersectionsSubjetToSRule.jpg" width="600">
</center>

> graphics grabbed from [Fazzi 17](#Fazzi17)


<center>
<img src="https://ncatlab.org/nlab/files/D6D8BraneIntersectionWithImplicitSRume.jpg" width="600">
</center>

> graphics grabbed from [GKSTY 02](#GKSTY02)

[[fuzzy funnel]] [[noncommutative geometry]]:

<center>
<img src="https://ncatlab.org/nlab/files/D6D8FuzzyFunnel.jpg" width="600">
</center>

> graphics grabbed from [Fazzi 17, Fig. 3.14](#Fazzi17), taken in turn from [Gaiotto-Tomassiello 14, Figure 5](#GaiottoTomassiello14)


Generally [[Dp-D(p+2)-brane intersections]] [[geometric engineering of QFT|geometrically engineer]] [[Yang-Mills monopoles]] in the [[worldvolume]] of the higher dimensional D$(p+2)$-branes.

Specifically for $p = 6$, i.e. for [[D6-D8-brane intersections]], this fits with the [[Witten-Sakai-Sugimoto model]] [[geometric engineering of QFT|geometrically engineering]] [[quantum chromodynamics]], and then gives a [[geometric engineering of QFT|geometric engineering]] of the [[Yang-Mills monopoles]] in actual [[QCD]] ([HLPY 08, p. 16](D6-D8-brane+intersection#HLPY08)).

<center>
<img src="https://ncatlab.org/nlab/files/WSSBraneConfigurationEngineeringQCDII.jpg" width="740"/>
</center>

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/D8D6NS5.jpg" width="380"/>
</div>

Here we are showing

1. the [[color charge|color]] [[D4-branes]];

1. the [[flavour (particle physics)|flavor]] [[D8-branes]];

   with

   1. the [[5d Chern-Simons theory]] on their [[worldvolume]]

   1. the corresponding [[4d WZW model]] on the boundary

   both exhibiting the [[meson fields]]

1. the [[baryon]] [[D4-branes]]

   (see at _[WSS -- Baryons](Witten-Sakai-Sugimoto+model#Baryons)_)

1. the [[Yang-Mills monopole]] [[D6-branes]] 

   (see at _[[D6-D8-brane bound state]]_)

1. the [[NS5-branes]].

> graphics grabbed from [Sati-Schreiber 20]()



#### NS5 half-branes
 {#NSHalfBranes}

By the discussion [above](NS5-brane#D6BranesEndingOnNS5Branes)_, a [[black brane|black]] [[D6-brane]] may end on a [[black brane|black]] [[NS5-brane]], and in fact a priori each [[black brane|brane]] [[NS5-brane]] has to be the junction of two [[black brane|black]] [[D6-branes]]. 

<img src="https://ncatlab.org/nlab/files/HalfNS5.jpg" width="650"/>

> from [GKSTY 02](#GKSTY02)

If in addition the [[black brane|black]] [[NS5-brane]] sits at an [[O8-plane]], hence at the [[orientifold]] [[fixed point]]-locus, then in the ordinary $\mathbb{Z}/2$-[[quotient]] it appears as a "[[half-brane]]" with only one copy of [[D6-branes]] ending on it:


<img src="https://ncatlab.org/nlab/files/HalfNS5II.jpg" width="400"/>

> from [GKSTY 02](#GKSTY02)

(In [Hanany-Zaffaroni 99](#HananyZaffaroni99) this is interpreted in terms of the [['t Hooft-Polyakov monopole]].)

{#LiftToMTheortyOfNS5Halfbrane} The lift to [[M-theory]] of this situation is an [[M5-brane]] [[brane intersection|intersecting]] an [[M9-brane]] (see at _[[MO5-plane]]_ and at _[[heterotic M-theory on ADE-orbifolds]]_):

<img src="https://ncatlab.org/nlab/files/M9KK6Intersection.jpg" width="650"/>

> from [GKSTY 02](#GKSTY02)

Alternatively the [[O8-plane]] may [[brane intersection|intersect]] the [[black brane|black]] [[D6-branes]] away from the [[black brane|black]] [[NS5-brane]]:

<img src="https://ncatlab.org/nlab/files/D6D8Intersection.jpg" width="650"/>

> from [HKLY 15](#HKLY15)

In general, some of the NS5 sit away from the [[O8-plane]], while some sit on top of it:


<img src="https://ncatlab.org/nlab/files/NS5D6O8.jpg" width="500"/>

> from [Hanany-Zaffaroni 98](#HananyZaffaroni98)


<img src="https://ncatlab.org/nlab/files/ApruzziFazziHalfM5.jpg" width="500"/>


> graphics grabbed from [Apruzzi-Fazzi 17, p. 18](#ApruzziFazzi17)


The lift to [[M-theory]] under [[duality between M-theory and heterotic string theory]] is the [[half M5-brane]]. 

See also at _[[intersecting D-brane models]]_ the section _[Intersection of D6s with O8s](intersecting+D-brane+model#IntersectionOfD6WithO8)_.




#### Webs

corresponding [[brane webs]]:


<img src="https://ncatlab.org/nlab/files/WebNS5D6.jpg" width="600"/>


> graphics grabbed from (Kimura 16 [pdf](http://www2.yukawa.kyoto-u.ac.jp/~qft.web/2016/slides/kimura.pdf))


### NS5/D4/D2 bound states
 {#NS5D4D2BoundStates}

[[bound states]] of NS5-branes with [[D4-branes]] and [[D2-branes]]: 

[Mitra-Roy 00, section 4](#MitraRoy00), [Mukhi-Suryanarayana 00](#MukhiSuryanarayana00), [Jia-Lu-Roy 17, p. 12, Table 1](#JiaLuRoy17), also [Mitra-Roy 01](#MitraRoy01), [Alishahiha-Oz 00](#AlishahihaOz00).

<img src="https://ncatlab.org/nlab/files/NS5-D4-D2.jpg" width="440"/>

> graphics grabbed from [Mukhi-Suryanarayana 00](#MukhiSuryanarayana00)

Notice that this includes configurations with the D4-branes and D2-branes contained strictly inside the NS5: [Mitra-Roy 00, section 4](#MitraRoy00)

Review includes [Camino 02, section 4.5](#Camino02)

see also [Petri 18](#Petri18)

For the lift to [[M-theory]] see at _[M2-M5 brane bound state](M2-brane#M2M5BoundStates)_



### Relation to Khovanov homology

[[Khovanov homology]] has long been expected to appear as the [[observables]] in a 4-[[dimension]]al [[TQFT]] in higher analogy of how the [[Jones polynomial]] arises as an observable in 3-dimensional [[Chern-Simons theory]]. For instance for $\Sigma : K \to K'$ a cobordism between two [[knots]] there is a natural [[morphism]]

$$
  \Phi_\Sigma : \mathcal{K}(K) \to \mathcal{K}(K')
$$

between the Khovanov homologies associated to the two knots.

In ([Witten11](#Witten11)) it is argued, following indications in ([GukovSchwarzVafa](#GukovSchwarzVafa))
that this 4d TQFT is related to the [[worldvolume]] theory of the _image_ in [[type IIA string theory|type IIA]] of [[D3-branes]] ending on NS5-branes in [[type IIB string theory|type IIB]] after one [[S-duality]] and one [[T-duality]] operation:

$$
  (D3 - NS4)
    \stackrel{S}{\mapsto}
  (D3 - D5)
    \stackrel{T}{\mapsto}
  (D4-D6)
  \,.
$$

Earlier indication for this had come from the observation that [[Chern-Simons theory]] is the [[effective QFT|effective background theory]] for the [[A-model]] 2d [[TCFT]] (see [TCFT &#8211; Worldsheet and effective background theories](http://ncatlab.org/nlab/show/TCFT#ActionFunctionals) for details).

Notice that after the above [[T-duality]] operation the $(D4-D6)$-system wraps the $S^1$ ([[circle]]) along which the T-duality takes place. 

Lifting that configuration to [[11-dimensional supergravity]] gives [[M5-branes]] (the erstwhile [[D4-brane]]s) on [[Taub-NUT spacetime|Taub-NUT]] ($\times S^1$). The [[M5-branes]] wrap the circle-fiber of Taub-NUT, which shrinks to zero size at the origin (the location of the erstwhile D6, which is where the D4s "end"). The low-energy theory, on a stack of M5-branes, is the [[6d (2,0)-susy QFT]]. 

## Related concepts

* [[small instanton]]

* [[brane]], [[string]]

* [[fivebrane structure]], [[differential fivebrane structure]]

[[!include table of branes]]


\linebreaK


## References

### As a black brane

The 5-brane in [[heterotic string theory]] was found as a [[black brane]] in

* {#Strominger91} [[Andrew Strominger]], 

  _Heterotic solitons_, Nucl.Phys. B343 (1990) 167-184 Nucl.Phys. B353 (1991) 565 ([spire](http://inspirehep.net/record/27900))

  Erratum: Nucl. Phys. B353 (1991) 565-565 (<a href="https://doi.org/10.1016/0550-3213(91)90349-3">doi:10.1016/0550-3213(91)90349-3</a>, [spire:27900](http://inspirehep.net/record/27900))

* {#CallanHarveyStrominger91} [[Curtis Callan]], [[Jeffrey Harvey]], [[Andrew Strominger]], _Worldbrane actions for string solitons_, Nuclear Physics B Volume 367, Issue 1, 16 December 1991, Pages 60-82 (<a href="https://doi.org/10.1016/0550-3213(91)90041-U">doi:10.1016/0550-3213(91)90041-U</a>)

* Marco Cariglia, [[Kurt Lechner]], _NS5-branes in IIA supergravity and gravitational anomalies_ ([arXiv:hep-th/0203238](http://arxiv.org/abs/hep-th/0203238))

The [[brane intersection|intersection]] laws with [[black brane|black]] [[D-branes]] are  discussed in

* {#Tseytlin96} [[Arkady Tseytlin]], _No-force condition and BPS combinations of p-branes in 11 and 10 dimensions_, Nucl.Phys.B487:141-154,1997 ([arXiv:hep-th/9609212](https://arxiv.org/abs/hep-th/9609212))

* {#HananyWitten97} [[Amihay Hanany]], [[Edward Witten]], _Type IIB Superstrings, BPS Monopoles, And Three-Dimensional Gauge Dynamics_, Nucl. Phys. B492:152-190, 1997 ([arXiv:hep-th/9611230](https://arxiv.org/abs/hep-th/9611230))

* {#ArgurioEnglertHouart97} R. Argurio, [[François Englert]], L. Houart, _Intersection Rules for $p$-Branes_, Phys. Lett. B398:61-68, 1997 ([arXiv:hep-th/9701042](https://arxiv.org/abs/hep-th/9701042))

* {#Witten97} [[Edward Witten]], _Solutions Of Four-Dimensional Field Theories Via M Theory_, Nucl.Phys.B500:3-42,1997 ([arXiv:hep-th/9703166](https://xxx.lanl.gov/abs/hep-th/9703166))

* {#BrodieHanany97} [[John Brodie]], [[Amihay Hanany]], _Type IIA Superstrings, Chiral Symmetry, and N=1 4D Gauge Theory Dualities_, Nucl.Phys. B506 (1997) 157-182 ([arXiv:hep-th/9704043](https://arxiv.org/abs/hep-th/9704043))

* {#EGKRS00} Shmuel Elitzur, Amit Giveon, [[David Kutasov]], Eliezer Rabinovici, Gor Sarkissian, _D-Branes in the Background of NS Fivebranes_, JHEP 0008 (2000) 046 ([arXiv:hep-th/0005052](https://arxiv.org/abs/hep-th/0005052))



Review includes

* {#Fazzi17} [[Marco Fazzi]], _Higher-dimensional field theories from type II supergravity_ ([arXiv:1712.04447](https://arxiv.org/abs/1712.04447))

The [[M-theory]]-lift of the black NS5-brane embedded into a [[D6-brane]] should be the configuration from section 8.3 of 

* {#MFF12} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], _Half-BPS M2-brane orbifolds_, Adv. Theor. Math. Phys. Volume 16, Number 5 (2012), 1349-1408. ([arXiv:1007.4761](http://arxiv.org/abs/1007.4761), [Euclid](https://projecteuclid.org/euclid.atmp/1408561553))


### As a Green-Schwarz sigma-model


The [[Green-Schwarz action functionals]] for the NS5-brane:

In [[heterotic string theory]] (see also at _[[dual heterotic string theory]]_):


* [[Kurt Lechner]], [[Mario Tonin]], _Worldvolume and target space anomalies in the D=10 super--fivebrane sigma--model_ ([arXiv:hep-th/9603094](http://arxiv.org/abs/hep-th/9603094))


* J. Mourad, _Anomalies of the $SO(32)$ five-brane and their cancellation_, Nucl.Phys. B512 (1998) 199-208 ([arxiv:hep-th/9709012](https://arxiv.org/abs/hep-th/9709012))

* {#Lechner10} [[Kurt Lechner]], _Quantum properties of the heterotic five-brane_, Phys.Lett.B693:323-329, 2010 ([arxiv:1005.5719](https://arxiv.org/abs/1005.5719))


In [[type IIA string theory]]:

* [[Igor Bandos]], Alexei Nurmagambetov, [[Dmitri Sorokin]], _The type IIA NS5--Brane_ ([arXiv:hep-th/0003169](http://arxiv.org/abs/hep-th/0003169))

* Daniel Persson, _Fivebrane Instantons and Hypermultiplets_ (2010) ([pdf](http://string.lpthe.jussieu.fr/QKPHYS2010/Persson.pdf))

as a [[higher WZW model]]:

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_

### Under dualities

Discussion of the effect of [[T-duality]] on NS5-branes includes

* Eduardo Eyras, Bert Janssen, Yolanda Lozano, _5-branes, KK-monopoles and T-duality_, Nucl.Phys. B531 (1998) 275-301 ([arXiv:hep-th/9806169](https://arxiv.org/abs/hep-th/9806169))

* [[David Tong]], _NS5-Branes, T-Duality and Worldsheet Instantons_, JHEP 0207:013,2002 ([arXiv:hep-th/0204186](https://arxiv.org/abs/hep-th/0204186))

### Relation to the M5-brane

Most of the following references are more on the [[M5-brane]].

The fact that the worldvolume theory of the M5-brane should support fields that are [[self-dual higher gauge theory|self-dual]] [[connections on a 2-bundle]] ($\sim$ a [[gerbe]]) is discussed in 

* {#Witten07} [[Edward Witten]], _[[Conformal field theory in four and six dimensions]]_, in [[Ulrike Tillmann]], _Topology, Geometry and Quantum Field Theory: Proceedings of the 2002 Oxford Symposium in Honour of the 60th Birthday of Graeme Segal_,  London Mathematical Society Lecture Note Series (2004) ([arXiv:0712.0157](http://arxiv.org/abs/0712.0157))

as well as sections 3 and 4 of 

* [[Edward Witten]], _Geometric Langlands From Six Dimensions_ ([arXiv:0905.2720](http://arxiv.org/abs/0905.2720))
 {#Witten09}.

A review of some aspects is in 

* [[Robbert Dijkgraaf]], _The mathematics of fivebranes_ ([pdf](http://arxiv.org/PS_cache/hep-th/pdf/9810/9810157v1.pdf))



The relation to [[Khovanov homology]] is discussed in 

* {#Witten11} [[Edward Witten]], _Fivebranes and Knots_, Quantum Topology, Volume 3, Issue 1, 2012, pp. 1-137 ([arXiv:1101.3216](http://arxiv.org/abs/1101.3216), [doi:10.4171/QT/26](https://www.ems-ph.org/journals/show_abstract.php?issn=1663-487X&vol=3&iss=1&rank=1))
 

* {#GukovSchwarzVafa} [[Sergei Gukov]], [[Albert Schwarz]], [[Cumrun Vafa]], _Khovanov-Rozansky Homology And Topological Strings_ , Lett. Math. Phys. 74 (2005) 53-74, ([arXiv:hep-th/0412243](http://arxiv.org/abs/hep-th/0412243))
 

See also

* [[Greg Moore]], _On the role of six&#8208;dimensional $(2,0)$-theories in recent developments in
Physical Mathematics_ , talk at _Strings2011_ ([pdf slides](http://www-conference.slu.se/strings2011/presentations/3%20Wednesday/930_Moore.pdf))

The above discussion makes use of some blog comments (notably by [[Jacques Distler]]) appearing at

* [[Urs Schreiber]], _4d QFT for Khovanov Homology_ ([web](http://golem.ph.utexas.edu/category/2011/02/4d_qft_for_khovanov_homology.html))

### Intersection with O8/D8

Intersection of [[black brane|black]] NS5-branes with [[O8-planes]]/[[black brane|black]] [[D8-branes]] is discussed in

* {#HananyZaffaroni98} [[Amihay Hanany]], [[Alberto Zaffaroni]], _Branes and Six Dimensional Supersymmetric Theories_, Nucl.Phys. B529 (1998) 180-206 ([arXiv:hep-th/9712145](https://arxiv.org/abs/hep-th/9712145))

* {#JanssenMeessenOrtin99} Bert Janssen, Patrick Meessen, Tomas Ortin, _The D8-Brane Tied up: String and Brane Solutions in Massive Type IIA Supergravity_, Phys. Lett. B453 (1999) 229-236 ([arXiv:hep-th/9901078](https://arxiv.org/abs/hep-th/9901078))

* {#HananyZaffaroni99} [[Amihay Hanany]], [[Alberto Zaffaroni]], _Monopoles in String Theory_, JHEP 9912 (1999) 014 ([arXiv:hep-th/9911113](https://arxiv.org/abs/hep-th/9911113))

* {#GKSTY02} E. Gorbatov, [[Vadim Kaplunovsky]], [[Jacob Sonnenschein]], [[Stefan Theisen]], [[Shimon Yankielowicz]], _On Heterotic Orbifolds, M Theory and Type I' Brane Engineering_, JHEP 0205:015, 2002 ([arXiv:hep-th/0108135](https://arxiv.org/abs/hep-th/0108135))

* {#GaiottoTomasiello14} [[Davide Gaiotto]], [[Alessandro Tomasiello]], _Holography for $(1,0)$ theories in six dimensions_ ([arXiv:1404.0711](https://arxiv.org/abs/1404.0711))

* {#HKLY15} Hirotaka Hayashi, Sung-Soo Kim, Kimyeong Lee, Futoshi Yagi, _6d SCFTs, 5d Dualities and Tao Web Diagrams_, JHEP05(2019)203 ([arXiv:1509.03300](https://arxiv.org/abs/1509.03300))

* {#ApruzziFazzi17} Fabio Apruzzi, Marco Fazzi, _$AdS_7/CFT_6$ with orientifolds_, J. High Energ. Phys. (2018) 2018: 124 ([arXiv:1712.03235](https://arxiv.org/abs/1712.03235))

* {#HSS18} [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], Example 2.2.7 of: _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_, Communications in Mathematical Physics (2019) ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987), [doi:10.1007/s00220-019-03442-3](http://link.springer.com/article/10.1007/s00220-019-03442-3))

* {#FSS19c} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 4 of: _[[schreiber:Super-exceptional embedding construction of the M5-brane|Super-exceptional geometry: origin of heterotic M-theory and super-exceptional embedding construction of M5]]_ ([arXiv:1908.00042](https://arxiv.org/abs/1908.00042))

On the [[orientifold]] [[T-duality|T-dual]] of half M5-branes:

* {#FengHeKarchUranga01} Bo Feng, [[Yang-Hui He]], [[Andreas Karch]], [[Angel Uranga]], _Orientifold dual for stuck NS5 branes_, JHEP 0106:065, 2001 ([arXiv:hep-th/0103177](https://arxiv.org/abs/hep-th/0103177))



For more see at _[[M-theory on S1/G_HW times H/G_ADE]]_.


### NS5/D4/D2 bound states
 {#ReferencesNS5D4D2BoundStates}

[[bound states]] of NS5-branes with [[D4-branes]] and [[D2-branes]] (see also at _[M2-branes -- Dyonic membranes](M2-brane#ReferencesDyonic)_)

* {#MitraRoy00} Indranil Mitra, Shibaji Roy, _(NS5,Dp) and (NS5,D(p+2),Dp) bound states of type IIB and type IIA string theories_, JHEP 0102:026, 2001 ([arXiv:hep-th/0011236](https://arxiv.org/abs/hep-th/0011236))


* {#AlishahihaOz00} Mohsen Alishahiha, Yaron Oz, _Supergravity and "New" Six-Dimensional Gauge Theories_, Phys.Lett.B495:418-426, 2000 ([arXiv:hep-th/0008172](https://arxiv.org/abs/hep-th/0008172))

* {#MitraRoy01} Indranil Mitra, Shibaji Roy, _(NS5,D5,D3) bound state, OD3, OD5 limits and SL(2,Z) duality_, Phys.Rev. D65 (2002) 106001 ([arXiv:hep-th/0107127](https://arxiv.org/abs/hep-th/0107127))

* {#MukhiSuryanarayana00} [[Sunil Mukhi]], Nemani V. Suryanarayana, _Stable Non-BPS States and Their Holographic Duals_, Int. J. Mod. Phys. A16 (2001) 966-975 ([arXiv:hep-th/0011185](https://arxiv.org/abs/hep-th/0011185))



* {#Camino02} J. M. Camino, section 4.5 of _Worldvolume Dynamics of Branes_ ([arXiv:hep-th/0210249](https://arxiv.org/abs/hep-th/0210249))

* {#JiaLuRoy17} Qiang Jia, J. X. Lu, Shibaji Roy, _On 1/4 BPS ((F, D1), (NS5, D5)) bound states of type IIB string theory_, JHEP 08 (2017) 007 ([arXiv:1704.01463](https://arxiv.org/abs/1704.01463))

* Giuseppe Dibitetto, Nicolò Petrim, _6d surface defects from massive type IIA_, JHEP 01 (2018) 039 ([arXiv:1707.06154](https://arxiv.org/abs/1707.06154))

* {#Petri18} Nicolò Petri, _Surface defects in massive IIA_, talk at [Recent Trends in String Theory and Related Topics](http://physics.ipm.ac.ir/conferences/stringtheory3/) 2018 ([pdf](http://physics.ipm.ac.ir/conferences/stringtheory3/note/N.Petri.pdf))

### Open D$p$-brane theories on the NS5

* {#GopakumarMinwallaSeibergStrominger00} [[Rajesh Gopakumar]], [[Shiraz Minwalla]], [[Nathan Seiberg]], [[Andrew Strominger]], _OM Theory in Diverse Dimensions_, JHEP 0008:008, 2000 ([arXiv:hep-th/0006062](https://arxiv.org/abs/hep-th/0006062))


* {#Harmark00} Troels Harmark, _Open Branes in Space-Time Non-Commutative Little String Theory_,  Nucl.Phys. B593 (2001) 76-98 ([arXiv:hep-th/0007147](https://arxiv.org/abs/hep-th/0007147))


* {#Lu06} J. X. Lu, _$(1 + p)$-Dimensional Open $D(p - 2)$ Brane Theories_, JHEP 0108:049, 2001 ([arXiv:hep-th/0102056](https://arxiv.org/abs/hep-th/0102056))


[[!redirects NS-5-brane]]
[[!redirects F5-brane]]
[[!redirects F-5-brane]]
[[!redirects 5-brane]]
[[!redirects fivebrane]]

[[!redirects NS5-branes]]
[[!redirects NS-5-branes]]
[[!redirects F5-branes]]
[[!redirects F-5-branes]]
[[!redirects 5-branes]]
[[!redirects fivebranes]]

[[!redirects half NS5-brane]]
[[!redirects half NS5-branes]]

