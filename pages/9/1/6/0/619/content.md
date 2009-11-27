#Contents#
* automatic table of contents goes here
{:toc}


## Definition

A [[full subcategory]] $C \subset D$ is **reflective** if its inclusion functor has a [[adjoint functor|left adjoint]]

$$
  C \stackrel{\stackrel{T}{\leftarrow}}{\hookrightarrow}
  D
  \,.
$$

The left adjoint is sometimes called the __reflector__.

The components of the unit 

$$
  \array{
    & \nearrow &\Downarrow^{\eta}& \searrow^{Id}
    \\
    D &\stackrel{T}{\to}& C &\hookrightarrow & D
  }
$$

of this [[adjunction]] "reflect" each object $d \in D$ into its image $T d$ in the reflective subcategory

$$
  \eta_d : d \to T  d
  \,.
$$

In the case that the functor $T$ is [[exact functor|left exact]] this reflection is called a [[localization]].

+--{.query}
Zoran: this is not universally accepted. In topos theory community yes. But in the setup of abelian categories, like categories of modules, people often use word localization even if left exactness is not met. If it is it is often said flat localization in those circles (though sometimes one says flat localization only if the stronger condition is satisfied: composed endofunctor is flat). The localization of the underlying ring (in the case of module categories) is the component of adjunction at that ring, and for Gabriel localizations (where $T$ is flat) the arget module is canonically a ring and the component of the adjunction is a ring morphism. But only if the localization is perfect this morphism of rings tell you all infrmation about the localization functor. 
=--

If the reflector $T$ is [[faithful functor|faithful]], the reflection is called a [[completion]].


## Characterizations

Given any adjoint pair $Q^*\dashv Q_*$ of functors  $Q^*:A\leftrightarrow B:Q_*$, the following are equivalent (Gabriel--Zisman):

* The right adjoint $Q_*$ is [[full and faithful functor|fully faithful]].

* The counit $\epsilon : Q_* Q^*\to 1_A$ of the adjunction is a [[natural isomorphism]] of functors.

* The [[monad]] $(Q^* Q_*,Q^*\varepsilon Q_*,\eta)$ associated to the adjunction is [[idempotent monad|idempotent]].

* Let $S$ be the set of morphisms $s$ in $A$ such that $Q^*(s)$ is invertible in $B$; and $P_S:A\to A[S^{-1}]$ canonical [[localization]] functor; then the unique functor $H : A[S^{-1}]\to B$ such that $Q^* = H\circ P_S$ (given by the universal property of localization) is an equivalence of categories.

+--{.query}
Zoran: Gabriel--Zisman neglect the set theoretical issues on the EXISTENCE of localizations. Is the last conditions really equivalent or we need to make some set-theoretical assumptions ?
=--


## Properties

A reflective subcategory is always closed under [[limit|limits]], and inherits [[colimit|colimits]] from the larger category by application of the reflector.

When the unit of the reflector is a [[monomorphism]], a reflective category is often thought of as a full subcategory of *complete* objects in some sense; the reflector takes each object in the ambient category to its completion.  Such reflective subcategories are sometimes called _mono-reflective_.  One similarly has _epi-reflective_ (when the unit is an [[epimorphism]]) and _bi-reflective_ (when the unit is a [[bimorphism]]).

In the last case, note that if the unit is an *iso*morphism, then the inclusion functor is an [[equivalence of categories]], so nontrivial bireflective subcategories can occur only in non-[[balanced categories]].  Also note that 'bireflective' does *not* mean reflective and [[coreflective subcategory|coreflective]].  One sees this term often in discussions of [[concrete categories]] (such as [[topological categories]]) where really something stronger holds: that the reflector lies over the [[identity functor]] on [[Set]].  In this case, one can say that we have a subcategory that is __reflective over $Set$__.


## Examples 

* Complete [[metric space]]s are mono-reflective in metric spaces; the reflector is called _completion_.

* The unital [[ring]]s form a mono-reflective subcategory of possibly nonunital rings; the reflector formally adjoins an [[identity element]].

* The [[category of sheaves]] on a [[site]] $S$ is a reflective subcategory of the category of presheaves on $S$; the reflector is called _[[sheafification]]_. In fact, categories of sheaves are precisely those reflective subcategories of presheaf categories for which the reflector is left [[exact functor|exact]]. This makes the inclusion functor precisely a [[geometric morphism]] of [[topos|topoi]].


## Property vs structure

Whenever $C$ is a full subcategory of $D$, we can say that objects of $C$ are objects of $D$ with some extra [[property, structure, stuff|property]].  But if $C$ is reflective in $D$, then we can turn this around and (by thinking of the left adjoint as a [[forgetful functor]]) think of objects of $D$ as objects of $C$ with (if we\'re lucky) some [[extra structure]] or (in any case) some [[extra stuff]].

This can always be made to work by brute force, but sometimes there is something insightful about it.  For example, a metric space is a complete metric space equipped with a dense subset.  Or, a possibly nonunital ring is a unital ring equipped with a unital homomorphism to the ring of integers.


##Generalizations

* [[reflective (infinity,1)-subcategory]]


[[!redirects reflector]]
