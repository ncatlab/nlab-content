
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

One incarnation of the [[holographic principle]] in [[quantum field theory]] is the correspondence between 3d $G$-[[Chern-Simons theory]] as the [[bulk field theory]] and the 2d [[Wess-Zumino-Witten model]] on a suitable [[Lie group]] $G$ as the [[boundary field theory]]. This case stands out in that it was known and understood already before the [[holographic principle]] was formulated as such, motivated from [[bulk field theories]] of [[gravity]]. Notably the CS/WZW correspondence is an actual [[theorem]] instead of just a vague [[conjecture]], as for much of the [[AdS-CFT correspondence]].

Indeed, the natural equivalence between the [[space of quantum states]] of [[Chern-Simons theory]] on a [[surface]] $\Sigma$ and the space of [[conformal blocks]] of the [[WZW model]] on $\Sigma$ was understood in the seminal article ([Witten 89](#Witten89)) and subsequently discussed in much detail, see also at [CS-theory -- References](Chern-Simons%20theory#References). The explicit holographic correspondence between the [[wavefunctions]] of Chern-Simons theory and the [[correlators]] of the WZW model is reviewed for instance in ([Gaw&#281;dzki 99, around p. 30](#Gawedzki99)). For the case of abelian gauge group and with an eye towards generalization to [[self-dual higher gauge theory]] a review is in ([Witten 96, section 2](#Witten96)).
(This correspondence is captured [[functor|functorially]] by the notion of the _[[modular functor]]_ of the 2d theory, see there for more.)

For instance the [[FRS formalism]] _constructs_ all [[rational conformal field theories]] as full [[FQFTs]] holographically from the [[Reshetikhin-Turaev construction]] of the 3d Chern-Simons theory and fully classifies them this way.

Later the [[AdS-CFT correspondence]] came to be understood as a canonical or default implementation of the [[holographic principle]]. Here the [[bulk field theory]] is a theory of [[3d quantum gravity]] which is very much like traditional [[Chern-Simons theory]] but may crucially differ from it, see at _[[Chern-Simons gravity]]_ the [comments on the non-perturbative regime](Chern-Simons%20gravity#ProblemsInTheNonPerturbativeRegime). Instead some variant of CS3/WTW2 appears as one "sector" inside AdS3/CFT2, this is discussed in ([Gukov-Martinec-Moore-Strominger 04](#GukovMartinecMooreStrominger04)).

But notice that also plain [[Chern-Simons theory]] is a [[string theory]], but of [[topological strings]]. For more on this see at _[[TCFT]]_ the section _[Worldsheet and effective background theories](TCFT#ActionFunctionals)_.

A general argument that in sectors of the [[AdS-CFT correspondence]] the [[conformal blocks]] on the CFT-side are given just by the [[higher dimensional Chern-Simons theory]]-sector inside the dual [[gravity]] theory is in ([Witten98](#Witten98)). This applies notably to the duality between [[7-dimensional Chern-Simons theory]] and the conformal blocks in the [[6d (2,0)-superconformal QFT]] on the [[M5-brane]].

## Related concepts

* [[p-adic AdS/CFT correspondence]]

* [[3d quantum gravity]]

* [[BTZ black hole]]

* [[quantization of Chern-Simons theory]]/[[quantization of loop groups]]

* [[super 1-brane in 3d]]

* [[TT deformation]]

## References

### CS/WZW

The original article on the CS/WZW correspondence is

* {#Witten89} [[Edward Witten]], _Quantum Field Theory and the Jones Polynomial_ Commun. Math. Phys. 121 (3) (1989) 351&#8211;399. MR0990772 ([project EUCLID](http://projecteuclid.org/euclid.cmp/1104178138))

More details were developed in 

* D. C. Cabra, G. L. Rossini, _Explicit connection between conformal field theory and 2+1 Chern-Simons theory_, Mod. Phys. Lett. A12 (1997) 1687-1697 ([arXiv:hep-th/9506054](https://arxiv.org/abs/hep-th/9506054))


Reviews include

* {#Gawedzki99} [[Krzysztof Gawędzki]], around p. 30 of _Conformal field theory: a case study_ ([arXiv:hep-th/9904145](http://arxiv.org/abs/hep-th/9904145))
 
* {#Witten96} [[Edward Witten]], section 2 of _Five-Brane Effective Action In M-Theory_ J. Geom. Phys. 22: 103-133, 1997 ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))

The relation of this $CS_3/WZW_2$-duality to the [[AdS-CFT correspondence]] is discussed in

* {#GukovMartinecMooreStrominger04} [[Sergei Gukov]], [[Emil Martinec]], [[Gregory Moore]], [[Andrew Strominger]], _Chern-Simons Gauge Theory and the $AdS_3/CFT_2$ Correspondence_, in: [[Mikhail Shifman]] et al.  (eds.) _From fields to strings_, vol. 2, 1606-1647, 2004 ([arXiv:hep-th/0403225](https://arxiv.org/abs/hep-th/0403225))
 
* Kristan Jensen, _Chiral anomalies and AdS/CMT in two dimensions_, JHEP 1101:109,2011 ([arXiv:1012.4831](https://arxiv.org/abs/1012.4831))

* [[Per Kraus]], [[Finn Larsen]], _Partition functions and elliptic genera from supergravity_, JHEP 0701:002, 2007 ([arXiv:hep-th/0607138](https://arxiv.org/abs/hep-th/0607138))

* [[Per Kraus]], _Lectures on black holes and the $AdS_3/CFT_2$ correspondence_,  Lect. Notes Phys. 755: 193-247, 2008 ([arXiv:hep-th/0609074](https://arxiv.org/abs/hep-th/0609074))

* Ville Keranen, _Chern-Simons interactions in AdS3 and the current conformal block_ ([arXiv:1403.6881](https://arxiv.org/abs/1403.6881))

A general argument about the relation between AdS/CFT duality and [[schreiber:infinity-Chern-Simons theory]] is in 

* {#Witten98} [[Edward Witten]], _AdS/CFT Correspondence And Topological Field Theory_ JHEP 9812:012,1998 ([arXiv:hep-th/9812012](http://arxiv.org/abs/hep-th/9812012)) 
 

An argument (via [[Chern-Simons gravity]], but see the caveats there) that [[3d quantum gravity]] with negative [[cosmological constant]] has as [[boundary field theory]] 2d [[Liouville theory]] is due to 

* {#CoussaertHenneauxvanDriel95} O. Coussaert, [[Marc Henneaux]], P. van Driel, _The asymptotic dynamics of three-dimensional Einstein gravity with a negative cosmological constant_, Class. Quant. Grav. 12 (1995) 2961-2966 ([arXiv:gr-qc/9506019](http://arxiv.org/abs/gr-qc/9506019))

Discussion of the [[Ising model]] [[2d CFT]] as a boundary theory to a 3d [[TQFT]] based on the [[Turaev-Viro model]], and the phenomenon of [[Kramers-Wannier duality]], is discussed in

* {#FreedTeleman18} [[Daniel Freed]], [[Constantin Teleman]], _Topological dualities in the Ising model_ ([arXiv:1806.00008](https://arxiv.org/abs/1806.00008))

[[!include 3d gravity and Chern-Simons theory -- references]]

### $AdS_3$/$CFT_2$

Discussion of [[AdS/CFT correspondence]] for [[3d gravity]]/[[2d CFT]]:

* [[Andrea Prinsloo]], [[Vidas Regelskis]], [[Alessandro Torrielli]], _Integrable open spin-chains in AdS3/CFT2_ ([arXiv:1505.06767](http://arxiv.org/abs/1505.06767))

An exact correspondence of the symmetric [[orbifold]] [[CFT]] of [[Liouville theory]] with a string theory on $AdS_3$ is claimed in:


* {#EberhardtGaberdiel19a} [[Lorenz Eberhardt]], [[Matthias Gaberdiel]], _String theory on $AdS_3$ and the symmetric orbifold of Liouville theory_ ([arXiv:1903.00421](https://arxiv.org/abs/1903.00421))

* {#EberhardtGaberdiel19b} [[Lorenz Eberhardt]], [[Matthias Gaberdiel]], _Strings on $AdS_3 \times S^3 \times S^3 \times S^1$_ ([arXiv:1904.01585](https://arxiv.org/abs/1904.01585))

* {#EberhardtGaberdielGopakumar19} [[Lorenz Eberhardt]], [[Matthias Gaberdiel]], [[Rajesh Gopakumar]], _Deriving the $AdS_3/CFT_2$ Correspondence_ ([arXiv:1911.00378](https://arxiv.org/abs/1911.00378))

* Andrea Dei, [[Lorenz Eberhardt]], _Correlators of the symmetric product orbifold_ ([arXiv:1911.08485](https://arxiv.org/abs/1911.08485))

based on

* Shouvik Datta, [[Lorenz Eberhardt]], [[Matthias Gaberdiel]], _Stringy $\mathcal{N} = (2,2)$ holography for $AdS_3$_ JHEP 1801 (2018) 146 ([arXiv:1709.06393](https://arxiv.org/abs/1709.06393))

See also

* [[Lorenz Eberhardt]], _$AdS_3/CFT_2$ at higher genus_ ([arXiv:2002.11729](https://arxiv.org/abs/2002.11729))


Relation of [[AdS3/CFT2]] to [[hyperbolic geometry]] and [[Arakelov geometry]] of [[algebraic curves]]:

* [[Yuri Manin]], [[Matilde Marcolli]], _Holography principle and arithmetic of algebraic curves_, Adv. Theor. Math. Phys. 5 (2002) 617-650 ([arXiv:hep-th/0201036](https://arxiv.org/abs/hep-th/0201036))

In the context of [[holography as Koszul duality]]:

* [[Kevin Costello]], [[Natalie Paquette]], _Twisted Supergravity and Koszul Duality: A case study in $AdS_3$_ ([arXiv:2001.02177](https://arxiv.org/abs/2001.02177))

Generalization to [[boundary field theory]]:

* Sanjit Shashi, _Quotient-AdS/BCFT: Holographic Boundary $CFT_2$ on $AdS_3$ Quotients_ ([arXiv:2005.10244](https://arxiv.org/abs/2005.10244))

* [[Tadashi Takayanagi]], Takahiro Uetoko, _Chern-Simons Gravity Dual of BCFT_ ([arXiv:2011.02513](https://arxiv.org/abs/2011.02513))




See also

* Stefano Speziali, _Spin 2 fluctuations in 1/4 BPS AdS3/CFT2_ ([arxiv:1910.14390](https://arxiv.org/abs/1910.14390))



[[!include AdS3-CFT2 on D1-D5 branes -- references]]

[[!include AdS3-CFT2 on D2-D4-D6-D8 branes -- references]]

[[!include Chern-Simons Wilson lines in AdS3-CFT2 -- references]]




[[!redirects CS-WZW correspondence]]

[[!redirects AdS3-CFT2]]
[[!redirects AdS3/CFT2]]


[[!redirects AdS3/CFT2 duality]]
[[!redirects AdS3-CFT2 duality]]
[[!redirects AdS3/CFT2 dualities]]
[[!redirects AdS3-CFT2 dualities]]

