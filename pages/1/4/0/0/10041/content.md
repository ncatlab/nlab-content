
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called _Verdier duality_  is the refinement of [[Poincaré duality]] from [[ordinary cohomology]] to [[abelian sheaf cohomology]]. 
The Grothendieck [[six operations]] formalism is a formalization of aspects of Verdier duality.

In general abstract formulation one says that a locally compact [[site]] $X$ (e.g. a [[locally compact topological space]]) _satisfies Verdier duality_ if there exists a [[derived functor|derived]] [[right adjoint]] $\mathbb{L}p^!$ ([[exceptional inverse image]]) to the operation $\mathbb{R}p_!$ of [[direct image with compact support]] for the terminal map $X \to \ast$. More generally, in the relative situation, for $f \colon X \to Y$ a map, Verdier duality of $f$ means that $\mathbb{R}f_!$ has a derived right adjoint. If here $X$ is a [[scheme]] and $f_! \simeq f_\ast$ coincides with the [[direct image]] ("[[Grothendieck context]]") then this is called _[[Grothendieck duality]]_. Therefore one often speaks of _Verdier-Grothendieck duality_. 



If these adjoints exist, then one has the _[[dualizing object in a closed category]]_ ([[dualizing module]]) $\omega \coloneqq \mathbb{L}p^! k$ (the image under the extra right adjoint of the [[unit object]]) and for every [[abelian sheaf]] $V$ on $X$ can define the [[dual object in a closed category]] 

$$
  \mathbb{D}V \coloneqq [V,\omega]
  \,.
$$ 

The analog of [[Poincaré duality]] is then the statement that the [[abelian sheaf cohomology]] with [[coefficients]] in $V$ is dual to the abelian sheaf cohomology with [[compact support]] with coefficients in $\mathbb{D}V$.


## Implementations

A fairly general class of implementations of Verdier-Grothendieck duality is discussed in ([Joshua, theorem 1.3](#Joshua)).

With assumption ([Joshua, 4.3](#Joshua)) this derives that dualization intertwines the two pushforwards as $\mathbb{D} \circ f_\ast \simeq f_! \circ \mathbb{D}$ ([Joshua, corollary 5.4](#Joshua)).

## Related concepts

* [[Verdier-Grothendieck context]]

* [[Grothendieck duality]]

* [[Poincaré duality]]
  

## References

The duality is named after [[Jean-Louis Verdier]].

Accounts of the traditional notion include

* [[Amnon Neeman]], _The Grothendieck duality theorem via Bousfield's techniques and Brown representability_, Jour. Amer. Math. Soc. 9 (1996), 205&#8211;236. ([JSTOR](http://www.jstor.org/stable/2152846))
 {#Neeman96}

* Wikipedia, _[Verdier duality](http://en.wikipedia.org/wiki/Verdier_duality)_

* Liviu Niculaescu, _The derived category of sheaves and the Poincar&#233;-Verdier duality_ ([pdf](http://www3.nd.edu/~lnicolae/Verdier-ams.pdf))

* [[Jacob Lurie]], lecture notes on _Verdier duality_ ([pdf](http://www.math.harvard.edu/~lurie/283notes/Lecture17-Verdier.pdf), [pdf](http://www.math.harvard.edu/~lurie/287xnotes/Lecture19.pdf))

A general abstract formalization is in 

* [[Roy Joshua]], _Grothendieck-Verdier duality in enriched symmetric monoidal $t$-categories_ ([[JoshuaDuality.pdf:file]])
 {#Joshua}

Discussion in the context of [[higher algebra]]/[[higher geometry]] is in 

* [[Roy Joshua]], _Generalised Verdier duality for presheaves of spectra&#8212;I_, Journal of Pure and Applied Algebra Volume 70, Issue 3, 29 March 1991, Pages 273&#8211;289

* [[Jonathan Block]] and [[Andrey Lazarev]], _Homotopy Theory and Generalized Duality for Spectral Sheaves_, IMRN International Mathematics Research Notices
1996, No. 20 ([pdf](http://www.math.upenn.edu/~blockj/papers/BlockLazarevSpectralSheaves.pdf))


* [[Vladimir Drinfeld]], [[Dennis Gaitsgory]], section 5.3 _On some finiteness questions for algebraic stacks_ ([arXiv:1108.5351](http://arxiv.org/abs/1108.5351))


* [[Jacob Lurie]], section 4.2 of _[[Representability theorems]]_

Formulation in terms of an equivalence between sheaves and cosheaves is in 

* [[Peter Schneider]], _Verdier duality on the building_, Journal reine angew. Math. 494, 1998 

* [[Justin Curry]], _Sheaves, Cosheaves and Applications_ ([arXiv:1303.3255](http://arxiv.org/abs/1303.3255))

* [[Jacob Lurie]], section 5.3.5 of _[[Higher Algebra]]_

Discussion in the context of prestacks and diagrams of schemes

* [[Dennis Gaitsgory]], _The Atiyah-Bott formula for the cohomology of the moduli space of bundles on a  curve_ ([arXiv:1505.02331](http://arxiv.org/abs/1505.02331))

* Alexey Kalugin, _On categorical approach to Verdier Duality_ ([arXiv:1505.06922](http://arxiv.org/abs/1505.06922))


[[!redirects Verdier dualities]]