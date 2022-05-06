

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
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

The _Witten genus_ is a [[genus]] with [[coefficients]] in [[power series]] in one variable, playing the role of a universal [[elliptic genus]].
This arises ([Witten 87](#Witten87)) as the [[large volume limit]] of the [[partition function]] of the [[superstring]] (hence in the string worldsheet [[perturbation theory]] about constant [[worldsheet]] configurations). Specifically, for the [[type II superstring]] this reproduces the universal [[elliptic genus]] as previously introduced by [[Serge Ochanine]], while for the [[heterotic string]] it yields what is now called the Witten genus proper.
Concretely, as Witten argued, this is a formal [[power series]] in string oscillation modes of the [[A-hat genus]] of the symmetric [[tensor powers]] of the [[tangent bundle]] that these modes take values in.

In ([Witten 86](#Witten86)) it is suggested, by regarding the [[superstring]] [[sigma-model]] as [[quantum mechanics]] on the [[smooth loop space]] of its [[target space]], that the Witten genus may be thought of as the [[large volume limit]] of an $S^1$-equivariant [[A-hat genus]] on [[smooth loop space]], hence the [[index]] of the [[Dirac-Ramond operator]] in that limit.  (Ever since this suggestion people have tried to make precise the concept of Dirac operator on a [[smooth loop space]] (e.g. [Alvarez-Killingback-Mangano-Windey 87](#AlvarezKillingbackManganoWindey87)). But notice that, by the above, only the [[formal loop space]] and the [[Dirac-Ramond operator]] really appears in the definition of the Witten genus.)

A priori the [[coefficients]] of the Witten genus as a genus on [[orientation|oriented]] manifolds are [[formal power series]] over the [[rational numbers]]

$$
  w \;\colon\; M SO_\bullet \longrightarrow \mathbb{Q}[ [ q ] ]
  \,.
$$

In the construction from [[string theory|string physics]] this map is interpreted as sending a [[target space|target]] [[spacetime]] $X$ of the [[superstring]] to the function $w_X(q) = w_X(e^{2 \pi i \tau})$ which to each modulus $\tau \in \mathbb{C}$ characterizing a toroidal [[Riemann surface]] assigns the [[partition function]] of the [[superstring]] with [[worldsheet]] the [[torus]] $\mathbb{C}/(\mathbb{Z} + \mathbb{Z}\tau)$ and propagating on [[target space]] $X$.

On manifolds with [[spin structure]] the genus refines to integral power series (via the integrality of the [[A-hat genus]] ([Chudnovsky-Chudnovsky 88](#ChudnovskyChudnovsky88), [Kreck-Stolz 93](#KreckStolz93), [Hovey 91](#Hovey91)). Moreover on manifolds with rational string structure it takes values in [[modular forms]] ([Zagier 86](#Zagier86)) and crucially, on manifolds with [[string structure]] it takes values in [[topological modular forms]] 

$$
  \array{
     M String_\bullet &\longrightarrow& 
     tmf_\bullet
       \\
     \downarrow && \downarrow
     \\
     \Omega_\bullet^{String, rat} &\longrightarrow& MF_\bullet  
     \\
     \downarrow && \downarrow
     \\
     M Spin_\bullet &\longrightarrow& \mathbb{Z}[[ q ] ]
     \\
     \downarrow && \downarrow
     \\
     M SO_\bullet &\stackrel{w}{\longrightarrow}& \mathbb{Q}[ [ q ] ]
  }
  \,.
$$

(On the left is the image under forming [[Thom spectra]]/[[cobordism rings]] of the first stages in the [[Whitehead tower]] of $BO$, see also at _[[higher spin structure]]_.)

Observe here that [[topological modular forms]] are the [[coefficient]] [[ring]] 
of the [[E-∞ ring]] [[spectrum]] known as _[[tmf]]_. By the general way in which [[genera]] (see there) tend to appear as [[decategorifications]] of [[homomorphisms]] of [[E-∞ rings]] out of a [[Thom spectrum]], this suggests that the Witten genus is the value on [[homotopy groups]] of a homomorphism of [[E-∞ rings]] of the form

$$
 \sigma \colon M String \longrightarrow tmf
$$

from the [[Thom spectrum]] of [[String bordism]] to the [[tmf]]-spectrum.  This lift of the Witten genus to a universal [[orientation in generalized cohomology|orientation]] in universal [[elliptic cohomology]] indeed exists and is called the _[[sigma-orientation]]_, or the _[[string orientation of tmf]]_.

This construction has been the central motivation behind the search for and construction of [[tmf]] ([Hopkins 94](#Hopkins94)). A construction of the [[string orientation of tmf]] is given in ([Ando-Hopkins-Rezk 10](#AndoHopkinsRezk)) and it is shown that indeed it refines the Witten genus ([Ando-Hopkins-Rezk 10, prop. 15.3](#AndoHopkinsRezk)).

It is maybe noteworthy that [[tmf]] (and hence its universal string orientation) also arises canonically from just studying [[chromatic homotopy theory]] (see [Mazel-Gee 13](#tmf#MazelGee13) for a nice survey of this) a fundamental topic in [[stable homotopy theory]], hence a fundamental topic in [[mathematics]]. Therefore in the Witten genus some very fundamental pure mathematics happens to equivalently incarnate as some conjecturally very fundamental [[physics]] ([[string theory]]).


## Properties

### Characteristic series
 {#CharacteristicSeries}

The [characteristic series](genus#LogarithmAndCharacteristicSeries) of the Witten genus as a [[power series]] in $z$ with [[coefficients]] in formal power series in $q$ over $\mathbb{Q}$ is

$$
  \begin{aligned}
    K_w(z)(q)
    & = 
    \frac{z}{\exp_w(z)(q)}
    \\
    & = 
    \frac{z}{\sigma_L(z)(q)}
    \\
    & =
    \frac{z/2}{sinh(z/2)}
    \prod_{n \geq 1}
    \frac{(1-q^n)^2}{(1-q^n e^z)(1-q^n e^{-z})}
      \\
      & = 
      \exp\left(
        \sum_{k \geq 2} G_k(q) \frac{z^k}{k!}
      \right)
   \end{aligned}
  \,,
$$

where 

* $\sigma_L$ is the [[Weierstrass sigma-function]] (see e.g. [Ando Basterra 00, section 5.1](#AndoBasterra00));

* $G_k$ are the [[Eisenstein series]] ([Zagier 86, equation (14)](#Zagier86), [Ando-Hopkins-Rezk 10, prop. 10.9](#AndoHopkinsRezk10)).

This is a [[modular form]] with respect to the variable $q$, see also the the discussion below at _[Integrality and modularity](#IntegralityAndModularity)_ . Such functions which are power series of two variables $z$ and $q$ with elliptic nature in $z$ and modular nature in $q$ are called _[[Jacobi forms]]_ ([Zagier 86, p. 8](#Zagier86), [Ando-French-Ganter 08](#AndoFrenchGanter08)).

There are various further ways to equivalently re-express the above in terms of other special [[modular forms]]. Here are some:

#### In terms of Kac-Weyl characters
 {#CharacteristicSeriesInTermsOfKacWeylCharacters}

The Witten genus has a close relation to the [[Kac-Weyl character]] of [[loop group representations]].

Consider of four [[irreducible representations|irreducible]] [[level]]-1  positive energy [[Spin group|Spin]]$(2k)$-[[loop group representation]] the one denoted

$$
  \tilde S_+ - \tilde S_- \in Rep(\tilde L Spin(2k))
$$

and write its [[Kac-Weyl character]] as

$$
  \chi(\tilde S_+ - \tilde S_-) \in Rep(Spin(2k))[ [ q^{1/12} ] ]
  \,.
$$

Under passing to [[group characters]] this is ([Brylinski 90, p. 7(467)](#Brylinski90), reviewed in [KL 96, section 1.2](#KL96)) equivalently 

$$
  \chi(\tilde S_+ - \tilde S_-) = \frac{\prod_{1}^k \theta}{\eta^k}
 \,,
$$

where on the right we have the [[Jacobi theta-function]] $\theta$ divided by the [[Dedekind eta-function]] $\eta$. 

Comparison shows that in terms of this the exponential series of the Witten genus is equivalently (by the [[splitting principle]] the $k$-fold products are left implicit):

$$
  \exp_w = z/K_w = \eta^2 \, \chi(\tilde S_+ - \tilde S_-)
  \,.
$$

Notice that, by the relation (see [here](equivariant+elliptic+cohomology#RelationToLoopGroupRepresentations)) between [[equivariant elliptic cohomology]] and [[loop group representations]], over the complex numbers $\chi(\tilde S_+ - \tilde S_-)$ may be regarded as an element of the $Spin(2k)$-[[equivariant elliptic cohomology]] of the point (at the [[Tate curve]], see at [[twisted ad-equivariant Tate K-theory]]).

### Integrality and modularity
 {#IntegralityAndModularity}

A priori, the Witten genus has [[coefficients]] the [[power series]] ring $\mathbb{Q}[ [q] ]$ over the [[rational numbers]]. But under suitable conditions ([[quantum anomaly cancellation]]) it takes values in more interesting subrings.


#### For the type II superstring
 {#ModularityForTypeIISuperstring}

The genus obtained from the [[type II superstring]] in the NS-R sector is a [[modular form]] for the [[congruence subgroup]] $\Gamma_2(2)$. ([Witten 87a, below (13)](Witten87a)) See at _[congruence subgroup -- Relation to spin structures](level+structure+on+an+elliptic+curve#RelationToSpinStructures)_ for more. 

Hence, with suitable normalization, the universal Witten-Ochanine genus takes values in the subring $MF_\bullet^{\mathbb{Q}}(\Gamma_0(2)) \hookrightarrow \mathbb{Q}[ [q] ]$ of [[modular forms]] for $\Gamma_0(2)\subset SL_2(\mathbb{Z})$ with rational coefficients ([Zagier 86, item d) on page 2](#Zagier86) based on [Chudnovsky-Chudnovsky 88](#ChudnovskyChudnovsky88)).

#### For the heterotic superstring
 {#ModularityForHeteroticString}


On manifolds with [[spin structure]] the heterotic string Witten genus has integral coeffcients, hence in the ring $\mathbb{Z}[ [ q ] ]$ ([Chudnovsky-Chudnovsky 88](#ChudnovskyChudnovsky88), [Landweber 88](#Landweber88)), see also ([Kreck-Stolz 93](#KreckStolz93), [Hovey 91](#Hovey91)). 

On manifolds with rational [[string structure]] (meaning spin structure and the [[first fractional Pontryagin class]] is at most [[torsion subgroup|torsion]]), then the Witten genus takes values in actual [[modular forms]] $MF_\bullet$ ([Zagier 86, page 6](#Zagier86)).



On manifolds with actual [[string structure]], finally, the Witten genus factors through [[topological modular forms]] ([Hopkins 94](#Hopkins94), [Ando-Hopkins-Rezk 10](#AndoHopkinsRezk)).

### Relation to Dirac operators and supersymmetric QM on loop space
 {#RelationToSuSyQMOnLoopSpace}

Originally in ([Witten 87a](#Witten87a)) the elliptic genus was derived as the [[large volume limit]] of the [[index]] of the [[supercharge]] of the [[superstring]] [[worldsheet]] [[2d SCFT]]. Here the "large volume limit" is what restricts the oscillations of the string to be "small". But then in ([Witten87b](#Witten87b)) it was observed that if this supercharge -- the [[Dirac-Ramond operator]] -- would really behave like a [[Dirac operator on smooth loop space]], then the elliptic genus would be the $S^1$-equivariant [[index of a Dirac operator]], where $S^1$ acts by rigid rotationl of the parameterization of the loops, and by analogy standard formulas for equivariant indices in K-theory would imply the localization to the tangent spaces to the space of constant loops. 

Notice that the would-be [[Dirac operator on smooth loop space]] is what would realize the [[superstring]] quantum dynamics as [[supersymmetric quantum mechanics]] on [[smooth loop space]]. This observation was the original motivation for the study of [[supersymmetric quantum mechanics]] in ([Witten 82](#Witten82), [Witten 85](#Witten85)) in the presence of a given [[Killing vector field]] (correspinding to the $S^1$-action on loop space ).

### Heterotic (twisted) Witten genus, loop group representations and parameterized WZW models
 {#TwistedWittenGenus}

If the [[superstring]] in question is the [[heterotic string]] then generally there is a "[[twisted differential string-structure|twist]]" of its [[background fields]] by a [[gauge field]], hence by a $G$-[[principal bundle]] for $G$ some simply connected [[compact Lie group]] (notably [[E8]]). The partition function in this case is a "twisted Witten genus" ([Witten 87, equations (30), (31)](#Witten87), [Brylinski 90](#Brylinski90), [KL 95](#KL95)). The modularity condition then is no longer just that the [[tangent bundle]] has [[string structure]], but that together with the gauge bundle it has [[twisted string structure]], hence [[string^c 2-group|String^c]]-structure for $c$ the $G$-[[second Chern class]] (explicitly identified as such in ([Chen-Han-Zhang 10](#ChenHanZhang10)).


An elegant formulation of twisted Witten genera (and proof of their rigidity) in terms of highest weight [[loop group representations]] is given in ([KL 95](#KL95)) along the lines of ([Brylinski 90](#Brylinski90)). In ([Distler-Sharpe 07](#DistlerSharpe07)), following suggestions around ([Ando 07](#Ando07)) this is interpreted geometrically in terms of fiberwise [[index|indices]] of [[parameterized WZW models]] [[associated bundle|associated]] to the given [[string 2-group|String]]-[[principal 2-bundle]].

What should be a concrete computation of the twisted Witten genus specifically for $G =$ [[E8]] is in ([Harris 12, section 4](#Harris12)).

### As the global character of sheaves of vertex operator algebras

For $U \subset \mathbb{C}$ an [[open subset]] of the [[complex plane]] then the space $\mathcal{D}^{ch}(U)$ of [[chiral differential operators]] on $U$ is naturally a [[super vertex operator algebra]]. For $X$ a [[complex manifold]] such that its [[first Chern class]] and [[second Chern class]] vanish over the [[rational numbers]], then this assignment gives a [[sheaf of vertex operator algebras]] $\mathcal{D}^{ch}_X(-)$ on $X$. Its [[cochain cohomology]] $H^\bullet(\mathcal{D}^{ch}_X)$ is itself a [[super vertex operator algebra]] and its super-[[Kac-Weyl character]] is proportional to the [[Witten genus]] $w(X)$ of $X$:

$$
  char H^\bullet(\mathcal{D}^{ch}_X)\propto w(X)
  \,.
$$

Physically this result is understood by observing that $\mathcal{D}^{ch}_X$is the sheaf of [[quantum observables]] of the [[topological twist|topologically twisted]] [[2d (2,0)-superconformal QFT]] (see there for more on this) of which the [[Witten genus]] is (the [[large volume limit]] of) the [[partition function]].

As highlighted in ([Cheung 10, p. 2](#Cheung10)), there is a [[resolution]]  by the [[chiral Dolbeault complex]] which gives a precise sense in which over a [[complex manifold]] the Witten genus is a stringy analog of the [[Todd genus]]. See ([Cheung 10](#Cheung10)) for a brief review, where furthermore the problem of generalizing of this construction to [[sheaves of vertex operator algebras]] over more general [[string structure]] manifolds is addressed.





### Stolz conjecture

The _[[Stolz conjecture]]_ due to ([Stolz 96](#Stolz96)) asserts that if $X$ is a [[closed manifold]] with [[String structure]] which furthermore admits a [[Riemannian metric]] with [[positive number|positive]] [[Ricci curvature]], then its Witten genus vanishes.


### Relation to BPS state counting on target space
 {#RelationToBPSStateCounting}

By [[supersymmetry]] and by the same argument that controls the expression of the [[index of a Dirac operator]] in terms of [[supersymmetric quantum mechanics]], the Witten genus may be thought of as counting those string states on which the left moving [[supercharge]] acts trivially. In terms of the [[target space]] theory these are the [[BPS states]]. (reviews include [Dijkgraaf 98](#Dijkgraaf98)).

Therefore the Witten genus may also be used as a generating function for BPS state counting. As such it has for instance been used in the microscopic explanation of [[Bekenstein-Hawking entropy]] of [[black holes]], see at _[[black holes in string theory]]_.

### Relation to Cayley plane bundles

The rational Witten genus vanishes on total spaces of [[Cayley plane]]-[[fiber bundles]], and is indeed characterized by this property ([McTague 10](#McTague10), [McTague 11](#McTague11)).


## Related concepts

* [[Witten index]]

* [[Tate K-theory]]

* [[elliptic Chern character]]

* [[M5-brane elliptic genus]]

[[!include genera and partition functions - table]]

## References
 {#References}

### General
 {#ReferencesGeneralCase}

The original description of the Witten genus from [[string theory]] is due to

* {#Witten87a} [[Edward Witten]],  _Elliptic Genera And Quantum Field Theory_ , Commun.Math.Phys. 109 525 (1987) ([Euclid](http://projecteuclid.org/euclid.cmp/1104117076))

* {#Witten87b} [[Edward Witten]], _The Index Of The Dirac Operator In Loop Space_ Proc. of Conf. on Elliptic Curves and Modular Forms in Algebraic Topology Princeton (1986) ([spire:245523](http://inspirehep.net/record/245523), [doi:10.1007/BFb0078045]( https://doi.org/10.1007/BFb0078045))

based on insights in

* {#Landweber88} [[Peter Landweber]], _Elliptic Cohomology and Modular Forms_, in _Elliptic Curves and Modular Forms in Algebraic Topology_, Lecture Notes in Mathematics Volume 1326, 1988, pp 55-68 ([[LandweberEllipticModular.pdf:file]])

* {#LandweberRavenelStong93} [[Peter Landweber]], [[Douglas Ravenel]], [[Robert Stong]], _Periodic cohomology theories defined by elliptic curves_, in [[Haynes Miller]] et al (eds.), _The Cech centennial: A conference on homotopy theory_, June 1993, AMS (1995) ([pdf](http://www.math.sciences.univ-nantes.fr/~hossein/GdT-Elliptique/Landweber-Ravenel-Stong.pdf))


(That the [[partition function]] in ([Witten 87 (11)](#Witten87)) is indeed, after some normalization, an [[elliptic genus]] is ([Landweber 88, theorem 3](#Landweber88))).


Rigorous proofs of the [[rigidity theorem for equivariant elliptic genera]] then appeared in

* [[Clifford Taubes]],  _$S^1$ actions and elliptic genera_, Comm. Math. Phys., 122(3):455&#8211;526, 1989.

* [[Raoul Bott]], [[Clifford Taubes]], _On the rigidity theorems of Witten_, J. of the Amer. Math. Soc., 2, 1989.


That a [[spin structure]] makes the Witten genus take values in integral series is due to

* {#ChudnovskyChudnovsky88} D.V. Chudnovsky, G.V. Chudnovsky, _Elliptic modular functions and elliptic genera_, Topology, Volume 27, Issue 2, 1988, Pages 163&#8211;170

* {#KreckStolz93} [[Matthias Kreck]], [[Stefan Stolz]], _$\mathbb{H}P^2$-bundles and elliptic homology_, Acta Mathematica 171 (1993), 231&#8211;261.

* {#Hovey91} [[Mark Hovey]], _Spin Bordism and Elliptic Homology_ (1991) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.53.3277))


That it takes a rational [[string structure]] to make the elliptic genus land in [[modular forms]] was noticed in 

* {#Zagier86} [[Don Zagier]], _Note on the Landweber-Stong elliptic genus_ 1986 ([pdf](http://people.mpim-bonn.mpg.de/zagier/files/doi/10.1007/BFb0078047/fulltext.pdf))

Surveys include

* [[Gerald Höhn]], _Complex elliptic genera and $S^1$-equivariant cobordism theory_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0405/0405232v1.pdf))

* {#Cheng13} Miranda Cheng, section 9 of _Mathematical tools for string theorists_, lecture notes 2013 ([pdf](http://www.math.jussieu.fr/~chengm/lecture_notes/Thalys_School.pdf))

Further discussion of the [[Jacobi form]]-property of the Witten genus is in

* {#AndoFrenchGanter08} [[Matthew Ando]], Christopher French, [[Nora Ganter]], _The Jacobi orientation and the two-variable elliptic genus_, Algebraic and Geometric Topology 8 (2008) p. 493-539 ([pdf](http://www.msp.warwick.ac.uk/agt/2008/08-01/agt-2008-08-016s.pdf))

Further discussion of the relation to [[quantum anomalies]] and the [[Green-Schwarz mechanism]] ([[string structure]], [[string^c structure]]) is in 

* [[Wolfgang Lerche]], B. Nilsson, A. Schellekens, N. Warner, _Anomaly cancelling terms from the elliptic genus_ (1987) ([pdf](http://lerche.web.cern.ch/lerche/papers/ellgenus1.pdf))

* [[Qingtao Chen]], [[Fei Han]], Weiping Zhang, _Generalized Witten Genus and Vanishing Theorems_, JDG, 88 (2011) 1-39 ([arXiv:1003.2325](http://arxiv.org/abs/1003.2325))

Discussion of the Witten genus via a KO-valued Chern-character on elliptic cohomology is in 

* [[Haynes Miller]], _The elliptic character and the Witten genus_, Contemporary mathematics, volume 96, 1989 ([pdf](http://dedekind.mit.edu/~hrm/papers/ell-char.pdf))

Relation to [[Cayley plane]]-[[fiber bundles]] is discussed in

* {#McTague10} [[Carl McTague]], _The Cayley Plane and the Witten Genus_ ([arXiv:1006.0728](http://arxiv.org/abs/1006.0728))

* {#McTague11} [[Carl McTague]], _The Cayley plane and String bordism_ ([arXiv:1111.4520](http://arxiv.org/abs/1111.4520))

On manifolds with [[SU(2)]]-[[action]]:

* [[Anand Dessai]], _The Witten genus and $S^3$-actions on manifolds_, 1994 ([pdf](https://homeweb.unifr.ch/dessaia/pub/papers/MZpreprint6_Witten_S3.pdf), [[DessaiWittenGenusS3.pdf:file]])



### Relation to Kac-Weyl characters of loop group representations
 {#ReferencesRelationToKacWeylCharacters}

The close relation of the Witten genus to [[Kac-Weyl characters]] of [[loop group representations]] has been highlighted and an elegant proof of rigidity of the Witten genus in these terms in

* [[Kefeng Liu]], _On elliptic genera and Theta functions_, Topology, Volume 35, Issue 3, July 1996, Pages 617&#8211;640 ([pdf](http://www.math.ucla.edu/~liu/Research/rigss1.pdf))

* {#KL95} [[Kefeng Liu]], _On modular invariance and rigidity theorems_, J. Differential Geom. Volume 41, Number 2 (1995), 247-514 ([eculid:1214456221](http://projecteuclid.org/euclid.jdg/1214456221), [pdf](http://www.math.ucla.edu/~liu/Research/loja.pdf))

along the lines of 

* {#Brylinski90} [[Jean-Luc Brylinski]], _Representations of loop groups, Dirac operators on loop space, and modular forms_, Topology, 29(4):461&#8211;480, 1990 (<a href="https://doi.org/10.1016/0040-9383(90)90016-D">doi:10.1016/0040-9383(90)90016-D</a>)

and further generalized to more general [[vertex operator algebra]] representations in ([DLM 02](#DLM02)).

Review and survey of some of this is in 

* {#KL96} [[Kefeng Liu]], _Modular forms and topology_, Proc. of the AMS Conference on the Monster and Related Topics, Contemporary Math. (1996) ([citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.130.9779))

### The Stolz conjecture

The [[Stolz conjecture]] on the Witten genus is due to

* {#Stolz96} [[Stephan Stolz]], _A conjecture concerning positive Ricci curvature and the Witten genus_, Mathematische Annalen Volume 304, Number 1 (1996),

Reviews include

* [[Anand Dessai]], _Some geometric properties of the Witten genus_ ([pdf](http://homeweb2.unifr.ch/dessaia/pub/papers/Arolla/DessaiArollaFinalRevised30June09.pdf))


### Refinement to the string-orientation of $tmf$

The refinement of the Witten genus from values in [[modular forms]] to [[topological modular forms]] and further to a morphism of [[E-∞ rings]], hence to the [[string orientation of tmf]] is due to 

* {#Hopkins94} [[Michael Hopkins]], _Topological modular forms, the Witten Genus, and the theorem of the cube_, Proceedings of the International Congress of Mathematics, Z&#252;rich 1994 ([pdf](http://www.mathunion.org/ICM/ICM1994.1/Main/icm1994.1.0554.0565.ocr.pdf))

* [[Michael Hopkins]], _Algebraic topology and modular forms_, Proceedings of the ICM, Beijing 2002, vol. 1, 283--309 ([arXiv:math/0212397](http://arxiv.org/abs/math/0212397))

* [[Matthew Ando]], [[Michael Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))
  {#AndoHopkinsRezk}

see also remark 1.4 of

* [[Paul Goerss]], _Topological modular forms (after Hopkins, Miller and Lurie)_ ([pdf](http://arxiv.org/PS_cache/arxiv/pdf/0910/0910.5130v1.pdf)).


and for more on the [[sigma-orientation]] see


* [[Matthew Ando]], _The sigma orientation for analytic circle-equivariant elliptic cohomology_, Geom. Topol. 7 (2003) 91-153 ([arXiv:math/0201092](http://arxiv.org/abs/math/0201092))

* {#AndoBasterra00} [[Matthew Ando]], Maria Basterra, _The Witten genus and equivariant elliptic cohomology_ ([arXiv:0008192](http://arxiv.org/abs/math/0008192))

### Via index theory of would-be Dirac operators on loop space

Further literature emphasising the perspective of  [[Dirac-Ramond operators]] as would-be [[Dirac operators on smooth loop space]] includes

* {#AlvarezKillingbackManganoWindey87} [[Orlando Alvarez]], T. P. Killingback, Michelangelo Mangano, [[Paul Windey]], _The Dirac-Ramond operator in string theory and loop space index theorems_, Nuclear Phys. B Proc. Suppl., 1A:189&#8211;215, 1987. Nonperturbative methods in field theory (Irvine, CA, 1987).

* [[Orlando Alvarez]], T. P. Killingback, Michelangelo Mangano,[[Paul Windey]], _String theory and loop space index theorems_, Comm. Math. Phys., 111(1):1&#8211;10, 1987.

* {#Brylinski90} [[Jean-Luc Brylinski]], _Representations of loop groups, Dirac operators on loop space, and modular forms_, Topology, 29(4):461&#8211;480, 1990.

* {#Landweber99} [[Gregory Landweber]], _Dirac operators on loop space_ PhD thesis (Harvard 1999) ([pdf](http://math.bard.edu/greg/LoopDirac.pdf))

* [[Orlando Alvarez]], [[Paul Windey]], _Analytic index for a family of Dirac-Ramond operators_, Proc. Natl. Acad. Sci. USA, 107(11):4845&#8211;4850, 2010

The observation thazt the realization of the [[Dirac-Ramond operator]] as a [[Dirac operator on smooth loop space]] would realize superstring quantum dynamics as [[supersymmetric quantum mechanics]] on [[smooth loop space]] is what inspired the observations in

* {#Witten82} [[Edward Witten]], _Supersymmetry and Morse theory_  J. Differential Geom. Volume 17, Number 4 (1982), 661-692. ([Euclid](http://projecteuclid.org/euclid.jdg/1214437492), [pdf](http://www.cimat.mx/~gil/docencia/2012/teoria_de_morse/witten_supersymmetry_and_morse_theory.pdf), [spire](http://inspirehep.net/record/176416?ln=de))

and 


* {#Witten85} [[Edward Witten]], _Global anomalies in string theory_, in W. Bardeen and A. White (eds.) _Symposium on Anomalies_, Geometry, Topology, pp. 61&#8211;99. World Scientific, 1985 


### Via (sheaves of) super vertex operator algebras

Formalization via [[super vertex operator algebras]] is discussed
in 

* Hirotaka Tamanoi, _Elliptic Genera and Vertex Operator Super-Algebras_, 1999

* {#DLM02} Chongying Dong, [[Kefeng Liu]], Xiaonan Ma, _Elliptic genus and vertex operator algebras_ ([arXiv:math/0201135](http://arxiv.org/abs/math/0201135))

and for  the [[topological twist|topologically twisted]] [[2d (2,0)-superconformal QFT]] (the [[heterotic string]] with enhanced supersymmetry) via [[sheaves of vertex operator algebras]] in

* {#Cheung10} Pokman Cheung, _The Witten genus and vertex algebras_ ([arXiv:0811.1418](http://arxiv.org/abs/0811.1418))

which is based on the detailed construction via [[chiral differential operators]] in 

* [[Vassily Gorbounov]], [[Fyodor Malikov]], [[Vadim Schechtman]], _Gerbes of chiral differential operators_, Math. Res. Lett. 7(1), 55&#8211;66 (2000) ([arXiv:math/9906117](http://arxiv.org/abs/math/9906117), [arXiv:math/0003170](http://arxiv.org/abs/math/0003170), [arXiv:math/0005201](http://arxiv.org/abs/math/0005201))



### Via other methods

In terms of [[(2,1)-dimensional Euclidean field theories and tmf]]:

* {#StolzTeichner} [[Stephan Stolz]], [[Peter Teichner]], _Supersymmetric field theories and generalized cohomology_ in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_, Proceeding of Symposia in Pure Mathematics, volume 83, AMS (2011) ([arXiv:1108.0189](http://arxiv.org/abs/1108.0189))
  

...and in terms of [[factorization algebras]] in 

* [[Kevin Costello]], _A geometric construction of the Witten genus, II_ ([arXiv:1112.0816](http://arxiv.org/abs/1112.0816))
 {#Costello}

### Twisted case
 {#ReferencesTwistedCase}

The twisted Witten genus in the present of [[background gauge field]] hence for a [[twisted string structure]]/[[string^c structure]] is discussed in terms of [[twisted string structures]] in

* {#ChenHanZhang10} [[Qingtao Chen]], [[Fei Han]], [[Weiping Zhang]], _Generalized Witten Genus and Vanishing Theorems_, Journal of Differential Geometry 88.1 (2011): 1-39. ([arXiv:1003.2325](http://arxiv.org/abs/1003.2325))

* Jianqing Yu, Bo Liu, _On the Witten Rigidity Theorem for $String^c$ Manifolds_, Pacific Journal of Mathematics 266.2 (2013): 477-508. ([arXiv:1206.5955](http://arxiv.org/abs/1206.5955))

based on formulas from 

* [[Qingtao Chen]], [[Fei Han]], _Elliptic Genera, Transgression and Loop Space Chern-Simons Forms_, Communications in Analysis and Geometry Volume 17 (2009) Number 1 ([arXiv:math/0611104](http://arxiv.org/abs/math/0611104), [doi:10.4310/CAG.2009.v17.n1.a4]( https://dx.doi.org/10.4310/CAG.2009.v17.n1.a4))

For the moment see the references at _[[string^c structure]]_ for more on this.

See also:

* [[Fei Han]], [[Varghese Mathai]], _Projective elliptic genera and elliptic pseudodifferential genera_, Adv. Math. 358 (2019) 106860  ([arXiv:1903.07035](https://arxiv.org/abs/1903.07035))


A geometric interpretation of this in terms of [[parameterized WZW models]] is suggested in

* {#DistlerSharpe07} [[Jacques Distler]], [[Eric Sharpe]], section 8.5 _Heterotic compactifications with principal bundles for general groups and general levels_, Adv. Theor. Math. Phys. 14:335-398, 2010 ([arXiv:hep-th/0701244](http://arxiv.org/abs/hep-th/0701244))
  

and with more emphasis on [[equivariant elliptic cohomology]] in 

* {#Ando07} [[Matthew Ando]], _Equivariant elliptic cohomology and the Fibered WZW models of Distler and Sharpe_, [talk 2007](http://www.math.ucsb.edu/~drm/GTPseminar/2007-fall.php) ([lecture notes pdf](http://www.math.ucsb.edu/~drm/GTPseminar/notes/20071026-ando/20071026-malmendier.pdf))

An explicit computation for an [[E8]]-gauge bundle is in section 4 of 

* {#Harris12} [[Chris Harris]], _The Index Bundle for a Family of Dirac-Ramond Operators_ ([arXiv:1202.2049](http://arxiv.org/abs/1202.2049))

### Relation to BPS state counting on target space

A survey of elliptic string genera with more context within [[string theory]] and in particular with discussion of the relation to [[BPS state]] counting is

* {#Dijkgraaf98} [[Robbert Dijkgraaf]], _Fields, strings, matrices and symmetric products_, lecture notes 1998 ([pdf](http://www.cgtp.duke.edu/ITP99/dijkgraaf/sym.pdf))










[[!redirects Witten genera]]

[[!redirects twisted Witten genus]]
[[!redirects twisted Witten genera]]