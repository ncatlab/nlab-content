
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

An **inaccessible cardinal** is a [[cardinal number]] $\kappa$ which cannot be "accessed" from smaller cardinals using only the basic operations on cardinals.  It follows that the collection of sets smaller than $\kappa$ satisfies the axioms of set theory.


## Definition

An **inaccessible cardinal** is a [[cardinal number|regular strong limit cardinal]].  Here, $\kappa$ is _regular_ if every sum of $\lt\kappa$ cardinals, each of which is $\lt\kappa$, is itself $\lt\kappa$; $\kappa$ is a _strong limit_ if $\lambda\lt \kappa$ implies $\vert\Omega\vert^\lambda\lt\kappa$, where $\Omega$ is the set of truth values. In other words, the class of sets of cardinality $\lt\kappa$ is closed under the operations of indexed [[union]]s and taking [[power set]]s.

By this definition, $0$ (the cardinality of the [[empty set]]), $1$ (the cardinality of the [[point]]), and $\aleph_0$ (the cardinality of the set of [[natural number]]s) are all inaccessible.  Usually one explicitly requires inaccessible cardinals to be uncountable, so as to exclude these cases.  One can also justify excluding $0$ and $1$ by interpreting the requirement that $1 \lt \kappa$ as the nullary part of a requirement whose binary part is closure under indexed unions.

A __weakly inaccessible cardinal__ is a regular weak limit cardinal; sometimes inaccessible cardinals are called _strongly inaccessible_ in contrast.  Here, $\kappa$ is a _weak limit_ if $\lambda\lt\kappa$ implies $\lambda^+\lt\kappa$, where $\lambda^+$ is the smallest cardinal number $\gt\lambda$.  Every strongly inaccessible cardinal is also weakly inaccessible, while the converse is true assuming the [[continuum hypothesis]].  


## Properties

An (uncountable) cardinal $\kappa$ is inaccessible precisely when the $\kappa$th level $V_\kappa$ of the [[von Neumann hierarchy]] is a [[Grothendieck universe]]  ([Williams](#Williams)), and hence in particular itself a model of axiomatic [[set theory]].  For this reason, the existence of inaccessible cardinals cannot be proven in ordinary axiomatic set theory such as [[ZFC]].  The axiom asserting that there exists an inaccessible (which amounts to the existence of a Grothendieck universe) is thus the beginning of the study of [[large cardinal]]s.  

If one thinks of $\aleph_0$ as already an inaccessible cardinal, then the [[axiom of infinity]] may be seen as itself the first large cardinal axiom.


## References

The proof that a Tarski-[[Grothendieck universe]] is equivalently a set of $\kappa$-small sets for $\kappa$ an inaccessible cardinal is in 

* N. H. Williams, _On Grothendieck universes_, Compositio Mathematica, 21:1 (1969) ([numdam]( http://www.numdam.org/item?id=CM_1969__21_1_1_0))
 {#Williams}

* Andreas Blass, Ioanna M. Dimitriou, Benedikt L&#246;we, _Inaccessible cardinals without the axiom of choice_, Fund. Math. 194 (2007) 179-189 [pdf](http://journals.impan.gov.pl/cgi-bin/fm/pdf?fm194-2-03) 

> Abstract: We consider four notions of strong inaccessibility that are equivalent in ZFC and show that they are not equivalent in ZF. 

[[!redirects inaccessible cardinals]]

[[!redirects strongly inaccessible cardinal]]
[[!redirects strongly inaccessible cardinals]]


