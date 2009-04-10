A [[cardinal number|cardinal]] is an [[ordinal]] ([[well-order]]ed [[transitive set]]) which is not a [[successor]] of any other ordinal. A cardinal $\pi$ is **regular** if it is not a union of $\lt\pi$ cardinals. A cardinal is a **strongly limiting cardinal** if $\lambda\lt \pi$ implies $2^\lambda\lt\pi$ (hence if $A\in\pi$ then the partitive (=power) set $P(A)\in\pi$). An **inaccessible cardinal** is any uncountable strongly limiting regular cardinal.

In ZFC one can not prove the existence of inaccessible cardinals. If one inaccessible cardinal exists, there are also infinitely many larger inaccessible cardinals.

The class $\mathbf{Card}$ of cardinals is the subclass of the well-ordered class $\mathbf{Ord}$ of [[ordinal]]s. Using transfinite recursion one defines a hierarchy of well-founded sets $V_\alpha$ where $\alpha\in\mathbf{Ord}$ as follows:
* $V_0 = \emptyset$
* $V_{\alpha+1} = P(V_\alpha)$
* $V_\alpha = \cup_{\beta\lt\alpha} V_\beta$ if $\alpha$ is a limiting ordinal. 

A [[Grothendieck universe]] in this approach is a set of the form $V_\alpha$ where $\alpha$ is an inaccessible cardinal. Thus the existence of inaccessible cardinals amounts to the axiom of existence of Grothendieck universes. 