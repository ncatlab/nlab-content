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
* table of contents goes here
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

   that is _graded_ skew-symmetric: is is skew symmetric on $\mathfrak{g}_{even}$ and _symmetric_ on $\mathfrak{g}_{odd}$.

1. that satisfied the $\mathbb{Z}_2$-graded Jacobi identity:

   $$
     [x, [y, z]] = [[x,y],z] + (-1)^{deg x deg y} [y, [x,z]]
     \,.
   $$

=--

+-- {: .num_note}
###### Note

Equivalently, a super Lie algebra is a "super-representable" Lie algebra internal to the [[cohesive (∞,1)-topos]] [[Super∞Grpd]] over the site of [[super point]]s. 

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

* [[Victor Kac]], _Lie superalgebras_. Advances in Math. 26 (1977), no. 1, 8--96.

Surveys:

* Groeger, _Super Lie groups and super Lie algebras_, lecture notes 2011 ([pdf](http://www.mathematik.hu-berlin.de/~groegerj/teaching_files/lecture12.pdf))

A useful survey with more pointers to the literature is

* L. Frappat, A. Sciarrino, P. Sorba, _Dictionary on Lie Superalgebras_ ([arXiv:hep-th/9607161](http://arxiv.org/abs/hep-th/9607161))

Another useful survey is

* D. Leites, _Lie superalgebras_, J. Soviet Math. 30 (1985), 2481--2512 ([web](http://dx.doi.org/10.1007/BF02249121))

* M. Scheunert, _The theory of Lie superalgebras. An introduction_, Lect. Notes Math. 716 (1979) 



[[!redirects Lie superalgebra]]
[[!redirects super Lie algebras]]

