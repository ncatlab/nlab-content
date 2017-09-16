# Definition #

A **topological space** is a set $X$ equipped with a set of [[subset]]s of $X$, called **open sets**, which are closed under [[finite intersection]]s and arbitrary [[union]]s.  Since $X$ itself is the intersection of zero subsets, it is open, and since the empty set $\emptyset$ is the union of zero subsets, it is also open.

The morphisms between topological spaces are **continuous maps**: functions $f:X\to Y$ such that the preimage of any open set is open.


# Alternate definitions #

There are many equivalent ways to define a topological space.  A non-exhaustive list follows:

* A set $X$ with a collection of open sets (as above).

* A set $X$ with a collection of closed sets (the complements of the open sets) satisfying dual axioms.

* A pair $(X, int)$, where $int: P(X) \to P(X)$ is a left exact comonad on the power set of $X$ (the "interior operator").  The open sets are exactly the fixed points of $int$.

* A pair $(X, cl)$ where $cl$ is a "closure operator" satisfying axioms dual to those of $int$.  The closed sets are the fixed points of $cl$.

* A relational $\beta$-module; that is, a lax algebra of the [[monad]] of [[ultrafilter]]s on the 2-category [[Rel]] of sets and (binary) [[relation]]s.  More explicitly, this means a set $X$ together with a relation called "convergence" between ultrafilters and points satisfying certain axioms.  See [[pseudotopological space]].

* A set with a convergence relation between [[net]]s and points, or even between transfinite [[sequence]]s and points, satisfying appropriate axioms.


# Variations #

The definition of topological space was a matter of some debate, especially about 100 years ago. Our definition is due to Bourbaki, so may be called **Bourbaki spaces**. For some purposes, including [[homotopy theory]], it is important to use [[nice topological space|nice topological spaces]] and/or a [[nice category of spaces]].  On the other hand, when doing [[topos]] theory or working in [[constructive mathematics]], it is often more appropriate to use [[locale|locales]] than topological spaces. Some applications to analysis require more general [[convergence space]]s or other generalisations.
