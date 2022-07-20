

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
#### Goodwillie calculus
+--{: .hide}
[[!include Goodwillie calculus - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _parameterized spectrum_ is a [[bundle]] of [[spectra]] ([May-Sigurdsson 06](#MaySigurdsson06)), hence a [[stable homotopy type]] in [[parameterized homotopy theory]].

Specifically, for $X$ a [[homotopy type]] thought of as  an [[∞-groupoid]], then a spectrum parameterized over $X$ is equivalently an [[(∞,1)-functor]] $X \longrightarrow Spec$ from $X$ to the [[stable (∞,1)-category of spectra]] ([Ando-Blumberg-Gepner 11](#AndoBlumbergGepner11)): this assigns to each [[object]] of $X$ a [[spectrum]], to each [[morphism]] an [[equivalence in an (infinity,1)-category|equivalence]] of spectra, to each [[2-morphism]] a [[homotopy]] between such equivalences, and so forth.

More generally, given an [[(∞,1)-topos]] $\mathbf{H}$, then its [[tangent (∞,1)-topos]] $T\mathbf{H}$ is the [[(∞,1)-category]] of all [[spectrum objects]] in $\mathbf{H}$ parameterized over any object of $\mathbf{H}$ (see also at *[[Joyal locus]]*).

The intrinsic [[cohomology]] of such a [[tangent (∞,1)-topos]] of parameterized spectra is [[twisted generalized cohomology]] in $\mathbf{H}$, and generally is [[twisted bivariant cohomology]] in $\mathbf{H}$.

For more see also at _[[tangent cohesive (∞,1)-topos]]_.

## Properties

### As (co)module spectra

For $X$ a connected homotopy type, then the $X$-parameterized spectra are equivalently the [[module spectra]] over the [[∞-group ∞-ring]] $\mathbb{S}[\Omega X]$ of the [[∞-group]] corresponding to the [[loop space]].  

To see this, use first that $X$-parameterized spectra are equivalently [[∞-functors]] of [[(∞,1)-categories]] of the form

$$
  B \Omega X \longrightarrow Spectra
$$

from the [[delooping]] [[∞-groupoid]] of $\Omega X$ to the [[(∞,1)-category of spectra]], then use that these are equivalenty Spectrum [[enriched functors]] out of the one-object spectrum enriched $\infty$-category with hom-spectrum $\mathbb{S}[\Omega X] \simeq \Sigma^\infty_+ \Omega X$.

Moreover $\mathbb{S}[\Omega X]$-[[module spectra]] are equivalent to [[comodule spectra]] over the coalgebra $\mathbb{S}[X] = \Sigma^\infty_+ X$ induced from the [[coalgebra object]] structure of $X$ in the [[Cartesian monoidal (∞,1)-category]] [[∞Grpd]] via the [[diagonal]] ([here](cartesian+monoidal+infinity%2C1-category#CoalgebraObjects)), and using that $\Sigma^\infty$ is a [[strong monoidal functor]]:

$$
   CoModSpectra_{\mathbb{S}[X]}
  \;\simeq\;
   ModSpectra_{\mathbb{S}[\Omega X]}
$$


([Hess-Shipley 14, theorem 1.2 with prop. 5.18](#HessShipley14))

See also at _[[A-theory]]_.


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

* [[excisive functor]]

* [[tangent (infinity,1)-category]]

* [[sheaf of spectra]]

* [[rational parameterized stable homotopy theory]]

* [[ex-space]]

* the [[K-theory]] of spectra parameterized over a connected $X$ is the _[[A-theory]]_ of $X$.

* [[twisted differential cohomology]]

## References
 {#References}


Parameterized spectra over a fixed base (in any suitable [[model category]]) are discussed in 

* {#Schwede97} [[Stefan Schwede]], section 3 of _Spectra in model categories and applications to the algebraic cotangent complex_, Journal of Pure and Applied Algebra 120 (1997) 104 ([pdf](http://www.math.uni-bonn.de/people/schwede/modelspec.pdf))

A comprehensive textbook account on parameterized spectra in [[∞Grpd]] $\simeq$ $L_{whe}$[[Top]] is in

* {#MaySigurdsson06} [[Peter May]], J. Sigurdsson, _[[Parametrized Homotopy Theory]]_, 2006
  

A formulation of aspects of this in [[(∞,1)-category theory]] is in 

* {#AndoBlumbergGepner11} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Parametrized spectra, multiplicative Thom spectra, and the twisted Umkehr map_, Geom. Topol. 22 (2018) 3761-3825 ([arXiv:1112.2203](http://arxiv.org/abs/1112.2203))
  
Discussion of convenient [[model category]] [[presentable (infinity,1)-category|presentations]]:

* {#BraunackMayer19} [[Vincent Braunack-Mayer]], _Combinatorial parametrised spectra_, based on the [[schreiber:thesis Braunack-Mayer|PhD thesis]] ([arXiv:1907.08496](https://arxiv.org/abs/1907.08496))

See also the further references at _[[(∞,1)-module bundle]]_.

Discussion of the [[Beck-Chevalley condition]] is in prop. 4.3.3 of

* {#HopkinsLurie14} [[Michael Hopkins]], [[Jacob Lurie]], _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_

Discussion of the Kozul duality between $\mathbb{S}[\Omega X]$-module spectra and $\mathbb{S}[X]$-comodule spectra is in

* {#HessShipley14} [[Kathryn Hess]], [[Brooke Shipley]], _Waldhausen K-theory of spaces via comodules_, Advances in Mathematics 290 (2016): 1079-1137 ([arXiv:1402.4719](https://arxiv.org/abs/1402.4719))


Discussion as a [[linear homotopy type theory]] is in 

* {#Schreiber14} [[Urs Schreiber]], _[[schreiber:Quantization via Linear homotopy types]]_ ([arXiv:1402.7041](http://arxiv.org/abs/1402.7041))


[[!redirects parametrized spectra]]

[[!redirects parameterized spectrum]]
[[!redirects parameterized spectra]]

[[!redirects parametrised spectrum]]
[[!redirects parametrised spectra]]


[[!redirects spectrum bundle]]
[[!redirects spectrum bundles]]

[[!redirects bundle of spectra]]
[[!redirects bundles of spectra]]