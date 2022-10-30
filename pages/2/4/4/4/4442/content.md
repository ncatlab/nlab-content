
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

the conjectural Ads/CFT correspondence asserts an identification of the [[state]]s of [[quantum gravity]] given by [[string theory]] on an asymptotically [[anti-de Sitter spacetime]] with [[correlator]]s of a [[CFT|superconformal]] [[Yang-Mills theory]] on the asymptotic boundary.

## Examples

### $AdS_5 / CFT_4$

[[type II string theory]] on 5d [[anti de Sitter spacetime]] is dual to [[N=4 D=4 super Yang-Mills theory]].

### $AdS_7 / CFT_6$
 {#AdS7CFT6}

We list some of the conjectured statements and their evidence concerning the case of $AdS_7/CFT_6$-duality.

The hypothesis ([Maldacena 97, section 3.1](#Maldacena)) is that 

* the [[6d (2,0)-superconformal QFT]] on the [[worldvolume]] of $N$ coincident [[M5-branes]] 

is holographically related to 

* [[11-dimensional supergravity]] [[Kaluza-Klein mechanism|reduced on]] the 4-[[sphere]] $S^4$ with $N$ units of [[flux]] of the [[supergravity C-field]] to [[7d supergravity]] on an asymptotically [[anti de Sitter spacetime]].

In ([Witten 98, section 4](#Witten98)) is is argued that the [[conformal blocks]] of the 6d theory are entirely given already by the [[state]]s of (just) the effective [[higher dimensional Chern-Simons theory|7-dimensional Chern-Simons term]] of the [[supergravity C-field]], which locally is

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

That therefore not an abelian, but this _nonabelian_ [[higher dimensional Chern-Simons theory]] should be dual to the 6d theory was maybe first said explicitly in ([LuWang 2010](#LuWang)).

Its gauge field is hence locally a pair consisting of the abelian 3-form field $C$ and a [[Spin group]] $Spin(6,1)$-valued [[connection on a bundle|connection]] (see _[[supergravity C-field]] for global descriptions of such pairs). Or maybe rather  $Spin(6,2)$ to account for the constraint that the configurations are to be asymptotic [[anti de Sitter spacetime]]s (in analogy to the well-understood situation in [[3d quantum gravity]], see there for more details).

Indeed, in ([SezginSundell 2002](#SezginSundell)) more detailed arguments are given that the 7-dimensional dual to the 6d theory is a [[higher spin gauge theory]] for a higher spin [[gauge group]] extending $SO(6,2)$.



## Formalizations

The full formalization of AdS/CFT is still very much out of reach. 

One proposal for a formalization of a toy version in the context of [[AQFT]] is [[Rehren duality]]. However, it does not seem that this actually formalizes AdS-CFT, but something else.


## Related concepts

* [[duality in physics]], [[duality in string theory]]

  * [[T-duality]], [[S-duality]], [[U-duality]]

  * [[open/closed string duality]]

     * [[KLT relations]]

[[!include table of branes]]

## References

### Original articles

The original article is

* [[Juan Maldacena]], _The Large N limit of superconformal field theories and supergravity_, Adv. Theor. Math. Phys. 2:231, 1998, [hep-th/9711200](http://arxiv.org/abs/hep-th/9711200); _Wilson loops in Large N field theories_, Phys. Rev. Lett. __80__ (1998) 4859, [hep-th/9803002](http://arxiv.org/abs/hep-th/9803002)
 {#Maldacena}

The relevance of this was amplified in

* [[Edward Witten]], _Anti-de Sitter space and holography_, Advances in Theoretical and Mathematical Physics 2: 253&#8211;291, 1998, [hep-th/9802150](http://arxiv.org/abs/hep-th/9802150)

### Introductions and surveys

Surveys and introductions include

* [[Ofer Aharony]], S.S. Gubser, [[Juan Maldacena]], H. Ooguri, Y. Oz, _Large N Field Theories, String Theory and Gravity_ ([arXiv:hep-th/9905111](http://arxiv.org/abs/hep-th/9905111))

* [[Horatiu Nastase]], _Introduction to AdS-CFT_ ([arXiv:0712.0689](http://arxiv.org/abs/0712.0689))


* [[Gaston Giribet]], _Black hole physics and $AdS^3/CFT_2$_, lectures and proceedings of [[Croatian black hole school]]. 

* Jens L. Petersen, _Introduction to the Maldacena Conjecture on AdS/CFT_, Int.J.Mod.Phys. A14 (1999) 3597-3672, [hep-th/9902131](http://arxiv.org/abs/hep-th/9902131) , [doi](http://dx.doi.org/10.1142/S0217751X99001676)

* Jan de Boer, _Introduction to AdS/CFT correspondence_, [pdf](http://www-library.desy.de/preparch/desy/proc/proc02-02/Proceedings/pl.6/deboer_pr.pdf)


* wikipedia: [AdS/CFT correspondence](http://en.wikipedia.org/wiki/AdS/CFT_correspondence)

* an AdS/CFT [bibliography](http://www.personal.uni-jena.de/~p5thul2/notes/adscft.html)

Further references include:

* Gary T. Horowitz, [[Joseph Polchinski]], _Gauge/gravity duality_, [gr-qc/0602037](http://arxiv.org/abs/gr-qc/0602037)

* S. S. Gubser, I. R. Klebanov, A. M. Polyakov, _Gauge theory correlators from non-critical string theory_, Physics Letters B428: 105&#8211;114 (1998),  [hep-th/9802109](http://arxiv.org/abs/hep-th/9802109).
 

* [[Edward Witten]], _Three-dimensional gravity revisited_, [arxiv/0706.3359](http://arxiv.org/abs/0706.3359)

* C.R. Graham, [[Edward Witten]], _Conformal anomaly of submanifold observables in AdS/CFT correspondence_, [hepth/9901021](http://arxiv.org/abs/hep-th/9901021).

* [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012))

### $AdS_5 / CFT_4$

* N. Beisert et al., _Review of AdS/CFT Integrability, An Overview_ 
Lett. Math. Phys. vv, pp (2011), ([arXiv:1012.3982](http://arxiv.org/abs/1012.3982)).

### $AdS_7 / CFT_6$

We list references specific to $AdS_7/CFT_6$.


In 

* [[Edward Witten]], _Five-Brane Effective Action In M-Theory_ J. Geom. Phys.22:103-133,1997 ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))
 {#WittenI}

* [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ JHEP 9812:012,1998 ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012)) 
 {#Witten98}

it is argued that the [[conformal blocks]] of the [[6d (2,0)-superconformal QFT]] are entirely controled just by the effective [[higher dimensional Chern-Simons theory|7d Chern-Simons theory]] inside [[11-dimensional supergravity]], but only the abelian piece is discussed explicitly.

The fact that this Chern-Simons term is in fact a _nonabelian_ [[higher dimensional Chern-Simons theory]] in $d = 7$, due the [[quantum anomaly]] cancellation, is clear from the original source, equation (3.14) of

* [[Michael Duff]], James T. Liu, R. Minasian, _Eleven Dimensional Origin of String/String Duality: A One Loop Test_ ([arXiv:hep-th/9506126](http://arxiv.org/abs/hep-th/9506126))
  {#DLM}

but seems not to be noted explicitly in the context of $AdS_7/CFT_6$ before the references

* H. L&#252;, Yi Pang, _Seven-Dimensional Gravity with Topological Terms_ Phys.Rev.D81:085016 (2010) ([arXiv:1001.0042](http://arxiv.org/abs/1001.0042))

* H. Lu, Zhao-Long Wang, _On M-Theory Embedding of Topologically Massive Gravity_ 	Int.J.Mod.Phys.D19:1197 (2010) ([arXiv:1001.2349](http://arxiv.org/abs/1001.2349))
  {#LuWang}

There is in fact one more quantization condition to be taken into account. For more in that see [[schreiber:7d Chern-Simons theory and the 5-brane|here]].
Up to the further twists discussed there, this means that the gauge group of the effective 7d theory is some contraction of the [[Spin group]] $Spin(10,1)$. The asymptotic AdS condition suggests maybe that it should be $Spin(6,2)$.

In fact, in 

* [[Ergin Sezgin]], P. Sundell, _Massless Higher Spins and Holography_ ([hep-th/0205131](http://arxiv.org/abs/hep-th/0205131))
 {#SezginSundell}

arguments are given that the 7d theory is a [[higher spin gauge theory]] extension of $SO(6,2)$.

More on the relation between the [[M5-brane]] and supergravity on $AdS_7 \times S^4$ and arguments for the $SO(5)$ [[R-symmetry]] group on the 6d theory from the 7d theory are given in 

* A. J. Nurmagambetov, I. Y. Park, _On the M5 and the AdS7/CFT6 Correspondence_ ([arXiv:hep-th/0110192](http://arxiv.org/abs/hep-th/0110192))

See also 

* M. Nishimura, Y. Tanii, _Local Symmetries in the AdS_7/CFT_6 Correspondence_, Mod. Phys. Lett. A14 (1999) 2709-2720 ([arXiv:hep-th/9910192](http://arxiv.org/abs/hep-th/9910192))

### Applications
 {#Appications}

#### To gravity

Discussion of [[event horizons]] of [[black holes]] in terms of AdS/CFT is in

* Kyriakos Papadodimas, Suvrat Raju, _An Infalling Observer in AdS/CFT_ ([arXiv:1211.6767](http://arxiv.org/abs/1211.6767))

#### To condensed matter physics
 {#ToCondensedMatterPhysics}

Applications of AdS-CFT duality to [[condensed matter physics]] are reviewed in 

* A S T Pires, _Ads/CFT correspondence in condensed matter_ ([arXiv:1006.5838](http://arxiv.org/abs/1006.5838))

* [[Subir Sachdev]], _Condensed matter and AdS/CFT_ ([arXiv:1002.2947](http://arxiv.org/abs/1002.2947))

* Yuri V. Kovchegov, _AdS/CFT applications to relativistic heavy ion collisions: a brief review_ ([arXiv:1112.5403](http://arxiv.org/abs/1112.5403))

* Alberto Salvio, _Superconductivity, Superfluidity and Holography_ ([arXiv:1301.0201](http://arxiv.org/abs/1301.0201))

[[!redirects AdS/CFT]]
[[!redirects AdS/CFT correspondence]]
[[!redirects AdS-CFT correspondence]]

[[!redirects AdS-CFT correspondence]]

[[!redirects AdS/CFT correspondence]]

[[!redirects AdS-CFT duality]]
