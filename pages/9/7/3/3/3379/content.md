# Definition

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

When these conditions hold, the adjunction is said to be **idempotent**.  It then follows that $F$ and $G$ restrict to an [[equivalence of categories]] between the [[full images]] of $F$ and of $G$.

# Examples

* Any adjunction between [[posets]] is idempotent.  This is a central fact in the theory of [[Galois connections]].

* The "frame of opens" and "space of points" functors between [[topological spaces]] and [[locales]] form an idempotent adjunction.  The resulting equivalence of categories is between [[sober spaces]] and spatial locales.
