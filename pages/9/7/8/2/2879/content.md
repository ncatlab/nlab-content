
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _Hopf algebroid_ is a (possibly [[noncommutative geometry|noncommutative]]) generalization of a structure which is dual to a [[groupoid]] (equipped with [[atlas]]) in the sense of [[Isbell duality|space-algebra duality]]. This is the concept that generalizes [[Hopf algebras]] with their relation to [[groups]] from groups to groupoids.

Just as for [[groups]] and their [[Hopf algebras]], there are _two_ ways to assign a Hopf algebroid to a [[groupoid]] $\mathcal{G}_\bullet$:

1. **commutative but non-co-commutative** Form the [[commutative algebra|commutative]] [[algebras of functions]] $C(\mathcal{G}_1)$ and $C(\mathcal{G}_0)$ and regard the operation induced by the partially defined [[composition]] in $\mathcal{G}_\bullet$ as an in general non-co-commutative [[coalgebra]] structure on $C(\mathcal{G}_1)$ over $C(\mathcal{G_0})$;

1. **non-commutative but co-commutative** Form the in general non-commutative [[groupoid convolution algebra]] $C_{conv}(\mathcal{G})$ and regard it as a co-commutative [[coalgebra]] over $C(\mathcal{G}_0)$.

Both of these resulting bialgebra structures can then be further generalized to allow them to be both non-commutative as well as non-co-commutative. 

(...)

 
## Definition


(...)

### Commutative Hopf algebroids

Given an internal [[groupoid]] in the category $Aff_k$ of affine algebraic $k$-[[schemes]], where $k$ is a field, the $k$-algebras of [[global sections]] over the scheme of objects and the scheme of morphisms have an additional structure of a commutative Hopf algebroid. In fact this is an [[dual equivalence|antiequivalence of categories]]. Commutative Hopf algebroids are useful also in a version in [[brave new algebra]] (the work of John Rognes). 

### Noncommutative Hopf algebroids 

There are several generalizations to the noncommutative case. A difficult part is to work over the noncommutative base (i.e., the object of objects is noncommutative). The definition of a [[bialgebroid]] is not that difficult and there is even a very old definition due Takeuchi. To add an antipode is nontrivial. A definition of Lu from mid 1990s is rather nonselfdual unlike the case of [[Hopf algebras]]. So a better solution is to abandon the idea of an antipode and have some replacement for it. There are two approaches, one via [[monoidal bicategory|monoidal bicategories]] due to Day and Street, and another due Gabi B&#246;hm, using pairs of a left and right bialgebroid. Gabi has later shown that the two definitions are in fact equivalent.

## References

The commutative version is classical, and there is an extensive literature. Some of the recent works on commutative case, related to homotopy theory and stacks are

* [[Mark Hovey]], _Homotopy theory of comodules over a Hopf algebroid_, [pdf](http://math.wesleyan.edu/~mhovey/papers/comodule.pdf); _Morita theory of Hopf algebroids_, [pdf](http://math.wesleyan.edu/~mhovey/talks/hopfalgebroids.pdf)

* [[Paul Goerss]], _Quasi-coherent sheaves on the moduli stack of formal groups_, [pdf](http://www.math.northwestern.edu/~pgoerss/papers/modfg.pdf)

* Barry Walker, _Hopf algebroids and stacks_  ([pdf](http://www.math.umn.edu/~tlawson/old/stackstalk.pdf))

For the relation to [[groupoid convolution algebras]] see also at _[groupoid convolution algebra -- References -- Convolution Hopf algebroids](category%20algebra#ReferencesConvolutionHopfAlgebroids)_.

* [[Mark Hovey]], _Morita theory for Hopf algebroids and presheaves of groupoids_ ([arXiv:math/0105137](http://arxiv.org/abs/math/0105137))

The version in [[brave new algebra]]

* A. Baker, A. Jeanneret, _Brave new Hopf algebroids and extensions of $M U$-algebras_, Homology Homotopy Appl. __4__:1 (2002), 163-173, [MR1937961](http://www.ams.org/mathscinet-getitem?mr=1937961), [euclid](http://projecteuclid.org/euclid.hha/1139840059)

One can straightforwardly keep the base commutative while having the total algebra noncommutative, and the image of source and target maps are required to commute mutually. This version is due Maltsiniotis; he also generalized this to [[quasi-Hopf algebra|quasi-Hopf]] version:

* [[Georges Maltsiniotis]], _Groupo&#239;des quantiques_, Comptes R
Rendus Acad. Sci. Paris __314__, pp. 249-252 (1992) [ps](http://people.math.jussieu.fr/~maltsin/ps/GRN-1.PS)
* G. Maltsiniotis, _Quasi-groupo&#239;des quantiques_ (travail en commun avec A. Brugui&#232;res), C.R. Acad. Sci. Paris __319__, pp. 933-936 (1994) [ps](http://people.math.jussieu.fr/~maltsin/ps/N-QSBIG.PS) 

Over a noncommutative base ring, there is a nonsymmetric version due J-H. Lu and a similar version is later studied by [[Ping Xu]]

*  Jiang-Hua Lu, _Hopf algebroids and quantum groupoids_, Int. J. Math. __7__, 1 (1996) pp. 47-70, [q-alg/9505024](http://arxiv.org/abs/q-alg/9505024), [MR95e:16037](http://www.ams.org/mathscinet-getitem?mr=95e:16037), [doi](http://dx.doi.org/10.1142/S0129167X96000050); _On the Drinfeld double and the Heisenberg double of a Hopf algebra_, Duke Math. J. __7__:3 (1994) 763-776, [MR1277953](http://www.ams.org/mathscinet-getitem?mr=1277953), [doi](http://dx.doi.org/10.1215/S0012-7094-94-07428-0)
* [[Ping Xu]], _Quantum groupoids_, Commun. Math. Phys., 216:539581, 2001, [q-alg/9905192](http://arxiv.org/abs/math/9905192), [doi](http://dx.doi.org/10.1007/s002200000334); _Quantum groupoids and deformation quantization_, [q-alg/9708020](http://arxiv.org/abs/q-alg/9708020), _Quantum groupoids associated to universal dynamical R-matrice_, [q-alg/9811172](http://arxiv.org/abs/math/9811172)
* blog discussion at [Theoretical Atlas](http://theoreticalatlas.wordpress.com/2009/03/18/a-note-on-quantum-groupoids)

The modern concept over the noncommutative base is discovered in two formally different formalisms, but the two concepts are equivalent: 
 
* [[B. Day]], [[R. Street]], _Monoidal bicategories and Hopf algebroids_, Advances in Mathematics __129__, 1 (1997) 99--157 

* [[G. Böhm]], _An alternative notion of Hopf algebroid_; in "Hopf algebras in noncommutative geometry and physics",  31--53, Lecture Notes in Pure and Appl. Math. __239__, Dekker, New York, 2005; <a href="http://arxiv.org/abs/math.QA/0301169"> math.QA/0301169 </a>
* [[G. Böhm]], _Hopf algebroids_, (a chapter of) Handbook of algebra, [arxiv:math.RA/0805.3806](http://arxiv.org/abs/0805.3806)
* G. B&#246;hm, [[K. Szlachányi]], _Hopf algebroids with bijective antipodes: axioms, integrals and duals_, Comm. Algebra __32__ (11) (2004) 4433 - 4464 [math.QA/0305136](http://arxiv.org/abs/math.QA/0305136)
* [[T. Brzeziński]], G. Militaru, _Bialgebroids, $\times_A$-bialgebras and duality_,  J. Algebra __251__: 279-294, 2002
[math.QA/0012164](http://arxiv.org/abs/math.QA/0012164)
[[!redirects Hopf algebroids]]