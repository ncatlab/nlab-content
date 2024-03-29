
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

In [[dependent type theory]], there are two notions of [[equality]], 

1. *strict* or *[[judgmental equality]]*,

1. *weak* or *[[typal equality]]*. 

Accordingly there are two corresponding notions of [[propositions]] or [[subsingletons]]:

1. The usual notion of proposition, [[h-propositions]], are the types $A$ where every two elements $a:A$ and $b:A$ are typally equal to each other $p(a, b):a =_A b$. 

1. *Strict propositions*, which are the types $A$ where every two elements $a:A$ and $b:A$ are [[judgemental equality|judgmentally equal]] to each other $a \equiv b:A$. 

Strict propositions are used to formalize [[logic over type theory]] in [[dependent type theory]] without having to postulate a separate proposition judgment, since strict propositions are judgmentally [[proof relevance|proof irrelevant]], and thus behave as propositions in traditional [[propositional logic]]. 

## Examples

* The [[empty type]] is a strict proposition.

* The strict [[unit type]] with judgmental [[computation rules]] is a strict proposition. 

* The [[squash type]] of any type is a strict proposition.


## Related concepts

* [[judgmental equality]]

* [[mere proposition]]

* [[squash type]]

* [[type of strict propositions]]

* [[strict singleton]]

## References

* [[Gaëtan Gilbert]], [[Jesper Cockx]], [[Matthieu Sozeau]], [[Nicolas Tabareau]], *Definitional Proof-Irrelevance without K*. Proceedings of the ACM on Programming Languages, Volume 3, Issue POPL, Article 3, pp 1–28, January 2019. ([doi:10.1145/3290316](https://doi.org/10.1145/3290316))

[[!redirects strict proposition]]
[[!redirects strict propositions]]