
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

## Properties

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

This is originally due to [Segal 71](#Segal71), a detailed proof is given by [tom Dieck 79, theorem 8.5.1](#tomDieck79). See also [Lück 05, theorem 1.13](#Lueck05), [tom Dieck-Petrie 78](#tomDieckPetrie78).

More generally, this staement is a special case of [[tom Dieck splitting]] of [[equivariant suspension spectra]], see [there](tom+Dieck+splitting#OfFixedPointSpectraOfEquivariantSuspensionSpectra).

[[!include Segal completion -- table]]

More explicitly, this means that the Burnside ring of a group $G$ is isomorphic to the [[colimit]]

$$
  A(G) \simeq \underset{\longrightarrow}{\lim}_V [S^V,S^V]_G
$$

over $G$-[[representations]] in a complete [[G-universe]], of $G$-[[homotopy classes]] of $G$-equivariant based [[continuous functions]] from the [[representation sphere]] $S^V$ to itself ([Greenlees-May 95, p. 8](#GreenleesMay95)).

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

## References

The concept was named by Dress, following

* {#Burnside1897} [[William Burnside]], _Theory of Groups of Finite Order_, 1897 ([pdf](http://www.gutenberg.org/files/40395/40395-pdf.pdf))

Textbook and lecture notes include

* {#tomDieck79} [[Tammo tom Dieck]], _[[Transformation Groups and Representation Theory]]_, Springer 1979

* {#tomDieck09} [[Tammo tom Dieck]], _Representation theory_, 2009 ([pdf](http://www.uni-math.gwdg.de/tammo/rep.pdf))

See also

* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], section 2 of _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))

* {#Schanuel91} [[Stephen Schanuel]], 1991, _Negative sets have Euler characteristic and dimension_, in: Proc. Como 1990. Lecture Notes in Mathematics, vol. 1488. Springer-Verlag, Berlin, pp. 379&#8211;385.

Discussion in relation to [[equivariant stable cohomotopy]] and the [[Segal-Carlsson completion theorem]] is in

* {#Segal71} [[Graeme Segal]], _Equivariant stable homotopy theory_, In Actes du Congr&egrave;s International des Math &eacute;maticiens (Nice, 1970), Tome 2 , pages 59–63. Gauthier-Villars, Paris, 1971

* {#tomDieckPetrie78} [[Tammo tom Dieck]], T. Petrie, _Geometric modules over the Burnside ring_, Invent. Math. 47 (1978) 273-287 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/tomDieck-geometric.pdf))

* Erkki Laitinen, _On the Burnside ring and stable cohomotopy of a finite group_,  Mathematica Scandinavica Vol. 44, No. 1 (August 30, 1979), pp. 37-72 ([jstor:24491306](https://www.jstor.org/stable/24491306), [[Laitinen79.pdf:file]])  

* [[Gunnar Carlsson]], _Equivariant Stable Homotopy and Segal's Burnside Ring Conjecture_,  Annals of Mathematics Second Series, Vol. 120, No. 2 (Sep., 1984), pp. 189-224 ([jstor:2006940](https://www.jstor.org/stable/2006940), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/carlsson.pdf))

* {#Lueck05} [[Wolfgang Lück]], _The Burnside Ring and Equivariant Stable Cohomotopy for Infinite Groups_ ([arXiv:math/0504051](https://arxiv.org/abs/math/0504051))

See also

* {#GayMorrisMorris} C. D. Gay, G. C. Morris, and I. Morris, _Computing Adams operations on the Burnside ring of a finite group_, J. Reine Angew. Math., 341 (1983), pp. 87–97.

[[!redirects Burnside rings]]

[[!redirects burnside ring]] 
[[!redirects burnside rings]] 

[[!redirects Burnside rig]] 
[[!redirects Burnside rigs]] 

[[!redirects burnside rig]] 
[[!redirects burnside rigs]] 
