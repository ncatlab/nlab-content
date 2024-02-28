
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
=--
=--

# The axiom of union
* table of contents
{: toc}

## Idea

In [[material set theory]] as a [[foundation of mathematics]], the axiom of union is an important axiom needed to get the foundations off the ground (to mix metaphors).  It states that [[unions]] exist.


## Statement

### In material set theory

The __axiom of union__ states the following:

+-- {: .un_defn}
###### Axiom (union)

If $\mathcal{X}$ is a (material) set, then there exists a set $U$ such that $a \in U$ whenever $a \in B \in \mathcal{X}$.
=--

Using the axiom of separation ([[bounded separation]] is enough), one can prove the existence of a particular set $U$ such that the members of the members of $\mathcal{X}$ are the *only* members of $U$.  Using the [[axiom of extensionality]], we can then prove that this set $U$ is unique; it is usually denoted $\bigcup\mathcal{X}$ and called the __[[union]]__ of (the elements of) $\mathcal{X}$.

A slightly different notation may be used when $\mathcal{X}$ is (Kuratowski)-[[finite set|finite]]; for example, $\bigcup\{A,B,C\}$ may be denoted $A \cup B \cup C$.  If $(B_k \;|\; k \in I)$ is a [[family of sets]], then we may write $\bigcup_{k \in I} B_k$ (and the usual variations for a [[sequence]] of sets) for $\bigcup \{B_k \;|\; k \in I\}$; however, we require the [[axiom of replacement]] to prove that the latter set (the [[range]] of the family) exists in general.

### In dependent type theory

In [[dependent type theory]], it is possible to define a [[Tarski universe]] $(V, \in)$ of [[pure sets]] which behaves as a [[material set theory]]. The universal type family of the Tarski universe is given by the type family $x:V \vdash \sum_{y:V} y \in x$. The **axiom of union** is given by the following [[inference rule]]:

$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{union}_V:\prod_{x:V} \sum_{U:V} \prod_{y:V} \prod_{z:V} (y \in x) \times (z \in y) \to (z \in U)}$$

## Related notions

If $\mathcal{X}$ is given as a collection of [[subsets]] of some ambient [[set]] $S$, then the axiom of union is not necessary; $S$ itself already satisfies the conclusion of the hypothesis (and then bounded separation gives us the union that we want).  This is the only case when unions are taken in [[structural set theory]].  However, structural set theory makes use of _[[disjoint unions]]_, and [[predicative mathematics]] requires an axiom giving their existence.  (In impredicative mathematics, we can construct disjoint unions from [[power sets]] and [[cartesian products]].)

One could also include [[union structure]] in the set theory. 

category: foundational axiom
