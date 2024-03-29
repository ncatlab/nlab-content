
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the [[categorical semantics]] of [[dependent type theory]] in some suitable [[category]] $\mathcal{C}$ (see at _[[relation between category theory and type theory]]_) a [[type]] $X$ in the empty [[context]] is usually interpreted as an [[object]] $[X]$ in the given target [[category]], such that the unique [[morphism]] $[X]\to \ast$ to the [[terminal object]] (which interprets the [[unit type]]) is a special morphism called a [[display map]]. Specifically in the context of [[homotopy type theory]] display maps are typically [[fibrations]] with respect to some [[homotopical category]] structure on $\mathcal{C}$ (for instance the structure of a [[category of fibrant objects]] or even that of a [[model category]], in particular that of a [[type-theoretic model category]]). Since in $\mathcal{C}$ objects $[X]$ for which $[X] \to \ast$ is a [[fibration]] are called _[[fibrant objects]]_, one may then call a closed type which is to be interpreted this way as a _fibrant type_.
More generally, an open type $T$ in context $\Gamma$ is called _fibrant_ if $[\Gamma.T] \to [\Gamma]$ is a fibration.

Usually _all_ types are required to be interpreted this way, and hence often the term "fibrant type" is not used, since often non-fibrant types are never considered. 

However in general one may want to consider flavors of [[dependent type theory]] with [[categorical semantics]] in suitable [[homotopical categories]] which explicitly distinguishes between fibrant and non-fibrant interpretation. One example of this is what has come to be called [[two-level type theory]] (2LTT).  Default [[homotopy type theory]] (HoTT) has interpretation in [[type-theoretic model categories]] which is such that, roughly, [[Quillen equivalence]] is respected in that the interpretation in a way only depends on the [[(infinity,1)-category]] which is [[presentable (infinity,1)-category|presented]] by the model category. Since up to [[weak equivalence]] every object in the model category is fibrant, this means that in this sense there is no sensible distinction between fibrant and non-fibrant objects/types. On the other hand, 2LTT is more a language for the [[type-theoretic model category]] itself (or whatever homotopical category plays its role), not just for the [[(infinity,1)-category]] that it is going to present. In its interpretation one explicitly wants to be able to distinguish between any object and its fibrant replacement. Hence in this context one distinguishes between "fibrant types" that are required to be interpreted as [[fibrant objects]] and "non-fibrant types" which may be interpreted as more general objects.

## Related concepts

* [[fibrant replacement]]
* [[contextual fibrancy]]

[[!redirects fibrant type]]
[[!redirects fibrant types]]
[[!redirects non-fibrant type]]
[[!redirects non-fibrant types]]
