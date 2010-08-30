
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

**Cat** is a name for the [[category]] or [[2-category]] of all [[category|categories]].  

This is also the archetypical [[2-topos]].

## Definition

To avoid set-theoretic problems related to Russell's paradox, it is typical to restrict $Cat$ to [[small category|small categories]].  But see [[CAT]] for alternatives.

To be explicit, define **Cat** to be the category with:

* [[small category|small categories]] as [[object|objects]],
* [[functor|functors]] as [[morphism|morphisms]];

* composition of morphisms the evident composition of functors.


This is probably the most common meaning of $Cat$ in the literature.

We more often use **Cat** to stand for the [[strict 2-category]] with:

* [[small category|small categories]] as [[object|objects]],
* [[functor|functors]] as [[morphism|morphisms]].
* [[natural transformation|natural transformations]] as [[2-morphism|2-morphisms]].

Here the [[vertical composition]] of 2-morphisms is the evident composition of component maps of matural transformations, whereas the [[horizontal composition]] is given by their [[Godement product]].


Finally, we can use **Cat** for the [[bicategory]] with:

* [[small category|small categories]] as [[object|objects]],
* [[anafunctor|anafunctors]] as [[morphism|morphisms]].
* [[ananatural transformation|ananatural transformations]] as [[2-morphism|2-morphisms]].

To be really careful, this version of $Cat$ is an [[anabicategory]].


## Size issues

As a $2$-category, $Cat$ could even include (some) [[large category|large categories]] without running into Russell's paradox.  More precisely, if $U$ is a [[Grothendieck universe]] such that $\Set$ is the category of all $U$-small sets, then you can define $\Cat$ to be the 2-category of all $U'$-small categories, where $U'$ is some Grothendieck universe containing $U$.  That way, you have $\Set \in \Cat$ without contradiction.  (This can be continued to [[higher category theory|higher categories]].)

By the [[axiom of choice]], the two definitions of $Cat$ as a $2$-[[2-category|category]] are [[equivalence of categories|equivalent]].  In contexts without choice, it is usually better to use anafunctors all along; if necessary, use $Str Cat$ for the strict $2$-category.  Even without choice, a functor or anafunctor between categories is an [[equivalence]] in the anabicategory $Cat$ iff it is [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|fully faithful]].  However, the weak inverse of such a functor may not be a functor, so it need not be an equivalence in $Str Cat$.  We can regard $Cat$ as obtained from $Str Cat$ using [[homotopy theory]] by "formally inverting" the essentially surjective and fully faithful functors as [[weak equivalence]]s.


category: category
