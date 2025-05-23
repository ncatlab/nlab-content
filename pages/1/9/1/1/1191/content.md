
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

The discussion here makes sense in the context of the [[axiom of choice]], since only then is the [[collection]] of [[cardinal numbers]] $Card$ [[well-ordered]] and indeed indexed by the collection of [[ordinal numbers]] $Ord$. In particular, we assume the [[law of excluded middle]] and thus use $2$ (instead of $\Omega$ or $Prop$) for the set of [[truth values]] in the definition.

An **inaccessible cardinal** is a [[regular cardinal|regular]] strong [[limit cardinal]].  Here, $\kappa$ is _regular_ if every sum of $\lt\kappa$ cardinals, each of which is $\lt\kappa$, is itself $\lt\kappa$; $\kappa$ is a _strong limit_ if $\lambda\lt \kappa$ implies $2^\lambda\lt\kappa$. In other words, the class of sets of cardinality $\lt\kappa$ is closed under the operations of indexed [[union]]s and taking [[power set]]s.

By this definition, $0$ (the cardinality of the [[empty set]]) and $\aleph_0$ (the cardinality of the set of [[natural number]]s) are both inaccessible.  Usually one explicitly requires inaccessible cardinals to be [[uncountable set|uncountable]], so as to exclude these cases.  One can also justify excluding $0$ by interpreting the requirement that $1 \lt \kappa$ as the nullary part of a requirement whose binary part is closure under indexed unions.

A __weakly inaccessible cardinal__ is a regular weak [[limit cardinal]]; sometimes inaccessible cardinals are called _strongly inaccessible_ in contrast.  Here, $\kappa$ is a _weak limit_ if $\lambda\lt\kappa$ implies $\lambda^+\lt\kappa$, where $\lambda^+$ is the smallest cardinal number $\gt\lambda$.  Every strongly inaccessible cardinal is also weakly inaccessible, while the converse is true assuming the generalized [[continuum hypothesis]].  

## Properties

An (uncountable) cardinal $\kappa$ is inaccessible precisely when the $\kappa$th level $V_\kappa$ of the [[von Neumann hierarchy]] is a [[Grothendieck universe]]  ([Williams](#Williams)), and hence in particular itself a model of axiomatic [[set theory]].  For this reason, the existence of inaccessible cardinals cannot be proven in ordinary axiomatic set theory such as [[ZFC]].  The axiom asserting that there exists an inaccessible (which amounts to the existence of a Grothendieck universe) is thus the beginning of the study of [[large cardinal]]s.  

If one thinks of $\aleph_0$ as already an inaccessible cardinal, then the [[axiom of infinity]] may be seen as itself the first large cardinal axiom.

## Generalisations

### In Boolean toposes

The concept of an inaccessible cardinal can be generalised to any [[Boolean topos]] with choice. Given an [[Boolean topos]] $\mathcal{E}$ where all [[epimorphisms]] are [[split epimorphism|split]], the set of [[cardinals]] $\mathrm{Card}(\mathcal{E})$ is the [[quotient set|quotient]] of the groupoid of objects $\mathrm{Ob}(\mathcal{E})$ by [[existential quantifier|mere existence]] of an [[isomorphism]], with the [[cardinality]] function being the canonical quotient map $t \mapsto \vert t \vert:\mathrm{Ob}(\mathcal{E}) \to \mathrm{Card}(\mathcal{E})$. 
$$\forall x, y \in \mathrm{Ob}(\mathcal{E}), \vert x \vert = \vert y \vert \iff \exists f \in \mathrm{Hom}_\mathcal{E}(x, y).(\exists g \in \mathrm{Hom}_\mathcal{E}(y, x).g \circ f = \mathrm{id}_x) \wedge (\exists h \in \mathrm{Hom}_\mathcal{E}(y, x).f \circ h = \mathrm{id}_y)$$
The same quotient operation leads to a [[poset]] structure on $\mathrm{Card}(\mathcal{E})$ induced by the [[monomorphisms]] in $\mathcal{E}$, and $\mathcal{E}$ being a [[Boolean topos]] implies that the poset structure on $\mathrm{Card}(\mathcal{E})$ is a [[decidable relation|decidable]] [[total order]] with its negation being a [[pseudo-order]]. As a result, the same definitions of a regular cardinal, a strong limit cardinal, and an inaccessible cardinal in set theory can be made in $\mathrm{Card}(\mathcal{E})$. 

An object $x \in \mathrm{Ob}(\mathcal{E})$ is called an **inaccessible object** if its cardinality is inaccessible. 

## Related concepts

* [[regular cardinal]]

* [[product-regular cardinal]]

* [[Grothendieck universe]]

* [[large cardinal]]


## References

Historical review with comprehensive references:

* [[Ralf Krömer]], §6.4.5 in: *Tool and object: A history and philosophy of category theory*, Science Networks. Historical Studies **32** (2007) &lbrack;[doi:10.1007/978-3-7643-7524-9](https://doi.org/10.1007/978-3-7643-7524-9)&rbrack;

See also:

* [[Tom Leinster]], *Large Sets 9*, [web](https://golem.ph.utexas.edu/category/2021/07/large_sets_9.html)

The proof that a Tarski-[[Grothendieck universe]] is equivalently a set of $\kappa$-small sets for $\kappa$ an inaccessible cardinal is in 

* N. H. Williams, _On Grothendieck universes_, Compositio Mathematica, 21:1 (1969) ([numdam]( http://www.numdam.org/item?id=CM_1969__21_1_1_0))
 {#Williams}

* Andreas Blass, Ioanna M. Dimitriou, Benedikt L&#246;we, _Inaccessible cardinals without the axiom of choice_, Fund. Math. 194 (2007) 179-189 [pdf](http://journals.impan.gov.pl/cgi-bin/fm/pdf?fm194-2-03) 

> Abstract: We consider four notions of strong inaccessibility that are equivalent in ZFC and show that they are not equivalent in ZF. 

[[!redirects inaccessible cardinals]]

[[!redirects strongly inaccessible cardinal]]
[[!redirects strongly inaccessible cardinals]]
[[!redirects weakly inaccessible cardinal]]
[[!redirects weakly inaccessible cardinals]]

[[!redirects inaccessible set]]

[[!redirects strongly inaccessible set]]
[[!redirects strongly inaccessible sets]]
[[!redirects weakly inaccessible set]]
[[!redirects weakly inaccessible sets]]

[[!redirects inaccessible object]]

[[!redirects strongly inaccessible object]]
[[!redirects strongly inaccessible objects]]
[[!redirects weakly inaccessible object]]
[[!redirects weakly inaccessible objects]]
