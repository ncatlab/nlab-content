## Determinants and bundles

Multivectors $e_1\wedge\ldots\wedge e_n$ transform according to the rule involving determinants. In particular, the exterior product is good to express the $n$-volume of the parallelepiped spanned by $n$-vectors. 

Given a linear map $T:V\to W$ of $n$-dimensional vector spaces, there is a induced map of the top exterior powers $det T: \Lambda^n V\to \Lambda^n W$, which is therefore identified an element in the line $\Lambda(V)^*\otimes\Lambda^n(W)$.

Given a functor (bifunctor...) $F$ from the category of vector spaces to vector spaces, with certain continuity assumption on $F$, induces a functor from the category of vector bundles over an arbitrary manifold to vector bundles. In particular, we have exterior powers, (Whitney) sums, dual bundles and so on. Notice that if $f_{ij}$ are transition functions for the original bundle $E$ with values in $GL(n)$ then the determinants $det(f_{ij})$ are the transition functions for the bundle $\Lambda^n(E)$. One can now look at operators $T:E\to F$ where $E,F$ are vector bundles of rank $n$ and the induced operators $\Lambda^n T : \Lambda^n E\to \Lambda^n F$ which can be considered as elements $det T\in (\Lambda^n E)^*\otimes\Lambda^n F$. 

Given a [[manifold]] $X$, the top exterior power $\Lambda^{dim X} T^* X$ is a line bundle called the __determinant bundle__ on $X$. Even more important is the case of when $X$ is replaced by an appropriate moduli space of [[connection]]s, instantons, holomorphic structures or some other objects related to Fredholm operators for which the determinants can be defined. 

## Quillen's determinant line bundle

There is a specific version called **Quillen's determinant line bundle** which is certain line bundle over the moduli space of complex structures on a fixed smooth vector bundle $E$ over a fixed Riemann surface $M$. A complex structure on the bundle corresponds to an operator which in local coordinates looks as $D = d\bar{z}(\partial_z+\alpha(z))$ where $\alpha(z)$ is a smooth matrix valued function. The set of such operators is an affine space $\mathcal{A}$ whose underlying vector space is the space of $(0,1)$-End-valued forms $\Omega^{0,1} (End M)$. Then again a determinant is an element of a line $\mathcal{L}_D = \lambda(Ker D)^*\otimes \lambda(Coker D)$ where $\lambda$ is taking the top exterior power. Now one has a family $\mathcal{L}_D$ depending on $D$ what determines a holomorphic line bundle over $\mathcal{A}$. This is the **determinant line bundle**. 

## Trivialization of determinant line bundle

If we had a trivialization of the Quillen's determinant line bundle, then we could identify every section with a holomorphic function on the base space, hence a holomorphic rule giving a number to a Cauchy-Riemann operator. For this one restricts first to the component consisting of the operators with the zero Fredholm index. Next, one considers the corresponding [[Laplace operator]] $D^* D$ and its determinant related to the [[zeta function]]. (This is related to the [[analytic torsion]]).

## Applications

These determinant line bundles are important in the study of [[quantum anomaly|quantum anomalies]], in the formulation of cohomological quantum field theories, study of some invariants of differential operators like $\eta$-invariant and so on. 

## References

* [[Daniel Quillen|D.G. Quillen]], _Determinants of Cauchy-Riemann operators over a Riemann surface_, Funkcionalnii Analiz i ego Prilozhenija __19__ (1985), 37-41, ([pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=faa&paperid=1334&volume=19&year=1985&issue=1&fpage=37&what=fullt&option_lang=eng) of Russian version).

* M. F. Atiyah, I. M. Singer, _Dirac operators coupled to vector potentials_, Proc. Nat. Acad. Sci. USA __81__, 2597-2600 (1984) ([pdf](http://www.pnas.org/content/81/8/2597.full.pdf) at pnas site)

* [[Dan Freed]], _On determinant line bundles_, Math. aspects of [[string theory]], ed. S. T. Yau, World Sci. Publ. 1987,  (revised [pdf](http://www.math.utexas.edu/~dafr/Index/determinants.pdf), [dg-ga/9505002](http://arxiv.org/abs/dg-ga/9505002))

* J.-M. Bismut, D.S. Freed, _The analysis of elliptic families.I. Metrics and connections on determinant bundles_, Comm. Math. Phys. __106__, 1 (1986), 159-176, [euclid](http://projecteuclid.org/euclid.cmp/1104115586), _II. Dirac operators, eta invariants, and the holonomy theorem_, Comm. Math. Phys. __107__, 1 (1986), 103-163. [euclid](http://projecteuclid.org/euclid.cmp/1104115934)

* J-M. Bismut, _Quillen metrics and determinant bundles_, 2 conference lectures in honour of A. N. Tyurin, video at [link](http://www.mathnet.ru/php/presentation.phtml?presentid=62&option_lang=eng)

* Kenro Furutani, _On the Quillen determinant_, J. Geom. Phys. __49__, 4, 366-375, [math.DG/0309127](http://arxiv.org/abs/math/0309127), [doi](http://dx.doi.org/10.1016/j.geomphys.2003.07.001)

* [[M. Kontsevich]], S. Vishik, _Geometry of determinants of elliptic operators_, in Functional Analysis on the Eve of the 21st Century. 
Vol. I (S. Gindikin, et al., eds.) In honor of the 80th birthday of [[Israel Gel'fand|I.M. Gelfand]]. Birkh&#228;user, Progr. Math. __131__ (1993), 173-197, [pdf](http://193.51.104.7/~maxim/TEXTS/geometry_determinants_12.pdf), [hep-th/9406140](http://arxiv.org/abs/hep-th/9406140)