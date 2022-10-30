

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
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

A _parameterized spectrum_ is a [[bundle]] of [[spectra]] ([May-Sigurdsson 06](#MaySigurdsson06)). Specifically, for $X$ a [[homotopy type]] thought of as  an [[∞-groupoid]], then a spectrum parameterized over $X$ is equivalently an [[(∞,1)-functor]] $X \longrightarrow Spec$ from $X$ to the [[stable (∞,1)-category of spectra]] ([Ando-Blumberg-Gepner 11](#AndoBlumbergGepner11)): this assigns to each [[object]] of $X$ a [[spectrum]], to each [[morphism]] an [[equivalence in an (infinity,1)-category|equivalence]] of spectra, to each [[2-morphism]] a [[homotopy]] between such equivalences, and so forth.

More generally, given an [[(∞,1)-topos]] $\mathbf{H}$, then its [[tangent (∞,1)-topos]] $T\mathbf{H}$ is the [[(∞,1)-category]] of all [[spectrum objects]] in $\mathbf{H}$ parameterized over any object of $\mathbf{H}$ (an observation promoted by [[Joyal]]).

The intrinsic [[cohomology]] of such a [[tangent (∞,1)-topos]] of parameterized spectra is [[twisted generalized cohomology]] in $\mathbf{H}$, and generally is [[twisted bivariant cohomology]] in $\mathbf{H}$.

For more see also at _[[tangent cohesive (∞,1)-topos]]_.

## Properties

### Six operations yoga 
 {#SixOperationsYoga}

For any map $f\colon X\longrightarrow Y $ between [[∞-groupoids]], the parameterized spectra form a [[Wirthmüller context]] version of the [[yoga of six functors]], in that 

$$
  [X,Spectra]
    \stackrel{\overset{f_!}{\longrightarrow}}{\stackrel{\overset{f^\ast}{\longleftarrow}}{\underset{f_\ast}{\longrightarrow}}}
  [Y,Spectra]
$$

in that $f^\ast$ is not only a [[strong monoidal functor]] but also a [[strong closed functor]], hence that [[Frobenius reciprocity]] holds.

Moreover, along ([[cospan|co-]])[[spans]] of morphisms pull-push $(f_!\dashv f^\ast)$ satisfies the [[Beck-Chevalley condition]] ([Hopkins-Lurie 14, prop. 4.3.3](#HopkinsLurie14)).

One way to summarize all this is to say that parameterized spectra over  [[∞Grpd]] constitute a [[linear homotopy type theory]] ([Schreiber 14](#Schreiber14)).

## Applications 

In [[twisted cohomology]].

## Related concepts

* [[sheaf of spectra]]

## References
 {#References}

A comprehensive textbook account on parameterized spectra in [[∞Grpd]] $\simeq$ $L_{whe}$[[Top]] is in

* [[Peter May]], J. Sigurdsson, _[[Parametrized Homotopy Theory]]_, 2006
  {#MaySigurdsson06]

A formulation of aspects of this in [[(∞,1)-category theory]] is in 

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Parametrized spectra, multiplicative Thom spectra, and the twisted Umkehr map_ ([arXiv:1112.2203](http://arxiv.org/abs/1112.2203))
  {#AndoBlumbergGepner11}

See also the further references at _[[(∞,1)-module bundle]]_.

Discussion of the [[Beck-Chevalley condition]] is in prop. 4.3.3 of


* {#HopkinsLurie14} [[Michael Hopkins]], [[Jacob Lurie]], _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_

Discussion as a [[linear homotopy type theory]] is in 

* {#Schreiber14} [[Urs Schreiber]], _[[schreiber:Quantization via Linear homotopy types]]_ ([arXiv:1402.7041](http://arxiv.org/abs/1402.7041))


[[!redirects parametrized spectra]]

[[!redirects parameterized spectrum]]
[[!redirects parameterized spectra]]

[[!redirects spectrum bundle]]
[[!redirects spectrum bundles]]

[[!redirects bundle of spectra]]
[[!redirects bundles of spectra]]