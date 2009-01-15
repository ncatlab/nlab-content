#The idea

According to the [usual definition](http://en.wikipedia.org/wiki/Partially_ordered_set), a partially ordered set, or 'poset' for short, is a set with a relation $\le$ that is reflexive, transitive and antisymmetric.  

But we can reformulate this definition by creating a category where the objects are the elements of our poset, and where there is a unique morphism $f: x \to y$ whenever $x \le y$.  This lets us think of a poset as a special sort of category.  

When we do this, we are soon led to contemplate a slight generalization of posets: namely [[preorder|preorders]].  The reason is that the antisymmetry law, saying that $x \le y$ and $y \le x$ imply $x = y$, is [[evil]] in a certain technical sense.

#Definition

A **poset** is a category $C$ such that:

* for any pair of objects $x, y$, there is at most one morphism from $x$ to $y$

* if there is a morphism from $x$ to $y$ and a morphism from $y$ to $x$, then $x = y$.

Equivalently, we may define a poset to be a [[skeleton|skeletal]] [[preorder]].

These definitions are both equivalent to the [usual definition](http://en.wikipedia.org/wiki/Partially_ordered_set).

#Intervals#

A (closed bounded) **interval** in a poset $C$ is a set of the form
$$[x,y] = \{r\in C|x\le r\le y\}.$$

A poset is **locally finite** if every closed bounded interval is finite.

#Remarks#

Sometimes it is useful to regard a poset equivalently as a category [[enriched category theory|enriched in]] [[truth value|truth values]].

#References#

* Marco Grandis, _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))
* Tim Porter: _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88 - 100.
* Tim Porter, _Enriched categories and models for spaces of
dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))