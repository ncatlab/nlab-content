
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
The Grothendieck [[six operations]] formalism is a formalization of aspects of Verider duality.

com
In general abstract formulation one says that a locally compact [[site]] $X$ (e.g. a [[locally compact topological space]]) _satisfies Verdier duality_ if there exists a [[derived functor|derived]] [[left adjoint]] $\mathbb{L}p^!$ to the operation $\mathbb{R}p_!$ of [[direct image with compact support]] for the terminal map $X \to \ast$. More generally, in the relative situation, for $f \colon X \to Y$ a map, Verdier duality of $f$ means that $\mathbb{R}f_!$ has a derived left adjoint.



If this is the case, then one has the _[[dualizing object]]_ ([[dualizing module]]) $\omega \coloneqq \mathbb{L}p^! k$ (the image under the extra right adjoint of the [[ground ring]]) and for every [[abelian sheaf]] $V$ on $X$ can define the [[dual object]] $V^\vee \coloneqq [V,\omega]$. The analog of [[Poincaré duality]] is then the statement that the [[abelian sheaf cohomology]] with [[coefficients]] in $V$ is dual to the abelian sheaf cohomology with [[compact support]] with coefficients in $V^\vee$.

Concretely if $X$ is a [[manifold]], then $\omega$ is the sheaf of [[densities]] and if $V$ is a complex of (sections of) [[vector bundles]], then $V^\vee$ is the _densitized linear dual_.


## Related concepts

* [[Grothendieck duality]]

* [[Poincaré duality]]
  

## References

The duality is named after [[Jean-Louis Verdier]].

Accounts of the traditional notion include

* [[Amnon Neeman]], _The Grothendieck duality theorem via Bousfield's techniques and Brown representability_, Jour. Amer. Math. Soc. 9 (1996), 205&#8211;236. ([JSTOR](http://www.jstor.org/stable/2152846))

* Wikipedia, _[Verdier duality](http://en.wikipedia.org/wiki/Verdier_duality)_

* Liviu Niculaescu, _The derived category of sheaves and the Poincar&#233;-Verdier duality_ ([pdf](http://www3.nd.edu/~lnicolae/Verdier-ams.pdf))

* [[Jacob Lurie]], lecture notes on _Verdier duality_ ([pdf](http://www.math.harvard.edu/~lurie/283notes/Lecture17-Verdier.pdf), [pdf](http://www.math.harvard.edu/~lurie/287xnotes/Lecture19.pdf))


Discussion in the context of [[higher algebra]]/[[higher geometry]] is in 

* Roy Joshua, _Generalised Verdier duality for presheaves of spectra&#8212;I_, Journal of Pure and Applied Algebra Volume 70, Issue 3, 29 March 1991, Pages 273&#8211;289

* [[Jonathan Block]] and [[Andrey Lazarev]], _Homotopy Theory and Generalized Duality for Spectral Sheaves_, IMRN International Mathematics Research Notices
1996, No. 20 ([pdf](http://www.math.upenn.edu/~blockj/papers/BlockLazarevSpectralSheaves.pdf))


* [[Vladimir Drinfeld]], [[Dennis Gaitsgory]], section 5.3 _On some finiteness questions for algebraic stacks_ ([arXiv:1108.5351](http://arxiv.org/abs/1108.5351))




[[!redirects Verdier dualities]]