# Contents
* table of contents
{: toc}

## Overview

It is expected that every [[elementary (infinity,1)-topos]] admits a model of homotopy type theory with the [[univalence axiom]] and [[higher inductive types]].  However, so far there is not a standard definition of elementary $(\infty,1)$-topos.  We do *almost* know that every [[Grothendieck (infinity,1)-topos]] admits such a model; the caveat is that we only get univalent [[universes]] that are *weakly a la Tarski* (see [[universe]]).

## Right proper Cisinski model categories

A [[Cisinski model category]] is a [[model category]] on a Grothendieck 1-topos whose cofibrations are the monomorphisms.  It is [[proper model category|right proper]] if weak equivalences are preserved by pullback along fibrations.  This ensures that the adjunctions $f^* \dashv f_*$ for a fibration $f$ are [[Quillen adjunctions]], so that the $(\infty,1)$-category presented by the model category is locally cartesian closed.

The fibrant objects in a right proper Cisinski model category can be shown to form a comprehension category, one of the structures used for [[semantics]] of type theory, which admits all the structure necessary to model the type-forming operations of the [[dependent type|dependent sum type]], [[dependent type|dependent product type]], and [[identity type|identity type]] (the latter by using path objects).  By applying the [[local universe model]] or [[natural model]] coherence theorem, we see that any right proper Cisinski model category models type theory.

Cisinski and Gepner-Kock have also shown that any locally presentable, locally cartesian closed $(\infty,1)$-category can be presented by a right proper Cisinski model category.  Therefore, any such $(\infty,1)$-category admits a model of type theory.

## Higher inductive types

Models of higher inductive types can be constructed in any simplicial combinatorial model category; for now, see the note at [[higher inductive types]].

## Strong univalent universes

In some cases we can construct a univalent universe which satisfies the rules to be a "strong" universe a la Tarski.  This means we have an object $U$ together with a fibration $\tilde{U}\to U$, which is "closed under the type-forming operations" up to isomorphism.  For instance, if $B\to A$ is a pullback of $\tilde{U}$ along some map $A\to U$, and likewise $C\to B$ is a pullback of $\tilde{U}$ along some map $B\to U$, then the composite $C\to A$ is a pullback of $\tilde{U}$ along some map $A\to U$.  In particular, we can apply this to the "generic" composable pair of fibrations over $U^{(1)}$, the "type of composable fibrations", to get a classifying map $U^{(1)}\to U$ of the composite that interprets the $\Sigma$-type former on the universe.  The requirements for $\Pi$-types and identity types are similar.  

In practice, the way we ensure these requirements is to show that a fibration is a pullback of $\tilde{U}\to U$ if and only if its "fibers" are bounded by some cardinal number $\kappa$ (used in defining $U$).  Then as long as $\kappa$ is inaccessible, such fibrations will be closed under the type-forming operations.

Strong univalent universes are known to exist in the Reedy model category $sSet^{R^op}$ of simplicial presheaves on an [[elegant Reedy category]] $R$; see [this paper](http://arxiv.org/abs/1203.3253) and [this paper](http://arxiv.org/abs/1307.6248).

## Weak univalent universes

Suppose we have any right proper Cisinski model category that presents a Grothendieck $(\infty,1)$-topos; we will show that it models a [[univalent]] [[universe]] which is "[[weakly Tarski universe|weakly a la Tarski]]".  (Since any Grothendieck $(\infty,1)$-topos is locally cartesian closed, such a model category always exists as remarked above.)

It is known that for any regular $\kappa$, an $(\infty,1)$-topos has an [[object classifier]] for $\kappa$-small morphisms, i.e. a $\kappa$-small morphism $\tilde{V}\to V$ such that for any object $A$, the space of maps $A\to V$ is naturally equivalent to the core of the category of $\kappa$-small morphisms into $A$.

Let $\kappa$ be inaccessible, and let $\tilde{U} \to U$ be a fibration between fibrant objects of the model category that represents $\tilde{V}\to V$.  Then since $\kappa$-small morphisms in the $(\infty,1)$-topos are closed under composition, diagonals, and dependent products, the fibrations in the model category that are homotopy pullbacks of $\tilde{U}\to U$ are also so closed.  In particular, we can again build the universal composable pair over $U^{(1)}$ and obtain a map $U^{(1)}\to U$ which classifies its composite *up to homotopy* (i.e. so that the composite is a homotopy pullback of $\tilde{U}\to U$ along it).  Dependent products and identity types are similar.

Thus, if we use the local universe coherence theorem, $U$ represents a "universe" which comes with type-forming "operations", but these operations do not literally respect the actual type-formers on actual types.  Instead we can say only that $El(\Sigma A B)$ is *equivalent* to $\Sigma (El A) (El B)$, and so on.  However, we can still define a map $Id_U(A,B) \to Equiv(El(A),El(B))$, and the full universal property of the object classifier implies that it is an equivalence (see for instance [Gepner-Kock](http://arxiv.org/abs/1208.1749)).  Thus, we have a univalent universe which is "weakly a la Tarski".

## Related entries

* [[Awodey's proposal]]

## References

* [[Denis-Charles Cisinski]], _Univalent universes for elegant models of homotopy types_, 2014 [PDF](http://arxiv.org/pdf/1406.0058)

