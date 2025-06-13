
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]], the notion of resizing the [[type of small propositions]] of a [[type universe]] to being a universe [[small type]]. 

## Definition

\begin{definition}
A [[Russell universe]] $U$ is **propositionally impredicative** or satisfies **propositional impredicativity** if the type of $U$-small propositions $\sum_{X:U} \mathrm{isProp}(X)$ is also $U$-small. 
\end{definition}

\begin{definition}
A [[Tarski universe]] $(U, T)$ is **propositionally impredicative** or satisfies **propositional impredicativity** if the type of $U$-small propositions $\sum_{X:U} \mathrm{isProp}(T(X))$ is [[essentially small type|essentially $U$-small]]. 
\end{definition}

A [[power set]] in $U$ is then just a [[function type]] into the type of $U$-small propositions. The universe of sets $\mathrm{Set}_U$ for $U$ is an [[elementary topos]] with propositional impredicativity.

## Generalizations to the dependent type theory itself

There are two senses in which a dependent type theory itself can be said to satisfy *propositional impredicativity*, generalizing the notion that a single type universe $U$ satisfies propositional impredicativity:

* In dependent type theory with [[type]] [[judgments]], the dependent type theory itself is **propositionally impredicative** or satisfies **propositional impredicativity** if each type judgment has an [[impredicative universe of propositions]]. The dependent type theory itself for each type judgment is thus the [[internal logic]] of the $(\infty,1)$-categorical analogue of an [[elementary topos]]. 

* In dependent type theory with a [[hierarchy of universes]] such that every type is an element of a universe in that hierarchy, the dependent type theory itself is **propositionally impredicative** or has **propositional impredicativity** if every universe $U$ satisfies propositional impredicativity. The universe of sets $\mathrm{Set}_U$ in this case is an [[elementary topos]] for every type universe $U$.

These two senses turn out to be equivalent for type theories with a hierarchy of [[Coquand universes]] and a type judgment for each Coquand universe. To see this, consider the [[inference rules]] for the [[negative type|negative]] [[dependent sum type]] $\sum_{X:U_i} \mathrm{isProp}(X)$ and then the inference rules for the [[impredicative universe of propositions]] $\mathrm{Prop}_i$. They are almost exactly the same, except for the fact that $\mathrm{Prop}_i$ uses type judgments $A \; \mathrm{type}_i$ while $\sum_{X:U_i} \mathrm{isProp}(X)$ uses universe term judgments $A:U_i$ in the [[inference rules]]. These judgments can be transformed into the other through the inference rules of [[Coquand universes]]. 

## Related concepts

* [[type of propositions]]

* [[impredicative polymorphism]]

* [[propositional resizing]]

* [[predicative mathematics]]

* [[taboo]]

## References

* [[Tom de Jong]], [[Martín Hötzel Escardó]], _Domain Theory in Constructive and Predicative Univalent Foundations_, in: _29th EACSL Annual Conference on Computer Science Logic_, [CSL 2021](https://csl2021.fmf.uni-lj.si/), LIPIcs proceedings 183, 2021 ([doi:10.4230/LIPIcs.CSL.2021.28](https://doi.org/10.4230/LIPIcs.CSL.2021.28), [arXiv:2008.01422](https://arxiv.org/abs/2008.01422))

[[!redirects propositional impredicativity]]

[[!redirects propositional resizing]]

[[!redirects axiom of propositional impredicativity]]
[[!redirects axioms of propositional impredicativity]]

[[!redirects propositional impredicativity axiom]]
[[!redirects propositional impredicativity axioms]]

[[!redirects propositionally impredicative universe]]
[[!redirects propositionally impredicative universes]]

[[!redirects propositionally impredicative type theory]]
[[!redirects propositionally impredicative type theory]]

[[!redirects propositionally impredicative dependent type theory]]
[[!redirects propositionally impredicative dependent type theory]]