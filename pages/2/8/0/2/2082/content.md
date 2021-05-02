
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The notion of _quantum group_ refers to various objects which are deformations of ([[algebras of functions]] on) [[groups]], but still have very similar properties to (algebras of functions on) groups, and in particular to [[semisimple Lie groups]]. Most important are the [[Hopf algebras]] _deforming_ the function algebras on [[semisimple Lie groups]] or to the enveloping algebras of Kac-Moody Lie algebras.

## Overview

It is a common experience in [[representation theory]] that a number of mathematical structures behaves very similarly to [[algebraic group|algebraic]] or [[Lie group|Lie]] groups. After the impetus of the theory of quantum [[integrable systems]], mainly the work of Leningrad's school of mathematical physics around 1980, several mathematicians (including Drinfeld, Manin, Woronowicz, Jimbo, Faddeev--Reshetikhin--Takhtajan) found, in different formalisms, major series of examples which are mostly noncommutative noncocommutative [[Hopf algebras]] and which deform enveloping algebras of (semisimple) Lie algebras, or algebras of functions on the corresponding algebraic groups. These deformations $G_q$ depend on a parameter $q$ (sometimes one prefers a formal parameter $h$ with $q = e^{h}$), which may be taken as belonging to the [[ground field]], but also being formal (transcendental over the ground field). A peculiar case is when the parameter $q$ of the deformation is an $l$-th root of unity; the remaining cases are usually called generic $q$.

The [[representation theory]] for these 'quantum' examples is highly developed; in fact many phenomena in the representation theory of semisimple Lie algebras (e.g. canonical bases) were discovered first as a limiting case of constructions in the quantum case, which become degenerate in the classical case (the principle that quantization removes degeneracy). While representations for generic $q$ parallel classical ones, the theory at roots of unity is peculiar and related to the representation theory of affine Lie algebras; the quantum groups at roots of unity as algebras have big centers. 

Nowadays, both the class of examples and the class of formalisms has been extended a lot, hence the term 'quantum group' is not a fixed notion but rather a collective term for a rather author-dependent class of group-like objects, most often subclasses or extensions of the concept of Hopf algebras which are sometimes required to belong to families of deformations of their classical counterparts. One of the common features is that if we forget the group-like features, the examples belong to the class of noncommutative spaces (see [[noncommutative geometry]]).  

Mathematically better defined are notions (sometimes equated by various authors with the class of quantum groups) like [[quasitriangular Hopf algebras]], [[quantum matrix groups]] (quantum linear groups, more general FRT-algebras and Majid's $A(R)$ where $R$ is a [[quantum Yang-Baxter matrix|quantum Yang-Baxter equation]]), quantized enveloping algebras, quantum function algebras, compact matrix pseudogroups, Kac algebras, Yangians etc. The representations of quasitriangular Hopf algebras form [[braided monoidal categories]], which are in main examples related to the mathematics of Iwahori--Hecke algebras, braid groups, knot theory, finite group Chern--Simons theory and Wess--Zumino--Novikov--Witten theory of [[CFT]]. One should note that in the classical limit quantum function algebras give not simply (functions on) algebraic (or Lie) groups but also a compatible (= multiplicative) Poisson structure giving rise to Poisson--Lie or Poisson algebraic groups. 

There is an extensive geometric theory of homogeneous spaces for quantum groups and [[fiber bundles]] whose structure groups are quantum groups. 

## Properties

### Tannaka duality

[[!include structure on algebras and their module categories - table]]

## Related concepts

* [[Hopf algebra]], [[bialgebra]], [[gebra]], [[braided monoidal category]], [[noncommutative algebraic geometry]], [[noncommutative geometry]], [[Hopf-Galois extension]], [[matrix bialgebra]], [[Knizhnik-Zamolodchikov equation]], [[Tannaka duality]], [[Yangian]], [[Yang-Baxter equation]], [[classical Yang-Baxter equation]], [[quantum Yang-Baxter equation]], [[dynamical Yang-Baxter equation]], [[quantum linear group]], [[quantized function algebra]], [[quantized enveloping algebra]]

* [[Poisson Lie group]]

* [[quantum 2-group]]

## References

* [[Vladimir Drinfel'd|V. G. Drinfel'd]], _Quantum groups_, Proceedings of the International Congress of Mathematicians 986, Vol. 1, 798&#8211;820, AMS 1987 ([djvu:1.3M](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0798.0820.ocr.djvu), [pdf:2.5M](http://www.mathunion.org/ICM/ICM1986.1/Main/icm1986.1.0798.0820.ocr.pdf))

* [[Christian Kassel]], _Quantum groups_, Graduate Texts in Mathematics __155__, Springer 1995 ([doi:10.1007/978-1-4612-0783-2](https://link.springer.com/book/10.1007/978-1-4612-0783-2), [webpage](http://www-irma.u-strasbg.fr/~kassel/QGbk.html), [errata pdf](http://www-irma.u-strasbg.fr/~kassel/QGerrata030399.pdf))


* [[Shahn Majid]], _Foundations of quantum group theory_, Cambridge University Press 1995, 2000.

* [[Yuri Manin|Yu. I. Manin]], _Quantum groups and non-commutative geometry_, CRM, Montreal 1988.

* B. Parshall, J.Wang, _Quantum linear groups_, Mem. Amer. Math. Soc. 89(1991), No. 439, vi+157 pp.

* N. Yu. Reshetikhin, L. A. Takhtajan, L. D. Faddeev, _Quantization of Lie groups and Lie algebras_, Algebra i analiz __1__, 178 (1989) (Russian), English translation in Leningrad Math. J. 1.

* [[Arun Ram]], _A survey of quantum groups: background, motivation, and results_, in: Geometric analysis and Lie theory in mathematics and physics, A. Carey and M. Murray eds., Australian Math. Soc. Lecture Notes Series __11__, Cambridge Univ. Press 1997, pp. 20-104. [pdf](http://www.ms.unimelb.edu.au/~ram/Publications/1997AustMSLectNotesv11p20.pdf)

* P. Etingof, O. Schiffmann, _Lectures on Quantum Groups_, Lectures in Math. Phys., International Press (1998).

* P.Etingof, I. Frenkel, _Lectures on representation theory and Knizhnik-Zamolodchikov equations_

* A. U. Klymik, K. Schmuedgen, _Quantum groups
and their representations_, Springer 1997.

* A. Joseph, _Quantum groups and their primitive ideals_,
Springer 1995.

* [[Ross Street]], _Quantum groups : a path to current algebra_, Cambridge Univ. Press 2007

* L. I. Korogodski, Ya. S. Soibelman, _Algebras of functions on quantum groups I_, Math. Surveys and Monographs 56, AMS 1998.

* A. Varchenko, _Hypergeometric functions and representation theory of Lie algebras and quantum groups_, Advanced Series in Mathematical Physics, Vol. 21, World Scientific (1995) 

* [[George Lusztig]], _Introduction to quantum groups_

* V. Chari, A. Pressley, _A guide to quantum groups_, Camb. Univ. Press 1994 


* Bangming Deng, Jie Du, [[Brian Parshall]], Jianpan Wang, _Finite dimensional algebras and quantum groups_, Mathematical Surveys and Monographs __150__, Amer. Math. Soc. 2008. xxvi+759 pp. [MR2009i:17023)](http://www.ams.org/mathscinet-getitem?mr=2457938)

* [[Tom Bridgeland]], _Quantum groups via Hall algebras of complexes_, Annals of Mathematics __177__:2 (2013) 739-759 (21 pages) 



In relation to [[hypergeometric functions]] and the [[Knizhnik-Zamolodchikov equation]]:

* [[Alexander Varchenko]], _Multidimensional hypergeometric functions and representation theory of Lie algebras and quantum groups_, Adv. Ser. in Math. Phys. __21__, World Sci. Publ. 1995. x+371 pp. ([doi:10.1142/2467](https://doi.org/10.1142/2467))

* V. Tarasov, [[Alexander Varchenko]], _Geometry of $q$-hypergeometric functions, quantum affine algebras and elliptic quantum groups_, Ast&#233;risque __246__ (1997), vi+135 pp. ([arXiv:q-alg/9703044](https://arxiv.org/abs/q-alg/9703044), [numdam:AST_1997__246__R1_0](http://www.numdam.org/item/AST_1997__246__R1_0))

See also:

* MathOverflow: [q.gr. as relative Drinfeld double](http://mathoverflow.net/questions/20683/quantum-group-as-relative-drinfeld-double), [why Drinfeld-Jimbo q.gr.](http://mathoverflow.net/questions/5538/why-drinfeld-jimbo-type-quantum-groups), [Lusztig perverse sheaves on quiver varieties](http://mathoverflow.net/questions/14361/what-do-the-local-systems-in-lusztigs-perverse-sheaves-on-quiver-varieties-look), [canonical bases for extended q.env.algebras](http://mathoverflow.net/questions/8110/canonical-basis-for-the-extended-quantum-enveloping-algebras), [groups-qgroups-and-... (on elliptic case)](http://mathoverflow.net/questions/58040/groups-quantum-groups-and-fill-in-the-blank), [all posts with quantum group tag](http://mathoverflow.net/questions/tagged/quantum-group)

category: noncommutative geometry
[[!redirects quantum groups]]