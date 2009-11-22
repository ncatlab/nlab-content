# Filters

A _filter_ is [[duality|dual]] to an [[ideal]].

* tic
{: toc}


## Definitions

A subset $F$ of a [[partial order|poset]] $L$ is called a __filter__ if it is upward-closed and downward-[[direction|directed]]; that is:
1. If $A \leq B$ in $L$ and $A \in F$, then $B \in F$;
1. for some $A$ in $L$, $A \in F$;
1. if $A \in F$ and $B \in F$, then for some $C \in F$, $C \leq A$ and $C \leq B$.

Sometimes the term 'filter' is used for an [[upper set]], that is any set satisfying axiom (1).  (Ultimately this connects with the use of 'ideal' in [[monoid]] theory.)

In a [[lattice]], one can use these alternative axioms:
1. If $A \in F$ and $B$ in $L$, then $A \vee B \in F$;
1. $\top \in F$;
1. if $A \in F$ and $B \in F$, then $A \wedge B \in F$.

Here, (1) is equivalent to the previous version; the others, which here say that the lattice is closed under finite [[meets]], are equivalent given (1).  (These axioms look more like the axioms for an ideal of a ring.)

You can also interpret these axioms to say that, if you think of $F$ as a function from $L$ to the set $TV$ of [[truth values]], then $F$ is a homomorphism of meet-semilattices.

A __filter of subsets__ of a given set $S$ is a filter in the [[power set]] of $S$.  One also sees filters of open subsets, filters of compact subsets, etc, especially in topology.


## Kinds of filters

A filter $F$ is __proper__ if there exists an element $A$ of $L$ such that $A \notin F$.  A filter in a lattice is proper iff $\bot \notin F$; in particular, a filter of subsets of $S$ is proper iff $\empty \notin F$.  In [[constructive mathematics]], however, one usually wants a stronger (but classically equivalent) notion: a filter $F$ of subsets of $S$ is __proper__ if every element of $F$ is [[inhabited set|inhabited]].

Filters are often assumed to be proper by default in analysis and topology, where proper filters correspond to [[nets]].  However, we will try to remember to include the adjective 'proper'.

If the complement of a filter is an ideal, then we say that the filter is __prime__ (and equivalently that the ideal is prime).  A prime filter is necessarily proper; a proper filter in a lattice is prime iff, whenever $A \cup B \in F$, either $A \in F$ or $B \in F$.  In other words, $F: L \to TV$ must be a homomorphism of lattices.

A filter is an __[[ultrafilter]]__, or __maximal filter__, if it is maximal among the proper filters.  (See that article for alternative formulations and applications.)  In a distributive lattice, every ultrafilter is prime; the converse holds in a [[Boolean algebra|Boolean lattice]].  In this case, we can say that $F: L \to TV$ is a homomorphism of Boolean lattices.

Given an element $x$ of $S$, the __principal ultrafilter__ (of subsets of $S$) at $x$ consists of every subset of $S$ to which $x$ belongs.  A principal ultrafilter is als called a __fixed ultrafilter__; more generally, a filter of subsets is __fixed__ if its [[intersection]] is [[inhabited set|inhabited]].  In contrast, if $F$ is an filter whose meet (of all elements) exists and is a [[bottom]] element (the [[empty set]] for a filter of subsets), then we call $F$ __free__.

Free ultrafilters on Boolean algebras are important in [[nonstandard analysis]] and [[model theory]].


## Filterbases

A subset $F$ of a lattice $L$ is a __filterbase__ if it becomes a filter when closed under axiom (1).  Equivalently, a filterbase is any downward-directed subset.  Any subset of a meet-semilattice may be used as a filter __subbase__; form a filterbase by closing under finite meets.

A filterbase $F$ of sets is proper (that is, it generates a proper filter of sets) iff each set in $F$ is inhabited.  A filter subbase of sets is proper iff it satisfies the finite intersection property (well known in topology from a criterion for [[compact spaces]]): every finite collection from the subfilter has inhabited intersection.


## Application to analysis and topology

Every [[net]] $\nu: I \to S$ defines an __eventuality filter__ $E_\nu$: let $A$ belong to $E_\nu$ if, for some index $k$, for every $l \geq k$, $\nu_l \in A$.  (That is, $\nu$ is eventually in $A$.)  Note that $E_\nu$ is proper; conversely, any proper filter $F$ has a net whose eventuality filter is $F$ (as described at [[net]]).  Everything below can be done for nets as well as for (proper) filters, but filters often lead to a cleaner theory.

In a [[topological space]] $S$, a filter $F$ on $S$ __converges__ to a point $x$ of $S$ if every neighbourhood of $x$ belongs to $F$.  A filter $F$ __clusters__ at a point $x$ if every neighbourhood of $x$ intersects every element of $F$.  With these definitions, the improper filter converges to every point and clusters at no point; a proper filter, however, clusters at every point that it converges to.

The concepts of continuous function and such conditions as [[compact space|compactness]] and [[Hausdorff space|Hausdorffness]] may be defined quite nicely in terms of the convergence relation.  In fact, everything about topological spaces may be defined in terms of the convergence relation, although not always nicely.  This is because topological spaces form a [[full subcategory]] of the category of [[convergence spaces]], where the convergence relation is the fundamental concept.  More details are there.

In a [[metric space]] $S$, a filter $F$ on $S$ is __Cauchy__ if it has elements of arbitrarily small diameter.  Then a [[sequence]] is a [[Cauchy sequence]] iff its eventuality filter is Cauchy.  (This can be generalised to [[uniform spaces]].)  The concept of completion of a metric space may be defined quite nicely in terms of the Cauchy filters, although not every property (not even every uniform property) of metric spaces can be defined in this way.  As for convergence, there is a general notion of [[Cauchy space]], but the forgetful functors from metric and uniform spaces are now not full.


## References

* [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Filter_%28mathematics%29).
* [[Peter Johnstone]] (1982). _[[Stone Spaces]]_. Cambridge University Press. ISBN 0-521-23893-5.


[[!redirects filters]]
[[!redirects filter of subsets]]
[[!redirects filters of subsets]]
[[!redirects proper filter]]
[[!redirects prime filter]]
[[!redirects fixed filter]]
[[!redirects free filter]]
[[!redirects proper filters]]
[[!redirects prime filters]]
[[!redirects fixed filters]]
[[!redirects free filters]]
[[!redirects filterbase]]
[[!redirects filterbases]]
[[!redirects filter base]]
[[!redirects filter bases]]
[[!redirects filter subbase]]
[[!redirects filter subbases]]