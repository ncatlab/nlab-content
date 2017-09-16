A _filter_ is [[duality|dual]] to an [[ideal]].

# Definitions

A subset $F$ of a [[poset]] $L$ is called a __filter__ if it is upward-closed and downward-[[direction|directed]]; that is:
1. If $A \leq B$ in $L$ and $A \in F$, then $B \in F$;
1. for some $A$ in $L$, $A \in F$;
1. if $A \in F$ and $B \in F$, then for some $C \in F$, $C \leq A$ and $C \leq B$.

Somtimes the term 'filter' is used for an [[upper set]], that is any set satisfying axiom (1).  (Ultimately this connects with the use of 'ideal' in [[monoid]] theory.)

In a [[lattice]], one can use these alternative axioms:
1. If $A \in F$ and $B$ in $L$, then $A \vee B \in F$;
1. $\top \in F$;
1. if $A \in F$ and $B \in F$, then $A \wedge B \in F$.

Here, (1) is equivalent to the previous version; the others, which here say that the lattice is closed under finite [[meet]]s, are equivalent given (1).  (These axioms look more like the axioms for an ideal of a ring.)

You can also interpret these axioms to say that, if you interpret $F$ as a function from $L$ to the set $TV$ of [[truth value]]s, that $F$ is a homomorphism of meet-semilattices.

A __filter of subsets__ of a given set $S$ is a filter in the [[power set]] of $S$.  One also sees filters of open subsets, filters of compact subsets, etc.

# Kinds of filters

A filter $F$ is __proper__ if there exists an element $A$ of $L$ such that $A \notin F$.  A filter in a lattice is proper iff $\bot \notin F$; in particular, a filter of subsets of $S$ is proper iff $\empty \notin F$.  In [[constructive mathematics]], however, one usually wants a stronger (but classically equivalent) notion: a filter $F$ of subsets of $S$ is __proper__ if every element of $F$ is [[inhabited set|inhabited]].

Filters are often assumed to be proper by default in analysis and topology, where proper filters correspond to [[net]]s.

If the complement of a filter is an ideal, then we say that the filter is __prime__ (and equivalently that the ideal is prime).  A prime filter is necessarily proper; a proper filter in a lattice is prime iff, whenever $A \cup B \in F$, either $A \in F$ or $B \in F$.  In other words, $F: L \to TV$ must be a homomorphism of lattices.

In [[nonstandard analysis]] and [[model theory]], a particularly important class of filters are the [[ultrafilter]]s.  A filter is an __ultrafilter__, or __maximal filter__, if it is maximal among the proper filters.  A filter $F$ in a [[Boolean algebra|Boolen lattice]] is an ultrafilter iff, given any subset $A$ of $S$, either $A$ or its complement belongs to $F$ but not both.  In constructive mathematics, an __ultrafilter__ is a filter of sets satisfying the axiom
$$ A \in F \;\Leftrightarrow\; \forall (B \in F),\; \exists (x \in A \cap B) .$$
This is equivalent to the previous definition, using [[excluded middle]].

In a distributive lattice, every ultrafilter is prime; the converse holds in a Boolean lattice.  In this case, we can say that $F: L \to TV$ is a homomorphism of Boolean lattices.

Given an element $x$ of $S$, the __principal ultrafilter__ (of subsets of $S$) at $x$ consists of every subset of $S$ to which $x$ belongs.  It is possible, if one denies the [[axiom of choice]], that every ultrafilter of subsets is principal.  In contrast, the [[Boolean prime ideal theorem]] states that any proper filter (in a Boolean lattice) may be extended to a maximal filter.

# Filterbases

A subset $F$ of a lattice $L$ is a __filterbase__ if it becomes a filter when closed under axiom (1).  Equivalently, a filterbase is any downward-directed subset.  Any subset of a meet-semilattice may be used as a filter __subbase__; form a filterbase by closing under finite meets.

A filterbase $F$ of sets is proper (that is, it generates a proper filter of sets) iff each set in $F$ is inhabited.  A filter subbase of sets is proper iff it satisfies the finite intersection property (well known in topology from a criterion for [[compact space]]s): every finite collection from the subfilter has inhabited intersection.

# References
* [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Ideal_%28order_theory%29)
* Johnstone, Peter T. (1982). _Stone Spaces_. Cambridge University Press. ISBN 0-521-23893-5.