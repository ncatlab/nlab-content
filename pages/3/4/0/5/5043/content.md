## Definition

Two diagrams $D,D'$ in $C$ (e.g.: directed systems, sub-posets, ... ) are **cofinal** if they have *equivalent colimits*.  It is *not* said that they are final if they have equivalent *limits* --- the "co"s are not freely mutable, although the dual situation is doubtless just as interesting.

## Examples

* Nonempty subsets of a finite total order are cofinal iff they have the same maximum
* Every infinite subset of $\omega$ is cofinal with $\omega$, as diagrams in $\omega+1$.

## Notes

In most cases where the word "cofinal" is used, it seems to be the case $D'$ is a subdiagram of $D$ in whatever sense of subdiagram appears suitable.  For example, let $D' = DF$, and let $L:D\times (0\to 1) \to C$ be an initial cocone over $D$; it seems natural to ask that $L\circ(F\times(0\to 1))$ be an initial cocone over $D'$.

As defined above, no relation is posited between $D$ and $D'$, and so it seems not too evil to define cofinalness[^1] "a single object is a colimit for both diagrams".

## Abuses

It is often said that two diagrams are cofinal even when neither has a colimit, if they acquire a common colimit on passing to a suitable completion of $C$.  This can probably be phrased internally to $C$, at the cost of intuition.

[^1]: [[cofinality]] is an ordinal invariant of ordinals, which doesn't make sense in the present generality, so we need another name for the adjective.