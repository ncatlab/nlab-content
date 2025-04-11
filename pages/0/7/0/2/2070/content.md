
> This entry is about regular elements in [[formal logic]] and [[topology]]. For regular elements in [[physics]]/[[quantum field theory]] see at _[[regularization (physics)]]_. For regular elements in [[ring theory]] and [[commutative algebra]], see [[cancellative element]]. 

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

A __regular element__ of a [[Heyting algebra]] is an element $x$ such that $\neg{\neg{x}} = x$.

Thus a [[Boolean algebra]] is precisely a Heyting algebra in which every element is regular.

As a special case, a __regular open__ in a [[locale]] $S$ is a regular element of $S$ as a [[frame]].  These define the __regular [[open sublocales]]__ of $S$.  We may also say __regular open [[subspace]]__ for this (or the following concept).

An analogous kind of regular open subspace is a __regular open set__ in a [[topological space]] $X$, which is a regular element of the [[frame of open sets]] of $X$.  Equivalently, this is an [[open set]] in $X$ that equals the interior of its closure, or equivalently the exterior of its exterior.  (This is the origin of the term, related to a [[regular space]].)

The __regularization__ of $x$ is $\neg{\neg{x}}$; note that this is regular.  In fact, any element of the form $\neg{y}$ is regular.  Note that $x \leq \neg{\neg{x}}$; in logic, this means that a double negation is a weaker statement.

In a topological space, the regularization of an open set $G$ can be constructed as $Int(Cl(G))$, or equivalently as $Ext(Ext(G))$.  Sometimes one performs this operation to an arbitrary set (in the space) to produce a regular open set.  But note that while $G \subseteq Int(Cl(G))$ when $G$ is open, this does not hold for an arbitrary set.

## Related concepts

* [[double negation]]

[[!redirects regular element]]
[[!redirects regular elements]]

[[!redirects regular open]]
[[!redirects regular opens]]
[[!redirects regular open set]]
[[!redirects regular open sets]]
[[!redirects regular open subset]]
[[!redirects regular open subsets]]
[[!redirects regular open subspace]]
[[!redirects regular open subspaces]]

[[!redirects regularisation]]
[[!redirects regularization]]
