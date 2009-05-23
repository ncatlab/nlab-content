A __Cauchy space__ is a set $S$ together with a collection of [[filter]]s declared to be __Cauchy filters__.  These must satisfy axioms:
1. If $F \subseteq G$, $F$ is Cauchy, and $G$ is proper, then $G$ is Cauchy;
1. Every principal ultrafilter is Cauchy;
1. If $F$ and $G$ are Cauchy and $F \cap G$ is proper, then $F \cap G$ is Cauchy;
1. Every Cauchy filter is proper.

The set of Cauchy filters is almost a filter of subsets of the set of proper filters (sort of a tongue twister), except that $F \cap G$ need not contain a Cauchy filter if it\'s not proper.

The morphisms of Cauchy spaces are the Cauchy functions; a function $f$ between Cauchy spaces is __Cauchy__ if $f(F)$ is Cauchy whenever $F$ is.  In this way, Cauchy spaces form a category $Cauchy$.

Any [[metric space]] is a Cauchy space: $F$ is Cauchy if it has elements of arbitrarily small diameter.  (In particular, a [[sequence]] is a [[Cauchy sequence]] iff its eventuality filter is Cauchy.)  In this way, the category of metric spaces becomes a [[subcategory]] (but not a full one) of $Cauchy$.  (This can be generalised to [[uniform space]]s; the inclusion is still not full.)

Every Cauchy space is a [[convergence space]]; $F \to x$ if the intersection of $F$ with the principal ultrafilter $F_x$ is Cauchy.  Note that any convergent proper filter must be Cauchy.  Conversely, if every Cauchy filter is convergent, then the Cauchy space is called __complete__.

A Cauchy space $S$ is __totally bounded__ (or __precompact__) if every proper filter is contained in a Cauchy filter.  Equivalently (assuming the [[ultrafilter theorem]], a weak form of the [[axiom of choice]]), $S$ is totally bounded iff every ultrafilter is Cauchy.

A Cauchy space is [[compact space|compact]] (as a convergence space) if and only if it is both complete and totally bounded.

# References #

Eva Lowen-Colebunders (1989). Function Classes of Cauchy Continuous Maps. Dekker, New York, 1989.