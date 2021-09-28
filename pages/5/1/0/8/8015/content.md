
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[stabilization]] of an [[(∞,1)-topos]] $\mathbf{H}$ 

$$
  (\Sigma^\infty \dashv \Omega^\infty) : 
  \mathbf{H}
   \stackrel{\overset{\Omega^\infty}{\leftarrow}}{\underset{\Sigma^\infty}{\to}}
  Stab(\mathbf{H})
$$

consist of [[spectrum objects]] in $\mathbf{H}$. By the "[stable Giraud theorem](http://ncatlab.org/nlab/show/stable+%28infinity%2C1%29-category#StabGiraud)" this is the [[localization of an (∞,1)-category|localization]] of an [[(∞,1)-category of (∞,1)-functors]] with values in the [[stable (∞,1)-category of spectra]]: $\infty$-sheaves of 
spectra.

This may be [[presentable (infinity,1)-category|presented]] by a [[model structure on presheaves of spectra]].

## Properties

### Relation to sheaves of chain complexes and abelian sheaf cohomology

The [[stable Dold-Kan correspondence]]

$$
  DK \;\colon\; Ch_\bullet(R) \stackrel{\simeq}{\longrightarrow} H R Mod(Spectra) \stackrel{U}{\longrightarrow} Spectra
$$

is an [[(∞,1)-limits]]-preserving [[(∞,1)-functor]] from the [[(∞,1)-category of chain complexes]] (over a given [[commutative ring]]) to the [[(∞,1)-category of spectra]]. Hence every [[(∞,1)-sheaf]]/[[∞-stack]] of chain complexes (as it appears (maybe implicitly) in [[abelian sheaf cohomology]]/[[hypercohomology]] canonically incarnates as an $(\infty,1)$-sheaf of spectra).

### Symmetric monoidal structure

The [[smash product|smash]] [[tensor product]] of the [[symmetric monoidal (∞,1)-category of spectra]] induced also a smash tensor product on any [[(∞,1)-category]] of sheaves of spectra

([[Spectral Schemes|Lurie, "Spectral Schemes", prop 1.5]]).

## Examples

* [[generalized étale cohomology]]

* [[tangent cohesion]]

  * [[smooth spectrum]]

  * [[differential cohomology]], 

* [[differential algebraic K-theory]]


## Related concepts

* [[sheaf of L-∞ algebras]]

* [[parameterized spectrum]]



## References

### General

The [[homotopy categories]] of sheaves of [[combinatorial spectra]] were discussed in  

* {#Brown73} [[Kenneth Brown]], part II of _[[Abstract homotopy theory and generalized sheaf cohomology]]_ (1973)

A [[model category]] structure of presheaves of spectra akin to the [[model structure on simplicial presheaves]] is discussed in 

* [[Rick Jardine]], _Stable homotopy theory of simplicial presheaves_, Canad. J. Math. 39(1987), 733-747 ([pdf](http://cms.math.ca/cjm/v39/cjm1987v39.0733-0747.pdf))

Plenty of further discussion in terms of [[model category]] theory is in 

* {#Jardine97} [[Rick Jardine]], _Generalized &#201;tale cohomology theories_, 1997 Progress in mathematics volume 146
  
Discussion in terms of [[(∞,1)-category]]/[[(∞,1)-topos]]-theory is in 

* [[Jacob Lurie]], _Sheaves of spectra_, section 1 of _[[Spectral Schemes]]_

### Application to K-theory

* [[Bertrand Toën]], section 1.2 of _K-theory and cohomology of algebraic stacks: Riemann-Roch theorems, D-modules and GAGA theorems_ ([arXiv:math/9908097](http://arxiv.org/abs/math/9908097))

* Michael Paluch, _Algebraic K-theory and topological spaces_ ([pdf](http://www.math.uiuc.edu/K-theory/0471/alg-top.pdf))

### Application to differential cohomology
 {#ReferencesApplicationToDifferentialCohomology}

Discussion of sheaves of spectra on the site of [[SmoothManifolds]] as a model for [[Whitehead-generalized cohomology theory|Whitehead-generalized]] [[differential cohomology]] (including the [[differential cohomology hexagon]]):

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_,  J. Homotopy Relat. Struct. 11, 1–66 (2016) ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

and withing the broader context of differential [[non-abelian cohomology]]:

* {#FSS20} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 4.3 in: _[[schreiber:The Character Map in Twisted Non-Abelian Cohomology|The character map in (twisted differential) non-abelian cohomology]]_ ([arXiv:2009.11909](https://arxiv.org/abs/2009.11909))

A book-length overview:

* {#AmabelDebrayHaine21} [[Araminta Amabel]], [[Arun Debray]], [[Peter J. Haine]] (eds.), _Differential Cohomology: Categories, Characteristic Classes, and Connections_. Based on [Fall 2019 talks at MIT's Juvitop seminar](https://math.mit.edu/juvitop/pastseminars/2019_Fall.html) by: A. Amabel, D. Chua, A. Debray, S. Devalapurkar, D. Freed, P. Haine, M. Hopkins, G. Parker, C. Reid, and A. Zhang. ([arXiv:2109.12250](https://arxiv.org/abs/2109.12250))



[[!redirects sheaves of spectra]]
[[!redirects stack of spectra]]
[[!redirects stacks of spectra]]

[[!redirects presheaf of spectra]]
[[!redirects presheaves of spectra]]

[[!redirects (∞,1)-sheaf of spectra]]
[[!redirects (∞,1)-sheaves of spectra]]

[[!redirects ∞-stack of spectra]]
[[!redirects ∞-stacks of spectra]]