
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_prop #RepresentationSpheresAreGCWComplexes}
###### Proposition
**(G-representation spheres are G-CW-complexes)**

For $G$ a [[compact Lie group]] (e.g. a [[finite group]]) and $V \in RO(G)$ a [[finite dimensional vector space|finite-dimensional]] [[orthogonal group|orthogonal]] $G$-[[linear representation]], the [[representation sphere]] $S^V$ admits the structure of a [[G-CW-complex]].

=--

+-- {: .proof}
###### Proof

Observe that we  have a $G$-equivariant [[homeomorphism]] between the representation sphere of $V$ and the [[unit sphere]] in $\mathbb{R} \oplus V$, where $\mathbb{R}$ is the 1-dimensional [[trivial representation]] 

$$ 
  S^V \;\simeq\; S(\mathbb{R} \oplus V)
  \,.
$$

It is thus sufficient to show that unit spheres in orthogonal representations admit G-CW-complex structure. 

This in turn follows as soon as there is a $G$-equivariant [[triangulation]] of $S(\mathbb{R}\oplus V)$, hence a [[triangulation]] with the property that the $G$-[[action]] restricts to a [[bijection]] on its sets of $k$-dimensional cells, for each $k$. Because then if $G/H$ is an [[orbit]] of this $G$-action on the set of $k$-cells, we have a cell $G/H \times D^k$ of an induced [[G-CW-complex]].

The existence of such $G$-[[equivariant triangulations]] follows for general [[compact Lie groups]] $G$ from the _[[equivariant triangulation theorem]]_ ([Illman 83](#Illman83)).

More explicitly, in the case that $G$ is a [[finite group]] such an equivariant triangulation may be constructed as follows:

Let $\{b_1, b_2, \cdots, b_{n+1}\}$ be an [[orthonormal basis]] of $\mathbb{R} \oplus V$. Take then as [[vertices]] of the triangulation all the distinct points $\pm g(b_i) \in \mathbb{R} \oplus V$, and as [[edges]] the [[geodesics]] (great circle segments) between nearest neighbours of these points, etc.

=--

## Examples

(...)

## References

* {#Illman78} [[Sören Illman]], _Smooth equivariant triangulations ofG-manifolds for $G$ a finite group_, Math. Ann. (1978) 233: 199 ([doi:10.1007/BF01405351](https://doi.org/10.1007/BF01405351))

* {#Illman83} [[Sören Illman]], _The Equivariant Triangulation Theorem for Actions of Compact Lie Groups_, Mathematische Annalen (1983) Volume: 262, page 487-502 ([dml:163720](https://eudml.org/doc/163720))

[[!redirects representation spheres are G-CW-complexes]]
