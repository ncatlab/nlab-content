## Idea

An equivalence of dg-categories is in an [[equivalence in an (infinity,1)-category|equivalence]] in the [[(infinity,1)-category of dg-categories]]. They are analogous to [[Dwyer-Kan equivalences of simplicial categories]].

## Definition

Let $u : C \to D$ be a functor of [[dg-categories]].

+-- {: .un_defn}
###### Definition
The functor $u$ is called **fully faithful** if for all objects $x,y \in C$ the canonical morphisms of [[mapping complexes]]
  $$ Map(x,y) \longrightarrow Map(u(x), u(y)) $$
are [[quasi-isomorphisms]] of [[chain complexes]].

The functor $u$ is called **essentially surjective** if the induced functor on the [[homotopy category of a dg-category|homotopy categories]] is [[essentially surjective]].

The functor $u$ is called an **equivalence** or **Dwyer-Kan equivalence** if it is fully faithful and essentially surjective.
=--

In the literature the term _quasi-equivalence_ is often used for this notion.

Equivalences are [[dg-categories]] are precisely the [[equivalences in an (infinity,1)-category|equivalences]] in the [[(infinity,1)-category of dg-categories]], which is presented by the [[Dwyer-Kan model structure on dg-categories]].

## References

See the references at [[dg-category]].

[[!redirects equivalences of dg-categories]]
[[!redirects quasi-equivalence of dg-categories]]
[[!redirects quasi-equivalences of dg-categories]]
[[!redirects Dwyer-Kan equivalence of dg-categories]]
[[!redirects Dwyer-Kan equivalences of dg-categories]]