# Definition

Let $F: C \rightleftarrows D : G$ be an [[adjunction]] with unit $\eta$ and counit $\varepsilon$.  Then the following conditions are equivalent:

1. $F \eta$ is a natural isomorphism.
1. $\varepsilon F$ is a natural isomorphism.
1. $G \varepsilon F$ is a natural isomorphism.
1. $G F \eta = \eta G F$.
1. $G F \eta G = \eta G F G$.
1. The duals of each of the above conditions.

When these conditions hold, the adjunction is said to be **idempotent**.  It then follows that $F$ and $G$ restrict to an [[equivalence of categories]] between the [[full images]] of $F$ and of $G$.

# Examples

* Any adjunction between [[posets]] is idempotent.  This is a central fact in the theory of [[Galois connections]].

* The "frame of opens" and "space of points" functors between [[topological spaces]] and [[locales]] form an idempotent adjunction.  The resulting equivalence of categories is between [[sober spaces]] and spatial locales.
