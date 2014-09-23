
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

This construction subsumes various other construction in [[algebraic K-theory]]. Specifically when restricted to 1-categories it reproduces the classical construction by ([Segal 74](#Segal74)) described at _[[K-theory of a permutative category]]_, see [below](#RelationToClassicalAlgebraicKTheory).

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
Also, instead of just group-completing one may "ring complete" to produce K-theory spectra equipped with the structure of [[E-∞ rings]] ([Bunke-Tamme 13, section 2.4](#BunkeTamme13)).

## Properties

### Relation to classical algebraic K-theory
 {#RelationToClassicalAlgebraicKTheory}

For $R$ a [[commutative ring]], and $R$[[Mod]] its [[category of modules]] ([[projective modules]]), then $\mathcal{K}(R Mod)$ is Quillen's [[algebraic K-theory]] of $R$.
More generally this reproduces the [[K-theory of a permutative category]] etc. ([Nikolaus 13, section 6](#Nikolaus13)).

In particular, applied to the [[stack]] of [[algebraic vector bundles]] this produces the [[sheaf of spectra]] of [[algebraic K-theory]] of [[schemes]] ([Bunke-Tamme 12, section 3.3](#BunkeTamme12)), see at  _[differential algebraic K-theory -- Algebraic K-theory sheaf of spectra](differential+algebraic+K-theory#AlgebraicKTheorySheafOfSpectra)_. 

## Examples

### On monoidal stacks

Algebraic K-theory is traditionally applied to single [[symmetric monoidal (∞,1)-categories|symmetric monoidal]]/[[stable (∞,1)-category|stable]] [[(∞,1)-categories]], but to the extent that it is [[(∞,1)-functor|functorial]] it may just as well be applied to [[(∞,1)-sheaves]] with values in these.

Notably, applied to the monoidal [[stack]] of [[vector bundles]] (with [[connection on a bundle|connection]]) on the [[site]] of [[smooth manifolds]], the [[K-theory of a symmetric monoidal (∞,1)-category|K-theory of a monoidal category]]-functor produces a [[sheaf of spectra]] which is a form of [[differential K-theory]] and whose [[geometric realization]] is the [[topological K-theory]] spectrum. For more on this see at _[differential cohomology hexagon -- Differential K-theory](differential%20cohomology%20diagram#DifferentialKTheory)_.



## Related concepts

* [[regulator in algebraic K-theory]]

* [[K-theory of a permutative category]], [[K-theory of a bipermutative category]]

## References

### Traditional category theoretic

The functor from [[symmetric monoidal categories]] to [[connective spectra]] was originally given in

* {#Segal74} [[Graeme Segal]], _Categories and cohomology theories_, Topology 13 (1974), 293&#8211;312.

See also

* {#Thomason82} [[Robert Thomason]], _First quadrant spectral sequences in algebraic K-theory via homotopy colimits_. Comm. Algebra, 10(15):1589&#8211;1668, 
1982.

The following article showed that this construction produces all [[connective spectra]], up to equivalence

* {#Thomason95} [[Robert Thomason]], Symmetric monoidal categories model all connective spectra, Theory Appl. Categ. 1 (1995), no. 5, 78&#8211;118.

and a new proof of that is in 

* [[Michael Mandell]], _An Inverse K-Theory Functor_ ([arXiv:1002.3622](http://arxiv.org/abs/1002.3622))

### $\infty$-Category theoretic

The natural generalization of the construction to [[symmetric monoidal (∞,1)-categories]] appears in

* {#BunkeTamme12} [[Ulrich Bunke]], [[Georg Tamme]], section 2.1 of _Regulators and cycle maps in higher-dimensional differential algebraic K-theory_ ([arXiv:1209.6451](http://arxiv.org/abs/1209.6451))

* {#Nikolaus13} [[Thomas Nikolaus]] _Algebraic K-Theory of $\infty$-Operads_ ([arXiv:1303.2198](http://arxiv.org/abs/1303.2198))

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], def. 6.1 in  _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

* {#GepnerGrothNikolaus13} [[David Gepner]], [[Moritz Groth]], [[Thomas Nikolaus]], _Universality of multiplicative infinite loop space machines_, [arXiv:1305.4550](http://arxiv.org/abs/1305.4550).

* {#BunkeTamme13} [[Ulrich Bunke]], [[Georg Tamme]], _Multiplicative differential algebraic K-theory and applications_ ([arXiv:1311.1421](http://arxiv.org/abs/1311.1421))

[[!redirects algebraic K-theory of symmetric monoidal (∞,1)-categories]]


[[!redirects K-theory of symmetric monoidal (∞,1)-categories]]

[[!redirects algebraic K-theory of a symmetric monoidal (∞,1)-category]]
[[!redirects algebraic K-theory of a symmetric monoidal (∞,1)-categories]]

[[!redirects K-theory of a symmetric monoidal (infinity,1)-category]]
[[!redirects K-theory of a symmetric monoidal (infinity,1)-categories]]


[[!redirects algebraic K-theory of a symmetric monoidal (infinity,1)-category]]
[[!redirects algebraic K-theory of a symmetric monoidal (infinity,1)-categories]]

