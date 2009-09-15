<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


# Idea #

A _partial order_ on a set is a way of ordering its elements to say that some elements precede others, but allowing for the possibility that two elements may be incomparable without being the same.


# Definitions #

## As a set with [[extra structure]]

Given a [[set]] $S$, a __partial order__ on $S$ is a (binary) [[relation]] $\leq$ with the following properties:
* [[reflexive relation|reflexivity]]: $x \leq x$ always;
* [[transitive relation|transitivity]]: if $x \leq y \leq z$, then $x \leq z$;
* [[antisymmetric relation|antisymmetry]]: if $x \leq y \leq x$, then $x = y$.

A __poset__ is a set equipped with a partial order.


## As a category with [[extra properties]] #

A __poset__ is a [[category]] such that:

* for any pair of objects $x, y$, there is at most one morphism from $x$ to $y$
* if there is a morphism from $x$ to $y$ and a morphism from $y$ to $x$, then $x = y$.

Equivalently, we may define a poset to be a [[skeleton|skeletal category]] [[enriched category|enriched over]] the [[cartesian monoidal category]] of [[truth values]].

When we do this, we are soon led to contemplate a slight generalization of partial orders: namely [[preorder|preorders]].  The reason is that the antisymmetry law, saying that $x \le y$ and $y \le x$ imply $x = y$, is [[evil]] in a certain sense.  (On the other hand, it is not evil if taken as a *definition* of [[equality]].)


## Monotone functions

The morphisms of partially ordered sets are [[monotone functions]]; a __monotone function__ $f$ from a poset $S$ to a poset $T$ is a [[function]] from $S$ to $T$ (seen as seen as structured sets) that preserves $\leq$:
$$ x \leq y \;\Rightarrow\; f(x) \leq f(y) .$$
Equivalently, it is a [[functor]] from $S$ to $T$ (seen as certain categories).

In this way, posets form a [[category]] [[Pos]].


#Intervals#

A (closed bounded) **[[interval]]** in a poset $C$ is a set of the form
$$[x,y] = \{r\in C|x\le r\le y\}.$$

A poset is **[[locally finite poset|locally finite]]** if every closed bounded interval is finite.


#Kinds of posets

A poset with a [[top element]] and [[bottom element]] is called __bounded__.  (But note that a *subset* of a poset may be bounded without being a bounded poset itself.)

A poset with all [[meets]] and [[joins]] is called a __[[lattice]]__; if it has only one or the other, it is still a __[[semilattice]]__.

A poset in which every finite set has an upper bound (but perhaps not a *least* upper bound, that is a join) is a __[[directed set]]__.

As remarked above, a poset in which each interval $[x,y]$ is a [[finite set]] is called __locally finite__ or a __[[causet]]__.


# Higher versions

See [[n-poset]].


#References#

* Marco Grandis, _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))
* Tim Porter: _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88--100.
* Tim Porter, _Enriched categories and models for spaces of
dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))


[[!redirects partially ordered]]
[[!redirects partially ordered set]]
[[!redirects partially ordered sets]]
[[!redirects poset]]
[[!redirects posets]]
[[!redirects partial orders]]
[[!redirects partially-ordered]]
[[!redirects partially-ordered set]]
[[!redirects partially-ordered sets]]
[[!redirects bounded poset]]