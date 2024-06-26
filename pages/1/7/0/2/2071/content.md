
\tableofcontents

## Definition


The __symmetric difference__ of two sets $A$ and $B$ (either [[pure sets]] or [[subsets]] of some fixed [[set]]), written $A \uplus B$, $A\oplus B$, $A\triangle B$ (and a host of other ways), may be defined using [[exclusive disjunction]]:
$$ A \uplus B = \{ x \;|\; x \in A \;&#8891;\; x \in B \} .$$
You can also call this [[exclusive union]], especially if you want to use it analogously to exclusive disjunction; then the exclusive union of $n$ sets consists of those elements $x$ that belong to exactly one of the $n$ sets.

The term _symmetric difference_, however, is usually used as the addition in a [[Boolean ring]] and so interpreted as an associative operation; then the symmetric difference of $n$ sets consists of those elements $x$ that belong to an *odd* number of the $n$ sets.

## Properties

The [[empty set]] is the [[neutral element]] for this operation; it is the symmetric difference (or exclusive union, for that matter) of no sets.

In [[constructive mathematics]], the symmetric difference cannot be proved [[associativity|associative]] and so becomes less useful (unless one restricts attention to sets with [[decidable equality]], where it can be proved associative).  This is a problem in [[measure theory]]; see [[Cheng measurable space]] for one way to fix this.

Note that the [[union]], symmetric difference, and (internal, or external up to [[natural isomorphism]]) [[disjoint union]] of a family of (pairwise) [[disjoint sets]] are all the same.  For a family that is not disjoint, however, the union and symmetric difference are different, the internal disjoint union does not make sense, and the external disjoint union is not isomorphic to either the union or the symmetric difference (at least not naturally, and in some cases not at all).

## Related concepts

* [[union]]

* [[Boolean algebra]]

[[!redirects symmetric differences]]