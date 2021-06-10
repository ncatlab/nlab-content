
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The evident generalization of the concept of _[[localization of categories]]_ from [[categories]] to [[2-categories]].

## Definition

+-- {: .num_defn #2Localization}
###### Definition
**(localization of a 2-category)**

Let $\mathcal{C}$ be a [[2-category]] and let $W \subset 1Mor(\mathcal{C})$ be a sub-[[class]] of its [[1-morphisms]]. 

Then [[generalized the|the]] the _2-localization_ x is, if it exists, 

1. a [[2-category]] $\mathcal{C}[W^{-1}]$;

1. a [[2-functor]] $\mathcal{C} \overset{\gamma}{\longrightarrow} \mathcal{C}[W^{-1}]$

such that

1. $\gamma$ sends all elements of $W$ to an [[equivalence in a 2-category|equivalence in the 2-category]] $\mathcal{C}[W^{-1}]$;

1. $\gamma$ is [[universal property|universal with this property]]: precomposition with $\gamma$ induces for every [[2-category]] $\mathcal{D}$ an [[equivalence of 2-categories]]

   $$
     (-) \circ \gamma
     \;\colon\;
      2Func(\mathcal{C}[W^{-1}], \mathcal{D})
      \overset{\simeq}{\longrightarrow}
      2Func(\mathcal{C},\mathcal{D})_{W}
      \subset 
      2Func(\mathcal{C}, \mathcal{D})
   $$

   from the [[2-functor 2-category]] from $\mathcal{C}[W^{-1}]$ to $\mathcal{D}$ to the [[full sub-2-category]] of the [[2-functor 2-category]] from $\mathcal{C}$ to $\mathcal{D}$ on those [[2-functors]] that send element of $W$ to [[equivalences in a 2-category|equivalences]].

=--

## Examples

### Homotopy 2-category of combinatorial model categories
  {#Homotopy2CategoryOfCombinatorialModelCategories}

+-- {: .num_example #2CategoryOfModelCategories}
###### Definition
**(the [[2-category]] of [[combinatorial model category|combinatorial]] [[model categories]])**

Write 

1. $ModCat$ for the [[2-category]] whose [[objects]] are [[model categories]], [[1-morphisms]] are [[left adjoint]] [[functors]] of [[Quillen adjunctions]] and [[2-morphisms]] are [[natural transformations]].

1. $CombModCat \subset ModCat$ for the [[full sub-2-category]] on the [[combinatorial model categories]].

=--

+-- {: .num_remark #LocalPresentationOfCombinatorialModelCategories}
###### Remark
**(local presentation of combinatorial model categories)**

By [[Dugger's theorem]], we may choose for every $\mathcal{C} \in CombModCat$ a [[simplicial set]] $\mathcal{S}$ and a [[Quillen equivalence]]

$$
  \mathcal{C}^p
  \;\coloneqq\;
  [\mathcal{S}^{op}, sSet]_{proj,loc}
  \overset{\simeq_{Qu}}{\longrightarrow}
  \mathcal{C}
$$ 

from the local projective [[model structure on sSet-enriched presheaves]] over $\mathcal{S}$.

=--

+-- {: .num_theorem #Homotopy2CategoryOf2CatOfCombinatorialModelCategories}
###### Theorem
**(the [[homotopy 2-category]] of [[combinatorial model categories]])**

The [[2-localization]] (Def. \ref{2Localization}) 

$$
  CombModCat\big[QuillenEquivalences^{-1}\big]
$$ 

of the [[2-category]] of [[combinatorial model categories]] (Def. \ref{2CategoryOfModelCategories}) at the [[Quillen equivalences]] exists. Up to [[equivalence of 2-categories]], it has the same [[objects]] as $CombModCat$ and for any $\mathcal{C}, \mathcal{D} \in CombModCat$ its [[hom-category]] is the [[localization of categories]] 

$$
  CombModCat\big[QuillenEquivalences^{-1}\big](\mathcal{C}, \mathcal{D})
  \;\simeq\;
  ModCat( \mathcal{C}^p, \mathcal{D}^p )\big[\{QuillenHomotopies\}^{-1}\big]
$$

of the category of [[left Quillen functors]] and [[natural transformations]] between local presentations $\mathcal{C}^p$ and $\mathcal{D}^p$ (Remark \ref{LocalPresentationOfCombinatorialModelCategories}) at those [[natural transformation]] that on [[cofibrant objects]] have components that are [[weak equivalences]] ("Quillen homotopies").

=--

This is the statement of [Renaudin 06, theorem 2.3.2](#Renaudin06).



For $\mathcal{C}$ a [[2-category]] write

1. $\mathcal{C}_0$ for the 1-category obtained by discarding all [[2-morphisms]];

1. $\pi_0^{iso}(\mathcal{C})$ for the [[1-category]] obtained by identifying isomorphic [[2-morphisms]].



+-- {: .num_prop}
###### Proposition

The composite 1-functor

$$
  CombModCat_0
   \longrightarrow
  \pi_0^{iso}(CombModCat)
    \overset{\pi_0^{iso}(\gamma)}{\longrightarrow}
  \pi_0^{iso}( CombModCat[QuillenEquivalences^{-1}] )
$$

induced from the [[2-localization]] of Theorem \ref{Homotopy2CategoryOf2CatOfCombinatorialModelCategories} exhibits the ordinary [[localization of a category]] of the 1-category $CombModCat$ at the [[Quillen equivalences]], hence [[Ho(CombModCat)]].

=--

This is the statement of [Renaudin 06, cor. 2.3.8](#Renaudin06).



## Related concepts

* [[bicategory of fractions]]

* [[homotopy 2-category]]


## References

* {#Renaudin06} [[Olivier Renaudin]], Section 1.2 of: *Plongement de certaines théories homotopiques de Quillen dans les dérivateurs*, Journal of Pure and Applied Algebra Volume 213, Issue 10, October 2009, Pages 1916-1935
([arXiv:math/0603339](https://arxiv.org/abs/math/0603339), [doi:10.1016/j.jpaa.2009.02.014](https://doi.org/10.1016/j.jpaa.2009.02.014))

Via [[bicategories of fractions]]:

* [[Dorette A. Pronk]], Section 2 of: _Etendues and stacks as bicategories of fractions_, Comp. Math. **102** 3 (1996) pp.243-303. ([numdam:CM_1996__102_3_243_0](http://www.numdam.org/item/?id=CM_1996__102_3_243_0))


[[!redirects localizations of a 2-category]]
[[!redirects localizations of 2-categories]]

[[!redirects 2-localization of a 2-category]]
[[!redirects 2-localizations of a 2-category]]
[[!redirects 2-localizations 2-categories]]

[[!redirects 2-localization]]
[[!redirects 2-localizations]]

[[!redirects pseudo-localization]]
[[!redirects pseudo-localizations]]

[[!redirects pseudolocalization]]
[[!redirects pseudolocalizations]]

