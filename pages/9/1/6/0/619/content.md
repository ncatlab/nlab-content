A [[full subcategory]] is **reflective** if its inclusion functor has a [[adjunction|left adjoint]].  The left adjoint is sometimes called the _reflector_.

A reflective subcategory is always closed under [[limit|limits]], and inherits [[colimit|colimits]] from the larger category by application of the reflector.

Given any adjoint pair $Q^*\dashv Q_*$ of functors  $Q^*:A\leftrightarrow B:Q_*$, the following are equivalent (Gabriel-Zisman):

* right adjoint $Q_*$ is fully faithful

* the counit $\varepsilon : Q_* Q^*\to 1_A$ of the adjunction is a natural isomorphism of functors 

* the monad $(Q^* Q_*,Q^*\varepsilon Q_*,\eta)$ associated to the adjunction is idempotent

* let $S$ be the set of morphisms $s$ in $A$ such that $Q^*(s)$ is invertible in $B$; and $P_S:A\to A[S^{-1}]$ canonical localization functor; the unique functor $H : A[S^{-1}]\to B$ such that $Q^* = H\circ P_S$ (given by the universal property of localization) is an equivalence of categories

When the reflector is a [[monomorphism]], a reflective category is often thought of as a full subcategory of *complete* objects in some sense; the reflector takes each object in the ambient category to its completion.  Example: Complete metric spaces within metric spaces. Category of sheaves over a site $S$ is a reflective subcategory of category of presheaves on $S$.