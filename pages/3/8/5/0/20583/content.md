# Contents
* table of contents
{: toc}

## Idea

When we define internal categories of some category $\mathcal{C}$ as monads in $\mathrm{Span}(\mathcal{C})$, there is a subtlety concerning the definition of internal functors. It is not the case that the morphisms of monads (namely colax monad morphisms) give us internal functors directly: we need to ask that the 1-cell of the morphism is a left adjoint in $\mathrm{Span}(\mathcal{C})$ (which corresponds to asking that the left leg of the span be the identity, or an isomorphism). (This is related to the [[profunctor#Properties|behaviour of profunctors]] in that they correspond to functors (via Yoneda) exactly when they are left adjoints.)  If in considering morphisms of monads in $Span(\mathcal{C})$ we _don't_ require this left-adjoint condition then we end up constructing **Mealy morphisms** between internal categories. 

'Mealy morphisms' are  named after [[Mealy machines]], which, in turn, were named after  [[George H. Mealy]].

## References

The notion of Mealy morphism between [[enriched categories]] was introduced in the paper: 

* {#Pare12} [[Robert Paré]], _Mealy Morphisms of Enriched Categories_, Applied Categorical Structures **20** (2012) pp 251--273, doi:[10.1007/s10485-010-9238-8](https://doi.org/10.1007/s10485-010-9238-8).

Mealy morphisms are mentioned in Example 16.8 and Example 16.27 in the paper: 

* {#GarnerShulman16} [[Richard Garner]], [[Michael Shulman]], _Enriched categories as a free cocompletion_, Advances in Mathematics, 289, 2016 ([arXiv:1301.3191](https://arxiv.org/abs/1301.3191), [doi:10.1016/j.aim.2015.11.012](https://doi.org/10.1016/j.aim.2015.11.012))

An application of Mealy morphisms to symmetric [[delta lens|(delta) lenses]] is the topic of the paper: 

* {#Clarke21} [[Bryce Clarke]], _A diagrammatic approach to symmetric lenses_, EPTCS, 333, 2021 ([doi:10.4204/EPTCS.333.6](https://doi.org/10.4204/EPTCS.333.6))

Mealy morphisms are also considered under the name "two-dimensional partial map" (a notion attributed to [[Lawvere]]) in the Appendix of the paper: 

* {#LackStreet02} [[Stephen Lack]], [[Ross Street]], _The formal theory of monads II_, Journal of Pure and Applied Algebra, 175, 2002 ( [doi:10.1016/S0022-4049(02)00137-8](https://doi.org/10.1016/S0022-4049(02)00137-8))

Some talk slides which mention Mealy morphisms: 

* [[Robert Paré]], [Mealy Morphisms for Tensor Categories](https://www.mscs.dal.ca/~pare/June2010.pdf) 

* [[Bryce Clarke]], [Internal lenses as monad morphisms](http://conferences.inf.ed.ac.uk/ct2019/slides/63.pdf)

[[!redirects Mealy morphisms]]