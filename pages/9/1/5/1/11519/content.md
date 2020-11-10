
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
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

Consider the [[unit sphere]] $S(\mathbb{R}\oplus V)$ where $\mathbb{R}$ carries the [[trivial representation]]. Then the [[stereographic projection]] homeomorphism

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

(e.g. [MP 04, p. 2](#MP04))

Similarly, if $V$ is 1-dimensional over the given [[ground field]] $k$, [[stereographic projection]] identifies the [[representation sphere]] of $V$ with the [[projective G-space]] of $V \oplus \mathbf{1}$:

$$
  \array{
    V^{cpt}
    &
      \longrightarrow
    &
    k P
   \big(
     V \oplus \mathbf{1}
   \big)
    \\
    v &\mapsto&
    \left\{
    \array{
      [v,1] &\vert& v \in V
      \\
      [1,0] &\vert& v = \infty
    }
    \right.
  }
$$

(e.g. [Atiyah 68, Sec. 4](projective+G-space#Atiyah68), [Greenlees 01, 9.1](projective+G-space#Greenlees01))

### $G$-CW-Complex structure

+-- {: .num_prop #RepresentationSpheresAreGCWComplexes}
###### Proposition
**([[G-representation spheres are G-CW-complexes]])**

For $G$ a [[compact Lie group]] (e.g. a [[finite group]]) and $V \in RO(G)$ a [[finite dimensional vector space|finite-dimensional]] [[orthogonal group|orthogonal]] $G$-[[linear representation]], the [[representation sphere]] $S^V$ admits the structure of a [[G-CW-complex]].

=--

+-- {: .proof}
###### Proof

Observe that we  have a $G$-equivariant [[homeomorphism]] between the representation sphere of $V$ and the [[unit sphere]] in $\mathbb{R} \oplus V$, where $\mathbb{R}$ is the 1-dimensional [[trivial representation]]  (Prop. \ref{RepresentationSpheresAsUnitSpheres})

\[
  \label{RepresentationSphereAsUnitSphere}
  S^V \;\simeq\; S(\mathbb{R} \oplus V)
  \,.
\]

It is thus sufficient to show that unit spheres in orthogonal representations admit G-CW-complex structure. 

This in turn follows as soon as there is a $G$-equivariant [[triangulation]] of $S(\mathbb{R}\oplus V)$, hence a [[triangulation]] with the property that the $G$-[[action]] restricts to a [[bijection]] on its sets of $k$-dimensional cells, for each $k$. Because then if $G/H$ is an [[orbit]] of this $G$-action on the set of $k$-cells, we have a cell $G/H \times D^k$ of an induced [[G-CW-complex]].

Since the unit spheres in (eq:RepresentationSphereAsUnitSphere) are [[smooth manifolds]] with [[smooth function|smooth]] $G$-[[action]], the existence of such $G$-[[equivariant triangulations]] follows for general [[compact Lie groups]] $G$ from the _[[equivariant triangulation theorem]]_ ([Illman 83](#Illman83)).

More explicitly, in the case that $G$ is a [[finite group]] such an equivariant triangulation may be constructed as follows:

Let $\{b_1, b_2, \cdots, b_{n+1}\}$ be an [[orthonormal basis]] of $\mathbb{R} \oplus V$. Take then as [[vertices]] of the triangulation all the distinct points $\pm g(b_i) \in \mathbb{R} \oplus V$, and as [[edges]] the [[geodesics]] (great circle segments) between nearest neighbours of these points, etc.

=--


## References

* {#Blumberg17} [[Andrew Blumberg]], Example 1.1.5 of _Equivariant homotopy theory_, 2017 ([pdf](https://www.ma.utexas.edu/users/a.debray/lecture_notes/m392c_EHT_notes.pdf), [GitHub](https://github.com/adebray/equivariant_homotopy_theory))

* {#MP04} Waclaw Marzantowicz, Carlos Prieto, _The unstable equivariant fixed point index and the equivariant degree_, Jourmal of the London Mathematical Society,  Volume 69, Issue 1 February 2004 , pp. 214-230 ([pdf](http://hopf.math.purdue.edu/Marzantowicz-Prieto/Marprieto.pdf), <a href=" https://doi.org/10.1112/S0024610703004721">doi:10.1112/S0024610703004721</a>)



[[!redirects representation spheres]]

[[!redirects G-representation sphere]]
[[!redirects G-representation spheres]]

