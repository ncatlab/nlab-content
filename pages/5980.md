
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[formal logic]] such as [[type theory]] a _term_ $z$ is an entity/expression of the formal language which is of some [[type]] $Z$. One writes $z : Z$ to express this (a _typing [[judgement]]_). The [[semantics]] of terms in [[Set]] is:  _[[elements]]_ of a [[set]], where one writes $z \in Z$. One also says $z$ is an _inhabitant_ of the type $Z$ and that $Z$ is an _[[inhabited type]]_ if it has a term.

A term $z : Z$ may _depend_ on [[free variables]] $x$ that are themselves terms $x : X$ of some other [[type]] $X$. For instance $z \coloneqq x + 3$ may be a term of type $Z \coloneqq \mathbb{Z}$ (the [[integers]]) which depends on a [[variable]] term $x$ also of type $X \coloneqq \mathbb{Z}$ the integers. The notation for this in the [[metalanguage]] is

$$
  x : X \vdash z : Z
  \,.
$$

Generally here also the type $Z$ itself may depend on the variable $x$ (hence the term $z$ may be of different type depending on its free variables) in which case one says that $z$ is a term of $X$-[[dependent type]].

## Definition

In the [[metalanguage]] of [[type theory]] called [[natural deduction]], terms are what the [[term introduction rules]] produce. 

## Categorical semantics

Here are comments on the interpretation of types in the  [[categorical semantics]] of [[dependent type theory]].

In the [[internal language]] of any [[category]] $C$, a [[morphism]]

$$
  f : B \to A
$$

is a _term_ $f(x)$ of _[[type]]_ $A$ where $x$ is a _free [[variable]]_ of _[[type]]_ $B$, which in [[type theory|type-theoretic]] symbols is given by

$$ 
  x\colon B \vdash f(x)\colon A
  \,.
$$

## Related concepts

* [[element]], [[generalized element]]

* [[dependent term]]

* [[term introduction rule]], [[term elimination rule]]

[[!redirects terms]]
[[!redirects inhabitant]]
[[!redirects inhabitants]]

