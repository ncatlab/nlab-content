#Idea#

In the context of $V$-[[enriched category theory]], for 
$
  F,G : C \to D
$
two $V$-[[enriched functor]]s between $V$-[[enriched category|enriched categories]], the collection of [[natural transformation]]s from $F$ to $G$ can also be given the structure of an object in $V$, so that the [[functor category]], denoted $[C,D]$ in the enriched context, is itself a $V$-enriched category.


#Definition#

For $C$ and $D$ $V$-enriched categories, there is a $V$-[[enriched category]] denoted $[C,D]$ whose

* objects are the $V$-functors $F : C \to D$

* hom-objects $[C,D](F,G)$ between $V$-functors $F, G$ are given by the $V$-enriched [[end]]
$$
  [C,D](F,G) := \int_{c \in C} D(F(c), G(c))
$$

over the functor
$$
  D(F(-),G(-)) : C^{op} \otimes C \to V
  \,.
$$

+-- {: .un_prop}
######Proposition

For $V = $[[Set]], so that $V$-enriched categories are just ordinary [[locally small category|locally small categories]], the $V$-enriched functor category coincides with the ordinary [[functor category]]. (See the examples below.)
=--

#Examples#

## ordinary functor categories ##

To understand the role of the [[end]] here, it is useful to spell this out for the case where $V =$ [[Set]], where we are dealing with ordinary [[locally small category|locally small]] categories.

So let $V = Set$ where set is equipped with its [[cartesian monoidal category|cartesian monoidal structure]].

Recall the definition of the [[end]] over

$$
  D(F(-),G(-)) : C^{op} \otimes C \to Set
$$

as an [[equalizer]]: it is the universal subobject 

$$
  \int_{c \in C} D(F(c), G(c))
  \hookrightarrow
  \prod_{c \in Obj(C)} D(F(c), G(c))
$$

of the product of all [[hom-set]]s in $D$ between the images of objects in $C$ under the functors $F$ and $G$. So one element $ \eta \in \int_{c \in C} D(F(c), G(c))$ is a collection of morphisms

$$
  ( F(c) \stackrel{\eta_c}{\to} G(c))_{c \in Obj(c)}
$$

such that the "left and right [[action]]" (in the sense of [[distributor]]s) of $D(F(-),G(-))$ on these elements coincides. Unwrapping what this action is (see the details at [[end]]) one find that 

* the "right [[action]]" by a morphism $c \stackrel{f}{\to} d$ is the postcomposition $
  (F(c) \stackrel{\eta_c}{\to} G(c)) \mapsto
  (F(c) \stackrel{\eta_c}{\to} G(c) \stackrel{G(f)}{\to} G(d))
$

* the "left [[action]]" by a morphism $c \stackrel{f}{\to} d$ is the precomposition $
  (F(d) \stackrel{\eta_d}{\to} G(d)) \mapsto
  (F(c) \stackrel{F(f)}{\to} F(d) \stackrel{\eta_d}{\to} G(d) )
$.

So the invariants under the combined action are those $eta$ for which for all $f : c \to d$ in $C$ the diagram
$$
  \array{
    F(c) &\stackrel{\eta_c}{\to} & G(c)
    \\
    \downarrow^{F(f)}
    &&
    \downarrow^{G(f)}
    \\
    F(d) &\stackrel{\eta_d}{\to} & G(d)
  }
$$

commutes. Evidently, this means that the elements $\eta$ of the [[end]] $\int_{c \in C} D(F(c), G(c))$ are precisely the [[natural transformation]]s between $F$ and $G$.


#References#

See [section 2.2 p. 29](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf#page=29)
of the standard

* Kelly, _Basic concepts of enriched category theory_ ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))