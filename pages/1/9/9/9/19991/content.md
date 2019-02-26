[[!redirects space group]]

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

A **space group** in [[dimension]] $n$, also known as a **crystallographic group**, is a [[subgroup]] of the corresponding [[Euclidean group]], hence of the [[isometry group]] of [[Euclidean space]] $\mathbb{R}^n$, that contains some [[lattice in a vector space|lattice]] in $\mathbb{R}^n$ as a [[subgroup]], and is contained within the [[automorphism group]] of that lattice. In other words, it is a subgroup of the automorphism group of the lattice that contains all the [[translations]] by elements of the lattice itself.

Equivalently, a crystallographic group on a [[Euclidean space]] $E$ is a [[finite group|finite]] [[subgroup]] $S \subset Iso(E)$ of the [[isometry group]] of $E$ (its [[Euclidean group]]) that contains a [[lattice (discrete subgroup)|lattice]] $N \subset E \subset Iso(E)$ of [[translation group|translations]] as a [[normal subgroup]] $N \subset S$. The corresponding [[quotient group]] $G \coloneqq S/N$ is called the _[[point group]]_ of the crystallographic group. 

This situation is reflected in [[short exact sequences]]

$$
  \array{
    & 
    1 && 1
    \\
    & \downarrow && \downarrow
    \\
    {\text{normal subgroup}
    \atop
    \text{lattice of translations}}
    & 
    N &\subset& E
    &
    {\text{translation} \atop \text{group}}
    \\
    &
    \big\downarrow && \big\downarrow 
    \\
    {\text{crystallographic} \atop \text{group}}
    &
    S &\subset& Iso(E)
    &
    {\text{Euclidean}
    \atop
    \text{isometry group}}
    \\
    &
    \big\downarrow && \big\downarrow 
    \\
    {\text{point} \atop \text{group}}
    &
    G &\subset& O(E) 
    &
    {\text{orthogonal} \atop \text{group}}
    \\
    &
    \downarrow && \downarrow
    \\
    &
    1 && 1
  }
$$

If the [[short exact sequence]] on the left [[split exact sequence|splits]], hence if the space group $S \simeq G \ltimes N$ is the [[semidirect product]] of the [[point group]] with the translational lattice, $S$ is called a _symmorphic space group_.

## Properties

### Classification

In 2 [[dimensions]], there are precisely 17 crystallographic groups, which are distinct up to [[isomorphism]]; these are known as the _[[wallpaper groups]]_. In 3 dimensions, there are 219 distinct types, or 230 if chiral copies are considered distinct. The classification of space groups has been carried out up to 6 dimensions.

On the classification of symmorphic space groups see also [this MO comment](https://mathoverflow.net/q/77682/381).

### Compact flat orbifolds
 {#CompactFlatOrbifolds}

+-- {: .num_prop #InducedPointGroupActionOnTorus}
###### Proposition
**(induced point group action on torus)**

The assumption that the crystallographic translation group $N \subset S$ is a [[normal subgroup]]

$$
  1 \to N \longrightarrow S \longrightarrow G \to 1
$$

implies that the [[action]] of the [[point group]] $G = S/N$ descends to the [[torus]] [[quotient space]] $E/N$

$$
  \array{
    E 
      &\overset{g}{\longrightarrow}&
    E
    \\
    \big\downarrow
    &&
    \big\downarrow
    \\
    E/N 
      &\underset{g}{\longrightarrow}& 
    E/N
  }
$$

=--

+-- {: .proof}
###### Proof

By the definition of [[quotient space]], the condition for this to be the case is that for all $x \in E$ we have $g(n(x)) = n'(g(x))$, or equivalently $g(n(g^{-1}(y))) = n'(y)$, which is implied by $N$ being a [[normal subgroup]]: $g N g^{-1} = N$.

=--

+-- {: .num_remark}
###### Remark

The further [[homotopy quotient]] $(E/N)\sslash G$ of the [[torus]] $E/N$ by this induced [[action]] of the [[point group]] $G$ is a [[compact topological space|compact]] [[flat orbifold]], and most compact flat orbifolds arise this way.

=--

## References

* _The Crystallographic Groups_, Pure and Applied Mathematics
Volume 50, 1972, Pages 16-60 (<a href="https://doi.org/10.1016/S0079-8169(08)60959-9">doi:10.1016/S0079-8169(08)60959-9</a>)

* Daniel R. Farkas, _Crystallographic groups and their mathematics_, Rocky Mountain J. Math. Volume 11, Number 4 (1981), 511-552 ([doi:10.1216/RMJ-1981-11-4-511](https://projecteuclid.org/euclid.rmjm/1250128489))

See also

* Groupprops, _[Space group](https://groupprops.subwiki.org/wiki/Space_group)_

* Wikipedia, _[Space group](https://en.wikipedia.org/wiki/Space_group)_

* Wikipedia, _[Point group](https://en.wikipedia.org/wiki/Point_group)_

[[!redirects space groups]]

[[!redirects point group]]
[[!redirects point groups]]

[[!redirects symmorphic space group]]
[[!redirects symmorphic space groups]]

[[!redirects symmorphic crystallographic group]]
[[!redirects symmorphic crystallographic groups]]


[[!redirects crystallographic group]]
[[!redirects crystallographic groups]]
