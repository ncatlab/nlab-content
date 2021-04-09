+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A _filter_ is [[duality|dual]] to an [[ideal]].

A [[proper filter]] is equivalently the [[eventuality filter]] of a [[net]].

Filters of subsets form a [[category of filters|category]]
whose [[situs|simplicial category]] provides a somewhat more 
formalisation of the intuion of "nearness" than the usual topological one; in particular, it contains the categories of topological and of uniform spaces, of simplicial sets, and of filters themselves, allowing to reformulate in terms of this category notions 
such as limit, equicontinuity, locally trivial, and geometric realization.  

## Definitions

A subset $F$ of a [[partial order|poset]] $L$ is called a __filter__ if it is upward-closed and downward-[[direction|directed]]; that is:

1. If $A \leq B$ in $L$ and $A \in F$, then $B \in F$;
2. for some $A$ in $L$, $A \in F$;
3. if $A \in F$ and $B \in F$, then for some $C \in F$, $C \leq A$ and $C \leq B$.

Sometimes the term 'filter' is used for an [[upper set]], that is any set satisfying axiom (1).  (Ultimately this connects with the use of '[[ideal in a monoid|ideal]]' in [[monoid]] theory.)


In a [[lattice]], one can use these alternative axioms:

1. If $A \in F$ and $B$ in $L$, then $A \vee B \in F$;
2. $\top \in F$;
3. if $A \in F$ and $B \in F$, then $A \wedge B \in F$.

Here, (1) is equivalent to the previous version; the others, which here say that the lattice is closed under finite [[meets]], are equivalent given (1).  (These axioms look more like the axioms for an ideal of a ring.)

You can also interpret these axioms to say that, if you think of $F$ as a function from $L$ to the set $TV$ of [[truth values]], then $F$ is a homomorphism of meet-semilattices.


A __filter of subsets__ of a given set $S$ is a filter in the [[power set]] of $S$.  One also sees filters of open subsets, filters of compact subsets, etc, especially in topology.


## Kinds of filters

A filter $F$ is __proper__ if there exists an element $A$ of $L$ such that $A \notin F$.  A filter in a lattice is proper iff $\bot \notin F$; in particular, a filter of subsets of $S$ is proper iff $\empty \notin F$.  In [[constructive mathematics]], however, one usually wants a stronger (but classically equivalent) notion: a filter $F$ of subsets of $S$ is __proper__ if every element of $F$ is [[inhabited set|inhabited]].  If $A \in F$ for every $A$ (in particular if $\empty \in F$), then we have the __[[improper filter]]__.  Compare [[proper subset]] and [[improper subset]].

Filters are often assumed to be proper by default in analysis and topology, where proper filters correspond to [[nets]].  However, we will try to remember to include the adjective 'proper'.

If the complement of a filter is an ideal, then we say that the filter is __prime__ (and equivalently that the ideal is prime).  A prime filter is necessarily proper; a proper filter in a lattice is prime iff, whenever $A \vee B \in F$, either $A \in F$ or $B \in F$.  In other words, $F: L \to TV$ must be a homomorphism of lattices.  The generalisation to arbitrary joins gives a [[completely prime filter]].

A filter is an __[[ultrafilter]]__, or __maximal filter__, if it is maximal among the proper filters.  (See that article for alternative formulations and applications.)  In a distributive lattice, every ultrafilter is prime; the converse holds in a [[Boolean algebra|Boolean lattice]].  In this case, we can say that $F: L \to TV$ is a homomorphism of Boolean lattices.

Given an element $x$ of $S$, the __principal ultrafilter__ (of subsets of $S$) at $x$ consists of every subset of $S$ to which $x$ belongs.  A principal ultrafilter is also called a __fixed ultrafilter__; more generally, a filter of subsets is __fixed__ if its [[intersection]] is [[inhabited set|inhabited]].  In contrast, if $F$ is an filter whose meet (of all elements) exists and is a [[bottom]] element (the [[empty set]] for a filter of subsets), then we call $F$ __free__.

Free ultrafilters on Boolean algebras are important in [[nonstandard analysis]] and [[model theory]].


## Filterbases

A subset $F$ of a lattice $L$ is a __filter[[base]]__ if it becomes a filter when closed under axiom (1).  Equivalently, a filterbase is any downward-directed subset.  Any subset of a meet-semilattice may be used as a filter __[[subbase]]__; form a filterbase by closing under finite meets.

A filterbase $F$ of sets is proper (that is, it generates a proper filter of sets) iff each set in $F$ is inhabited.  A filter subbase of sets is proper iff it satisfies the finite intersection property (well known in topology from a criterion for [[compact spaces]]): every finite collection from the subfilter has inhabited intersection.


## The poset of filters and push-forwards

If $f:L_1\to L_2$ is a [[monotone map]] and $F\subseteq L_1$ a filter, then $\lbrace f(A) \mid A\in F\rbrace\subseteq L_2$ is a filter base. Let $f_\ast(F)$ be the filter generated by this filter base.
The set of filters $Filters(L)$ is a poset in its own right w.r.t. inclusion and $f_\ast: (Filters(L_1),\subseteq)\to(Filters(L_2),\subseteq)$ is monotone. Therefore $L\mapsto Filters(L), f\mapsto f_\ast$ is a functor from the category of posets to itself.

If $f$ satisfies stronger properties than mere monotony, then $f_\ast$ will be better behaved as well:

* If $L$ is a meet-[[semilattice]], then $Filters(L)$ is a complete join-semilattice: $\bigvee_{i\in I} F_i = \left\langle \bigwedge_{j\in J} A_j \mid J\subseteq I\text{ finite}, A_j\in F_j\right\rangle$. If $f:L_1\to L_2$ respects finite meets, then $f_\ast$ respects all joins. If $f$ is merely monotone, then $f_\ast$ respects all filtered joins.
* If $L$ has all $|I|$-fold joins for some indexing set $I$, then $Filters(L)$ has $|I|$-fold meets: $\bigwedge_{i\in I} F_i = \lbrace \bigvee_{i\in I} A_i \mid A_i\in F_i\rbrace$. If $f$ respects $|I|$-fold joins, then $f_\ast$ respects $|I|$-fold meets.
* If $L$ is a [[distributive lattice]], then $Filters(L)$ is a [[frame]], i.e. the infinite distributive law $F \wedge \bigvee_{i\in I} G_i = \bigvee_{i\in I} (F\wedge G_i)$ holds. The other distributive law also holds for finite meets: $F \vee \bigwedge_{i\in I} G_i = \bigwedge_{i\in I} (F\vee G_i)$ if $I$ is finite. It holds more generally if $L$ has all $|I|$-fold meets, the $|I|$-fold distributive law $A\wedge \bigvee_{i\in I} B_i = \bigvee_{i\in I} (A\wedge B_i)$ holds in $L$ and $F$ is closed under $|I|$-fold meets.

* If $L$ is a complete join-semilattice, then $Filters(L)$ is a complete lattice. If $f$ respects all joins, then $f_\ast$ respects all meets. In this case $f_\ast$ has a [[left adjoint]] $f^\ast: L_2\to L_1$ which is given by $f^\ast(G) = \bigwedge \lbrace F | G\subseteq f_\ast(F)\rbrace$ so that $f^\ast(G)\subseteq F \iff G\subseteq f_\ast(F)$ holds. As a left adjoint $f^\ast$ respects all joins.

* If $(f,g)$ is an adjoint pair between $L_1$ and $L_2$, that is f$: L_1 \to L_2$, $g: L_2\to L_1$ monotone and $f(x) \leq y \iff x\leq g(y)$ for all $x\in L_1$, $y\in L_2$, then $(g_\ast,f_\ast)$ is an adjoint pair between $Filters(L_2)$ and $Filters(L_1)$. Note that the push-forward turns left adjoints into right adjoint and vice versa.

### Examples

* If $L_1=(P(X),\subseteq), L_2=(P(Y),\subseteq)$ for some sets $X,Y$ and $\alpha:X\to Y$ is any map, then $f:L_1\to L_2, A\mapsto \alpha(A)$ is monotone and respects arbitrary joins. Therefore $f_\ast: Filters(L_1)\to Filters(L_2)$ respects arbitrary meets. Note that even though $L_1, L_2$ are meet-semilattices, $f$ does not respect meets in general, because $\alpha(A\cap A')\subseteq \alpha(A)\cap\alpha(A')$ holds, but equality is equivalent to $\alpha$ being injective.
* $f$ is the left adjoint of $g: L_2\to L_1, B\mapsto \alpha^{-1}(B)$. Therefore $f_\ast$ is the right adjoint of $f^\ast=g_\ast$ which is given by taking preimage filters: $g_\ast(G) = \langle \alpha^{-1}(B) | B\in G\rangle$.
* $g$ has not only the left adjoint $f$, but also a right adjoint $h:L_1\to L_2$. It can be described as follows: Call a set $A\subseteq X$ is called $\alpha$-saturated if it is the union of fibers of $\alpha$, i.e. if $\alpha^{-1}(\alpha(A)) = A$. There is a biggest $\alpha$-saturated subset $A_\alpha$ of every $A$. The morphism $h$ is given by $h(A) := \alpha(A_\alpha) \cup (Y\setminus \alpha(X))$.
* Therefore $g_\ast$ not only preserves all joins but all meets as well.

## Application to analysis and topology

Every [[net]] $\nu: I \to S$ defines an __[[eventuality filter]]__ $E_\nu$: let $A$ belong to $E_\nu$ if, for some index $k$, for every $l \geq k$, $\nu_l \in A$.  (That is, $\nu$ is eventually in $A$.)  Note that $E_\nu$ is proper; conversely, any proper filter $F$ has a net whose eventuality filter is $F$ (as described at [[net]]).  Everything below can be done for nets as well as for (proper) filters, but filters often lead to a cleaner theory.

In a [[topological space]] $S$, a filter $F$ on $S$ __[[convergence|converges]]__ to a point $x$ of $S$ if every [[neighbourhood]] of $x$ belongs to $F$.  A filter $F$ __clusters__ at a point $x$ if every neighbourhood of $x$ intersects every element of $F$.  With these definitions, the improper filter converges to every point and clusters at no point; a proper filter, however, clusters at every point that it converges to.

The concepts of continuous function and such conditions as [[compact space|compactness]] and [[Hausdorff space|Hausdorffness]] may be defined quite nicely in terms of the convergence relation.  In fact, everything about topological spaces may be defined in terms of the convergence relation, although not always nicely.  This is because topological spaces form a [[full subcategory]] of the category of [[convergence spaces]], where the convergence relation is the fundamental concept.  More details are there.

In a [[metric space]] $S$, a filter $F$ on $S$ is __Cauchy__ if it has elements of arbitrarily small diameter.  Then a [[sequence]] is a [[Cauchy sequence]] iff its eventuality filter is Cauchy.  (This can be generalised to [[uniform spaces]].)  The concept of completion of a metric space may be defined quite nicely in terms of the Cauchy filters, although not every property (not even every uniform property) of metric spaces can be defined in this way.  As for convergence, there is a general notion of [[Cauchy space]], but the forgetful functors from metric and uniform spaces are now not full.


## References

* [Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Filter_%28mathematics%29).
* [[Peter Johnstone]] (1982); _[[Stone Spaces]]_; Cambridge University Press. ISBN 0-521-23893-5.

[[!redirects filters]]

[[!redirects filter of subsets]]
[[!redirects filters of subsets]]

[[!redirects proper filter]]
[[!redirects proper filters]]
[[!redirects prime filter]]
[[!redirects prime filters]]
[[!redirects fixed filter]]
[[!redirects fixed filters]]
[[!redirects free filter]]
[[!redirects free filters]]

[[!redirects filterbase]]
[[!redirects filterbases]]
[[!redirects filter base]]
[[!redirects filter bases]]
[[!redirects filter subbase]]
[[!redirects filter subbases]]
