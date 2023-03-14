
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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
 {#Idea}

*S-modules* is the name (due to [EKMM 97](#EKMM97)) of one model of [[highly structured spectra]] that supports a [[symmetric monoidal smash product of spectra]]. 

Here "$S$" stands for the *[[sphere spectrum]]* (other traditional notation being "$Q S^0$" for the [[suspension spectrum]] $Q$ of the [[0-sphere]]) regarded as a [[ring spectrum]]. Namely, in [[categorification|homotopification]] of how general [[abelian groups]] may equivalently be understood as [[integers|$\mathbb{Z}$]]-[[modules]], so general [[spectra]] may (once their [[brave new algebra|brave new algebraic]] [[stable homotopy theory]] is set up) equivalently be understood as [[module spectra]] over the [[sphere spectrum]].

Concretely, the [[1-category]] of _S-modules_ as set up in [EKMM 97](#EKMM97) is a *[[presentable (∞,1)-category|presentation]]* (see at *[[model structure on S-modules]]*) of the [[symmetric monoidal (∞,1)-category]] [[stable (infinity,1)-category of spectra|of spectra]], with the special property that it implements the [[smash product of spectra]] such as to yield itself a [[symmetric monoidal category|symmetric]] [[monoidal model category|monoidal]] [[model category of spectra]]: the _[[model structure on symmetric spectra]]_. This implies in particular that with respect to this [[symmetric smash product of spectra]] an [[E-∞ ring]] is presented simply as a plain [[commutative monoid]] [[internalization|in]] S-modules.

Other presentations sharing this property are _[[symmetric spectra]]_ and _[[orthogonal spectra]]_.

## Construction

The construction of [[S-modules]] by ([EKMM 97](#EKMM97)) begins with the notion of [[coordinate-free spectrum|coordinate free Lewis-May spectra]].  Using the [[linear isometries operad]], one can construct a [[monad]] $\mathbb{L}$ on the category $\mathcal{S}$ of such spectra, and the category of $\mathbb{L}$-algebras is a well-behaved model for the stable homotopy category, and moreover admits a smash product which is associative up to isomorphism, but unital only up to weak equivalence.  However, the subcategory of the $\mathbb{L}$-algebras for which the unit transformations are isomorphisms is again a well-behaved model for $Ho \mathbb{S}$, which is moreover symmetric monoidal.

Since the unit transformation is of the form $S\wedge E \to E$, where $S$ is the [[sphere spectrum]], and this map looks like the action of a ring on a module, the objects of this subcategory are called **$S$-modules** and the category is called $Mod_S$.  The intuition is that just as an abelian group is a [[module]] over the archetypical ring $\mathbb{Z}$ of [[integer|integers]], a spectrum should be regarded as a module over the archetypal ring spectrum, namely the sphere spectrum.

Similarly, just as an ordinary [[ring]] is a [[monoid]] in the category $Mod_\mathbb{Z}$ of $\mathbb{Z}$-[[module]]s, i.e. a $\mathbb{Z}$-algebra, an $A_\infty$ or $E_\infty$ ring spectrum is a (possibly commutative) monoid in the category of $S$-modules, and thus referred to as an **$S$-algebra**.  More generally, for any $A_\infty$-[[A-infinity-ring|ring spectrum]] $R$, there is a notion of $R$-[[module]] spectra forming a category $Mod_R$, which in turn carries an associative and commutative smash product $\wedge_R$ and a [[model category]] structure on $Mod_R$ such that $\wedge_R$ becomes unital in the [[homotopy category]].  All this is such that an $A_\infty$-[[A-infinity-algebra|algebra]] over $R$ is a [[monoid object]] in $(Mod_R, \wedge_R)$.  Similarly $E_\infty$-[[E-infinity-algebra|algebras]] are commutative monoid objects in $(Mod_R, \wedge_R)$.

## Related concepts

[[model structure on spectra]], [[symmetric monoidal smash product of spectra]]

* [[symmetric spectrum]], [[model structure on symmetric spectra]]

* [[orthogonal spectrum]], [[model structure on orthogonal spectra]]

* **S-module**, [[model structure on S-modules]]

## References

The construction originates in

* {#EKMM97} [[Anthony Elmendorf]], [[Igor Kriz]], [[Michael Mandell]], [[Peter May]], *[[Rings, modules and algebras in stable homotopy theory]]*, AMS 1997 (2014) &lbrack;[ISBN:978-0-8218-4303-1](https://bookstore.ams.org/surv-47-s), [pdf](http://www.math.uchicago.edu/~may/BOOKS/EKMM.pdf)&rbrack;

Review:

* [[Anthony Elmendorf]], [[Igor Kriz]], [[Peter May]], sections 2 and 3 of _[[Modern foundations for stable homotopy theory]]_ ([pdf](http://hopf.math.purdue.edu/Elmendorf-Kriz-May/modern_foundations.pdf))

[[!redirects S-modules]]



