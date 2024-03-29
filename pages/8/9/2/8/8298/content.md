
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _projective presentation_ of an [[object]] is a realization of that object as a suitable [[quotient]] of a [[projective object]]. 

In [[homological algebra]] projective presentations can sometimes be used in place of genuine [[projective resolutions]] in the computation of [[derived functors]]. See for instance at _[[Ext-functor]]_ for examples.

The [[duality|dual]] notion is that of [[injective presentation]].

## Definition

### In abelian categories

Let $\mathcal{A}$ be an [[abelian category]]. For $X \in \mathcal{A}$ any [[object]], a _projective presentation_ of $X$ is a [[short exact sequence]] of the form

$$
  0 \to N \stackrel{i}{\hookrightarrow}
  P \stackrel{p}{\to}
  X \to 0
  \,,
$$

hence exhibiting $X$ as the [[cokernel]]

$$
  X \simeq coker(N \hookrightarrow P)
$$

such that  $P$ is a [[projective object]].

## Related concepts

* [[projective object]], **projective presentation**, [[projective cover]], [[projective resolution]]

  * [[projective module]]

* [[injective object]], [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * [[injective module]]

* [[free object]], [[free resolution]]
 
  * [[free module]]

* flat object, [[flat resolution]]

  * [[flat module]]


[[!redirects projective presentations]]
