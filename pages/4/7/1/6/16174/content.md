
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

## Idea

The Burnside ring $A(G)$ of a [[finite group]] $G$ is the analogue of the [[representation ring]] in the category of [[finite sets]], as opposed to the category of [[finite dimensional vector spaces]] over a field $F$.

Elements of the Burnside ring are thus formal differences of [[G-sets]] (with respect to [[disjoint union]]).

$A$ is a contravariant functor $\text{FinGrp} \xrightarrow{A} \text{AbRing}$.

## Definition 

For *any* group $G$, the *Burnside [[rig]]* of $G$ is the set of isomorphism classes of the [[topos]] $FinSet^G$, the category of [[permutation representations]] of $G$ on finite sets, equipped with the addition operation descended from [[coproducts]] in $FinSet^G$ and the multiplication operation descended from [[products]] in $FinSet^G$. In fact the Burnside rig $B(G)$ is an [[exponential rig]], where exponentiation is derived from the [[cartesian closed category|cartesian closed structure]] of the topos. 

The *Burnside ring* $A(G)$ is then the (additive) [[group completion]] of the Burnside rig, $A(G) = \mathbb{Z} \otimes_{\mathbb{N}} B(G)$. (This tensor product in [[commutative monoids]] is the coproduct of $\mathbb{Z}$ and $B(G)$ in the category of commutative rigs, and $\mathbb{Z} \otimes_{\mathbb{N}} -$ is [[left adjoint]] to the forgetful functor from [[commutative rings]] to commutative rigs.) 

More generally, any [[distributive category]] determines a Burnside rig ([Schanuel91](#Schanuel91)). 

Explicitly, the Burnside ring can be seen to be the free abelian group on the set $G / H_1 , G / H_2, \ldots, G / H_t$ of $G$, where $H_{1}, \ldots, H_{t}$ are representatives of the distinct conjugacy classes of $G$, equipped with the product described in Definition \ref{BurnsideMultiplicities}. 

## Properties

### Span by the coset spaces $G/H$

Since every [[finite set|finite]] [[G-set]] is a [[direct sum]] of the basic [[coset spaces]] $G/H$, for $H \hookrightarrow G$ [[subgroups]] of $G$, and since $G/H_1$ and $G/H_2$ are [[isomorphism|isomorphic]] [[G-sets]] of $H_1$ and $H_2$ are [[conjugation action|conjugate]] to each other, the Burnside ring is spanned, as an [[abelian group]] by the $[G/H]$ for $H$ ranging over [[conjugacy classes]] of subgroups.

$$
  A(G)
  \;\simeq_{\mathbb{Z}}\;
  \underset{[H \subset G]}{\oplus}
  [G/H]
  \,.
$$

Notice that the [[permutation representations]] $k[G/H]$ corresponding to these generators are precisely the [[induced representations of trivial representations]]: $k[G/H] \simeq ind_H^G(\mathbf{1})$.

### In terms of the table of marks
 {#InTermsOfTheTableOfMarks}

We discuss how the product in the Burnside ring is encoded in the [[table of marks]] of the given [[finite group]].

+-- {: .num_defn #BurnsideMultiplicities}
###### Definition
**(Burnside multiplicities)**

Given a choice of [[linear order]] on the [[conjugacy classes]] of [[subgroups]] of $G$ (for instance as in [this Lemma](table+of+marks#LinearOrderOnConjugacyClassesOfSubgroups)), we say that the corresponding _structure constants_ of the [[Burnside ring]] (or _Burnside multiplicities_) are the [[natural numbers]] 

\[
  n_{i j}^\ell \;\in\; \mathbb{N}
\] 

uniquely defined by the [[equation]]

\[
  \label{BurnsideStructureConstants}
  [G/H_i] \times [G/H_j]
  \;=\;
  \underset{ \ell }{\sum}
  n_{i j}^\ell [G/H_\ell]
  \,.
\]

=--

+-- {: .num_prop #BurnsideProductInTermsOfTableOfMarks}
###### Proposition
**([[Burnside ring]] product in terms of [[table of marks]])**

The Burnside ring structure constants  $\left( n_{i j}^\ell\right)$ (Def. \ref{BurnsideMultiplicities}) are equal to the following algebraic expression in the [[table of marks]] $M$ and its [[inverse matrix]] $M^{-1}$ (which exists by [this Prop.](table+of+marks#TableOfMarksIsInvertibleUpperTriangular)):

$$
  n_{i j}^l
  \;=\;
  \underset{1 \leq m \leq t}{\sum}
  M_{i m} \cdot M_{j m}
  \cdot
  (M^{-1})_{m l}
$$

where $t$ is the dimension of $M$, i.e. $M$ is a $t \times t$ matrix.
=--

For [[proof]] see at _[[table of marks]]_, [this Prop.](table+of+marks#BurnsideProductInTermsOfTableOfMarks)

<br/>

### As the equivariant stable cohomotopy of the point
 {#AsTheEquivariantStableCohomotopyOfThePoint}

+-- {: .num_prop #BurnsideRingIsEquivariantStableCohomotopyOfPoint}
###### Proposition
**([[Burnside ring is equivariant stable cohomotopy of the point]])**

Let $G$ be a [[finite group]], then its [[Burnside ring]] $A(G)$ is [[isomorphism|isomorphic]] to the [[equivariant stable cohomotopy]] [[cohomology ring]] $\mathbb{S}_G(\ast)$ of the [[point]] in degree 0. 

$$
  A(G) \overset{\simeq}{\longrightarrow} \mathbb{S}_G(\ast)
  \,.
$$

=--

This is originally due to [Segal 71](#Segal71), a detailed proof is given by [tom Dieck 79, theorem 7.6.7, 8.5.1](#tomDieck79). See also [Lück 05, theorem 1.13](#Lueck05), [tom Dieck-Petrie 78](#tomDieckPetrie78).

From a broader perspective, this statement is a special case of [[tom Dieck splitting]] of [[equivariant suspension spectra]] (e.g. [Schwede 15, theorem 6.14](#Schwede15)), see [there](tom+Dieck+splitting#OfFixedPointSpectraOfEquivariantSuspensionSpectra). 

[[!include Segal completion -- table]]

More explicitly, this means that the Burnside ring of a group $G$ is isomorphic to the [[colimit]]

$$
  A(G) \simeq \underset{\longrightarrow}{\lim}_V [S^V,S^V]_G
$$

over $G$-[[representations]] in a complete [[G-universe]], of $G$-[[homotopy classes]] of $G$-equivariant based [[continuous functions]] from the [[representation sphere]] $S^V$ to itself ([Greenlees-May 95, p. 8](#GreenleesMay95)).

### As the endomorphism ring of the additive Burnside category



+-- {: .num_example #BurnsideRingIsEndomorphismRingInBurnsideCategory}
###### Example
**([[Burnside ring]] is [[endomorphism ring]] of [[additive Burnside category]])**

The [[endomorphism ring]] of the [[terminal object|terminal]] [[G-set]] (the [[point]] $\ast$ equipped with the, necessarily, [[trivial action]]) in the [[additive Burnside category]] $G Burn_{ad}$ is the _Burnside ring_ $A(G)$:

$$
  End_{G Burn_{ad}}(\ast, \ast)
  \;\simeq\;
  A(G)
  \,.
$$


=--


### Relation to representation ring

Let $G$ be a [[finite group]]. Consider

1. the [[Burnside ring]] $A(G)$, which is the [[Grothendieck group]] of the [[monoidal category]] $G Set$ of [[finite set|finite]] [[G-sets]];

1. the [[representation ring]] $R(G)$, which is the [[Grothendieck group]] of the monoidal category $G Rep$ of [[finite dimensional vector space|finite dimensional]] $G$-[[linear representations]].

Then then map that sends a G-set to the corresponding linear [[permutation representation]] is a [[strong monoidal functor]]

$$
  G Set \overset{\mathbb{C}[-]}{\longrightarrow} G Rep
$$

and hence induces a [[ring homomorphism]]

$$
  A(G) \overset{ \mathbb{C}[-] }{\longrightarrow} R(G)
$$

Under the identitification

1. of the [[Burnside ring]] with the [[equivariant stable cohomotopy]] of the point 

   $$
     A(G) \;\simeq\; \mathbb{S}_G(\ast)
   $$

   (as [above](#AsTheEquivariantStableCohomotopyOfThePoint))

1. of the [[representation ring]] with the [[equivariant K-theory]] of the point

   $$
     R(G) \;\simeq\; K_G(\ast)
   $$

   (see [there](representation+ring#AsEquivariantKTheoryOfThePoint))

this should be the image of the initial morphism of [[E-infinity ring spectra]]

$$
  \mathbb{S} \longrightarrow KU
$$

from the [[sphere spectrum]] to [[KU]].

For details on this comparison map see at _[[permutation representation]]_, [this section](permutation+representation#ExamplesVirtualPermutationRepresentations).



## Related concepts

* [[orbit category]]

* [[Segal conjecture]]

* [[equivariant stable cohomotopy]]

* [[beta-ring]]

* [[objective number theory]]

## References
 {#References}

The Burnside product seems to first appear as equation (i) in:

* {#Burnside01} [[William Burnside]], _On the Representation of a Group of Finite Order as a Permutation Group, and on the Composition of Permutation Groups_, Proceedings of the American Mathematical Society 1901 ([doi:10.1112/plms/s1-34.1.159](https://doi.org/10.1112/plms/s1-34.1.159))

(beware the terminology: a [[G-set]] is called a "permutation group $G$" in that article, a [[subset]] is called a "compound" and the [[Cartesian product]] of $G$-sets is called their "compounding").

It is then included (not in the first but) in the second edition (Sections 184-185) of:

* {#Burnside1897} [[William Burnside]], _Theory of Groups of Finite Order_,  Second edition Cambridge 1911 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/burnside1911.pdf)) 

  reprinted by Cambridge University Press 2012 ([doi:10.1017/CBO9781139237253]( https://doi.org/10.1017/CBO9781139237253))


The term "Burnside ring" as well as "Burnside algebra" is then due to (see [NMT 04, Vol. 1 p. 60](William+Burnside#NMT04) for historical comments) 

* {#Solomon67} [[Louis Solomon]], _The Burnside algebra of a finite group_, Journal of Combinatorial Theory Volume 2, Issue 4, June 1967, Pages 603-615 (<a href="https://doi.org/10.1016/S0021-9800(67)80064-4">doi:10.1016/S0021-9800(67)80064-4</a>)

Modern textbook accounts and lecture notes:

* Charles Curtis, Irving Reiner, chapter XI of _Representation theory of finite groups and associative algebras_, AMS 1962

* {#tomDieck79} [[Tammo tom Dieck]], _[[Transformation Groups and Representation Theory]]_, Springer 1979

* {#tomDieck87} [[Tammo tom Dieck]], Chapter IV of: _[[Transformation Groups]]_, de Gruyter 1987 ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372)) 

* {#Bouc00} Serge Bouc, _Burnside rings_, in _Handbook of Algebra_ Volume 2, 2000, Pages 739-804 (<a href="https://doi.org/10.1016/S1570-7954(00)80043-1">doi:10.1016/S1570-7954(00)80043-1</a>)

* {#tomDieck09} [[Tammo tom Dieck]], _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

* {#Schwede15} [[Stefan Schwede]], section 6 of _[[Lectures on Equivariant Stable Homotopy Theory]]_, 2015 ([pdf](http://www.math.uni-bonn.de/people/schwede/equivariant.pdf))


See also

* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], section 2 of _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

* {#Schanuel91} [[Stephen Schanuel]], 1991, _Negative sets have Euler characteristic and dimension_, in: Proc. Como 1990. Lecture Notes in Mathematics, vol. 1488. Springer-Verlag, Berlin, pp. 379&#8211;385.


Discussion in relation to [[equivariant stable cohomotopy]] and the [[Segal-Carlsson completion theorem]] is in

* {#Segal71} [[Graeme Segal]], _Equivariant stable homotopy theory_, In Actes du Congr&egrave;s International des Math &eacute;maticiens (Nice, 1970), Tome 2 , pages 59–63. Gauthier-Villars, Paris, 1971 ([[SegalEquivariantStableHomotopyTheory.pdf:file]])

* {#tomDieckPetrie78} [[Tammo tom Dieck]], T. Petrie, _Geometric modules over the Burnside ring_, Invent. Math. 47 (1978) 273-287;
chapter 10 in: _[[Transformation Groups and Representation Theory]]_  ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/tomDieck-geometric.pdf))

* Erkki Laitinen, _On the Burnside ring and stable cohomotopy of a finite group_,  Mathematica Scandinavica Vol. 44, No. 1 (August 30, 1979), pp. 37-72 ([jstor:24491306](https://www.jstor.org/stable/24491306), [[Laitinen79.pdf:file]])  

* [[Gunnar Carlsson]], _Equivariant Stable Homotopy and Segal's Burnside Ring Conjecture_,  Annals of Mathematics Second Series, Vol. 120, No. 2 (Sep., 1984), pp. 189-224 ([jstor:2006940](https://www.jstor.org/stable/2006940), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/carlsson.pdf))

* {#GayMorrisMorris} C. D. Gay, G. C. Morris, and I. Morris, _Computing Adams operations on the Burnside ring of a finite group_, J. Reine Angew. Math., 341 (1983), pp. 87–97.

* {#Lueck05} [[Wolfgang Lück]], _The Burnside Ring and Equivariant Stable Cohomotopy for Infinite Groups_ ([arXiv:math/0504051](https://arxiv.org/abs/math/0504051))

Computational aspects are discussed in 

* Martin Kreuzer, _Computational aspects of Burnside rings, part I: the ring structure_, D.P. Beitr Algebra Geom (2017) 58: 427 ([doi:10.1007/s13366-016-0324-4](https://doi.org/10.1007/s13366-016-0324-4))

[[!redirects Burnside rings]]

[[!redirects burnside ring]] 
[[!redirects burnside rings]] 

[[!redirects Burnside rig]] 
[[!redirects Burnside rigs]] 

[[!redirects burnside rig]] 
[[!redirects burnside rigs]] 
