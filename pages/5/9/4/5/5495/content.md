
# The axiom of union
* table of contents
{: toc}

## Idea

In [[material set theory]] as a [[foundation of mathematics]], the axiom of union is an important axiom needed to get the foundations off the ground (to mix metaphors).  It states that [[unions]] exist.


## Statement

The __axiom of union__ states the following:

+-- {: .un_axiom}
###### Axiom (union)

If $\mathcal{X}$ is a (material) set, then there exists a set $U$ such that, for every set $a$, $a \in U$ if and only if, for some set $B$, $a \in B$ and $B \in \mathcal{X}$.
=--

Using the [[axiom of extensionality]], one can prove that the set $U$ above is unique; it is usually denoted $\bigcup\mathcal{X}$ and called the __[[union]]__ of (the elements of) $\mathcal{X}$.  A slightly different notation may be used when $\mathcal{X}$ is (Kuratowski)-[[finite set|finite]]; for example, $\bigcup\{A,B,C\}$ may be denoted $A \cup B \cup C$.


## Related notions

If $\mathcal{X}$ is given as a collection of [[subsets]] of some ambient [[set]], then the axiom of union is not necessary.  This is the only case when unions are taken in [[structural set theory]].  However, structural set theory in [[predicative mathematics]] requires an axiom giving the existence of [[disjoint unions]].  (In impredicative mathematics, we can construct disjoint unions from [[power sets]] and [[cartesian products]].)
