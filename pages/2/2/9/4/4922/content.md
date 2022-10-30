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

Given a [[group]] $G$ and a [[subgroup]] $H$, then their _coset_ is the [[quotient]] $G/H$, hence the set of [[equivalence classes]] of elements of $G$ where two are regarded as equivalent if they differ by right multiplication with an element in $H$.

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

Specializing the above definition to the case where $C$ is the well-pointed topos $Set$, given an element $g$ of $G$, its orbit $gH$ is an element of $G/H$ and is called a _left coset_.

Using [[comprehension]], we can write

$$
  G/H = \{g H | g \in G\}
$$

Similarly there is a coset on the right $H \backslash G$.

### For Lie groups and Klein geometry

If $H \hookrightarrow G$ is an inclusion of [[Lie groups]] then the quotient $G/H$ is also called a _[[Klein geometry]]_.

### For $\infty$-groups

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

See at _[[∞-action]]_ for more on this definition. See at _[[higher Klein geometry]_ and _[[higher Cartan geometry]]_ for the corresponding concepts of [[higher geometry]].

## Properties 

The coset inherits the structure of a group if $H$ is a [[normal subgroup]].

Unless $G$ is abelian, considering both left and right coset spaces provide different information. 

The natural projection $G\to G/H$, mapping the element $g$ to the element $g H$, realizes $G$ as an $H$-[[principal bundle]] over $G/H$. We therefore have a [[homotopy pullback]]
$$
  \array{
   G & \to&* 
   \\
    \downarrow && \downarrow
   \\
   G/H &\to& \mathbf{B}H
  }
$$
where $\mathbf{B}H$ is the [[delooping|delooping groupoid]] of $H$.
By the [[pasting law]] for [[homotopy pullbacks]] then we get the [[homotopy pullback]]

$$
  \array{
   G/H & \to&\mathbf{B}H 
   \\
    \downarrow && \downarrow
   \\
   * &\to& \mathbf{B}G
  }
$$

## Examples

### $n$-Spheres

+-- {: .num_example #nSphereAsCosetSpace}
###### Example

The [[n-spheres]] are coset spaces of [[orthogonal groups]]

$$
  S^n \simeq O(n+1)/O(n)
  \,.
$$

For fix a unit vector in $\mathbb{R}^{n+1}$. Then its [[orbit]] under the defining $O(n+1)$-[[action]] on $\mathbb{R}^{n+1}$ is clearly the canonical embedding $S^n \hookrightarrow \mathbb{R}^{n+1}$. But precisely the subgroup of $O(n+1)$ that consists of rotations around the axis formed by that unit vector [[stabilizer group|stabilizes]] it, and that subgroup is isomorphic to $O(n)$, hence $S^n \simeq O(n+1)/O(n)$.

=--

### Sequences of coset spaces
 {#QuotientMapsOfCosetSpaces}

For $K \hookrightarrow H \hookrightarrow G$
two consecutive group inclusions, then there is a [[fiber bundle]] of the form

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

If this is indeed a [[homotopy fiber sequence]], then it induces the corresponding [[long exact sequence of homotopy groups]]

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

Then by example \ref{nSphereAsCosetSpace} we have that $O(n+1)/O(n) \simeq S^n$ is the [[n-sphere]] and hence there is a [[long exact sequence of homotopy groups]] of the form 

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

[[!redirects coset]]
[[!redirects cosets]]
[[!redirects left coset]]
[[!redirects right coset]]
[[!redirects left cosets]]
[[!redirects right cosets]]

[[!redirects coset space]]
[[!redirects coset spaces]]

