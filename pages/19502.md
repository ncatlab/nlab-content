
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

+-- {: .num_defn}
###### Definition

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

## Related concepts

* [[bicategory of fractions]]


## References

* {#Renaudin06} Olivier Renaudin, section 1.2 of _Theories homotopiques de Quillen combinatoires et derivateurs de Grothendieck_ ([arXiv:math/0603339](https://arxiv.org/abs/math/0603339))

[[!redirects localizations of a 2-category]]

[[!redirects 2-localization]]
[[!redirects 2-localizations]]

[[!redirects pseudo-localization]]
[[!redirects pseudo-localizations]]

[[!redirects pseudolocalization]]
[[!redirects pseudolocalizations]]

