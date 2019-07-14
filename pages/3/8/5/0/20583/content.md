# Contents
* table of contents
{: toc}

## Idea

When we define internal categories of some category $\mathcal{C}$ as monads in $\mathrm{Span}(\mathcal{C})$, there is a subtlety concerning the definition of internal functors. It is not the case that the morphisms of monads (namely colax monad morphisms) give us internal functors directly: we need to ask that the 1-cell of the morphism is a left adjoint (which corresponds to asking that the left leg of the span be the identity, or an isomorphism). This is related to the [[profunctor#Properties|behaviour of profunctors]] in that they correspond to functors (via Yoneda) exactly when they are left adjoints. The point, then, is that if we _don't_ require this left-adjoint condition then we end up constructing **Mealy morphisms** between internal categories.

## References

* Robert Paré, "Mealy Morphisms of Enriched Categories", Appl Categor Struct (2012) 20:251--273.