
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
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

The original _Witten genus_ is an [[elliptic genus]] evaluated on the [[Tate curve]], hence a [[genus]] for [[string structure]]-[[cobordisms]] with values in [[topological modular forms]].

Witten obtained this originally as the [[partition function]] of the [[heterotic string]] in the [[perturbation theory]] about constant [[worldsheet]] configurations. This is what the [[Tate curve]] expresses.

The universal [[elliptic genus|elliptic]] [[genus]] is a morphism $\phi_2 : \Omega_\bullet^{SO} \otimes \mathbb{C} \to M_\bullet(\Gamma_1(2)) \simeq \mathbb{C}[\delta, \epsilon]$ from the complexified [[cobordism ring]].
[[Edward Witten]] argued that the value of the elliptic genus on $X$ can be understood as the $S^1$-[[equivariant cohomology|equivariant]] [[index]] of a [[Dirac operator]] on a [[loop space]] $\mathcal{L} X$.

As such it can be understood as the [[partition function]] of an $N=1$ $d=2$ [[sigma-model]] [[SCFT]] ("the [[heterotic string]]"). Formalizations of this construction exist both in [[AQFT]]-type ([Costello](#Costello)) and in [[FQFT]]-type [[quantum field theory]] ([Stolz-Teichner]())

This can be refined to a morphism of [[ring spectra]] ([Ando-Hopkins-Rezk 10](#AndoHopkinsRezk))

$$
 \sigma : MString \to tmf
$$

from the [[Thom spectrum]] of [[String bordism]] to the [[tmf]]-spectrum, also called the _[[sigma-orientation]]_, the [[string orientation of tmf]].

## Related concepts

[[!include genera and partition functions - table]]

## References
 {#References}

### General

The original reference on the [[string theory|string theoretic]] analytic interpretation of [[elliptic genera]] and on the Witten genus is

* [[Edward Witten]], 

  * _Elliptic Genera And Quantum Field Theory_ , Commun.Math.Phys. 109 525 (1987) ([Euclid](http://projecteuclid.org/euclid.cmp/1104117076))


  * _The Index Of The Dirac Operator In Loop Space_ Proc. of Conf. on Elliptic Curves and Modular Forms in Algebraic Topology Princeton (1986).

Rigorous formulations of the relation then appeared in

* [[Clifford Taubes]],  _$S^1$ actions and elliptic genera_, Comm. Math. Phys., 122(3):455&#8211;526, 1989.

* [[Raoul Bott]], [[Clifford Taubes]], _On the rigidity theorems of Witten_, J. of the Amer. Math. Soc., 2, 1989.

A simpler proof and many further cases were then discussed by [[Kefeng Liu]]. 

That it takes a [[string structure]] to make the elliptic genus land in [[modular forms]] was noticed in 

* [[Don Zagier]], _Note on the Landweber-Stong elliptic genus_ 1986 ([pdf](http://people.mpim-bonn.mpg.de/zagier/files/doi/10.1007/BFb0078047/fulltext.pdf))

Surveys are in

* [[Gerald Höhn]], _Complex elliptic genera and $S^1$-equivariant cobordism theory_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0405/0405232v1.pdf))

* Anand Dessai, _Some geometric properties of the Witten genus_ ([pdf](http://homeweb2.unifr.ch/dessaia/pub/papers/Arolla/DessaiArollaFinalRevised30June09.pdf))


Further discussion of the relation to [[quantum anomalies]] and the [[Green-Schwarz mechanism]] ([[string structure]], [[string^c structure]]) is in 

* [[Wolfgang Lerche]], B. Nilsson, A. Schellekens, N. Warner, _Anomaly cancelling terms from the elliptic genus_ (1987) ([pdf](http://lerche.web.cern.ch/lerche/papers/ellgenus1.pdf))

* Qingtao Chen, [[Fei Han]], Weiping Zhang, _Generalized Witten Genus and Vanishing Theorems_, JDG, 88 (2011) 1-39 ([arXiv:1003.2325](http://arxiv.org/abs/1003.2325))

Discussion of the Witten genus via a KO-valued Chern-character on elliptic cohomology is in 

* [[Haynes Miller]], _The elliptic character and the Witten genus_, Contemporary mathematics, volume 96, 1989 ([pdf](http://dedekind.mit.edu/~hrm/papers/ell-char.pdf))


The refinement of the Witten genus from values in [[modular forms]] to [[topological modular forms]] and further to a morphism of [[E-∞ rings]], hence to the [[string orientation of tmf]] is due to 

* [[Michael Hopkins]], _Topological modular forms, the Witten Genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematics, Z&#252;rich 1994 ([pdf](http://www.mathunion.org/ICM/ICM1994.1/Main/icm1994.1.0554.0565.ocr.pdf))

* [[Michael Hopkins]], _Algebraic topology and modular forms_, Proceedings of the ICM, Beijing 2002, vol. 1, 283--309 ([arXiv:math/0212397](http://arxiv.org/abs/math/0212397))

* [[Matthew Ando]], [[Michael Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))
  {#AndoHopkinsRezk}

see also remark 1.4 of

* [[Paul Goerss]], _Topological modular forms (after Hopkins, Miller and Lurie)_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0910/0910.5130v1.pdf)).

and for more on the [[sigma-orientation]] see

* [[Matthew Ando]], _The sigma orientation for analytic circle-equivariant elliptic cohomology_, Geom. Topol. 7 (2003) 91-153 ([arXiv:math/0201092](http://arxiv.org/abs/math/0201092))


Discussion of the relation to [[vertex operator algebras]] is in 

* Chongying Dong, _Elliptic Genus and Vertex Operator Algebras_, ([pdf](http://www.math.jussieu.fr/~ma/mypubli/dlvoaPAMQ05.pdf))

Other references include

* [[Stephan Stolz]], _A conjecture concerning positive Ricci curvature and the Witten genus_, Mathematische Annalen Volume 304, Number 1 (1996),

* [[Matthew Ando]], Maria Basterra, _The Witten genus and equivariant elliptic cohomology_ ([arXiv:0008192](http://arxiv.org/abs/math/0008192))

Constructions of the [[sigma-model]] [[QFT]] that is supposed to give the Witten genus are proposed 

in terms of [[chiral differential operators]] in

* V. Gorbounov, F. Malikov and V. Schechtman, _Gerbes of chiral differential operators_, Math. Res. Lett. 7(1), 55&#8211;66 (2000) ([arXiv:math/9906117](http://arxiv.org/abs/math/9906117), [arXiv:math/0003170](http://arxiv.org/abs/math/0003170), [arXiv:math/0005201](http://arxiv.org/abs/math/0005201))

in terms of [[vertex operator algebra]] in 

* Pokman Cheung, _The Witten genus and vertex algebras_ ([arXiv:0811.1418](http://arxiv.org/abs/0811.1418))

in terms of [[FQFT]] in 

* [[Stephan Stolz]], [[Peter Teichner]], _Supersymmetric field theories and generalized cohomology_ in _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ ([arXiv:1108.0189](http://arxiv.org/abs/1108.0189))
  {#StolzTeichner}

and in terms of [[factorization algebra]] in 

* [[Kevin Costello]], _A geometric construction of the Witten genus, II_ ([arXiv:1112.0816](http://arxiv.org/abs/1112.0816))
 {#Costello}

### Twisted case

The twisted Witten genus in the present of [[background gauge field]] hence for a [[twisted string structure]]/[[string^c structure]] was considered in 

* Qingtao Chen, [[Fei Han]], [[Weiping Zhang]], _Generalized Witten Genus and Vanishing Theorems_ ([arXiv:1003.2325](http://arxiv.org/abs/1003.2325))

For the moment see the references at _[[string^c structure]]_ for more on this.

[[!redirects Witten genera]]

[[!redirects twisted Witten genus]]
[[!redirects twisted Witten genera]]

