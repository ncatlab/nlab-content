
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
* table of contents
{:toc}

The notion of _cograph of a functor_ is dual to that of [[graph of a functor]]: for
$f : C \to D$ a functor between [[n-categories]] is the fibration 
classified by the [[profunctor]] correspondence $\chi_f : C^{op}\times D \to (n-1)Cat$. But $f$ also determines a morphism $\bar f : I \to n Cat$ from the [[interval category]] $I$. The **cograph** of $f$ is the fibration classified by $\bar f$.


Recall that the graph of a function $f: A \to B$ is the [[subset]] determined by the [[monomorphism]] $\langle 1, f \rangle: A \to A \times B$. This makes sense in any category with products. Under one definition, the notion of cograph of a function $f: A \to B$ is the categorically dual notion: it is the [[quotient object|quotient]] determined by the [[epimorphism]] $(f, 1): A \sqcup B \to B$. 

A more vivid presentation of cograph is given by the pictures we draw of functions $f: A \to B$: as [[directed graph]]s (in the graph-theoretic sense!) whose vertices are elements in $A \sqcup B$, with an edge drawn from $a$ to $f(a)$ for each $a$ in $A$. This can also be conceived as a [[poset]] $P_f$ with underlying set $A \sqcup B$, in which $a \leq f(a)$ and all other instances of $\leq$ are the reflexive ones. The connected components function $(P_f)_0 \to \pi_0(P_f)$ is then the cograph in the sense given above. 

In this article we give a definition of cograph which generalizes this poset picture of cograph of a function, and which applies to any functor between $n$-categories.



# Examples #

## Cographs of functors between 0-categories ##

In the case that $C, D$ are [[0-category|0-categories]], i.e. [[sets]], a functor $f : C \to D$
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


## Cographs of functors between 1-categories ##

For $f : C \to D$ an ordinary  [[functor]], $cograph(f)$ is the category with $Obj(cograph(f)) = Obj(C) \coprod Obj(D)$ and with

$$
  Hom_{cograph(f)}(x,y) = 
  \left\{
    \array{
      Hom_C(x,y) & if\; x,y \in C
      \\
      Hom_D(x,y) & if\; x,y \in D
      \\
      Hom_D(f(x),y) & if\; x \in C ,y \in D
      \\
      \emptyset & if\; x \in D ,y \in C
    }
  \right.
$$ 

with composition defined as induced from $C$, from $D$, and from the action of $f$.  This is a special case of the [[cograph of a profunctor]], specialized to the representable [[profunctor]] $D(f-,-)$.

This cograph is denoted $C \star^f D$ in section 2.3.1 (_Correspondences_) in 

* [[Jacob Lurie]], [[Higher Topos Theory]]

where it is understood as a generalization of the [[join of simplicial sets]]
and where it serves as a motivation for the study of cographs of 
functors between [[(∞,1)-category|(∞,1)-categories]] discussed
below.

## Adjoint functors in terms of cographs 
 {#AdjointFunctorsInTermsOfCographs}

As emphasized in the beginning of section 5.2 there, cographs of functors may be used to characterize [[adjoint functors]].  This is just one way of stating the characterization of adjoints in terms of [[profunctors]] (which in turn makes sense in any [[2-category equipped with proarrows]]).

+-- {: .num_prop }
###### Proposition

Two functors $L : C \to D$ and $R : D \to C$ are [[adjoint functors]] precisely if $cograph(L)$ and $cograph(R^{op})^{op}$ are isomorphic under $C$ and $D$:

$$
  (L \dashv R) \Leftrightarrow 
  (cograph(L) \cong cograph(R^{op})^{op})
$$

where the isomorphism is in the [[co-slice category]] $(C\sqcup D)/Cat$.
=--

More precisely, there is a bijection between adjunctions $L\dashv R$ and isomorphisms as above.

+-- {: .proof}
###### Proof

The category $cograph(L)$ is the category with $Obj(cograph(L)) = Obj(C) \coprod Obj(D)$ and with

$$
  Hom_{cograph(L)}(x,y) = 
  \left\{
    \array{
      Hom_C(x,y) & if\; x,y \in C
      \\
      Hom_D(x,y) & if\; x,y \in D
      \\
      Hom_D(L(x),y) & if\; x \in C ,y \in D
      \\
      \emptyset & if\; x \in D ,y \in C
    }
  \right.
$$ 

(This set is also called the set of [[heteromorphisms]] between objects in $C$ and $D$.)

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

Evidently these categories are isomorphic under $C$ and $D$ precisely if for all $x \in C, y \in D$ we have

$$
  Hom_D(L(x),y) \cong Hom_C(x,R(y))
  \,.
$$

naturally in $x$ and $y$.  It is natural because the isomorphism is an isomorphism of categories, and the functoriality of $Hom_D(L(-),-)$ and $Hom_C(-,R(-))$ is encoded by composition in the cograph.  Of course, such a natural isomorphism is precisely the structure of an adjunction $L\dashv R$.

=--

Note also that just as $cograph(L)$ is the cograph of the profunctor $D(L-,-)$, also $cograph(R^{op})^{op}$ is the cograph of the profunctor $C(-,R-)$.  Thus, this theorem can be viewed as one way of stating the characterization of adjunctions in terms of homsets, as can be [formulated](http://ncatlab.org/nlab/show/2-category+equipped+with+proarrows#HomsetAdjn) in terms of profunctors in any 2-category equipped with proarrows.


## Cographs of functors between $(\infty,1)$-categories ##

In the context of [[(∞,1)-category]] theory there is a good theory of [[Cartesian fibrations]] $X \to S$ and of their classification by [[(∞,1)-functors]] $S^{op} \to (\infty,1)Cat$ to the [[(∞,1)-category of (∞,1)-categories]] as described at [[universal fibration of (∞,1)-categories]].

Accordingly, the above notion of cograph of a functor has a direct generalization to [[(∞,1)-functors]]:

+-- {: .num_defn}
###### Definition

For $f : C \to D$ an [[(∞,1)-functor]], identified with a morphism

$$
  \bar f : I \to (\infty,1)Cat
$$

in the [[(∞,1)-category of (∞,1)-categories]], it **cograph** is the [[Cartesian fibration]] $cograph(f) \to I$ classified by it. In terms of the [[universal fibration of (∞,1)-categories]] this is the [[homotopy pullback]]

$$
  \array{
    cograph(f) &\to& S^{op}
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

## Related concepts

* [[graph of a functor]]

* **cograph of a functor**, [[cograph of a profunctor]]

## References 

The notion of cographs of $(\infty,1)$-functors and the theory of how to re-obtain $(\infty,1)$-functors from their cographs is the content of section 5.2.1, _Correspondences and associated functors_,  of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ .