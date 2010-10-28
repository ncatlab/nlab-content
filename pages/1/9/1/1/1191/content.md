
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An **inaccessible cardinal** is a [[cardinal number]] $\kappa$ which cannot be "accessed" from smaller cardinals using only the basic operations on cardinals.  It follows that the collection of sets smaller than $\kappa$ satisfies the axioms of set theory.

## Definition

An **inaccessible cardinal** is a regular strong limit [[cardinal number|cardinal]].  Here, $\kappa$ is _regular_ if every sum of $\lt\kappa$ cardinals, each of which is $\lt\kappa$, is itself $\lt\kappa$; $\kappa$ is a _strong limit_ if $\lambda\lt \kappa$ implies $2^\lambda\lt\kappa$.  In other words, the class of sets of cardinality $\lt\kappa$ is closed under the operations of indexed [[union]]s and taking [[power set]]s.

By this definition, $0$ (the cardinality of the [[empty set]]), $1$ (the cardinality of the [[point]]), and $\aleph_0$ (the cardinality of the set of [[natural number]]s) are all inaccessible.  Usually one explicitly requires inaccessible cardinals to be uncountable, so as to exclude these cases.  One can also justify excluding $0$ and $1$ by interpreting the requirement that $1 \lt \kappa$ as the nullary part of a requirement whose binary part is closure under indexed unions.

A __weakly inaccessible cardinal__ is a regular weak limit cardinal; sometimes inacessible cardinals are called _strongly inaccessible_ in contrast.  Here, $\kappa$ is a _weak limit_ if $\lambda\lt\kappa$ implies $\lambda^+\lt\kappa$, where $\lambda^+$ is the smallest cardinal number $\gt\lambda$.  Every strongly inaccessible cardinal is also weakly inaccessible, while the converse is true assuming the [[continuum hypothesis]].  A weakly inaccessible cardinal may be strengthened to produce a (generally larger) strongly inaccessible cardinal.

+--{: .query}
[[Mike Shulman|Mike]]: What does that last sentence mean?  It seems obviously false to me in the absence of CH.

_Toby_:  It means that if a weakly inaccessible cardinal exists, then a strongly inaccessible cardinal exists, but I couldn\'t find the formula for it.  Something like $\beth_\kappa$ is strongly inaccessible if $\kappa$ is weakly inaccessible (note that $\aleph_\kappa = \kappa$ then), but I couldn\'t verify that (or check how it holds up in the absence of choice).

[[Mike Shulman|Mike]]: I don't believe that.  Suppose that the smallest weakly inaccessible is not strongly inaccessible, and let $\kappa$ be the smallest strongly inaccessible.  Then $V_\kappa$ is a model of set theory in which there are weakly inaccessibles but not strong ones.  I'm almost certain there is no reason for the smallest weakly inaccessible to be strongly inaccessible.
=--

## Properties

A cardinal $\kappa$ is inaccessible precisely when the $\kappa$th level $V_\kappa$ of the [[von Neumann hierarchy]] is a [[Grothendieck universe]], and hence in particular itself a model of axiomatic [[set theory]].  For this reason, the existence of inaccessible cardinals cannot be proven in ordinary axiomatic set theory such as [[ZFC]].  The axiom asserting that there exists an inaccessible (which amounts to the existence of a Grothendieck universe) is thus the beginning of the study of [[large cardinal]]s.  If one thinks of $\aleph_0$ as already an inaccessible cardinal, then the [[axiom of infinity]] may be seen as itself the first large cardinal axiom.
