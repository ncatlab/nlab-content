A [[filter]] is an __ultrafilter__, or __maximal filter__, if it is maximal among the proper filters.  A filter $F$ in a [[Boolean algebra|Boolean lattice]] is an ultrafilter iff, given any subset $A$ of $S$, either $A$ or its complement belongs to $F$ but not both.  In constructive mathematics, an __ultrafilter__ is a filter of sets satisfying the axiom
$$ A \in F \;\Leftrightarrow\; \forall (B \in F),\; \exists (x \in A \cap B) .$$
This is equivalent to the previous definition, using [[excluded middle]].

In a distributive [[lattice]], every ultrafilter is prime; the converse holds in a Boolean lattice.  In this case, we can say that $F: L \to TV$ is a homomorphism of Boolean lattices.

Given an element $x$ of $S$, the __principal ultrafilter__ (of subsets of $S$) at $x$ consists of every subset of $S$ to which $x$ belongs.  It is possible, if one denies the [[axiom of choice]], that every ultrafilter of subsets is principal.  In contrast, the [[Boolean prime ideal theorem]] states that any proper filter (in a Boolean lattice) may be extended to a maximal filter.
