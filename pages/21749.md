
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
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

Let $G$ be a [[finite group]] and $X$ a suitable [[topological G-space]]. Then the _delocalized $G$-equivariant cohomology_ of $X$ ([Connes-Baum 89, p. 165](#ConnesBaum89)) is the [[ordinary cohomology]] of the [[quotient space]] 

$$
  \left(
  \underset{
    h \in G
  }{\sqcup}
  X^{h}
  \right) / G
$$

of the [[disjoint union]] of [[fixed loci]], where the [[action]] of $g \in G$ is by 

$$
  \left(h,\, x \in X^h  \right)
  \;\;
  \overset{g}{\mapsto}
  \;\;
  \left(g^{-1}\cdot h \cdot g ,\, x \cdot g \in X^{g^{-1} h g}  \right)
  \,.
$$

([Connes-Baum 89, over (7.3)](#ConnesBaum89))

## Properties

### Relation to Chen-Ruan cohomology
 {#RelationtoChenRuanCohomology}

The definition of delocalized equivariant cohomology coincides with that of [[Chen-Ruan cohomology]] for the [[global quotient orbifold]] ([[orbispace]]) $X \sslash G$. (Manifestly so, also highlighted in [Bunke-Spitzweck-Schick 06, Section 1.3](#BunkeSpitzweckSchick06))

### Relation to Bredon cohomology

In turn, [[Chen-Ruan cohomology]] of [[global quotient orbifolds]] (and hence, by the [above](#RelationtoChenRuanCohomology) delocalized equivariant cohomology) coincides with [[Bredon cohomology]] with [[coefficients]] in the [[rationalization|rationalized]] [[representation ring]]-functor $G/H \mapsto Rep(H)$ on the [[orbit category]].

### Relation to rationalized equivariant K-theory

In further turn, even-periodic [[Bredon cohomology]] with coefficients in the [[representation ring]]-functor is equivalent to [[rationalization|rationalized]] [[equivariant K-theory]]:

\linebreak

[[!include incarnations of rational equivariant topological K-theory -- table ]]


## Related concepts

* [[equivariant Chern character]]

## References

* {#ConnesBaum89} [[Alain Connes]], [[Paul Baum]], _Chern character for discrete groups_, A Fête of Topology, Papers Dedicated to Itiro Tamura 1988, Pages 163-232 ([doi:10.1016/B978-0-12-480440-1.50015-0](https://doi.org/10.1016/B978-0-12-480440-1.50015-0))

* {#BunkeSpitzweckSchick06} [[Ulrich Bunke]], [[Markus Spitzweck]], [[Thomas Schick]], _Inertia and delocalized twisted cohomology_, Homotopy, Homology and Applications, vol 10(1), pp 129-180 (2008) ([arXiv:math/0609576](https://arxiv.org/abs/math/0609576))


