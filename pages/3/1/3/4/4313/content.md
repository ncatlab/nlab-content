
# Matrix factorizations
* table of contents
{: toc}

There are two different meanings of phrase "matrix factorization" which are closely related

* (typically canonical) [[matrix decomposition]]s of matrices into products of matrices of specific kind, like [[Gauss decomposition]], [[polar decomposition]], LU-decomposition etc. 

* decomposition of a ring element, understood as a diagonal matrix, as a product of matrices over a ring, in the sense of Eisenbud and followers. 

This entry is dedicated to the latter as it concerns appearance of certain categories in mathematical physics. 

## Overview

Matrix factorizations were introduced by [[David Eisenbud]], and they were originally studied in the context of [[commutative algebra]].

Matrix factorizations arise in [[string theory]] as categories of [[D-branes]] for [[Landau-Ginzburg model|Landau-Ginzburg]] [[B-model]]s. This was proposed by Kontsevich and elaborated in the paper of Kapustin-Li.

Matrix factorizations have also been used by Khovanov-Rozansky in knot theory [math/0401268](http://arxiv.org/abs/math/0401268).

__Matrix factorization categories__ are examples of [[Calabi-Yau categories]], hence correspond to [[TCFT]]s by the Costello/Kontsevich/Hopkins-Lurie theorem. The Calabi-Yau structure is elucidated in recent work of Dyckerhoff-Murfet and Polishchuk-Vaintrob.

Dyckerhoff has proved that the [[Hochschild homology]] of the matrix factorizations category of an isolated singularity is the [[Jacobian ring]] of the singularity. See also the work of E. Segal and Caldararu-Tu. In light of the Costello/Kontsevich/Hopkins-Lurie theorem, this result has been anticipated for some time, as the closed state space of a Landau-Ginzburg B-model is the Jacobian ring.

There is also the Calabi-Yau/Landau-Ginzburg correspondence. In some cases, categories of matrix factorizations turn out to be equivalent to categories of coherent sheaves.

For general theory and properties of matrix factorizations, see work of Orlov. For example, matrix factorization categories are related to derived categories of singularities.

## Definition

(Eisenbud 1980) A __matrix factorization__ of an element $x$ in a commutative ring $A$ is an ordered pair of maps of free $A$-modules $(\phi:F\to G,\psi: G\to F)$ such that $\phi\circ\psi = x\cdot 1_G$ and $\psi\circ\phi = x\cdot 1_F$.

Note that if $(\phi,\psi)$ is a matrix factorization of $x$, then $x$ annihilates $Coker\phi$.

## Related concepts

* [[Landau-Ginzburg model]]

## Literature

* [[David Eisenbud]], _Homological algebra on a complete intersection, with an application to group representations_, Trans. Amer. Math. Soc. __260__:3564 (1980) [doi](https://doi.org/10.1090/S0002-9947-1980-0570778-7)

* [[Tobias Dyckerhoff]], _Compact generators in the categories of matrix factorizations_,  Duke Math. J. 159(2): 223-274 (2011) [doi](https://doi.org/10.1215/00127094-1415869) [arXiv:0904.4713](https://arxiv.org/abs/0904.4713)

The definition of a [[triangulated category]] of B-branes for the [[Landau-Ginzburg model]] via [[matrix factorization]] was proposed by [[Maxim Kontsevich]] and is written out in

* [[Anton Kapustin]], Yi Li, _D-Branes in Landau-Ginzburg Models and Algebraic Geometry_ ([arXiv:hep-th/0210296](http://arxiv.org/abs/hep-th/0210296))

* {#Orlov} [[Dmitri Orlov]], _Triangulated categories of singularities and D-branes in Landau-Ginzburg models_, Proc. Steklov Inst. Math. 2004, no. 3 (246), 227--248 ([arXiv:math/0302304](http://arxiv.org/abs/math/0302304))

* [[Dmitri Orlov]], _Derived categories of coherent sheaves and triangulated categories of singularities_, Algebra, arithmetic, and geometry: in honor of Yu. I. Manin. Vol. II, 503--531, Progr. Math. __270__, Birkh&#228;user 2009 arXiv:[math.AG/0503632](https://arxiv.org/abs/math.ag/0503632)

See also

* Junwu Tu, _Matrix factorizations via Koszul duality_, Compositio Mathematica __150__:9 (2014) 1549--1578
[doi](https://doi.org/10.1112/S0010437X14007295) [arXiv:1009.4151](https://arxiv.org/abs/1009.4151)

* J. Burke, M. E. Walker, _Matrix factorizations over projective schemes_, Homology, Homotopy and Applications __14__(2) (2012) 37--61 [arXiv:1110.2918](https://arxiv.org/abs/1110.2918)

* Matthew Ballard, David Favero, [[Ludmil Katzarkov]], _A category of kernels for graded matrix factorizations and its implications for Hodge theory_, Publ.math.IHES 120, 1–111 (2014) [doi](https://doi.org/10.1007/s10240-013-0059-9) [arXiv:1105.3177](https://arxiv.org/abs/1105.3177)

* [[Alexander I. Efimov]], _Cyclic homology of categories of matrix factorizations_,  Intern. Math. Res. Notices __12__ (2018) 3834--3869 [doi](https://doi.org/10.1093/imrn/rnw332) [arXiv:1212.2859](https://arxiv.org/abs/1212.2859)

* A. Polishchuk, [[Arkady Vaintrob]], _Matrix factorizations and cohomological field theories_, J. Reine Angew. Math. 714 (2016) 1--122

* [[Alexander Polishchuk]], _Homogeneity of cohomology classes associated with Koszul matrix factorizations_, Compositio Math. __152__ (2016) 2071--2112
[doi](https://doi.org/10.1112/S0010437X16007557) [arXiv:1409.7115](https://arxiv.org/abs/1409.7115)

* A. Efimov, L. Positselski, _Coherent analogues of matrix factorizations and relative singularity categories_, Algebra & Number Theory __9__ (2015) 1159--1292 [doi](https://doi.org/10.2140/ant.2015.9.1159)

On a connection to the representation theory of loop groups and families of Dirac operators (and the [[string 2-group]]) 

* {#FreedTeleman14} [[Daniel S. Freed]], [[Constantin Teleman]], _Dirac families for loop groups as matrix factorizations_, Comptes Rendus Mathematique __353__:5 (2015) 415-419 [doi](https://doi.org/10.1016/j.crma.2015.02.011) [arXiv:1409.6051](https://arxiv.org/abs/1409.6051)


On a [[bicategory]] of [[Landau-Ginzburg models]] with [[matrix factorizations]] as [[1-morphisms]]:

* [[Nils Carqueville]], [[Daniel Murfet]], *Adjunctions and defects in Landau-Ginzburg models*, Adv. Math. **289** (2016) 480-566 ([doi:10.1016/j.aim.2015.03.033](https://doi.org/10.1016/j.aim.2015.03.033), [arXiv:1208.1481](https://arxiv.org/abs/1208.1481))

On a category of [[matrix factorizations]] in the context of [[Landau-Ginzburg models]], described in terms of [[linear logic]] and the [[geometry of interactions]]:

* [[Daniel Murfet]], _The cut operation on matrix factorisations_, J. Pure Appl. Alg. **222** 7 (2018) 1911-1955 ([arXiv:1402.4541](https://arxiv.org/abs/1402.4541), [doi:10.1016/j.jpaa.2017.08.014](https://doi.org/10.1016/j.jpaa.2017.08.014))


[[!redirects matrix factorization]]
[[!redirects matrix factorizations]]
[[!redirects matrix factorisation]]
[[!redirects matrix factorisations]]

[[!redirects matrix factorization category]]
[[!redirects matrix factorisation category]]
