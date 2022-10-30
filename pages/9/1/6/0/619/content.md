A [[full subcategory]] is **reflective** if its inclusion functor has a [[adjoint functor|left adjoint]].  The left adjoint is sometimes called the _reflector_.

A reflective subcategory is always closed under [[limit|limits]], and inherits [[colimit|colimits]] from the larger category by application of the reflector.

Given any adjoint pair $Q^*\dashv Q_*$ of functors  $Q^*:A\leftrightarrow B:Q_*$, the following are equivalent (Gabriel--Zisman):

* The right adjoint $Q_*$ is [[full and faithful functor|fully faithful]].

* The counit $\epsilon : Q_* Q^*\to 1_A$ of the adjunction is a [[natural isomorphism]] of functors.

* The [[monad]] $(Q^* Q_*,Q^*\varepsilon Q_*,\eta)$ associated to the adjunction is [[idempotent monad|idempotent]].

* Let $S$ be the set of morphisms $s$ in $A$ such that $Q^*(s)$ is invertible in $B$; and $P_S:A\to A[S^{-1}]$ canonical [[localization]] functor; then the unique functor $H : A[S^{-1}]\to B$ such that $Q^* = H\circ P_S$ (given by the universal property of localization) is an equivalence of categories.

When the unit of the reflector is a [[monomorphism]], a reflective category is often thought of as a full subcategory of *complete* objects in some sense; the reflector takes each object in the ambient category to its completion.  Such reflective subcategories are sometimes called _mono-reflective_.  One similarly has _epi-reflective_ (when the unit is an [[epimorphism]]) and _bi-reflective_ (when the unit is a [[bimorphism]]).

In the last case, note that if the unit is an *iso*morphism, then the inclusion functor is an [[equivalence of categories]], so nontrivial bireflective subcategories can occur only in non-[[balanced categories]].  Also note that 'bireflective' does *not* mean reflective and [[coreflective subcategory|coreflective]].  One sees this term often in discussions of [[concrete categories]] (such as [[topological categories]]) where really something stronger holds: that the reflector lies over the [[identity functor]] on [[Set]].  In this case, one can say that we have a subcategory that is __reflective over $Set$__.


## Examples #

* Complete [[metric space]]s are mono-reflective in metric spaces; the reflector is called _completion_.

* The unital [[ring]]s form a mono-reflective subcategory of possibly nonunital rings; the reflector formally adjoins an [[identity element]].

* The [[category of sheaves]] on a [[site]] $S$ is a reflective subcategory of the category of presheaves on $S$; the reflector is called _[[sheafification]]_. In fact, categories of sheaves are precisely those reflective subcategories of presheaf categories for which the reflector is left [[exact functor|exact]]. This makes the inclusion functor precisely a [[geometric morphism]] of [[topos|topoi]].


## Property vs structure

Whenever $C$ is a full subcategory of $D$, we can say that objects of $C$ are objects of $D$ with some extra [[property, structure, stuff|property]].  But if $C$ is reflective in $D$, then we can turn this around and (by thinking of the left adjoint as a [[forgetful functor]]) think of objects of $D$ as objects of $C$ with some [[extra stuff]].

This can always be made to work by brute force, but sometimes there is something insightful about it.  For example, a metric space is a complete metric space equipped with a dense subset.  Or, a possibly nonunital ring is a unital ring equipped with a unital homomorphism to the ring of integers.


##Generalizations#

* [[reflective (infinity,1)-subcategory]]