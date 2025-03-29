
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

* [[quantum algebra]]
* [[noncommutative geometry]], [[noncommutative algebraic geometry]], [[deformation quantization]]

* [[quantum inverse scattering method]], [[Knizhnik-Zamolodchikov equation]], [[Tannaka duality]], [[Yang-Baxter equation]], [[classical Yang-Baxter equation]], [[quantum Yang-Baxter equation]], [[dynamical Yang-Baxter equation]], [[reflection equation]]
* [[Hopf algebra]], [[bialgebra]], [[gebra]], [[Yangian]], [[RTT algebra]], [[matrix bialgebra]], [[quantum linear group]], [[quantized function algebra]], [[quantized enveloping algebra]]
* [[braided monoidal category]], [[quantum double]], [[Heisenberg double]], [[Yetter-Drinfeld module]]
* [[quantum homogeneous space]], [[quantum flag manifold]], [[quantum symmetric pair]], [[Hopf-Galois extension]], [[noncommutative principal bundle]]

* [[Poisson Lie group]], [[dressing action]]

* [[quantum 2-group]]

* [[quantum topology]]


## References


* {#Drinfeld87} [[Vladimir Drinfeld]], _Quantum groups_, in: A. Gleason (ed.) *[Proceedings of the](https://archive.org/details/proceedingsofint0002inte_v5c3/mode/2up) [1986 International Congress of Mathematics](https://inspirehep.net/conferences/966215?ui-citation-summary=true)* **1** (1987) 798--820 &lbrack;[pdf](https://www.mathunion.org/fileadmin/ICM/Proceedings/ICM1986.1/ICM1986.1.ocr.pdf)&rbrack;

  expanded version:

  Journal of Soviet Mathematics **41** (1988) 898--915 &lbrack;[doi:10.1007/BF01247086](https://doi.org/10.1007/BF01247086)&rbrack;

* {#Tjin92} [[Tjark Tjin]], *An introduction to quantized Lie groups and algebras*, Int. J. Mod. Phys. A **7** (1992) 6175--6213 &lbrack;[arXiv:hep-th/9111043](https://arxiv.org/abs/hep-th/9111043), [doi:10.1142/S0217751X92002805](https://doi.org/10.1142/S0217751X92002805)&rbrack;


* [[Christian Kassel]]: *Quantum groups*, Graduate Texts in Mathematics __155__, Springer (1995) &lbrack;[doi:10.1007/978-1-4612-0783-2](https://link.springer.com/book/10.1007/978-1-4612-0783-2), [webpage](http://www-irma.u-strasbg.fr/~kassel/QGbk.html), [errata pdf](http://www-irma.u-strasbg.fr/~kassel/QGerrata030399.pdf)&rbrack;

* [[Yuri Manin|Yu. I. Manin]], _Quantum groups and non-commutative geometry_, CRM Press (1988)

* [[Nikolai Reshetikhin|N. Yu. Reshetikhin]], [[Leon  Takhtajan|L. A. Takhtajan]], [[Ludwig Fadeev|L. D. Faddeev]], _Quantization of Lie groups and Lie algebras_, Algebra i analiz __1__, 178 (1989) (Russian), English translation in Leningrad Math. J. 1.

* [[Brian Parshall]], J.Wang, _Quantum linear groups_, Mem. Amer. Math. Soc. **89** 439 (1991)

* V. Chari, [[Andrew Pressley]], _A guide to quantum groups_, Camb. Univ. Press (1994)


* A. Joseph, _Quantum groups and their primitive ideals_, Springer (1995)

* [[Shahn Majid]], _Foundations of quantum group theory_, Cambridge University Press (1995, 2000)

* [[Alexander Varchenko]]: _Hypergeometric functions and representation theory of Lie algebras and quantum groups_, Advanced Series in Mathematical Physics **21**, World Scientific (1995) 


* [[Larry A. Lambe]], [[David E. Radford]]: *Introduction to the quantum Yang-Baxter equation and quantum groups: an algebraic approach*, Mathematics and Its Applications __423__, Springer, Kluwer (1997) &lbrack;[doi:10.1007/978-1-4615-4109-7](https://doi.org/10.1007/978-1-4615-4109-7)&rbrack;


* [[Arun Ram]], _A survey of quantum groups: background, motivation, and results_, in: Geometric analysis and Lie theory in mathematics and physics, A. Carey and M. Murray eds., Australian Math. Soc. Lecture Notes Series __11__, Cambridge Univ. Press (1997) 20-104 &lbrack;[pdf](http://www.ms.unimelb.edu.au/~ram/Publications/1997AustMSLectNotesv11p20.pdf)&rbrack;

* A. U. Klymik, K. Schmuedgen, _Quantum groups and their representations_, Springer (1997)

* L. I. Korogodski, [[Yan S. Soibelman]]: _Algebras of functions on quantum groups I_, Math. Surveys and Monographs 56, AMS (1998)

* [[Pavel Etingof]], O. Schiffmann, _Lectures on Quantum Groups_, Lectures in Math. Phys., International Press (1998)


* {#EtingofFrenkelKirillov98} [[Pavel Etingof]], [[Igor Frenkel]], [[Alexander Kirillov]], *Lectures on Representation Theory and Knizhnik-Zamolodchikov Equations*, Mathematical surveys and monographs **58**, American Mathematical Society (1998) &lbrack;[ISBN:978-1-4704-1285-2](https://bookstore.ams.org/surv-58), [review pdf](http://www.ams.org/journals/bull/2000-37-02/S0273-0979-00-00853-3/S0273-0979-00-00853-3.pdf)&rbrack;


* [[Ross Street]], _Quantum groups : a path to current algebra_, Cambridge Univ. Press (2007)

* Bangming Deng, Jie Du, [[Brian Parshall]], Jianpan Wang, _Finite dimensional algebras and quantum groups_, Mathematical Surveys and Monographs __150__, Amer. Math. Soc. (2008) [MR2009i:17023)](http://www.ams.org/mathscinet-getitem?mr=2457938)


* [[George Lusztig]], _Introduction to quantum groups_ (2010) &lbrack;[doi:10.1007/978-0-8176-4717-9](https://doi.org/10.1007/978-0-8176-4717-9)&rbrack;


* [[Tom Bridgeland]], _Quantum groups via Hall algebras of complexes_, Annals of Mathematics __177__:2 (2013) 739--759 (21 pages) 

* [[Richard Borcherds]], [[Mark Haiman]], [[Theo Johnson-Freyd]], [[Nicolai Reshetikhin]], [[Vera Serganova]], *Berkeley Lectures on Lie Groups and Quantum Groups* (2020) &lbrack;[pdf](http://categorified.net/LieQuantumGroups.pdf)&rbrack;


Lecture notes on [[Hopf algebras]] and quantum groups in view of [[topological field theory]]:

* [[Christoph Schweigert]]: *Hopf algebras, quantum groups and topological field theory*, lecture notes (2022) &lbrack;[pdf](https://www.math.uni-hamburg.de/home/schweigert/skripten/hskript.pdf)&rbrack;


In relation to [[hypergeometric functions]] and the [[Knizhnik-Zamolodchikov equation]]:

* [[Alexander Varchenko]], _Multidimensional hypergeometric functions and representation theory of Lie algebras and quantum groups_, Adv. Ser. in Math. Phys. __21__, World Sci. Publ. 1995. x+371 pp. ([doi:10.1142/2467](https://doi.org/10.1142/2467))

* V. Tarasov, [[Alexander Varchenko]], _Geometry of $q$-hypergeometric functions, quantum affine algebras and elliptic quantum groups_, Ast&#233;risque __246__ (1997), vi+135 pp. ([arXiv:q-alg/9703044](https://arxiv.org/abs/q-alg/9703044), [numdam:AST_1997__246__R1_0](http://www.numdam.org/item/AST_1997__246__R1_0))

In the generality of [[noncartesian internal categories]]:

* [[Marcelo Aguiar]],  *Internal categories and quantum groups*, PhD thesis, Cornell 1997 ([pdf](http://pi.math.cornell.edu/~maguiar/thesis2.pdf), [[Aguiar_InternalCategoriesAndQuantumGroups.pdf:file]]) 

On elliptic quantum groups:

* [[Hitoshi Konno]], *Elliptic Quantum Groups*,  in *[[Encyclopedia of Mathematical Physics 2nd ed]]*, Elsevier (2024) &lbrack;[arXiv:2405.11193](https://arxiv.org/abs/2405.11193)&rbrack;


See also:

* MathOverflow: [q.gr. as relative Drinfeld double](http://mathoverflow.net/questions/20683/quantum-group-as-relative-drinfeld-double), [why Drinfeld-Jimbo q.gr.](http://mathoverflow.net/questions/5538/why-drinfeld-jimbo-type-quantum-groups), [Lusztig perverse sheaves on quiver varieties](http://mathoverflow.net/questions/14361/what-do-the-local-systems-in-lusztigs-perverse-sheaves-on-quiver-varieties-look), [canonical bases for extended q.env.algebras](http://mathoverflow.net/questions/8110/canonical-basis-for-the-extended-quantum-enveloping-algebras), [groups-qgroups-and-... (on elliptic case)](http://mathoverflow.net/questions/58040/groups-quantum-groups-and-fill-in-the-blank), [all posts with quantum group tag](http://mathoverflow.net/questions/tagged/quantum-group)

category: noncommutative geometry
[[!redirects quantum groups]]