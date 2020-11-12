
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
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

A projective $G$-space is a [[projective space|projective]] [[topological G-space]].

## Definition

Let $G$ be a [[finite group]] (or maybe a [[compact Lie group]]) and let $V$ be a $G$-[[linear representation]] over some [[topological field|topological]] [[ground field]] $k$.

Then the corresponding _projective $G$-space_ is the [[quotient space]] of the [[complement]] of the origin in (the [[Euclidean space]] underlying) $V$ by the given [[action]] of the [[group of units]] of $k$ (from the $k$-[[vector space]]-[[mathematical structure|structure]] on $V$):

$$
  k P(V)
  \;:=\;
  \big(
    V \setminus \{0\}
  \big) / k^\times
$$

and equipped with the residual $G$-[[action]] on $V$ (which passes to the [[quotient space]] since it commutes with the $k$-action, by linearity).

## Examples

### Ordinary projective spaces

If $G = 1$ is the [[trivial group]], then

$$
  k P(k^{n+1})
  \;=\;
  k P^n
$$

is ordinary (non-equivariant) [[projective space]] of [[dimension]] $n$ over $k$.

### Representation spheres

+-- {: .num_prop #OneDimensionalRepresentationSpheresAsProjectiveLine}
###### Proposition
**(1-dimensional [[representation spheres]] are [[projective G-spaces]])**

If $\mathbf{1}_V \,\in\, G Representations_k$ is 1-dimensional over the given [[ground field]] $k$, [[stereographic projection]] identifies the [[representation sphere]] of $V$ with the [[projective G-space]] over $k$ of $\mathbf{1}_V \oplus \mathbf{1}$:

$$
  \array{
    V^{cpt}
    &
      \longrightarrow
    &
    k P
   \big(
     \mathbf{1}_V \oplus \mathbf{1}
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

=--

(e.g. [Atiyah 68, Sec. 4](#Atiyah68), [Greenlees 01, 9.C](#Greenlees01))

Prop. \ref{OneDimensionalRepresentationSpheresAsProjectiveLine} underlies the concept of [[equivariant complex oriented cohomology theory]].

### Infinite projective space



+-- {: .num_defn #InfiniteProjectiveGSpace}
###### Definition
**([[infinite complex projective G-space]])**

For $G$ an [[abelian group|abelian]] [[compact Lie group]], let 

\[
  \label{GUniverseForInfiniteComplexProjectiveSpace}
  \mathcal{U}_G
  \;\coloneqq\;
  \underset{k \in \mathbb{N}}{\bigoplus}
  \underset{\mathbf{1}_V \in R(G)}{\bigoplus}
  \mathbf{1}_V
\]

be the [[G-universe]] being the infinite [[direct sum]] of all [[complex numbers|complex]] 1-[[dimension|dimensional]] [[linear representations]] of $G$, regarded as a [[topological G-space]] with [[topological space|toplogy]] the [[colimit]] of its [[finite dimensional vector space|finite-dimensional]] [[linear subspaces]].


Then the _[[infinite complex projective G-space]]_ is the [[colimit]]

$$
  P\big( 
    \mathcal{U}_G
  \big)
  \;\coloneqq\;
  \underset{
    \underset{
      {
        V \subset \mathcal{U}_G
      }
      \atop
      {
         dim(V) \lt \infty
      }
    }{\longrightarrow}
  }{\lim}
  P\big( V \big)
$$

of the [[projective G-spaces]] for all the [[finite dimensional vector space|finite-dimensional]] $G$-[[linear representations]] inside the [[G-universe]] (eq:GUniverseForInfiniteComplexProjectiveSpace).

=--

(e.g. [Greenlees 01, Sec. 9.2](#Greenlees01))

## Properties

### Equivariant complex K-theory


+-- {: .num_prop #EquivariantKTheoryOfProjectiveGSpace} 
###### Proposition
**([[equivariant K-theory of projective G-space]])**

For $G$ an [[abelian group]] [[compact Lie group]], let 

$$
  \underset{i}{\oplus}
  \,
  \mathbf{1}_{V_i}
  \;\;
  \in
  \;\;
  G Representations_{\mathbb{C}}^{fin}
$$

be a [[finite dimensional vector space|finite-dimensional]] [[direct sum]] of [[complex numbers|complex]] 1-[[dimension|dimensional]] [[linear representations]].


The $G$-[[equivariant K-theory]] [[cohomology ring|ring]] $K_G(-)$ of the corresponding [[projective G-space]] $P(-)$ is the following [[quotient ring]] of the [[polynomial ring]] in one [[variable]] $L$ over the complex [[representation ring]] $R(G)$ of $G$:

$$
  K_G
  \Big(
    P
    \big(
      \underset{i}{\oplus}
      \,
      \mathbf{1}_{V_i}
    \big)
  \Big)
  \;\;
    \simeq
  \;\;
  R(G)
  \big[
    L
  \big]
  \big/
  \underset{i}{\prod}
  \big(
    1 - 1_{{}_{V_i}} L
  \big)
  \,,
$$

where

* $L \,=\, \big[ \mathcal{L}_{ \underset{i}{\oplus} \mathbf{1}_{V_i} }\big]$ is the K-theory class of the [[tautological equivariant line bundle]] on the given [[projective G-space]]

* $ 1_{{}_{V_i}}  L \;=\; \big[  \mathbf{1}_{V_i} \boxtimes \mathcal{L}_{ \underset{i}{\oplus} \mathbf{1}_{V_i} } \big]$ is the class of its [[external tensor product]] of [[equivariant vector bundles]] with the given [[linear representation]].

=--

([Greenlees 01, p. 248 (24 of 39)](#Greenlees01))
 
## Related concepts

* [[tautological equivariant line bundle]]

## References

Discussion in the context of [[Bott periodicity]] in [[equivariant K-theory]]:

* {#Atiyah68} [[Michael Atiyah]], _Bott periodicity and the index of elliptic operators_, The Quarterly Journal of Mathematics, Volume 19, Issue 1, 1968, Pages 113–140 ([doi:10.1093/qmath/19.1.113](https://doi.org/10.1093/qmath/19.1.113))

Discussion in the context of [[equivariant complex oriented cohomology theory]]:

* {#Greenlees01} [[John Greenlees]], Section 9.A of _Equivariant formal group laws and complex oriented cohomology theories_, Homology Homotopy Appl. Volume 3, Number 2 (2001), 225-263 ([euclid:hha/1139840255](https://projecteuclid.org/euclid.hha/1139840255))

[[!redirects projective G-spaces]]

