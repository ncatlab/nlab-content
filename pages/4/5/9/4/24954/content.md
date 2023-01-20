
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

\tableofcontents

## Overview

There are a few major differences between set theory and dependent type theory. 

### Logic

Set theory of all flavors, including [[material set theory]] and [[structural set theory]], have two notions of logic, 

* the external [[predicate logic]] with primitive notions of [[proposition]], [[true]], [[false]], [[conjunction]], [[disjunction]], [[implication]], [[existential quantifier]], and [[universal quantifier]]

* the [[internal logic]] built from [[subsingletons]], the [[singleton]], the [[empty set]], binary [[products]] of two subsingletons, the [[support]] of the binary [[disjoint union]] of two subsingletons, [[function sets]] of two subsingletons, the support of the indexed disjoint union of a family of subsingletons, and the indexed product of a [[family of subsets|family of subsingletons]]. 

Dependent type theory only has one notion of logic, which would correspond to the internal logic of the set theory. Thus, propositions are subsingletons. 

### Equality

Set theory of all flavors have only one notion of equality, [[propositional equality]], which is a proposition in the external logic. 

Most dependent type theories, like [[Martin-Löf type theory]], [[cubical type theory]], ([[higher observational type theory|higher]]) [[observational type theory]], [[two-level type theory]], [[simplicial type theory]], et cetera, all have two notions of equality, [[judgmental equality]] and [[typal equality]]. 

The only dependent type theory which only has one notion of equality is [[objective type theory]], and corresponds to typal equality. 

In addition, the equality in all set theories are by definition propositions, while only in [[set-level type theories]] such as those with [[UIP]], [[axiom K]], or [[boundary separation]] have subsingleton-valued typal equality. More general dependent type theories have equalities which could be sets, or types representing [[infinity-groupoids]]. 

### Functions

Categorical set theory has two notions of functions, either as elements of [[function sets]] $f \in B^A$ or as a primitive $f:A \to B$ in the set theory. One could compare functions for equality in either case.

Dependent type theory only has one notion of function which could be compared for equality: an element of a [[function type]] $f:A \to B$. The corresponding primitive notion is the concept of family of elements $x:A \vdash f(x):B$, of which there is no corresponding notion of equality of a family of elements. 

## See also

* [[set theory]]
* [[dependent type theory]]
* [[material versus structural set theory]]

[[!redirects set theory and dependent type theory]]