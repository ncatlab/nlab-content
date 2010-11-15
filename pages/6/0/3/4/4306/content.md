
* This page is about functors between linear categories.  For other notions of "linear functor," see [[Goodwillie calculus]] and [[polynomial functor]].

***

A [[linear category]] is a category [[enriched category|enriched]] over [[Vect]], and similarly a **linear functor** is a [[functor]] enriched over $Vect$.  Unwrapping this a bit: given objects $x, y$ in a linear category $C$, the homset $hom(x,y)$ is equipped with the structure of a [[vector space]], and a functor $F: C \to D$ between linear categories is said to be **linear** if the map

$$ F: hom(x,y) \to hom(F(x), F(y)) $$

is linear for all $x,y \in C$.

Note that a linear functor between linear [[additive categories]] is automatically [[additive functor|additive]].
