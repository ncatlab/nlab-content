
# Positive elements
* table of contents
{: toc}

## Idea

In [[classical mathematics]], an element of a [[poset]] is positive if and only if it not a [[bottom element]].

A more subtle definition is needed in [[constructive mathematics|constructive]] or [[predicative mathematics|predicative]] mathematics; analogously to how "nonempty sets" may need to be replaced by [[inhabited sets]].  In [[predicative mathematics|predicative]] *and* constructive mathematics, positivity can be axiomatised but not defined.


## Definitions

Let $L$ be a [[preordered set]], and let $x$ be an element of $L$.

+-- {: .num_defn #classdef}
###### Definition
**(in [[classical mathematics]])**
An element $x\in L$ is __positive__ if it not a [[bottom element]].
=--

+-- {: .num_defn #preddef}
###### Definition
**(in [[predicative mathematics]] with [[classical logic]])**
An element $x\in L$ is __positive__ if there exists an element $y\in L$ such that $x \leq y$ is false.
=--

+-- {: .num_defn #constdef}
###### Definition
**(in impredicative [[constructive mathematics]])**
An element $x\in L$ is __positive__ if for any way of writing $x$ as a [[join]] of some [[subset]] $A$ of $L$, $A$ is [[inhabited subset|inhabited]].
=--

+-- {: .num_defn #predconstdef}
###### Definition
**(in [[predicative mathematics|predicative]] [[constructive mathematics|constructive]] mathematics)**
A **positivity predicate** on $L$ is a [[predicate]] pronounced "$x$ is positive" such that
*  Whenever $x$ is positive and $x$ is the [[join]] of $A$, then some element of $A$ is positive;
*  If $x$ is the join of $A$ on the assumption that $x$ is positive, then $x$ really is the join of $A$.
=--

Any two of these definitions can be shown to be equivalent in the union of the corresponding foundational systems.  Specifically:

* In impredicative constructive mathematics, one can prove that every preorder has a unique positivity predicate, which must match Definition \ref{preddef}.

* In predicative mathematics with classical logic, one can prove that every poset has a unique positivity predicate, which must match the Definition \ref{constdef}.

* In [[classical mathematics]] (with [[classical logic]] and impredicativity), all the definitions are equivalent.

## Related pages

* The notion of positivity plays a role in [[locale]] theory, and especially in the definition of an [[overt space]].  This theory is often considered constructively (but impredicatively).

* In predicative constructive mathematics, a positivity predicate is used in the corresponding theory of [[formal topology]].


[[!redirects positive element]]
[[!redirects positive elements]]
[[!redirects positivity predicate]]
[[!redirects positivity predicates]]
