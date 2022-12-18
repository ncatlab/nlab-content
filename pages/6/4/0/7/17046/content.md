+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

One can wonder when an expression of the form $lim colim$ can be replaced by an expression of the form $colim lim$, i.e., under which circumstances [[limits]] and [[colimits]] can be permuted.

## Commutativity of limits and colimits

__Commutativity of limits and colimits__ refers to the situation
when we have a diagram $X\colon I\times J\to C$
and the canonical morphism $colim_{i\in I} lim_{j\in J} X_{i,j} \to lim_{j\in J} colim_{i\in I} X_{i,j}$
is an isomorphism (or an equivalence in the case of ∞-categories).

The article [[commutativity of limits and colimits]]
explores the situations for which such a commutativity
property holds.

## Distributivity of limits over colimits

__Distributivity of limits over colimits__, in its
easiest possible formulation, is stated for $X$ as above,
and requires the canonical map $colim_{i\in I^J} lim_{j\in J} X_{i(j),j} \to lim_{j\in J} colim_{i\in I} X_{i,j}$
to be an isomorphism (or an equivalence in the case of ∞-categories).  Note that here $i$ is an element of the [[functor category]] $I^J$, and $i(j)$ denotes its value at $j\in J$.

More generally, one may allow the indexing category $I$
to depend on $j\in J$, i.e., the functor $I\times J\to J$
is replaced by some arbitrary [[Grothendieck fibration]] in categories.
Then $I^J$ is replaced by the category of sections of
this Grothendieck fibration.

The article [[distributivity of limits over colimits]]
explores the situations for which such a distributivity
property holds.

## Related concepts

* [[commutativity of limits and colimits]]

* [[distributivity of limits and colimits]]