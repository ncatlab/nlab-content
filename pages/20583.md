# Contents
* table of contents
{: toc}

## Idea

When we define internal categories of some category $\mathcal{C}$ as monads in $\mathrm{Span}(\mathcal{C})$, there is a subtlety concerning the definition of internal functors. It is not the case that the morphisms of monads (namely colax monad morphisms) give us internal functors directly: we need to ask that the 1-cell of the morphism is a left adjoint in $\mathrm{Span}(\mathcal{C})$ (which corresponds to asking that the left leg of the span be the identity, or an isomorphism). (This is related to the [[profunctor#Properties|behaviour of profunctors]] in that they correspond to functors (via Yoneda) exactly when they are left adjoints.)  If in considering morphisms of monads in $Span(\mathcal{C})$ we _don't_ require this left-adjoint condition then we end up constructing **Mealy morphisms** between internal categories. 

'Mealy morphisms' are  named after [[Mealy machines]], which, in turn, were named after  [[George H. Mealy]].

## References

* {#Pare2012} Robert Paré, _Mealy Morphisms of Enriched Categories_, Applied Categorical Structures **20** (2012) pp 251--273, doi:[10.1007/s10485-010-9238-8](https://doi.org/10.1007/s10485-010-9238-8).

* [[Bryce Clarke]], [Internal lenses as monad morphisms](http://conferences.inf.ed.ac.uk/ct2019/slides/63.pdf)

[[!redirects Mealy morphisms]]