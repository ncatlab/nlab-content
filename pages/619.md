A [[full subcategory]] is **reflective** if its inclusion functor has a [[adjoint functor|left adjoint]].  The left adjoint is sometimes called the _reflector_.

A reflective subcategory is always closed under [[limit|limits]], and inherits [[colimit|colimits]] from the larger category by application of the reflector.

Given any adjoint pair $Q^*\dashv Q_*$ of functors  $Q^*:A\leftrightarrow B:Q_*$, the following are equivalent (Gabriel--Zisman):

* The right adjoint $Q_*$ is [[full and faithful functor|fully faithful]].

* The counit $\epsilon : Q_* Q^*\to 1_A$ of the adjunction is a [[natural isomorphism]] of functors.

* The [[monad]] $(Q^* Q_*,Q^*\varepsilon Q_*,\eta)$ associated to the adjunction is [[idempotent monad|idempotent]].

* Let $S$ be the set of morphisms $s$ in $A$ such that $Q^*(s)$ is invertible in $B$; and $P_S:A\to A[S^{-1}]$ canonical [[localization]] functor; then the unique functor $H : A[S^{-1}]\to B$ such that $Q^* = H\circ P_S$ (given by the universal property of localization) is an equivalence of categories.

When the unit of the reflector is a [[monomorphism]], a reflective category is often thought of as a full subcategory of *complete* objects in some sense; the reflector takes each object in the ambient category to its completion.  Such reflective subcategories are sometimes called _mono-reflective_.

# Examples #

* Complete [[metric space]]s are mono-reflective in metric spaces; the reflector is called _completion_.

* The category of [[sheaf|sheaves]] on a [[site]] $S$ is a reflective subcategory of the category of presheaves on $S$; the reflector is called _[[sheafification]]_.


#Generalizations#

* [[reflective (infinity,1)-subcategory]]