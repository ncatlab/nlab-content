#Definition#

Let $S$ be one of the categories of [[geometric shapes for higher structures]], such as the [[globe category]] $G$, the [[simplex category]] $\Delta$, the [[cube category]] $\Box$, the cyclic category $\Lambda$ of Connes, or certain category $\Omega$ related to trees whose corresponding presheaves are dendroidal sets. 

If $C$ is any [[locally small category|locally small]] category or, more generally, a $V$-[[enriched category]] equipped with a [[functor]]
$$
  i : S \to C
$$
we obtain a functor

$$
  N : C \to V^{S^{op}}
$$

from $C$ to [[globular set]]s or [[simplicial set]]s or [[cubical set]]s, respectively, (or the corresponding $V$-objects) given on an [[object]] $c \in C$ by

$$
  N_i(c) : S^{op} \stackrel{i}\to C^{op} 
    \stackrel{C(-,c)}{\to}
    V
  \,.
$$

This $N_i(c)$ is the **nerve** of $c$ with respect to the chosen $i : S \to V$.

Typically, one wants that $i$ is [[dense functor]], i.e. that every object $c$ of $C$ is canonically a colimit of a diagram of objects in $M$, more precisely,
$$
\mathrm{colim}((i/c)\stackrel{\mathrm{pr}_S}{\longrightarrow} S \stackrel{i}{\to} C) = c,
$$
what is equivalent to the requirement that the corresponding nerve functor is fully faithful (on other words, if $i$ is inclusion then $S$ is a left adequate subcategory of $C$ in terminology of [Isbell1960]). 
The nerve functor may be viewed as a [[singular functor]] of the functor $i$.

#Examples#

* The standard example is $C =$ [[Cat]] and $i : \Delta \to Cat$ the functor which embeds the [[simplex category]] (regarded, say, as the full subcategory of finite occupied linear [[quiver]]s). Then for $D$ any category its _nerve_, $N(D)$ is a simplicial set whose set of $n$-simplices is the set of sequences of composable morphisms of length $n$ in $D$. The face and degeneracy maps come from composition of morphisms and from inserting identity morphisms.

* This previous example is the restriction to 1-categories of the nerve ("$\omega$-nerve") on [[strict omega-category|strict omega-categories]] which is induced by the [[oriental]]s $i := O : \Delta \to \omega Cat$. This nerve is not fully faithful.

* When $C$ is the strict 1-category of [[2-category|2-categories]] or of [[bicategory|bicategories]] and homomorphisms of bicategories, and $S=\Delta$ the corresponding nerve is called the _Duskin nerve_.

#Remarks:# 

##Geometric realization##
Often the operation of taking the nerve of a (higher) category is followed by forming the [[geometric realization]] of the corresponding cellular set.

##Nerves and higher categories##
For many purposes it is convenient to conceive categories and especially [[infinity-category|infinity-categories]] entirely in terms of their nerves: those simplicial sets that arise as certain nerves are usually characterized by certain properties. So one can turn this around and _define_ an [[infinity-category]] as a simplicial set with certain properties. This is the strategy of a [[geometric definition of higher category]]. Examples for this are [[complicial set|complicial sets]], [[Kan complex|Kan complexes]], [[quasi-category|quasi-categories]], [[simplicial T-complex|simplicial T-complexes]],...

##Internal nerve##
A variant of the nerve construction can also be applied _internally_ within a category, to any internal category, see the discussion at [[internal category]].

##Literature##

[DwyerKan1984]
W. G. Dwyer, D. M. Kan, Singular functors and realization functors, Nederl. Akad. Wetensch. Indag. Math. 46 (1984), no. 2, 147--153. <a href="http://www.nd.edu/~wgd/Dvi/SingularAndRealization.pdf"> pdf </a>

[Isbell1960] J. R. Isbell, Adequate subcategories, Illinois J. Math. 4, 541-552 (1960)

[Leinster2004] T. Leinster, Higher operads, higher categories, London Mathematical Society Lecture Note Series, 298. Cambridge Univ. Press 2004. xiv+433 pp. ISBN: 0-521-53215-9, <a href="http://front.math.ucdavis.edu/0305.5049">arXiv:math.CT/0305049</a>

[Street1987] R. Street, The algebra of oriented simplexes,
J. Pure Appl. Algebra 49 (1987), no. 3, 283--335.  