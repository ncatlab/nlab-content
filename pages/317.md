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

## Definition

The __terminal category__ or __trivial category__ or __final category__ is [[generalized the|the]] [[terminal object]] in [[Cat]].  It is the unique (up to isomorphism) [[category]] with a single [[object]] and a single [[morphism]], necessarily the [[identity morphism]] on that object. It is often denoted $1$ or $\mathbf{1}$ or $\ast$.

In [[enriched category theory]], often instead of the terminal category one is interested in the [[unit enriched category]].


## Properties

A [[functor]] from the terminal category $1$ to any [[category]] $C$ is the [[equivalence|equivalently]] an [[object]] of $C$.  More generally, the [[functor category]] $[1, C] \simeq C$ from the terminal category to $C$ is canonically [[equivalence of categories|equivalent]] (in fact, isomorphic) to the category $C$ itself.

The terminal category is a [[discrete category]] that, as a [[set]], may be called the _singleton_.  As a [[subset]] of the singleton, it is in fact a [[truth value]], true ($\top$).  In general, all of these (and their analogues in [[higher category theory]] and [[homotopy theory]]) may be called the [[point]].

So far we have interpreted "terminal" as referring to the 1-category $Cat$.  If instead we interpret "terminal" in the [[2-limit|2-categorical]] sense, then any category [[equivalence of categories|equivalent]] to the one-object-one-morphism category described above is also terminal.  A category is terminal in this sense precisely when it is [[inhabited set|inhabited]] and [[indiscrete category|indiscrete]].  For such a category $1$, the functor category $[1,C]$ is equivalent, but not isomorphic, to $C$.

## Related concepts

* [[initial category]]

* [[point]]

[[!redirects trivial category]]
[[!redirects final category]]