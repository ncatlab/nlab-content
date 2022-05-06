
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

A good survey is given in

* [[Ben Webster]], _Hall algebras are Grothendieck groups_ ([SBS](http://sbseminar.wordpress.com/2011/04/18/hall-algebras-are-grothendieck-groups/#more-3988))
 {#Webster}

The characterization via [[2-Segal spaces]] is due to

* Tobias Dyckerhoff, [[Mikhail Kapranov]], _Higher Segal spaces I_, ([arxiv:1212.3563](http://arxiv.org/abs/1212.3563))
 {#DyckerhoffKapranov12}


Canonical references on Hall algebras include the following.

* [[Kapranov|M. Kapranov]], _Eisenstein series and quantum affine algebras_, Journal Math. Sciences __84__ (1997), 1311&#8211;1360.
* M. Kapranov, E. Vasserot, _Kleinian singularities, derived categories and Hall algebras_,  Math. Ann.  __316__  (2000), 565-576, [arxiv/9812016](http://arxiv.org/abs/math/9812016)
* [[Bernhard Keller]], Dong Yang, Guodong Zhou, _The Hall algebra of a spherical object_, J. London Math Soc. (2) __80__ (2009) 771&#8211;784, [doi](http://dx.doi.org/10.1112/jlms/jdp054), [pdf](www.math.jussieu.fr/~keller/publ/HallAlgSphericalObject.pdf)
* C. Ringel, _Hall algebras and quantum groups_, Invent. Math. __101__ (1990), no. 3, 583&#8211;591.
* O. Schiffmann, _Lectures on Hall algebras_, [arXiv:math/0611617](http://arXiv.org/abs/math/0611617)
* O. Schiffmann, E. Vasserot, _The elliptic Hall algebra_, Cherednik Hecke algebras and Macdonald polynomials, [arXiv:0802.4001](http://arxiv.org/abs/0802.4001), (2008), to appear in Compositio Math.; _The elliptic Hall algebra and the equivariant K-theory of the Hilbert scheme of A2, [arXiv:0905.2555](http://arXiv.org/abs/0905.2555)
* O. Schiffman, _Drinfeld realization of the elliptic Hall algebra_, [arxiv/1004.2575](http://arxiv.org/abs/1004.2575) 
* O. Schiffmann, E. Vasserot, _Hall algebras of curves, commuting varieties and Langlands duality_, [arxiv/1009.0678](http://arxiv.org/abs/1009.0678)
* [[Toen|B. Toen]], _Derived Hall algebras_, [arxiv/0501343](http://arxiv.org/abs/math/0501343)


* [[Alexander I. Efimov|Alexander Efimov]], _Cohomological Hall algebra of a symmetric quiver_, [arxiv/1103.2736](http://arxiv.org/abs/1103.2736) 

* Description of seminar on stability conditions, Hall algebras and [[Stokes phenomenon|Stokes factors]] in Bonn 2009 ([[Daniel Huybrechts|D. Huybrechts]]), [pdf](http://www.math.uni-bonn.de/people/compgeo/Hall.pdf)

* wikipedia: [Hall algebra](http://en.wikipedia.org/wiki/Hall_algebra), [Ringel-Hall algebra](http://en.wikipedia.org/wiki/Ringel&#8211;Hall_algebra)

* sbseminar blog: [Hall algebras and Donaldson-Thomas invariants-i](http://sbseminar.wordpress.com/2009/03/25/hall-algebras-and-donaldson-thomas-invariants-i)

* Bangming Deng, Jie Du, [[Brian Parshall]], Jianpan Wang, _Finite dimensional algebras and quantum groups_, Mathematical Surveys and Monographs __150__, Amer. Math. Soc. 2008. xxvi+759 pp. (chap. 10: Ringel-Hall algebras) [MR2009i:17023)](http://www.ams.org/mathscinet-getitem?mr=2457938)

* David Hernandez, Bernard Leclerc, _Quantum Grothendieck rings and derived Hall algebras_, [arxiv/1109.0862](http://arxiv.org/abs/1109.0862)

* Parker E. Lowrey, _The moduli stack and motivic Hall algebra for the bounded derived category_, [arxiv/1110.5117](http://arxiv.org/abs/1110.5117)

* [[Tobias Dyckerhoff]], _Higher categorical aspects of Hall Algebras_, In: Herbera D., Pitsch W., Zarzuela S. (eds) Building Bridges Between Algebra and Topology. Advanced Courses in Mathematics - CRM Barcelona. Birkhäuser 2015 [arXiv:1505.06940](https://arxiv.org/abs/1505.06940) [doi](https://doi.org/10.1007/978-3-319-70157-8_1)


Motivic Hall algebras:

* {#Bridgeland10} [[Tom Bridgeland]], _An introduction to motivic Hall algebra_ ([arXiv:1002.4372](http://arxiv.org/abs/1002.4372))

* {#KontsevichSoibelman08} [[Maxim Kontsevich]], [[Yan Soibelman]], _Stability structures, motivic Donaldson-Thomas invariants and cluster transformations_ ([arXiv:0811.2435](http://arxiv.org/abs/0811.2435))

* [[Kontsevich|M. Kontsevich]], [[Yan Soibelman|Y. Soibelman]], _Motivic Donaldson-Thomas invariants: summary of results_, [arxiv/0910.4315](http://arxiv.org/abs/0910.4315)


* [[Maxim Kontsevich]], [[Yan Soibelman]], _Cohomological Hall algebra, exponential Hodge structures and motivic Donaldson-Thomas invariants_, [arxiv/1006.2706](http://arxiv.org/abs/1006.2706)


[[!redirects Hall algebras]]

[[!redirects motivic Hall algebra]]
[[!redirects motivic Hall algebras]]
