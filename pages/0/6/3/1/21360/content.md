## Idea

A complete spread over a [[locale]] $X$ is a [[map of locales]] $L\to X$
that is in the same relation to an [[etale map]] of [[locales]] $L\to X$
as a [[cosheaf]] of sets over $X$ is to a [[sheaf]] of sets over $X$.

## Definition

The original definition of complete spreads
is due to R. H. Fox in 1957 and is slightly different
from the definition for [[locales]] presented below.

A __spread__ over a [[locale]] $X$ is a [[locally connected locale]] $L$
together with a [[map of locales]] $l\colon L\to X$
such that the connected components of opens $l^*U$ for all opens $U$ in $X$
form a [[base]] for the [[locale]] $L$.

See Proposition 4.3 in \cite{Funk} for other equivalent
characterizations of spreads.

Recall that the [[category of elements]]
of the [[cosheaf of connected components]] of $l\colon L\to X$
has as objects pairs $(U,c)$, where $U$ is an open in $X$
and $c$ is a connected component of the open $l^*U$ in $L$.

A __complete spread__ over a [[locale]] $X$ is a spread $l\colon L\to X$
such that the [[unit]] of the adjunction between
[[locally connected locales]] over $X$ and [[cosheaves]] of sets over $X$
given by the [[display locale]] functor and the [[cosheaf of connected components]] functor is an isomorphism.

## Properties

Complete spreads form precisely the [[essential image]]
of the [[display locale]] functor,
which therefore becomes an equivalence
between the category of [[cosheaves]] of sets on a [[locale]] $X$
and the category of [[complete spreads]] over $X$.

The inverse functor is given by the [[cosheaf of connected components]] construction.

## References

* {#Funk} [[Jonathon Funk]], _The display locale of a cosheaf_.

* [[Marta Bunge]], [[Jonathon Funk]], _[[Singular Coverings of Toposes]]_.

[[!redirects spread]]
[[!redirects spreads]]
[[!redirects complete spreads]]