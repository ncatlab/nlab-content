
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

If the $G$-representation $V$ is 1-dimensional over the given [[ground field]] $k$, [[stereographic projection]] identifies the [[representation sphere]] of $V$ with the [[projective G-space]] of $V \oplus \mathbf{1}$:

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

(e.g. [Atiyah 68, Sec. 4](#Atiyah68), [Greenlees 01, 9.1](#Greenlees01))

## Related concepts

* [[tautological equivariant line bundle]]

## References

Discussion in the context of [[Bott periodicity]] in [[equivariant K-theory]]:

* {#Atiyah68} [[Michael Atiyah]], _Bott periodicity and the index of elliptic operators_, The Quarterly Journal of Mathematics, Volume 19, Issue 1, 1968, Pages 113–140 ([doi:10.1093/qmath/19.1.113](https://doi.org/10.1093/qmath/19.1.113))

Discussion in the context of [[equivariant complex oriented cohomology theory]]:

* {#Greenlees01} [[John Greenlees]], Section 9.A of _Equivariant formal group laws and complex oriented cohomology theories_, Homology Homotopy Appl. Volume 3, Number 2 (2001), 225-263 ([euclid:hha/1139840255](https://projecteuclid.org/euclid.hha/1139840255))

[[!redirects projective G-spaces]]

