## Idea ##

A Cauchy space is a generalisation of a [[metric space]] with a bare minimum of structure for the concepts of Cauchy sequence, Cauchy-continuous map, and Cauchy completion to make sense.  Topologically (that is, up to continuous maps), any Cauchy space is a [[convergence space]], but not much more than that.


## Definitions ##

A __Cauchy space__ is a set $S$ together with a collection of [[filter]]s declared to be __Cauchy filters__.  These must satisfy axioms:

1. Centred: The principal ultrafilter $F_x = \{ A \;|\; x \in A \}$ at $x$ is Cauchy;
1. Isotone: If $F \subseteq G$ and $F$ is Cauchy, then $G$ is Cauchy;
1. Filtered: If $F$ and $G$ are Cauchy, then $F \cap G$ is Cauchy.

That is, the set of Cauchy filters is a filter of filters that contains all principal ultrafilters (sort of a tongue twister).  Often one sees a more complicated definition that uses only proper filters, but this simpler definition works if you accept that the improper filter (which is the [[power set]] of $X$) may be Cauchy (in which case it necessarily is).  In any case, the Cauchy structure may be reconstructed from the proper Cauchy filters.


The definition can also be phrased in terms of [[net]]s; a __Cauchy net__ is a net whose eventuality filter is Cauchy.  In particular, a __Cauchy sequence__ is a [[sequence]] whose eventuality filter is Cauchy.


The morphisms of Cauchy spaces are the Cauchy-continuous functions; a function $f$ between Cauchy spaces is __Cauchy-continuous__ if $f(F)$ is a (base of a) Cauchy filter whenever $F$ is.  In this way, Cauchy spaces form a category $Cau$.


## Examples ##

Any [[metric space]] is a Cauchy space: $F$ is a Cauchy filter if it has elements of arbitrarily small diameter.  This reconstructs the usual definitions of Cauchy sequence and Cauchy-continuous map for metric spaces.  (In particular, a map between metric spaces is Cauchy-continuous if it maps every Cauchy sequence to a Cauchy sequence; the result for general nets follows since a metric space is [[sequential space|sequential]].)  The [[forgetful functor]] from $Met$ (metric spaces and short maps) to $Cau$ is [[faithful functor|faithful]] but not [[full functor|full]].


More generally, any [[uniform space]] is a Cauchy space: $F$ is a Cauchy filter if, given any entourage $U$, $A \times A \subseteq U$ for some $A \in F$.  This reconstructs the usual definitions of Cauchy net and Cauchy-continuous map for uniform spaces.  (In general, we need nets rather than just sequences here.)  The [[forgetful functor]] from $Unif$ (uniform spaces and uniformly continuous maps) to $Cau$ is [[faithful functor|faithful]] but still not [[full functor|full]].


## Properties ##

Every Cauchy space is a [[convergence space]]; $F \to x$ if the intersection of $F$ with the principal ultrafilter $F_x$ is Cauchy.  Note that any convergent filter must be Cauchy.  Conversely, if every Cauchy filter is convergent, then the Cauchy space is called __complete__.


The set of proper Cauchy filters on a Cauchy space has a natural Cauchy structure which is complete and (as a convergence space) [[Hausdorff space|Hausdorff]]; this is the (Hausdorff) __completion__ of the original Cauchy space.  The complete Cauchy spaces thus form a [[reflective subcategory]] of $Cau$.  This completion agrees with the completion of a metric or uniform space; that is, Cauchy completion, even of a metric space, is an operation on its Cauchy structure only.


A Cauchy space $S$ is __precompact__ (or __totally bounded__) if every filter is contained in a Cauchy filter.  Equivalently (assuming the [[ultrafilter theorem]], a weak form of the [[axiom of choice]]), $S$ is precompact iff every ultrafilter is Cauchy.  A Cauchy space is [[compact space|compact]] (as a convergence space) if and only if it is both complete and precompact.  Conversely, it is precompact iff its completion is compact.


# References #

Eva Lowen-Colebunders (1989). Function Classes of Cauchy Continuous Maps. Dekker, New York, 1989.