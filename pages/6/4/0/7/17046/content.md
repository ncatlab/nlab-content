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

In [[category theory]] one may ask when an expression of the form "$lim \, colim$" can be replaced by an expression of the form "$colim \, lim$", i.e., under which circumstances [[limits]] and [[colimits]] can be "permuted".

There are (at least) two different types of such "permutation" of limits and colimits:

- [commutativity](#Commutativity),

- [distributivity](#Distributivity):

## Commutativity of limits and colimits
 {#Commutativity}

__Commutativity of limits and colimits__ refers to the situation
when we have a [[diagram]] of the form 

\[
  \label{TheDiagram}
  X \,\colon\, I\times J\to C
\]

and the canonical morphism 

\[
  \label{ComparisonMapForCommutativity}
  \underset
    {i\in I}
    {colim}
  \;
  \underset
    {j\in J}
    {lim} 
  \;
  X_{i,j} 
  \longrightarrow 
  \underset
    {j\in J}
    {lim}
  \;
  \underset
    {i\in I}
    {colim}
  \;
  X_{i,j}
\]

is an [[isomorphism]] (or an [[equivalence in an (infinity,1)-category|equivalence]] in the case of [[(infinity,1)-category|∞-categories]]).

This situation is discussed at *[[commutativity of limits and colimits]]*

## Distributivity of limits over colimits
 {#Distributivity}

__Distributivity of limits over colimits__, in its
easiest possible formulation, is stated for $X$ as above (eq:TheDiagram),
and requires the canonical map 

\[
  \label{ComparisonMapForPermutativity}
  \underset
    {i\in I^J}
    {colim}
  \;
  \underset
    {j\in J}
    {lim}
  \;
  X_{i(j),j} 
  \longrightarrow 
  \underset
    {j\in J}
    {lim}
  \;
  \underset
    {i\in I}
    {colim}
  X_{i,j}
\]

{#WhereNow} to be an [[isomorphism]] (or an [[equivalence in an (infinity,1)-category|equivalence]] in the case of [[(infinity,1)-categories|∞-categories]]), where now -- on the left of (eq:ComparisonMapForPermutativity) -- $i$ is an [[object]] of the [[functor category]] $I^J$, and $i(j)$ denotes the value of this [[functor]] at $j\in J$.

More generally, one may allow the indexing category $I$
to depend on $j\in J$, in that the functor $I\times J\to J$
is replaced by some arbitrary [[Grothendieck fibration]] in categories and $I^J$ by the category of its [[sections]].

This situation is discussed at *[[distributivity of limits over colimits]]*.

## Related concepts

* [[commutativity of limits and colimits]]

* [[distributivity of limits and colimits]]