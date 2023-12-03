
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

Let $\kappa$ be a [[regular cardinal]]. Recall an object $X: \mathcal{C}$ is $\kappa$-compact iff $\mathcal{C}(X,-)$ commutes with $\kappa$-filtered colimits.

+-- {: .num_defn }
###### Definition 

A [[locally small category]] $\mathcal{C}$ is **$\kappa$-accessible** if:

1.  the category has $\kappa$-[[directed colimits]] (or, equivalently, $\kappa$-filtered colimits), and

1.  there is a [[set]] of $\kappa$-[[compact objects]] that generate the category under $\kappa$-directed colimits.

Then $\mathcal{C}$ is an **accessible category** if there exists a $\kappa$ such that it is $\kappa$-accessible.

=--

+-- {: .num_remark }
###### Remark

Unlike for [[locally presentable categories]], it does not follow that if $\mathcal{C}$ is $\kappa$-accessible and $\kappa\lt \lambda$ then $\mathcal{C}$ is also $\lambda$-accessible.  It is true, however, that for any accessible category, there are arbitrarily large cardinals $\lambda$ such that $C$ is $\lambda$-accessible.

=--

+-- {: .num_prop }
###### Proposition

Equivalent characterizations include that $C$ is accessible iff:

* it is the category of [[models]] (in [[Set]]) of some small [[sketch]].

* it is of the form $\mathrm{Ind}_\kappa(S)$ for $S$ small, i.e. the $\kappa$-[[ind-object|ind-completion]] of a small category, for some $\kappa$.

* it is of the form $\kappa\,\mathrm{Flat}(S)$ for $S$ small and some $\kappa$, i.e. the category of $\kappa$-[[flat functor|flat]] functors from some small category to $Set$.

* it is the category of models (in $\mathbf{Set}$) of a suitable type of logical theory.

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

If $\mathcal{C}$ is $\lambda$-accessible and $\lambda\unlhd\mu$ (see [[sharply smaller cardinal]]), then $\mathcal{C}$ is $\mu$-accessible.  Thus, any accessible category is $\mu$-accessible for arbitrarily large cardinals $\mu$.

### Stability under various constructions

+-- {: .num_prop}
###### Proposition 

If $\mathcal{C}$ is an accessible category and $K$ is a [[small category]], then the [[functor category]] $Func(K^{op}, \mathcal{C})$ is again accessible.

=--

([Lurie, prop. 5.4.4.3](#Lurie))

+-- {: .num_prop #StabilityUnderInverseImage}
###### Proposition 
**(preservation of accessibility under inverse images)**

Let $F : \mathcal{C} \to \mathcal{D}$ be a [[functor]] between [[locally presentable categories]] which preserves $\kappa$-[[filtered category|filtered]] [[colimits]], and let $\mathcal{D}_0 \subset \mathcal{D}$ be an accessible subcategory. Then the inverse image $f^{-1}(\mathcal{D}_0) \subset C$ is a $\kappa$-accessible subcategory.

=--


This appears as [[Higher Topos Theory|HTT, corollary A.2.6.5]].


+-- {: .num_prop}
###### Proposition 
**(accessibility of fibrations and weak equivalences in a combinatorial model category)**

Let $\mathcal{C}$ be a [[combinatorial model category]], $Arr(\mathcal{C})$ its [[arrow category]], $W \subset Arr(\mathcal{C})$ the [[full subcategory]] on the weak equivalences and $F \subset Arr(\mathcal{C})$ the full subcategory on the fibrations. Then $F$, $W$ and $F \cap W$ are accessible subcategories of $Arr(\mathcal{C})$.

=--

This appears as [[Higher Topos Theory|HTT, corollary A.2.6.6]].


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

[Makkai & Paré (1989)](#MakkaiParé1989) say that this means accessibility is an "almost pure smallness condition."


### Categories of models over a theory

+-- {: .num_prop }
###### Proposition

For a [[category]] $\mathcal{M}$ the following are equivalent:

* $\mathcal{M}$ is finitely [[accessible category|accessible]].

* $\mathcal{M}\simeq \mathbb{T}\text{-}Mod(Set)$ for some [[theory of presheaf type|theory $\mathbb{T}$ of presheaf type]].

=--

Moreover, one has the following result due to [[Christian Lair]]:

+-- {: .num_prop }
###### Proposition

For a [[category]] $\mathcal{M}$ the following are equivalent:

* $\mathcal{M}$ is [[accessible category|accessible]].

* $\mathcal{M}$ is [[sketch|sketchable]].
=--

See also at _[categorical model theory](model+theory#CategoricalModelTheory)_.


### Well-poweredness and well-copoweredness

* Every accessible category $\mathcal{C}$ is [[well-powered category|well-powered]], since it has a small [[dense subcategory]] $\mathcal{A}$, for which the [[restricted Yoneda embedding]] $\mathcal{C} \to [\mathcal{A}^{op},Set]$ is fully faithful and preserves monomorphisms, hence embeds the subobject posets of $\mathcal{C}$ as sub-posets of those of $[\mathcal{A}^{op},Set]$.

* Every accessible category with [[pushouts]] is well-*copowered*.  This is shown in [Adamek-Rosicky, Proposition 1.57 and Theorem 2.49](#AdámekRosický1994).  Whether this is true for all accessible categories depends on what [[large cardinal]] properties hold: by Corollary 6.8 of Adamek-Rosicky, if [[Vopenka's principle]] holds then all accessible categories are well-copowered, while by Example A.19 of Adamek-Rosicky, if all accessible categories are well-copowered then there exist arbitrarily large [[measurable cardinals]].

### The 2-category of accessible categories
 {#TheTwoCategoryOfAccessibleCategories}

Write [[AccCat]] for the [[2-category]] whose

* [[objects]] are [[accessible categories]], 

* [[1-morphisms]] are [[accessible functors]] 

* [[2-morphisms]] are [[natural transformations]].

\begin{proposition}
\label{AccCatHasAllPIELimits}
  The [[2-category]] [[AccCat]] has all (lax) [[2-limits]] and these are [[preserved limit|preserved]] by the inclusion $AccCat \to$ [[Cat]].
\end{proposition}
This appears as [Makkai & Paré (1989), Thm. 5.1.6, Cor. 5.1.8](#MakkaiParé1989), [Adámek & Rosický (1994) around Thm. 2.77](#AdámekRosický1994).

\begin{proposition}
Given a [[cosmos for enrichment]] $\mathcal{V}$ which is ([[symmetric monoidal category|symmetric monoidal]] [[closed monoidal category|closed]] and) [[locally presentable category|locally presentable]], then the [[2-category]] $\mathcal{V}$-[[AccCat]] of $\mathcal{V}$-[[enriched category|enriched]] [[accessible categories]] has all [[PIE 2-limits]] and [[split idempotent|splittings]] of [[idempotent]] [[equivalence in a 2-category|equivalences]] (equivalently it has all [[flexible 2-limits]]), as well as [[2-pullbacks]] along [[isofibrations]].

The analogous statements holds for $\mathcal{V}$-enriched and *[[conical limit|conically]]* accessible categories, in which case the [[forgetful functor]] $\mathcal{V}\text{-}ConAccCat \to \mathcal{V}\text{-}Cat$ [[preserved limit|preserves]] these [[2-limits]].
\end{proposition}
This is [Lack & Tendas (2023), Thm. 5.5, Thm. 5.9](#LackTendas23).

\begin{proposition}
**(directed unions)**
\linebreak
The [[2-category]] [[AccCat]] has [[directed colimits|directed]] [[2-colimits]] of systems of [[fully faithful functors]].  If there is a proper class of [[strongly compact cardinals]], then it has directed colimits of systems of [[faithful functors]].
\end{proposition}

[Paré & Rosický (2013)](#ParéRosický13)


## Examples

- Every small [[discrete category]] is $\kappa$-accessible for every [[regular cardinal]] $\kappa$, since every discrete filtered diagram is trivial.

### Functor categories

See at _[Functor category -- Accessibility](functor+category#LocalPresentability)_.

## Related concepts

* [[class-accessible category]]

[[!include locally presentable categories - table]]



## References 

### General

The term _accessible category_ is due to

* {#MakkaiParé1989} [[Michael Makkai]], [[Robert Paré]],  _Accessible categories: The foundations of categorical model theory_,  Contemporary Mathematics **104**, American Mathematical Society, (1989) &lbrack;[ISBN:978-0-8218-7692-3](https://bookstore.ams.org/conm-104)&rbrack;

Further monographs (with focus on [[locally presentable categories]]):

* {#AdámekRosický1994} [[Jiří Adámek]], [[Jiří Rosický]], *[[Locally presentable and accessible categories]]*, London Mathematical Society Lecture Note Series **189**, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511600579](https://doi.org/10.1017/CBO9780511600579)&rbrack;

See also

* {#ParéRosický13} [[Robert Paré]], [[Jiří Rosický]], *Colimits of accessible categories*, Math. Proc. Cambr. Phil. Soc. **155** (2013) 47-50 &lbrack;[doi:10.1017/S0305004113000030](https://doi.org/10.1017/S0305004113000030), [arXiv:1110.0767](http://arxiv.org/abs/1110.0767)&rbrack;
 

* [[Jiří Adámek]], [[Francis Borceux]], [[Stephen Lack]], [[Jiří Rosický]], _A classification of accessible categories,_ Journal of Pure and Applied Algebra 175:7-30, 2002. [abstract](http://maths.mq.edu.au/~slack/papers/acc.html)

which further stratifies the accessible categories in terms of [[sound doctrines]].


The concept is studied in a 2-categorical setting in

* [[John Bourke]], _Accessible aspects of 2-category theory_ , arXiv:2003.06375 (2020). ([abstract](https://arxiv.org/abs/2003.06375))

A discussion of [[accessible (∞,1)-categories]] is in [section 5.4, p. 341](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=341)
of

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_ 

Some recent developments in the theory of accessible categories can be found in a series of papers on [categorical model theory](model+theory#CategoricalModelTheory) and [[abstract elementary classes]] (many of which also contain some results about arbitrary accessible categories), such as:

* [[Tibor Beke]], [[Jiří Rosický]], *Abstract elementary classes and accessible categories*, 2011, [arxiv](https://arxiv.org/abs/1005.2910)

* Michael Lieberman, [[Jiří Rosický]], Sebastien Vasey, *Internal sizes in μ-abstract elementary classes*, [arxiv](https://arxiv.org/abs/1708.06782)

* Michael Lieberman, [[Jiří Rosický]], Sebastien Vasey , *Set-theoretic aspects of accessible categories*, [arxiv](https://arxiv.org/abs/1902.06777)

See also:

* {#Rezk2021} [[Charles Rezk]], *Generalizing accessible ∞-categories*, 2021 ([pdf](https://faculty.math.illinois.edu/~rezk/accessible-cat-thoughts.pdf))

### In enriched category theory
 {#ReferencesInEnrichedCategoryTheory}

Discussion of accessible [[enriched categories]] (see also [references on enriched locally presentable categories](locally+presentable+category#ReferencesInEnrichedCategoryTheory)):

* [[Francis Borceux]], [[Carmen Quinteriro]], *Enriched accessible categories*, Bull. Austral. Math. Soc. __54__ (1996) 489-501 &lbrack;[doi:10.1017/S0004972700021900](https://doi.org/10.1017/S0004972700021900)&rbrack;

* [[Francis Borceux]], [[Carmen Quinteriro]], [[Jiří Rosický]], *A theory of enriched sketches*, Theory and Applications of Categories, **4** 3 (1998) 47-72 &lbrack;[tac:4-03](http://www.tac.mta.ca/tac/volumes/1998/n3/4-03abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/1998/n3/n3.pdf)&rbrack;

* {#LackTendas23} [[Stephen Lack]], [[Giacomo Tendas]], *Virtual concepts in the theory of accessible categories*, Journal of Pure and Applied Algebra **227** 2 (2023) 107196 &lbrack;[arXiv:10.1016/j.jpaa.2022.107196](https://doi.org/10.1016/j.jpaa.2022.107196), [arXiv:2205.11056](https://arxiv.org/abs/2205.11056)&rbrack;

  > New characterizations of (enriched) accessible categories and introducing the notions of virtual orthogonality and virtual reflectivity. 
 




[[!redirects accessible categories]]

[[!redirects enriched accessible category]]
[[!redirects enriched accessible categories]]


