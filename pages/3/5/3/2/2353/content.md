Recall that the [[graph of a functor]] $f : C \to D$ between [[n-category|n-categories]] is the fibration 
classified by the [[profunctor]] correspondence $\chi_f : C^{op}\times D \to (n-1)Cat$. 

+--{.query} 

[[Todd Trimble|Todd]]: I'd start with something more basic: recall that the graph of a function $f: A \to B$ is the [[subset]] determined by the [[monomorphism]] $\langle 1, f \rangle: A \to A \times B$. This makes sense in any category with products. Under one definition, the notion of cograph of a function $f: A \to B$ is the categorically dual notion: it is the [[quotient object|quotient]] determined by the epimorphism $(f, 1): A \sqcup B \to B$. 

A more vivid presentation of cograph is given by the pictures we draw of functions $f: A \to B$: as graphs (in the graph-theoretic sense!) whose vertices are elements in $A \sqcup B$, with an edge drawn from $a$ to $f(a)$ for each $a$ in $A$. This can also be conceived as a [[poset]] $P_f$ with underlying set $A \sqcup B$, in which $a \leq f(a)$ and all other instances of $\leq$ are the reflexive ones. The connected components function $(P_f)_0 \to \pi_0(P_f)$ is then the cograph in the sense given above. 

In this article we give a definition of cograph which generalizes this poset picture of cograph of a function, and which applies to any functor between $n$-categories, following the work of Jacob Lurie...

(Anyway, that's the basic idea; it could be made even more reader-friendly I'm sure.) 

=--

But $f$ also determines a morphism $\bar f : I \to n Cat$. The **cograph** of $f$ is the fibration classified by $\bar f$.

# Examples #

## cographs of functors between 0-categories ##

In the case that $C, D$ are [[0-category|0-categories]], i.e. [[set]]s, a functor $f : C \to D$
is just a [[function]] between sets. The cograph [[2-pullback]] 

$$
  \array{
    cograph(f) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    I &\stackrel{\bar f}{\to}& Set
  }
$$

is computed by the ordinary [[pullback]]

$$
  \array{
    cograph(f) &\to& Set_{*}
    \\
    \downarrow && \downarrow
    \\
    I &\stackrel{\bar f}{\to}& Set
  }
$$

and identifies $cograph(f)$ with the [[category of elements]] of $\bar f$,
as described there: the objects of $cograph(f)$
are the disjoint union of $C$ and $D$: $Obj(cograph(f)) = C \coprod D$
and the nontrivial morphisms are of the form $x \to y$ whenever $x \in C$, $y \in D$
and $f(x) = y$.

What [[Bill Lawvere]] called the [[cograph of a function]] is the connected components
$\pi_0(Cograph(f))$ of this category.


## cographs of functors between 1-categories ##

For $f : C \to D$ an ordinary  [[functor]], 
the full category $cograph(f)$ is what is denoted $C \star^f D$ in section 2.3.1
_Correspondences_ in 

* [[Jacob Lurie]], [[Higher Topos Theory]]

where it is understood as a generalization of the [[join of simplicial sets]]
and where it serves as a motivation for the study of cographs of 
functors between [[(∞,1)-category|(∞,1)-categories]] discussed
below.

### adjoint functors in terms of cographs ###

As emphasized in the beginning of section 5.2 there, cographs of functors may be used to characterize
[[adjoint functor]]s.

+-- {: .un_prop }
###### Proposition

Two functors $L : C \to D$ and $R : D \to C$ are [[adjoint functor]]s precisely if their cographs (modulo the obvious passage to [[opposite categories]]) are isomorphic under $C$ and $D$:

$$
  (L \dashv R) \Leftrightarrow 
  (cograph(L) \cong cograph(R^{op})^{op})
$$

where the isomorphism is in the co-slice category $(C\sqcup D)/Cat$.
=--

More precisely, there is a bijection between adjunctions $L\dashv R$ and isomorphisms as above.

+-- {: .proof}
###### Proof

The category $cograph(L)$ is the category with $Obj(cograph(L)) = Obj(C) \coprod Obj(D)$ and with

$$
  Hom_{cograph(L)}(x,y) = 
  \left\{
    \array{
      Hom_C(x,y) & if x,y \in C
      \\
      Hom_D(x,y) & if x,y \in D
      \\
      Hom_D(L(x),y) & if x \in C ,y \in D
      \\
      \emptyset & if x \in D ,y \in C
    }
  \right.
$$ 

The category $cograph(R^{op})^{op}$ accordingly is the category with $Obj(cograph(R)) = Obj(C) \coprod Obj(D)$ and with

$$
  Hom_{cograph(R^{op})^{op}}(x,y) = 
  \left\{
    \array{
      Hom_C(x,y) & if x,y \in C
      \\
      Hom_D(x,y) & if x,y \in D
      \\
      Hom_C(x,R(y)) & if x \in C ,y \in D
      \\
      \emptyset & if x \in D ,y \in C
    }
  \right.
$$ 

Evidently these categories are isomorphic precisely if for all $x \in C, y \in D$ we have

$$
  Hom_D(L(x),y) \cong Hom_C(x,R(y))
  \,.
$$

Such a natural isomorphism is precisely the structure of an adjunction $L\dashv R$.  (It is natural because the isomorphism is an isomorphism of categories, and the functoriality of $Hom_D(L(-),-)$ and $Hom_C(-,R(-))$ is encoded by composition in the cograph.)

=--

Note that under the identification of [[profunctors]] with *codiscrete cofibrations* in $Cat$, the cograph of a functor is the profunctor associated to it (and the cograph $cograph(R^{op})^{op}$ is the *other* profunctor associated to it).


## cographs of functors between $(\infty,1)$-categories ##

In the context of [[(∞,1)-category]] theory there is a good theory of [[Cartesian fibration]]s $X \to S$ and of their classification by [[(∞,1)-functor]]s $S^{op} \to (\infty,1)Cat$ to the [[(∞,1)-category of (∞,1)-categories]] as described at [[universal fibration of (∞,1)-categories]].

Accordingly, the above notion of cograph of a functor has a direct generalization to [[(∞,1)-functor]]s:

+-- {: .un_defn}
###### Definition

For $f : C \to D$ an [[(∞,1)-functor]], identified with a morphism

$$
  \bar f : I \to (\infty,1)Cat
$$

in the [[(∞,1)-category of (∞,1)-categories]], it **cograph** is the [[Cartesian fibration]] $cograph(f) \to I$ classified by it. In terms of the [[universal fibration of (∞,1)-categories]] this is the [[homotopy pullback]]

$$
  \array{
    cograph(f) &\to& Z^{op}
    \\
    \downarrow && \downarrow
    \\
    I &\stackrel{\bar f}{\to}& (\infty,1)Cat
  }
  \,.
$$

=--


As for every [[Cartesian fibration]] the functor $f : C \to D$ is determined uniquely up to equivalence by its cograph. In general, obtaining the classifying $(\infty,1)$-functor from a given [[Cartesian fibration]] may be difficult. In the special case of cographs as Cartesian fibrations over the simple [[interval category]] it is easier. This is discussed in the following:


...


# References #

The notion of cographs of $(\infty,1)$-functors and the theory of how to re-obtain $(\infty,1)$-functors from their cographs is the content of section 5.2.1, _Correspondences and associated functors_,  of

* [[Jacob Lurie]], [[Higher Topos Theory]] .