
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Theta functions
+--{: .hide}
[[!include theta functions - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In a [[conformal field theory]] the conditions on [[correlators]] can be divided into two steps

1. for a fixed [[cobordism]] the correlators need to depend in a certain way on the choice of [[conformal structure]], they need to satisfy the [[Ward identities]] (e.g. [Gawedzki 99, around p. 30](#Gawedzki99));

1. the correlators need to glue correctly underly composition of cobordisms.

The spaces of functionals that satisfy the first of these conditions are called _conformal blocks_ . The second condition is called the [[sewing constraint]] on conformal blocks.

So conformal blocks are something like "precorrelators" or "potential correlators" of a [[CFT]]. 

The assignment of spaces of conformal blocks to surfaces and their [[isomorphisms]] under [[diffeomorphisms]] of these surfaces together constitutes the _[[modular functor]]_. Under [[AdS3-CFT2 and CS-WZW correspondence|CS/WZW holography]] this is essentially the data also given by the [[Hitchin connection]], see at _[[quantization of 3d Chern-Simons theory]]_ for more on this.

From a point of view closer to [[number theory]] and [[geometric Langlands correspondence]] elements of conformal blocks are naturally thought of ([Beauville-Laszlo 93](#BeauvilleLaszlo93)) as generalized [[theta functions]] (see there for more).


## Properties
 {#Properties}

### Relation to braiding of field insertions
 {#RelationToBraidingOfFieldInsertions}

In the case of [[2d CFT|2d]] [[rational CFT]] the [[representation category]] of the corresponding [[vertex operator algebra]] is a [[modular tensor category]] (see [there](modular+tensor+category#RepCategoriesOfVOAs)), hence a [[braided monoidal category]] with extra properties.

 In this case the [[monoidal category|monoidal]]- and the [[braided monoidal category|braided]] [[structure]] (hence the [[modular tensor category|modular tensor structure]]) on the underlying [[representation category]] is entirely fixed by the space of [[conformal blocks]] of the [[2d CFT]] on the [[Riemann sphere]] (the "genus zero conformal blocks").

This may be found highlighted in [EGNO 15, p. 266](modular+tensor+category#EGNO15), [Runkel, Sec. 4.3](modular+tensor+category#Runkel). The essentially equivalent fact that the genus=0 conformal blocks already determine the [[modular functor]] of the CFT is proven in [Andersen & Ueno 2012](modular+functor#AndersenUeno12).


### Holographic correspondence

The conformal blocks at least of the [[WZW model]] are by a [[holographic principle|holographic]] correspondence given by the [[space of quantum states]] of 3d [[Chern-Simons theory]]. See at _[[AdS3-CFT2 and CS-WZW correspondence]]_.

### Relation to equivariant elliptic cohomology

For the $G$-[[WZW model]] the assignment of spaces of conformal blocks, hence by the above equivalently modular functor for $G$-[[Chern-Simons theory]] restricted to [[genus of a surface|genus-1 surfaces]] ([[elliptic curves]]) is essentially what is encoded in the universal $G$-[[equivariant elliptic cohomology]] (equivariant [[tmf]]). In fact equivariant elliptic cohomology remembers also the [[local prequantum field theory|pre-quantum]] incarnation of the modular functor as a systems of [[prequantum line bundles]] over Chern-Simons [[phase spaces]] (which are [[moduli stacks of flat connections]]) and remembers the [[quantization]]-process from there to the actual [[space of quantum states]] by forming holomorphic [[sections]]. See at _[equivariant elliptic cohomology -- Idea -- Interpretation in Quantum field theory](equivariant+elliptic+cohomology#InterpretationInQuantumFieldTheory)_ for more on this.


## Related concepts

* [[FFRS-formalism]]

* [[Laughlin wavefunction]]

[[!include holographic principle -- table]]

## References

### For 2d CFT

A review is around p. 30 of

* {#Gawedzki99} [[Krzysztof Gawędzki]], _Conformal field theory: a case study_ ([arXiv:hep-th/9904145](http://arxiv.org/abs/hep-th/9904145))

On the [[Knizhnik-Zamolodchikov connection]] on [[configuration spaces of points]] and [[conformal blocks]]:

* {#Kohno14} [[Toshitake Kohno]], _Local Systems on Configuration Spaces, KZ Connections and Conformal Blocks_,  Acta Math Vietnam 39, 575–598 (2014)  &lbrack;[doi:10.1007/s40306-014-0088-6](https://doi.org/10.1007/s40306-014-0088-6), [pdf](https://www.ms.u-tokyo.ac.jp/~kohno/papers/kohno_config.pdf)&rbrack;

* [[Toshitake Kohno]], §1.4 in: *Conformal field theory and topology*, transl. from the 1998 Japanese original by the author. Translations of Mathematical Monographs __210__. Iwanami Series in Modern Mathematics. Amer. Math. Soc. (2002) &lbrack;[AMS:mmono-210](https://bookstore.ams.org/mmono-210)&rbrack;

and via [[Bohr-Sommerfeld leaves]] in [[geometric quantization]]:

* [[Andrei Tyurin]], *On Bohr-Sommerfeld bases*, Izvestiya: Mathematics **64** 5 (2000) 1033–1064 &lbrack;[arXiv:math/9909084](https://arxiv.org/abs/math/9909084), [doi:10.1070/IM2000v064n05ABEH000308](https://iopscience.iop.org/article/10.1070/IM2000v064n05ABEH000308), [pdf](https://www.mathnet.ru/links/d8ad7540137cf2f33c44ab3e9455d392/im308_eng.pdf)&rbrack;


Brief review:

* [[Jürgen Fuchs]], [[Christoph Schweigert]], [[Simon Wood]], [[Yang Yang]], pp. 8 of: *Algebraic structures in two-dimensional conformal field theory*, Encyclopedia of Mathematical Physics &lbrack;[arXiv:2305.02773](https://arxiv.org/abs/2305.02773)&rbrack;


Discussion in terms of [[conformal nets]]:

* {#BartelsDouglasHenriques14} [[Arthur Bartels]], [[Christopher Douglas]], [[André Henriques]], _Conformal nets II: conformal blocks_ ([arXiv:1409.8672](http://arxiv.org/abs/1409.8672))

See also

* A. Tsuchiya, [[Kenji Ueno]], Y. Yamada, _Conformal field theory on universal family of stable curves with gauge symmetries_, Adv. Studies in Pure Math. __19__, 459--566, Academic Press (1989) [MR92a:81191](http://www.ams.org/mathscinet-getitem?mr=92a:81191)

* [[Kenji Ueno]], _Conformal field theory with gauge symmetry_, Fields Institute Monographs 2008 [book page](http://www.ams.org/bookstore-getitem/item=FIM-24)

* Ratul Mahanta, Tanmoy Sengupta, *Modular linear differential equations for four-point sphere conformal blocks* &lbrack;[arXiv:2211.05158](https://arxiv.org/abs/2211.05158)&rbrack;

* Mikhail Pavlov, *Global torus blocks in the necklace channel* &lbrack;[arXiv:2302.10153](https://arxiv.org/abs/2302.10153)&rbrack;

* Vladimir Belavin, Juan Ramos Cabezas, Boris Runov: *Shadow formalism for supersymmetric conformal blocks* &lbrack;[arXiv:2408.07684](https://arxiv.org/abs/2408.07684)&rbrack;



Conformal blocks for [[self-dual higher gauge theory]]:

* [[Kiyonori Gomi]], _An analogue of the space of conformal blocks in $(4k+2)$-dimensions_ ([pdf](http://www.math.kyoto-u.ac.jp/~kgomi/papers/acb.pdf))

In particular, argument that the higher conformal blocks of the [[D=6 N=(2,0) SCFT|$D=6$ $\mathcal{N}=(2,0)$ SCFT]] reduce to confomal blocks of the ordinary 2d [[WZW model]] after [[KK-compactification]] on a [[Riemann surface]]:

* {#Witten09} [[Edward Witten]], [p. 22](https://arxiv.org/pdf/0905.2720.pdf#page=22) of: *Geometric Langlands From Six Dimensions*, in Peter Kotiuga (ed.) _A Celebration of the Mathematical Legacy of Raoul Bott_, CRM Proceedings & Lecture Notes **50** AMS (2010) &lbrack;[arXiv:0905.2720](http://arxiv.org/abs/0905.2720), [ISBN:978-0-8218-4777-0](https://bookstore.ams.org/crmp-50)&rbrack;

On irregular conformal blocks for [[Liouville theory]]

* [[Davide Gaiotto]], Joel Lamy-Poirier: *Irregular Singularities in the $H_3^+$ WZW Model* &lbrack;[arXiv:1301.5342](https://arxiv.org/abs/1301.5342)&rbrack;

* [[Babak Haghighat]], [[Yihua Liu]], [[Nicolai Reshetikhin]], *Flat Connections from Irregular Conformal Blocks* &lbrack;[arXiv:2311.07960](https://arxiv.org/abs/2311.07960)&rbrack;

* [[Xia Gu]], [[Babak Haghighat]], [[Kevin Loo]], *Irregular Fibonacci Conformal Blocks* &lbrack;[arXiv:2311.13358](https://arxiv.org/abs/2311.13358)&rbrack;

* [[Babak Haghighat]]: *Flat Connections from Irregular Conformal Blocks*, [talk at ](CQTS#HaghighatFeb2024) [[CQTS]] (Feb 2024) &lbrack;video: [zm](https://nyu.zoom.us/rec/share/c41GdU--I_-g2XLJ7A6T0HxK6AxI-utrlGb2mStB0XBOaJ3FrvC1JzoL_FsjWrEi.MBPR87t2nBR8f99t), [kt](https://cdnapisec.kaltura.com/p/1674401/sp/167440100/embedIframeJs/uiconf_id/23435151/partner_id/1674401?iframeembed=true&playerId=kaltura_player&entry_id=1_qyu7rg1l)&rbrack;

See also:

* Qianyu Hao, [[Andrew Neitzke]]: *A new construction of $c=1$ Virasoro blocks* &lbrack;[arXiv:2407.04483](https://arxiv.org/abs/2407.04483)&rbrack;





### Relation to theta functions

Relation to [[theta functions]]:

* {#BeauvilleLaszlo93} [[Arnaud Beauville]], [[Yves Laszlo]], _Conformal blocks and generalized theta functions_, Comm. Math. Phys. __164__ (1994), 385 - 419, [euclid](http://projecteuclid.org/euclid.cmp/1104270837), [alg-geom/9309003](http://arxiv.org/abs/alg-geom/9309003), [MR1289330](http://www.ams.org/mathscinet-getitem?mr=1289330)
 
* [[Arnaud Beauville]], _Conformal blocks, fusion rings and the Verlinde formula_, Proc. of the Hirzebruch 65 Conf. on Algebraic Geometry, Israel Math. Conf. Proc. __9__, 75-96 (1996) [pdf](http://math.unice.fr/~beauvill/pubs/Hirz65.pdf)

* [[Krzysztof Gawędzki]], _Lectures on CFT_ (from Park City, published in QFT and strings for mathematicians, Dijkgraaf at al editors, [site](http://www.math.ias.edu/qft), [source](http://www.math.ias.edu/QFT/fall/NewGaw.tex), [dvi](http://www.math.ias.edu/QFT/fall/NewGaw.dvi), [ps](http://www.math.ias.edu/QFT/fall/NewGaw.ps)

* [[Alexander Beilinson]], [[Yuri Manin]], [[Vadim Schechtman]], _Sheaves of Virasoro and Neveu-Schwarz algebras_, Lecture Notes in Math. __1289__, Springer 1987, 52&#8211;66 

* A.Mironov, A.Morozov, Sh.Shakirov, _Conformal blocks as Dotsenko-Fateev integral discriminants_, [arxiv/1001.0563](http://arxiv.org/abs/1001.0563)





[[!include hypergeometric KZ-solutions -- references]]





[[!include Laughlin wavefunctions as conformal blocks -- references]]








[[!redirects conformal blocks]]
