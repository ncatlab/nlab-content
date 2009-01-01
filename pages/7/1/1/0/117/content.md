#Idea

According to the [usual definition](http://en.wikipedia.org/wiki/Partially_ordered_set), a partially ordered set, or 'poset' for short, is a set with a relation $\le$ that is reflexive, transitive and antisymmetric.  

But, we can reformulate this definition by creating a category where the objects are the elements of our poset, and where there is a unique morphism $f: x \to y$ whenever $x \le y$.  This lets us think of a poset as a special sort of category.  

When we do this, we are soon led to contemplate a slight generalization of posets: namely [[preorder|preorders]].

#Definition

A _poset_ is a category such that:

* for any pair of objects $x, y$, there is at most one morphism from $x$ to $y$

* if there is a morphism from $x$ to $y$ and a morphism from $y$ to $x$, then $x = y$.

Equivalently, we may define a poset to be a [[skeleton|skeletal]] [[preorder]].

These definitions are both equivalent to the [usual definition](http://en.wikipedia.org/wiki/Partially_ordered_set).

#Remarks#

Sometimes it is useful to regard a poset equivalently as a category [[enriched category theory|enriched in]] [[(-1)-category|(-1)-categories]].