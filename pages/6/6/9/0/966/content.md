<div class="rightHandSide toc">
[[!include category theory - contents]]
</div>


A basic result of [[category theory]] is that [[adjoint functor|right adjoints]] preserve all [[limit]]s that exist in their domain, and dually left adjoints preserve all [[colimit]]s.  An **adjoint functor theorem** is a statement that (under certain conditions) the converse holds: a functor which preserves limits is a right adjoint.

The basic idea of an adjoint functor theorem is very simple.  Given a functor $G:D\to C$ which preserves limits, for $c\in C$ define $F c$ to be the limit
$$F c = \lim_{c\to G d} d.$$
Here the limit is taken over the [[comma category]] $(c/G)$ whose objects are pairs $(d,f:c\to G d)$ and whose morphisms are arrows $d\to d'$ in $D$ making the obvious tringle commute in $C$.  Now for any $d$ there is an obvious projection $F G d = \lim_{G d \to G d} d \to d$, while because $G$ preserves limits, we have $G F c = \lim_{c\to G d} G d$ and so there is an obvious map $c\to G F c$.  It is easy to check that these are the unit and counit of an adjunction $F\dashv G$.

The problem with this argument is, of course, that in general the comma category $(c/G)$ may not be [[small category|small]], while it is usually only reasonable to assume that $D$ has _small_ limits.  In fact, a classical theorem of Freyd says that if $D$ has limits of the size of its set of objects (and $(c/G)$ is usually this large), then it is a [[preorder]].  Another way to say this is that any small [[complete category]] is a preorder.  Thus, at least we have a **adjoint functor theorem for posets**: If $G:D\to C$ is any functor between (small) preorders such that $D$ has, and $G$ preserves, all small [[join]]s, then $G$ has a left adjoint.

To obtain adjoint functor theorems for categories that are not preorders, one must impose various additional "size conditions" on the category $D$ and/or the functor $G$.  Some sufficient conditions include:

* $D$ is [[complete category|complete]] and [[locally small category|locally small]], and $G$ satisfies the [[solution set condition]].  This is Freyd's original version, sometimes called the "General Adjoint Functor Theorem."
* $D$ is complete, locally small [[well-powered category|well-powered]], and has a small [[generating set|cogenerating set]], and $C$ is locally small.  This is sometimes called the "Special Adjoint Functor Theorem."
* $D$ is [[total category|cototal]] and $C$ is locally small.

In the first two cases, which work by replacing large limits by small ones, it suffices to assume that $G$ preserves small limits (that it preserves all limits will follow).  The third case works by assuming that $D$ has, while not all large limits, enough so that the theorem goes through; thus is this case $G$ must be already known to preserve [[large category|large]] limits as well.

## Version for (∞,1)-categories

[[Jacob Lurie]] proved an adjoint functor theorem for (∞,1)-categories (see section 5.5 of [[Higher Topos Theory]]:

A functor between [[presentable (infinity,1)-category|presentable (∞,1)-categories]] has a [[right adjoint]] if and only if it preserves small [[colimit]]s, and has a [[left adjoint]] if and only if it is [[accessible (infinity,1)-category|accessible]] and preserves small [[limit]]s.