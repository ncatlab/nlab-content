#Idea#

According to the general pattern on [[(n,r)-category]], an $(\infty,1)$-category is a (weak) [[infinity-category]] in which all $n$-morphisms for $n \geq 2$ are [[equivalence]]s.

To some extent an $(\infty,1)$-category can be thought of as a [[enriched category|category enriched in]] [[(infinity,0)-category|(infinity,0)]]-categories, namely in [[infinity-groupoid]]s.

For a discussion of the motivation and purpose of $(\infty,1)$-categories see [[why (infinity,1)-categories?]].


#Definition#

We start with the definition promoted by [[Andre Joyal]], which goes back to Boardman-Vogt.

This is a [[geometric definition of higher category]] which conceives an $(\infty,1)$-category as a [[simplicial set]] with extra [[stuff, structure, property|property]]. It is a straightforward generalization of the definition of [[infinity-groupoid]] as a [[Kan complex]]. 

Recall that a [[Kan complex]] is a [[simplicial set]] in which every [[horn]] $\Lambda^k[n]$ has a filler. This condition may be read in words as: every collection of adjacent $n$-cells has a composite, even if the orientations of the cells don't match. This implicitly encodes the _invertibility_ of every cell: if the orientation does not match, we can invert the cell and hence its orientation and then compose.

From this perspective one observes, by looking closely at the combinatorics, that the invertibility of the 1-cells in the simplicial set is enforced particularly by the condition that the [[horn|outer horns] $\Lambda^0[n]$ and $\Lambda^n[n]$ have fillers.

Therefore in a [[simplicial set]] in which _only the inner horns_ $\Lambda^k[n]$ for $0 \lt k \lt n$ have fillers all cells are required to have a kind of inverse, except the 1-cells. (They may have inverses, too, but are not reuqired to).

This is evidently a realization of the idea of an [[(n,r)-category]] with $n = \infty$ and $r = 1$.


Such a simplicial set with fillers for all inner horns

* Boardman-Vogt called a _weak Kan complex_ ; 

* [[Andre Joyal]] called a [[quasi-category]];

* [[Jacob Lurie]] called an $\infty$-category.
 
Being just [[simplicial set]]s with extra property, there are evident and simple definitions of

Here we follow Joyal when we mean concretely the simplicial sets with extra property, and use the term $(\infty,1)$-category for this or any of its equivalent models, discussed below, in order to distinguish from the term [[infinity-category]] that is in large circles understood to generically mean an $\infty$-category with no conditions on invertibility, i.e. an $(\infty,\infty)$-category.

Being just simplicial sets with extra property, there are evident and simple definitions for

* [[quasi-category of (infinity,1)-functors|(infinity,1)-category of (infinity,1)-functors]] between two [[quasi-category|quasi-categories]] $C$ and $D$;

* [[quasi-category of all quasi-categories|(infinity,1)-category of (infinity,1)-categories]].

Similarly, as [[Andre Joyal]] and [[Jacob Lurie]] have shown, all other constructions in [[category theory]] have good generalizations to quasi-categories, which usually have conceptually simple formulations: see the list of keywords at [[Higher Topos Theory]].

...

By definition, the [[model category]] of $(\infty,1)$-categories is one which is [[Quillen equivalence|Quillen equivalent]] to any one of

 * [[quasi-category|quasi-categories]];

 * [[simplicially enriched category|simplicially enriched categories]];

 * [[Segal category|Segal categories]];

 * [[complete Segal space]]s;


#References#

A comparison of the four [[model category]] structures of these four models is in

* Julia E. Bergner, _A survey of $(\infty,1)$-categories_ ([arXiv](http://arxiv.org/abs/math/0610239))

A comprehensive discussion of the theory of $(\infty,1)$-categories in terms of the models [[quasi-category]] and [[simplicially enriched category]] is

* [[Jacob Lurie]], [[Higher Topos Theory]].

More discussion of the other two models can be found at

* [[Jacob Lurie]], _On the classification of topological field theories_ ([pdf](http://www-math.mit.edu/~lurie/papers/cobordism.pdf)).