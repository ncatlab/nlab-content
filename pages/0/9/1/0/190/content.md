
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Categories of categories
+--{: .hide}
[[!include categories of categories - contents]]
=--
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

**Cat** is a name for the [[category]] or [[2-category]] of all [[category|categories]].  

This is also the archetypical [[2-topos]].

## Definition

To avoid set-theoretic problems related to [[Russell's paradox]], it is typical to restrict $Cat$ to [[small category|small categories]].  But see [[CAT]] for alternatives.

To be explicit, define **Cat** to be the category with:

* [[small category|small categories]] as [[object|objects]],
* [[functor|functors]] as [[morphism|morphisms]];

* composition of morphisms the evident composition of functors.


This is probably the most common meaning of $Cat$ in the literature.

We more often use **Cat** to stand for the [[strict 2-category]] with:

* [[small category|small categories]] as [[object|objects]],
* [[functor|functors]] as [[morphism|morphisms]].
* [[natural transformation|natural transformations]] as [[2-morphism|2-morphisms]].

Here the [[vertical composition]] of 2-morphisms is the evident composition of component maps of natural transformations, whereas the [[horizontal composition]] is given by their [[Godement product]].


Finally, we can use **Cat** for the [[bicategory]] with:

* [[small category|small categories]] as [[object|objects]],
* [[anafunctor|anafunctors]] as [[morphism|morphisms]].
* [[ananatural transformation|ananatural transformations]] as [[2-morphism|2-morphisms]].

To be really careful, this version of $Cat$ is an [[anabicategory]].

## Properties

### Cartesian closed structure 

The category $Cat$, at least in its traditional version comprising small categories only, is [[cartesian closed]]: the [[exponential objects]] are [[functor categories]].  Direct proofs can be found in:

* p. 98 of [[Categories Work]], 2nd ed.
* remark below Definition 4.3.9 in [[Category Theory in Context]]
* [[Steve Awodey]], *Category Theory*, Second Edition, Sections 7.5-7.7.

A more indirect proof could proceed by identifying $Cat$ via the [[nerve]] construction as a [[reflective subcategory]] of [[sSet]], which is cartesian closed as it is a [[presheaf category]], and showing that this subcategory is an [[exponential ideal]].

### Size issues

As a $2$-category, $Cat$ could even include (some) [[large category|large categories]] without running into Russell's paradox.  More precisely, if $U$ is a [[Grothendieck universe]] such that $\Set$ is the category of all $U$-small sets, then you can define $\Cat$ to be the 2-category of all $U'$-small categories, where $U'$ is some Grothendieck universe containing $U$.  That way, you have $\Set \in \Cat$ without contradiction.  (This can be continued to [[higher category theory|higher categories]].)

By the [[axiom of choice]], the two definitions of $Cat$ as a $2$-[[2-category|category]] are [[equivalence of categories|equivalent]].  In contexts without choice, it is usually better to use anafunctors all along; if necessary, use $Str Cat$ for the strict $2$-category.  Even without choice, a functor or anafunctor between categories is an [[equivalence]] in the anabicategory $Cat$ iff it is [[essentially surjective functor|essentially surjective]] and [[full and faithful functor|fully faithful]].  However, the weak inverse of such a functor may not be a functor, so it need not be an equivalence in $Str Cat$.  We can regard $Cat$ as obtained from $Str Cat$ using [[homotopy theory]] by "formally inverting" the essentially surjective and fully faithful functors as [[weak equivalence]]s.


### Colimits

* [[pushout]]s in [[Cat]] of injective functors are considered in ([MacdonaldScull](#MacdonalScull)).

## Related concepts

* [[elementary theory of the category of categories]]

[[!include categories of categories - contents]]


## References

* {#Law66} [[William Lawvere]], *The Category of Categories as a Foundation for Mathematics*, pp.1-20 in Eilenberg, Harrison, MacLane, R&#246;hrl (eds.), _Proceedings of the Conference on Categorical Algebra - La Jolla 1965_, Springer Heidelberg 1966 ([doi:10.1007/978-3-642-99902-4_1](https://doi.org/10.1007/978-3-642-99902-4_1))

* [[John Gray]], _[[Adjointness for 2-Categories|Formal category theory: adjointness for 2-categories]]_, Lecture Notes in Mathematics, Vol. 391. 
Springer 1974 ([doi:10.1007/BFb0061280](https://doi.org/10.1007/BFb0061280))

See also the references at _[[category]]_ and _[[category theory]]_.

Discussion of (certain) [[pushouts]] in $Cat$ is in 

* {#MacdonalScull} John Macdonald, Laura Scull, _Amalgamations of categories_ ([pdf](http://faculty.fortlewis.edu/Scull_L/pushouts.pdf))


category: category

[[!redirects category of categories]]
[[!redirects 2-category of categories]]
