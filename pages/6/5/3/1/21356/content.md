## Idea

The category of [[cosheaves]] of sets on a [[locale]] $X$
is equivalent to the category of [[complete spreads]] over $X$.
The equivalence functor sends a [[cosheaf]] $D$ of sets over $X$
to its display locale over $X$.

Thus, the functor described here
plays the same role in the equivalence between
[[cosheaves]] of sets on $X$ and [[complete spreads]] over $X$
as the [[etale locale]] construction
plays in the equivalence between
[[sheaves]] of sets on $X$ and [[etale locales]] over $X$.

## Definition.

The __display locale__ of a [[precosheaf]] $D$ on a [[locale]] $X$
is a locale over $X$ (i.e., an object in the [[slice category]] $Loc/X$)
given by the [[base change]]
of the morphism
$$Alex(elem(D))\to Alex(elem(1_X))$$
(induced by the unique morphism $D\to 1_X$)
along the morphism $X\to Alex(elem(1_X))$.

Here $1_X$ denotes the [[terminal]] [[precosheaf]] on $X$.

The functor $elem\colon Precosheaf(X) \to Poset$
computes the [[category of elements]] of a [[precosheaf]] on $X$.

The functor $Alex\colon Poset \to Locale$
computes the [[Alexandroff locale]] of a poset $P$
by sending it the [[locale]] whose [[frame]]
consists of downward closed subsets of $P$.

The morphism $X\to Alex(elem(1_X))$ has as its underlying
[[morphism of frames]] the map that sends a downward closed subset of $X$
to its [[supremum]].

## Adjunction

The display locale functor
$$Cosheaf(X) \to LocConLoc/X$$
is [[right adjoint]]
to the [[cosheaf of connected components]] functor
$$LocConLoc/X \to Cosheaf(X).$$

(The above adjunction also makes holds for [[precosheaves]]
if we generalize the [[cosheaf of connected components]] construction
accordingly, see Section 2 in Funk \cite{Funk}.)

This adjunction exhibits the category of [[cosheaves]] of sets on $X$
as a (full) [[reflective subcategory]] of [[locally connected locales]] over $X$.
The [[essential image]] of the inclusion is known as the category
of [[complete spreads]] over $X$.

## References

\bibitem{Funk} [[Jonathon Funk]], _The display locale of a cosheaf_.