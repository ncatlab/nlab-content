## Idea

_dg-localization_ is the analogue in the world of [[dg-categories]] to the notion of [[simplicial localization]]. In good cases it is [[dg-category presented by a model category|presented]] by a [[dg-model category]].

## Definition

+-- {: .un_defn}
###### Definition
The **dg-localization** of a [[dg-category]] $T$ at a subset of morphisms $S$ is the data of a morphism
  $$ \gamma : T \longrightarrow T[S^{-1}] $$
in the [[(infinity,1)-category of dg-categories]] $dg-cat$ such that for any [[dg-category]] $T' \in dg-cat$ the induced morphism
  $$ \gamma^* : Map(T[S^{-1}], T')
       \longrightarrow Map(T, T') $$
of [[mapping spaces]] is [[injective]] on [[connected components]] and has [[image]] the subset of morphisms $T \to T'$ in $dgcat$ that send morphisms of $S$ to [[equivalences]] in $T'$.
=--

+-- {: .un_proposition}
###### Proposition (Toen)
The dg-localization of any [[dg-category]] at a set of [[morphisms]] exists.
=--

## Related concepts

* [[dg-quotient]]
* [[simplicial localization]]

## References

See section 8.2 of

* [[B. Toen]], _The homotopy theory of dg-categories and derived Morita theory_, [arXiv:math/0408337](http://arxiv.org/abs/math/0408337).

and section 4.3 of

* [[B. Toen]], _Lectures on dg-categories_, [pdf](http://www.hamilton.tcd.ie/events/swisk.pdf).