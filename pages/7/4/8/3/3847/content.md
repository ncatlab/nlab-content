
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

### In terms of 2-Segal spaces

Given a [[2-Segal space]] $X_\bullet$ such that the [[spans]]

$$
  X_1 \times X_1 \stackrel{(\partial_2, \partial_0)}{\leftarrow} X_2 \stackrel{\partial_1}{\rightarrow} X_1
$$

and

$$  
  pt \leftarrow X_0 \stackrel{s_0}{\to} X_1
$$

admit pull-push [[integral transforms]] in some given [[cohomology theory]] $h$. Then the **Hall algebra** of $X$ with [[coefficients]] in $H$ is the [[associative algebra]] structure on $h(X_1)$ induced by these pull-push operations. 

This is the perspective of [Dyckerhoff-Kapranov 12, def. 8.1.8](#DyckerhoffKapranov12).

### Motivic Hall algebra
 {#MotivicHallAlgebra}

Specifically for a given [[algebraic stack]] $X$ and with 

$$
  X \leftarrow X^{(2)} \rightarrow X\times X
$$ 

denoting the moduli stack of 2-flags of coherent sheaves on $X$, then the corresponding pull-push multiplication on the motivic Grothendieck ring $K(X)$ is called the _motivic Hall algebra_ of $X$ (due to [[Dominic Joyce]] reviewed e.g. in [Bridgeland 10, 4.2](#Bridgeland10)). Discussion of motivic Hall algebras of [[Calabi-Yau 3-folds]] is in ([Kontsevich-Soibelman 08](#KontsevichSoibelman08)).

### In terms of constructible sheaves

The _Hall algebra_ of an [[abelian category]] is the [[Grothendieck group]] of [[constructible sheaves]]/[[perverse sheaves]] on the [[moduli stack]] of [[object]]s in the category. The Hall algebra is an algebra because the constructible derived category of the moduli stack of objects in an [[abelian category]] is [[monoidal category|monoidal]] in a canonical way.

This perspective is taken from ([Webster11](#Webster)). See there for more details.


## References

Survey:

* [[Claus M. Ringel]], *The Hall multiplication]*, lecture notes  (2006) &lbrack;[web](https://www.math.uni-bielefeld.de/~ringel/lectures/green/Welcome.html)&rbrack; 

* {#Webster} [[Ben Webster]], _Hall algebras are Grothendieck groups_ (2011) &lbrack;[webpage](http://sbseminar.wordpress.com/2011/04/18/hall-algebras-are-grothendieck-groups/#more-3988)&rbrack;
 
* [[Olivier Schiffmann]], *Lectures on Hall algebras* &lbrack;[arXiv:math/0611617](https://arXiv.org/abs/math/0611617)&rbrack;

* [[Matthew B. Young]], *Self-Dual Hall modules*, PhD thesis, Stony Brook (2013) &lbrack;[pdf](https://www.math.stonybrook.edu/alumni/2013-Matthew-Young.pdf), [[Young-HallModules.pdf:file]]&rbrack;

* Wikipedia: [Hall algebra](https://en.wikipedia.org/wiki/Hall_algebra), [Ringel-Hall algebra](https://en.wikipedia.org/wiki/Ringel&#8211;Hall_algebra)


The characterization via [[2-Segal spaces]]/decomposition spaces is independently due to

* [[Tobias Dyckerhoff]], [[Mikhail Kapranov]], _Higher Segal spaces I_, ([arxiv:1212.3563](http://arxiv.org/abs/1212.3563))
 {#DyckerhoffKapranov12} (now part of their book _Higher Segal spaces_, Springer Lec. Notes in Math. 2244  [doi](https://doi.org/10.1007/978-3-030-27124-4))
* [[Imma Gálvez-Carrillo]], [[Joachim Kock]], [[Andrew Tonks]], _Decomposition spaces, incidence algebras and Möbius inversion_, [arXiv:1404.3202](https://arxiv.org/abs/1404.3202)

Anew light on the interplay between 2-Segal and Hall product:

* [[Matthew B. Young]], _Relative 2-Segal spaces_, 
Algebraic & Geometric Topology **18&& (2018) 975--1039 &lbrack;[doi:10.2140/agt.2018.18.975](https://doi.org/)&rbrack;

  > We introduce a relative version of the 2–Segal simplicial spaces defined by Dyckerhoff and Kapranov, and Gálvez-Carrillo, Kock and Tonks. Examples of relative 2–Segal spaces include the categorified unoriented cyclic nerve, real pseudoholomorphic polygons in almost complex manifolds and the $\mathcal{R}_\bullet$-construction from Grothendieck–Witt theory. We show that a relative 2–Segal space defines a categorical representation of the Hall algebra associated to the base 2–Segal space. In this way, after decategorification we recover a number of known constructions of Hall algebra representations. We also describe some higher categorical interpretations of relative 2–Segal spaces.

Further references:

* [[Mikhail Kapranov]], _Eisenstein series and quantum affine algebras_, Journal Math. Sciences __84__ (1997), 1311&#8211;1360.

* [[Mikhail Kapranov]], [[Eric Vasserot]], _Kleinian singularities, derived categories and Hall algebras_,  Math. Ann.  __316__  (2000) 565-576, [arXiv/9812016](https://arxiv.org/abs/math/9812016)

* [[Bernhard Keller]], Dong Yang, Guodong Zhou, _The Hall algebra of a spherical object_, J. London Math Soc. (2) __80__ (2009) 771--784, [doi](https://doi.org/10.1112/jlms/jdp054), [pdf](www.math.jussieu.fr/~keller/publ/HallAlgSphericalObject.pdf)

* [[Claus M. Ringel]], _Hall algebras and quantum groups_, Invent. Math. __101__ (1990), no. 3, 583--591

Green has introduced a coproduct on Hall algebras of a quiver which are related to quantum groups; Green's theorem states that the Hall algebra of the category of representations of a quiver over a finite field is a twisted bialgebra. The coproduct than agrees with the one on quantum groups:

* J. A. Green, _Hall algebras, hereditary algebras and quantum groups_, Invent. Math. __120__ (2), 361--377
(1995)
* J.  Xiao, F. Xu, M. Zhao, _Ringel-Hall algebras beyond their quantum groups I: Restriction functor and Green formula. Algebras & Represent. Theory __22__ (2019) , 1299--1329 [doi](https://doi.org/10.1007/s10468-018-9821-5)
* J. Xiao, _Drinfeld double and Ringel-Green theory of Hall algebras_, J Algebra __190__ (1997) 100--144 [Zbl0874.16026](https://zbmath.org/0874.16026)
* Matthew B. Young, _Degenerate versions of Green's theorem for Hall modules_, J. Pure & Applied Algebra
__225__:4 (2021) 106557 [doi](https://doi.org/10.1016/j.jpaa.2020.106557)

Elliptic Hall algebras

* [[Olivier Schiffmann]], [[Eric Vasserot]], _The elliptic Hall algebra_, Cherednik Hecke algebras and Macdonald polynomials, Compositio Mathematica __147__:1 (2011) 188-234 [doi](https://doi.org/10.1112/S0010437X10004872) [arXiv:0802.4001](https://arxiv.org/abs/0802.4001), (2008); _The elliptic Hall algebra and the equivariant K-theory of the Hilbert scheme of $\mathbf{A}^2$_,  Duke Math. J. 162(2): 279-366 (2013) [doi](https://doi.org/10.1215/00127094-1961849) [arXiv:0905.2555](http://arXiv.org/abs/0905.2555)
* O. Schiffman, _Drinfeld realization of the elliptic Hall algebra_, J. Algebr. Comb. 35 (2012) 237--262  [doi](https://doi.org/10.1007/s10801-011-0302-8) [arxiv/1004.2575](https://arxiv.org/abs/1004.2575) 
* O. Schiffmann, [[Eric Vasserot]], _Hall algebras of curves, commuting varieties and Langlands duality_, Math. Ann. 353 (2012) 1399-1451 [doi](https://doi.org/10.1007/s00208-011-0720-x) [arXiv:1009.0678](https://arxiv.org/abs/1009.0678)

Toen's derived Hall algebras

* [[Bertrand Toen]], _Derived Hall algebras_,  Duke Math. J. 135(3): 587-615 (2006) [doi](https://doi.org/10.1215/S0012-7094-06-13536-6) [arXiv:0501343](https://arxiv.org/abs/math/0501343)

* [[Alexander I. Efimov]], _Cohomological Hall algebra of a symmetric quiver_, Compositio Mathematica __148__:4 (2012) 1133-1146 [doi](https://doi.org/10.1112/S0010437X12000152) [arxiv/1103.2736](https://arxiv.org/abs/1103.2736) 

* Description of seminar on stability conditions, Hall algebras and [[Stokes phenomenon|Stokes factors]] in Bonn 2009 ([[Daniel Huybrechts|D. Huybrechts]]), [pdf](http://www.math.uni-bonn.de/people/compgeo/Hall.pdf)

* sbseminar blog: [Hall algebras and Donaldson-Thomas invariants-i](http://sbseminar.wordpress.com/2009/03/25/hall-algebras-and-donaldson-thomas-invariants-i)

* Bangming Deng, Jie Du, [[Brian Parshall]], Jianpan Wang, _Finite dimensional algebras and quantum groups_, Mathematical Surveys and Monographs __150__, Amer. Math. Soc. 2008. xxvi+759 pp. (chap. 10: Ringel-Hall algebras) [MR2009i:17023)](https://mathscinet.ams.org/mathscinet-getitem?mr=2457938)

* [[David Hernandez]], [[Bernard Leclerc]], _Quantum Grothendieck rings and derived Hall algebras_, J. Reine Angew. Math. 701 (2015) 77--126 [doi](https://doi.org/10.1515/crelle-2013-0020) [arXiv/1109.0862](https://arxiv.org/abs/1109.0862)

* Parker E. Lowrey, _The moduli stack and motivic Hall algebra for the bounded derived category_, [arxiv/1110.5117](http://arxiv.org/abs/1110.5117)

* [[Tobias Dyckerhoff]], _Higher categorical aspects of Hall Algebras_, In: Herbera D., Pitsch W., Zarzuela S. (eds) Building Bridges Between Algebra and Topology. Advanced Courses in Mathematics - CRM Barcelona. Birkhäuser 2015 [arXiv:1505.06940](https://arxiv.org/abs/1505.06940) [doi](https://doi.org/10.1007/978-3-319-70157-8_1)

* [[Mauro Porta]], Francesco Salla, _Two-dimensional categorified Hall algebras_, J. Eur. Math. Soc. __25__:3 (2023) 1113-1205 [doi](https://doi.org/10.4171/jems/1303)
* J. Xiao, F. Xu, _Hall algebras associated to triangulated categories_, Duke Math. J. 143 (2) (2008) 357--373

A realization of (Drinfeld-Jimbo) [[quantum group]]s via a "Bridgeland" version of Hall algebra,

* [[Tom Bridgeland]], _Quantum groups via Hall algebras of complexes_, Ann of Math __177__ (2) (2013) 739--759



Motivic Hall algebras:

* {#Bridgeland10} [[Tom Bridgeland]], _An introduction to motivic Hall algebra_ ([arXiv:1002.4372](https://arxiv.org/abs/1002.4372))

* {#KontsevichSoibelman08} [[Maxim Kontsevich]], [[Yan Soibelman]], _Stability structures, motivic Donaldson-Thomas invariants and cluster transformations_ ([arXiv:0811.2435](https://arxiv.org/abs/0811.2435))

* [[Kontsevich|M. Kontsevich]], [[Yan Soibelman|Y. Soibelman]], _Motivic Donaldson-Thomas invariants: summary of results_, [arXiv/0910.4315](https://arxiv.org/abs/0910.4315)

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Cohomological Hall algebra, exponential Hodge structures and motivic Donaldson-Thomas invariants_, [arXiv/1006.2706](https://arxiv.org/abs/1006.2706)

* Richard Rimányi, _Motivic characteristic classes in cohomological Hall algebras_, Advances in Mathematics __360__ (2020) 106888 [doi](https://doi.org/10.1016/j.aim.2019.106888) [arXiv:1808.05654](https://arxiv.org/pdf/1808.05654)

* Alexei Latyntsev, _Vertex algebras, moduli stacks,
cohomological Hall algebras and quantum groups_, PhD thesis, Oxford 2022 [pdf](https://people.maths.ox.ac.uk/joyce/theses/LatyntsevDPhil.pdf)

[[!redirects Hall algebras]]

[[!redirects motivic Hall algebra]]
[[!redirects motivic Hall algebras]]
