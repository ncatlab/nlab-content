
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The notion of _enriched $(\infty,1)$-category_ is the generalization of the notion of _[[enriched category]]_ from [[category theory]] to [[(∞,1)-category theory]]. For $\mathcal{V}$ a [[monoidal (∞,1)-category]], a _$\mathcal{V}$-enriched $(\infty,1)$-category_ $C$ is 

* a [[set]]/[[class]] of [[objects]] $Obj(C)$;

* for every tuple $(a \in C,b \in C)$ an object $C(a,b) \in \mathcal{V}$ "of [[morphisms]]" from $a$ to $b$ in $C$;

* for each sequence $(a_i \in C)_{i = 0}^n$ of objects in $C$ an object $C(a_0, \cdots, a_n) \in \mathcal{V}$ "of sequences of composable morphisms _and_ their composites";

* such that these composites exist essentially uniquely and satisfy [[associativity]] in a [[coherence|coherent]] fashion.

One way to make this precise in a general abstract way should be to define $C$ to be a [[∞-algebra over an (∞,1)-operad]] in $\mathcal{V}^{\otimes}$ over [[Assoc]]${}_{Obj(C)}$, the $Obj(C)$-colored version of the [[associative operad]];

$$
  C \in Alg_{Assoc_{Obj(C)}}(\mathcal{V}^\otimes)
  \,.
$$

For $\mathcal{V} \in$ [[∞Grpd]], this should be [[equivalence of (∞,1)-categories|equivalent]] to ordinary [[(∞,1)-categories]]. This is for instance in ([Lurie, def. 4.2.1.12](#Lurie)).

A construction that should be a model for this notion in terms of a [[model category]] presentation for $\mathcal{V}$ is discussed in ([Simpson](#Simpson)). For the case that $\mathcal{V} = $ [[∞Grpd]] [[presentable (∞,1)-category|presented]] by the standard [[model structure on simplicial sets]] this reproduces the notion of _[[Segal categories]]_. (See there for further details and references.) The iteration of this construction yields [[Segal n-categories]], a model for [[(∞,n)-categories]].

Once a model category $V$ for $\mathcal{V}$ has been chosen, one can consider [[semi-strict infinity-category|semi-strict]] $\infty$-enrichments given by ordinary $V$-[[enriched categories]] equipped with a notion of weak equivalence that remembers that these are presentations for enriched $(\infty,1)$-categories. See also _[[enriched homotopical category]]_. 

## Examples
 {#Examples}

A [[stable (∞,1)-category]] is naturally enriched in the [[(∞,1)-category of spectra]].

More generally, for $R$ an [[E-∞ ring]] then an $R$-[[linear (∞,1)-category]] is naturally enriched in $R$-[[∞-modules]]. (This includes the previous case for $R$ the [[sphere spectrum]].)

A [[closed monoidal (∞,1)-category]] is naturally enriched over itself.

([Gepner-Haugseng 13](#GepnerHaugseng13))


## Related concepts

* [[enriched (∞,1)-functor]]

* [[Segal category]], [[Segal n-category]]

* [[enriched homotopical category]], [[weak enrichment]]

* [[internal category in an (∞,1)-category]]

* [[table - models for (∞,1)-operads]]

## References

* [[Carlos Simpson]], _[[Homotopy Theory of Higher Categories]]_ ([arXiv:1001.4071](http://arxiv.org/abs/1001.4071))
 {#Simpson}

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}

* {#GepnerHaugseng13} [[David Gepner]], [[Rune Haugseng]], _Enriched ∞-categories via non-symmetric ∞-operads_ ([arXiv:1312.3178](http://arxiv.org/abs/1312.3178))

* Hadrian Heine, _An equivalence between enriched ∞-categories and ∞-categories with weak action_, [arxiv](https://arxiv.org/abs/2009.02428), 2020

* [[John D. Berman]], *Enriched infinity categories I: enriched presheaves* ([arXiv:2008.11323](https://arxiv.org/abs/2008.11323))


Further discussion of [[(infinity,n)-categories]] as $\infty$-categories enriched in $(\infty,n-1)$-categories is (via [[Theta-spaces]]) in

* {#BergnerRezk} [[Julie Bergner]], [[Charles Rezk]], _Comparison of models for $(\infty,n)$-categories_, I ([arXiv:1204.2013](http://arxiv.org/abs/1204.2013))
 
* {#BergnerRezk14} [[Julie Bergner]], [[Charles Rezk]], _Comparison of models for $(\infty,n)$-categories_, II ([arXiv:1406.4182](http://arxiv.org/abs/1406.4182))

See also

* {#Haugseng15} [[Rune Haugseng]], _Bimodules and natural transformations for enriched ∞-categories_ ([arXiv:1506.07341](http://arxiv.org/abs/1506.07341))

[[!redirects enriched (∞,1)-category]]
[[!redirects enriched (∞,1)-categories]]

[[!redirects enriched (infinity,1)-categories]]