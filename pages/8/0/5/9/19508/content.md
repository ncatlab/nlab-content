
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

is [[equivalence of categories|equivalent]] to the [[homotopy category of an (infinity,1)-category|homotopy category]] of [[Pr(∞,1)Cat]], the [[(∞,1)-category]] of [[locally presentable (∞,1)-categories]] and [[(∞,1)-colimit]]-[[preserved limit|preserving]] [[(∞,1)-functors]] between them. 

A proof for this statement, not just for [[homotopy categories]] but for the full homotopy theories ([[(infinity,1)-categories|$(\infty,1)$-categories]]), is now claimed in [Pavlov 2021](#Pavlov21).

An anlogous equivalence, but with presentable [[derivators]] and just at the level of [[homotopy 2-categories]], is due to  [Renaudin 06](#Renaudin06), see Corollary \ref{EquivalenceToHoPrDer} below.


## Definition and 2-localization
 {#Details}

\begin{definition}
\label{2CategoryOfModelCategories}
**([[2-category]] of [[combinatorial model category|combinatorial]] [[model categories]])**

Write 

1. $ModCat$ for the [[2-category]] whose [[objects]] are [[model categories]], whose [[1-morphisms]] are [[left Quillen functors]] and [[2-morphisms]] are [[natural transformations]].

1. $\Delta ModCat$ for the [[2-category]] whose [[objects]] are [[simplicial model categories]] ([[classical model structure on simplicial sets|$sSet_{Qh}$]]-[[enriched model categories]]), whose [[1-morphisms]] are [[simplicial Quillen adjunction|simplicial]] [[left Quillen functors]] and [[2-morphisms]] are [[natural transformations]].


1. $CombModCat \subset ModCat$ and $\Delta CombModCa \subset \Delta ModCa$ for the [[full sub-2-categories]] on the [[left proper model categories|left proper]] [[combinatorial model categories]],

1. $LPropCombModCat \subset CombModCat$ and $LPropCombModCat \subset CombModCat$ for the further [[full sub-2-categories]] on the [[left proper model categories|left proper]] [[combinatorial model categories]].

\end{definition}


\begin{remark}
\label{LocalPresentationOfCombinatorialModelCategories}
**(local presentation of combinatorial model categories)**
\linebreak
By [[Dugger's theorem]], we may choose for every $\mathcal{C} \in CombModCat$ (Def. \ref{2CategoryOfModelCategories}) an [[sSet-category]] $\mathcal{S}$ and a [[Quillen equivalence]]

$$
  \mathcal{C}^p
  \;\coloneqq\;
  [\mathcal{S}^{op}, sSet]_{proj,loc}
  \overset{\simeq_{Qu}}{\longrightarrow}
  \mathcal{C}
$$ 

from the local projective [[model structure on sSet-enriched presheaves]] over $\mathcal{S}$. The latter is still a [[combinatorial model category]] but is also a [[left proper model category|left proper]] [[simplicial model category]].
\end{remark}



\begin{prop}
\label{Homotopy2CategoryOf2CatOfCombinatorialModelCategories}
**(the [[homotopy 2-category]] of [[combinatorial model categories]])**

The [[2-localization of a 2-category]] 

$$
  LPropCombModCat\big[QuillenEquivs^{-1}\big]
$$ 

of the [[2-category]] of [[left proper model category|left proper] [[combinatorial model categories]] (Def. \ref{2CategoryOfModelCategories}) at the [[Quillen equivalences]] exists. Up to [[equivalence of 2-categories]], it has the same [[objects]] as $CombModCat$ and for any $\mathcal{C}, \mathcal{D} \in CombModCat$ its [[hom-category]] is the [[localization of categories]] 

$$
  LPropCombModCat\big[QuillenEquivs^{-1}\big](\mathcal{C}, \mathcal{D})
  \;\simeq\;
  ModCat( \mathcal{C}^p, \mathcal{D}^p )\big[\{QuillenHomotopies\}^{-1}\big]
$$

of the category of [[left Quillen functors]] and [[natural transformations]] between local presentations $\mathcal{C}^p$ and $\mathcal{D}^p$ (Remark \ref{LocalPresentationOfCombinatorialModelCategories}) at those [[natural transformation]] that on [[cofibrant objects]] have components that are [[weak equivalences]] ("Quillen homotopies").
\end{prop}

This is the statement of [Renaudin 06, theorem 2.3.2](#Renaudin06).[^1]


## Relation to derivators

+-- {: .num_prop #}
###### Proposition

There is an [[equivalence of 2-categories]]

$$
  LPropCombModCat\big[ QuillenEquivs^{-1} \big]
  \;\simeq\;
  PresentableDerivators
$$

between the [[homotopy 2-category]] of [[combinatorial model categories]] (Prop. \ref{Homotopy2CategoryOf2CatOfCombinatorialModelCategories}) and the 2-category of presentable [[derivators]] with left adjoint morphisms between them.

=--

This is the statement of [Renaudin 06, theorem 3.4.4](#Renaudin06).[^1]


For $\mathcal{C}$ a [[2-category]] write

1. $\mathcal{C}_1$ for the 1-category obtained by discarding all [[2-morphisms]];

1. $\pi_0^{iso}(\mathcal{C})$ for the [[1-category]] obtained by identifying isomorphic [[2-morphisms]].



+-- {: .num_prop}
###### Proposition
**([[localization]] of $CombModCat$ at the [[Quillen equivalences]])**

The composite 1-functor

$$
  LPropCombModCat_1
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

* [[formal (infinity,1)-category theory|formal $\infty$-category theory]]

* [[2-model category]]

* [[Ho(Cat)]]

* [[double category of model categories]]

* [[Quillen adjoint triple]]

* [[PrCat]], [[Pr(∞,1)Cat]]


[[!include locally presentable categories - table]]


## References
 {#References}

The equivalence of the [[homotopy 2-category]] of [[combinatorial model categories]] with that of presentable [[derivators]] is due to:

* {#Renaudin06} [[Olivier Renaudin]], *Plongement de certaines théories homotopiques de Quillen dans les dérivateurs*, Journal of Pure and Applied Algebra Volume 213, Issue 10, October 2009, Pages 1916-1935
([arXiv:math/0603339](https://arxiv.org/abs/math/0603339), [doi:10.1016/j.jpaa.2009.02.014](https://doi.org/10.1016/j.jpaa.2009.02.014))

  > Beware that, for the time being, the entry [above](#Details) is referring to the numbering in the arXiv version of [Renaudin 2006](#Renaudin06), which differs from that in the published version.

The equivalence of the full homotopy theory (in particular the [[homotopy 2-category]]) of [[combinatorial model categories]] with [[presentable (infinity,1)-categories|presentable $\infty$-categories]] is due to

* {#Pavlov21} [[Dmitri Pavlov]], *Combinatorial model categories are equivalent to presentable quasicategories* ([arXiv:2110.04679](https://arxiv.org/abs/2110.04679))

[^1]: The condition of left properness does not appear in the arXiv version of [Renaudin 2006](#Renaudin06), but is added in the published version. While  [[Dugger's theorem]] (Rem. \ref{LocalPresentationOfCombinatorialModelCategories}) ensures that every combinatorial model category is Quillen equivalent to a left proper one, it is not immediate that every [[zig-zag]] of Quillen equivalences between left proper combinatorial model categories may be taken to pass through only left proper ones.


[[!redirects HoCombModCat]]

[[!redirects 2Ho(CombModCat)]]
