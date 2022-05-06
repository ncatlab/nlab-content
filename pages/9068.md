

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--
# Contents
* automatic table of contents goes here
{:toc}

##Idea

Just as the concept of a [[dense functor]] is a generalization of [[dense subspace]]. A **codense functor** generalizes the concept of a [[codense subspace]].


## Definition

Let $F\colon A \to B$ be a [[functor]] between [[categories]]. It is **codense** when for each $b \in B$ the following is true:

  $Lim((b \downarrow F) \to A \to B) = b$

(where $(b \downarrow F)$ is a [[comma category]] (in this case the [[under category]]) from $b$ to the functor $F$.

This notion is dual to the notion of [[dense functor]].

Equivalently, a functor $F$ is **codense** iff $Id_B$, together with identity natural transformation $Id_F\colon F \to F$, is the pointwise [[Kan extension]] of $F$ along $F$.

Also, $F$ is **codense** iff  its [[codensity monad]] is the identity.  