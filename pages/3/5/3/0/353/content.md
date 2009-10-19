[[!redirects $n$-category]]
[[!redirects n-categories]]
[[!redirects weak n-category]]
[[!redirects weak n-categories]]


$n$-categories are the main subject of [[higher category theory]], and give its name to the $n$-[[About|Lab]].

#Idea#

An $n$-category is an [[∞-category]] such that all $(n+1)$-morphisms are [[equivalence]]s, and all parallel pairs of $j$-morphisms are equivalent for $j > n$. (One says that the $\infty$-category is _trivial_ in degree greater than $n$.) This is the same thing as an $(n,n)$-category in the sense of $(n,r)$-[[(n,r)-category|categories]].

Up to equivalence, you may assume that all equivalent pairs of $j$-morphisms for $j > n$ are in fact equal, and many authorities include this as a requirement. On the other hand, you can also write down a definition of $n$-category from scratch (without passing through $\infty$-categories), and then this question never comes up. The point is that you don\'t talk about $j$-morphisms for $j > n$; you stop at $n$-morphisms.

#Examples#

* A $0$-category is a [[set]].

* A $1$-category is an ordinary [[category]].

* A $2$-[[2-category|category]] is (depending on how strict was your initial notion of $\infty$-category) either a [[strict 2-category]] or a [[bicategory]].

One also speaks of $(-1)$-[[(-1)-category|categories]] and $(-2)$-[[(-2)-category|categories]], but these concepts are not as well behaved.

# Categories of $n$-categories #

Just as the collection of all ([[small category|small]]) sets is the prototypical example of a category, so the collection of all small $n$-categories is the prototypical example of an $(n+1)$-category.

Actually, if you define things cleverly, then you can get an $(n+1)$-category of *all* $n$-categories.  If one assumes the [[Grothendieck universe|Axiom of Universes]], then there is a sequence of Grothendieck universes
$$U_0 \subset U_1 \subset U_2 \subset \cdots$$
and we can say a set is **$U_i$-small** if it is an element of $U_i$.  This allows us to make the following definitions:

* $\Set$ is the category of all $U_0$-small sets;
* $\Cat$ is the 2-category of all $U_1$-small categories;
* $2\Cat$ is the 3-category of all $U_2$-small 2-categories;
* etc.

This is a convenient way to settle size questions once and for all for finite $n$, but it doesn\'t really work for $\infty$-categories.

For more, see the discussion at [sci.logic](http://groups.google.com/group/sci.logic/browse_thread/thread/6891c85c2d9b2caf).