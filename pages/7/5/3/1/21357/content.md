## Idea

The [[display locale]] construction defines a fully faithful functor
from [[cosheaves]] of sets on a [[locale]] $X$
to the [[slice category]] $Loc/X$ of [[locales]] over $X$.

The construction in this article describes a functor
in the opposite direction that yields
the inverse of the above functor
once restricted to the appropriate subcategory.

Thus, the functor described here
plays the same role in the equivalence between
[[cosheaves]] of sets on $X$ and [[complete spreads]] over $X$
as the sheaf of sections construction
plays in the equivalence between
[[sheaves]] of sets on $X$ and [[etale locales]] over $X$.

## Definition

Suppose $l\colon L\to X$ is a [[map of locales]],
where $L$ is a [[locally connected locale]].
Define a [[precosheaf]] $\lambda_l$ on $X$ as follows.
Send an open $U$ in $X$ to the set of [[connected components]]
of $l^* U$, which is a [[locally connected locale]] because so is $L$.
Send an inclusion of opens to the induced map on the sets of [[connected components]].

\begin{proposition}
(Funk, Proposition 2.1.)
This [[precosheaf]] is a [[cosheaf]].
\end{proposition}

## Related notions

* [[display locale]]

* [[cosheaf]]

## References

* [[Jonathon Funk]], _The display locale of a cosheaf_.