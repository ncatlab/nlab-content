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

There are various equivalent ways to state the definition of super Lie algebras. Here are a few (for more discussion see at _[[geometry of physics -- superalgebra]]_):

### As Lie algebras internal to super vector spaces

+-- {: .num_defn #SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}
###### Definition

A _[[super Lie algebra]]_ is a [[Lie algebra]] [[internalization|internal]]
to the [[symmetric monoidal category]] $sVect = (Vect^{\mathbb{Z}/2}, \otimes_k, \tau^{super} )$ of [[super vector spaces]].
Hence this is

1. a [[super vector space]] $\mathfrak{g}$;

1. a homomorphism

   $$
     [-,-] \;\colon\; \mathfrak{g} \otimes_k \mathfrak{g} \longrightarrow \mathfrak{g}
   $$

   of super vector spaces (the _super Lie bracket_)

such that

1. the bracket is skew-symmetric in that the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       \mathfrak{g} \otimes_k \mathfrak{g}
         &
           \overset{\tau^{super}_{\mathfrak{g},\mathfrak{g}}}{\longrightarrow}
         &
       \mathfrak{g} \otimes_k \mathfrak{g}
       \\
       {}^{\mathllap{[-,-]}}\downarrow && \downarrow^{\mathrlap{[-,-]}}
       \\
       \mathfrak{g} &\underset{-1}{\longrightarrow}& \mathfrak{g}
     }
   $$

   (here $\tau^{super}$ is the [[braiding]] [[natural isomorphism]] in the category of [[super vector spaces]])

1. the [[Jacobi identity]] holds in that the following [[commuting diagram|diagram commutes]]

   $$
     \array{
       \mathfrak{g} \otimes_k \mathfrak{g} \otimes_k \mathfrak{g}
       &&
         \overset{\tau^{super}_{\mathfrak{g}, \mathfrak{g}} \otimes_k id }{\longrightarrow}
       &&
       \mathfrak{g} \otimes_k \mathfrak{g} \otimes_k \mathfrak{g}
       \\
       & {}_{\mathllap{[-,[-,-]]} - [[-,-],-] }\searrow && \swarrow_{\mathrlap{[-,[-,-]]}}
       \\
       && \mathfrak{g}
     }
     \,.
   $$

=--




### As super-graded Lie algebras


Externally this means the following:

+-- {: .num_prop #SuperLieAlgebraTraditional}
###### Proposition

A [[super Lie algebra]] according to def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces} is equivalently

1. a $\mathbb{Z}/2$-[[graded vector space]] $\mathfrak{g}_{even} \oplus \mathfrak{g}_{odd}$;

1. equipped with a [[bilinear map]] (the _super Lie bracket_)

   $$
     [-,-] : \mathfrak{g}\otimes_k \mathfrak{g} \to \mathfrak{g}
   $$

   which is _graded_ skew-symmetric: for $x,y \in \mathfrak{g}$ two elements of homogeneous degree $\sigma_x$, $\sigma_y$, respectively, then

   $$
     [x,y] = -(-1)^{\sigma_x \sigma_y} [y,x]
     \,,
   $$

1. that satisfies the $\mathbb{Z}/2$-graded [[Jacobi identity]] in that
for any three elements $x,y,z \in \mathfrak{g}$ of homogeneous super-degree $\sigma_x,\sigma_y,\sigma_z\in \mathbb{Z}_2$ then

   $$
     [x, [y, z]] = [[x,y],z] + (-1)^{\sigma_x \cdot \sigma_y} [y, [x,z]]
     \,.
   $$

A [[homomorphism]] of super Lie algebras is a homomorphisms of the underlying [[super vector spaces]]
which preserves the Lie bracket. We write

$$
  sLieAlg
$$

for the resulting [[category]] of super Lie algebras.

=--


### As formal duals of a Chevalley-Eilenberg super-algebras

+-- {: .num_defn #CEAlgebraofSuperLieAlgebra}
###### Definition

For $\mathfrak{g}$ a [[super Lie algebra]] of [[finite number|finite]] [[dimension]], then its _[[Chevalley-Eilenberg algebra]]_ $CE(\mathfrak{g})$ is the super-[[Grassmann algebra]] on the [[dual vector space|dual]] super vector space

$$
  \wedge^\bullet  \mathfrak{g}^\ast
$$

equipped with a [[differential]] $d_{\mathfrak{g}}$ that on generators is the linear dual of the super Lie bracket

$$
  d_{\mathfrak{g}} \;\coloneqq\; [-,-]^\ast \;\colon\; \mathfrak{g}^\ast \to \mathfrak{g}^\ast \wedge \mathfrak{g}^\ast
$$

and which is extended to $\wedge^\bullet \mathfrak{g}^\ast$ by the graded Leibniz rule (i.e. as a graded [[derivation]]).

$\,$

Here all elements are $(\mathbb{Z} \times \mathbb{Z}/2)$-bigraded, the first being the _cohomological grading_ $n$ in $\wedge^\n \mathfrak{g}^\ast$, the second being the _super-grading_ $\sigma$ (even/odd).

For $\alpha_i \in CE(\mathfrak{g})$ two elements of homogeneous bi-degree $(n_i, \sigma_i)$, respectively,
the [[signs in supergeometry|sign rule]] is

$$
  \alpha_1 \wedge \alpha_2 = (-1)^{n_1 n_2} (-1)^{\sigma_1 \sigma_2}\; \alpha_2 \wedge \alpha_1
  \,.
$$

(See at _[[signs in supergeometry]]_ for discussion of this sign rule and of an alternative sign rule that is also in use. )

=--

We may think of $CE(\mathfrak{g})$ equivalently as the [[dg-algebra]] of [[invariant differential form|left-invariant]]
[[super differential forms]] on the [[Lie theory|corresponding]] simply connected [[super Lie group]] .


The concept of [[Chevalley-Eilenberg algebras]] is traditionally introduced as a means to define
[[Lie algebra cohomology]]:

+-- {: .num_defn #SuperLieAlgebraCohomology}
###### Definition

Given a [[super Lie algebra]] $\mathfrak{g}$, then

1. an _$n$-cocycle_ on $\mathfrak{g}$ (with [[coefficients]] in $\mathbb{R}$) is an element of degree $(n,even)$ in its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$ (def. \ref{CEAlgebraofSuperLieAlgebra}) which is $d_{\mathbb{g}}$ closed.

1. the cocycle is non-trivial if it is not $d_{\mathfrak{g}}$-exact

1. hene the _super-[[Lie algebra cohomology]]_ of $\mathfrak{g}$ (with [[coefficients]] in $\mathbb{R}$) is the [[cochain cohomology]] of its [[Chevalley-Eilenberg algebra]]

   $$
     H^\bullet(\mathfrak{g}, \mathbb{R}) = H^\bullet(CE(\mathfrak{g}))
     \,.
   $$

=--



The following says that the [[Chevalley-Eilenberg algebra]] is an equivalent incarnation of the [[super Lie algebra]]:

+-- {: .num_prop}
###### Proposition

The functor

$$
  CE \;\colon\; sLieAlg^{fin}  \hookrightarrow dgAlg^{op}
$$

that sends a finite dimensional [[super Lie algebra]] $\mathfrak{g}$ to its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$
(def. \ref{CEAlgebraofSuperLieAlgebra}) is a [[fully faithful functor]] which hence exibits [[super Lie algebras]]
as a [[full subcategory]] of the [[opposite category]] of [[differential-graded algebras]].

=--


### As super-representable Lie algebras in the topos over superpoints



Equivalently, a super Lie algebra is a "super-representable" Lie algebra [[internalization|internal]] to the [[cohesive (∞,1)-topos]] [[Super∞Grpd]] over the site of [[super points]] ([Sachse 08](#Sachse08)). 

See the discussion at [[superalgebra]] for details on this.



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

Some obvious but important classes of examples are the following:

+-- {: .num_example #SuperVectorSpaceAsAbelianSuperLieAlgebra}
###### Example

every $\mathbb{Z}/2$-[[graded vector space]] $V$ becomes a
[[super Lie algebra]]
(def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}, prop. \ref{SuperLieAlgebraTraditional})
by taking the super Lie bracket to be the [[zero morphism|zero map]]

$$
  [-,-] = 0
  \,.
$$

These may be called the "abelian" super Lie algebras.

=--


+-- {: .num_example #OrdinaryLieAlgebraAsSuperLieAlgebra}
###### Example

Every ordinary [[Lie algebras]] becomes a [[super Lie algebra]]
(def. \ref{SuperLieAlgebraAsLieAlgebraInternalToSuperVectorSpaces}, prop. \ref{SuperLieAlgebraTraditional})
concentrated in even degrees. This constitutes a [[fully faithful functor]]

$$
  LieAlg \hookrightarrow sLieAlg
  \,.
$$

which is a  [[coreflective subcategory]] inclusion in that it has a [[left adjoint]]

$$
  LieAlg
    \underoverset
     {\underset{ \overset{ \rightsquigarrow}{(-)} }{\longleftarrow}}
     {\hookrightarrow}
     {\bot}
  sLieAlg
$$

given on the underlying super vector spaces by restriction to the even graded part

$$
  \overset{\rightsquigarrow}{\mathfrak{s}} = \mathfrak{s}_{even}
  \,.
$$

=--


* The [[super Poincare Lie algebra]] and various of its polyvector extension are super-extension of the ordinary [[Poincare Lie algebra]]. These are the [[supersymmetry algebras]] in the strict original sense of the word.  For more on this see at _[[geometry of physics -- supersymmetry]]_.

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


Discussion in the topos over superpoints is in 

* {#Sachse08} [[Christoph Sachse]], _A Categorical Formulation of Superalgebra and Supergeometry_ ([arXiv:0802.4067](http://arxiv.org/abs/0802.4067))


Discussion of  [[Lie algebra extensions]] for super Lie algebras includes

* [[Dmitri Alekseevsky]], [[Peter Michor]], Wolfgang Ruppert, _Extensions of super Lie algebras_, J. Lie Theory 15 (2005) No. 1, 125--134 ([arXiv:math/0101190](http://arxiv.org/abs/math/0101190))


[[!redirects Lie superalgebra]]
[[!redirects super Lie algebras]]