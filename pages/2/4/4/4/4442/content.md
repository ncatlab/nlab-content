
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

The _AdS-CFT correspondence_ (or _[Maldacena](Maldacena) duality_ ) is a class of cases for which there is strong evidence that it realizes the more general and more conjectural [[holographic principle|holographic duality]]:

the conjectural Ads/CFT correspondence asserts an identification of the [[state]]s of [[quantum gravity]] given by [[string theory]] on an [[asymptotically anti de Sitter spacetime|asymptotically]] [[anti-de Sitter spacetime]] with [[correlator]]s of a [[CFT|superconformal]] [[Yang-Mills theory]] on the asymptotic boundary.

## Examples

The solutions to [[supergravity]] that preserve the maximum of 32 [[supersymmetries]] are (e.g. [HEGKS 08 (1.1)](BPS+state#HEGKS08))

* $AdS_5 \times S^5$ in [[type II supergravity]]

* $AdS_7 \times S^4$ in [[11-dimensional supergravity]]

* $AdS_4 \times S^7$ in [[11-dimensional supergravity]]

as well as their [[Minkowski spacetime]] and plane wave limits. These are the main [[KK-compactifications]] for the following examples-


### $AdS_5 / CFT_4$ -- Horizon limit of D3-branes
 {#AdS5CFT4}

[[type II string theory]] on 5d [[anti de Sitter spacetime]] (times a 5-sphere) is dual to [[N=4 D=4 super Yang-Mills theory]] on the [[worldvolume]] of a [[D3-brane]] at the asymptotic boundary

([Maldacena 97, section 2](#Maldacena97))

([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 3 and 4](#AharonyGubserMaldacenaOoguriOz99))

### $AdS_7 / CFT_6$ -- Horizon limit of M5-branes
 {#AdS7CFT6}

We list some of the conjectured statements and their evidence concerning the case of $AdS_7/CFT_6$-duality.

The hypothesis ([Maldacena 97, section 3.1](#Maldacena97)) (see ([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 6.1.1](#AharonyGubserMaldacenaOoguriOz99)) for a review) 
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

Analogous discussion of the 6d theory as a higher WZW analog of a7d Chern-Simons theory phrased in terms of [[extended quantum field theory]] is ([[4-3-2 8-7-6|Freed 12]]).

### $AdS_4 / CFT_3$ --Horizon limit of M2-branes
 {#AdS4CFT3}

[[11d supergravity]]/[[M-theory]] on the asymptotitc $AdS_4$
spacetime of an [[M2-brane]].

([Maldacena 97, section 3.2](#Maldacena97), [Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 6.1.2](#AharonyGubserMaldacenaOoguriOz99), [Klebanov-Torri 10](KlebanovTorri10))


### $AdS_3 / CFT_2$ -- Horizon limit of D1-D5 brane bound states
 {#AdS3CFT2}

[[D1-D5 brane system]] in [[type IIB string theory]]

([Maldacena 97, section 4](#Maldacena97))

([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 5](#AharonyGubserMaldacenaOoguriOz99))

see also at _[[AdS3-CFT2 and CS-WZW correspondence]]_

(...)

### Non-conformal duals

#### Horizon limit of $Dp$-branes for arbitrary $p$

([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 6.1.3](#AharonyGubserMaldacenaOoguriOz99))


#### Horizon limit of NS5-brane

([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 6.1.4](#AharonyGubserMaldacenaOoguriOz99))


#### QCD models

While all of the above horizon limits product [[super Yang-Mills theory]], one can consider certain limits of these in which they look like plain [[QCD]], at least in certain sectors. This leads to a discussion of hologrpahic description of QCD properties that are actually experimentally observed. 

([Aharony-Gubser-Maldacena-Ooguri-Oz 99, section 6.2](#AharonyGubserMaldacenaOoguriOz99))

See the _[References -- Applications -- In condensed matter physics](#ToCondensedMatterPhysics)_.



### Further gauge theories induced by compactification and twisting

[[!include gauge theory from AdS-CFT -- table]]

## Formalizations

The full formalization of AdS/CFT is still very much out of reach. 

One proposal for a formalization of a toy version in the context of [[AQFT]] is [[Rehren duality]]. However, it does not seem that this actually formalizes AdS-CFT, but something else.


## Related concepts

* [[near-horizon geometry]]

* [[Fefferman-Graham ambient construction]]

* [[holographic entanglement entropy]]

* [[duality in physics]], [[duality in string theory]]

  * [[T-duality]], [[S-duality]], [[U-duality]]

  * [[open/closed string duality]]

     * [[KLT relations]]

* [[S-matrix theory]]

* [[anti de Sitter gravity]]

[[!include table of branes]]

## References

### Original articles

The original articles are

* [[Juan Maldacena]], _The Large N limit of superconformal field theories and supergravity_, Adv. Theor. Math. Phys. 2:231, 1998, [hep-th/9711200](http://arxiv.org/abs/hep-th/9711200); 
 {#Maldacena97}

* [[Juan Maldacena]], _Wilson loops in Large N field theories_, Phys. Rev. Lett. __80__ (1998) 4859, [hep-th/9803002](http://arxiv.org/abs/hep-th/9803002)
 {#Maldacena97}

The relevance of this was amplified in

* [[Edward Witten]], _Anti-de Sitter space and holography_, Advances in Theoretical and Mathematical Physics 2: 253&#8211;291, 1998, [hep-th/9802150](http://arxiv.org/abs/hep-th/9802150)

Detailed discussion of how [[Green-Schwarz action functionals]] for super $p$-branes in AdS target spaces induce, after diffeomorphism gauge fixing, superconformal field theory on the [[worldvolumes]] includes

* [[Gianguido Dall'Agata]], Davide Fabbri, Christophe Fraser, [[Pietro Fré]], Piet Termonia, Mario Trigiante, _The $Osp(8|4)$ singleton action from the supermembrane_, Nucl.Phys.B542:157-194, 1999 ([arXiv:hep-th/9807115](http://arxiv.org/abs/hep-th/9807115))

* [[Paolo Pasti]], [[Dmitri Sorokin]], Mario Tonin, _Branes in Super-AdS Backgrounds and Superconformal Theories_ ([arXiv:hep-th/9912076](http://arxiv.org/abs/hep-th/9912076))

See also at _[super p-brane -- As part of the AdS-CFT correspondence](Green-Schwarz+action+functional#AsPartOfTheAdSCFTCorrespodence)_.


### Introductions and surveys

Surveys and introductions include

* [[Ofer Aharony]], S.S. Gubser, [[Juan Maldacena]], H. Ooguri, Y. Oz, _Large N Field Theories, String Theory and Gravity_ ([arXiv:hep-th/9905111](http://arxiv.org/abs/hep-th/9905111))
 {#AharonyGubserMaldacenaOoguriOz99}

* [[Horatiu Nastase]], _Introduction to AdS-CFT_ ([arXiv:0712.0689](http://arxiv.org/abs/0712.0689))


* [[Gaston Giribet]], _Black hole physics and $AdS^3/CFT_2$_, lectures and proceedings of [[Croatian black hole school]]. 

* Jens L. Petersen, _Introduction to the Maldacena Conjecture on AdS/CFT_, Int.J.Mod.Phys. A14 (1999) 3597-