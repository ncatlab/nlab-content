
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

* If $G = 1$ is the [[trivial group]], then

  $$
    k P(k^{n+1})
    \;=\;
    k P^n
  $$

  is ordinary (non-equivariant) [[projective space]] of [[dimension]] $n$ over $k$.

## Related concepts

* [[tautological equivariant line bundle]]

## References

Discussion in the context of [[equivariant complex oriented cohomology theory]]:

* {#Greenlees01} [[John Greenlees]], Section 9.A of _Equivariant formal group laws and complex oriented cohomology theories_, Homology Homotopy Appl. Volume 3, Number 2 (2001), 225-263 ([euclid:hha/1139840255](https://projecteuclid.org/euclid.hha/1139840255))

[[!redirects projective G-spaces]]

