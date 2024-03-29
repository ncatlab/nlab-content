
# Disjoint subsets
* table of contents
{: toc}

## Idea

Two [[concrete sets]] are disjoint if they have no common [[elements]].


## Definitions

Given an [[abstract set]] $V$, two [[subsets]] $A$ and $B$ of $V$ __meet__ if their [[intersection]] is [[inhabited subset|inhabited]]; $A$ and $B$ are __disjoint__ if they do not meet, in other words if their intersection is [[empty subset|empty]].


## Foundational issues

In [[material set theory]], we may speak of take $A$ and $B$ to be simply [[sets]], rather than subsets of some [[ambient set]] $V$.  Equivalently, one may take $V$ to be the [[von Neumann universe|class of all sets]] by default.  (In this context, it's important that whether $A$ and $B$ meet or are disjoint is independent of the ambient set or class.)

In [[constructive mathematics]], the default meaning of 'disjoint' is as above, but sometimes one wants a definition relative to some [[inequality relation]] $\ne$ on $V$.  Then $A$ and $B$ are __$\ne$-disjoint__ if, whenever $x \in A$ and $y \in B$, $x \ne y$.  (Ordinary disjointness is relative to the [[denial inequality]].)


## Properties

### Relation to disjoint unions

The concrete sets $A$ and $B$ are disjoint iff they have an internal [[disjoint union]], in other words if their [[inclusions]] into their [[union]] $A \cup B$ form a [[coproduct]] diagram in [[the category of sets]].  (Etymologically, of course, this is backwards.)

Many authors are unfamiliar with disjoint unions.  When the disjoint union oid two [[abstract sets]] $A$ and $B$ is needed, they will typically lapse into [[material set theory]] (even when the work is otherwise perfectly [[structural set theory|structural]]), and make some comment such as 'without loss of generality, assume that $A$ and $B$ are disjoint' or (especially when $A = B$) 'take two [[isomorphic]] copies of $A$ and $B$', then call the disjoint union simply a 'union'.  (This works by the previous paragraph.)


### Internalization

In any [[category]] with an [[object]] $V$, two [[subobjects]] $A$ and $B$ are __disjoint__ if their [[pullback]] is [[initial object|initial]] in $C$.  Then disjoint subsets are precisely disjoint subobjects in [[Set]].

To internalize the characterization in terms of internal disjoint unions is harder.  If $A$ and $B$ have a [[join]] in the [[poset of subobjects]] $Sub(V)$, then we may ask whether this forms a [[coproduct]] diagram in $C$.  This should be equivalent if $C$ has [[disjoint coproducts]].


## Related concepts

* [[disjoint coproduct]]

[[!redirects disjoint set]]
[[!redirects disjoint sets]]
[[!redirects disjoint subset]]
[[!redirects disjoint subsets]]

[[!redirects disjoint]]
