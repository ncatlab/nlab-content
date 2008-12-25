_Cat_ is a name for the category of all [[category|categories]].  To avoid set-theoretic problems related to Russell's paradox, it is typical to define _Cat_ to be the category with:

* [[small category|small categories]] as [[object|objects]],

* [[functor|functors]] as [[morphism|morphisms]].

We can also use _Cat_ to stand for the [[strict 2-category]] with:

* small categories as objects,

* functors as morphisms,

* [[natural transformation|natural transformations]] as [[2-morphism|2-morphisms]].

Here we could even allow [[large category|large categories]] without running into Russell's paradox.

+--{.query}
Mike Shulman asks: Do you have a precise mathematical meaning in mind for that last sentence?  Certainly, in ordinary ZF set theory, there is no 2-category of large categories, since a proper class cannot be an element of another proper class.  On the other hand, if we assume a universe, then we can have a (very large) 2-category of large categories, but we can also have a very large 1-category of large categories.

Toby Bartels replies: I think that the point is that one *can* define things this way, using a sequence $U_0 \subset U_1 \subset U_2 \subset \cdots$ of universes:
* $\Set$ is the category of all $U_0$-small sets;
* $\Cat$ is the 2-category of all $U_1$-small categories;
* $2\Cat$ is the 3-category of all $U_2$-small 2-categories;
* etc.

Of course, this is just one way to do things. I\'ve liked it since 1997 (&lt;http://groups.google.com/group/sci.logic/browse_thread/thread/6891c85c2d9b2caf>), and it\'s a convenient way to settle size questions once and for all for finite $n$. But it doesn\'t really work for $\infty$-categories.
=--

category: category