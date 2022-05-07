
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of _[[model categories]]_ is one way of formulating the concept of certain classes of _[[homotopy theories]]_ or _[[(∞,1)-categories]]_. One way to make this precise while staying strictly within the context of [[1-category|1-]][[category theory]] is to consider the [[homotopy category]] of the ([[very large category|very large]]) category of [[model categories]] of (left) [[Quillen functors]] between them, hence its [[localization of a category]] at the [[Quillen equivalences]].

This should be particularly well-behaved for the sub-category $CombModCat$ of [[combinatorial model categories]]. Due to [[Dugger's theorem]], it should be true that 

$$
  Ho(CombModCat)
  \;\coloneqq\;
  CombModCat\big[QuillenEquivs^{-1}\big]
  \;\simeq\;
  Ho(Pr(\infty,1)Cat)
$$

is [[equivalence of categories|equivalent]] to the [[homotopy category of an (infinity,1)-category]] of [[Pr(∞,1)Cat]], the [[(∞,1)-category]] of [[locally presentable (∞,1)-categories]] and [[(∞,1)-colimit]]-[[preserved limit|preserving]] [[(∞,1)-functors]] between them. At least when the latter is formalized in terms of [[derivators]], then this is proven in [Renaudin 06](#Renaudin06), see Corollary \ref{EquivalenceToHoPrDer} below.

## Details

+-- {: .num_example #2CategoryOfModelCategories}
###### Definition
**(the [[2-category]] of [[combinatorial model category|combinatorial]] [[model categories]])**

Write 

1. $ModCat$ for the [[2-category]] whose [[objects]] are [[model categories]], whose [[1-morphisms]] are [[left Quillen functors]] and [[2-morphisms]] are [[natural transformations]].

1. $CombModCat \subset ModCat$ for the [[full sub-2-category]] on the [[combinatorial model categories]].

=--

+-- {: .num_remark #LocalPresentationOfCombinatorialModelCategories}
###### Remark
**(local presentation of combinatorial model categories)**

By [[Dugger's theorem]], we may choose for every $\mathcal{C} \in CombModCat$ an [[sSet-category]] $\mathcal{S}$ and a [[Quillen equivalence]]

$$
  \mathcal{C}^p
  \;\coloneqq\;
  [\mathcal{S}^{op}, sSet]_{proj,loc}
  \overset{\simeq_{Qu}}{\longrightarrow}
  \mathcal{C}
$$ 

from the local projective [[model structure on sSet-enriched presheaves]] over $\mathcal{S}$.

=--

+-- {: .num_prop #Homotopy2CategoryOf2CatOfCombinatorialModelCategories}
###### Proposition
**(the [[homotopy 2-category]] of [[combinatorial model categories]])**

The [[2-localization of a 2-category]] 

$$
  CombModCat\big[QuillenEquivs^{-1}\big]
$$ 

of the [[2-category]] of [[combinatorial model categories]] (Def. \ref{2CategoryOfModelCategories}) at the [[Quillen equivalences]] exists. Up to [[equivalence of 2-categories]], it has the same [[objects]] as $CombModCat$ and for any $\mathcal{C}, \mathcal{D} \in CombModCat$ its [[hom-category]] is the [[localization of categories]] 

$$
  CombModCat\big[QuillenEquivs^{-1}\big](\mathcal{C}, \mathcal{D})
  \;\simeq\;
  ModCat( \mathcal{C}^p, \mathcal{D}^p )\big[\{QuillenHomotopies\}^{-1}\big]
$$

of the category of [[left Quillen functors]] and [[natural transformations]] between local presentations $\mathcal{C}^p$ and $\mathcal{D}^p$ (Remark \ref{LocalPresentationOfCombinatorialModelCategories}) at those [[natural transformation]] that on [[cofibrant objects]] have components that are [[weak equivalences]] ("Quillen homotopies").

=--

This is the statement of [Renaudin 06, theorem 2.3.2](#Renaudin06).



+-- {: .num_prop #}
###### Proposition

There is an [[equivalence of 2-categories]]

$$
  CombModCat\big[ QuillenEquivs^{-1} \big]
  \;\simeq\;
  PresentableDerivators
$$

between the [[homotopy 2-category]] of [[combinatorial model categories]] (Prop. \ref{Homotopy2CategoryOf2CatOfCombinatorialModelCategories}) and the 2-category of presentable [[derivators]] with left adjoint morphisms between them.

=--

This is the statement of [Renaudin 06, theorem 3.4.4](#Renaudin06).


For $\mathcal{C}$ a [[2-category]] write

1. $\mathcal{C}_1$ for the 1-category obtained by discarding all [[2-morphisms]];

1. $\pi_0^{iso}(\mathcal{C})$ for the [[1-category]] obtained by identifying isomorphic [[2-morphisms]].



+-- {: .num_prop}
###### Proposition
**([[localization]] of $CombModCat$ at the [[Quillen equivalences]])**

The composite 1-functor

$$
  CombModCat_1
   \longrightarrow
  \pi_0^{iso}(CombModCat)
    \overset{\pi_0^{iso}(\gamma)}{\longrightarrow}
  \pi_0^{iso}( CombModCat[QuillenEquivs^{-1}] )
$$

induced from the [[2-localization]] of Prop. \ref{Homotopy2CategoryOf2CatOfCombinatorialModelCategories} exhibits the ordinary [[localization of a category]] of the 1-category $CombModCat$ at the [[Quillen equivalences]], hence [[Ho(CombModCat)]]:

$$
  Ho(CombModCat)
  \;\coloneqq\;
  CombModCat_1\big[ QuillenEquivs^{-1} \big]
  \simeq
  \pi_0^{iso}( CombModCat[QuillenEquivs^{-1}] )
  \,.
$$

Moreover, this localization inverts precisely (only) the [[Quillen equivalences]].


=--

This is the statement of [Renaudin 06, cor. 2.3.8 with prop. 2.3.4](#Renaudin06).


+-- {: .num_cor #EquivalenceToHoPrDer}
###### Corollary

There is an [[equivalence of categories]]

$$
  Ho(CombModCat)
  \;\simeq\;
  Ho(PresentableDerivators)
$$

between the [[homotopy category]] of [[combinatorial model categories]] and that of presentable [[derivators]] with left adjoint morphisms between them.

=--


## Related concepts

* [[PrCat]], [[Pr(∞,1)Cat]]

* [[Ho(Cat)]]

* [[double category of model categories]]

[[!include locally presentable categories - table]]


## References

* {#Renaudin06} [[Olivier Renaudin]], *Plongement de certaines théories homotopiques de Quillen dans les dérivateurs*, Journal of Pure and Applied Algebra Volume 213, Issue 10, October 2009, Pages 1916-1935
([arXiv:math/0603339](https://arxiv.org/abs/math/0603339), [doi:10.1016/j.jpaa.2009.02.014](https://doi.org/10.1016/j.jpaa.2009.02.014))
