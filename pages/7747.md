+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In one sense of the term, a _framing_ of a [[manifold]] is a choice of trivialization of its [[tangent bundle]], hence a choice of [[section]] of the corresponding [[frame bundle]]. 

A manifold that admits a framing is also called a **parallelizable manifold**. A manifold equipped with a framing is also called a **parallelized manifold**.

More generally, one means by a _framing_ not a trivialization of the tangent bundle itself, but

* of the [[normal bundle]] if the manifold is understood  [[embedding|embedded]] in some [[Cartesian space]] $\mathbb{R}^d$

* of the _[[stable tangent bundle]]_.

Accordingly, a _framed cobordism_ is a [[cobordism]] equipped with a framing on the underlying manifold (see also at [[MFr]]).

For $dim(X)$ the [[dimension]] of the manifold and $n \geq dim(X)$, then one also speaks of an _$n$-framing_ to mean a trivialization of the "$n$-stabilized tangent bundle"  $T X \oplus \mathbb{R}^{n-dim(X)}$ (where the right [[direct sum|direct summand]] denotes the trivial real [[vector bundle]] of [[rank]] $n - dim(X)$). These $n$-framed manifolds appear in particular in the construction of the  [[cobordism category]] of framed $n$-dimensional cobordisms. The [[cobordism hypothesis]] asserts essentially that the [[(∞,n)-category of cobordisms]] with $n$-framing is the [[free construction|free]] [[symmetric monoidal (∞,n)-category with duals]].

Beware that there is also the term "[[2-framing]]" due to ([Atiyah](#Atiyah)), which is related but different.

## Examples

+-- {: .num_prop}
###### Proposition

Every [[Lie group]] is a parallelizable manifold.

=--

+-- {: .proof}
###### Proof

Every non-zero [[invariant vector field]] on the Lie group provides an everywhere non-vanishing section of the tangent bundle.

=--

The following is obvious:

+-- {: .num_prop #SpinManifoldAdmitsFraming}
###### Proposition

Every 3-[[dimension|dimensional]] [[manifold]] with [[spin structure]] admits a framing.

=--

+-- {: .proof}
###### Proof

That a 3-manifold $X$  has [[spin structure]] means that we have a [[reduction of the structure group]] of the tangent bundle to the [[spin group]], and hence the tangent bundle is classified by a map $X \to B Spin(3)$. But $Spin(3)$ has vanishing [[homotopy groups]] in degree $0 \leq k \leq 2$. Therefore its [[delooping]] [[classifying space]] $B Spin(3)$ has vanishing homotopy groups below degree 4 and hence every morphism out of a 3-dimensional manifold into it is homotopically constant.

=--

But in fact the following stronger statement is also true.

+-- {: .num_prop #EveryOrientable3ManifoldsIsParallelizable}
###### Proposition

Every [[orientation|orientable]] 3-[[dimension|dimensional]] [[manifold]] admits a framing.

=--

+-- {: .proof}
###### Proof

By the argument in the proof of 
prop. \ref{SpinManifoldAdmitsFraming}, the only possible 
obstruction is the [[second Stiefel-Whitney class]] $w_2$.  By the discussion at _[[Wu class]]_, this vanishes on an oriented manifold precisely if the second [[Wu class]] vanishes. This in turn is by definition defined to represent the [[Steenrod square]] under [[cup product]], and this vanishes on a 3-manifold by degree reasons.

=--


+-- {: .num_remark #In4dFirstOrderGravity}
###### Remark

Prop. \ref{EveryOrientable3ManifoldsIsParallelizable} has some impact in the context of the [[first order formulation of gravity]], where one is interested in [[vielbein]] fields on 4-dimensional [[spacetime manifolds]], and in particular in [[globally hyperbolic spacetimes]], which, as [[topological spaces]], are the [[Cartesian product]] of the [[real line]] (time) with a [[3-manifold]] (space). Prop. \ref{EveryOrientable3ManifoldsIsParallelizable} implies that already when that spatial 3-manifold is orientable, then the whole globally hyperbolic spacetime admits a framing. (See also at _[[teleparallel gravity]]_.)

=--

+-- {: .num_theorem}
###### Theorem

The $n$-[[spheres]] that admit a framing are precisely only

* the 0-sphere $S^0 = \ast \coprod \ast$, the unit [[real numbers]]

* the 1-sphere $S^1$, the [[circle]] underlying the [[circle group]] (the unit [[complex numbers]]);

* the 3-sphere $S^3$, underlying the [[special unitary group]] $SU(2)$, is isomorphic to the unit [[quaternions]];

* the 7-sphere $S^7$, which underlies a [[Moufang loop]] internal to [[Diff]], namely the unit [[octonions]],

where the algebras appearing are precisely the four [[normed division algebras]].

=--

This is due to ([Adams 58](#Adams58)), proven with the [[Adams spectral sequence]].

### Stable homotopy elements

Left invariant framings $\mathcal{L}$ on compact connected Lie groups $G$ with $dim(G)=k$ give rise to elements $[G,\mathcal{L}]$ in the stable homotopy group $\pi_k^s$ of spheres. One can restrict attention to semisimple Lie groups $G$ since this construction behaves well with respect to products, $G \to T\times G/T$ gives a framed diffeomorphism and  $[S^1,\mathcal{L}] \in \pi_1^s$ is the generator. The following facts are assembled from ([Ossa 1982](#Ossa82)) and ([Minami 2016](#Minami16)).

* For any *semisimple* compact connected Lie group $G$, Ossa proved that $72[G,\mathcal{L}]=0$. In particular the only possible torsion is at the primes 2 and 3.

* The left invariant framings on $SO(n),Spin(n)$ and $SU(n)$ give the zero element for $n\geq 7$, those on $Sp(n)$ for $n\geq 4$, as do those on $F_4,E_6,E_7,E_8, SO(4),SO(6),SU(5),SU(6)$. (this means that the undetermined cases of rank 4 in Ossa's Table 1 are in fact all 0)

* The left invariant framings on the remaining groups ($SU(2)=Spin(3)=Sp(1),SU(3),SU(4)=Spin(6),Sp(2)=Spin(5),Sp(3),SO(3),SO(5)$ and $G_2$) represent known nonzero classes in $\pi_\ast^s$.




## Properties

### Relation to intersection pairing and Kervaire invariant
 {#IntersectionPairing}

On a framed manifold there is a canonical [[quadratic refinement]] of the [[intersection pairing]]. The associated invariant is the _[[Kervaire invariant]]_.

## Properties 

### Moduli of framings

The [[homotopy type]] of the [[moduli space of framed manifolds|moduli space of framings]] on a fixed manifold is a disjoint union of subgroups of the oriented [[mapping class group]] which fix a given isotopy type of framings.

## Related concepts

* [[normal framing]], [[normal twisted framing]]

* [[2-framing]]

* [[framed elliptic curve]]

* [[moduli space of framed manifolds]]

* [[teleparallel gravity]]

Formalization in [[differential cohesion]] is discussed [there](http://ncatlab.org/nlab/show/differential+cohesive+%28infinity%2C1%29-topos#GLnTangentBundles).

## References

### General

Rieview in the context of the [[Kervaire invariant]] includes

* [[Akhil Mathew]], _The Kervaire invariant I_ ([web](https://amathew.wordpress.com/2012/10/01/the-kervaire-invariant-i/#more-3888))


The theorem about the parallizablitiy of spheres is due to

* {#Adams58} [[John Adams]], _On the Non-Existence of Elements of Hopf Invariant One_ Bull. Amer. Math. Soc. 64, 279-282, 1958, Ann. Math. 72, 20-104, 1960.

Relation to existence of [[flat connections]] on the [[tangent bundle]] is discussed in 

* {#Thorpe65} [[John Thorpe]], _Parallelizablility and flat manifolds_, 1965 ([[ThorpeParallelizable.pdf:file]])

### For 2-manifolds

The [[moduli space of framed surfaces]] is discussed in 

*  [[Oscar Randal-Williams]], _Homology of the moduli spaces and mapping class groups of framed, r-Spin and Pin surfaces_ ([arXiv:1001.5366](http://arxiv.org/abs/1001.5366))

### For 3-manifolds

* [[Rob Kirby]], [[Paul Melvin]], _Canonical framings for 3-manifolds_, Turkish Journal of Mathematics, volume 23, number 1,1999 ([[KirbyMelvon3Framings.pdf:file]])
 
The relation to "[[2-framings]]" is discussed in

* {#Atiyah} [[Michael Atiyah]], _On framings of 3-manifolds_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/atiyahfr.pdf))

### Left invariant framings on compact connected Lie groups

* {#Ossa82} Erich Ossa, Lie groups as framed manifolds, Topology, 21 (1982), 315–323, ([doi](https://doi.org/10.1016/0040-9383%2882%2990013-1))

* {#Minami16} Haruo Minami, _On framed simple Lie groups_, ([pdf](http://projecteuclid.org/euclid.jmsj/1468956166))

For an extension to [[p-compact groups]] see

* [[Tilman Bauer]], _p-compact groups as framed manifolds_, ([paper](https://people.kth.se/~tilmanb/publication/p-compact-groups-as-framed-manifolds/))



[[!redirects framed manifolds]]

[[!redirects framed cobordism]]
[[!redirects framed cobordisms]]

[[!redirects parallelizable manifold]]
[[!redirects parallelized manifold]]
[[!redirects parallelizable manifolds]]
[[!redirects parallelized manifolds]]

[[!redirects framing]]
[[!redirects framings]]

[[!redirects parallelizable sphere]]
[[!redirects parallelizable spheres]]

[[!redirects parallelizable]]


[[!redirects n-framing]]
[[!redirects n-framings]]
[[!redirects 1-framing]]
[[!redirects 1-framings]]
[[!redirects 3-framing]]
[[!redirects 3-framings]]
[[!redirects 4-framing]]
[[!redirects 4-framings]]
[[!redirects 5-framing]]
[[!redirects 5-framings]]