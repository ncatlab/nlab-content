**Cat** is a name for the category of all [[category|categories]].  To avoid set-theoretic problems related to Russell's paradox, it is typical to define **Cat** to be the category with:

* [[small category|small categories]] as [[object|objects]],
* [[functor|functors]] as [[morphism|morphisms]].

We can also use **Cat** to stand for the [[strict 2-category]] with:

* [[small category|small categories]] as [[object|objects]],
* [[functor|functors]] as [[morphism|morphisms]].
* [[natural transformation|natural transformations]] as [[2-morphism|2-morphisms]].

Here, the [[horizontal composition]] of functors is given by their [[Godement product]].

As a $2$-category, $Cat$ could even include (some) [[large category|large categories]] without running into Russell's paradox. More precisely, if $U$ is the [[Grothendieck universe]] such that $\Set$ is the category of all $U$-small sets, then you can define $\Cat$ to be the 2-category of all $U'$-small categories, where $U'$ is some Grothendieck universe containing $U$. That way, you have $\Set \in \Cat$ without contradiction.

category: category