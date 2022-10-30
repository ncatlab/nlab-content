
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

The _[[algebraic K-theory]]_ $\mathcal{K}(\mathcal{C})$ of a _[[symmetric monoidal (∞,1)-category]]_ $\mathcal{C}$ is the [[generalized (Eilenberg-Steenrod) cohomology theory]] [[Brown representability theorem|represented]] by the [[∞-group completion]] of the [[commutative ∞-monoid]] which is the [[core]] of $\mathcal{C}$.

This construction subsumes various other construction in [[algebraic K-theory]].

## Definition

Write

$$
  \mathcal{K} \;\colon\;  CMon_\infty(\infty Cat) \stackrel{CMon_\infty(core)}{\longrightarrow} CMon_\infty(\infty Gpd) \stackrel{F}{\longrightarrow} AbGrp_\infty(\infty Grpd) \hookrightarrow  Spectra
$$

the composite of

1. the [[core]] functor from [[symmetric monoidal (∞,1)-categories]] to [[E-∞ spaces]];

1. their [[∞-group completion]] to [[abelian ∞-groups]];

1. the inclusion of "[[abelian ∞-groups]]", hence [[connective spectra]] into all [[spectra]]. 

This $\mathcal{K}$ is the _algebraic K-theory of symmetric monoidal (∞,1)-categories_. ([Nikolaus 13, below remark 5.3](#Nikolaus13), [Bunke-Nikolaus-V&#246;lkl 13, def.6.1](#BunkeNikolausVoelkl13))

More generally, one may start with construction with other objects that map to [[Picard ∞-groups]], such as [[(∞,1)-operads]] ([Nikolaus 13](#Nikolaus13)).

## Properties

### Relation to algebraic K-theory

For $R$ a [[commutative ring]], and $R$[[Mod]] its [[category of modules]](projective modules), then $\mathcal{K}(R Mod)$ is Quillen's [[algebraic K-theory]] of $R$.
More generally this reproduces the [[K-theory of a permutative category]] etc. ([Nikolaus 13, section 6](#Nikolaus13)).


## Related concepts

* [[regulator in algebraic K-theory]]

## References

* {#Thomason82} [[Robert Thomason]], _First quadrant spectral sequences in algebraic K-theory via homotopy colimits_. Comm. Algebra, 10(15):1589&#8211;1668, 1982.

* {#BunkeTamme12} [[Ulrich Bunke]], [[Georg Tamme]], section 2.1 of _Regulators and cycle maps in higher-dimensional differential algebraic K-theory_ ([arXiv:1209.6451](http://arxiv.org/abs/1209.6451))

* {#Nikolaus13} [[Thomas Nikolaus]] _Algebraic K-Theory of $\infty$-Operads_ ([arXiv:1303.2198](http://arxiv.org/abs/1303.2198))

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], def. 6.1 in  _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

[[!redirects algebraic K-theory of symmetric monoidal (∞,1)-categories]]


[[!redirects K-theory of symmetric monoidal (∞,1)-categories]]

[[!redirects algebraic K-theory of a symmetric monoidal (∞,1)-category]]
[[!redirects algebraic K-theory of a symmetric monoidal (∞,1)-categories]]

[[!redirects algebraic K-theory of a symmetric monoidal (infinity,1)-category]]
[[!redirects algebraic K-theory of a symmetric monoidal (infinity,1)-categories]]