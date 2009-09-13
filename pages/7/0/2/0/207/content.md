There is a lot of interesting stuff to be said about equality in [[logic]], [[higher category theory]], and the [[foundations]] of mathematics, but it hasn\'t been said here yet.

Some important distinctions, possibly all the same thing using different terminologies:
*  the difference between axiomatic and defined equality;
*  the difference between identity and equality,
*  the difference between intensional and extensional equality,
*  the difference between equality and [[isomorphism]],
*  the difference between equality and [[equivalence]],
*  the possibility of operations that might not preserve equality.

Here is an important practical fact: every [[set]] $S$ has an __equality relation__, a binary [[relation]] according to which two elements $x$ and $y$ of $S$ are related if and only if they are equal; in this case we write $x = y$.  This is the smallest [[reflexive relation]] on $S$, and it is in fact an [[equivalence relation]]; it is the only equivalence relation on $S$ that is also a [[partial order]] (although that fact is somewhat circular).  This relation is often called the __identity relation__ on $S$, either because 'identity' can mean 'equality' or because it is the [[identity]] for [[composition]] of relations.

As a [[subset]] of $S \times S$, the equality relation is often called the __[[diagonal]]__ and written $\Delta_S$ or similarly.  As an abstract set, this subset is [[isomorphism|isomorphic]] to $S$ itself, so one also sees the diagonal as a map, the [[diagonal function]] $S \overset{\Delta_S}\to S \times S$, which maps $x$ to $(x,x)$; note that $x = x$.  This is in [[Set]]; analogous [[diagonal morphisms]] exist in any [[cartesian monoidal category]].


[[!redirects equality relation]]
[[!redirects equality predicate]]
[[!redirects equal]]
[[!redirects identity relation]]
[[!redirects diagonal relation]]