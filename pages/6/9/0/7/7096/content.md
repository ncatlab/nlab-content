
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The first of the [[Chern classes]]. The unique [[characteristic class]] of [[circle bundles]] / complex [[line bundles]].

## Definition

### In bare homotopy-type theory

As a [[universal characteristic class]], the first Chern class is the 
[[weak homotopy equivalence]]


$$
  c_1 : B U(1) \stackrel{\simeq}{\to} K(\mathbb{Z},2)
  \,.
$$


### In complex analytic geometry
 {#InComplexAnalyticGeometry}

In [[complex analytic geometry]] consider the [[exponential exact sequence]]

$$
  \mathbb{Z}\to \mathbb{G}\to \mathbb{G}^\times
  \,.
$$

For any [[complex analytic space]] $X$ this induces the [[long exact sequence in cohomology]] with [[connecting homomorphism]]

$$
  c_1\;\colon\;H^1(X,\mathbb{G}^\times ) \longrightarrow H^2(X,\mathbb{Z})
  \,.
$$

This is the first Chern-class map. It sends a [[holomorphic line bundle]] ($H^1(X,\mathbb{G}^\times)$ is the [[Picard group]] of $X$) to an integral cohomology class.

If $D$ is a [[divisor]] in $X$, then $c_1(\mathcal{O}_X(D))$ is the [[Poincaré duality|Poincaré dual]] of the [[fundamental class]] of $D$ (e.g. [Huybrechts 04, prop. 4.4.13](#Huybrechts04)).

Over a [[Riemann surface]] $\Sigma$ the evaluation of the Chern class $c_1(L)$ of a [[holomorphic line bundle]] $L$ on a [[fundamental class]] is the [[degree of a coherent sheaf|degree]] of $L$:

$$
  deg(L) = \langle c_1(L), X\rangle \in H^2(\Sigma, \mathbb{Z}) \simeq \mathbb{Z}
  \,.
$$

## Related concepts

* [[Chern class]], [[top Chern class]]

* [[Dixmier-Douady class]]

* [[complex oriented cohomology]]

## References

See the references at _[[Chern class]]_ and _[[characteristic class]]_.

In [[complex geometry]]

* {#Huybrechts04} [[Daniel Huybrechts]], _Complex geometry - an introduction_. Springer (2004). Universitext. 309 pages. ([pdf](http://www.math.uh.edu/~shanyuji/2012/Geometry/Huybrechts.pdf))

[[!redirects first Chern classes]]
