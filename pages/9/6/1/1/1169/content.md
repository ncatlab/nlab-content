
#Contents#
* automatic table of contents goes here
{:toc}

# Idea

A _Reedy category_ is a category $R$ equipped with a structure enabling the inductive construction of diagrams and natural transformations of shape $R$.  

The most important consequence of a Reedy structure on $R$ is the existence of a [[model category|model structure]] on the [[functor category]] $M^R$ whenever $M$ is a model category (no extra hypotheses on $M$ are required): the 

* [[Reedy model structure]] .

# Definition

A **Reedy category** is a [[category]] $R$ equipped with two [[wide subcategory|lluf subcategories]] $R_+$ and $R_-$ and a [[function]] $d:ob(R) \to \alpha$ called _degree_, where $\alpha$ is an [[ordinal number]], such that:

* Every nonidentity morphism in $R_+$ raises degree,
* Every nonidentity morphism in $R_-$ lowers degree, and
* Every morphism $f$ in $R$ factors uniquely as a map in $R_-$ followed by a map in $R_+$.


# Examples

* Any ordinal $\alpha$, considered as a [[poset]] and hence a category, is a Reedy category with $\alpha_+=\alpha$, $\alpha_-$ the [[discrete category]] on $ob(\alpha)$, and $d$ the identity.

* The [[opposite category|opposite]] of any Reedy category is a Reedy category; simply exchange $R_+$ and $R_-$.

* The prototypical examples of Reedy categories are the [[simplex category]] $\Delta$ and its opposite $\Delta^{op}$.  More generally, for any [[simplicial set]] $X$, its [[category of simplices]] $\Delta/X$ is a Reedy category.




# Generalizations

## generalized Reedy category ##

One problem with the notion of Reedy category is that it is [[evil]]: it is not invariant under [[equivalence of categories]].  It's not hard to see that any Reedy category is necessarily skeletal.  In fact, it's even worse: no Reedy category can have _any_ nonidentity isomorphisms!  This is problematic for many $\Delta$-like categories such as the [[category of cycles]], Segal's category $\Gamma$, the [[tree category]] $\Omega$, and so on.

The following generalization of the notion of Reedy category, due to
Ieke Moerdijk and Clemens Berger, avoids these problems and maintains
the truth of the  Theorem relating Reedy categories and model
structures from [[Reedy model structure]].  Define a **generalized Reedy category** to be a category $R$ with the same structure $R_+$, $R_-$, and $d$ as before, but now such that

* every non-isomorphism in $R_+$ raises degree,
* every non-isomorphism in $R_-$ lowers degree,
* every morphism $f$ factors as a map in $R_-$ followed by a map in $R_+$, uniquely up to isomorphism, and
* If $f\in R_-$ and $\theta$ is an isomorphism such that $\theta f = f$, then $\theta = 1$ (isomorphisms see the maps in $R_-$ as [[epimorphism|epis]]).

The last condition is not self-dual, but has an obvious dual version.

## enriched Reedy category ##

There is also a generalization of the notion of Reedy category to the context of [[enriched category theory]]: this is an [[enriched Reedy category]].
