
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Differential algebraic K-theory is the [[differential cohomology]]-refinement of [[algebraic K-theory]].

In ([Bunke-Tamme 12](#BunkeTamme12)) this is realized effectively as the [[schreiber:differential cohomology in a cohesive topos]] of the [[tangent (∞,1)-topos]] of the [[cohesive (∞,1)-topos]]

$$
  Sh_\infty\left(SmthMfd, Sh_\infty\left(Sch_{\mathbb{Z}}\right)\right)
  \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  Sh_\infty(Sch_{\mathbb{Z}})
$$

of [[∞-stacks]] on the [[site]] of [[smooth manifolds]] with values in turn in [[∞-stack]] over a [[site]] of [[arithmetic schemes]], hence by [[smooth ∞-groupoids]] but over a [[base (∞,1)-topos]] of algebraic [[∞-stacks]].

It is observed in this context that the [[Beilinson regulator]] in [[algebraic K-theory]] is naturally understood as a [[Chern character]] in this perspective of [[differential cohomology]] ([Bunke-Tamme 12](#BunkeTamme12)), which helps with studying it.

## Definition

There is a refinement of the [[Beilinson regulator]] to a smoothly parameterized version $\mathbf{K}$ of [[algebraic K-theory]].

Differential algebraic K-theory is the [[homotopy pullback]] of that along a suitable inclusion of cycles. ([Bunke-Tamme 13, def. 3.1](#BunkeTamme13))

## Applications

* differential refinement of [[Becker-Gottlieb transfer]] and its image under [[Borel regulators]]. See at _[[transfer index conjecture]]_.

## Related concepts

* [[differential K-theory]]

## References

* [[Ulrich Bunke]], [[Georg Tamme]], _Regulators and cycle maps in higher-dimensional differential algebraic K-theory_ ([arXiv:1209.6451](http://arxiv.org/abs/1209.6451))
 {#BunkeTamme12}

* [[Ulrich Bunke]], [[David Gepner]], _Differential function spectra, the differential Becker-Gottlieb transfer, and applications to differential algebraic K-theory_ ([arXiv:1306.0247](http://arxiv.org/abs/1306.0247))

* [[Ulrich Bunke]], [[Georg Tamme]], _Multiplicative differential algebraic K-theory and applications_ ([arXiv:1311.1421](http://arxiv.org/abs/1311.1421))
 {#BunkeTamme13}

[[!redirects differential algebraic K-theory]]

[[!redirects differential algebraic K-theories]]

[[!redirects differential algebraic K-theories]]