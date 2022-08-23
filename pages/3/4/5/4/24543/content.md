
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc} 

## Idea 

A **sind-object** of a [[category]] $\mathcal{C}$ is a **formal [[sifted colimit]]** of objects of $\mathcal{C}$.  Here "formal" means that the colimit is taken in the [[category of presheaves]] of $\mathcal{C}$ (the [[free cocompletion]] of $\mathcal{C}$). The category of sind-objects of $\mathcal{C}$ is written $sind$-$\mathcal{C}$ or $SInd(\mathcal{C})$. It is the sifted colimit completion of $\mathcal{C}$.

There is an analogy here with [[ind-objects]], which are formal filtered colimits, and where the category of ind-objects $Ind(\mathcal{C})$ is the filtered colimit completion of $\mathcal{C}$.

Typically the main case of interest here is the situation where $\mathcal{C}$ is small with finite coproducts. If a small category $\mathcal{C}$ has finite coproducts, the sifted colimit completion comprises the finite-product-preserving presheaves: 

 $$Sind(\mathcal{C})\cong FP(\mathcal{C}^{op},Set)$$ 

The analogy here is that if a small category $\mathcal{C}$ has finite [[colimits]], the filtered colimit completion comprises the finite limit preserving presheaves: 

 $$Ind(\mathcal{C})\cong Lex(\mathcal{C}^{op},Set)$$ 

One reason this is often relevant because if $\mathcal{C}^\op$ has finite [[products]], it can be regarded as an [[algebraic theory]], and then the sifted colimit completion comprises the category of models of the theory. 

Another point of relevance is that this is a canonical way of building a [[cartesian closed category]] out of a [[distributive category]]. 

## Definition

If $\mathcal{C}$ has finite coproducts then consider the category of finite product preserving functors 

$$Sind(\mathcal{C})\cong  FP(\mathcal{C}^{op},Set)$$

The representable objects always preserves finite products, and so the Yoneda embedding $\mathcal{C}\to [\mathcal{C}^{op},Set]$ factors through $Sind(\mathcal{C})$. This exhibits $Sind(\mathcal{C})$ as the free sifted colimit completion of $\mathcal{C}$. 

+-- {: .num_prop}
###### Proposition


If $\mathcal{D}$ is has sifted colimits then the Yoneda embedding induces a natural bijection between functors $\mathcal{C}\to \mathcal{D}$ and sifted-colimit-preserving functors $Sind(\mathcal{C})\to \mathcal{D}$. 

=--

The construction has another universal property, as the free colimit completion of a category respecting the existing finite coproducts. 

+-- {: .num_prop}
###### Proposition


If $\mathcal{D}$ is has colimits then the Yoneda embedding induces a natural bijection between finite-coproduct-preserving functors $\mathcal{C}\to \mathcal{D}$ and colimit-preserving-functors $Sind(\mathcal{C})\to \mathcal{D}$. 

=--

## Distributive categories and cartesian closure

The sifted-colimit-completion also gives a way of [[full and faithful|full and faithfully]] embedding a [[distributive category]] in a [[cartesian closed]] category, while preserving the structure. From a type-theoretic perspective, this shows that function types are a conservative extension of finite type theory. 

+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be a small category with finite coproducts and products. The following are equivalent. 

* $\mathcal{C}$ is a [[distributive category]]. 

* $Sind(\mathcal{C})$ is [[cartesian closed]]. 

=--

## References

*  {#AdamekRosickyVitale10} [[Jiri Adamek]], [[Jiri Rosicky]], [[Enrico Vitale]], _What are sifted colimits?_, TAC **23** (2010) pp. 251&#8211;260. ([web](http://www.tac.mta.ca/tac/volumes/23/13/23-13abs.html)) 

* {#AdamekRosicky01}[[Jiri Adamek]], [[Jiri Rosicky]], _On sifted colimits and generalized varieties_, TAC **8** (2001) pp 33&#8211;53. ([web](http://www.tac.mta.ca/tac/volumes/8/n3/8-03abs.html))

The idea of product-preserving-functors as a cartesian closed category is in various sources, including:

* [[Marcelo Fiore]], "Enrichment and representation theorems for categories of domains and partial functions". 1996. [web](http://www.cl.cam.ac.uk/~mpf23/papers/ADT/rep.ps.gz). 

* [[John Power]], "Generic models for computational effects",  Theor. Comput. Sci. 364(2): 254-269 (2006)

* Younesse Kaddar, "Ideal distributors", Section 1. 2020. [report](https://younesse.net/assets/ARPE_report.pdf).