
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

For *any* group $G$, the *Burnside rig* of $G$ is the set of isomorphism classes of the [[topos]] $FinSet^G$, the category of [[permutation representations]] of $G$ on finite sets, equipped with the addition operation descended from [[coproducts]] in $FinSet^G$ and the multiplication operation descended from [[products]] in $FinSet^G$. In fact the Burnside rig $B(G)$ is an [[exponential rig]], where exponentiation is derived from the [[cartesian closed category|cartesian closed structure]] of the topos. 

The *Burnside ring* $A(G)$ is then the (additive) [[group completion]] of the Burnside rig, $A(G) = \mathbb{Z} \otimes_{\mathbb{N}} B(G)$. (This tensor product in [[commutative monoids]] is the coproduct of $\mathbb{Z}$ and $B(G)$ in the category of commutative rigs, and $\mathbb{Z} \otimes_{\mathbb{N}} -$ is [[left adjoint]] to the forgetful functor from [[commutative rings]] to commutative rigs.) 

## Properties

### In equivariant homotopy theory

It turns out that the Burnside ring is isomorphic to the [[colimit]]

$$
  A(G) \simeq \underset{\longrightarrow}{\lim}_V [S^V,S^V]_G
$$

over $G$-[[representations]] in a complete [[G-universe]], of $G$-[[homotopy classes]] of $G$-equivariant based [[continuous functions]] from the [[representation sphere]] $S^V$ to itself.

([Greenlees-May 95, p. 8](#GreenleesMay95))

See also at _[[orbit category]]_.

## References

* {#GreenleesMay95} [[John Greenlees]], [[Peter May]], section 2 of _Equivariant stable homotopy theory_, in I.M. James (ed.), _Handbook of Algebraic Topology_ , pp. 279-325. 1995. ([pdf](http://www.math.uchicago.edu/~may/PAPERS/Newthird.pdf))


[[!redirects burnside ring]] 
[[!redirects Burnside rig]] 
[[!redirects burnside rig]] 
