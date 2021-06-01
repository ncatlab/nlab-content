
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea 

An accessible [[category]] is a possibly [[large category]] which is however essentially determined by a [[small category]], in a certain way.  

## Definition 

+-- {: .num_defn }
###### Definition 

A [[locally small category]] $C$ is **$\kappa$-accessible** for a [[regular cardinal]] $\kappa$ if:

1.  the category has $\kappa$-[[directed colimits]] (or, equivalently, $\kappa$-filtered colimits), and

1.  there is a [[set]] of $\kappa$-[[compact objects]] that generate the category under $\kappa$-directed colimits.

Then $C$ is an **accessible category** if there exists a $\kappa$ such that it is $\kappa$-accessible.

=--

+-- {: .num_remark }
###### Remark

Unlike for [[locally presentable categories]], it does not follow that if $C$ is $\kappa$-accessible and $\kappa\lt \lambda$ then $C$ is also $\lambda$-accessible.  It is true, however, that for any accessible category, there are arbitrarily large cardinals $\lambda$ such that $C$ is $\lambda$-accessible.

=--

+-- {: .num_prop }
###### Proposition

Equivalent characterizations include that $C$ is accessible iff:

* it is the category of [[models]] (in [[Set]]) of some small [[sketch]].

* it is of the form $Ind_\kappa(S)$ for $S$ small, i.e. the $\kappa$-[[ind-object|ind-completion]] of a small category, for some $\kappa$.

* it is of the form $\kappa\,Flat(S)$ for $S$ small and some $\kappa$, i.e. the category of $\kappa$-[[flat functor|flat]] functors from some small category to $Set$.

* it is the category of models (in $Set$) of a suitable type of logical theory.

=--

The relevant notion of [[functor]] between accessible categories is 

+-- {: .num_defn }
###### Definition 

A [[functor]] $F\colon C\to D$ between accessible categories is 
an **[[accessible functor]]**  if there exists a $\kappa$ such that $C$ and $D$ are both $\kappa$-accessible and $F$ preserves $\kappa$-[[filtered colimits]].

=--

## Properties 
 {#Properties}

### Raising the index of accessibility

If $C$ is $\lambda$-accessible and $\lambda\unlhd\mu$ (see [[sharply smaller cardinal]]), then $C$ is $\mu$-accessible.  Thus, any accessible category is $\mu$-accessible for arbitrarily large cardinals $\mu$.

### Stability under various constructions

+-- {: .num_prop}
###### Proposition 

If $\mathcal{C}$ is an accessible category and $K$ is a [[small category]], then the [[category of presheaves]] $Func(K^{op}, \mathcal{C})$ is again accessible.

=--

([Lurie, prop. 5.4.4.3](#Lurie))

+-- {: .num_prop #StabilityUnderInverseImage}
###### Proposition 
**(preservation of accessibility under inverse images)**

Let $F : C \to D$ be a [[functor]] between [[locally presentable categories]] which preserves $\kappa$-[[filtered category|filtered]] [[colimits]], and let $D_0 \subset D$ be an accessible subcategory. Then the inverse image $f^{-1}(D_0) \subset C$ is a $\kappa$-accessible subcategory.

=--


This appears as [[Higher Topos Theory|HTT, corollary A.2.6.5]].



+-- {: .num_prop}
###### Proposition 
**(accessibility of fibrations and weak equivalences in a combinatorial model category)**

Let $C$ be a [[combinatorial model category]], $Arr(C)$ its [[arrow category]], $W \subset Arr(C)$ the [[full subcategory]] on the weak equivalences and $F \subset Arr(C)$ the full subcategory on the fibrations. Then $F$, $W$ and $F \cap W$ are accessible subcategories of $Arr(C)$.

=--

This appears as [[Higher Topos Theory|HTT, corollary A.2.6.6]].



+-- {: .num_prop #Limits}
###### Proposition 
**(closure under limits)**

The [[2-category]] $Acc$ of accessible categories, accessible functors, and natural transformations has all small [[2-limits]].

=--

This can be found in [Makkai-Par&#233;](#MakkaiPare).  Some special cases are proven in [Ad&#225;mek-Rosick&#253;](#AdamekRosicky).



+-- {: .num_prop}
###### Proposition 
**(directed unions)**

The [[2-category]] $Acc$ has [[directed colimits]] of systems of [[fully faithful functors]].  If there is a proper class of [[strongly compact cardinals]], then it has directed colimits of systems of [[faithful functors]].

=--

See ([Par&#233;-Rosick&#253;](#Par&#233;Rosick&#253;)).

### Adjoint functor theorem

+-- {: .num_prop}
###### Proposition 
**(adjoint functors)**

Every accessible functor satisfies the [[solution set condition]], and every left or right adjoint between accessible categories is accessible.  Therefore, the [[adjoint functor theorem]] takes an especially pleasing form for accessible categories that are complete and cocomplete (i.e. are [[locally presentable categories|locally presentable]]): a functor between such categories is a left (resp. right) adjoint iff it is accessible and preserves all small colimits (resp. limits).

=--

### Idempotence completeness

+-- {: .num_prop}
###### Proposition 

A [[small category]] is accessible precisely when it is [[idempotent complete category|idempotent complete]].  

=--

[Makkai-Par&#233;](#MakkaiPare) say that this means accessibility is an "almost pure smallness condition."


### Categories of models over a theory

+-- {: .num_prop }
###### Proposition

For a [[category]] $\mathcal{M}$ the following are equivalent:

* $\mathcal{M}$ is finitely [[accessible category|accessible]].

* $\mathcal{M}\simeq \mathbb{T}\text{-}Mod(Set)$ for some [[theory of presheaf type|theory $\mathbb{T}$ of presheaf type]].

=--

Moreover, one has the following result due to Christian Lair:

+-- {: .num_prop }
###### Proposition

For a [[category]] $\mathcal{M}$ the following are equivalent:

* $\mathcal{M}$ is [[accessible category|accessible]].

* $\mathcal{M}$ is [[sketch|sketchable]].
=--

See also at _[categorical model theory](model+theory#CategoricalModelTheory)_.


### Well-poweredness and well-copoweredness

* Every accessible category $C$ is [[well-powered category|well-powered]], since it has a small [[dense subcategory]] $A$, for which the [[restricted Yoneda embedding]] $C\to [A^{op},Set]$ is fully faithful and preserves monomorphisms, hence embeds the subobject posets of $C$ as sub-posets of those of $[A^{op},Set]$.

* Every accessible category with [[pushouts]] is well-*copowered*.  This is shown in [Adamek-Rosicky, Proposition 1.57 and Theorem 2.49](#AdamekRosicky).  Whether this is true for all accessible categories depends on what [[large cardinal]] properties hold: by Corollary 6.8 of Adamek-Rosicky, if [[Vopenka's principle]] holds then all accessible categories are well-copowered, while by Example A.19 of Adamek-Rosicky, if all accessible categories are well-copowered then there exist arbitrarily large [[measurable cardinals]].


## Examples

### Functor categories

See at _[Functor category -- Accessibility](functor+category#LocalPresentability)_.

## Related concepts

* [[class-accessible category]]

[[!include locally presentable categories - table]]



## References 

The term _accessible category_ is due to

* {#MakkaiPare89}  [[Michael Makkai]], [[Robert Paré]], _Accessible categories: The foundations of categorical model theory_ Contemporary Mathematics 104. American Mathematical Society, Rhode Island, 1989.1989. 
{#MakkaiPare}

The standard textbook on the theory of accessible categories is

* [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 {#AdamekRosicky}

See also

* [[Robert Paré]], [[Jiří Rosický]], _Colimits of accessible categories_ ([arXiv:1110.0767](http://arxiv.org/abs/1110.0767))
 {#Par&#233;Rosick&#253;}

and 

* [[Jiří Adámek]], [[Francis Borceux]], [[Stephen Lack]], [[Jiří Rosický]], _A classification of accessible categories,_ Journal of Pure and Applied Algebra 175:7-30, 2002. [abstract](http://maths.mq.edu.au/~slack/papers/acc.html)

which further stratifies the accessible categories in terms of [[sound doctrines]].

The concept is studied in a 2-categorical setting in

* [[John Bourke]], _Accessible aspects of 2-category theory_ , arXiv:2003.06375 (2020). ([abstract](https://arxiv.org/abs/2003.06375))

A discussion of [[accessible (∞,1)-categories]] is in [section 5.4, p. 341](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=341)
of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

Some recent developments in the theory of accessible categories can be found in a series of papers on [categorical model theory](model+theory#CategoricalModelTheory) and [[abstract elementary classes]] (many of which also contain some results about arbitrary accessible categories), such as:

* [[Tibor Beke]], [[Jiří Rosický]], *Abstract elementary classes and accessible categories*, 2011, [arxiv](https://arxiv.org/abs/1005.2910)

* Michael Lieberman, Jiří Rosický, Sebastien Vasey, *Internal sizes in μ-abstract elementary classes*, [arxiv](https://arxiv.org/abs/1708.06782)

* Michael Lieberman, Jiří Rosický, Sebastien Vasey , *Set-theoretic aspects of accessible categories*, [arxiv](https://arxiv.org/abs/1902.06777)



[[!redirects accessible categories]]