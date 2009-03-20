A _filter_ is [[duality|dual]] to an [[ideal]].

# Definitions

A subset $F$ of a [[poset]] $L$ is called a __filter__ if it is upward-closed and downward-[[direction|directed]]; that is:
1. If $A \leq B$ in $L$ and $A \in F$, then $B \in F$;
1. for some $A$ in $L$, $A \in F$;
1. if $A \in F$ and $B \in F$, then for some $C \in F$, $C \leq A$ and $C \leq B$.

Sometimes the term 'filter' is used for an [[upper set]], that is any set satisfying axiom (1).  (Ultimately this connects with the use of 'ideal' in [[monoid]] theory.)

In a [[lattice]], one can use these alternative axioms:
1. If $A \in F$ and $B$ in $L$, then $A \vee B \in F$;
1. $\top \in F$;
1. if $A \in F$ and $B \in F$, then $A \wedge B \in F$.

Here, (1) is equivalent to the previous version; the others, which here say that the lattice is closed under finite [[meet]]s, are equivalent given (1).  (These axioms look more like the axioms for an ideal of a ring.)

You can also interpret these axioms to say that, if you think of $F$ as a function from $L$ to the set $TV$ of [[truth value]]s, then $F$ is a homomorphism of meet-semilattices.

A __filter of subsets__ of a given set $S$ is a filter in the [[power set]] of $S$.  One also sees filters of open subsets, filters of compact subsets, etc, especially in topology.

# Kinds of filters

A filter $F$ is __proper__ if there exists an element $A$ of $L$ such that $A \notin F$.  A filter in a lattice is proper iff $\bot \notin F$; in particular, a filter of subsets of $S$ is proper iff $\empty \notin F$.  In [[constructive mathematics]], however, one usually wants a stronger (but classically equivalent) notion: a filter $F$ of subsets of $S$ is __proper__ if every element of $F$ is [[inhabited set|inhabited]].

Filters are often assumed to be proper by default in analysis and topology, where proper filters correspond to [[net]]s.  However, we will try to remember to include the adjective 'proper'.

If the complement of a filter is an ideal, then we say that the filter is __prime__ (and equivalently that the ideal is prime).  A prime filter is necessarily proper; a proper filter in a lattice is prime iff, whenever $A \cup B \in F$, either $A \in F$ or $B \in F$.  In other words, $F: L \to TV$ must be a homomorphism of lattices.

A filter is an __[[ultrafilter]]__, or __maximal filter__, if it is maximal among the proper filters.  (See that article for alternative formulations.)  In a distributive lattice, every ultrafilter is prime; the converse holds in a [[Boolean algebra|Boolean lattice]].  In this case, we can say that $F: L \to TV$ is a homomorphism of Boolean lattices.

Given an element $x$ of $S$, the __principal ultrafilter__ (of subsets of $S$) at $x$ consists of every subset of $S$ to which $x$ belongs.  In contrast, if $F$ is an filter whose meet (of all elements) exists and is a [[bottom]] element, then we call $F$ __free__.

Free ultrafilters on Boolean algebras are important in [[nonstandard analysis]] and [[model theory]].

+--{.query}
I restored some of the material on ultrafilters for the sake of completeness in this article.  In particular, principal ultrafilters are used below.  --Toby
=--

# Filterbases

A subset $F$ of a lattice $L$ is a __filterbase__ if it becomes a filter when closed under axiom (1).  Equivalently, a filterbase is any downward-directed subset.  Any subset of a meet-semilattice may be used as a filter __subbase__; form a filterbase by closing under finite meets.

A filterbase $F$ of sets is proper (that is, it generates a proper filter of sets) iff each set in $F$ is inhabited.  A filter subbase of sets is proper iff it satisfies the finite intersection property (well known in topology from a criterion for [[compact space]]s): every finite collection from the subfilter has inhabited intersection.

# Application to analysis and topology

Every [[net]] $\nu: I \to S$ defines an __eventuality filter__ $E_\nu$: let $A$ belong to $E_\nu$ if, for some index $k$, for every $l \geq k$, $\nu_l \in A$.  (That is, $\nu$ is eventually in $A$.)  Note that $E_\nu$ is proper; conversely, any proper filter $F$ has a net whose eventuality filter is $F$ (as described at [[net]]).  Everything below can be done for nets as well as filters, but filters often lead to a cleaner theory.

## Convergent filters

A __convergence space__ is a [[set]] $S$ together with a [[relation]] $\to$ from $\mathcal{F}S$ to $S$, where $\mathcal{F}S$ is the set of filters on $S$, satisfying some axioms.  (If $F \to x$, we say that $F$ __converges__ to $x$.)  The axioms are these:
1. If $F \subseteq G$ and $F \to x$, then $G \to x$;
1. The principal ultrafilter $F_x$ at $x$ converges to $x$;
1. If $F \to x$ and $G \to x$, then $F \cap G \to x$.

It follows that $F \to x$ if and only if $F \cap F_x$ does.  Given that, the convergence space is defined precisely by specifying, for each point $x$, a filter of subsets of the set of subfilters of the principal ultrafilter at $x$.  (But that is sort of a tongue twister.)

The morphisms of convergence spaces are the continuous functions; a function $f$ between convergence spaces is __continuous__ if $F \to x$ implies that $f(F) \to f(x)$, where $f(F)$ is the filter generated by the filterbase $\{F(A) \;|\; A \in F\}$.  In this way, convergence spaces form a [[category]] $Conv$.

Any [[topological space]] is a convergence space: $F \to x$ if every neighbourhood of $x$ belongs to $F$.  A convergence space is __topological__ if it comes from a topology on $S$.  The [[full subcategory]] of $Conv$ consisting of the topological convergence spaces is [[equivalence of categories|equivalent]] to the category [[Top]] of topological spaces.  In this way, the definitions in this section all become theorems about topological spaces.  However, not every convergence in analysis is topological; convergence in measure is a good counterexample.

Note that the improper filter (the power set of $S$) converges to every point.  Conversely, a convergence space $S$ is __Hausdorff__ if every proper filter converges to at most one point; then we have a [[partial function]] $\lim$ from $\mathcal{F}S$ to $S$.

A convergence space $S$ is __[[compact space|compact]]__ if every proper filter is contained in a convergent filter.  Equivalently (assuming the Boolean prime ideal theorem), $S$ is compact iff every ultrafilter converges.

## Cauchy filters

A __Cauchy space__ is a set $S$ together with a collection of filters declared to be __Cauchy filters__.  These must satisfy axioms:
1. If $F \subseteq G$, $F$ is Cauchy, and $G$ is proper, then $G$ is Cauchy;
1. Every principal ultrafilter is Cauchy;
1. If $F$ and $G$ are Cauchy and $F \cap G$ is proper, then $F \cap G$ is Cauchy;
1. Every Cauchy filter is proper.

The set of Cauchy filters is almost a filter of subsets of the set of proper filters (another tongue twister), except that $F \cap G$ need not contain a Cauchy filter if it\'s not proper.

The morphisms of Cauchy spaces are the Cauchy functions; a function $f$ between Cauchy spaces is __Cauchy__ if $f(F)$ is Cauchy whenever $F$ is.  In this way, Cauchy spaces form a category $Cauchy$.

Any [[metric space]] is a Cauchy space: $F$ is Cauchy if it has elements of arbitrarily small diameter.  (In particular, a [[sequence]] is a [[Cauchy sequence]] iff its eventuality filter is Cauchy.)  In this way, the category of metric spaces becomes a [[subcategory]] (but not a full one) of $Cauchy$.  (This can be generalised to uniform spaces; the inclusion is still not full.)

Every Cauchy space is a convergence space; $F \to x$ if the intersection of $F$ with the principal ultrafilter $F_x$ is Cauchy.  Note that any convergent proper filter must be Cauchy.  Conversely, if every Cauchy filter is convergent, then the Cauchy space is called __complete__.

A Cauchy space $S$ is __totally bounded__ (or __precompact__) if every proper filter is contained in a Cauchy filter.  Equivalently (assuming the Boolean prime ideal theorem), $S$ is totally bounded iff every ultrafilter is Cauchy.

A Cauchy space is compact (as a convergence space) if and only if it is both complete and totally bounded.

# References
* [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Filter_%28mathematics%29).
* Johnstone, Peter T. (1982). _Stone Spaces_. Cambridge University Press. ISBN 0-521-23893-5.
* Eva Lowen-Colebunders (1989). Function Classes of Cauchy Continuous Maps. Dekker, New York, 1989.