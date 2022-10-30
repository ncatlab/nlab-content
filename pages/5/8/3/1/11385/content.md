[[!redirects power operations]]

> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Power operations are [[cohomology operations]] in [[multiplicative cohomology theory]] which are higher-degree analogs of [[cup products]]-squares [[symmetric algebra|symmetrized]] in the right [[homotopy theory|homotopy-theoretic sense]].

For $E$ an [[E-∞ ring]] and $X$ a [[topological space]] ([[∞-groupoid]], [[homotopy type]]), then a map $a\;\colon\;X \to E$ is a [[cocycle]] in the [[cohomology]] of $X$ with [[coefficients]] in $E$. 

The $n$-th [[cup product]] power of this $a$ is the composite

$$
  a^n \;\colon\; X^{\times n} \stackrel{(a,\cdots,a)}{\longrightarrow} E^{\times n} \stackrel{\mu}{\longrightarrow} E
  \,,
$$

where the second map is the product operation in $E$. Since this is by assumption commutative up to coherent higher homotopy, this map factors through the [[homotopy quotient]] by the [[∞-action]] of the [[symmetric group]] $\Sigma_n$

$$
  a^n \;\colon\; X \times \ast //\Sigma_n \simeq   X^n//\Sigma_n \longrightarrow E
  \,.
$$

The cohomology class of this $E$-cocycle on $X \times B \Sigma_n$ is the $n$-th (symmetric) power of $a$.





## Examples

* on [[ordinary cohomology]] over a [[topological space]], the power operations are the [[Steenrod operations]];

  Specifically for $n = 2$ and $E = H \mathbb{Z}_2$ then the second (symmetric) power of $a \in H(X,\mathbb{Z}_2)$ is an element in $H^\bullet(\mathbb{R}P^\infty \times X, \mathbb{Z}_2) \simeq H^bullet(X,\mathbb{Z}_2)[x]$ and the [[coefficients]] of this [[polynomial]] in $x$ are the [[Steenrod operations]] on $a$.

* on an [[infinite loop space]] they are the Kudo-Araki-Dyer-Lashof operations

* in the context of  [[complex K-theory]] they are the [[Adams operations]]

## Related concepts

* [[Adams operation]]

* [[logarithmic cohomology operation]]

## References

The basic idea is nicely described in 

* [[Charles Rezk]], [MO comment](http://mathoverflow.net/a/6384/381) Nov 09

(from which some of the above text is adapted).

A more technical survey is in 

* [[Charles Rezk]], _Power operations in Morava E-theory --  a survey_ (2009) ([pdf](http://www.math.uiuc.edu/~rezk/midwest-2009-power-ops.pdf))

The original articles are

* {#Rezk06} [[Charles Rezk]], _The units of a ring spectrum and a logarithmic cohomology operation_, J. Amer. Math. Soc. 19 (2006), 969-1014 ([arXiv:math/0407022](http://arxiv.org/abs/math/0407022))

* [[Charles Rezk]], _Power operations for Morava E-theory of height 2 at the prime 2_ ([arXiv:0812.1320](http://arxiv.org/abs/0812.1320))

* [[Charles Rezk]], _The congruence criterion for power operations in Morava E-theory_ ([arXiv:0902.2499](http://arxiv.org/abs/0902.2499))
