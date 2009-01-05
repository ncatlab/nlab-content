**Cat** is a name for the category of all [[category|categories]].  To avoid set-theoretic problems related to Russell's paradox, it is typical to define **Cat** to be the category with:

* [[small category|small categories]] as [[object|objects]],
* [[functor|functors]] as [[morphism|morphisms]].

We can also use **Cat** to stand for the [[strict 2-category]] with:

* [[small category|small categories]] as [[object|objects]],
* [[functor|functors]] as [[morphism|morphisms]].
* [[natural transformation|natural transformations]] as [[2-morphism|2-morphisms]].

Here we could even allow some categories that are not small, without running into Russell's paradox. More precisely, if $U$ is the [[Grothendieck universe]] such that $\Set$ is the category of all $U$-small sets, then you can define $\Cat$ to be the 2-category of all $U'$-small categories, where $U'$ is some Grothendieck universe containing $U$. That way, you have $\Set \in \Cat$ without contradiction.

# Generalisation

[This should probably be moved to $n$-[[n-category|category]].]

If one assumes the [Axiom of Universes](http://en.wikipedia.org/wiki/Universe_%28mathematics%29#In_category_theory), there is a sequence of [Grothendieck universes](http://en.wikipedia.org/wiki/Grothendieck_universe)
$$U_0 \subset U_1 \subset U_2 \subset \cdots$$
and we can say a set is **$U_i$-small** if it is an element of $U_i$.  This allows us to make the following definitions:

* $\Set$ is the category of all $U_0$-small sets;
* $\Cat$ is the 2-category of all $U_1$-small categories;
* $2\Cat$ is the 3-category of all $U_2$-small 2-categories;
* etc.

This is a convenient way to settle size questions once and for all for finite $n$, but it doesn\'t really work for $\infty$-categories.

For more, see the discussion at [sci.logic](http://groups.google.com/group/sci.logic/browse_thread/thread/6891c85c2d9b2caf).

category: category