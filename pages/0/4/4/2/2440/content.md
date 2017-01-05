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


## Properties

### Classification
 {#Classification}

([Kac 77a](Kac77a), [Kac 77b](#Kac77b)) states a classification of super Lie algebras which are

1. finite dimensional

1. simple

1. over a [[field]] of [[characteristic zero]].

Such an algebra is called of _classical type_ if the [[action]] of its even-degree part on the odd-degree part is completely reducible. Those simple finite dimensional algebras not of classical type are of _Cartan type_.

1. classical type

   1. four infinite series
 
      1. $A(m,n)$

      1. $B(m,n) = $ [[osp]]$(2m+1,2n)$ $m\geq 0$, $n \gt 0$

      1. $C(n)$

      1. $D(m,n) = $[[osp]]$(2m,2n)$ $m \geq 2$, $n \gt 0$

   1. two exceptional ones

      1. $F(4)$

      1. $G(3)$

   1. a family $D(2,1;\alpha)$ of deformations of $D(2,1)$

   1. two "strange" series

      1. $P(n)$

      1. $Q(n)$

1. Cartan type

   (...)


The underlying even-graded [[Lie algebra]] for type 2 is as follows

| $\mathfrak{g}$ |  $\mathfrak{g}_{even}$  |  $\mathfrak{g}_{even}$ rep on $\mathfrak{g}_{odd}$ |
|----------------|-------------------------|------------------|
| $B(m,n)$  | $B_m \oplus C_n$  | vector $\otimes$ vector |
| $D(m,n)$  | $D_m \oplus C_n$  | vector $\otimes$ vector |
| $D(2,1,\alpha)$ |  $A_1 \oplus A_1 \oplus A_1$ | vector $\otimes$ vector $\otimes$ vector |
| $F(4)$ | $B_3\otimes A_1$ | spinor $\otimes$ vector |
| $G(3)$ | $G_2\oplus A_1$ | spinor $\otimes$ vector |
| $Q(n)$ | $A_n$ | adjoint |


For type 1 the $\mathbb{Z}/2\mathbb{Z}$-grading lifts to an $\mathbb{Z}$-grading with $\mathfrak{g} = \mathfrak{g}_{-1}\oplus \mathfrak{g}_0 \oplus \mathfrak{g}_1$. 

| $\mathfrak{g}$ |  $\mathfrak{g}_{even}$  |  $\mathfrak{g}_{even}$ rep on $\mathfrak{g}_{{-1}}$ |
|----------------|-------------------------|------------------|
| $A(m,n)$ |  $A_m \oplus A_n \oplus C$ | vector $\otimes$ vector $\otimes$ $\mathbb{C}$ |
| $A(m,m)$ | $A_m \oplus A_n$ | vector $\otimes$ vector |
| $C(n)$ | $\mathbb{C}_{-1} \oplus \mathbb{C}$ | vector $\otimes$ $\mathbb{C}$ |

reviewed e.g. in ([Farmer 84, p. 25,26](#Farmer84), [Minwalla 98, section 4.1](#Minwalla98)).

## Examples

* The [[super Poincare Lie algebra]] and various of its polyvector extension are super-extension of the ordinary [[Poincare Lie algebra]]. These are the [[supersymmetry algebra]]s in the strict original sense of the word. 

* [[super q-Schur algebra]]

* higher super Lie algebras

  Just as [[Lie algebra]]s are [[vertical categorification|categorified]] to [[L-infinity algebra]]s and [[L-infinity algebroid]]s, so super Lie algebras categorifie to [[super L-infinity algebra]]s.  A secretly famous example is the

  * [[supergravity Lie 3-algebra]], [[supergravity Lie 6-algebra]]

## Related entries

* [[Haag??opusza?ski?Sohnius theorem]]

* [[geometry of physics -- supersymmetry]]

## References

According to [Kac77b](#Kac77b) the definition of super Lie algebra is originally due to

* [[Felix Berezin]], G. I. Kac, Math. Sbornik 82, 343&#8212;351 (1970) (Russian)

The original references on the classification of super Lie algebras are

* {#Kac77a} [[Victor Kac]], _Lie superalgebras_, Advances in Math. 26 (1977), no. 1, 8--96.

* {#Kac77b} [[Victor Kac]], _A sketch of Lie superalgebra theory_, Comm. Math. Phys.
Volume 53, Number 1 (1977), 31-64. ([EUCLID](https://projecteuclid.org/euclid.cmp/1103900590))

See also

* [[Werner Nahm]], V. Rittenberg, [[Manfred Scheunert]], _The classification of graded Lie algebras_ , Physics Letters B Volume 61, Issue 4, 12 April 1976, Pages 383&#8211;384 ([publisher](http://www.sciencedirect.com/science/article/pii/0370269376905943))

* M. Parker, _Classification Of Real Simple Lie Superalgebras Of Classical Type_, J.Math.Phys. 21 (1980) 689-697 ([spire](http://inspirehep.net/record/157627?ln=en))

Further discussion of classification related specifically to [classification of supersymmetry](#supersymmetry#Classification) is due to

* {#Nahm78} [[Werner Nahm]], _[[Supersymmetries and their Representations]]_, Nucl.Phys. B135 (1978) 149 ([spire](https://inspirehep.net/record/120988/), [pdf](http://cds.cern.ch/record/132743/files/197709213.pdf))

* {#Shnider88} [[Steven Shnider]], _The superconformal algebra in higher dimensions_, Letters in Mathematical Physics November 1988, Volume 16, Issue 4, pp 377-383

* [[Victor Kac]], _Classification of supersymmetries_, Proceedings of the ICM, Beijing 2002, vol. 1, 319--344 ([arXiv:math-ph/0302016](http://arxiv.org/abs/math-ph/0302016))

Introductions and surveys include

* {#Farmer84} Richard Joseph Farmer, _Orthosymplectic superalgebras in mathematics and science_, PhD Thesis (1984) ([web](http://eprints.utas.edu.au/19542/), [pdf](http://eprints.utas.edu.au/19542/1/whole_FarmerRichardJoseph1985_thesis.pdf))

* L. Frappat, A. Sciarrino, P. Sorba, _Dictionary on Lie Superalgebras_ ([arXiv:hep-th/9607161](http://arxiv.org/abs/hep-th/9607161))

* Groeger, _Super Lie groups and super Lie algebras_, lecture notes 2011 ([pdf](http://www.mathematik.hu-berlin.de/~groegerj/teaching_files/lecture12.pdf))

* L. Frappat, A. Sciarrino, P. Sorba, _Dictionary on Lie Superalgebras_ ([arXiv:hep-th/9607161](http://arxiv.org/abs/hep-th/9607161))

* D. Leites, _Lie superalgebras_, J. Soviet Math. 30 (1985), 2481--2512 ([web](http://dx.doi.org/10.1007/BF02249121))

* [[Manfred Scheunert]], _The theory of Lie superalgebras. An introduction_, Lect. Notes Math. 716 (1979) 

* D. Westra, _Superrings and supergroups_ ([pdf](http://www.mat.univie.ac.at/~michor/westra_diss.pdf))

* {#Minwalla98} [[Shiraz Minwalla]], _Restrictions imposed by superconformal invariance on quan tum field theories_ Adv. Theor. Math. Phys. 2, 781 (1998)
([arXiv:hep-th/9712074](http://arxiv.org/abs/hep-th/9712074)).

Discussion of  [[Lie algebra extensions]] for super Lie algebras includes

* [[Dmitri Alekseevsky]], [[Peter Michor]], Wolfgang Ruppert, _Extensions of super Lie algebras_, J. Lie Theory 15 (2005) No. 1, 125--134 ([arXiv:math/0101190](http://arxiv.org/abs/math/0101190))


[[!redirects Lie superalgebra]]
[[!redirects super Lie algebras]]