
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
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

The _Freyd--Mitchell embedding theorem_ says that every [[abelian category]] $\mathcal{A}$ is a [[full subcategory]] of a [[category of modules]] over some [[ring]] $R$, such that the [[fully faithful functor|embedding functor]] $\mathcal{A} \hookrightarrow R Mod$ is an [[exact functor]].

## Details

+-- {: .num_remark}
###### Remark

It is easy to see that not every abelian category is _[[equivalence of categories|equivalent]]_ to $R$[[Mod]] for some [[ring]] $R$.  The reason is that $R Mod$ has all [[small category|small]] [[limits]] and [[colimits]].  But for instance, for $R$ [[noetherian ring|Noetherian]], the category of [[finitely generated module|finitely generated]] $R$-modules is an abelian category but lacks these properties.

=--

However, we have:

\begin{theorem}
\label{MitchellEmbeddingTheorem}
**(Mitchell embedding theorem)**
\linebreak
Every [[small category|small]] [[abelian category]] admits a [[full functor|full]], [[faithful functor|faithful]] and [[exact functor|exact]] functor to the category $R$[[Mod]] for some [[ring]] $R$.
\end{theorem}


This result can be found as Theorem 7.34 on page 150 of ([Freyd](#Freyd)).  (The terminology there is a bit outdated, in that it calls an abelian category "fully abelian" if it admits a full and faithful exact functor to a category of $R$-modules.)  A pedagogical discussion is in section 1.6 of ([Weibel](#Weibel)). See also ([Wikipedia](http://en.wikipedia.org/wiki/Mitchell%27s_embedding_theorem)) for the idea of the proof.

+-- {: .proof #Proof}
###### Proof

(...)

=--


We can also characterize which abelian categories _are_ equivalent to a category of $R$-modules:

+-- {: .num_theorem}
###### Theorem

Let $C$ be an [[abelian category]].  If $C$ has all [[small category|small]] [[coproducts]] and has a [[compact object|compact]] [[projective object|projective]] [[generator]], then $C \simeq R Mod$ for some ring $R$.  

In fact, in this situation we can take $R = C(x,x)^{op}$ where $x$ is any compact projective generator.   Conversely, if $C \simeq R Mod$, then $C$ has all small coproducts and $x = R$ is a compact projective generator.

=--

This theorem, minus the explicit description of $R$, can be found as Exercise F on page 103 of ([Freyd](#Freyd)).
The first part of this theorem can also be found as Prop. 2.1.7 in ([Ginzburg](#Ginzburg)).  Conversely, it is easy to see that $R$ is a compact projective generator of $R Mod$. 


Going further, we can try to characterize functors between categories of $R$-modules that come from tensoring with bimodules.  Here we have

+-- {: .num_theorem}
###### Watts' Theorem

If $B$ is an an $S$-$R$-bimodule, the [[tensor product]] functor

$$  
  B \otimes_R -\colon R Mod \to S Mod 
$$

is [[right exact functor|right exact]] and preserves [[small category|small]] [[coproducts]].  Conversely, if $F\colon Mod_R \to Mod_S$ is right exact and that preserves small coproducts, it is naturally isomorphic to $B \otimes_R -$ where $B$ is the $S$-$R$-bimodule $F R$.  

=--


This theorem was more or less simultaneously proved by Watts and Eilenberg; a generalization is proved in ([Nyman-Smith](#NymanSmith)), and references to the original papers can be found there.


Going still further we should be able to obtain a nice theorem describing the [[image]] of the embedding of the [[2-category]] of

* rings
* bimodules
* bimodule homomorphisms

into the strict 2-category of 

* abelian categories
* right exact functors
* natural transformations.

For more discussion see the [$n$-Cafe](http://golem.ph.utexas.edu/category/2007/08/questions_about_modules.html).

## Related concepts

* [stable model category -- as A-infinity algebroid module categories](stable+model+category#AsCategoriesOfModules)

* [[reconstruction theorem]]

* [[derived category]]

## References

Original articles:

* [[Barry Mitchell]], *The Full Imbedding Theorem*, American Journal of Mathematics **86** 3 (1964) 619-637 &lbrack;[doi:10.2307/2373027](https://doi.org/10.2307/2373027)&rbrack;

Textbook account:

* {#Freyd} [[Peter Freyd]], *Abelian Categories*, Harper and Row (1964), Reprints in Theory and Applications of Categories **3** (2003) 23-164 &lbrack;[tac:tr3](http://www.tac.mta.ca/tac/reprints/articles/3/tr3abs.html)&rbrack;

Details on the proof and its variants are also in

* {#Weibel} [[Charles Weibel]], section 1.6 of: _[[An Introduction to Homological Algebra]]_
 
and

* {#Ginzburg} [[Victor Ginzburg]], _Lectures on noncommutative geometry_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf))
 

* {#NymanSmith} A. Nyman , S. Paul Smith, _A generalization of Watts's Theorem: Right exact functors on module categories_ ([arXiv:0806.0832](http://arxiv.org/abs/0806.0832))
 

An introductory survey is for instance also in section 3 of 

* Geillan Aly, _Abelian Categories and the Freyd-Mitchell Embedding Theorem_ ([pdf](http://www.u.arizona.edu/~geillan/research/ab_categories.pdf))

See also

* Wikipedia, _[Mitchell's embedding theorem](http://en.wikipedia.org/wiki/Mitchell%27s_embedding_theorem)_

[[!redirects Freyd-Mitchell embedding theorem]]
[[!redirects Freyd–Mitchell embedding theorem]]
[[!redirects Freyd--Mitchell embedding theorem]]
[[!redirects Freyd-Mitchell embedding]]
[[!redirects Freyd–Mitchell embedding]]
[[!redirects Freyd--Mitchell embedding]]
[[!redirects Freyd-Mitchell theorem]]
[[!redirects Freyd–Mitchell theorem]]
[[!redirects Freyd--Mitchell theorem]]

[[!redirects Mitchell theorem]]
[[!redirects Mitchell's theorem]]
[[!redirects Mitchell's theorem]]

[[!redirects Watt's theorem]]
[[!redirects Watt theorem]]

[[!redirects Mitchell embedding theorem]]
