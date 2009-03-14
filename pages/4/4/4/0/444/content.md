#Definition#

Let $S$ be one of the categories of [[geometric shapes for higher structures]], such as the [[globe category]] $G$ or the [[simplex category]] $\Delta$, or the [[cube category]] $\Box$. 

Then for $C$ any [[locally small category|locally small]] or otherwise $V$-[[enriched category]] equipped with a [[functor]]
$$
  s : S \to C
$$

we obtain a functor

$$
  N : C \to V^{S^{op}}
$$

from $C$ to [[globular set]]s or [[simplicial set]]s or [[cubical set]]s, respectively, (or the corresponding $V$-objects) given on an [[object]] $c \in C$ by

$$
  N_s(c) : S^{op} \stackrel{s}{\to} C^{op} 
    \stackrel{C(-,c)}{\to}
    V
  \,.
$$

This $N_s(c)$ is the **nerve** of $c$ with resppect to the chosen $s : S \to V$.

#Examples#

* The standard example is $C =$ [[Cat]] and $s : \Delta \to Cat$ the functor which embeds the [[simplex category]] (regarded, say, as the full subcategory of finite occupied linear [[quiver]]s). Then for $D$ any category its _nerve_, $N(D)$ is a simplicial set whose set of $n$-simplices is the set of sequences of composable morphisms of length $n$ in $D$. The face and degeneracy maps come from composition of morphisms and from inserting identity morphisms.

* This previous example is the restriction to 1-categories of the nerve ("$\omega$-nerve") on [[strict omega-category|strict omega-categories]] which is induced by the [[oriental]]s $s := O : \Delta \to \omega Cat$.

* The nerve at the level of [[2-category|2-categories]] and [[bicategory|bicategories]] is called the _Duskin nerve_.

#Remarks:# 

##Geometric realization##
Often the operation of taking the nerve of a (higher) category is followed by forming the [[geometric realization]] of the corresponding cellular set.

##Nerves and higher categories##
For many purposes it is convenient to conceive categories and especially [[infinity-category|infinity-categories]] entirely in terms of their nerves: those simplicial sets that arise as certain nerves are usually characterized by certrain properties. So one can turn this around and _define_ an [[infinity-category]] as a simplicial set with certain properties. This is the strategy of a [[geometric definition of higher category]]. Examples for this are [[complicial set|complicial sets]], [[Kan complex|Kan complexes]], [[quasi-category|quasi-categories]], [[simplicial T-complex|simplicial T-complexes]],...

##Internal nerve##
The nerve construction can also be applied _internally_ within a category, to any internal category, see the discussion at [[internal category]].