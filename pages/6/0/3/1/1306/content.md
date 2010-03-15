
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of Reedy category, though useful, is in some contexts inconveniently restrictive, since no Reedy category can contain any nonidentity isomorphisms.  This is problematic for many "shape categories" such as Connes' [[category of cycles]] $\Lambda$, Segal's category $\Gamma$, the [[tree category]] $\Omega$, and so on.  The notion of *generalized Reedy category* lifts this restriction, while maintaining the truth of the main theorem about Reedy categories: the existence of the [[Reedy model structure]].

## Definition

A **generalized Reedy category** is a category $R$ together with two [[wide subcategories]] $R_+$ and $R_-$, and a function $d\colon ob(R)\to \alpha$ called *degree*, for some [[ordinal]] $\alpha$, such that

* every non-isomorphism in $R_+$ raises degree,
* every non-isomorphism in $R_-$ lowers degree,
* every isomorphism in $R$ preserves degree,
* $R_+\cap R_-$ is the [[core]] of $R$ (equivalently, every isomorphism is in both $R_+$ and $R_-$, i.e. they are not just wide but [[pseudomonic functor|pseudomonic]] subcategories),
* every morphism $f$ factors as a map in $R_-$ followed by a map in $R_+$, uniquely up to isomorphism, and
* If $f\in R_-$ and $\theta$ is an isomorphism such that $\theta f = f$, then $\theta = 1$ (isomorphisms see the maps in $R_-$ as [[epimorphism|epis]]).

The last condition implies that the isomorphism in the penultimate condition must be unique.  It is not self-dual, but has an obvious dual version.  A generalized Reedy category is said to be **dualizable** if it satisfies both this condition and its dual.

For clarity, in the context of generalized Reedy categories, an ordinary [[Reedy category]] may be called a *strict Reedy category*.


## Examples

* Any [[Reedy category]] is a generalized Reedy category.

* Any [[groupoid]] $G$ is also a generalized Reedy category, with $G_+ = G_- = G$.

* Connes' [[category of cycles]] $\Lambda$.

* Segal's category $\Gamma$.

* the Moerdijk-Weiss [[tree category]] $\Omega$.

* Any generalized [[direct category]] or generalized [[inverse category]] is also a generalized Reedy category, in which either $R_-$ or $R_+$ consists only of the isomorphisms.


## References

* [[Clemens Berger]] and [[Ieke Moerdijk]], _On an extension of the notion of Reedy category_ , [arXiv:0809.3341](http://arxiv.org/abs/0809.3341)

[[!redirects generalized Reedy categories]]
