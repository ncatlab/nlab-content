* table of contents
{: toc}


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

When these conditions hold, the adjunction is said to be **idempotent**.  It then follows that $F$ and $G$ restrict to an [[equivalence of categories]] between the [[full images]] of $F$ and of $G$ (which are, respectively, a [[reflective subcategory]] of $D$ and a coreflective subcategory of $C$).

Note that if an idempotent adjunction is [[monadic adjunction|monadic]], then (up to equivalence) it consists of the inclusion and reflection of a [[reflective subcategory]] (i.e. the algebras for an [[idempotent monad]]).  Dually, if it is comonadic, it consists of the inclusion and coreflection of a coreflective subcategory.  Thus, the primary interest in isolating the notion of *idempotent adjunction* is when considering adjunctions which are neither monadic nor comonadic.


# Examples

* Any adjunction between [[posets]] is idempotent.  This is a central fact in the theory of [[Galois connections]].  Thus, in a sense, *non-idempotent* adjunctions are an important new idea arising by the "groupoidal" form of [[vertical categorification]].

* The "frame of opens" and "space of points" functors between [[topological spaces]] and [[locales]] form an idempotent adjunction.  The resulting equivalence of categories is between [[sober spaces]] (which are reflective in [[Top]]) and spatial locales (which are coreflective in [[Loc]]).

* There is an idempotent adjunction (or 2-adjunction) between models of [[material set theory]] and models of [[structural set theory]], although one has to be careful with the exact morphisms one chooses to define the relevant (2-)categories, say $Mat$ and $Struc$.  The left adjoint from $Mat$ to $Struc$ constructs the category of sets in a material set theory, while the right adjoint from $Struc$ to $Mat$ constructs the model of [[pure sets]] as certain extensional relations.

  The resulting reflective subcategory of $Mat$ consists of models satisfying the [[axiom of foundation]] (or [[axiom of anti-foundation|anti-foundation]], depending on the type of extensional relation used) along with the existence of [[transitive closure]]s and [[Mostowski's lemma]].  (In particular, [[ZFC]] suffices.)  This is then equivalent to the coreflective subcategory of $Struc$ consisting of models in which every set can be embedded into an extensional relation of the appropriate type (which may be seen as a structural version of the axiom of (anti)foundation).
