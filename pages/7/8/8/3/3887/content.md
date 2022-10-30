
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

In a [[conformal field theory]] the conditions on [[correlators]] can be divided into two steps

1. for a fixed [[cobordism]] the correlators need to depend in a certain way on the choice of [[conformal structure]], they need to satisfy the [[Ward identities]] (e.g. [Gawedzki 99, around p. 30](#Gawedzki99));

1. the correlators need to glue correctly underly composition of cobordisms.

The spaces of functionals that satisfy the first of these conditions are called _conformal blocks_ . The second condition is called the [[sewing constraint]] on conformal blocks.

So conformal blocks are something like "precorrelators" or "potential correlators" of a [[CFT]]. 

The assignment of spaces of conformal blocks to surfaces and their [[isomorphisms]] under [[diffeomorphisms]] of these surfaces together constitutes the _[[modular functor]]_. Under [[AdS3-CFT2 and CS-WZW correspondence|CS/WZW holography]] this is essentially the data also given by the [[Hitchin connection]], see at _[[quantization of 3d Chern-Simons theory]]_ for more on this.

From a point of view closer to [[number theory]] and [[geometric Langlands correspondence]] elements of conformal blocks are naturally thought of ([Beauville-Laszlo 93](#BeauvilleLaszlo93)) as generalized [[theta functions]] (see there for more).


## Properties

### Holographic correspondence

The conformal blocks at least of the [[WZW model]] are by a [[holographic principle|holographic]] correspondence given by the [[space of quantum states]] of 3d [[Chern-Simons theory]]. See at _[[AdS3-CFT2 and CS-WZW correspondence]]_.

### Relation to equivariant elliptic cohomology

For the $G$-[[WZW model]] the assignment of spaces of conformal blocks, hence by the above equivalently modular functor for $G$-[[Chern-Simons theory]] restricted to [[genus of a surface|genus-1 surfaces]] ([[elliptic curves]]) is essentially what is encoded in the universal $G$-[[equivariant elliptic cohomology]] (equivariant [[tmf]]). In fact equivariant elliptic cohomology remembers also the [[local prequantum field theory|pre-quantum]] incarnation of the modular functor as a systems of [[prequantum line bundles]] over Chern-Simons [[phase spaces]] (which are [[moduli stacks of flat connections]]) and remembers the [[quantization]]-process from there to the actual [[space of quantum states]] by forming holomorphic [[sections]]. See at _[equivariant elliptic cohomology -- Idea -- Interpretation in Quantum field theory](equivariant+elliptic+cohomology#InterpretationInQuantumFieldTheory)_ for more on this.


## Related concepts

* [[FFRS-formalism]]

[[!include holographic principle -- table]]

## References

### For 2d CFT

A review is around p. 30 of

* {#Gawedzki99} [[Krzysztof Gawędzki]], _Conformal field theory: a case study_ ([arXiv:hep-th/9904145](http://arxiv.org/abs/hep-th/9904145))

Detailed discussion in terms of [[conformal nets]] is in

* {#BartelsDouglasHenriques14} [[Arthur Bartels]], [[Christopher Douglas]], [[André Henriques]], _Conformal nets II: conformal blocks_ ([arXiv:1409.8672](http://arxiv.org/abs/1409.8672))


See also

* A. Tsuchiya, K. Ueno, Y. Yamada, _Conformal field theory on universal family of stable curves with gauge symmetries_, Adv. Studies in Pure Math. __19__, 459--566, Academic Press (1989) [MR92a:81191](http://www.ams.org/mathscinet-getitem?mr=92a:81191)
* Kenji Ueno, _Conformal field theory with gauge symmetry_, Fields Institute Monographs 2008 [book page](http://www.ams.org/bookstore-getitem/item=FIM-24)

### Relation to theta functions

Relation to [[theta functions]]:

* {#BeauvilleLaszlo93} [[Arnaud Beauville]], [[Yves Laszlo]], _Conformal blocks and generalized theta functions_, Comm. Math. Phys. __164__ (1994), 385 - 419, [euclid](http://projecteuclid.org/euclid.cmp/1104270837), [alg-geom/9309003](http://arxiv.org/abs/alg-geom/9309003), [MR1289330](http://www.ams.org/mathscinet-getitem?mr=1289330)
 
* [[Arnaud Beauville]], _Conformal blocks, fusion rings and the Verlinde formula_, Proc. of the Hirzebruch 65 Conf. on Algebraic Geometry, Israel Math. Conf. Proc. __9__, 75-96 (1996) [pdf](http://math.unice.fr/~beauvill/pubs/Hirz65.pdf)

* [[Krzysztof Gawędzki]], _Lectures on CFT_ (from Park City, published in QFT and strings for mathematicians, Dijkgraaf at al editors, [site](http://www.math.ias.edu/qft), [source](http://www.math.ias.edu/QFT/fall/NewGaw.tex), [dvi](http://www.math.ias.edu/QFT/fall/NewGaw.dvi), [ps](http://www.math.ias.edu/QFT/fall/NewGaw.ps)

* A.A. Beilinson, Yu.I. Manin, V.V. Schechtman, _Sheaves of Virasoro and Neveu-Schwarz algebras_, Lecture Notes in Math. __1289__, Springer 1987, 52&#8211;66 

* A.Mironov, A.Morozov, Sh.Shakirov, _Conformal blocks as Dotsenko-Fateev integral discriminants_, [arxiv/1001.0563](http://arxiv.org/abs/1001.0563)

### For higher dimensional CFT

Conformal blocks for [[self-dual higher gauge theory]] are discussed in

* [[Kiyonori Gomi]], _An analogue of the space of conformal blocks in $(4k+2)$-dimensions_ ([pdf](http://www.math.kyoto-u.ac.jp/~kgomi/papers/acb.pdf))

[[!redirects conformal blocks]]
