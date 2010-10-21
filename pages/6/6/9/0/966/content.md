
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

_Adjoint functor theorems_ are theorems stating that under certain conditions a [[functor]] that preserves [[limit]] is a [[right adjoint]], and that a functor that preserves [[colimit]]s is a [[left adjoint]].

## Statement

A basic result of [[category theory]] is that [[adjoint functor|right adjoints]] preserve all [[limit]]s that exist in their domain, and dually left adjoints preserve all [[colimit]]s.  An **[[adjoint functor]] theorem** is a statement that (under certain conditions) the converse holds: a functor which preserves limits is a right adjoint.

The basic idea of an adjoint functor theorem is very simple.  Given a functor $G:D\to C$ which preserves limits, for $c\in C$ define $F c$ to be the limit
$$F c = \lim_{c\to G d} d.$$
Here the limit is taken over the [[comma category]] $(c/G)$ whose objects are pairs $(d,f:c\to G d)$ and whose morphisms are arrows $d\to d'$ in $D$ making the obvious tringle commute in $C$.  Now for any $d$ there is an obvious projection $F G c = \lim_{G c \to G d} d \to d$, while because $G$ preserves limits, we have $G F c = \lim_{c\to G d} G d$ and so there is an obvious map $c\to G F c$.  It is easy to check that these are the unit and counit of an [[adjunction]] $F\dashv G$.

The problem with this argument is, of course, that in general the comma category $(c/G)$ may not be [[small category|small]], while it is usually only reasonable to assume that $D$ has _small_ limits.  In fact, a classical theorem of Freyd says that 

+-- {: .un_theorem}
###### Theorem

If the [[category]] $D$ has [[limit]]s of the size of its set of objects (and $(c/G)$ is usually this large), then it is a [[preorder]].  

In other words: any [[small category|small]] [[complete category]] is a [[preorder]].  

=--

Thus, at least we have a **adjoint functor theorem for posets**: 

+-- {: .un_theorem}
###### Theorem

If $G:D\to C$ is any functor between (small) preorders such that $D$ has, and $G$ preserves, all small [[join]]s, then $G$ has a left adjoint.

=--

To obtain adjoint functor theorems for categories that are not preorders, one must impose various additional "size conditions" on the category $D$ and/or the functor $G$.  

+-- {: .un_theorem}
###### Theorem

Some sufficient conditions for a limit-preseving functor $G : D \to C$ to be a right adjoint include:

* $D$ is [[complete category|complete]] and [[locally small category|locally small]], and $G$ satisfies the [[solution set condition]].  This is Freyd's original version, sometimes called the "General Adjoint Functor Theorem."

* $D$ is complete, locally small [[well-powered category|well-powered]], and has a [[small set|small]] [[cogenerating set]], and $C$ is [[locally small category|locally small]].  This is sometimes called the "Special Adjoint Functor Theorem."

* $D$ is [[total category|cototal]] and $C$ is locally small.

=--

In the first two cases, which work by replacing large limits by small ones, it suffices to assume that $G$ preserves small limits (that it preserves all limits will follow).  The third case works by assuming that $D$ has, while not all large limits, enough so that the theorem goes through; thus is this case $G$ must be already known to preserve [[large category|large]] limits as well.

## Examples {#Examples}

### In presheaf categories {#InPresheafCategories}

It is instructive to spell out the construction of the [[right adjoint]] from a colimit preserving functor $L$ in the simple case where all categories are [[categories of presheaves]]. This is a particularly simple case, but is useful in itself and serves as a template for the general case.

So let now $C$ and $D$ be [[small categories]] and 

$$
  L : PSh(C) \to PSh(D)
$$

a colimit-preserving functor. Then its [[right adjoint]] is given by

$$
  R A  := Hom_{PSh(D)}(L(-),A)
$$

as we shall check in a moment. But first notice that using the [[co-Yoneda lemma]] this may be rewritten as

$$
  \cdots \simeq \int^{c \in C} Hom_{PSh(D)}(L(c), X) \cdot c
$$

where the [[coend]] is equivalently given by the [[colimit]]

$$
  = \lim_{\underset{L c \to A}{\to}} c
  \,.
$$

This is the formula for the would-be right adjoint from the general discussion above, only that here the colimit is only over the representables, hence over a small category.

Now we check that the $R$ thus obtained is indeed right adjoint to $L$, by explicitly checking the hom-isomorphism of the pair of [[adjoint functor]]s:

We compute $Hom_{PSh(D)}(L(X),A)$. In the first step

$$
  Hom_{PSh(D)}(L(X), A)
  \simeq
  Hom_{PSh(D)}(L (\int^{c \in C} X(c) \cdot c), A)
$$

we use the [[co-Yoneda lemma]] for $X$. Then because $L$ preserves colimits this is

$$
  \cdots \simeq Hom_{PSh(D)}(\int^c X(c) \cdot L(c), A)
  \,.
$$

Since the hom preserves limits in both arguments, we can take the [[coend]] out to get an [[end]]

$$
  \cdots \simeq \int_{c \in C} Hom_{PSh(D)}(X(c) \cdot L(c), A)
$$

Then we use the standard [[copower|tensoring]] of our categories over [[Set]] to get

$$
  \cdots \simeq \int_{c \in C} Hom_{Set}(X(c), Hom_{PSh(D)}(L(c),A))
  \,.
$$

And finally this is recognized as the formula for the [[hom-set]] of presheaves (see [[functor category]])

$$
  \cdots \simeq Hom_{PSh(C)}(X, Hom(L(-),A)) = Hom_{PSh(C)}(X, R A)
  \,.
$$

In total this establishes the hom-isomorphism

$$
  Hom_{PSh(D)}(L(X), A) \simeq Hom_{PSh(C)}(X, R(A))
  \,.
$$

## In higher category theory

### For (∞,1)-categories

[[Jacob Lurie]] proved an adjoint functor theorem for (∞,1)-categories (see section 5.5 of [[Higher Topos Theory]]:

A functor between [[presentable (infinity,1)-category|presentable (∞,1)-categories]] has a [[right adjoint]] if and only if it preserves small [[colimit]]s, and has a [[left adjoint]] if and only if it is [[accessible (infinity,1)-category|accessible]] and preserves small [[limit]]s.



* [[adjoint (infinity,1)-functor theorem]]



## References

A detailed expository survey is

* Oliver Kullmann, _The adjoint functor theorem_ ([pdf slides](http://www.cs.swan.ac.uk/~csoliver/Hauptseminar/Quellen/200702Swansea_b.pdf))

The adjoint functor theorem in context with [[Yoneda embedding]] is discussed in 

* Friedrich Ulmer, _The adjoint functor theorem and the Yoneda embedding_  Illinois J. Math. Volume 15, Issue 3 (1971), 355-361. ([web](http://projecteuclid.org/euclid.ijm/1256052605))

[[!redirects adjoint functor theorem]]