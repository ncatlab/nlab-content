#Idea#

In the context of $V$-[[enriched category theory]], for 
$
  F,G : C \to D
$
two $V$-enriched functors between $V$-enriched categories, the collection of natural transformation from $F$ to $G$ can also be given the structure of an object in $V$, so that the [[functor category]] denoted $[C,D]$ in the enriched context is itself a $V$-enriched category.

#Definition#


For $C$ and $D$ $V$-enriched categories, there is a $V$-enriched category denoted $[C,D]$ whose

* objects are the $V$-functors $F : C \to D$

* hom-objects $[C,D](F,G)$ between $V$-functors $F, G$ are given by the [[end]]s
$$
  [C,D](F,G) := \int_{c \in C} D(F(c), G(c))
  \,.
$$

#References#

See [section 2.2 p. 29](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf#page=29)
of the standard

* Kelly, _Basic concepts of enriched category theory_ ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))