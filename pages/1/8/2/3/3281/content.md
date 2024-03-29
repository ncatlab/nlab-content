
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Stable homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _stable model category_ is a 1-[[category]] structure used to present a [[stable (∞,1)-category]] in analogy to how a general [[model category]] encodes a (generally non-stable) [[(∞,1)-category]].


## Defintion

A **stable model category** $\mathcal{C}$ is

* a [[pointed model category]]

* such that the [[loop space object]] functor $\Omega$ and the [[suspension object]] functor $\Sigma$, are inverse [[equivalence of categories|equivalences]] on the [[homotopy category of a model category|homotopy category]] $Ho(C)$:

  $$ 
    \Omega 
    \colon 
    Ho(\mathcal{C}) 
     \stackrel{\overset{\simeq}{\longleftarrow}}{\underset{\simeq}{\longrightarrow}}  
   Ho(\mathcal{C}) 
   \colon 
  \Sigma
   \,.
  $$

## Properties

### Triangulated homotopy category

The [[homotopy category of a model category|homotopy category]] $Ho(\mathcal{C})$ of a stable model category, equipped with the [[reduced suspension]] functor $\Sigma \colon Ho(\mathcal{C})\overset{\simeq}{\to} Ho(\mathcal{C})$ is a [[triangulated category]] ([Hovey 99, section 7](#Hovey99)).


### Relation to stable $\infty$-categories

Stabilization of model categories is a model for the abstractly defined [[stabilization]] in [[(infinity,1)-category theory]] ([Robalo 12, prop. 4.15](#Robalo12)).


### As $A_\infty$-algebroid module categories
 {#AsCategoriesOfModules}


+-- {: .num_prop #ModuleProp}
###### Proposition

Let $\mathcal{C}$ be a _stable model category_ that is in addition

* a [[simplicial model category]];

* a [[cofibrantly generated model category]];
* a [[proper model category]];

* with a [[set]] $S$ of [[compact object|compact]] generators;

then there is a chain of [[simplicial Quillen adjunction|sSet-enriched]] [[Quillen equivalences]]  linking $\mathcal{C}$ to the the [[spectrum]]-[[enriched functor category]] 

$$
  \mathcal{C} \simeq_Q A_S Mod \coloneqq Sp Cat(A_S, Sp)
$$

equipped with the [[global model structure on functors]],
where $A_S$ is the $Sp$-[[enriched category]] whose set of objects is $S$

=--

This is  in ([Schwede-Shipley, theorem 3.3.3](#SchwedeShipley))

+-- {: .num_remark}
###### Remark

An $Sp$-enriched category is a homotopy-theoretic analog of an [[Ab-enriched category]], which may be thought of as a many-object version of a [[ring]], a "[[ringoid]]". Accordingly, an $Sp$-enriched category is an $A_\infty$-ringoid. It is has a single object then (as a pointed category) it is an [[A-infinity algebra]].

=--

Hence:

+-- {: .num_cor}
###### Corollary

If if in prop. \ref{ModuleProp} there is just one compact generator $P \in \mathcal{C}$, then there is a one-object $Sp$-enriched category, hence an [[A-infinity algebra]] $A$, which is the [[endomorphisms]] $A \simeq End_{\mathcal{C}}(P)$, and the stable model category is its [[category of modules]]:

$$
  \mathcal{C} \simeq_Q A Mod
  \,.
$$



=--

This is  in ([Schwede-Shipley, theorem 3.1.1](#SchwedeShipley))

+-- {: .num_remark}
###### Remark

This may be thought of as a homotopy-theoretic analog of the [[Freyd-Mitchell embedding theorem]] for [[abelian categories]].

=--

+-- {: .num_remark}
###### Remark

One way to read this is that [[formal duals]] of presentable [[stable infinity-categories]] are a model for [[spaces]] in ("[[derived noncommutative geometry|derived]]") [[noncommutative geometry]].

=--


If $A$ is an [[Eilenberg-MacLane spectrum]], then this identifies the corresponding stable model categories with the [[model structure on unbounded chain complexes]].

This is ([Schwede-Shipley 03, theorem 5.1.6](#SchwedeShipley03)).


## Related concepts

* [[linear model category]]



## References

The concept originates with

* {#Hovey99} [[Mark Hovey]], section 7 of _Model Categories_ Mathematical Surveys and Monographs, Volume 63, AMS (1999) ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/hovey-model-cats.pdf), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover))


The classification theorems are due to

* {#SchwedeShipley03} [[Stefan Schwede]], [[Brooke Shipley]], _Classification of stable model categories_ or _Stable model categories are categories of modules_, Topology 42 (2003) 103-153 ([arXiv:0108143](http://arxiv.org/abs/math/0108143))
 

Discussion of the notion of stable model categories with the abstract notion of [[stabilization]] in [[(infinity,1)-category theory]] is in section 4.2 (prop. 4.15) of

* {#Robalo12} [[Marco Robalo]], _Noncommutative Motives I: A Universal Characterization of the Motivic Stable Homotopy Theory of Schemes_, June 2012 ([arxiv:1206.3645](http://arxiv.org/abs/1206.3645))

On ([[monoidal localization|monoidal]]) [[Bousfield localization of model categories|Bousfield localization]] of stable model categories:

* [[Luca Pol]], [[Jordan Williamson]], *The Left Localization Principle, completions, and cofree $G$-spectra*, J. Pure Appl. Algebra **224** 11 (2020) 106408 &lbrack;[arXiv:1910.01410](https://arxiv.org/abs/1910.01410), [doi:10.1016/j.jpaa.2020.106408](https://doi.org/10.1016/j.jpaa.2020.106408)&rbrack;

  

[[!redirects stable model categories]]