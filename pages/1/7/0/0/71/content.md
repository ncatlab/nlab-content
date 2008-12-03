#Idea#

Orientals are "oriented simplices": the $n$-th oriental $O(\Delta^n)$ is the simplicial $n$-simplex equipped with the structure of a (free, see below) [[omega-category]] such that $k$-morphisms in $O(\Delta^n)$ are pasting diagrams of $k$-faces in $\Delta^n$.

Therefore orientals translate between the [[simplicial set|simplicial]] and the [[globular set|globular]] world of [[higher category theory|infinity-categories]].

The first few orientals look as follows:

<img src="http://www.math.uni-hamburg.de/home/schreiber/pics/orientals.gif" alt=""></img>

#Structures#

##As cosimplicial $\omega$-category##

The construction of orientals is designed to be compatible with face and degeneracy maps. Therefore the orientals arrange themselves into a cosimplicial [[omega-category]], i.e. a functor

$$
  O : \Delta \to \omega Cat
$$

from the [[simplicial category]] $\Delta$ to the category of [[omega-category|omega-categories]].

## $\omega$-Nerve ##

The $\omega$-nerve $N(C)$ of an [[omega category]] $C$ is a simplicial set which generalizes the [[nerve]] of an ordinary category: the collection of $k$-simplices in $N(C)$ is the collection of images of the $k$-th oriental $O_k$ in $C$, i.e.

$$
  (N(C))_k := Hom_{\omega Cat}(O([k]), C)
  \,.
$$

This naturally extends to a functor

$$
  N : \omega Cat \stackrel{Hom_{\omega Cat}(O([-_2]),-_1)}{\to}
  SimplicialSets
  \,.
$$

## Free $\omega$-Category on a simplicial set##

The $\omega$-nerve has a left [[adjoint]], the free $\omega$category on a simplicial set

$$
  F : SimplicialSets \to \omega Cat
$$

given by the [[end and coend|coend]]

$$
  F(S_\bullet) := \int^{[n] \in \Delta} S_n \cdot
   O([n])
  \,.
$$

(Here one uses that $\omega Cat$ is naturally tensored over $Sets$. See [[Enriched Category Theory]].)


+-- {: .query}

Is $F$ faithful? It seems to be... If not, how does it fail to be faithful? 

=--

#Relation to $\omega$-groupoids#

Regarding the standard $n$-simplex as a filtered space with the standard filtering, and denoting for $X$ a filtered space by $\Pi_\omega(X)$ the fundamental filter-respecting $\omega$-groupoid of $X$, we obtain a cosimplicial [[omega-category|omega-groupoid]]

$$
  \Pi_\omega(\Delta^{-})
  :
  \Delta \to \omega Groupoids
$$




#Literature#

The orientals were introduced in

* Ross Street, _The algebra of oriented simplexes_, J. Pure Appl. Algebra 49 (1987) 283-335; MR89a:18019 ([pdf](http://www.math.mq.edu.au/~street/aos.pdf)).

The $\omega$-groupoids $\Pi_\omega(\Delta^{n})$ are discussed in detail in

* Ronald Brown, Philip J. Higgins and Rafael Sivera, _Nonabelian algebraic topology_ ([pdf](http://www.bangor.ac.uk/~mas010/rbrsbookb-e-131008.pdf))

#Further resources#

We had related blog discussion in the following $n$-Caf&eacute;-entries:

* [Freely generated $\omega$-categories](http://golem.ph.utexas.edu/category/2008/10/freely_generated_categories.html)