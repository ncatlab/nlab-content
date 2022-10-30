+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _super Lie algebra_ is the analog of a [[Lie algebra]] in [[superalgebra]]/[[supergeometry]]. 

See also [[supersymmetry]].

## Definition

+-- {: .num_defn}
###### Definition

A **super Lie algebra** over a [[field]] $k$ is a [[Lie algebra]] [[internalization|internal]] to the [[symmetric monoidal category|symmetric monoidal]] $k$-linear [[category]] [[SVect]] of [[super vector space]]s.

=--

+-- {: .num_note}
###### Note

This means that a super Lie algebra is 

1. a [[super vector space]] $\mathfrak{g} = \mathfrak{g}_{even} \oplus \mathfrak{g}_{odd}$;

1. equipped with a bilinear bracket
 
   $$
     [-,-] : \mathfrak{g}\otimes \mathfrak{g} \to \mathfrak{g}
   $$

   that is _graded_ skew-symmetric: it is skew symmetric on $\mathfrak{g}_{even}$ and _symmetric_ on $\mathfrak{g}_{odd}$.

1. that satisfies the $\mathbb{Z}_2$-graded [[Jacobi identity]] in that for any three element $x,y,z \in \mathbb{g}$ of homogeneous degree $deg(x),deg(y),deg(z))\in \mathbb{Z}$ then

   $$
     [x, [y, z]] = [[x,y],z] + (-1)^{deg(x)\cdot deg(y)} [y, [x,z]]
     \,.
   $$

=--

+-- {: .num_note}
###### Note

Equivalently, a super Lie algebra is a "super-representable" Lie algebra internal to the [[cohesive (∞,1)-topos]] [[Super∞Grpd]] over the site of [[super points]]. 

See the discussion at [[superalgebra]] for details on this.

=--

## Examples

* The [[super Poincare Lie algebra]] and various of its polyvector extension are super-extension of the ordinary [[Poincare Lie algebra]]. These are the [[supersymmetry algebra]]s in the strict original sense of the word. 

* [[super q-Schur algebra]]

* higher super Lie algebras

  Just as [[Lie algebra]]s are [[vertical categorification|categorified]] to [[L-infinity algebra]]s and [[L-infinity algebroid]]s, so super Lie algebras categorifie to [[super L-infinity algebra]]s.  A secretly famous example is the

  * [[supergravity Lie 3-algebra]], [[supergravity Lie 6-algebra]]

## References

One of the original references (or the original reference?) is

* [[Victor Kac]], _Lie superalgebras_, Advances in Math. 26 (1977), no. 1, 8--96.

Discussion of classification is in 

* {#Nahm78} [[Werner Nahm]], _[[Supersymmetries and their Representations]]_, Nucl.Phys. B135 (1978) 149 ([spire](https://inspirehep.net/record/120988/), [pdf](http://cds.cern.ch/record/132743/files/197709213.pdf))

* {#Shnider88} [[Steven Shnider]], _The superconformal algebra in higher dimensions_, Letters in Mathematical Physics November 1988, Volume 16, Issue 4, pp 377-383

* [[Victor Kac]], _Classification of supersymmetries_, Proceedings of the ICM, Beijing 2002, vol. 1, 319--344 ([arXiv:math-ph/0302016](http://arxiv.org/abs/math-ph/0302016))

Introductions and surveys include

* Groeger, _Super Lie groups and super Lie algebras_, lecture notes 2011 ([pdf](http://www.mathematik.hu-berlin.de/~groegerj/teaching_files/lecture12.pdf))

* L. Frappat, A. Sciarrino, P. Sorba, _Dictionary on Lie Superalgebras_ ([arXiv:hep-th/9607161](http://arxiv.org/abs/hep-th/9607161))

* D. Leites, _Lie superalgebras_, J. Soviet Math. 30 (1985), 2481--2512 ([web](http://dx.doi.org/10.1007/BF02249121))

* M. Scheunert, _The theory of Lie superalgebras. An introduction_, Lect. Notes Math. 716 (1979) 

* D. Westra, _Superrings and supergroups_ ([pdf](http://www.mat.univie.ac.at/~michor/westra_diss.pdf))

Discussion of  [[Lie algebra extensions]] for super Lie algebras includes

* [[Dmitri Alekseevsky]], [[Peter Michor]], Wolfgang Ruppert, _Extensions of super Lie algebras_, J. Lie Theory 15 (2005) No. 1, 125--134 ([arXiv:math/0101190](http://arxiv.org/abs/math/0101190))


[[!redirects Lie superalgebra]]
[[!redirects super Lie algebras]]
