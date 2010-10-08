# Idempotent adjunctions

* table of contents
{: toc}


## Definition

Let $F: C \rightleftarrows D : G$ be an [[adjunction]] with unit $\eta$ and counit $\varepsilon$.  Then the following conditions are equivalent:

1. $F \eta$ is a natural isomorphism.
1. $\varepsilon F$ is a natural isomorphism.
1. $G \varepsilon F$ is a natural isomorphism &#8212; i.e. the [[monad]] induced by the adjunction is [[idempotent monad|idempotent]].
1. $G F \eta = \eta G F$.
1. $G F \eta G = \eta G F G$.
1. $G\varepsilon$ is a natural isomorphism.
1. $\eta G$ is a natural isomorphism.
1. $F \eta G$ is a natural isomorphism &#8212; i.e. the [[comonad]] induced by the adjunction is idempotent.
1. $F G \varepsilon = \varepsilon F G$.
1. $F G \varepsilon F = \varepsilon F G F$.
1. The adjunction can be factored as a composite $C \underoverset{G_1}{F_1}{\rightleftarrows} E \underoverset{G_2}{F_2}{\rightleftarrows} D$ where $F_2$ and $G_1$ are [[fully faithful functor|fully faithful]], i.e. $F_1\dashv G_1$ is a [[reflective subcategory|reflection]] and $F_2 \vdash G_2$ is a coreflection.

When these conditions hold, the adjunction is said to be **idempotent**.  It then follows that $F$ and $G$ restrict to an [[equivalence of categories]] between the [[full images]] of $F$ and of $G$ (which are, respectively, a [[reflective subcategory]] of $D$ and a coreflective subcategory of $C$).

Note that if an idempotent adjunction is [[monadic adjunction|monadic]], then (up to equivalence) it consists of the inclusion and reflection of a [[reflective subcategory]] (i.e. the algebras for an [[idempotent monad]]).  Dually, if it is [[comonadic adjunction|comonadic]], it consists of the inclusion and coreflection of a [[coreflective subcategory]].  Thus, the primary interest in isolating the notion of *idempotent adjunction* is when considering adjunctions which are neither monadic nor comonadic.


## Examples

* Any adjunction between [[posets]] is idempotent.  This is a central fact in the theory of [[Galois connections]].  Thus, in a sense, *non-idempotent* adjunctions are an important new idea arising by the "groupoidal" form of [[vertical categorification]].

* More generally, an adjunction in which the [[full image]] of either functor is a poset must be idempotent.  This follows from conditions 4, 5, 9, and 10 above.  This fact arises when constructing [[generalized kernel]]s.

* The "frame of opens" and "space of points" functors between [[topological spaces]] and [[locales]] form an idempotent adjunction.  The resulting equivalence of categories is between [[sober spaces]] (which are reflective in [[Top]]) and spatial locales (which are coreflective in [[Loc]]).

* For any [[topological space]] $X$, there is an idempotent adjunction between the category $[O(X)^{\op}, Set]$ of [[presheaves]] on $X$ and the category $Top/X$ of spaces over $X$ (the right adjoint gives the presheaf of [[sections]] of a space over $X$).  The resulting equivalence of categories is between [[sheaves]] in the modern sense of presheaves satisfying [[descent]], and sheaves in the original sense as [[étalé spaces]].  See [this blog post](http://golem.ph.utexas.edu/category/2010/02/sheaves_do_not_belong_to_algeb.html).

* The [[material-structural adjunction]] between [[material set theory|material set theories]] and [[structural set theory|structural set theories]] is idempotent.  The fixed categories consist of the models satisfying appropriate versions of the [[axiom of foundation]] or anti-foundation.


## References

??
