
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
=--
=--

\tableofcontents

## Idea

In [[dependent type theory]], the notion of resizing the [[type of small propositions]] of a [[type universe]] to being a universe [[small type]]. 

## Definition

\begin{definition}
A [[Russell universe]] $U$ satisfies **propositional impredicativity** if the type of $U$-small propositions $\sum_{X:U} \mathrm{isProp}(X)$ is also $U$-small. 
\end{definition}

\begin{definition}
A [[Tarski universe]] $(U, T)$ satisfies **propositional impredicativity** if the type of $U$-small propositions $\sum_{X:U} \mathrm{isProp}(T(X))$ is [[essentially small type|essentially $U$-small]]. 
\end{definition}

A [[power set]] in $U$ is then just a [[function type]] into the type of $U$-small propositions. 

In dependent type theory where for every type $A$, there is a [[type universe]] $U$ such that $A$ is (essentially) $U$-small, one can also say that the dependent type theory itself has **propositional impredicativity** if every universe $U$ satisfies propositional impredicativity.  

## Related concepts

* [[type of propositions]]

* [[impredicative polymorphism]]

* [[propositional resizing]]

## References

* [[Tom de Jong]], [[Martín Hötzel Escardó]], _Domain Theory in Constructive and Predicative Univalent Foundations_, in: _29th EACSL Annual Conference on Computer Science Logic_, [CSL 2021](https://csl2021.fmf.uni-lj.si/), LIPIcs proceedings 183, 2021 ([doi:10.4230/LIPIcs.CSL.2021.28](https://doi.org/10.4230/LIPIcs.CSL.2021.28), [arXiv:2008.01422](https://arxiv.org/abs/2008.01422))

[[!redirects propositional impredicativity]]

[[!redirects propositionally impredicative universe]]
[[!redirects propositionally impredicative universes]]

[[!redirects propositionally impredicative universe]]
[[!redirects propositionally impredicative universes]]