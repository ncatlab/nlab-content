
> under construction and incoherent

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

The _Witten genus_ is a [[genus]] with [[coefficients]] in [[power series]] in one variable that may be regarded as the universal [[elliptic genus]].
This arises ([Witten 87](#Witten87)) as the [[large volume limit]] of the [[partition function]] of the [[heterotic string]] (hence in the string worldsheet [[perturbation theory]] about constant [[worldsheet]] configurations). Concretely, as Witten argued, this is a formal [[power series]] in string oscillation modes of the [[A-hat genus]] of the [[tensor powers]] of the [[tangent bundle]] that these modes take values in.

In ([Witten 86](#Witten86)) it is suggested, by regarding the [[superstring]] [[sigma-model]] as [[quantum mechanics]] on the [[smooth loop space]] of its [[target space]], that the Witten genus may be thought of as the [[large volume limit]] of an $S^1$-equivariant [[A-hat genus]] on [[smooth loop space]], hence the [[index]] of a [[Dirac operator]] on loop space; and ever since this suggestion people have tried to make this perspective precise (e.g. [Landweber 99](#Landweber99)). 

A priori the [[coefficients]] of the Witten genus as a genus on [[orientation|oriented]] manifolds are [[formal power series]] over the [[rational numbers]]

$$
  w \;\colon\; M SO_\bullet \longrightarrow \mathbb{Q}[ [ q ] ]
  \,.
$$

In the construction from [[string theory|string physics]] this map is interpeted as sending a [[target space|target]] [[spacetime]] $X$ of the [[superstring]] to the function $w_X(q) = w_X(e^{i \tau})$ which to each modulus $\tau \in \mathbb{C}$ characterizing a toroidal [[Riemann surface]] assigns the [[partition function]] of the [[superstring]] with [[worldsheet]] the [[torus]] $\mathbb{C}/(\mathbb{Z} + \mathbb{Z}\tau)$ andpropagating on [[target space]] $X$.

On manifolds with [[spin structure]] the genus refines to integral power series (via the integrality of the [[A-hat genus]]). Moreover andcrucially, on manifolds with [[string structure]] it takes values in [[modular forms]] for the group $\Gamma_1(2))$

$$
  \array{
     M String_\bullet &\longrightarrow& 
     M_\bullet(\Gamma_1(2)) & \simeq \mathbb{C}[\delta, \epsilon]
     \\
     \downarrow && \downarrow
     \\
     M Spin_\bullet &\longrightarrow& \mathbb{Z}[[ q ] ]
     \\
     \downarrow && \downarrow
     \\
     M SO_\bullet &\longrightarrow& \mathbb{Q}[ [ q ] ]
  }
$$


Observer here that [[topological modular forms]] are the [[coefficient]] [[ring]] 
of the [[E-∞ ring]] [[spectrum]] known as _[[tmf]]_. By the general way in which [[genera]] (see there) tend to appear as [[decategorifications]] of [[homomorphisms]] of [[E-∞ rings]] out of a [[Thom spectrum]], this suggests that the Witten genus is the value on [[homotopy groups]] of a homomorphism of [[E-∞ rings]] of the form

$$
 \sigma \colon M String \longrightarrow tmf
$$

from the [[Thom spectrum]] of [[String bordism]] to the [[tmf]]-spectrum.  This lift of the Witten genus to a universal [[orientation in generalized cohomology|orientation]] in universal [[elliptic cohomology]] indeed exists and is called the _[[sigma-orientation]]_, or the _[[string orientation of tmf]]_.

This construction has been the central motivation behind the search for and construction of [[tmf]] ([Hopkins 94](#Hopkins94)). A construction of the [[string orientation of tmf]] is given in ([Ando-Hopkins-Rezk 10](#AndoHopkinsRezk)) and it is shown that indeed it refines the Witten genus ([Ando-Hopkins-Rezk 10, prop. 15.3](#AndoHopkinsRezk)).

It is maybe noteworthy that [[tmf]] (and hence its universal string orientation) also arises canonically from just studying [[chromatic homotopy theory]] (see [Mazel-Gee 13](#tmf#MazelGee13) for a nice survey of this) a fundamental topic in [[stable homotopy theory]], hence a fundamental topic in [[mathematics]]. Therefore in the Witten genus some very fundamental pure mathematics happens to euivalently incarnate as some conjecturally very fundamental [[physics]] ([[string theory]]).


## Properties

### Characteristic series

The [[characteristic series]] of the Witten genus as a [[power series]] in $z$ with [[coefficients]] in formalpower series over $\mathbb{Q}$ is

$$
  \frac{z/2}{sinh(z/2)}
  \prod_{n \geq 1}
  \frac{(1-q^n)^2}{(1-q^n e^z)(1-q^n e^{-z})}
$$

### Integrality and modularity

The Witten genus takes values in $\mathbb{Z}[ [ q ] ]$ on manifolds with [[spin structure]] (by its expression as a power series of [[A-hat genera]] and their integrality on spin manifolds). 

On manifolds with [[string structure]] then its takes values in (the $q$-expansion of) [[modular forms]] for $SL_2(\mathbb{Z})$, meaning that setting $q = e^{2 \pi i \tau}$ then as a function $f$ of the parameter $\tau$ taking vakues in the [[upper half plane]] the Witten genus satisfies


$$
  f(-1/\tau) = (-\tau)^n f(\tau)
  \,.
$$


### Stolz conjecture

The _[[Stolz conjecture]]_ due to ([Stolz 96](#Stolz96)) asserts that if $X$ is a [[closed manifold]] with [[String structure]] which furthermore admits a [[Riemannian metric]] with [[positive number|positive]] [[Ricci curvature]], then its Witten genus vanishes.




## Related concepts

* [[elliptic Chern character]]

[[!include genera and partition functions - table]]

## References
 {#References}

### General
 {#ReferencesGeneralCase}

The original description of the Witten genus from [[string theory]] is due to

* {#Witten87} [[Edward Witten]],  _Elliptic Genera And Quantum Field Theory_ , Commun.Math.Phys. 109 525 (1987) ([Euclid](http://projecteuclid.org/euclid.cmp/1104117076))


* {#Witten86} [[Edward Witten]], _The Index Of The Dirac Operator In Loop Space_ Proc. of Conf. on Elliptic Curves and Modular Forms in Algebraic Topology Princeton (1986).

Rigorous formulations then appeared in

* [[Clifford Taubes]],  _$S^1$ actions and elliptic genera_, Comm. Math. Phys., 122(3):455&#8211;526, 1989.

* [[Raoul Bott]], [[Clifford Taubes]], _On the rigidity theorems of Witten_, J. of the Amer. Math. Soc., 2, 1989.

A simpler proof and many further cases were then discussed by [[Kefeng Liu]]. 

That it takes a [[string structure]] to make the elliptic genus land in [[modular forms]] was noticed in 

* [[Don Zagier]], _Note on the Landweber-Stong elliptic genus_ 1986 ([pdf](http://people.mpim-bonn.mpg.de/zagier/files/doi/10.1007/BFb0078047/fulltext.pdf))

Surveys are in

* [[Gerald Höhn]], _Complex elliptic genera and $S^1$-equivariant cobordism theory_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0405/0405232v1.pdf))

* [[Anand Dessai]], _Some geometric properties of the Witten genus_ ([pdf](http://homeweb2.unifr.ch/dessaia/pub/papers/Arolla/DessaiArollaFinalRevised30June09.pdf))

Further discussion of the idea of Dirac operators on loop space includes

* C. H. Taubes, _$S^1$-actions and elliptic genera_, Commun. Math. Phys. 122, 455-526 (1989)

* {#Landweber99} [[Gregory Landweber]], _Dirac operators on loop space_ PhD thesis (Harvard 1999) ([pdf](http://math.bard.edu/greg/LoopDirac.pdf))


Further discussion of the relation to [[quantum anomalies]] and the [[Green-Schwarz mechanism]] ([[string structure]], [[string^c structure]]) is in 

* [[Wolfgang Lerche]], B. Nilsson, A. Schellekens, N. Warner, _Anomaly cancelling terms from the elliptic genus_ (1987) ([pdf](http://lerche.web.cern.ch/lerche/papers/ellgenus1.pdf))

* Qingtao Chen, [[Fei Han]], Weiping Zhang, _Generalized Witten Genus and Vanishing Theorems_, JDG, 88 (2011) 1-39 ([arXiv:1003.2325](http://arxiv.org/abs/1003.2325))

Discussion of the Witten genus via a KO-valued Chern-character on elliptic cohomology is in 

* [[Haynes Miller]], _The elliptic character and the Witten genus_, Contemporary mathematics, volume 96, 1989 ([pdf](http://dedekind.mit.edu/~hrm/papers/ell-char.pdf))


The refinement of the Witten genus from values in [[modular forms]] to [[topological modular forms]] and further to a morphism of [[E-∞ rings]], hence to the [[string orientation of tmf]] is due to 

* {#Hopkins94} [[Michael Hopkins]], _Topological modular forms, the Witten Genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematics, Z&#252;rich 1994 ([pdf](http://www.mathunion.org/ICM/ICM1994.1/Main/icm1994.1.0554.0565.ocr.pdf))

* [[Michael Hopkins]], _Algebraic topology and modular forms_, Proceedings of the ICM, Beijing 2002, vol. 1, 283--309 ([arXiv:math/0212397](http://arxiv.org/abs/math/0212397))

* [[Matthew Ando]], [[Michael Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))
  {#AndoHopkinsRezk}

see also remark 1.4 of

* [[Paul Goerss]], _Topological modular forms (after Hopkins, Miller and Lurie)_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0910/0910.5130v1.pdf)).

and for more on the [[sigma-orientation]] see

* [[Matthew Ando]], _The sigma orientation for analytic circle-equivariant elliptic cohomology_, Geom. Topol. 7 (2003) 91-153 ([arXiv:math/0201092](http://arxiv.org/abs/math/0201092))

* [[Matthew Ando]], Maria Basterra, _The Witten genus and equivariant elliptic cohomology_ ([arXiv:0008192](http://arxiv.org/abs/math/0008192))


Discussion of the relation to [[vertex operator algebras]] is in 

* Chongying Dong, _Elliptic Genus and Vertex Operator Algebras_, ([pdf](http://www.math.jussieu.fr/~ma/mypubli/dlvoaPAMQ05.pdf))

The [[Stolz conjecture]] on the Witten genus is due to

* {#Stolz96} [[Stephan Stolz]], _A conjecture concerning positive Ricci curvature and the Witten genus_, Mathematische Annalen Volume 304, Number 1 (1996),

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
 {#ReferencesTwistedCase}

The twisted Witten genus in the present of [[background gauge field]] hence for a [[twisted string structure]]/[[string^c structure]] was considered in 

* Qingtao Chen, [[Fei Han]], [[Weiping Zhang]], _Generalized Witten Genus and Vanishing Theorems_ ([arXiv:1003.2325](http://arxiv.org/abs/1003.2325))

For the moment see the references at _[[string^c structure]]_ for more on this.

[[!redirects Witten genera]]

[[!redirects twisted Witten genus]]
[[!redirects twisted Witten genera]]
