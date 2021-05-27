# Irreflexive comparison
* table of contents
{: toc}

## Idea

Just as [[preorders]] generalise [[equivalence relations]] and [[total orders]], _irreflexive comparisons_ should generalise [[apartness relations]] and [[linear orders]]

## Definitions

An **irreflexive comparison** on a set $S$ is a (binary) [[relation]] $\lt$ on $S$ that is both [[irreflexive relation|irreflexive]] and a [[comparison]].  That is:

* $x \lt x$ is always false;
* If $x \lt z$, then $x \lt y$ or $y \lt z$

An irreflexive comparison that is also a [[connected relation]] (if $x \lt y$ is false and $y \lt x$ is false, then $x = y$) is a __connected irreflexive comparison__. 

If the set is an [[inequality space]], then an irreflexive comparison is __strongly connected__ if $x \neq y$ implies $x \lt y$ or $y \lt x$.

If an irreflexive comparison satisfies symmetry (if $x \lt y$ then $y \lt x$ then it is an [[apartness relation]]. 

If a connected irreflexive relation is also symmetric (if $x \lt y$, then $y \lt x$), then it is a [[tight apartness relation]], and if it is transitive (if $x \lt y$ and $y \lt z$, then $x \lt z$), then it is a [[linear order]]. 

Thus, irreflexive comparisons are dual to [[preorders]] while connected irreflexive comparisons are dual to [[partial orders]]. 

## Properties

A [[set]] $S$ equipped with an irreflexive comparison is a [[category]] (with $S$ as the set of [[objects]]) [[enriched category|enriched]] over the [[cartesian monoidal category]] $TV^\op$, that is the [[opposite category|opposite]] of the [[partial order|poset]] of [[truth value|truth values]], made into a [[monoidal category]] using [[disjunction]]. $TV^\op$ is a [[co-Heyting algebra]]. 

## Related concepts

* [[apartness relation]]

* [[tight apartness relation]]

* [[linear order]]

* [[preorder]]

* [[partial order]]

* [[quasiorder]]


[[!redirects irreflexive comparisons]]
[[!redirects connected irreflexive comparison]]
[[!redirects connected irreflexive comparisons]]