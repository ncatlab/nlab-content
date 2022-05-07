
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

Given a [[cohesive (∞,1)-topos]] $\mathbf{H}$, then then [[shape modality|shape]] $&#643; X$ of any object $X$ behaves like the [[path ∞-groupoid]] of $X$. For some $\mathbf{H}$ this is true verbatim, in that the shape operation is represented by a geometric [[singular simplicial complex]]

$$
  &#643; X 
  \;\simeq\;
  \underset{\longrightarrow}{\im}_n Maps(\Delta^n, X)
  \,,
$$ 

where on the right we have a [[homotopy colimit]] over [[internal homs]] from a cohesive incarnation of the [[n-simplex]] into $X$.


This is true for instance for the case

* $\mathbf{H} = $ [[Smooth∞Grpd]] 

This is due to ([BEBP](#BEBP), see [Pavlov, theorem 0.2](#Pavlov)). For $X$ a [[stable homotopy type]] in the [[tangent (∞,1)-topos]] $T Smooth\infty Grpd$ this was observed in [Bunke-Nikolaus-Voelkl 13](#BunkeNikolausVoelkl13)

## Related concepts

* [[concordance]]

## References


* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_, Journal of Homotopy and Related Structures October 2014 ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

* {#BEBP} [[Daniel Berwick-Evans]], [[Pedro Boavida de Brito]], [[Dmitri Pavlov]], _Classifying spaces of infinity-sheaves_ ([arXiv:1912.10544](https://arxiv.org/abs/1912.10544))

* {#Pavlov} [[Dmitri Pavlov]], _Structured Brown representability via concordance_ ([pdf](https://dmitripavlov.org/concordance.pdf))

[[!redirects shape via cohesive path infinity-groupoid]]
