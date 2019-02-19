
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

## Idea

Given a linear [[representation]] of a [[group]] ([[topological group]]) $G$ in a [[vector space]]/[[Cartesian space]] $\mathbb{R}^n$, then the corresponding _representation sphere_ is the [[one-point compactification]] of this $\mathbb{R}^n$ (the $n$-[[sphere]]) regarded as a [[G-space]].

Representation spheres induce the [[looping and delooping]] which is used in 
[[RO(G)-grading|RO(G)-graded]] [[equivariant cohomology]] theory, [[Brown representability theorem|represented]] by [[genuine G-spectra]] in [[equivariant stable homotopy theory]].

## Properties


### Equivariant stereographic projection
 {#Construction}


+-- {: .num_prop #RepresentationSpheresAsUnitSpheres}
###### Proposition
**([[representation spheres]] of $V$ are [[unit spheres]] in $\mathbb{R} \oplus V$)**

Let $G$ be a [[finite group]] and $V \in RO(G)$ a [[finite dimensional vector space|finite-dimensional]] [[linear representation]] of $G$.

Conside the [[unit sphere]] $S(\mathbb{R}\oplus V)$ where $\mathbb{R}$ carries the [[trivial representation]]. Then the [[stereographic projection]] homeomorphism

$$
  S(\mathbb{R}\oplus V)\setminus \{(1,\mathbf{0})\}
  \stackrel{\simeq}{\longrightarrow} 
  V
$$ 

is manifestly $G$-equivariant, with its inverse exhibiting $S(\mathbb{R}\oplus V)$ as the [[one-point compactification]] of $V$, hence

$$
  S^V \simeq_G S(\mathbb{R}\oplus V)
  \,.
$$

This also shows that $S^V$ is a [[smooth manifold]] with smooth $G$-[[action]].

=--

### $G$-CW-Complex structure

+-- {: .num_prop #RepresentationSpheresAreGCWComplexes}
###### Proposition
**([[G-representation spheres]] are [[G-CW-complexes]])**

For $G$ a [[compact Lie group]] (e.g. a [[finite group]]) and $V \in RO(G)$ a [[finite dimensional vector space|finite-dimensional]] [[orthogonal representation|orthogonal]] $G$-[[linear representation]], the [[representation sphere]] $S^V$ admits the structure of a [[G-CW-complex]].

=--

Proof idea: By Prop. \ref{RepresentationSpheresAsUnitSpheres} we may realize $S^V$ as the unit sphere $S(\mathbb{R} \oplus V)$. Consider then the [[convex hull]] of all the points $\pm g(b_i) \in \mathbb{R} \oplus V$, for $g \in G$ and $\{b_1, b_2, \cdots, b_{n+1}\}$ a [[linear basis]] of $\mathbb{R} \oplus V$. This induces an equivariant triangulation of $S(\mathbb{R} \oplus V)$, whose cells constitute the required [[G-CW-complex]] structure.

The argument in the larger generality of $G$ a [[compact Lie group]]: e.g. proof of Prop. B.43 in [this](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/3AF92C4A288F9A831EEBEC8C1C8CC661/9781108425810apx2_735-792.pdf/equivariant_spaces.pdf)



## References

* {#Blumberg17} [[Andrew Blumberg]], Example 1.1.5 of _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))


[[!redirects representation spheres]]

[[!redirects G-representation sphere]]
[[!redirects G-representation spheres]]

