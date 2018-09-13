

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
    R(R)
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

[[!include Segal completion -- table]]

## Examples

### Permutation representations
 {#ExamplesPermutationRepresentations}

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

### Virtual permutation representations
 {#ExamplesVirtualPermutationRepresentations}

We discuss here examples of the operation of forming _virtual_ linear permutation representations (Remark \ref{VirtualLinearPermuationRepresentations}), regarded as the canonical [[ring homomorphism]]

$$
  A(G) \overset{ \phantom{AA} \beta \coloneqq K(k[-]) \phantom{AA} }{\longrightarrow} R(G)
$$

from Def. \ref{ComparisonMapBurnsideRingRepresentationRing}. 

For emphasis, notice that among plain [[linear representation]] the linear permutation representations generally form but a tiny sub-class, i.e. generically a [[linear representation]] is _not_ a linear permutation representation. But this statement may change radically as we pass to _virtual_ representations:

If the [[ring homomorphism]] $\beta$ (Def. \ref{ComparisonMapBurnsideRingRepresentationRing}) is [[surjective function]], this means that in fact _all_ virtual linear $G$-representation are virtual linear permutation representations. This is not the case for all groups, but it is the case for large classes of groups! This is the content of Prop. \ref{WhenAllVirtualLinearRepsAreVirtualPermutationReps} below.

Notice that when this is the case, it means that the [[representation theory]] of the given group is, in a precise sense, purely _[[combinatorics|combinatorial]]_, or equivalently, in view of (eq:ComparisonInStableHomotopytheoryInStages), that it is fully determined over the [[absolute ground field]] $\mathbb{F}_1$.

+-- {: .num_prop #WhenAllVirtualLinearRepsAreVirtualPermutationReps}
###### Proposition
**(virtual linear reps from virtual permutation reps)**

For [[ground field]] $k = \mathbb{Q}$ the [[rational numbers]], the comparison morphism

$$
  A(G) \overset{ \beta = K(k[-]) }{\longrightarrow} R(G)
$$

from Def. \ref{ComparisonMapBurnsideRingRepresentationRing}, which sends [[Burnside ring|virtual G-sets]]  to [[representation ring|virtual linear G-representations]],

1. is [[surjective map|surjective]] in the following cases (not mutually exclusive):

   1. $G$ is a [[p-primary group]],

   1. $G$ is a [[cyclic group]],

1. is _not_ [[surjective map|surjective]] in the following example:

   * $G = \mathbb{Z}/3 \times Q_8$ ([[direct product]] of [[cyclic group]] of [[order of a group|order]] 3 with [[quaternion group]] or order 8);

1. is [[injective map|injective]] precisely if

   * $G$ is a [[cyclic group]];

1. is an [[isomorphism]] if 

   * $G$ is a [[cyclic group]].

=--


+-- {: .proof}
###### Proof


The proof of surjectivity for [[p-primary groups]] is due to [Segal 72](#Segal72). (As Segal remarks on his first page, it may also be deduced from [Feit 67 (14.3)](#Feit67). See also [Ritter 72](#Ritter72).)

To see surjectivity for [[cyclic groups]]: By the previous statement we have surjectivity already for those cyclic groups whose order is a prime power. But by the [[fundamental theorem of cyclic groups]], every cyclic group is a [[direct product group]] of cyclic groups of prime power order. Moreover, every irreducible representation of a direct product group is an [[external tensor product]] of irreps of the group factors ([this prop.](direct+product+group#IrrepsOfDirectProductsAreExternalTensorProductsOfIrreps)). But $\beta$ sends "external Cartesian products" to external tensor products, by the same elementary argument which shows that $\beta$ sends plain Cartesian products to tensor products. This way the statement reduces to that for $p$-primary cyclic groups.

The non-surjectivity for $G = \mathbb{Z}/3 \times Q_8$ was remarked in [Serre 77, p. 104](#Serre77).

To see that injectivity holds precisely for [[cyclic groups]], notice that over $k = \mathbb{Q}$ we have that

1. the number of [[isomorphism classes]] of [[irreducible representations]] of $G$ equals the number of [[conjugacy classes]] of _[[cyclic group|cyclic]2]_ [[subgroups]];

1. the number of [[isomorphism classes]] of indecomposable ([[transitive action|transitive]]) [[G-sets]] (i.e. $G$-[[orbit]] types) is the number of [[conjugacy classes]] of _all_ [[subgroups]].

(stolen from [Webster on MO, 2013](https://mathoverflow.net/a/21204/381)).

This means that for $G$ not a cyclic group we have $dim(A(G)) \gt dim(R(G))$, so that $\beta$ cannot be injective. On the other hand, for $G$ a cyclic group this says that $dim(A(G)) = dim(R(G))$, so that if $\beta$ were not injective, its image would have dimension $\lt dim(R(G))$, which however contradicts the surjectivity asserted by item 2 above.

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
**(virtual permutation representations of [[symmetric group]] $S_4$)**

For $G = S_4$ the [[symmetric group]] on four elements, the comparison morphism from the [[Burnside ring]] to the [[representation ring]] (Def. \ref{ComparisonMapBurnsideRingRepresentationRing}) 

$$
  A(S_4)
  \overset{\beta}{\longrightarrow}
  R(S_4)
$$

is a  [[surjective map]] at least over $k =\mathbb{R}$ (see [Montaldi](#Montaldi), bottom of [this page](http://www.maths.manchester.ac.uk/~jm/wiki/Representations/S4)) and $k =\mathbb{C}$ (see at _[Categorified Gram-Schmidt process](Gram-Schmidt+process#CategorifiedGramSchmidtProcess)_).


=--


## Related entries

* [[representation theory]], [[linear representation]],
  [[category of representations]]

* [[covering space]]

* [[Burnside ring]]

* [[groupoidification]]

## Related concepts

* [[regular representation]]

* [[∞-permutation representation]]

## References

* {#Feit67} [[Walter Feit]], _Characters of Finite Groups_, W. A. Benjamin New York, 1967

* D. L. Johnson, _Minimal Permutation Representations of Finite Groups_, 
American Journal of Mathematics Vol. 93, No. 4 (Oct., 1971), pp. 857-866 ([jstor:2373739](https://www.jstor.org/stable/2373739))

* {#Ritter72} J. Ritter, _Ein Induktionssatz fuer rationale Charaktere von nilpotenten Gruppen, J. Reine Angew. Math. 254 (1972), 133–151

* {#Segal72} [[Graeme Segal]], _Permutation representations of finite $p$-groups, Quart. J. Math. Oxford (2) 23 (1972), 375–381 ([web](https://academic.oup.com/qjmath/article/23/4/375/1560108))

* {#Serre77} [[Jean-Pierre Serre]], _Linear Representations of Finite Groups_, Graduate Texts in Math., vol. 42, Springer–Verlag, New York, 1977

* {#Berz94} G. Berz, _Permutationsbasen fuer endliche Gruppen_, Ph.D. thesis, Augsburg, 1994 (Zbl0924.20003)

* {#HambletonTaylor99} I. Hambleton, L. R. Taylor, _Rational permutation modules for finite groups_, Math. Z. 231 (1999), 707–726 ([pdf](https://link.springer.com/content/pdf/10.1007/PL00004749.pdf))

* {#BartelDokchitser11} Alex Bartel, Tim Dokchitser, _Brauer relations in finite groups_, J. Eur. Math. Soc. 17 (2015), 2473-2512 ([arXiv:1103.2047](https://arxiv.org/abs/1103.2047))

* {#BartelDokchitser14} Alex Bartel, Tim Dokchitser, _Rational representations and permutation representations of finite groups_, Math. Ann. 364 no. 1 (2016), 539-558 ([arXiv:1405.6616](https://arxiv.org/abs/1405.6616))


See also

* {#Montaldi} James Montaldi, _[Real representations of finite groups](http://www.maths.manchester.ac.uk/~jm/wiki/Representations/Representations)_

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