

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}



## Definition

For $G$ a [[group]] (tyically a [[finite group]]), consider a [[G-set]] $(S, \rho)$, hence a [[set]] $S$ (typically a [[finite set]]), equipped with an [[action]] of $G$

$$
  \rho \;\colon\; G \times S \longrightarrow S
  \,.
$$

Equivalently this is a [[group homomorphism]]

$$
  \rho \;\colon\; G \longrightarrow Aut_{Set}(S)
$$

from $G$ to the group of [[permutations]] of elements of $S$. As such it is a representation of $G$ "by permutations".

Specifically, if $S$ is a [[finite set]] and an [[isomorphism]] $S \simeq \{1, 2, 3, \cdots, n\}$ is understood, it is equivalently a [[group homomorphism]]

$$
  \rho \;\colon\; G \longrightarrow S_n
$$

to the [[symmetric group]] $S_n$ on $n$ elements.


For $k$ any [[field]] (or, more generally, any [[commutative ring]], but one mostly considers fields) this $G$-[[action]] may be _linearized_ to a $k$-[[linear representation]] of $G$ in an evident way: 

+-- {: .num_defn #LinearPermutationRepresentation}
###### Definition
**(linear permutation representation)**

The _linear permutation representation_ of a [[G-set]] $(S,\rho)$ is the following $k$-[[linear representation]] of $G$:

1. The underlying $k$-[[vector space]] is the [[free module|freely]] [[linear span|spanned]] vector space $k[S]$, whose elements ([[vectors]]) are the [[formal linear combinations]] 

   $$
     k[S]
     \;=\;
     \left\{
       v =\underset{ s \in S_{fin} \subset S }{\sum} v_s \, s
       \;\vert\;
       S_{fin} \, \text{finite subset}
       ,\;
       v_s \in k
     \right\}
   $$

   of elements of $S$ with [[coefficients]] in $k$, hence is the $k$-vector space for which $S$ is a canonical [[linear basis]].

1. The linear $G$-[[action]]

   $$
     k[\rho] \;\colon\; G \times k[\mathbb{C}] \longrightarrow k[\mathbb{C}]
   $$

   is given on [[linear basis]]-elements $s \in S \hookrightarrow k[S]$ by $\rho$, which uniquely defines it by linearity to act on a general vector as

   $$
     k[\rho]\left(g\right)
     \;\colon\;
     v 
     \;\mapsto\;
     \underset{ s \in S_{fin} \subset S }{\sum} v_s \, \rho(g)(s)
     \,.
   $$

=--

This concept immediately generalizes to [[groupoid representations]] and so forth, see also at _[[infinity-action]]_ the section _[Examples -- Discrete group actions on sets](infinity-action#ExamplesPermutationRepresentations)_.



## Properties

### Functoriality

+-- {: .num_prop #FunctorialityOfLinearPermutationRepresentations}
###### Proposition
**(functoriality of linear permutation representations)**

The construction of linear permutation representations (Def. \ref{LinearPermutationRepresentation}) evidently extends to a [[functor]] from the [[category of G-sets]] $G Set$ to the [[category of representations|category of linear representations]] $G Rep$

$$
  G Set
    \overset{ \phantom{AA} k[-] \phantom{AA} }{\longrightarrow}
  G Rep
  \,.
$$

Both of these categories are [[rig categories]] with respect to [[disjoint union]] and [[Cartesian product]] on the left, and [[direct sum]] and [[tensor product of representations]] on the right.

The functor $k[-]$ is canonically a homomorphism of rig-categories in that in that it is canonically a [[strong monoidal functor]] for both "addition" and "multiplication" [[monoidal category|monoidal structures]]:

$$
  \big(G Set, \sqcup, \times\big)
    \overset{ \phantom{AA} k[-] \phantom{AA} }{\longrightarrow}
  \big(G Rep, \oplus, \otimes \big)
  \,.
$$



=--

### Comparison from Burnside- to representation ring
 {#ComparisonMapFromBurnsideRingToRepresentationRing}


Let $G$ be a [[finite group]] and assume all [[G-sets]] in the following to be [[finite sets]] and all [[linear representations]] to be [[finite-dimensional vector spaces|finite dimensional]].

Consider

1. the [[Burnside ring]] $A(G)$, which is the [[Grothendieck ring]] of the [[rig-category]] $(G Set, \sqcup, \times)$ [[category of G-sets|of finite G-sets]];

1. the [[representation ring]] $R(G)$, which is the [[Grothendieck ring]] of the [[rig category]] $(G Rep, \oplus, \otimes)$ [[representation category|of finite-dimensional linear G-representations]].

+-- {: .num_defn #ComparisonMapBurnsideRingRepresentationRing}
###### Definition
**([[permutation representations]] make [[ring homomorphism]] from [[Burnside ring]] to [[representation ring]])**

Since forming $k$-linear permutation representations (Def. \ref{LinearPermutationRepresentation}) is a rig-functor $G Set\overset{k[-]}{\longrightarrow} G Rep$ (Prop. \ref{FunctorialityOfLinearPermutationRepresentations}), under passing to [[Grothendieck rings]] it induces a [[ring homomorphism]]

$$
  K(k[-])
  \;\colon\;
    K( G Set, \sqcup, \times )
    =
    \;
    A(G)
     \overset{\phantom{AA} \beta \phantom{AA}}{\longrightarrow}
    R(G)
    \;
    =
    K( G Rep, \oplus, \otimes)
$$

from the [[Burnside ring]] of $G$ to its [[representation ring]].

This homomorphism is traditionally denoted $\beta$, as shown.

Its [[kernel]] is known as the _Brauer relations_ (e.g. [Bartel-Dokchitser 11](#BartelDokchitser11)). 


=--

+-- {: .num_remark #VirtualLinearPermuationRepresentations}
###### Remark
**(virtual linear permutation representations)**

The [[image]] of the comparison morphism $\beta = K(k[-])$ (Def. \ref{ComparisonMapBurnsideRingRepresentationRing}) may be called the _virtual_ linear permutation representations. 

=--

+-- {: .num_remark}
###### Remark
**(virtual permutation representations from [[equivariant stable cohomotopy]] into [[equivariant K-theory]])**

Under the identitification

1. of the [[Burnside ring]] with the [[equivariant stable cohomotopy]] of the point 

   $$
     A(G) \;\simeq\; \mathbb{S}_G(\ast)
   $$

   (see [there](Burnside+ring#AsTheEquivariantStableCohomotopyOfThePoint))

1. of the [[representation ring]] with the [[equivariant K-theory]] of the point

   $$
     R(G) \;\simeq\; K_G(\ast)
   $$

   (see [there](representation+ring#AsEquivariantKTheoryOfThePoint))

the [[ring homomorphism]] of Def. \ref{ComparisonMapBurnsideRingRepresentationRing} should be image under forming [[equivariant cohomology]] of the [[point]] of the [[initial object in an (infinity,1)-category|initial]] morphism of [[E-infinity ring spectra]]

$$
  \mathbb{S} \longrightarrow KU
$$

from the [[sphere spectrum]] to [[KU]].

Noticing that we may regard [[stable cohomotopy]]/the [[sphere spectrum]] as being the [[algebraic K-theory]] of the "[[field with one element]]" $\mathbb{F}_1$ (see [there](stable+cohomotopy#AsAlgebraicKTheoryOverTheFieldWithOneElement))

$$
  \mathbb{S} \simeq K \mathbb{F}_1
$$

we may regard this as [[extension of scalars]] along $\mathbb{F}_1 \to  \mathbb{C}$ followed by the [[comparison map between algebraic and topological K-theory]]:

\[
  \label{ComparisonInStableHomotopytheoryInStages}
  \mathbb{S} \simeq K\mathbb{F}_1
  \to K\mathbb{C}
  \to KU
  \,.
\]

=--


<center>
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=23">
<img src="https://ncatlab.org/schreiber/files/EquivariantCohomotopyLinearizedToKTheory.jpg" width="640">
</a>
</center>

> graphics grabbed from [SS19](equivariant+Hopf+degree+theorem#SatiSchreiber19)

See also at _[[equivariant Hopf degree theorem]]_.

[[!include Segal completion -- table]]


### Characters

The [[character of a linear representation|characters]] of permutation representations are the [[Burnside marks]] of the underlying [[G-sets]]:

+-- {: .num_prop #MarkHomomorphismIsCharactersOfPermutationRepresentation}
###### Proposition
**([[mark homomorphism]] on [[cyclic groups]] agrees with [[character of a linear representation|characters]] of corresponding [[permutation representations]])**

For $S \in G Set_{fin}$ a [[finite set|finite]] [[G-set]], for $k$ any [[field]] and $k[S] \in Rep_k(G)$ the corresponding [[permutation representation]], the [[character of a representation|character]] $\chi_{k[S]}$ of the [[permutation representation]] at any $g \in G$ equals the [[Burnside marks]] (Def. \ref{BurnsideCharacter}) of $S$ under the [[cyclic group]] $\langle g\rangle \subset G$ [[generators and relations|generated]] by $g$:

$$
  \chi_{k[S]}\big( g \big)
  \;=\;
  \left\vert X^{\langle g \rangle} \right\vert
  \;\in\;
  \mathbb{Z} \longrightarrow k
  \,.
$$

Hence the [[mark homomorphism]] (Def. \ref{BurnsideCharacter}) of $G$-sets restricted to [[cyclic group|cyclic]] [[subgroups]] coincides with the [[character of a representation|characters]] of their [[permutation representations]].

This statement immediately generalizes from plain representations to [[virtual representations]], hence to the [[Burnside ring]].

=--

(e.g. [tom Dieck 09, (2.15)](#tomDieck09))

+-- {: .proof}
###### Proof

By definition of _[[character of a linear representation]]_, we have that 

$$
  \chi_{k[S]}(g)
  = 
  tr_{k[S]}(g)
$$

is the [[trace]] of the [[linear map|linear]] [[endomorphism]] $k[S] \overset{g}{\to} k[S]$ of the given [[permutation representation]].

Now the canonical $k$-[[linear basis]] for $k[S]$ is of course the [[set]] $S$ itself, and so 

$$
  \begin{aligned}
    \chi_{k[S]}(g)
    & =
    \underset{
      s \in S
    }{\sum}
    \left\{
      \array{
         1 &\vert& g(s) = s
         \\
         0 &\vert& \text{otherwise}
      }
    \right.
    \\
    & = 
    \left\vert S^g \right\vert
    \\
    &
    =
    \left\vert S^{\langle g \rangle} \right\vert
  \end{aligned}
$$

Here in the first step we spelled out the definition of [[trace]] in the canonical basis, and in the second step we observed that the [[fixed point set]] of a [[cyclic group]] equals that of any one of its generating elements.

=--



## Examples

### Basic examples

+-- {: .num_example #RegularRepresentation}
###### Example
**([[regular representation]])

For $G$ a [[group]], write, for emphasis, $G_s$ for its underlying [[set]]. Let 

$$
  \array{
    G \times G_s
     &\overset{ \rho_\ell }{\longrightarrow}&
    G_s
    \\
    (g,s) &\mapsto& g \cdot s
  }
$$

be the canonical [[action]] of $G$ on itself, by left multiplication in the group. The corresponding linear permutation representation $(k[G_s], k(\rho_\ell))$ (Def. \ref{LinearPermutationRepresentation}) is called the _[[regular representation]]_ of $G$.

=--


+-- {: .num_example}
###### Example
**([[induced representation of the trivial representation]])**

Let $G$ be a [[finite group]] and $H \overset{\iota}{\hookrightarrow} G$ a [[subgroup]]-inclusion. Then the [[induced representation]] in [[representation category|Rep(G)]] of the [[trivial representation]] $\mathbf{1} \in Rep(H)$ is the [[permutation representation]] $k[G/H]$ of the [[coset]] [[G-set]] $G/H$:

$$
  \mathrm{ind}_H^G\big( \mathbf{1}\big)
  \;\simeq\;
  k[G/H]
  \,.
$$ 

This follows directly as a special case of the general formula for [[induced representations]] of [[finite groups]] ([this Example](induced+representation#InductionOfFiniteDimensionalRepresentationsOfFiniteGroups)).

See at _[[induced representation of the trivial representation]]_ for more.

=--


### Virtual permutation representations
 {#ExamplesVirtualPermutationRepresentations}

We discuss here examples of the operation of forming _virtual_ linear permutation representations (Remark \ref{VirtualLinearPermuationRepresentations}), regarded as the canonical [[ring homomorphism]]

$$
  A(G) \overset{ \phantom{AA} \beta \coloneqq K(k[-]) \phantom{AA} }{\longrightarrow} R(G)
$$

from Def. \ref{ComparisonMapBurnsideRingRepresentationRing}. 

For emphasis, notice that among plain [[linear representations]] the linear permutation representations generally form but a tiny sub-class, i.e. generically a [[linear representation]] is _not_ a linear permutation representation. But this statement may change radically as we pass to _virtual_ representations:

If the [[ring homomorphism]] $\beta$ (Def. \ref{ComparisonMapBurnsideRingRepresentationRing}) is a [[surjective function]], this means that in fact _all_ virtual linear $G$-representation are virtual linear permutation representations. This is not the case for all groups, but it is the case for large classes of groups! This is the content of Prop. \ref{WhenAllVirtualLinearRepsAreVirtualPermutationReps} below.

Notice that when this is the case, it means that the [[representation theory]] of the given group is, in a precise sense, purely _[[combinatorics|combinatorial]]_, or equivalently, in view of (eq:ComparisonInStableHomotopytheoryInStages), that it is fully determined over the [[absolute ground field]] $\mathbb{F}_1$.

+-- {: .num_prop #WhenAllVirtualLinearRepsAreVirtualPermutationReps}
###### Proposition
**(virtual linear reps from virtual permutation reps)**

For [[ground field]] $k = \mathbb{Q}$ the [[rational numbers]], the comparison morphism

$$
  A(G) \overset{ \beta = K(k[-]) }{\longrightarrow} R(G)
$$

from Def. \ref{ComparisonMapBurnsideRingRepresentationRing}, which sends [[Burnside ring|virtual G-sets]]  to their permutation rep [[representation ring|virtual linear G-representations]],

1. is [[surjective map|surjective]] for $G$ among one of the following classes of [[finite groups]] (not mutually exclusive)

   1. [[cyclic groups]],

   1. [[symmetric groups]],

   1. [[p-groups]],

   1. [[binary dihedral groups]] $\;$ $2 D_{2n}$ for (at least) $2 n \leq 12$

   1. the [[binary tetrahedral group]], [[binary octahedral group]], [[binary icosahedral group]],

   1. the [[general linear group]] $GL(2,\mathbb{F}_3)$

1. is _not_ [[surjective map|surjective]] for $G = \mathbb{Z}/3 \times Q_8$ ([[direct product]] of [[cyclic group]] of [[order of a group|order]] 3 with [[quaternion group]] or order 8);

1. is [[injective map|injective]] precisely for [[cyclic groups]], 

1. hence is an [[isomorphism]] precisely for cyclic groups.

=--


+-- {: .proof}
###### Proof

Isomorphy for the case of cyclic groups is spelled out in [tom Dieck 09, Example (4.4.4)](#tomDieck09).

Surjectivity for the case of symmetric groups follows from the theory of [[Young diagrams]] ([Dress 86, section 3](#Dress86)), see also Example \ref{VirtualPermuationRepresentationOfS4} below for further pointers.

The proof of surjectivity for [[p-primary groups]] is due to [Segal 72](#Segal72). (As Segal remarks on his first page, it may also be deduced from [Feit 67 (14.3)](#Feit67). See also [Ritter 72](#Ritter72).) The proof is recalled as [tom Dieck 79, Theorem 4.4.1](#tomDieck79).

Surjectivity for [[binary dihedral groups]] $2 D_{2n}$ for (at least) $2 n \leq 12$, the [[binary tetrahedral group]], [[binary octahedral group]], [[binary icosahedral group]] and the [[general linear group]] $GL(2,\mathbb{F}_3)$ is checked by [[computer experiment]] in [Burton-Sati-Schreiber 18](#BurtonSatiSchreiber18).


The non-surjectivity for $G = \mathbb{Z}/3 \times Q_8$ was remarked in [Serre 77, p. 104](#Serre77).

To see that injectivity holds at most for [[cyclic groups]], notice that over $k = \mathbb{Q}$ we have that

1. the number of [[isomorphism classes]] of [[irreducible representations]] of $G$ equals the number of [[conjugacy classes]] of _[[cyclic group|cyclic]]_ [[subgroups]];

1. the number of [[isomorphism classes]] of indecomposable ([[transitive action|transitive]]) [[G-sets]] (i.e. $G$-[[orbit]] types) is the number of [[conjugacy classes]] of _all_ [[subgroups]].

([tom Dieck 09, Prop. 4.5.4](#tomDieck09))

This means that for $G$ not a cyclic group we have that the [[free abelian group]] $A(G))$ has more [[generators and relations|generators]] than $R(G)$, so that $\beta$ cannot be injective. 

=--

A more general analysis of the [[cokernel]] of $\beta$ is due to [Berz 94](#Berz94), reviewed and expanded on in [Hambleton-Taylor 99](#HambletonTaylor99). See also [Bartel-Dokchitser 14, p. 1](#BartelDokchitser14).

+-- {: .num_example #VirtualPermutationRepresentationsOfZ2}
###### Example
**([[virtual permutation representations]] of the [[group of order 2]]

Let $G = \mathbb{Z}/2$ be the [[cyclic group|cyclic]] [[group of order 2]].

It has two [[conjugacy classes]] of [[subgroups]], 

1. $H =\mathbb{Z}/2$ the group itself,

1. $H = 1$ the [[trivial group]];

and hence two [[isomorphism classes]] of [[transitive action|transitive]] [[G-sets]]

1. $(\mathbb{Z}/2)/(\mathbb{Z}/2) = \ast$ the [[point]] with the [[trivial action]],

1. $(\mathbb{Z}/2)/1 = \mathbb{Z}/2$ the group itself, with the [[regular action]].


The corresponding linear permutation representations (Def. \ref{LinearPermutationRepresentation}) are

1. $k[ (\mathbb{Z}/2)/(\mathbb{Z}/2)] \;\simeq\; \mathbf{1} $, 

   the 1-dimensional [[trivial representation]];

1. $k[ (\mathbb{Z}/2)/1 ] \; \simeq\; \mathbf{1} \oplus \mathbf{1}_{alt}$, 

   the [[direct sum]] of the 1d [[trivial representation]] with the [[alternating representation]].

To see the second item, observe that the non-trivial element $\sigma \in \mathbb{Z}/2$ is represented on $k[\mathbb{Z}/2] \simeq \langle e,\sigma\rangle$ by the [[permutation matrix]]

$$
  \left(
    \array{
      0 & 1
      \\
      1 & 0
    }
  \right)
  \,,
$$

which is [[diagonal matrix|diagonalizable]] over $k = \mathbb{Z}$ with [[eigenvectors]]

1. $\left[\array{ 1 \\ 1 }\right]$ of [[eigenvalue]] $1$, [[linear span|spanning]] the [[trivial representation]] $\mathbf{1}$ of dimension 1;

1. $\left[\array{ 1 \\ -1 }\right]$ of [[eigenvalue]] $-1$, [[linear span|spanning]] the [[alternating representation]] $\mathbf{1}_{alt}$ of dimension 1.

Hence, the [[abelian group]] underlying the [[representation ring]] may be identified with the [[linear span]]

$$
  R(\mathbb{Z}/2) \;\simeq_k\; \langle \mathbf{1}, \mathbf{1}_{alt}  \rangle
$$

and the comparison morphism from the [[Burnside ring]] (Def. \ref{ComparisonMapBurnsideRingRepresentationRing}) is

$$
  \array{
    A(\mathbb{Z}/2)
    &\overset{ \phantom{AA} \beta \phantom{AA}}{\longrightarrow}&
    R(\mathbb{Z}/2)
    \\
    1\, (\mathbb{Z}/2)/(\mathbb{Z}/2) \;-\; 0\, (\mathbb{Z}/2)/(\mathbb{Z}/2) 
      &\mapsto& 
    \mathbf{1}
    \\
    1\, (\mathbb{Z}/2)/1 \;-\; 1\, (\mathbb{Z}/2)/(\mathbb{Z}/2)
      &\mapsto&
    \mathbf{1}_{alt}
    \,,
  }
$$

which is manifestly an [[isomorphism]], in accord with Prop. \ref{WhenAllVirtualLinearRepsAreVirtualPermutationReps}.

=--

+-- {: .num_example #VirtualPermuationRepresentationOfS4}
###### Example
**(virtual permutation representations of [[symmetric groups]])**

For $G = S_n$ a [[symmetric group]] on $n$ elements, the comparison morphism from the [[Burnside ring]] to the [[representation ring]] (Def. \ref{ComparisonMapBurnsideRingRepresentationRing}) 

$$
  A(S_n)
  \overset{\beta}{\longrightarrow}
  R(S_n)
$$

is a  [[surjective map]] over $\mathbb{Q}$ but also over $\mathbb{R}$ and $\mathbb{C}$. 

The special case of $S_4$ is made explicit for $k =\mathbb{R}$ in [Montaldi](#Montaldi), bottom of [this page](http://www.maths.manchester.ac.uk/~jm/wiki/Representations/S4), and for $k =\mathbb{C}$ at _[Categorified Gram-Schmidt process](Gram-Schmidt+process#CategorifiedGramSchmidtProcess)_.

=--



## Related concepts

* [[table of marks]]

* [[symmetric group]]

* [[covering space]]

* [[regular representation]]

* [[Burnside ring]], [[stable cohomotopy]]

* [[groupoidification]]

* [[∞-permutation representation]]

* [[permutation D-brane]]

* [[RR-field tadpole cancellation]]

## References


Textbook accounts and lecture notes include

* Charles Curtis, Irving Reiner, from p. 43 on in _Representation theory of finite groups and associative algebras_, AMS 1962

* {#Feit67} [[Walter Feit]], _Characters of Finite Groups_, W. A. Benjamin New York, 1967

* {#tomDieck79} [[Tammo tom Dieck]], Section 4 of _[[Transformation Groups and Representation Theory]]_, Lecture Notes in Mathematics 766, Springer 1979 ([doi:10.1007/BFb0085965](https://link.springer.com/book/10.1007/BFb0085965))


* {#tomDieck09} [[Tammo tom Dieck]], section 1.2 of _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))


Original articles include

* D. L. Johnson, _Minimal Permutation Representations of Finite Groups_, 
American Journal of Mathematics Vol. 93, No. 4 (Oct., 1971), pp. 857-866 ([jstor:2373739](https://www.jstor.org/stable/2373739))

* {#Ritter72} J. Ritter, _Ein Induktionssatz fuer rationale Charaktere von nilpotenten Gruppen, J. Reine Angew. Math. 254 (1972), 133–151

* {#Segal72} [[Graeme Segal]], _Permutation representations of finite $p$-groups, Quart. J. Math. Oxford (2) 23 (1972), 375–381 ([doi:10.1093/qmath/23.4.375](https://doi.org/10.1093/qmath/23.4.375))

* {#Serre77} [[Jean-Pierre Serre]], _Linear Representations of Finite Groups_, Graduate Texts in Math., vol. 42, Springer–Verlag, New York, 1977

* {#Dress86} [[Andreas Dress]], _Congruence relations characterizing the representation ring of the symmetric group_, Journal of Algebra 101, 350-364 (1986) ([pdf](https://core.ac.uk/download/pdf/82196473.pdf), [[Dress86.pdf:file]])

* {#Berz94} G. Berz, _Permutationsbasen fuer endliche Gruppen_, Ph.D. thesis, Augsburg, 1994 (Zbl0924.20003)

* {#HambletonTaylor99} I. Hambleton, L. R. Taylor, _Rational permutation modules for finite groups_, Math. Z. 231 (1999), 707–726 ([pdf](https://link.springer.com/content/pdf/10.1007/PL00004749.pdf))

* {#BartelDokchitser11} Alex Bartel, Tim Dokchitser, _Brauer relations in finite groups_, J. Eur. Math. Soc. 17 (2015), 2473-2512 ([arXiv:1103.2047](https://arxiv.org/abs/1103.2047))

* {#BartelDokchitser14} Alex Bartel, Tim Dokchitser, _Rational representations and permutation representations of finite groups_, Math. Ann. 364 no. 1 (2016), 539-558 ([arXiv:1405.6616](https://arxiv.org/abs/1405.6616))

* Vladimir V. Kornyak, _An Algorithm to Decompose Permutation Representations of Finite Groups: Polynomial Algebra Approach_ ([arXiv:1801.09786](https://arxiv.org/abs/1801.09786))

* {#BurtonSatiSchreiber18} [[Simon Burton]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Lift of fractional D-brane charge to equivariant Cohomotopy theory|Lift of fractional D-brane charge to equivariant Cohomotopy theory]]_ ([arXiv:1812.09679](https://arxiv.org/abs/1812.09679), [Python code](https://arxiv.org/src/1812.09679v1/anc))


See also

* {#Montaldi} [[James Montaldi]], _[Real representations of finite groups](http://www.maths.manchester.ac.uk/~jm/wiki/Representations/Representations)_

* {#PlanetMathRepAndBurn} [[PlanetMath]], _[representation ring vs burnside ring](https://planetmath.org/RepresentationRingVsBurnsideRing)_


[[!redirects permutation representation]]
[[!redirects permutation representations]]

[[!redirects linear permutation representation]]
[[!redirects linear permutation representations]]

[[!redirects virtual permutation representation]]
[[!redirects virtual permutation representations]]

[[!redirects permutation action]]
[[!redirects permutation actions]]

[[!redirects Brauer relation]]
[[!redirects Brauer relations]]