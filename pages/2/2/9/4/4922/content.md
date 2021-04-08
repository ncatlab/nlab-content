+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[group]] $G$ and a [[subgroup]] $H$, then their _coset object_ is the [[quotient]] $G/H$, hence the set of [[equivalence classes]] of elements of $G$ where two are regarded as equivalent if they differ by right multiplication with an element in $H$.

If $G$ is a [[topological group]], then the quotient is a [[topological space]] and usually called the _coset space_. This is in particular a [[homogeneous space]], see there for more.

## Definition

### Internal to a general category

In a category $C$, for $G$ a [[group object]] and $H \hookrightarrow G$ a [[subgroup|subgroup object]], the left/right _object of cosets_ is the [[orbit|object of orbits]] of $G$ under left/right multiplication by $H$.

Explicitly, the left coset space $G/H$ [[coequalizes]] the parallel morphisms
$$
  H \times G \underoverset{\mu}{proj_G}\rightrightarrows G 
$$ 
where $\mu$ is (the inclusion $H\times G \hookrightarrow G\times G$ composed with) the group multiplication.  

Simiarly, the right coset space $H\backslash G$ [[coequalizes]] the parallel morphisms
$$
  G \times H \underoverset{proj_G}{\mu}\rightrightarrows G 
$$ 

### Internal to $Set$

Specializing the above definition to the case where $C$ is the well-pointed topos $Set$, given an element $g$ of $G$, its orbit $g H$ is an element of $G/H$ and is called a _left coset_.

Using [[comprehension]], we can write

$$
  G/H = \{g H | g \in G\}
$$

Similarly there is a coset on the right $H \backslash G$.

### For Lie groups and Klein geometry

If $H \hookrightarrow G$ is an inclusion of [[Lie groups]] then the quotient $G/H$ is also called a _[[Klein geometry]]_.

### For $\infty$-groups
 {#ForInfinityGroups}

More generally, given an [[(∞,1)-topos]] $\mathbf{H}$ and a [[homomorphism]] of  [[∞-group]] ojects $H \to G$, hence equivalently a morphism of their [[deloopings]]
$\mathbf{B}H \to \mathbf{B}G$, then the [[homotopy quotient]] $G/H$ is given by the [[homotopy fiber]] of this map

$$
  \array{
    G/H &\longrightarrow& \mathbf{B}H
    \\
    && \downarrow
    \\
    && \mathbf{B}G
  }
  \,.
$$

See at _[[∞-action]]_ for more on this definition. See at _[[higher Klein geometry]]_ and _[[higher Cartan geometry]]_ for the corresponding concepts of [[higher geometry]].

## Properties 

### For normal subgroups

The coset inherits the structure of a group if $H$ is a [[normal subgroup]].

Unless $G$ is abelian, considering both left and right coset spaces provide different information. 


### Topology of the quotient map
 {#QuotientMaps}

+-- {: .num_prop #QuotientProjectionForCompactLieGroupActingFreelyOnManifoldIsPrincipa}
###### Proposition

For $X$ a [[smooth manifold]] and $G$ a [[compact Lie group]] equipped with a [[free action|free]] smooth [[action]] on $X$, then the [[quotient]] [[projection]]

$$
  X \longrightarrow X/G
$$

is a $G$-[[principal bundle]] (hence in particular a [[Serre fibration]]).

=--

This is originally due to ([Gleason 50](#Gleason50)). See e.g. ([Cohen, theorem 1.3](#Cohen))


+-- {: .num_cor #QuotientProjectionForCompactLieSubgroupIsPrincipal}
###### Corollary

For $G$ a [[Lie group]] and $H \subset G$ a [[compact Lie group|compact]] [[subgroup]], then the [[coset]] [[quotient]] [[projection]]

$$
  G \longrightarrow G/H
$$

is an $H$-[[principal bundle]] (hence in particular a [[Serre fibration]]).  

=--

This is originally due to ([Samelson 41](#Samelson41)). 

+-- {: .num_prop #ProjectionOfCosetsIsFiberBundleForClosedSubgroupsOfCompactLieGroup}
###### Proposition

For $G$ a [[compact Lie group]] and $K \subset H \subset G$ [[closed subspace|closed]] [[subgroups]], then the [[projection]] map

$$
  p \;\colon\; G/K \longrightarrow G/H
$$

is a locally trivial $H/K$-[[fiber bundle]] (hence in particular a [[Serre fibration]]).

=--

+-- {: .proof}
###### Proof

Observe that the projection map in question is equivalently

$$
  G \times_H (H/K) \longrightarrow G/H
  \,,
$$

(where on the left we form the [[Cartesian product]] and then divide out the [[diagonal action]] by $H$). This exhibits it as the $H/K$-[[fiber bundle]] [[associated bundle|associated]] to the $H$-[[principal bundle]] of corollary \ref{QuotientProjectionForCompactLieSubgroupIsPrincipal}.

=--

\begin{prop}\label{CosetSpaceCoprojectionsWithLocalSections}
**([[coset space coprojections with local sections]])**\linebreak
Let $G$ be a [[topological group]] and $H \subset G$ a [[subgroup]].

Sufficient conditions for the [[coset space]] [[coprojection]] $G \overset{q}{\to} G/H$ to admit [[local sections]], in that there is an [[open cover]] $\underset{i \in I}{\sqcup}U_i \to G/H$ and a [[continuous section]] $\sigma_{\mathcal{U}}$ of the [[pullback]] of $q$ to the cover,

$$
  \array{
    &&
    G_{\vert \mathcal{U}}
    &\longrightarrow&
    G
    \\
    &
    {}^{\mathllap{
      \exists \sigma
    }}
    \nearrow
    &
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow 
    \\
    \mathllap{ \exists \; } 
    \underset{i \in I}{\sqcup} U_i    
    &=&
    \underset{i \in I}{\sqcup} U_i
    &\longrightarrow&
    G/H
    \mathrlap{\,,}
  }
$$

include the following:

* $G$ is any [[topological group]] 

  and $H$ is a [[compact Lie group]]

  (in particular for $H$ a [[closed subgroup]] if $G$ itself is a [[compact Lie group]], since [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]).

  ([Gleason 50, Thm. 4.1](#Gleason50))


or:

* The underlying [[topological space]] of $G$ is

  1. [[locally compact topological space|locally compact]];

  1. [[separable metric space]];

  1. of [[finite number|finite]] [[dimension of a separable metric space]]

  (e.g. if $G$ is a [[Lie group]])

  and $H \subset G$ is a [[closed subgroup]].

  ([Mostert 53, Theorem 3](#Mostert53))


\end{prop}


### As a homotopy fiber

+-- {: .num_remark}
###### Remark

In [[geometric homotopy theory]] (in an [[(∞,1)-topos]]), for $H \longrightarrow G$ any homomorphisms of [[∞-group]] objects, then the natural projection $G \longrightarrow G/H$, generally realizes $G$ as an $H$-[[principal ∞-bundle]] over $G/H$. This is exhibited by a [[homotopy pullback]] of the form

$$
  \array{
   G & \longrightarrow &* 
   \\
    \downarrow && \downarrow
   \\
   G/H &\longrightarrow& \mathbf{B}H
  }
  \,.
$$

where $\mathbf{B}H$ is the [[delooping|delooping groupoid]] of $H$. This also equivalently exhibits the [[∞-action]] of $H$ on $G$ (see there for more).

By the [[pasting law]] for [[homotopy pullbacks]] then we get the [[homotopy pullback]]

$$
  \array{
   G/H & \longrightarrow &\mathbf{B}H 
   \\
    \downarrow && \downarrow
   \\
   * & \longrightarrow & \mathbf{B}G
  }
$$

which exhibits the coset as the [[homotopy fiber]] of $\mathbf{B}H \to \mathbf{B}G$.

=--

## Examples

### $n$-Spheres

+-- {: .num_example #nSphereAsCosetSpace}
###### Example

The [[n-spheres]] are coset spaces of [[orthogonal groups]]:

$$
  S^n \simeq O(n+1)/O(n)
  \,.
$$

The odd-dimensional spheres are also coset spaces of [[unitary groups]]:

$$
  S^{2n+1}
  \simeq
  U(n+1)/U(n)
$$

=--

+-- {: .proof}
###### Proof

Regarding the first statement:

Fix a [[unit vector]] in $\mathbb{R}^{n+1}$. Then its [[orbit]] under the defining $O(n+1)$-[[action]] on $\mathbb{R}^{n+1}$ is clearly the canonical embedding $S^n \hookrightarrow \mathbb{R}^{n+1}$. But precisely the subgroup of $O(n+1)$ that consists of rotations around the axis formed by that unit vector [[stabilizer group|stabilizes]] it, and that subgroup is isomorphic to $O(n)$, hence $S^n \simeq O(n+1)/O(n)$.

The second statement follows by the same kind of reasoning:

Clearly $U(n+1)$ [[transitive action|acts transitively]] on the [[unit sphere]] $S^{2n+1}$ in $\mathbb{C}^{n+1}$. It remains to see that its [[stabilizer subgroup]] of any point on this sphere is $U(n)$. If we take the point with [[coordinates]] $(1,0, 0, \cdots,0)$ and regard elements of $U(n+1)$ as [[matrices]], then the stabilizer subgroup consists of matrices of the block diagonal form

$$
  \left(
    \array{
      1 & \vec 0
      \\
      \vec 0 & A
    }
  \right)
$$

where $A \in U(n)$.

=--

There are also various exceptional realizations of spheres as coset spaces. For instance:

[[!include coset space structure on n-spheres -- table]]

\linebreak



### Sequences of coset spaces
 {#QuotientMapsOfCosetSpaces}

Consider $K \hookrightarrow H \hookrightarrow G$ two consecutive group inclusions with their induced coset [[quotient]] [[projections]]

$$
  \array{
    H/K & \longrightarrow&  G/K 
    \\
    && \downarrow 
    \\
    && G/H
  }
  \,.
$$

When $G/K \to G/H$ is a [[Serre fibration]], for instance in the situation of prop. \ref{ProjectionOfCosetsIsFiberBundleForClosedSubgroupsOfCompactLieGroup} (so that this is indeed a [[homotopy fiber sequence]] with respect to the [[classical model structure on topological spaces]]) then it induces the corresponding [[long exact sequence of homotopy groups]]

$$
  \cdots
  \to 
  \pi_{n+1}(G/H)
  \longrightarrow
  \pi_n(H/K) \longrightarrow \pi_n(G/K) \longrightarrow \pi_n(G/H)
  \longrightarrow 
  \pi_{n-1}(H/K)
  \to \cdots
  \,.
$$


+-- {: .num_example #CofiberSequencesOfCosetsOfOrthogonalGroups}
###### Example

Consider a sequence of inclusions of [[orthogonal groups]] of the form

$$
  O(n) \hookrightarrow O(n+1) \hookrightarrow O(n+k)
  \,.
$$

Then by example \ref{nSphereAsCosetSpace} we have that $O(n+1)/O(n) \simeq S^n$ is the [[n-sphere]] and by corollary \ref{QuotientProjectionForCompactLieSubgroupIsPrincipal} the quotient map is a [[Serre fibration]]. Hence there is a [[long exact sequence of homotopy groups]] of the form 

$$
  \cdots
  \to 
  \pi_q(S^n) 
  \longrightarrow \pi_q(O(n+k)/O(n)) \longrightarrow \pi_q(O(n+k)/O(n+1))
  \longrightarrow 
  \pi_{q-1}(S^n)
  \to \cdots
  \,.
$$

Now for $q \lt n$ then $\pi_q(S^n) = 0$ and hence in this range we have [[isomorphisms]]

$$
  \pi_{\bullet \lt n}(O(n+k)/O(n)) 
     \stackrel{\simeq}{\longrightarrow}
  \pi_{\bullet \lt n}(O(n+k)/O(n+1))
 \,.
$$

=--



## Related concepts

* [[coset space]]

* [[coadjoint orbit]]

* [[index of a subgroup]]

* [[class equation]]

* [[flag variety]]

* [[Klein geometry]]

* [[WZW model]]

* [[double coset]]

## References

* {#Samelson41} [[Hans Samelson]], _Beiträge zur Topologie der Gruppenmannigfaltigkeiten_, Ann. of Math. 2, 42, (1941), 1091 - 1137. ([jstor:1970463](https://www.jstor.org/stable/1970463), [doi:10.2307/1970463](https://doi.org/10.2307/1970463))

* {#Gleason50} [[Andrew Gleason]], _Spaces with a compact Lie group of transformations_, Proc. of A.M.S 1, (1950), 35 - 43 ([jstor:2032430](https://www.jstor.org/stable/2032430), [doi:10.2307/2032430](https://doi.org/10.2307/2032430))

* {#Steenrod51} [[Norman Steenrod]], Section I.7 of: _The topology of fibre bundles_, Princeton Mathematical Series 14, Princeton Univ. Press, 1951.


* {#Mostert53} [[Paul Mostert]], _Local Cross Sections in Locally Compact Groups_, Proceedings of the American Mathematical Society, Vol. 4, No. 4 (Aug., 1953), pp.645-649 ([jstor:2032540](https://www.jstor.org/stable/2032540), [doi:10.2307/2032540](https://doi.org/10.2307/2032540))

* {#Bredon72} [[Glen Bredon]], Section I.4 of: _[[Introduction to compact transformation groups]]_, Academic Press  1972 ([ISBN 9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1), [pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))


* {#Cohen} R. Cohen, _Topology of fiber bundles_, Lecture notes ([pdf](http://math.stanford.edu/~ralph/fiber.pdf))


[[!redirects coset]]
[[!redirects cosets]]
[[!redirects left coset]]
[[!redirects right coset]]
[[!redirects left cosets]]
[[!redirects right cosets]]

[[!redirects coset space]]
[[!redirects coset spaces]]

