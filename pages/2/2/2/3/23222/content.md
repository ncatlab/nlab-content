[[!redirects empty 210]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Compact objects
+-- {: .hide}
[[!include compact object - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

A _locally strongly finitely presentable category_ is like a [[locally finitely presentable category]], but where the class of [[filtered colimits]] (respectively the class of [[finite limits]]) is replaced by the class of [[sifted colimits]] (respectively the class of [[finite products]]).

Locally strongly finitely presentable category are precisely those categories equivalent to [[varieties of algebras]].

## Definition

A category $C$ satisfying (any of) the following equivalent conditions is said to be __locally strongly finitely presentable__ (or **lsfp**):

1. $C$ is the [[free cocompletion]] of a [[small category]] with [[finite coproducts]] under [[sifted colimits]]: see [[sind-object]].
1. $C$ has all small [[colimit|colimits]], the category $C_{sfp}$ is [[essentially small category|essentially small]], and any object in $C$ is a [[sifted colimit]] of the canonical diagram of strongly finitely presentable objects mapping into it.
1. $C$ is the category of models for an [[algebraic theory]].
1. $C$ is the category of models for a finite product [[sketch]].
1. $C_{sfp}$ has finite coproducts, and the restricted [[Yoneda embedding]] $C\hookrightarrow [C_{sfp}^{op},Set]$ identifies $C$ with the category of finite-product-preserving functors $C_{fp}^{op} \to Set$.

## Related pages

- [[sind-object]]
- [[locally finitely presentable category]]
- [[sifted category]]

## References

*  [[Jiri Adamek]], [[Jiri Rosicky]], _On sifted colimits and generalized varieties_, TAC **8** (2001) pp.33-53. ([tac](http://www.tac.mta.ca/tac/volumes/8/n3/8-03abs.html))

*  [[Jiri Adamek]], [[Jiri Rosicky]], [[Enrico Vitale]], _What are sifted colimits?_, TAC __23__ (2010) pp. 251--260. ([tac](http://www.tac.mta.ca/tac/volumes/23/13/23-13abs.html))

* [[Jiri Adamek]], [[Jiri Rosicky]], [[Enrico Vitale]], _Algebraic Theories - a Categorical Introduction to General Algebra_ , Cambrige UP 2010. (ch. 2) ([draft](https://perso.uclouvain.be/enrico.vitale/gab_CUP2.pdf))
