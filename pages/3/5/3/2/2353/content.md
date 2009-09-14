Recall that the [[graph of a functor]] $f : C \to D$ between [[n-category|n-categories]] is the fibration 
classified by the [[profunctor]] correspondence $\chi_f : C^{op}\times D \to (n-1)Cat$.

But $f$ also determines a morphism $\bar f : I \to n Cat$. The **cograph** of $f$ is the fibration classified by $\bar f$.

# Examples #

## cographs of functors between 0-categories ##

In the case that $C, D$ are [[0-category|0-categories]], i.e. [[set]]s, a functor $f : C \to D$
is just a [[function]] between sets. The cograph [[weak pullback]] 

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
functors between [[(infinity,1)-category|(infinity,1)-categories]] discussed
below.

### adjoint functors in terms of cographs ###

As emphasized in the beginning of section 5.2 there, cographs of functors may be used to characterize
[[adjoint functor]]s.

+-- {: .un_prop }
###### Proposition

Two functors $L : C \to D$ and $R : D \to C$ are [[adjoint functor]]s precisely
if they have the same cographs up to the obvious  passage to [[opposite category|opposite categories]]:

$$
  (L \dashv R) \Leftrightarrow 
  (cograph(L) = cograph(R^{op})^{op})
  \,.
$$

=--

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
  Hom_{cograph(R^{op})^{op}(x,y) = 
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

Evidently these categories are equivalent (even equal) precisely if for all $x \in C, y \in D$ we have

$$
  Hom_D(L(x),y) \simeq Hom_C(x,R(y))
  \,.
$$

This is precisely the condition that $L$ and $R$ are [[adjoint functor]]s.

=--




## cographs of functors between $(\infty,1)$-categories ##

This is described in detail in section 5.2.1, _Correspondences and associated functors_,  of

* [[Jacob Lurie]], [[Higher Topos Theory]].