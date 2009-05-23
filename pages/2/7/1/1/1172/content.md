A __Cauchy space__ is a set $S$ together with a collection of [[filter]]s declared to be __Cauchy filters__.  These must satisfy axioms:
1. Centred: The principal ultrafilter $F_x = \{ A \;|\; x \in A \}$ at $x$ is Cauchy;
1. Isotone: If $F \subseteq G$ and $F$ is Cauchy, then $G$ is Cauchy;
1. Filtered: If $F$ and $G$ are Cauchy, then $F \cap G$ is Cauchy.

That is, the set of Cauchy filters is a filter of filters that contains all principal ultrafilters (sort of a tongue twister).

The morphisms of Cauchy spaces are the Cauchy-continuous functions; a function $f$ between Cauchy spaces is __Cauchy-continuous__ if $f(F)$ is a (base of a) Cauchy filter whenever $F$ is.  In this way, Cauchy spaces form a category $Cau$.

Any [[metric space]] is a Cauchy space: $F$ is Cauchy if it has elements of arbitrarily small diameter.  (In particular, a [[sequence]] is a [[Cauchy sequence]] iff its eventuality filter is Cauchy, and a Cauchy-continuous function between metric spaces is one that maps every Cauchy sequence to a Cauchy sequence.)  In this way, the category of metric spaces becomes a [[subcategory]] (but not a full one) of $Cau$.  (This can be generalised to [[uniform space]]s; the inclusion is still not full.)

Every Cauchy space is a [[convergence space]]; $F \to x$ if the intersection of $F$ with the principal ultrafilter $F_x$ is Cauchy.  Note that any convergent filter must be Cauchy.  Conversely, if every Cauchy filter is convergent, then the Cauchy space is called __complete__.

The set of proper Cauchy filters on a Cauchy space has a natural Cauchy structure which is complete and (as a convergence space) [[Hausdorff space|Hausdorff]]; this is the (Hausdorff) __completion__ of the original Cauchy space.  This completion agrees with the completion of a metric or uniform space; that is, Cauchy completion, even of a metric space, is an operation on its Cauchy structure only.  The complete Cauchy spaces thus form a [[reflective subcategory]] of $Cau$.

A Cauchy space $S$ is __precompact__ (or __totally bounded__) if every proper filter is contained in a Cauchy filter.  Equivalently (assuming the [[ultrafilter theorem]], a weak form of the [[axiom of choice]]), $S$ is precompact iff every ultrafilter is Cauchy.

A Cauchy space is [[compact space|compact]] (as a convergence space) if and only if it is both complete and precompact.  Conversely, it is precompact iff its completion is compact.

# References #

Eva Lowen-Colebunders (1989). Function Classes of Cauchy Continuous Maps. Dekker, New York, 1989.