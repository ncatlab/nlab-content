An __ultrafilter__ on a set $S$ is a collection $F$ of [[subset]]s of $S$ satisfying the axiom
$$ A \in F \;\Leftrightarrow\; \forall (B \in F),\; \exists (x \in A \cap B) .$$
This is the only axiom necessary; from this, you can prove that $F$ is a [[filter]].

+--{.query}
No, I guess that you need to state closure under binary meets too.  (Counterexample:  $S$ is $\{a,b,c\}$, $F$ consists of the pairs and their supersets.)  Alternatively, generalise from $B$ to $B_1, \ldots, B_n$; which is better?  ---Toby
=--

Using [[excluded middle]], it is equivalent to say that a filter $F$ is an ultrafilter if, given any subset $A$ of $S$, either $A$ or its complement belongs to $F$.  This version generalises to any [[Boolean algebra]].  Another way to define an ultrafilter on a Boolean algebra $L$ is as a Boolean-algebra homomorphisms from $L$ to the set $\{\bot,\top\}$ of [[truth value]]s.

Actually, we can define an __ultrafilter__ in any [[partial order|poset]] to be a proper [[filter]] that is maximal among proper filters.  In a distributive [[lattice]], every ultrafilter is prime; the converse holds in a Boolean lattice.

Given an element $x$ of $S$, the __principal ultrafilter__ (on $S$) at $x$ consists of every subset of $S$ to which $x$ belongs.  In contrast, if $F$ is an ultrafilter on $S$ such that the intersection of the elements of $F$ is [[empty set|empty]], then we call $F$ a __free ultrafilter__.  It is possible, if one denies the [[axiom of choice]], that every ultrafilter of subsets is principal.  In contrast, the [[Boolean prime ideal theorem]] states that any proper filter (in a Boolean lattice) may be extended to a maximal filter.

Free ultrafilters are important in [[nonstandard analysis]] and [[model theory]], where the Boolean prime ideal theorem seems to be a necessity.