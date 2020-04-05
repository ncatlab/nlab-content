## Idea

A tangle is like a [[knot]] that was cut at several points
and the resulting strands were pulled apart.

## Definition

Tangles form a [[category]].
Its objects are finite [[subsets]] of $\mathbf{R}^2$.
Morphisms $A\to B$ are embeddings
of unions of finitely many closed intervals and circles
into $[0,1]\times\mathbf{R}^2$
such that the restriction of the embedding
to the endpoints yields a bijection to $A\sqcup B$.

Morphisms are composed by gluing two copies of $[0,1]$ together
and rescaling.

As usual, this suffers from being associative only up to an ambient isotopy.
Thus, one can either take ambient isotopy classes of such embeddings,
obtaining a [[1-category]] of tangles,
or instead turn tangles into an [[(∞,1)-category]],
in which case morphisms $A\to B$ will encode
the whole [[homotopy type]] of the space of embeddings described above.