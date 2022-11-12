
# The axiom of union
* table of contents
{: toc}

## Idea

In [[material set theory]] as a [[foundation of mathematics]], the axiom of union is an important axiom needed to get the foundations off the ground (to mix metaphors).  It states that [[unions]] exist.


## Statement

The __axiom of union__ states the following:

+-- {: .un_defn}
###### Axiom (union)

If $\mathcal{X}$ is a (material) set, then there exists a set $U$ such that $a \in U$ whenever $a \in B \in \mathcal{X}$.
=--

Using the axiom of separation ([[bounded separation]] is enough), one can prove the existence of a particular set $U$ such that the members of the members of $\mathcal{X}$ are the *only* members of $U$.  Using the [[axiom of extensionality]], we can then prove that this set $U$ is unique; it is usually denoted $\bigcup\mathcal{X}$ and called the __[[union]]__ of (the elements of) $\mathcal{X}$.

A slightly different notation may be used when $\mathcal{X}$ is (Kuratowski)-[[finite set|finite]]; for example, $\bigcup\{A,B,C\}$ may be denoted $A \cup B \cup C$.  If $(B_k \;|\; k \in I)$ is a [[family of sets]], then we may write $\bigcup_{k \in I} B_k$ (and the usual variations for a [[sequence]] of sets) for $\bigcup \{B_k \;|\; k \in I\}$; however, we require the [[axiom of replacement]] to prove that the latter set (the [[range]] of the family) exists in general.

## Relation to indexed disjoint unions

In [[structural set theory]], a [[family of sets]] $(X_i)_{i \in I}$ indexed by the set $I$ is represented by a [[function]] $f:X \to I$, where $I$ is the index set and the fiber of $f$ at each element $i \in I$ is the set $X_i$, with elements $e \in X_i$. This could be represented materially as a sequence of membership relations $e \in i \in I$, where the set $i$ in material set theory represents both the set $X_i$ and the index element $i$ in [[structural set theory]]. Then the union $\bigcup I$ is the indexed [[disjoint union]] $\biguplus_{i \in I} X_i$. 

## Related notions

If $\mathcal{X}$ is given as a collection of [[subsets]] of some ambient [[set]] $S$, then the axiom of union is not necessary; $S$ itself already satisfies the conclusion of the hypothesis (and then bounded separation gives us the union that we want).  This is the only case when unions are taken in [[structural set theory]].  However, structural set theory makes use of _[[disjoint unions]]_, and [[predicative mathematics]] requires an axiom giving their existence.  (In impredicative mathematics, we can construct disjoint unions from [[power sets]] and [[cartesian products]].)


category: foundational axiom
