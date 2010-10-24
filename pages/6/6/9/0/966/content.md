
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
Here the limit is taken over the [[comma category]] $(c/G)$ whose objects are pairs $(d,f:c\to G d)$ and whose morphisms are arrows $d\to d'$ in $D$ making the obvious tringle commute in $C$.  Now for any $d$ there is an obvious projection $F G d = \lim_{G d \to G d'} d' \to d$, while because $G$ preserves limits, we have $G F c = \lim_{c\to G d} G d$ and so there is an obvious map $c\to G F c$.  It is easy to check that these are the unit and counit of an [[adjunction]] $F\dashv G$.

The problem with this argument is, of course, that in general the comma category $(c/G)$ may not be [[small category|small]], while it is usually only reasonable to assume that $D$ has _small_ limits, not limits of diagrams whose size is on the order of $(c/G)$ or $D$.  Even if we pass to a universe in which $(c/G)$ is considered small, a classical theorem of Freyd says that 

+-- {: .un_theorem}
###### Theorem

If (in some universe $U$) a $U$-small [[category]] $D$ has [[product]]s of families of objects whose size is at least that of its set of morphisms, then $D$ is a [[preorder]].  

In other words: any [[small category|U-small]] [[complete category|U-small-complete category]] is a [[preorder]].  

=--

+-- {: .proof}
######Proof
Let $x$, $y$ be any two objects, and suppose (contrary to $D$ being a preorder) that there are two morphisms $f, g: x \stackrel{\to}{\to} y$. Then the set of morphisms 

$$x \to \prod_{f \in Mor(D)} y$$ 

has cardinality $2^{|Mor(D)|} \gt |Mor(D)|$, which is a contradiction. 
=-- 

Thus, the argument we gave above is necessarily an **adjoint functor theorem for preorders**: 

+-- {: .un_theorem}
###### Theorem

If $G:D\to C$ is any functor between (small) preorders such that $D$ has, and $G$ preserves, all small [[meet]]s, then $G$ has a left adjoint.

=--

To obtain adjoint functor theorems for categories that are not preorders, one must impose various additional "size conditions" on the category $D$ and/or the functor $G$.  

+-- {: .un_theorem}
###### Theorem

Sufficient conditions for a limit-preserving functor $G : D \to C$ to be a [[right adjoint]] include:

* $D$ is [[complete category|complete]] and [[locally small category|locally small]], and $G$ satisfies the [[solution set condition]].  

  This is Freyd's original version, sometimes called the "**General Adjoint Functor Theorem**".

* $D$ is complete, locally small [[well-powered category|well-powered]], and has a [[small set|small]] [[cogenerating set]], and $C$ is [[locally small category|locally small]].  

  This is sometimes called the "**Special Adjoint Functor Theorem**".

* $D$ is [[total category|cototal]] and $C$ is locally small.

=--

In the first two cases, which work by replacing large limits by small ones, it suffices to assume that $G$ preserves small limits (that it preserves all limits will follow).  The third case works by assuming that $D$ has, while not all large limits, enough so that the theorem goes through; thus is this case $G$ must be already known to preserve [[large category|large]] limits as well.


+-- {: .proof}
###### Proof

Here is a proof that a functor $R : C \to D$ out of a [[locally small category]] $C$ with all small limits has a left adjoint if it preserves these [[limit]]s and satisfies the [[solution set condition]]. 

From the discussion at <a href="http://ncatlab.org/nlab/show/adjoint%20functor#UniversalArrows">adjoint functors -- In terms of universal arrows</a> we have that the existence of the adjoint is equivalent to the existence for each $d \in D$ of an [[initial object]] $i_d : d \to R L d$ in the [[comma category]] $(d \downarrow R)$: an object such that for each $f : d' \to R d$ there is a unique $\tilde f$ such that 

$$
  \array{
    && d 
    \\
    & {}^{\mathllap{i_d}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R L d &&\underset{R \tilde f}{\to}&& R d'
    \\
    \\
    L d &&\underset{\tilde f}{\to}&& d'
  }
$$

commutes. Now an initial object is the limit of the identity functor, but this is generally a large limit; we replace this with some small limit conditions that guarantee existence of an initial object. 

1. Let $Y$ be a category. Call a small family of objects $F$ _weakly initial_ if for every object $y$ of $Y$ there exists $x \in F$ and a morphism $f: x \to y$. 

1. Suppose $Y$ has small products. If $F$ is a weakly initial family, then $\prod_{x \in F} x$ is a [[weak multilimit|weakly initial]] object. 

1. **Claim:** Suppose $Y$ is locally small and small complete. If $x$ is a weakly initial object, then the domain $e$ of the joint equalizer $i: e \to x$ of all arrows $x \to x$ is an initial object. **Proof:** clearly $e$ is weakly initial. Suppose given an object $y$ and arrows $f, g: e \to y$; we must show $f = g$. Let $j: d \to e$ be the equalizer of $f$ and $g$. There exists an arrow $k: x \to d$. The arrow $i: e \to x$ equalizes $1_x$ and $i j k: x \to x$, so $i j k i = i$. Since $i$ is monic, $j (k i) = 1_e$. Thus $j$ is an epi, and $f = g$ follows. 

If $C$ is locally small and small-complete and $R: C \to D$ preserves limits, then $d \downarrow R$ is locally small and small-complete for every object $d$ of $D$. 

If in addition each $d \downarrow R$ has a weakly initial family (solution set condition), then by 2. and 3. each $d \downarrow R$ has an initial object. This restates the condition that $R$ has a left adjoint.

=--


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

## Related concepts

* **adjoint functor theorem**

* [[adjoint (∞,1)-functor theorem]]



## References

A brief introductory discussion is around [theorem 5.4](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf#page=54) of

* [[Jaap van Oosten]], _Basic category theory_ ([pdf](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf))

A detailed expository survey is

* Oliver Kullmann, _The adjoint functor theorem_ ([pdf slides](http://www.cs.swan.ac.uk/~csoliver/Hauptseminar/Quellen/200702Swansea_b.pdf))

The adjoint functor theorem in context with [[Yoneda embedding]] is discussed in 

* Friedrich Ulmer, _The adjoint functor theorem and the Yoneda embedding_  Illinois J. Math. Volume 15, Issue 3 (1971), 355-361. ([web](http://projecteuclid.org/euclid.ijm/1256052605))

[[!redirects adjoint functor theorem]]